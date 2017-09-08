---
title: Stack Underflow, Or: Garbage Questions In, Garbage Answers Out
author: Micah Mynatt
layout: essay
type: essay
date: 2017-09-07
labels:
- software engineering
- stack overflow
- reflection
---

## Questions: Do We Really Need Them? (The Answer Is Yes)

Whether a developer is self-taught or formally educated, a situation will inevitably arise in which an idea, concept, solution, etc. is out of their immediate reach. And in many cases, said developer is able to pull from the pre-communicated knowledge of those that came before them to take hold of the information they need, without disturbing others. 

However, in cases where this is not possible, developers must rely on the experience of their elders through inquiry. That is, they must ask a question, and they must ask it in such a way that they move closer to their answer. They must be careful that they don't strain their relationships with the developers of yore, that they might be able to draw upon their knowledge once again in the future.

Learning to ask questions goes beyond the technicalities of systems you don't quite understand. I've had the opportunity to work on a variety of projects under different kinds of people, and that's allowed me to begin to understand how important question asking is with regards to *knowing what it is you're supposed to be doing*. This is, of course, very important from a software perspective, but even  more important if you're also taking on other roles, by necessity or happenstance.

I've heard experienced engineers say before that the requirements to real-life projects aren't nearly as cut-and-dry as they are while learning to be an engineer, and this is true in most of the situations I've experienced thus far. But a hearty amount of focused and thoughtful questioning allows you to properly scope your projects, know the boundaries of your responsibilities, the limitations of all potential environments, and so on. Knowing these things in advance - even if it's just scratching the surface - can prevent many future headaches for when these things come up in the middle of development. 

## Is There Such a Thing As a Stupid Question? (The Answer Is Yes)

Eric S. Raymond, software developer and OSS advocate, has [written pretty extensively on the topic][article]. I think his main points on good and bad questions can be summarized as such:

Good questions:

- Demonstrate effort in attempting constructing a good question before asking
- Demonstrate a desire and ability to learn and contribute to solving the problem at hand
- Are targeted properly towards those in the know
- Are well-written

To contrast, bad questions:

- Don't suggest any existing effort
- Assume entitlement to an answer
- Don't target to experts correctly
- Are sloppily-written

Let's take a look at a few examples from questions pulled from [Stack Overflow][so], a site dedicated to asking questions and (hopefully) getting answers.

## What Not To Do

The following question [can be found here][badq]:

> I believe this is not the kind of question I should be asking here so I apologize in advance. I have an exam in 2 days and the teacher that was supposed to give me a lesson clearing out all of my questions had to cancel, so now I have no one to ask. I am resolving an exam from last year, and one of the questions is to make a little java program where we pretty much simulate a lottery game of 6 numbers. My question is about efficiency, the exam is written on paper and I feel like if I was to write everything I typed on the computer I would not have enough time, we have 90 minutes and this is only one of the problems, swing is not my strong point so that leads me to think that I could write this in much fewer lines. The public instance variable 'key' is there to simulate a method from another class that generates a random key that we do not need to implement. We are only allowed to use FlowLayout, BorderLayout, CardLayout and GridLayout. [large, uncomment code block]

How does this question do, according to Raymond's qualifications? Let's take a look.

- *"[large, uncommented code block]"* - I removed the actual code because it was a mess, and this doesn't exactly demonstrate the effort one would look for in a question asker. It's just a code dump, and doesn't guide one towards the question, the restrictions, the problem, the desired solution or anything of that manner.
- *"now I have no one to ask"* - an assumption of entitlement to an answer: "If you don't answer this, I'm doomed!"
- *"I believe this is not the kind of question I should be asking here so I apologize in advance"* - incorrectly targeted, by their own admission?!
- *"My question is about efficiency [...] that leads me to think that I could write this in much fewer lines"* - ultimately, the "question" isn't even really a question: it's an assumption that the "answer" will perform this task for them. 

Oof. This person didn't do so well. Many of the initial answers were pretty negative, and didn't address the person's underlying concerns at all:

> "don't just bloat the site with your code dump, point out the specifics and ask question that are readable."
> "Your suspicions were correct, this kind of question does not belong on this site."
> "And your question is?"

As one can clearly see, this kind of question asking certainly doesn't fill those who could help with joy or determination.

## What To Do, Maybe?

The following question [can be found here][goodq]: 

> Anyone tinkering with Python long enough has been bitten (or torn to pieces) by the following issue:
> 
```
def foo(a=[]):
a.append(5)
return a
```
> Python novices would expect this function to always return a list with only one element: [5]. The result is instead very different, and very astonishing (for a novice):
> 
```
>>> foo()
[5]
>>> foo()
[5, 5]
>>> foo()
[5, 5, 5]
>>> foo()
[5, 5, 5, 5]
>>> foo()
```
> A manager of mine once had his first encounter with this feature, and called it "a dramatic design flaw" of the language. I replied that the behavior had an underlying explanation, and it is indeed very puzzling and unexpected if you don't understand the internals. However, I was not able to answer (to myself) the following question: what is the reason for binding the default argument at function definition, and not at function execution? I doubt the experienced behavior has a practical use (who really used static variables in C, without breeding bugs?)

Let's take a look at this question:
- Demonstrates curiosity into the subject
- Demonstrates prior experience and 
- Correctly targeted towards those with experience in Python

This question is a little different from the previous, in that it doesn't ask for a "solution"; instead, it's more interested in discussing the reasoning and ramifications of certain design decisions of the language itself. With **1769 upvotes**, **588 stars**, and **29 answers**, one can clearly see a very interested and positive reaction to this question. How wonderful! I'm sure the question asker is very intellectually satisfied with how this all turned out.

## Ask Away!

I've asked a large swath of good and bad questions alike in my time learning programming, and doing this kind of analysis on others' questions has left me feeling a little more confident in my own abilities to ask for help. Should the need arise in the future, I don't think I'll be quite as hesitant to ask away!

[article]: http://www.catb.org/esr/faqs/smart-questions.html
[so]: https://stackoverflow.com/
 
[badq]: https://stackoverflow.com/questions/46108186/java-lottery-game-efficiency-swing
[goodq]: https://stackoverflow.com/questions/1132941/least-astonishment-and-the-mutable-default-argument
