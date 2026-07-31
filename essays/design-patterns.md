---
layout: essay
type: essay
title: "Patterns: The Art of Not Reinventing the Wheel"
date: 2026-07-30
published: true
labels:
  - ICS 314
  - Learning
  - Software Architecture
  - Design Patterns
---

## Introduction

Imagine this for a second: You’re interviewing for a position as a software developer, sitting across from a senior developer, taking a slow sip of water, when they hit you with a deceptively simple architectural question: "What are design patterns?" Naturally, this is immediately followed by its inevitable follow-up: "And what design patterns have you actually used in your own projects?"  

It’s a classic developer pop quiz, and a great way to understand both your grasp of fundamental software design concepts and your ability to implement them. If you spit out a dry, textbook definition, you'll sound like ChatGPT when it first launched. If you say, "I used a Singleton once because a tutorial told me to," you risk sounding like you’re just throwing stuff at the wall until something works for you. The reality is that design patterns aren't some magic spell or some holy text—they're just battle-tested architectural blueprints crafted by developers who got tired of solving the exact same structural problems from scratch.  

## Architectural Blueprints

<img src="../img/design-patterns/blueprint.jpg" width="400" alt="A picture of a blueprint.">  
<caption><small>
  Figure 1: A picture of a blueprint.<br>
  <em>Source: <a href="https://stock.adobe.com/search?k=blueprint&asset_id=101655538" target="_blank">Adobe Stock</a></em>
</small></caption>  
<br>

To understand what design patterns actually are, let's imagine you're an architect designing a new gym. You don't need to invent lockers, nor do you need to calculate how a load-bearing column supports a second-floor weight room from scratch. Architects before you have already solved these structural problems. They've documented the blueprints, safety thresholds, and configurations needed to make all those components work reliably.  

In software engineering, design patterns are those exact architectural blueprints. A design pattern isn't a pre-written snippet of code that you can copy and paste into your project like a library or a Bootstrap class. Instead, it's a high-level, reusable solution to a recurring architectural problem in software design. It gives developers a shared vocabulary and a proven structural framework so they don't have to reinvent the wheel every time they write new features.  

These blueprints generally fall into three main categories:

* <b>Creational Patterns:</b> Blueprints focused on object creation mechanisms, ensuring objects are instantiated in a controlled manner (e.g., <em>Singleton, Factory</em>).
* <b>Structural Patterns:</b> Blueprints for assembling classes and objects into larger, flexible structures (e.g., <em>Adapter, Decorator, Composite</em>).
* <b>Behavioral Patterns:</b> Blueprints that manage communication, algorithms, and responsibility delegation between objects (e.g., <em>Observer, State, Strategy</em>).

## Chaotic Coupling vs. Elegant Patterns

<img src="../img/design-patterns/elegant-pattern.avif" width="400" alt="A picture of an elegant pattern.">  
<caption><small>
  Figure 2: A picture of an elegant pattern.<br>
  <em>Source: <a href="https://www.magnific.com/free-vector/abstract-background-with-elegant-pattern_10852064.htm#fromView=keyword&page=1&position=1&uuid=7744b8ea-18bd-4dcb-949c-28daf5e01438&query=Elegant+pattern" target="_blank">Magnific</a></em>
</small></caption>  
<br>

Let's move to some more concrete examples. Let's say you're building a feature where updating a user's fitness profile needs to update a navigation bar, trigger a notification, and log an activity event. Without a clear design pattern, you might end up tightly coupling all of those operations directly inside a single update function:
```typescript
function updateUserProfile(user: User, newLevel: number) {
    user.level = newLevel;
    
    NavbarComponent.refreshUserBadge(user);
    NotificationSystem.sendAlert(user, "Level Up!");
    AnalyticsLogger.logEvent("level_change", user.id);
}
```
This works fine until you add a fourth or fifth component that also needs to listen for user updates, or until one subsystem fails and breaks the entire program.  

This is where the Observer Pattern comes into play. Instead of ``updateUserProfile()`` knowing about every component in your app, components just "subscribe" to status events. When a change happens, the system broadcasts the update to anyone listening.
```typescript
class UserStatusSubject {
    private observers: Observer[] = [];

    public subscribe(observer: Observer): void {
        this.observers.push(observer);
    }

    public notify(user: User): void {
        this.observers.forEach(observer => observer.update(user));
    }
}
```
Now, your core logic doesn't care who is listening or how many subscribers exist. The components are cleanly isolated, easier to test, and effortless to expand.  

## Practicing Pattern Recognition at the Rainbow Gym

<img src="../img/design-patterns/rainbow-gyms.png" width="400" alt="The Rainbow Gyms Logo.">  
<caption><small>
  Figure 3: The Rainbow Gymms Logo<br>
  <em>Source: <a href="https://github.com/rainbow-gyms" target="_blank">Rainbow Gyms</a></em>
</small></caption>  
<br>

Talking about theoretical patterns is easy, but applying them in a project is quite literally where theory meets reality. For our final project, my team is building [Rainbow Gyms](https://github.com/rainbow-gyms/rainbow-gyms-nextjs)—a gym session scheduling web app tailored for University of Hawaiʻi students. The goal of Rainbow Gyms is to help students balance academic workloads with personal fitness goals by enabling them to create workout sessions, browse filtered activities by location or workout type, and level up their profiles through community participation.  

We didn't start the project with a rigid checklist forcing patterns into places they didn't belong. Instead, as our codebase expanded, design patterns just kinda naturally emerged out of necessity to keep our application clean, secure, and scalable.  

Here are two primary design patterns we utilized in Rainbow Gyms:

### 1. The Singleton Pattern (Database Client Management)

In Next.js server-side rendering, routes and server actions frequently need to query the database. During development, fast-refresh re-executes code modules repeatedly. If every route file instantiates its own database client connection, you quickly exhaust connection limits and flood server resources.  

To solve this, we used the Singleton pattern through our Prisma database client. The Singleton pattern ensures that a class or client has only one centralized instance across the application lifecycle while providing a global point of access to it.
```typescript
import { prisma } from "@/lib/prisma";
```
In server components like our session page or our profile verification handler, we import this single, shared instance to execute database queries:
```typescript
const profile = await prisma.profile.findUnique({
  where: {
    userId: Number(session.user.id),
  },
});
```
By relying on a single database client instance across server routes, we maintain a stable connection pool and keep database access performant across the entire application.  

### 2. The Guard Pattern / Authorization Interceptor

<img src="../img/design-patterns/security-guard.png" width="400" alt="A Security Guard.">  
<caption><small>
  Figure 4: A Security Guard.<br>
  <em>Source: <a href="https://eliteguard.com/category/security-guards/" target="_blank">Elite Guard</a></em>
</small></caption>  
<br>

Across Rainbow Gyms, we have pages that shouldn't be accessible to just anyone floating around the web—like the session creation page or a user's private workout schedule. Instead of letting an unauthenticated request render a half-broken UI or crash midway through rendering, we put a bouncer at the door using the Guard Pattern (or Authorization Interceptor). A Guard sits right at the very top of our server-side route components, evaluating prerequisites like user authentication and profile setup before handing off control to the page UI.  

Here's how we set up this bouncer in our route for creating a new gym session:
```typescript
export default async function Create() {
  // 1. Authentication Guard: Redirect if user is unauthenticated
  const session = await auth();

  if (!session?.user?.id) {
    redirect("/auth/signin");
  }

  // 2. Profile Existence Guard: Redirect if profile setup is incomplete
  const profile = await prisma.profile.findUnique({
    where: {
      userId: Number(session.user.id),
    },
  });

  if (!profile) {
    redirect("/profile/setup");
  }

  // 3. Execution: Render the creation form once guards pass
  return <CreateForm />;
}
```
By placing these guard conditions right at the entry point of our protected server routes, we cleanly decouple security and access verification from the core UI rendering logic found in client components like CreateForm. It keeps our authorization logic centralized at the door and prevents our UI components from becoming bloated with redundant auth checks.  

## The Dark Side of Over-Engineering

#Much like my experience working with UI frameworks where slathering a dozen utility classes onto a single element creates ugly, cluttered code, design patterns carry their own major pitfall: over-engineering. In software development, there's a well-known trap called "patternitis"—the irresistible urge to force complex patterns onto simple problems where a direct solution is infinitely cleaner.  

Take our CreateForm component, for instance. It’s a standard form with six inputs allowing students to set up a workout session with a name, workout type, location, start time, group size, and any other additional info. We could have over-engineered this form by wrapping every single input field inside an abstract ``InputHandlerFactoryStrategy`` pattern. But why make life difficult? React's built-in ``useState`` hook handles state updates cleanly and predictably in just a few lines of code.  

## Conclusion

When an interviewer asks you about design patterns, they aren't looking for a memorized textbook dump. They want to see if you understand software architecture, maintainability, and how to structure applications efficiently.  

Design patterns aren't rigid rules etched in stone. They're practical tools in your developer kit—blueprints you can rely on when your application's architecture starts growing. Whether it’s using a Singleton to manage Prisma database connections cleanly or applying Guard patterns to protect user session routes in your website, mastering these blueprints allows you to write cleaner code without constantly reinventing the wheel.

<hr>

<i>This essay was grammar checked using Google Gemini.</i>  
<i>All images belong to their respective copyright holders.</i>