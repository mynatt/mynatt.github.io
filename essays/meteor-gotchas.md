---
title: Meteor Gotchas
author: Micah Mynatt
layout: essay
type: essay
date: 2017-10-19
labels:
- software engineering
- meteor
- javascript
- frameworks
- reflection
---

Meteor is a Javascript application and website framework, and is full-stack, meaning you can use it to develop for both the client and server portions of code. Developing in it can be efficient and enjoyable, but the structure and form of the framework can lead to confusion or irritation if you go into it having certain expectations of what a Javascript framework should do. While these can vary in number depending on the developer, I'd like to outline two specific incidences I've run into while learning Meteor.

## Needlessly Complicated Standard File Structure

The file structure for Meteor typically includes **client** and **server** folders, each with a **main.js** file. The documentation allows for protection on these files, and insists that the majority of application code is in a separate folder called **imports**, which typically has its own strange structuring. They allow the structure of the folders up to you, while imposing certain rules that may make it untenable to actually use those different formats.

While I understand that leaving these options more open can allow for greater developer freedom in certain situations, I feel that the vast majority of applications don't benefit from these and are actually a hinderance. If instead the structure included a **client.js** and **server.js** files, and allowed the other directory structures to be completely  protected and up to you, I think more developers would find that enjoyable to use and develop in. 

## Preference to Packaging

Depending on what frameworks you're familiar with, you might have come to expect certain features. Some might prefer the approach of leaving "unnecessary" code and features to packages that might better encapsulate them and remove dependencies that might not be required for your current project. However, I feel that Meteor does this in a misguided way, removing core functionality and semantics of the client-side of the web, while still touting itself as a full-stack framework.

The prime example that comes to mind is routing, the mutual reflection of UI and navigation on URLs. Meteor does not ship with routing, as it [views URLs as essentially unrelated to the semantics and base function of Meteor](https://guide.meteor.com/routing.html). However, they acknowledge that it's important to many who build web applications and webpages because of the existing application stacks and expectations therein. For this reason, it's bundled in a separate package called FlowRouter. This might be 

## The Good News

Despite the gotchas outlined above and the ones left unsaid, Meteor seems to remain a perfectly functional and practical framework that can be used to develop websites and applications in a timely manner. While I continue to learn it, I expect to stumble upon many more "gotchas", and hope that these don't greatly impact its usefulness.