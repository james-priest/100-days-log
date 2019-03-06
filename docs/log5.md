---
title: 100 Days of Code - Round 5
description: by James Priest
pg_bk_color: '#e6e8de'
header_bk_color: '#1a7f6d'
link_color: '#1a7f6d'
---
<!-- markdownlint-disable MD022 MD024 MD032 MD033 -->

# James Priest
<p class="toc"><a href="./index.html">&lt;– back to Table of Contents</a></p>

## 100 Days of Code

| Log 1 | Log 2 | Log 3 | Log 4 | Log 5 |
| --- | --- | --- | --- | --- |
| [Round 1](https://james-priest.github.io/100-days-of-code-log/) | [Round 2](https://james-priest.github.io/100-days-of-code-log-r2/) | [Round 3](https://james-priest.github.io/100-days-of-code-log-r3/) | [Round 4](https://james-priest.github.io/100-days-of-code-log-r4/) | this log |

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

## 7. React Redux Tutorial Pt 4
### Day 7: March 5, 2019 - Tuesday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](assets/images/day7-small.jpg)](assets/images/day7.jpg)<br>
**Live Demo:** [React Redux Thunk](https://codesandbox.io/s/84o941vx4j?fontsize=14) on CodeSandbox

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

Today I went through the last part of a tutorial called

- *[React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)*

This focused on introducing redux-thunk middleware which allows asynchronous operations to work with Redux. Some of the specifics around redux-thunk are:

- Normally action creators are limited to returning an object.
- Redux Thunk is middleware that allows action creators to return a function.
- Promise-based asynchronous operations can be conducted in the action creator.
- Actions can be dispatched from the action creator as well.

Here's a sample of async code used  in the action creator.

[![Redux](assets/images/day7a-small.jpg)](assets/images/day7a.jpg)

**Links:**
- Live Demo - [React Redux Thunk](https://codesandbox.io/s/84o941vx4j?fontsize=14) on CodeSandbox
- GitHub Repo - [react-redux-middleware](https://github.com/james-priest/react-redux-middleware)
- Tutorial - [React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---

## 6. React Redux Tutorial Pt 3
### Day 6: March 4, 2019 - Monday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](assets/images/day6-small.jpg)](assets/images/day6.jpg)<br>
**Live Demo:** [React Redux Middleware](https://codesandbox.io/s/0oj8rqmo70?fontsize=14) on CodeSandbox

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

Today I went through the third part of a tutorial called

- *[React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)*

This focused on introducing Redux middleware in order to provide logic to our dispatched actions. It provides the following benefits.

- the logic can live outside React (or any other library/framework)
- middlewares become reusable pieces of logic, easily to reason about
- middlewares can be tested in isolation
- we keep the components clean

In this example I intercept an ADD_ARTICLE action after dispatch and check for the presence of unwanted words.

[![Redux](assets/images/day6c-small.jpg)](assets/images/day6c.jpg)

If a forbidden word (such as 'money') was found then the FOUND_BAD_WORD action was dispatched instead. It was then handled by our reducer.

Testing out the logic filters out entries with unwanted words.

[![Redux](assets/images/day6b-small.jpg)](assets/images/day6b.jpg)

Our state is displayed using Redux DevTools.

[![Redux](assets/images/day6a-small.jpg)](assets/images/day6a.jpg)

**Links:**
- Live Demo - [React Redux Middleware](https://codesandbox.io/s/0oj8rqmo70?fontsize=14) on CodeSandbox
- GitHub Repo - [react-redux-middleware](https://github.com/james-priest/react-redux-middleware)
- Tutorial - [React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---

## 5. React Redux Tutorial Pt 2
### Day 5: March 3, 2019 - Sunday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](assets/images/day5-small.jpg)](assets/images/day5.jpg)<br>
**Live Demo:** [React Redux](https://codesandbox.io/s/v3ykn3oo5?fontsize=14) on CodeSandbox

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

Today I went through the second part of a tutorial called

- *[React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)*

[![Redux](assets/images/day5a-small.jpg)](assets/images/day5a.jpg)

This focused on combining Redux & React with the react-redux package and doing the following:

- Wrapping the app with a `<Provider>` HOC (Higher Order Component)
- Calling `connect()` on any components we want to connect to Redux
- Using `mapStateToProps` and `mapDispatchToProps` to allow us to access state and dispatch from a React component's props.  

This was put into practice by creating an App, List, and Form component.

- App -  parent component containing List and Form. App is wrapped with `<Provider>` to allow React to access Redux store.
- List - used `mapStateToProps` to display titles from Redux store (state).
- Form - used `mapDispatchToProps` to dispatch ADD_ARTICLE action and update the store.

**Links:**
- Live Demo - [Redux Redux](https://codesandbox.io/s/v3ykn3oo5?fontsize=14) on CodeSandbox
- Tutorial - [React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---

## 4. React Redux Tutorial Pt 1
### Day 4: March 2, 2019 - Saturday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](assets/images/day4-small.jpg)](assets/images/day4.jpg)<br>
**Live Demo:** [Redux in console](https://codesandbox.io/s/9z2py96vqo?fontsize=14) on CodeSandbox

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

Today I went through the first part of a tutorial called

- *[React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)*

This first half focused on the basic elements of Redux and using it in console.

- The store
- Getting state
- Subscribing to state changes
- Dispatching actions

[![Redux](assets/images/day4a-small.jpg)](assets/images/day4a.jpg)

The next part will deal with connecting Redux and React together.

**Links:**
- Live Demo - [Redux in console](https://codesandbox.io/s/9z2py96vqo?fontsize=14) on CodeSandbox
- Tutorial - [React Redux Tutorial for Beginners: The Definitive Guide (2019)](https://www.valentinog.com/blog/redux/)
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---

## 3. Create Log Template Repo
### Day 3: March 1, 2019 - Friday

**Project:** 100 Days of Code Log  Template

[![new code log](assets/images/day3-small.jpg)](assets/images/day3.jpg)

**Progress:** Created a new GitHub repo for my 100 Days of Code Log Template project.

I quickly realized that I needed to create a separate master template repo from the one I had my current log in.

Separating the template from the log allows me to update my log without in affecting the template and update the template with affecting the log. This way anyone following changes on the template won't be notified on every log commit I make.

Additionally, any changes to the template or template instructions can the be pulled down without overwriting my log entires.

**Links:**
- GitHub repo - [https://github.com/james-priest/100-days-log-template](https://github.com/james-priest/100-days-log-template)
- Demo Site - [Sample Template Site](https://james-priest.github.io/100-days-log-template/log1.html)

---

## 2. Redux, JS, & HTML UI
### Day 2: February 28, 2019 - Thursday

**Project:** [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

[![Redux](https://james-priest.github.io/udacity-nanodegree-react/assets/images/rr32-small.jpg)](https://james-priest.github.io/udacity-nanodegree-react/assets/images/rr32.jpg)<br>
**Live Demo:** [Redux Todo Goals App](https://codesandbox.io/s/42zkzvrn14?fontsize=14) on CodeSandbox

**Progress:** Continued Udacity Redux lesson for my React Nanodegree Program.

This lesson focused implementing Redux with vanilla JavaScript and a simple HTML UI.

The kept the focus limited to:

- The store
- Getting state
- Subscribing to state changes
- Dispatching actions

You can read more in my notes: [Udacity React & Redux - 2.4 Introducing Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#24-introducing-redux)

**Links:**
- Live Demo - [Redux Todo Goals App](https://codesandbox.io/s/42zkzvrn14?fontsize=14) on CodeSandbox
- Repo - [Redux Todos & Goals App](https://github.com/james-priest/reactnd-redux-todos-goals/tree/master) on GitHub
- Course notes - [Udacity React & Redux](https://james-priest.github.io/udacity-nanodegree-react/course-notes/react-redux.html#react--redux)
- Link to [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019)

---

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