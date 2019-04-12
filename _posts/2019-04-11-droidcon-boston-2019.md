---
layout: post
title: "Droidcon Boston 2019 Recap"
categories: website
author: "cliveleehere"
---

I had a change to attend and speak at Droidcon Boston again this year, and heard some amazing talks. I wanted to do a quick write up, with key takeaways.

Here's the [link to the agenda](https://www.droidcon-boston.com/agenda/), and a [link to some of the slides](https://github.com/Droidcon-Boston/slides/tree/master/2019)

#### Destination Navigation
This talk, given by Eric Maxwell, was a detailed overview on how to use Navigation Component. There was a lot of useful info here, and I got a great sense of some of advantages of using Navigation Component, including simpler deeplinks.  There were also some practical suggestions for migrating to Navigation Components, including steps to reducing the number of activities.

#### Select * From Kotlin
Given by the Mr. Handstand Sam himself, this talk went into couple of database libraries that are great for use with Kotlin: Room and SqlDelight. He compared and contrasted the features and how to use them. The general sense I got was that it's better to stick with Room for now, as SqlDelight stills seems pretty new.

#### WorkManager
Divya Jain gave us a detailed look into the various different features of WorkManager and when you would want to use it. (Side note: I always appreciate it when speakers give us some guidance on WHEN it's useful and not as useful to use what they're presenting on). The ability to group different tasks, chaing them, and even run them in parallel, seem really powerful!

#### MotionLayout
Michael Scarnell gave us a detailed look into MotionLayouts. It's a combination of property animation framework, layout transitions with TransitionManager, and CoordinatorLayout. Because MotionLayout is a layout, all its features are specified via the layout .xml file. I do wonder though, that while MotionLayout seems very powerful, its layout file may become gigantic!

#### Flutter, a Designer and Developer Walk into a Project
Adrian Catalan and Carmen Gonzalez talked about using Flutter as a team.  Having played around with Flutter, I can see the appeal of it from the Designer's perspective, and how it can be a shared language between devs and designers.

#### Achieving Fully Reactive Code Using Both LiveData and RxJava
Alex Sullivan gave us an overview of Reactive programming, LiveData, and RxJava.  He dived into an example app, as well as how to test it.

#### How we seamlessly internally test our Android apps within Microsoft
Keerthan Kumar gave us a talk on how Microsoft provides many different tools for testing Android apps, including testing on the cloud. 

#### Android Routines with Coroutines
Sean McQuillan gave us an overview on Coroutines.  He gave us a briefly histroy of coroutines, and assured us with historical argument that coroutines are NOT a fad! He also presented on Structure Concurrency, which was a relatively new concept, that tries to solve the problem of leaking work, guaranteeing that all work was completed when a function returns, and a way to organize scopes by parent-child relationships.  My biggest takeaway is, learning coroutines in any language will be a great use of your time, as it will be a transferrable concept!

#### Finite State Machine to the Rescue
This talk was on how Emanuel Moecklin used Finite State Machines (FSM) written in Kotlin DSL to great effect. He also gave us some tips: don't use FSM for navigation only, use it for flows with different types of activities (ui, async calls, different lifecycles), and draw the state diagram before writing code.  Some of the benefits he mentioned seemed compelling: clear separation of concerns, reduced complexity (and hence easier to under, maintain, and scale the team), eliminated edge cases (less error prone, fewer regressions) and easier to change. I'll have to be on the lookout to when I can use FSM in the future!

#### Asynchrony in Kotlin: Rx or Coroutines
Anton Spanns presented a comparison of Rx and Coroutines. He presented on the advantages and disadvantages of coroutines as compared to Rx.  For anything to do with streaming and cold streams, Rx wins (for now, until Flow library becomes better defined). There there were some comparison of syntax, and this part was entertaining as it had some audiences cheering and shouting out their preferences for one or the other on different use cases. I did wish that there was some more structure or guideline on how he picked Rx or Coroutine as 'winner' in different circumstances. It felt like we were just going by whatever 'looks' better. In any case, the talk was informative and fun; another confirmation that coroutines will be good to learn!

#### Augmented Reality: From Fun to Furnished
I gave a talk on Augmented Reality. I gave a general overview of where Wayfair's AR feature is at, outlined some of the challenges & opportunities, and proposed a couple architectural solution that would help us meet those challenges. I also showed pictures of my cats. 

#### Working Offline: Data sync patterns at Toast
Couple of engineers from Toast gave a general overview on things they do for their specific use cases. I appreciated that they spent some time painting the picture of their specific problems and use cases. It seemed like they approached the solutions from many different angles (e.g. switching to protobuf, choosing LevelDB which was best for append workloads, MVI-like app architecture), which is cool! I do wonder whether they've considered any libraries/frameworks that are more prevalent within the Android ecosystem and could've saved them some time, like using a gRPC library directly instead of running it on Netty that runs on Android.

#### A dozen technique for everyday DSLs
Greg Milette gave us some real practical tips for writing Kotlin DSLs. One of the tips that sticks out to me is using lambdas with the receiver as the builder class. This means that the lambda will act like an extension function for the builder class that's the receiver! Three different kotlin concepts rolled into one, for a more concise, natural DSL!). I also learned about @DslMarker, and Kluent, a kotlin, fluent, assertion library.

#### On-device Machine Learning for Android Development
Eric Haddad from Google gave us an overview of everything that's possible for on-device ML, and we can do A LOT! Hitting the cloud will give us better results, but on-device (depending on the hardware) seems like it'll be good enough for many use cases.

#### Code + AI = Will Robots take our Coding jobs? ML applied to Programming
Stephen Magill assured us that this won't be the case. Great overview on ML, and of how analyzing Abstract Syntax Trees (AST), ML can be used for various different tasks such as labelling, better naming, comments, code completiong, and correction of mis-remembered APIs. The end result is that we'll have better tools, and can focus on the fun/creative parts of the job. Whew!

#### Highlights
- Live Sketchnotes!
- Courtines
- Kotlin DSL & FSM
- Machine learning!
- Catching up with old colleagues and where they're at!
