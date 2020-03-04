---
layout: post
title: "Maintainable Code: An Analogy"
categories: website
author: "cliveleehere"
---

Have you ever listened to a talk that explained a complex idea in a simple way?  Such talks are refreshing to listen to, and make complex ideas more comprehensible.  On the other hand, some talks explain a simple idea in a complex way.  Whether it's confusing structure or unnecessary details, these talks obfuscate the underlying ideas, and the audience may quickly lose their interest.  

Maintainable code is similar to a good talk.  Maintainable code expresses a complex functionality in a way that's easy to understand.  But easy to understand for who?  'Maintainability' implies that there will be future 'maintainers', whether it's the original author or another programmer.  Future maintainers are the audience of the code you write today.

<p align="center">
...
</p>

There are many different types of talks that serve different purposes. There are stand-up comedies, science lectures, homilies, political speeches, slam poetry, and more. All these types of oral communication have different patterns and structures based on the expectations of the audience. 

What are the expectations of the future maintainers of your code, and how should those expectations shape the patterns and structures that you use?  Their "expectations" will depend on their knowledge, experiences, skills, and available resources.  For instance, you could assume that a future maintainer will know about some of the design patterns, e.g. a singleton, since the classic 'Gang-of-Four' design patterns are well-known across software engineering.  Furthermore, based on the technology you're working with, you can have more specific assumptions about the future maintainers' knowledge and resources available to them.  If you are writing an Android app, for example, you could assume that the future maintainers will have at least some familiarity with Google's Architecture Components or at the very least know where to look.

The future maintainers' knowledge may also be institutional knowledge.  If you've worked at a big company, you may have come across a situation where everyone was mandated to use some old, outdated pattern.  One rationale for sticking with an old pattern is so that future maintainers will know how to work with any code written in that pattern, since they've seen it before everywhere else in the codebase.  (Of course, the flip side of the argument is that if the pattern is so outdated that the platform has moved on to cleaner patterns that work better with rest of the ecosystem, and new hires complaining about legacy code... but that's another story!)

The expectations of the future maintainers even applies to brand new architectural designs.  When you are creating a brand new architecture, try to mimic existing structures that future maintainers may be familiar with.  For instance, even if you can't use a VIPER framework used by your company, try to mimic the VIPER classes in both naming and functionality.  This way, the future maintainer from your company who maintains your code will have an easier time understanding what everything does.

<p align="center">
    ...
</p>

Simple talks are concise.  But they're not more concise than they need to be.  Every word, every character, serves a purpose. How can we write code that's simple, concise, with singularity of purpose, such that the code is more maintainable?

'Literal' simplicity is an important first step.  To go back to the analogy of a talk, the audience will have harder time following the speaker when he uses long sentences, uses complicated sentence structures, or goes on long tangents.  I'm definitely in the "less comments the better" camp.  Your code should be the documentation.  I'm also in favor of shorter functions and classes.  But a function can be too short.  For example, if a private function is one line long, it might be too short.  'Literal' simplicity is easy to detect with the use of linters and static analysis tools, which should be used to avoid 'bike-shedding.'

'Conceptual' simplicity is harder to detect.  If you're listening to a talk that's poorly organized conceptually, you'll find it harder to understand what the speaker is trying to say.  There's an old adage that says "Every problem in computer software can be solved with an abstraction."  For unmaintainable code, not every abstraction solves a problem.  One way to write simple code is to only introduce abstractions when you need them.  In my experience, these layers of abstractions are harder to maintain or delete than to write (which is probably worth another post!), so it's best to start with least amount of abstractions necessary to express all your use cases.  

<p align="center">
    ...
</p>

A lot of the discussions around maintainability unfortunately stops at the 'literal' simplicity and doesn't address either the 'conceptual' simplicity or the expectations of the audience.  This analogy, in comparing code to talks, should hopefully be helpful in thinking about the principle behind maintainable code.

In summary:
 - Maintainable code is shaped by the expectations of the audience, the future maintainers; and
 - Maintainable code is simple on both literal and conceptual levels.