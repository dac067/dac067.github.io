---
layout: post
title:  "Autonomous Line Follower"
date: 2017-05-07
categories: [front, electronics]
thumbnail: linescan1.jpg
---
<heading>Hello</heading>

![post-image]({{site.url}}/assets/linescan1.jpg)

During the 2016-2017 school year, I worked on a project called Grand PrIEEE. It is a yearlong project where multiple teams create a small autonomous vehicle that would navigate through a preset track made of white tape. At the end of the year, the teams would compete against each other for the quickest completion time. This competition was hosted by UCSD's IEEE club.

In my group, I worked with 3 other people. My contributions include: selecting hardware/vehicle components, completing the H bridge motor driver circuit, assembling the system, and working on the overall line detection code.

![post-image]({{site.url}}/assets/linescan2.jpg)

Our hardware system operated as follows: <br>
A 12 volt LiPo battery was connected to the half bridge motor driver circuit. The 12 volt driver powered and controlled the speed of the motor. <br>
The 12 volt battery was also connected to a UBEC (Universal Battery Elimination Circuit), which created and regulated a 6 volt output. <br>
This 6 volt output powered the Arduino and steering servo. <br>
The Arduino's 5 volt pins were used to power the bluetooth module and linescan camera.

Our software system operated as follows: <br>
The Arduino sent a PWM signal to the motor driver circuit such that the motor ran at a constant speed. <br>
The Arduino would continuously read data from the linescan camera so determine the location of the white line track.<br>
The steering servo was shifted accordingly to our proportional controller code so that the car stays on track.<br>
The motor could be shut off remotely by issuing commands to the bluetooth module.

![post-image]({{site.url}}/assets/linescan3.jpg)

![post-image]({{site.url}}/assets/linescan4.jpg)

Grand prIEEE 2017
I'll write a detailed explanation sometime later.
..and fix embedding

<iframe width="720" height="405" src="https://www.youtube.com/embed/7dBl0f6NcCU" frameborder="0" allowfullscreen></iframe>
