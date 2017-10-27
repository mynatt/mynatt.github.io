---
title: I'll Pass on This Shooting Star
author: Micah Mynatt
layout: essay
type: essay
date: 2017-10-26
labels:
- software engineering
- meteor
- javascript
- frameworks
- reflection
---

Meteor is a full-stack Javascript framework, that lets you make websites and web applications using a shared code-base. I've had the opportunity to try it out a bit, and while I might be a little biased, I'm not a fan of it for a few reasons.

## A Full-Stack Soup

The distinctions between client and server aren't that clear with Meteor. Sure, there are **/client** and **/server** directories that get served to each part individually, but [those are recommended to be minimal anyways](https://guide.meteor.com/structure.html#javascript-structure), with only a **main.js** file living in each as an entrypoint. 

[Most of the code will live in your **/imports** directory](https://guide.meteor.com/structure.html#structuring-imports), which is shared between both server and client, and can be freely imported between them. With a more complicated file and import structure as a more complicated application demands, this can quickly get out of hand. Through habits of working with technology that restricts their usage to one side or the other quite clearly, I prefer a clear separation of purpose and place. The example applications I've seen feel quite clumsy in their file structure, and the lack of boundaries makes me uncertain how you'd go about tidying up such a situation.

## Package Infatuation

I've also mentioned this in my [Meteor Gotchas](http://folio.micah.zone/essays/meteor-gotchas.html) essay, but I'm not a fan of how Meteor places functionality that I would consider core to its main uses inside of external, community-managed packages. This can lead to problems with management, updating, quality control, or all of the above!

The poster-child for this problem is their URL routing. URL routing is the relationship between UI and URLs, and is pretty important when developing websites and web applications. However, Meteor views URLs as essentially unrelated to the semantics and base function, and offloaded that functionality to an external package. That package [has since been abandoned](https://forums.meteor.com/t/flow-router-is-dead-long-live-flow-router/28861/34), yet [is still recommended in the official Meteor guide](https://guide.meteor.com/routing.html). While forks and alternate packages exist for routing, I feel that shouldn't be necessary for core functionality.

## Dissatisfaction

Ultimately, I don't think Meteor is for me. While it tries to play on shared code between server and client as a strength, I can only find it a bit confusing and would rather that distinction remain. I'm not sure a full-stack framework is what I want, nor what I'm looking for. I think, were I to continue to learn more about web technologies on my own, I'd check out something like Express for the backend, and something like React for the front end.