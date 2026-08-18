---
layout: essay
type: essay
title: "Guesstimates and Git Commits: The Reality of Tracking Project Time"
# All dates must be YYYY-MM-DD format!
date: 2026-08-17
published: true
labels:
  - ICS 314
  - Learning
  - Software Engineering
---

## Introduction

If you’ve ever tried to guess how long a coding task will take, you probably already know that software engineers are notoriously terrible at estimating time. For our final project, our team relied on Issue-Driven Project Management (IDPM)—which is essentially a project management strategy where you break a massive project down into bite-sized, trackable chunks. 

As part of this process, we were instructed to estimate the time it would take to complete our assigned tasks and then record how long they actually took us. Estimating code time is a bit like forecasting the weather in Hawaii: you can look at the radar all you want, but you're still probably going to get rained on. In this essay, I want to go over my slightly chaotic estimation methodology, compare those estimations with reality, look at the benefits of this practice, and finally, explore ways I can stop relying on pure guesswork in the future.

## Look to the Past to Predict the Future

This final project wasn't the first time we've had to make time estimations. Throughout the semester, we've had to complete various "Workouts of the Day" (WODs). Think of these like wind sprints for programmers—short, timed coding exercises designed to drill core concepts into our heads and give us an opportunity to practice implementing them. 

While no single WOD matched the sheer scale of our final project, the estimations I made for these exercises helped me to gradually refine my internal clock over the course of the semester. By comparing my initial WOD estimations with the actual time it took me to finish them, I was able to get a rough idea of how long it would take me to do routine things, like spinning up a navigation bar or setting up a database using Prisma. Even though my estimations were frequently off, this background knowledge gave me a baseline, and I used that baseline to do my absolute best to make predictions for the GitHub Issues I was assigned during the final project.

## The Reality of Tracking Effort

If I'm being completely honest, my method for tracking effort on the final project was less "scientific data collection" and more "crime scene forensics." To figure out how long a task took me, I relied almost entirely on my Git commit history. Since I usually tackled my assigned issues in one or two continuous sittings, I would just look at the timestamps between my initial commit and my final push. This gave me a reasonably accurate "best guess" of how long I spent actively typing away at that specific issue.  

Was this the best method to track my effort? Absolutely not. There are dozens of better ways I could've handled this, like simply setting a stopwatch on my phone. However, to be perfectly honest, I didn't actually realize I needed to keep track of my exact effort until after the fact, so I had to improvise.  

Now, was tracking this actual effort genuinely useful for the project itself? Honestly, no. 

The core problem was that I was constantly working on vastly different components. The final project was incredibly diverse in its requirements. Knowing the exact time it took me to figure out the UI for a calendar component didn't help me at all when estimating how long it would take to build a backend filter for our database. The tasks were completely apples and oranges. Trying to use historical tracking data from a front-end UI task to predict a backend logic task is like using your recipe for baking chocolate chip cookies to figure out how to rebuild a car engine. It just doesn't map well.

## Reflections for Next Time

As I've already admitted, my little Git commit forensic method is deeply flawed. Among other things, a commit history doesn't account for the "invisible work" of software engineering. It doesn't track the hour I spent reading obscure documentation, the 45 minutes I spent skimming Stack Overflow for bug fixes, or the time I spent just staring at the ceiling trying to plan out the logic before writing my first line of code. 

If I had to track my process and progress next time, I would entirely overhaul my methodology. Instead of relying on retroactive best guesses through Git timestamps, I would explicitly write down my actual start and end times in a notebook. Logging concrete data from the exact moment I begin brainstorming an issue to the moment I finally merge it into the main branch would give me a much truer reflection of my effort, and leave a lot less room for forensic guesswork.

## Conclusion

At the end of the day, estimating and tracking time on a final project is less about predicting the future with 100% accuracy and more about building a structured mindset. While my actual tracking might not have perfectly informed my future estimates due to the wildly varying nature of our project's features, the *act* of estimating still kept me grounded and accountable. 

Just like applying coding standards or utilizing design patterns, estimating time is a discipline. It taught me how to allocate my resources, prepare for the worst-case scenarios, and ultimately get our final product working and out the door before the deadline. 

<hr>

<i>This essay was grammar checked using Google Gemini.</i>  
<i>All images belong to their respective copyright holders.</i>