---
layout: project
type: project
image: images/rpsMain.png
title: Rock-Paper-Scissors
permalink: projects/RPS
# All dates must be YYYY-MM-DD format!
date: 2019-10-10
labels:
  - Rock, Paper, Scissors
  - C
  - Game
summary: A rock, paper, scissor game made in C where users can verse a computer. 
---

<img class="ui image" src="{{ site.baseurl }}/images/rpsSub.png">

This project was made to complete the challenge of making a simple rock, paper, scissor game where a user can verse a computer. To do this, I implemented a random number generator so that the computer choices were alwasy completely random and not following a set routine. Here is how it was done:
```c
/**
 *Randomly generated computer selection from 0-2.
 *0: Rock, 1: Paper, 2:Scisscors
 */
char getComputerChoice(){
  srand(time(NULL)); //initialize RNG
  int i = rand() % 3; 
  //Switch case to apply RNG
  switch(i){
  case 0:
    return 'r'; //Computer chooses rock
  case 1:
    return 'p'; //Computer chooses paper
  case 2: 
    return 's'; //Computer chooses scisscor
  }
}
```
The only real difficult challenge I ran into during the creation of this simple game was the user's choices and determining if the user won or if the computer won. To solve this problem, I created a nested if statement that first checked to see what the user inputted. If they put in a choice for rock, paper, or scissors, the game continued. If the user put in 'q' for quit, the game exited and would stop running. To fix the error of the game crashing on a wrong input, it was done in the else statement to print a simple statement letting the user know that they put in something wrong. Inside the first if statement I stated, were all the choices. This was just comparing each choice the user made and what the computer choice was. When it found out the winner, it incremented that score of the user, computer, or tie by 1.

The take away from this project was what I learned about how random number generators work in C.  You first have to initialize it before you can actually use it. it used ```c srand(time(NULL))``` to first initialize it, then used ```c int i = rand() % 3``` to create a random number between 1 - 3. The reason the numbers just had to be 1 - 3 was just so it was assigned a number for each choice possible. By doing so, I was able to use a switch statement to make the computer return a choice.

Source: 
