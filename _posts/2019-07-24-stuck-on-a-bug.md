---
layout: post
title: "Stuck on a bug?"
categories: website
author: "cliveleehere"
---

Have you ever spent multiple hours or days trying to fix a small bug?  You've already googled every terms you could think of. At some point, you may have felt like you were trying different permutations of arguments or settings, just to see if it would work, because you're _so close_ from fixing the problem? And yet most of the time, the small tweaks don't work! You have _some_ mental model of how things work, but you seem to be missing some small yet important piece that's the source of the bug. You've tried everything at this point, and you've exhausted all the options (or permutations). What do you do now?

#### 1. Slow down
Often times, the urge to _just get it done_ actually prevents you from taking the time to understand the problem.  When your attempts to tweak things without completely grokking the issue fails, slow down! Take a deep breath. Take a short walk. Think about something else for a few minutes. Rest your eyes. Drink a cup of water. 

Okay, you good? Let's keep going then!

#### 2. Look Around
Look for other resources. If you're like most programmers, you've already googled or searched Stack overflow. And they _are_ great resources. 

But skip them. Go directly to the source. RTFM. Read the API documentation. Research more about the framework you're using. Watch a tech talk about the library, even. Find out the terminology of the platform that you're using. 

Knowledge is contextual; when you build context around the firm, concrete sources of truth, you'll be able to formulate better mental models of how the different pieces fit together. You may also learn about the ways in which you can use different tools to fix similar bugs.

#### 3. Dig Down
You may have picked up a new tool or a setting in the tool you didn't know about. Time to start digging.

Debugging never goes out of style. If you're working on UI, you may have come across some tools that captures and/or presents the state of the UI. Go one level deeper than you've gone before. Keep digging, shift through the dirt, and look for clues. As you do so, refer back to the API documentations, the source code of the library, etc. from step 2. Because you have greater context, you'll be able to better process your investigation.

#### 4. Go Faster
By now, you've slowed down so that your mind is ready to form new ideas, you've learned new ideas and have formed new hypotheses, and you've dug deeper into the problem. You can now move fast again. But _before_ you can move fast, you have to have the right setup.

Fast iteration is crucial in software development in general, and it's just as crucial when you're trying to fix a bug. When you're developing a mental model around an _unknown_, it's nearly impossible to hold on to the mental model when you have _slow_ iterations. Say you have a hypothesis and make some changes to your code, and it takes ten minutes to build. By the time your code runs, you've already half-forgotten the exact details of your hypothesis.

If you have the time and resources, use all the dirt you've dug up  - in step 3 ;) - and build a sandcastle. Build a smaller, isolated facsimile of your program that also has the bug.  Build a sandcastle that has the characteristics of the problem. It should be small, faster to compile, and have only the necessary parts that isolates and demonstrates the bug.  Building a sandcastle will seem like a lot of work. But if your code is modularized and separated out into clean layers, creating a sandcastle will be straight-forward. If your codebase isn't separated out very well, you may still be able create an entirely new sandcastle, especially if the bug is related to using a specific library or platform. Another benefit to building a sandcastle, is that you'll gain a greater understanding how the pieces fit together while building out the sandcastle. (Note: a 'sandcastle' is just a term I made up. It isn't a standard terminology, so if your coworkers give you a weird stare when you tell them to build a sandcastle, don't be surprised!)

Building a whole new program _is_ a drastic step, but this isn't your only option for increasing your iteration speed. You could also pare down your program so that it compiles faster. Remove external dependencies.  Turn off different compile-time tasks or IDE features (e.g. code indexing). Unload different modules that aren't necessary for replicating the bug. (Side note: use a build system that supports incremental builds, build caches, and implementation configurations). You could also improve the iteration by using a sandbox environment, mocking data, or adding a debug menu that's accessible during runtime.

#### 5. Victory lap
After you've finally fixed the bug, it's time to do a victory lap.  Raise your arms above your head, let out a roar and do a lap around the office!