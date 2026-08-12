---
layout: essay
type: essay
title: "The Use of AI in my Software Engineering Journey"
# All dates must be YYYY-MM-DD format!
date: 2026-08-11
published: true
labels:
  - ICS 314
  - Learning
  - AI
---

## Introduction

If you’ve spent any time at all on the internet over the last few years, you’ve probably heard the doomsday prophecies: AI is going to take our jobs, write all our code, and make software engineers and programmers completely obsolete. But if you actually sit down and try to use these tools to build something—or in other words, you try vibe coding—you quickly realize that AI isn't really all that it's cracked up to be. AI can create code that works, but it tends to be insecure and hard to update. That's why you tend to see stories about large tech companies like Google and Meta rehiring the software engineers they laid off. However, while AI might not have replaced software engineers, that doesn't mean it hasn't shaken up the field. 

Instead of spending hours skimming through forum posts for a specific bug fix, developers can use Large Language Models (LLMs) like ChatGPT or Google Gemini to contextualize our specific codebases and provide feedback tailored for them. Throughout the ICS 314 course, I used Google Gemini 3.5. It served as a supplementary tool to help me debug code, break down concepts I didn't quite understand at first like TypeScript array functions, and grammar-check my essays. But there's a difference between using AI to help you learn and using it to replace learning altogether. 

## Personal Experience with AI

AI served as a valuable tool to help me throughout the ICS 314 course, especially because of the sheer quantity of assignments in this course. I didn't use it for everything, but where I did use it, it was incredibly helpful. Here is a look at how I used AI across the various parts of this course:

### Experience Quizzes

No AI was used to generate any code for these assignments. However, for the first two experience quizzes, I used Google Gemini to verify that my code actually did what it was required to do. In these two cases, I used the exact same prompt: "Here are the instructions for this assignment: &lt;Experience Quiz Instructions&gt;. Please verify my code completes this assignment: &lt;My Code&gt;." While it did work for verifying my code, I stopped using it afterwards because I thought I'd learn more from manually testing my code. I never used AI to complete any of these assignments for me, because I believed it would've completely defeated the point of doing them in the first place. These experience quizzes are designed as basic exercises to grasp core concepts. If I can't even get the basics down on my own, I might as well switch majors. 

### Practice Quizzes

AI was not used during any of my WODs for the same reasons it wasn't used to complete my experience quizzes for me: it would've defeated the whole purpose of the WOD. However, I did use AI to help prepare for WODs, especially once we reached the WODs related to Bootstrap. I would often ask Gemini to explain what various Bootstrap classes did, like "What does Bootstrap md={4} do?", or how I could implement something using Bootstrap, like "What is the Bootstrap equivalent of 'justify-content: center'?". This worked to great effect, and with the introduction of React and Next.js, it helped me to warm up to the idea of using Bootstrap outside of just this course.

### Quizzes

I did not use AI for any of my quizzes, with one exception. Quizzes are meant to serve as a test of our knowledge. Asking an LLM like Gemini would've defeated the whole purpose of a quiz. With that being said, you're probably wondering what that one exception was. Well, for one of our quizzes, the goal was to create a webpage that was structured to simulate the appearance of a book. However, the provided link for the background image we were instructed to use was broken, so I used both Gemini and Google Image Search to try to find the source image. I was ultimately unsuccessful, so I just used Windows' basic built-in image editor to color over the text in the example screenshot with a white brush and used that as my background image.

### Essays

I did not use AI to write any of my essays for me. Once again, it would've defeated the whole purpose of the assignment. I did use Google Gemini to grammar-check my essays to ensure they followed proper English conventions, but aside from those corrections, the words in my essays were my own.

### Final Project

Gemini was invaluable in helping me to complete my final project. I would often use it for ideas on how I could implement certain features on my website. For example, I used the prompt "In React Bootstrap, what could I use to implement a filter system to allow users to filter through entries in a database?". In return, Gemini taught me about the existence of the Form component, which I would go on to use to implement a filter system for users to search through entries from my database. Gemini was also instrumental in debugging broken code. I would often ask Gemini "Please explain what is causing this error &lt;Error Text&gt;", and it would usually give me an explanation of the potential causes of the error in question that I could understand and work off of. There weren't really any downsides in particular to using AI for my final project in the way that I did, other than potentially costing me a bit of skill development.

### Learning a concept / tutorial

I used Gemini extensively for this purpose. This was the case especially for the TypeScript array functions and Bootstrap classes. For example, I’d ask prompts like "Explain how .reduce() works in TypeScript by using a minimal code example" or "Explain how Bootstrap's d-flex, justify-content-between, and align-items-center classes interact when laying out a navigation bar.". By using prompts like these, AI helped me to understand a lot of the concepts we covered throughout the course.

### Answering a question in class or in Discord

I did not use AI to answer any questions asked by my classmates on Discord. By questions, I mean the one technical question I tried to help answer. I didn't bother using AI because I didn't really have the full context of what was causing their problem, and it was only a few minutes before the deadline for the assignment they were trying to complete. Instead, I just tried my best to answer their question using my own experience with the assignment.

### Asking or answering a smart-question

I did not use AI to ask or answer any smart questions. This was because no smart questions were ever posted in the class Discord server's #smart-questions channel, not even by me.

### Coding example e.g. “give an example of using Underscore .pluck”

I used Gemini whenever I needed a quick, isolated code example to see how a specific function or method worked. This was especially helpful when working with the TypeScript array methods. For example, I'd tell Gemini to "Give me a minimal code example showing how to use .map() in TypeScript to transform an array of user objects into an array of just their email strings." Just like the "Learning a concept / tutorial" subsection, this helped me to understand a lot of the concepts we covered throughout the course, beyond just TypeScript array methods.

### Explaining code

Like using Gemini to provide coding examples, I'd often ask Gemini to explain what certain methods or classes did. In the case of methods, I'd also ask what a method's parameters were and what they each did. For example, I'd ask Gemini, "Please explain what the .filter() function in TypeScript does, what its parameters are, and provide a simple example of the function in use." Similarly, this helped me understand the concepts and languages we covered throughout the course.

### Writing code

Outside of using Gemini to write example code to help me understand key concepts and methods, and to debug my code, I also used it to write replacement code for the sections causing errors. This was mostly for the final project, where I'd ask Gemini to help write replacement code whenever something broke, especially when it came to the Prisma code for the database. For example, I'd ask Gemini "Please identify the error in this code: &lt;Broken Code&gt; and fix it." Without Gemini, a lot of my final project would've remained broken.

### Documenting code

I did not use AI to write any comments in my code. This was because I barely wrote any comments, and the few comments I did write were simple, so I didn't need to use AI to write them.

### Quality assurance e.g. “What’s wrong with this code &lt;code here&gt;” or “Fix the ESLint errors in &lt;code here&gt;”

As shown in the other subsections, I used Gemini quite extensively to help with debugging, although I didn't need it to help with my ESLint errors.

### Other uses in ICS 314 not listed

To my recollection, I did not use AI in any ways that haven't already been listed or explained.

## Impact on Learning and Understanding

So, did using AI stunt my learning, or enhance it? Honestly, it was a massive enhancement, but in a way, it came with its own learning curve. Using Gemini was like having a really good—albeit occasionally confused—tutor sitting next to me at all times. It helped with my comprehension by drastically reducing the time I'd spend stuck fixing errors. Instead of being hit with a wall of red text in my console and just calling it a night, I could ask Gemini to explain what the error was in plain English. This allowed me to keep working. Of course, it still challenged my own understanding of code by forcing me to review the code I was being handed. Just as you can't trust everything an AI tells you, you can't just blindly trust whatever code it spits out. I feel that using AI helped me to improve my code-reading skills because I was constantly reviewing whatever code it gave me to make sure it worked properly.

## Practical Applications

Outside of ICS 314, the practical applications of AI in real-world software engineering are undeniable. In real-world projects, the hardest part isn't usually writing the code; it's understanding the massive, undocumented system you just inherited. AI tools are proving incredibly effective at mapping out complex codebases, identifying security vulnerabilities, or simply deciphering a multi-hundred-line function. That's coming from personal experience, since I've used it to learn how the code written by my predecessors worked. It's saved me from having to read through thousands of lines of poorly formatted code, and if it can do that much for a simple web developer like me, just imagine the good it can do in other fields.

## Challenges and Opportunities

Of course, it isn't all sunshine and rainbows. The biggest problem with using AI is that it doesn't have access to the whole picture. There were times I'd ask Gemini to help me resolve an error or give me suggestions on how I could implement something, and it would either give me code that didn't work with the rest of my assignment or didn't meet the requirements. This was especially apparent with the Final Project, where Gemini didn't have access to the dozens of other components, schemas, and pages that worked in tandem with the chunk of code I was trying to fix. Another challenge is the risk of over-reliance. It's incredibly tempting to let the AI do the heavy lifting when you're tired, which can lead to a degradation of your own problem-solving capabilities. However, the opportunities are massive. I can imagine a future where AI is integrated even more seamlessly into IDEs—not just as an autocomplete tool, but as a real-time tutor that prompts the student to think. Imagine an AI that, instead of giving you the answer, highlights a line of code and asks, "Are you sure this array won't be null here?"


## Comparative Analysis

If we compare traditional teaching methods like textbooks, static lectures, and Stack Overflow searches to AI-enhanced approaches, the biggest difference can be found in engagement and context. Traditional methods require a high degree of critical thinking. If you have a bug, you have to find a forum post where someone had a similar bug, identify the underlying issue, and apply it to your own unique context. This builds immense character and deep research skills. AI, on the other hand, provides instant, context-aware answers. It bypasses the search phase and jumps straight to the solution. While this drastically improves practical skill development and keeps engagement high because you aren't stuck for hours, it poses a risk to knowledge retention. If you don't struggle for the answer, you might not remember it the next time you need it.

## Future Considerations

So, what's the verdict? Are we all going to be replaced by AI overlords? No, I don't think so. But I do believe the future of software engineering education will undergo a massive shift. We'll likely move away from testing students on syntax memorization and move toward testing them on system design, architecture, and—as dumb as it sounds—Prompt Engineering. In the future, knowing how to talk to an AI, how to frame a problem, and how to rigorously test its output will be just as important as knowing how to write a for loop. The computer science curricula of tomorrow will need to teach AI literacy as a foundational skill.

## Conclusion

At the end of the day, AI tools like Google Gemini are exactly that—tools. A hammer can build a house, but it can't draw the blueprints. My experience in ICS 314 has shown me that AI can drastically accelerate the learning process, untangle complex bugs, and translate cryptic documentation into plain English. But it can't replace the critical thinking required to create good software. To optimize AI in future courses, I don't think professors should ban it. Instead, they should teach students how to use it responsibly. Just like power tools, the calculator, and the humble computer, AI can be used to help us be more efficient and productive. But in order for it to do so, we need to learn how to use it properly.

<hr>

<i>This essay was grammar checked using Google Gemini.</i>  
<i>All images belong to their respective copyright holders.</i>