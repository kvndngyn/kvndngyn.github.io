---
layout: essay
type: essay
title: Stay Organized and Productive
# All dates must be YYYY-MM-DD format!
date: 2020-02-13
labels:
  - Coding Standards
---

<img class="ui centered fluid rounded image" src="../images/codingStandards.png">

## Understand Instantly

Have you ever had trouble reading someone else's code? What if there was a way to make it so that it would be easier? Now, what if I say that there already is a way to make it easier? By setting a coding standard, it means that a code you make will most likely be similar to a code someone else did. By setting and learning a coding standard, it makes things a lot easier to read as it follows a guideline that you are also following. For example, lets take the following from the [airbnb guide](https://github.com/airbnb/javascript#the-javascript-style-guide-guide):
```javascript
// bad
const foo = a && b < 0 || c > 0 || d + 1 ===0;

// good
const foo = (a && b < 0) || c > 0 || (d + 1 === 0);
```
Looking at it, you can tell that both do return the same result, but which one was faster and easier to read? In the bad example, we see a bunch of symbols but we need to look try and split them up from the "or (||)" and then we have to find out what each one does. There is still a bunch of symbols for the good example however, you can instantly tell what each argument is trying to ask for.

## My Experience with ESLint

So far, after a week of using ESLint, I find it really useful to keep my style consistent. There are times where I wouldn't have the whitespace I would want or maybe I declared a variable with "let" when I could just use "const". ESLint conforms to my style of writing code and I have adjusted well into getting used to it. Seeing that green check mark helps reassure me that I am being consistent in my writing and I am doing one thing one way and another thing another way. Thinking ahead, I know that if I ever look back at my code in the future, I will easily be able to read it and remember what it does. I believe that ESLint will help me not only stay organized in my programming, but also help me stay consistent in other matters as well. By forcing myself to stay consistent and seeing this organization, it just becomes eye opening to see the effects it has on your productivity. If you are looking for something, you will know where to find it.
