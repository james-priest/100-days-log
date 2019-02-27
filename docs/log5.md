---
title: 100 Days of Code - Round 5
description: by James Priest
pg_bk_color: '#e6e8de'
header_bk_color: '#1a7f6d'
link_color: '#1a7f6d'
---
<!-- markdownlint-disable MD022 MD024 MD032 MD033 -->

[<-- back to Log Table of Contents](../index.html)
# James Priest

## 100 Days of Code

| Log 1 | Log 2 | Log 3 | Log 4 | Log 5 |
| --- | --- | --- | --- | --- |
| [100 Days Round 1](https://james-priest.github.io/100-days-of-code-log/) | [100 Days Round 2](https://james-priest.github.io/100-days-of-code-log-r2/) | [100 Days Round 3](https://james-priest.github.io/100-days-of-code-log-r3/) | [100 Days Round 4](https://james-priest.github.io/100-days-of-code-log-r4/) | this log |

## Challenge & Commitment
This is part of Alexander Kallaway's [100DaysOfCode](https://github.com/Kallaway/100-days-of-code "the official repo") challenge. More details about the challenge can be found here: [100daysofcode.com](http://100daysofcode.com/ "100daysofcode.com").

**Commitment:** *I will code daily for the next 100 days.*

|  Start Date   | End Date     |
| ------------- | ------------ |
| February 25, 2019  | - - - |

## Goals

- [x] Code daily
- [x] Successfully complete Udacity's [React Nanodegree](https://www.udacity.com/course/react-nanodegree--nd019) program

# Code Log

---

<!-- 
## 100. Redux - UI + State
### Day 100: February 24, 2018 - Sunday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](https://james-priest.github.io/udacity-nanodegree-react/assets/images/rr31-small.jpg)](https://james-priest.github.io/udacity-nanodegree-react/assets/images/rr31.jpg)<br>
GitHub Repo: [Redux Todos & Goals App](https://github.com/james-priest/reactnd-redux-todos-goals/tree/master)

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

This lesson focused on connecting a UI to our store. It provided the following:

- Clicking the Add button dispatches AddTodoAction and adds item to the store.
- Store Subscription allows updates to the DOM with new state whenever state changes.
- Marking an item as complete dispatches the toggleTodoAction.
- Clicking delete button dispatches removeTodoAction.
- Similar functionality was created for Goals.

Here's the subscribe code that loops through each store item and updates the DOM

```js
store.subscribe(() => {
  const { todos, goals } = store.getState();

  document.getElementById('goals').innerHTML = '';
  document.getElementById('todos').innerHTML = '';

  todos.forEach(addTodoToDOM); // todos.forEach(todo => addTodoToDOM(todo));
  goals.forEach(addGoalToDOM); // goals.forEach(goal => addGoalToDOM(goal));
});
```

You can read more in my notes: [Udacity React & Redux - 2. UI + Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#2-ui--redux)

**Links:**
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---
 -->

## 1. Round 5 Code Log & Repo
### Day 1: February 26, 2019 - Tuesday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![new code log](assets/images/day1-small.jpg)](assets/images/day1.jpg)

**Progress:** Created a new GitHub repo for my Round 5 code log.

This repo is redesigned so that it can be forked and cloned for others to use. I'm still in the process of writing out the README to cover the following areas

- installation instructions
- usage instructions
- customization
- image optimization
- set-up & testing

**Links:** My GitHub repo [https://github.com/james-priest/100-days-log](https://github.com/james-priest/100-days-log)