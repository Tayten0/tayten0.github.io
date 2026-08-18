---
layout: essay
type: essay
title: "Not All Software Engineering is Web Development, but All Web Development is Software Engineering"
# All dates must be YYYY-MM-DD format!
date: 2026-08-17
published: true
labels:
  - ICS 314
  - Learning
  - Software Engineering
---

## Introduction

> "Programs must be written for people to read, and only incidentally for machines to execute."  
> — Harold Abelson  
> <em>Structure and Interpretation of Computer Programs</em> (1984)[^1]

If you had looked over my shoulder for the past few months, you’d probably assume I was training to be a full-time web developer. I’ve spent hours staring at terminal errors, tweaking user interfaces, and trying to get databases to work with my front-end code without blowing up. Because the technology stack for this class was built entirely around web applications, I wouldn't blame you if you thought ICS 314 was just "The Web Dev Class."

However, in my very first essay, I described software engineering as a vehicle, not a destination. If you actually take a step back and look at the bigger picture, you'll realize that web applications are just that: a vehicle. The web stack was just a shiny, modern playground designed to trick us into learning the real meat and potatoes of the course: fundamental software engineering. Software engineering isn't just about knowing how to write code; it's about knowing how to write code well, how to organize it, and how to work with others to actually get a product out the door. To prove my point, let’s take a look at three core concepts I learned this semester and explore how they stretch far beyond the boundaries of a web browser.

## The Real Meat of Software Engineering

If you're like me from a few months ago, terms like "Agile" or "Design Patterns" probably sound like corporate buzzwords invented by managers to make meetings longer. But as it turns out, they are the backbone of any successful project. 

### Agile Project Management (Issue Driven Project Management)

<img src="../img/software-engineering/to-do.jpg" width="400" alt="A To-Do List.">  
<caption><small>
  Figure 1: A To-Do List.<br>
  <em>Source: <a href="https://www.vecteezy.com/vector-art/26162009-to-do-list-icon-with-hand-drawn-text-checklist-task-list-vector-illustration-in-flat-style-on-white-background" target="_blank" referrerpolicy="no-referrer">Vecteezy</a></em>
</small></caption>  
<br>
  
Let's start with Agile Project Management. To put it simply, Agile is a project management philosophy that prioritizes flexibility, collaboration, and continuous improvement over rigid, set-in-stone planning. Instead of trying to build an entire software system in one massive, stressful push, you break the project down into bite-sized chunks and work in short cycles. In this class, we practiced a specific flavor of this called Issue Driven Project Management (IDPM). In IDPM, every single feature, bug, or task is converted into a distinct "Issue" on a board like GitHub Projects. You assign the issue to a teammate, they work on it, finish it, and move it to the "Done" column before picking up the next one. 

Does this apply outside of web development? Absolutely. Imagine you're' working at a game development studio building a massive open-world RPG. You can't just tell your team, "Go make the game." That'd just be ridiculous. Instead, using IDPM, you'd break it down. One issue might be "Program the player's jump physics." Another might be "Design the texture for the starting sword." By using IDPM, you ensure that everyone knows exactly what they're supposed to be doing, progress is easily trackable, and no one gets overwhelmed.  

### Coding Standards

<img src="../img/software-engineering/rules.jpg" width="400" alt="Blocks spelling 'Rules'.">  
<caption><small>
  Figure 2: Blocks spelling "Rules".<br>
  <em>Source: <a href="https://abilityministry.com/top-10-benefits-of-having-classroom-rules/" target="_blank" referrerpolicy="no-referrer">Ability Ministry</a></em>
</small></caption>  
<br> 
  
Next up, let's talk about Coding Standards. Coding standards are a set of rules, guidelines, and conventions that dictate how code should be formatted and written. This includes things like how to name your variables (e.g., using `camelCase` vs `snake_case`), how to format your brackets, and when to leave comments. In our class, we used automated tools (specifically ESLint) that would literally yell at us and refuse to deploy our code if we forgot a space or left a variable unused.

If you don't understand why coding standards matter, think of it like grammar and punctuation in an English essay. Sure, you could write a whole essay without periods, commas, or capital letters, and the basic information would technically still be there. But anyone who tries to read it will probably get a headache and hate you for it. The same goes for code. When you're writing software for a drone's flight controller, or designing the firmware for a medical device, you're rarely working alone. Coding standards ensure that whether someone wrote a function on Monday in Honolulu or on Thursday in Tokyo, the codebase looks unified. It makes debugging easier, prevents silly errors, and ensures that when a new developer joins the team, they can actually read and understand the logic without being omnipotent. 

### Design Patterns

<img src="../img/software-engineering/blueprint.jpg" width="400" alt="A blueprint.">  
<caption><small>
  Figure 3: A blueprint.<br>
  <em>Source: <a href="https://stock.adobe.com/search?k=blueprint&asset_id=101655538" target="_blank" referrerpolicy="no-referrer">Adobe Stock</a></em>
</small></caption>  
<br>
  
Finally, we have Design Patterns. A design pattern is essentially a generalized, reusable solution to a commonly occurring problem in software design. It's not a finished piece of code that you can just copy and paste into your project; rather, it’s a template or a conceptual blueprint for how to solve a problem in a way that has been tested and proven by thousands of developers and software engineers. 

While we applied these concepts to our web applications, design patterns are universal. Let's say you're building a desktop application for an accounting firm. You need a way to ensure that only a single instance of the database connection exists at any given time so the app doesn't crash from too many requests. You wouldn't try to invent a custom solution from scratch—you'd just implement the "Singleton" design pattern. Or, if you're building an operating system and need a way for different components to notify each other when a system event happens, you would use the "Observer" pattern. Design patterns give software engineers a shared vocabulary. Instead of spending 20 minutes explaining how you structured a feature, you can just tell your coworker, "I used a Model-View-Controller pattern," and (hopefully) they'll instantly know exactly what you mean.

## Am I a Web Developer or a Software Engineer?

<img src="../img/software-engineering/confused.jpg" width="400" alt="A confused student looking at his laptop.">  
<caption><small>
  Figure 4: A confused student looking at his laptop.<br>
  <em>Source: <a href="https://www.dreamstime.com/confused-student-laptop-seeking-help-library-perplexed-young-sitting-surrounded-books-looking-assistance-image312979411" target="_blank" referrerpolicy="no-referrer">Dreamstime</a></em>
</small></caption>  
<br>
  
"Tayten, I thought you said this class was about software engineering. Why did we spend so much time messing around with TypeScript, React, and UI Frameworks?" 

If you've read this far, I hope the answer to that question is starting to become clear. We used web development because it's highly visual, deeply interactive, and requires multiple pieces of a system to talk to each other. Yes, we used the technical skills we acquired exclusively to build a web application, but the foundational skills we built—learning how to manage a project by communicating with our teammates, how to write clean, standardized code, and how to apply proven structural patterns—are universal in nature. If you took everything I learned in this class and forced me to build a mobile app in Swift or a command-line tool in C++, the syntax would change, but the engineering principles would remain exactly the same.

## Conclusion

At the end of the day, a programmer is just someone who can write code to make a computer do something. A software engineer, however, is someone who can design, build, and maintain complex systems systematically and collaboratively. ICS 314 wasn't just about teaching us how to put a button on a webpage. It was about giving us the discipline, the tools, and the mindset required to build software that lasts, no matter what tech stack the future throws at us.

<hr>

<i>This essay was grammar checked using Google Gemini.</i>  
<i>All images belong to their respective copyright holders.</i>  

<hr>

[^1]: <a href="https://web.mit.edu/6.001/6.037/sicp.pdf" target="_blank" referrerpolicy="no-referrer"><em>Structure and Interpretation of Computer Programs</em>, 1996 (p. xxii)</a>
