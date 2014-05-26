title: Write The Docs
date: 2014-05-26 09:59:16
tags: [conferences, documentation]
---

If you know me, you probably know that I love technical conferences. I find them very rewarding both professionally and personally. I think I average at least 4 conferences per year, most of which require significant amount of my own time and money to attend. The most recent of these, Write The Docs, provided a very different perspective on technical topics than the conferences I normally attend.


## What is WTD?

Write The Docs is a conference focused on documentation systems, tech writing theory, and information delivery. From the website:

>Writing and maintaining documentation involves the talents of a multidisciplinary community of technical writers, designers, typesetters, developers, support teams, marketers, and many others. This conference creates a time and a place for this community of *documentarians* to share information, discuss ideas, and work together to improve the art and science of documentation.

It's basically a conference for technical and non-technical creators (and consumers) of technical writing to share and discuss ideas and best practices for writing amazing technical documentation.

<!--more-->

## Topics

I know what you're thinking... *a conference about writing documentation? Sounds boring!* I wasn't sure what to expect going into the conference, but in retrospect I thought most of the talks were very interesting. Topics varied greatly, and the quality of speakers was quite high. Some of my favorite talks covered:

* How Twitter is getting its engineers to write more useful documentation (and keep it updated)
* How volunteers can be motivated to make high quality contributions (e.g., for an open platform like [MDN](https://developer.mozilla.org/))
* How to use technical concepts from programming to "hack" the English language

I'll go into a bit more detail about each of my favorite talks below.


## Getting Engineers to WTD

[Simeon Franklin](https://twitter.com/simeonfranklin) and [Marko Gargenta](https://twitter.com/markog) shared some very interesting insight into Twitter's documentation culture and how they are trying to improve it.

Simeon and Marko ran a survey about internal engineering docs at Twitter, and using the net promoter score, determined that the docs were terrible. There were many issues that surfaced in the survey: inconsistencies between components, docs that were outdated or deprecated, incomplete, poorly-written, hard to find, etc.

The solution to this problem meant completely rethinking how documentation worked at Twitter. The first step was to centralize the documentation and get rid of wikis. Wikis are great for documentation in theory (easy to edit, easy to have many collaborators, etc), but in practice they are hard to navigate and search, and the logical separation between documentation and code frequently causes these doc-wikis to become outdated and inconsistent (or to never exist in the first place). To resolve this, Twitter engineers now commit their docs with the code itself. The documentation lives in git alongside the code and tests. This makes perfect sense from a maintainability standpoint: the code, the tests and the docs (all written by the same people) are all in one place. Documentation can now be reviewed just like code. In some projects, they even require that docs, just like tests, are created and updated before you can commit.

Twitter has taken an opt-in approach to this method of documentation, and it has been very successful so far. The team ran the same survey again referring to the new documentation system, and it showed a significant improvement.

I think Simeon and Marko are definitely on the right track. Documentation belongs alongside the project being documented, and ideally is written by the person (or people) that created or contribute to the project.


## Motivation

So... how can we get motivated to WTD?

[Ali Spivak](https://twitter.com/alispivak) from Mozilla gave a talk about how MDN is able to keep a community of unpaid volunteers motivated to write high quality documentation.

There are two types of motivation: intrinsic and extrinsic.

**Intrinsic motivation** involves engaging in a specific behavior because it's personally rewarding:

>Alice writes tests, because she finds comfort in the fact that her code is running as she intended.

**Extrinsic motivation** typically occurs when some sort of reward (or punishment) is the driving force behind the motivation:

>Bob writes tests, because he will get a bad performance review if he doesn't.

Extrinsic motivation can be a double-edged sword. On the one hand, you can motivate people to do something that they are normally not motivated to do, but on the other, you may lower the (already low) level of intrinsic motivation that person feels towards said thing. Extrinsic motivators, such as rewards, can be a good way to get stuff done *once*, but the work may not be done well, and it likely won't be done again unless these rewards are offered again.

However, there are extrinsic factors that can be used to build *intrinsic* motivation. For example, unsolicited (especially *unexpected*), "public" praise is an easy win:

> Alice calls out Bob for his awesome work on Project X this week in a company all-hands.

Since this is an unexpected "reward", it is not an extrinsic motivator, but certainly could have a positive effect on an individual's intrinsic motivation for future tasks.

Ideally (especially for something like writing tests or documentation, which is an eternal duty), most of the motivation driving the behavior should be intrinsic. This is certainly not easy to accomplish, because let's face it: this stuff can be *boring*. So how do we accomplish this? How do we get people motivated to do the boring stuff? Ideally we should find a way to increase intrinsic motivation. Mozilla has done a very good job of accomplishing this for the MDN community.

The three major sources of intrinsic motivation that Ali referenced were responsibility, mastery (or personal growth), and purpose.


### Responsibility

Mozilla can't tell its volunteers what to do; they are autonomous. When Mozilla trusts volunteers to contribute directly to MDN anyway, it adds to the sense of responsibility they feel toward the community. This feeling acts as a great intrinsic motivator.  Ali likens them to a "special herd of awesome cats."

Striving for and maintaining an extremely high set of standards (set by example, rather than some imaginary "quality bar"), and trusting people to meet these expectations can build a great sense of responsibility. This is something I think any organization could do to increase the sense of responsibility for things like writing high quality documentation and tests.


### Mastery

Another great source of intrinsic motivation for MDN contributors is professional mastery of specific topics. People contribute because it helps them grow as individuals. This desire to better oneself is something that must come from within the individual.

I believe create a community that nourishes and encourages this desire for personal development. We've already got some things down (e.g., regular tech talks), but I think we can do better, possibly by encouraging more people to attend conferences, make more time for side projects, take courses, etc.


### Purpose

People need to believe that what they are doing is worthwhile. The largest detriment to motivation may well be lack of purpose. *Why am I spending so much time on this? What's the point?* Indeed, we should not be wasting time on pointless tasks, but some tasks that may *seem* pointless are actually very necessary. In the case of tests and documentation, the importance of the work may not always be immediately clear. It is imperative that we build a culture that reinforces the purpose of important tasks; especially the particularly mundane ones.

Ali brought up a lot of really good ideas for motivation, and I think similar ideas can be applied at any organization.


## Hacking the English Language

After we're sufficiently motivated to write documentation on our projects, we should make sure we write documentation that's actually useful!

[Nina Vyedin](https://twitter.com/misskallisto) gave a really great talk about how we can apply basic concepts from programming to any type of writing.


### Make a Template

Starting from a blank slate is difficult. There is a great mental hurdle to overcome when starting something from scratch (not to mention a high likelihood of making a mistake.) For this reason, it's very common for programmers to use tools (e.g., Yeoman or other code generators) that generate project-specific templates to start from. Why not apply this same technique to writing? Create templates for the various types of documents you tend to write frequently. Whether it's meeting minutes, blog posts, or pieces of technical documentation, you should be able to create a template with a basic structure that each of these types of documents can build upon.


### Make a Spec

To make sure your document fulfills its purpose, you need to ensure that you ask the right questions. In programming projects, we call this a spec. The spec identifies (and answers) all the questions that must be addressed to build a correct product. In writing, we can apply a similar technique by asking the right questions before writing:

* What question(s) am I trying to answer?
* Who is the target audience?
* What is the current state of documentation on this topic?
* What is the work plan?
* etc...


### Use the Correct Architecture

In writing, we often start with an outline that lays the foundation for a document. This is certainly a valid approach, but it is often poorly executed. Perhaps the wrong outline was used. Instead of coercing content into an outline that doesn't fit, maybe we should use a different template.

The programming equivalents of outlines are "design patterns". Using an appropriate code architecture is very important to building a scalable, maintainable product. Again, we can apply this technique to writing! This ties closely to the "make a template" rule above; make sure your template follows the correct design pattern for the specific type of document you plan to write. Nina gave several patterns (with examples):

| Pattern | Description | Examples |
| --- | --- | --- |
| **Tell a story** | follow a linear timeline | walkthrough, tutorial |
| **Paint a picture** | describe everything on the screen | introduce a feature, blog post |
| **Reference** | introduce things one at a time and describe | troubleshooting document |
| **Theme + situations** | idea and use cases | introduction to a concept |
| **Drill down** | organized by hierarchy, general to specific | cross-platform to platform-specific concepts |
| **Level up** | start simple and reveal info as you go along | getting started guide |


### Name Your Variables

In programming, we use variable names that make sense so our code is easier to understand and maintain. In writing, we can apply good variable naming conventions to help our readers understand our writing better. Things to avoid:

* excessive use of undefined pronouns ("it", "they", etc)
* the passive voice, which tends to make processes or events seem to happen magically ("the window gets created when the app launches")
* vague and generic technical terms or unnamed ideas (a "view")


### Don't Just Edit - Refactor

We refactor code all the time. It's a natural part of maintaining and extending upon any complex system. In writing, typically you have someone edit or proofread your work for typos, grammatical errors, and correctness. In programming, syntax and correctness testing is done automatically by code linters and unit tests, but code reviews exist so that people can verify that the code makes sense, follows sane design patterns, etc. When reviewing someone else's writing, we should be considering the structure just as we would when reviewing their code. If something is out of place, or doesn't make sense in a certain context, refactor it!


## Continuing the Discussion

Write the Docs is building an awesome community of people that appreciate the need for well-written, accessible documentation. I'd certainly attend this conference in the future, and you should too!


## Useful Things

* [Videos](http://videos.writethedocs.org/category/2/na-2014) of the talks
* Andrew Spittle's [notes](http://andrewspittle.com/tag/write-the-docs/) are much better than mine
