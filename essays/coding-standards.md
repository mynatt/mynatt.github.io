---
title: Coding Without Cruft
author: Micah Mynatt
layout: essay
type: essay
date: 2017-09-21
labels:
- software engineering
- reflection
- coding standards
---

In a modern development environment, coding standards are essential to maintaining your sanity while working on any project, regardless of its size or the number of active developers. This can involve paying attention meticulous details like tab sizes, line breaks, symbol formatting, and even details like line endings. Keeping track of all these details can be necessary, but are time-consuming and tedious to track and correct. In many cases like these, developers opt to use helpful software utilities known as **linters**.

## Linting

The idea of [*linting*](https://en.wikipedia.org/wiki/Lint_(software)) comes from `lint`, a program originally developed for C programs that would statically analyze them and point out inconsistencies and potentially pitfalls that could cause unstable code. Linting programs exist for compiled languages like C++ and Objective C, as well as interpreted languages like Python, Lua and Javascript. Modern linting programs also have settings that allow you to check for formatting and feature usage, to keep in line with coding standards.

Linters can be run through command line interfaces to output analysis of the programs without running them (which might result in unwanted side effects) or compiling them (which might take a very long time). However, more often than not, linters are directly integrated into a developer's workflow, through the use of an **IDE**, or *integrated development environment*, which typically include a code editor through a graphical interface. These integrate directly with different linters, allowing on-the-fly feedback to changes made to code.
 
## The Right Environment

I don't hide the fact that I've disliked most IDEs that I've come in contact with. Too often, the IDEs I've used felt like the result of a million use-cases colliding and forming one giant behemoth of a program. They've tended to be slow and bulky, in my experience, like a large Swiss Army knife with too many utilities to be useful in swift, practical work. Some people use and enjoy the features provided by these environments, and if you happen to be one of them, more power to you. However, I know there are others like me who have a hard time with them.

For personal programming, and most programming in general, I prefer to use a lighter development environment that allows me to integrate the features that I need to for the occasion. For this reason, I prefer [Sublime Text](http://sublimetext.com) to many others. It's an editor with a very performant GUI written in C++, and powerful Python bindings that have lead to a very rich plugin ecosystem. It offers quick access to these through a third-party plugin manager called [Package Control](https://packagecontrol.io/), which lets you install, manage, and automatically update plugins directly in Sublime. 

Contrary to the approach taken above in most modern IDEs, Sublime provides a tight set of features that any developer can appreciate regardless of their language. These include a variety of color schemes, configurable key-bindings, a powerful find-and-replace feature for projects using RegEx, a customizable build system, and many more beyond that. And should a developer find the feature set wanting for the language they're working on, a quick dip into the plugins on display likely amends those problems.

Regardless of the development environment or language used, clean code that's comprehensible and more likely to work is useful to everyone. It's for that reason that every developer should at least consider the use of a linter or similar quality control system in their work, and should come up with their own set of standards to hold themselves to during the development process.