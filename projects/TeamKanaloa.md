---
layout: project
type: project
image: images/kanaloa.jpg
title: Team Kanaloa
permalink: projects/team-kanaloa
# All dates must be YYYY-MM-DD format!
date: 2020-12-08
labels:
  - UH Manoa VIP
  - Team Kanaloa
  - Autonomous
  - Virtual Robotics
summary: My contribution to Team Kanaloa's efforts in the Virtual Ocean Robotics Challenge
---

<img class="ui image" src="{{ site.baseurl }}/images/cora_front.png">

## Overview
Team Kanaloa is a Vertically Integrated Project (VIP) at the University of Hawai'i at Manoa. This team is split into multiple subsystems and for this case, I will be focusing on my contribution to the Sensor Fusion Subsytem. During the Fall 2020 semester, there was a virtual competition called Virtual Ocean Robotics CHallenge (VORC) that challenges teams to develop autonomous code to control a vessel model that they provide. The competition uses [Robot Operating System (ROS)](https://www.ros.org/) as the software to develop our virtual robot and [Gazebo](http://gazebosim.org/) to run our simulations. For ROS, the specific distribution used was Melodic which is ran in Ubuntu 18.04. 

## My Contributions
For this team, I helped with image labeling which would later be given to our neural network to help train it in object detection. I also handled submissions for our team through the use of [GitHub](https://github.com/) and [Docker](https://www.docker.com/).

#### Neural Network
For the Neural Network, our team utilizes [Darknet](https://pjreddie.com/darknet/) with [You Only Look Once (YOLO)](https://arxiv.org/abs/1506.02640) to help with object detection. To train it, others and I had to first manually label images taken from the simulation. We had to label totem's, surmarks, and polyforms ([details of the object](https://raw.githubusercontent.com/wiki/osrf/vorc/files/VORC2020_task_descriptions_latest.pdf)) in [labelImg](https://github.com/tzutalin/labelImg). This application creates a YOLO file which is formatted like this: 
```
2 0.445703 0.301389 0.036719 0.058333
2 0.557031 0.362500 0.026562 0.041667
2 0.826562 0.281250 0.020313 0.029167
1 0.745313 0.306944 0.026562 0.100000
1 0.720313 0.271528 0.012500 0.054167
0 0.946094 0.288194 0.028125 0.073611
1 0.819922 0.250694 0.007031 0.026389
1 0.939063 0.256944 0.012500 0.038889
```
The first column of numbers are assigned to one of the objects and will vary depending on how the configuration file for the application is. The numbers following that are the positions of the object. This was given to the neural network to detect the different objects so that we can further develop code to create autonomous object detection. 

#### Submissions
For submissions, I did the GitHub and Docker side of it. These submissions would have not been possible without the help from the other members of the Sensor Fusion team members. VORC had two phases, one to submit a video link demostrating what our team has accomplished at the time (phase 1), and the other a link to the image containing our workspace (phase 2). In phase 1, it was a simple process of the team creating a short video demostrating what we were or have accomplished. This video link would be submitted by first forking their main repository on GitHub. We then create our own folder and text file containing that video link for them to view. The real competition takes place with the Dockerhub image. This was my first taste of Docker and its capabilities, but essentially, we pull their ROS Melodic base image with comes with the neccessary packages we need. Using that, we add our own scripts that would execute on startup. This first bash script would source all of the necessary files so that it can run the simulation then pass it onto another bash script to run the system. The real competition begins when the second script executes a python script which determines what the current task is and executes the appropriate python code for that task. 

Quick Links:

<a href="https://www.oceanroboticschallenge.com/">VORC Website</a>

<a href="https://github.com/osrf/vorc">VORC Competition Details</a>

<a href="https://github.com/kvndngyn/KanaloaWork/blob/main/2020/2020KanaloaJournal.md">My Development Journal</a>

