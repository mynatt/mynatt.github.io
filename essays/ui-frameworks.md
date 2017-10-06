---
title: Imperfect Solutions for Complicated Systems - A Tale of UI Frameworks
author: Micah Mynatt
layout: essay
type: essay
date: 2017-10-05
labels:
- software engineering
- frameworks
- ui
- html
- css
---

In a parallel universe, we might have website infrastructure that properly divorces content and design to a stronger degree, allowing for better organization and easier development. Unfortunately, that's not the case; we're stuck (at the moment) with systems that often couple them quite strongly, made in languages that were never intended to bear the full burden of presentation that we put them under now. 

Fortunately, a stop-gap measure exists in the form of **UI frameworks**; toolkits that often resemble Rube-Goldberg machines, intended to quell the suffering of developers that work with these unsavory systems. These frameworks are usually quite complicated, with quirks and drawbacks of their own, but they serve a clear purpose in the modern web, allowing developers to sanely design projects that would otherwise be unmanageable, while also providing clearer paths towards both upgrading and maintaining backwards-compatibility.

## UI Frameworks?

**UI frameworks** are intended to simplify the design and creation of user interfaces, by providing a skeleton and a set of tools that one may use to build from. The subset I'll be describing involves UI web frameworks, which are intended for the development of web-based technology and presentation. In many cases, these are provided in the source languages, such as HTML and CSS, which allows one to build upon them without end, if one is willing to put in the time and effort. While suited specifically for quick development, they are also sometimes used in environments that may demand backwards-compatibility with less-recent browsers. 

## Previous Experience: Bootstrap

Prior to working with Semantic UI, I've used [Bootstrap](https://getbootstrap.com/) to quickly design responsive websites. I've previously used both Bootstrap 2 and 3 for smaller projects, and I've found them a bit frustrating to work with, but still preferable (in many cases) to developing without a framework at all. The language used to describe the desired effects can be quite tiresome, as there are a great many descriptors, and they aren't easily readable or interchangeable. The text alignment classes are a great example of those: `.text-left`, `.text-center`, `.text-right`, `.text-justify`, and `.text-nowrap`. These are tiresome to remember, annoying to type, and can be further confused with a separate class of text transformation classes in `.text-lowercase`, `.text-uppercase`, and `.text-capitalized`.

Though its descriptive language carries issues, it has strengths that can outweigh those in many situations. A particular strong-suit of Bootstrap is the ability to create responsive designs that behave somewhat predictably when given sets of resolutions. Classes like `.col-xs-6`, `.col-sm-3`, and `.col.md-2` can be applied to a single element, and allow it to change size and shape as needed with the viewport. These aren't always available in this format, and can be very helpful when working with responsive layouts.

## Previous Experience: Custom framework

I've also had the chance to design a small UI web framework from scratch. While not quite as robust as an open-source project such as Bootstrap or Semantic UI, I designed it with its use-cases in mind, and it served its purpose fairly well. The goals I kept in mind while developing it were:
1. minimal amounts of markup to maintain
2. flexible enough to permit normal presentational markup without workarounds
3. graceful degradation of presentation to descriptive raw content

You can read a little more about that project [here](projects/gloverltd).

## Semantic UI 

More recently, I've had the opportunity to develop in [Semantic UI](https://semantic-ui.com/), a UI web framework that purports itself to be easier to read, use and maintain. Semantic UI is a pretty clear appeal to developers who frequently dabble in design, front-end and back-end development. It tries to marry natural language, a wide suite of design tools, and Javascript integration into one package, and does so adequately.

The natural language involved in describing Semantic UI elements is much clearer, as one might simply add classes of `ui fitted menu container`, and the marked up element will be created as expected. This also helps with other features that are used in modern development environments, such as robust auto-completion and Emmet. Auto-completion terms can be completed much more efficiently when individual keywords can be selected and formed together. Similarly, Emmet shorthand is also much more easily constructed and readable when it can be directly constructed and read in natural language.

A few of the problems I have with Semantic UI include its greediness in markup, performance concerns, and the large variety of terms required to use it. The framework's markup tends to be quite greedy, and often "eats" your own work with regards to child elements, unless explicitly overridden with an `!important` marker. The framework also tends to have issues with large numbers of elements on screen at once, which is quite noticeable on mid-range computers and mobile devices that are viewing a large number of icons at the same time. And while "natural" language is a wonderful tool and a great thing to aspire to, it can be a burden in cases when you must remember which keyword exactly is needed for the job, and often the combinations don't quite work out the way they might be expected to, due to unclear scoping.

Despite these problems, Semantic UI is relatively enjoyable to work with, preferable to no framework in my opinion, and perhaps even more usable than Bootstrap 3, though I've yet to try Bootstrap 4.

## What's Next for the WORLD WIDE WEB?

I've personally grown quite tired of the web in its current state, yolked to the work of its predecessors in HTML and CSS, and constantly making concessions because of it. While it might be some time until we see it, the successor of the web will most certainly come someday, and I'm looking forward to what the future of the web might hold.
