---
layout: essay
type: essay
title: "The Growing of a Developer"
date: 2020-05-14
labels:
  - Software Engineering
---

## A Very Brief Introduction

What a wonderful learning experience it was to learn about functional programming, user interface frameworks, and when it came to group project, learning agile project managment is important. Over the course of a semester, my knowledge and love for programming has greatly increased as I have learned various new approaches to a problem. With functional programming I learned new ways to face problems that I have faced before. With user interface frameworks such as [Semantic UI](https://semantic-ui.com/) I learned to easily build an app that looks nice without the stress of doing a bunch of CSS. Finally, agile project management is important to not only be organized, but a way to communicate with your team even when not directly communicating to each other.

## Functional Programming

[UnderscoreJS](https://underscorejs.org/) is amazing. It is a JavaScript library that provides helpful functions that turns a piece of code of 7 lines into a piece of code of 3 lines. Take for example the summing of values in an array. Traditional programming will call for doing something such as a for loop, while loop, or even recursion. Of course, this problem can be achieved this way but it becomes a lot of work to code it out. Here is my example of using a for loop:
```javascript
function sumFor(lists) {
  let total = 0;
  for (const list of lists) {
    total += list;
  }
  return total;
}
```
Now if it works, it works. However, I enjoy the challenge of making my code as simple as possible for not only myself to understand but for other developers to understand as well. If we take a look at UnderscoreJS' documentation, we can find the [reduce function](https://underscorejs.org/#reduce). What this allows us to do is to take a list of values and to return a single value. To do this, we pass the array into the first parameter of reduce and then we pass a function into the second parameter. Now the cool thing about JavaScript are arrow functions which can help simplify it even more. Instead of `function(a, b) { return a + b; }` we can write it as `(a, b) => a + b`. Now to put all this together, we can simplify the code above by implementing UnderscoreJS as follows: 
```javascript
function sumTheSimpleWay(lists) {
  return _.reduce(lists, (memo, num) => memo + num);
}
```

## User Interface Frameworks

Semantic UI is a development framework that can create responsive layouts. It is an amazing way to get started on making a page of the 90s look more modern. Let's say for example we want to create a red button. Using vanilla HTML and CSS we will do it as such:
```html
HTML
<button class="red-button">Red Button</button>
```
```css
CSS
.red-button {
  border: none;
  color: white;
  padding: 15px 32px;
  font-size: 16px;
  margin: 4px 2px;
  background-color: red;
}
```
Now compare that to using [Semantic UI buttons](https://semantic-ui.com/elements/button.html) where all you need to do is import the framework and type:
```html
<button class="ui red button">Red Button</button>
```
Both of them produce similar results although the styling may differ slightly. To be an efficient programmer, do not be afraid to use frameworks to help as it will save not only time, but the stress of making something look the way you want it to. 

## Agile Project Management

For project management, the guidelines I follow are [Issue Driven Project Management Guidelines (IDPM)](http://courses.ics.hawaii.edu/ics314s20/morea/project-management/reading-guidelines-idpm.html). This is an amazing way to organize the porject because it fit the criterias of being a small team (less than 12) approach, and for a shorter term project of about a month. During the process of learning this, I also learned about creating [GitHub Project Boards](https://help.github.com/en/github/managing-your-work-on-github/about-project-boards) which allowed me and my group to easily create issues for each other to handle. The best thing about this guideline (in my opion) is that each task should only take 2-3 days to complete. If it took any longer, we knew the issue may be a bit more than expected and can easily break it down into smaller task. This helped the efficiency because, if any other developers are like me, I would continue to tackle an issue for a long time before asking for help. However, if my team noticed that I spent quite a while on the task, they can offer help or I can ask to break down the issue to smaller parts. It could be an issue where the searching works but breaks another function and can be easily fixed by breaking this down into two tasks. First to get the search function working then the second task of getting it working with everything else. With larger projects guidelines may differ, but the amazing part of an agile project management is to efficiently work with a team to accomplish the same goal.