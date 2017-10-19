---
layout: essay
type: essay
title: "Final Project Idea"
date: 2017-10-19
labels:
  - Software Engineering
  - Meteor
---

## Gym Partner

Gym Partner is a proposed final project idea that functions as a UH-specific fitness network, to promote the gym and its many offerings. Users will give their fitness information and schedules, and can organize with like-minded individuals and groups.

### Build a Profile

A typical user profile might include information such as:
 
- Hobbies
- Sports
- Weight Class
- Schedule

and based on this information, users will be able to experience the rest of the application.

### Connect With Friends

Users will be able to add existing friends based on other social networks such as **Facebook** and **Instagram**, and organize groups based on their collective interests.

### Make New Friends

Users will also be able to match with other students based on the information provided in their profiles. This gives them the opportunity to connect with other students with similar interests, and provides an outlet for communication at the gym, fostering a collective identity rather than isolated exercise environments.

### Organize Events

Users will be able to create and organize events in their groups or with their friends, and make them public, allowing other users to find and join them in the gym.

## Technical Details

### Mockup Page Ideas

```
/index
/connect
/events/:id
/groups/:id/:action
/users/:id
```

### Use Case Ideas

- New user registers for service: 
	- Homepage > Register > UH Login > New Profile > Connect
- Not-logged-in user tries to view events: 
	- Homepage > Events (Not Logged In) > Login > UH Login > Events
- Checking group-page for new updates: 
	- Homepage > Login > UH Login > Groups (Updates)

### Beyond the Basics

- Social media functionality (posting, viewing, and interacting with user updates that are based on their activities)
- Event administration connected with UH facilities and APIs
- Restrictions on disallowed events (event approval)
- Connectivity with existing social media
