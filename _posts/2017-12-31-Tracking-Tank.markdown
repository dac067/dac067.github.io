---
layout: post
title: "Object Tracking Robot"
date: 2017-12-31
categories: [front, electronics, printing]
thumbnail: pytank1.jpg
---


![post-image]({{site.url}}/assets/pytank1.jpg)

This is a RC tracked vehicle that can autonomously track and follow an object, in this case a yellow ball.

It is comprised of a Raspberry Pi, camera module, motor driver, and 3d printed parts.

![post-image]({{site.url}}/assets/pytank2.jpg)

The software utilizes OpenCV.
The Raspberry Pi extracts the yellowish pixels from the image frame and uses a circular Hough transform to verify if it is a circle.
If the yellow ball is detected, the center coordinate of the circle is mapped to a proportional controller. The proportionally controller takes the current ball coordinate and adjusts the left/right motor PWM values to face the robot towards the ball. Ideally, the ball coordinate should coincide with the center of the image frame.
This method relies on consistent exterior lighting.

![post-image]({{site.url}}/assets/pytank3.jpg)

The system is powered by two 18650 batteries in series for 7.4v. This is fed into the motor driver to run the small DC motors. The motor driver also regulates a 5v output, which powers the Raspberry Pi.

![post-image]({{site.url}}/assets/pytank4.jpg)

The robot is also capable of streaming video to a local webserver. This is facilitated with the RPi-Cam-Web_Interface software that can be found here:
https://elinux.org/RPi-Cam-Web-Interface
The robot can be driven remotely from SSH by reading user input with the python curses module. https://elinux.org/RPi-Cam-Web-Interface
This bypasses the need for X-forwarding, which has compatibility issues with different computers.

![post-image]({{site.url}}/assets/pytank5.jpg)

<iframe width="720" height="405" src="https://www.youtube.com/embed/Fyp27L07shM" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>

<br>

<iframe width="720" height="405" src="https://www.youtube.com/embed/M8-tdnEpVJU" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>
