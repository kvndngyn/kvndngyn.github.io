---
layout: essay
type: essay
title: "Jack of All Trades"
date: 2020-04-30
labels:
  - Software Engineering
  - Design Patterns
---

## The Blueprint

The beauty of design patterns is the versability of its usage. It is never a finished design that overcomes one problem but rather a template of how to solve problems for many situations. These patterns are for commonoly occurring problems in software engineering that creates a systematic way of solving a particular problem. This is not to be confused with functions or algorithms which can be copied into your program or give you a clear set of instructions of what to do. Rather, design patterns help allow you to systematicaly approach problems to find a solution. An amazing analogy used by [Refactoring Guru](https://refactoring.guru/design-patterns/what-is-pattern) is as follows:
>>>An analogy to an algorithm is a cooking recipe: both have clear steps to achieve a goal. On the other hand, a pattern is more like a blueprint: you can see what the result and its features are, but the exact order of implementation is up to you.

The benefits of learning these patterns is that you can use commonly known terms such as Factory, Singleton, Observer, or Model-View Controller (MVC) to communicate with other devlopers. Short explanations for these are: 
* Factory: creates objects without exposing underlying logic, potentiall returning objects associated with different classes, and/or creating dependent objects.
* Singleton: provides a global variable in an object oriented language that does not support global variables.
* Observer: when a set of objects needs to be informed whenever a change in state occurs to another object.
* Model-View Controller (MVC): internal represenation of information from the way it is presented to and accepted from the user.

## The Club and its Members

Before learning about design patterns, I was blinded by the fact that it was being used in my projects throughout my software engineering course. However, after learning about it, it becomes clear how relevant it is to my current project, more specifically, Observers. With Obervers, it helps design a general problem of objects interacting with another. This is relevant in the Mongo Database where we publish and subscribe data. When we subscribe to a data, we want to follow any changes or updates made to the publisher. Making this more relevant to my current project with [CL-UH-B](https://github.com/cl-uh-b), which consist of Singletons, Observers, and MVC. On a page, we will subscribe to our collection of clubs allowing the page to load the data and display it to the user. If the user is an admin, they can interact with this data in a frontend manner which allows them to easily make modifications to their specific club. Since multiple pages are subscribed to the publisher, when that admin made that update, all subscribing pages were updated along with it. This is useful because instead of changing each page one-by-one, the admin can easily go to one page, make an edit, and update it so that anyone viewing it will be able to see it. So where was it present?:
* Singleton: The list of clubs (database)
* Observer: The subscription and publication
* MVC: The interaction of the user and collection 