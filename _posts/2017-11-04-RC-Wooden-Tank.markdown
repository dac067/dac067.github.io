---
layout: post
title:  "Wooden RC Tank"
date: 2017-04-11
categories: [front, woodworking, electronics]
thumbnail: tank1.jpg
---
![post-image]({{site.url}}/assets/tank1.jpg)

I built this remote controlled tank in the summer of 2016.

![post-image]({{site.url}}/assets/tank3.jpg)

The electrical components include
<ul>
<li>two DC brushed motors</li>
<li>2x Quicrun 1060 electronic speed controllers</li>
<li>7.2V NiCad Battery</li>
<li>FlySky transmitter and receiver</li>
</ul>

I salvaged the DC motors from 7.2V Craftsman power drills. Using drill motors for this project
was ideal because they already had gearboxes attached. This provided enough torque to propel
the tank, which weighs over 12 pounds.

The transmitter I have is suited for model airplanes and has 6 channels. I connected each motor to
a channel and tweaked the throttle curves so that both chains moved consistently in sync.
The left and right motor channels was mapped to one stick and controls as following:
<ul>
<li>Forward - Move stick top-left</li>
<li>Reverse - Move stick bottom-right</li>
<li>Spin - Move stick top-right or bottom-left</li>
</ul>
The right motor was controlled by moving the stick up/down. The left motor was controlled
by left/right stick movement. Turning was achieved by running one motor faster than the other.

![post-image]({{site.url}}/assets/tank2.jpg)

I am currently working on removing the transmitter/receiver altogether and replacing it with
Arduino control. I connected the Arduino directly to the ESC and determined the signal sequence
that arms the ESC. By sending PWM signals directly to the ESC, I can control the speed of the
motor with code and programming. The tank would then be a platform for potential robotic
projects that I aim to do in the summer.

I plan to incorporate a Raspberry Pi into the system and implement computer vision. By using the Pi's camera module and the OpenCV repository, I can have the tank run autonomously. My stretch goal at the moment is to have the tank follow me around by scanning for QR code that would be attached to my shoe.

<iframe width="720" height="405" src="https://www.youtube.com/embed/ZYvNLW1jg90" frameborder="0" allowfullscreen></iframe>
