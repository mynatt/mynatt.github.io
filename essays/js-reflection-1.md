---
title: Timed Testing, the Flipped Classroom and the Usefulness of Memorization
author: Micah Mynatt
layout: essay
type: essay
date: 2017-08-29
labels:
- software engineering
- javascript
- reflection
---

This Fall 2017 semester, I'm taking a software engineering class that takes a slightly unorthodox approach to teaching, homework assignments, and testing. I have prior experience with Javascript, the language of choice in the class, which gives me a slight advantage in the class regardless of the teaching style. The ideas this class attempts to use have promise, but I believe that their current approaches are more harmful to the learning experience than they are helpful, and the execution leaves a lot to be desired.

The learning methods used in the class fundamentally conflict with the rest of the course, and are hurt by the assignments and testing methodology used. And although this modified way of teaching offers certain benefits, it's also constructed and proctored in a way that doesn't realistically reflect actual development practices. This can be demoralizing to students who don't have a tight grasp on new syntax or run into a particularly frustrating bug. I'd like to outline the ways the class currently functions, and discuss some ways I believe could alleviate these problems, based on my current experiences in the class and what I've observed so far.  

## Timed Testing
Some of the assignments and quizzes (which I'll refer to as *tests* for simplicity's sake) in the class are timed, with different tiers for performance. This presents an interesting challenge initially, but I believe it's unhelpful in the long run. It eventually turns into a test of how well you can remember what you did the previous attempt, and how quickly you can type. These are useful skills, certainly, but I think they are less useful at proving competency in accomplishing a task. They also don't necessarily encourage changing behaviors or techniques significantly to improve your code.

Another weak aspect of the timed tests currently provided is they don't have concrete inputs and outputs to do testing against, even informally. These can be calculated manually, but it would be much easier for students to know they're on the right track or have successfully completed their task if they had inputs to test with, and then knew the corresponding outputs to expect. This is very common in task-based programming tests.

The testing process currently shows a few very specific weak point of the timed testing. Currently, timed tests are administered in a common room, with all students starting simultaneously. The time taken completing the task directly correlates with the grade received on it, so students are encouraged to complete the task correctly as quickly as possible. On completion, students call attention to themselves, have their time recorded, and then exit the room, presumably to prevent test interference and allow for discussion. However, the quizzes also have a maximum time limit: if the time limit is reached, the students remaining receive a "did not finish" score, and the students who finished are called back into the class. 

This form of test administration is problematic because of the pressure and stress it applies on students, and the effects it can have on morale. Well-performing students quite visibly finish before their peers. This can leave the impression that "the material should be very easy", lowering the morale of those who might not immediately come up with a solution. Students who may be having trouble will eventually be left alone in the room as time runs out. Being singled out as receiving a poor grade in this way can be extremely demoralizing, as not only do they have the knowledge that they failed to finish, but those who return to the class can also clearly see who failed to finish.

My proposal to alleviate this problem is as such:
- Turning in the URL to the JSFiddle should be submit through a Sakai assignment, or a [Sakai test](https://www.sakaiproject.org/test-and-quizzes). When paired with the known start time of the test, this will allow minute-interval tracking of progress, and won't require intervention on behalf of the test administrator on completion, allowing other students to continue working uninterrupted and without distraction.
- Students will submit their URL on completion, and then either turn off their display or set their computer to sleep, withdrawing their hands from the keyboard. While this doesn't allow students to interact immediately after the test, this should maintain a steady work environment, allowing other students to complete their work without the pressure and morale hit that accompanies their peers leaving the room.

## Flipped Classrooms
The main problem with the flipped classroom I've experienced is that the base material is learned through FreeCodeCamp, via a collection of exercises with outputs to test against. This has problems of its own, including the lack of ES6 support, which puts it at ends with the ES6 syntax required by the rest of the class. Combined with timed testing, students are implicitly trained and encouraged to blow through the material as quickly as they can. This can result in students poorly absorbing core concepts. I don't think this method of learning the core material is compatible with the structure of the rest of the class.

I don't currently have a proposal to alleviate this problem. Teaching the language material in class would be helpful to an extent, but I think comes with its own problems as far as pacing goes. A more compatible learning system may be helpful, but still has conflicts with the timed testing methodology. Ultimately, timed-assignment style learning that covers the breadth of the language material might be the most fitting way to learn the material, but this comes with its own problems. 

## Useful Memorization
While memorizing and practicing core concepts are vital to effectively and efficiently programming, I don't believe that language syntax and specifics should fall under that same umbrella. Because of this, I propose a basic outline of syntax and basic built-ins/libraries should be provided and usable during timed assignments and testing. This doesn't need to be in-depth on their usage or why you'd use them, but at least provide a reference on what and how to use. The class currently encourages the use of the [Airbnb](https://github.com/airbnb/javascript) style guide, which also outline some core syntax in a helpful way.

The proposed syntax card could be written in a simple way, similar to those written for the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript). For example:
```js
let theta = 0;   // can reassign
const pi = 3.14; // can't reassign
const map = {change: "me"};  // can't reassign, but can mutate

let arr = [1, 2, 3];
arr.push(4); // arr = [1, 2, 3, 4]
let a = arr.pop(4); // a = 4, arr = [1, 2, 3]

let obj = {key1: 1, "key2": "value2"};
for (const key in obj) { // works on arrays and objects
	console.log(key); // prints: "key1", "key2" 
}
for (let val of arr) { // works on iterables like arrays, but not objects
	console.log(val); // prints: 1, 2, 3
}
```

I know not everyone would agree with the inclusion of a syntax or language reference during assignments or testing. However, in my personal experience, it's much more realistic to have such a resource on hand and be able to refer back to it when required during a task. Very rarely is one locked in a room with only a text editor and command prompt, free of any helpful materials that might lend even the slightest of "hints".

## Final Remarks

I believe the methodologies in use for this class hold serious promise, and I have found myself enjoying the class so far, despite some of the execution flaws. However, I believe by adopting my proposals, the beneficial properties of learning the material in a "trial by fire" could be kept, while minimizing the unnecessary stresses placed on the students, and allowing them a chance to gain gradual familiarity with the language syntax while exercising core concepts.

*UPDATE 2017-09-02: I mistakenly demonstrated the `for..of` loop on an object, believing it to work on both objects and arrays. It does not. I think this error came from my experience with Lua, and the similar `for _,v in pairs(obj) do .. end` syntax, which does work on objects. This error has been corrected.*
