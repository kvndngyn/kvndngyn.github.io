---
layout: essay
type: essay
title: Quick, Concise, and Beautiful
# All dates must be YYYY-MM-DD format!
date: 2020-02-27
labels:
  - User Interface
  - Framework
  - Semantic UI
---

<img class="ui centered fluid rounded image" src="../images/semanticUI.png">

> ### *User Interface (UI):*
> *The means by which the user and a computer system interact,* 
> *in particular the use of input devices and software.*

## Frameworks: Where Do Software Engineers Benefit?
Starting off, frameworks are an amazing way to make your websites more friendly to the eyes in a quick and simple manner. It is the frame of what you are trying to accomplish and you can continue to keep building on it as wanted. Sure, you can reach the same website design in the end with raw HTML and CSS, but why make something more complicated than it needs to be? Why not implement a framework to assist you with doing the same thing in a lot less time? Every line spent styling raw HTML with raw CSS can most likely be done in one line with frameworks (and it'll look a lot better too). Take this example of creating a navigation bar:
```html
Raw HTML
<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>
```
```css
Raw CSS
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}
```
It can be done in a framework (ex. in [Semantic UI](semantic-ui.com)) like this:
```html
<div class="ui three item menu">
  <a class="active item">Editorials</a>
  <a class="item">Reviews</a>
  <a class="item">Upcoming Events</a>
</div>
```
These two accomplish the same goal of creating a stylish navigation bar to not pain the eyes of the user using their website. However, as you can tell, raw HTML and CSS took a lot more lines to do than a framework. I think this sufficiently covers how Software Engineers greatly benefit from this.

## Learn a "New Language"
My experience so far with [Semantic UI](semantic-ui.com) has definetely impacted my joy of creating websites. Learning raw HTML and CSS was cool, but the results I got were horrendous. It looked like a site that was made back when the internet was just starting to get popular. Going from raw HTML and CSS to a framework such as Semantic UI, there were some "new language" I had to learn specific to it. Now I quote new language because it was pretty much just telling what you want the website to do and the framework will do it for you. An example I enjoyed from [Pluralsight's](www.pluralsight.com) course on Semantic UI was how you would describe a dog. When you see a large brown dog, you would describe it as a "large brown dog". You wouldn't describe it as "dog brown-dog large-dog". So while yes there were some new language to Semantic UI, it pretty much felt like I was just telling it what to do and it would do it. It is a bit picky on how you order the words, but once you get over that, it feels like I am typing for an English class.

If there is anything that should have been taken away from this, its not that raw HTML and CSS are terrible and frameworks are always better. In fact, its not even about comparing which one is better but rather which is more efficient when building a website from scratch. Raw HTML and CSS are defintely a great foundation to start at and layout when starting to learn how to build a website. Once you understand that, then it would be a good time to start learning a framework. There are numerous amounts of frameworks out there, just find one that is your style and go for it.