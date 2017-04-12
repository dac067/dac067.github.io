---
layout: post
title:  "Motion Detecting Speaker"
date: 2016-05-20
categories: [front, electronics]
thumbnail: seinfeld1.jpg
---

![post-image]({{site.url}}/assets/seinfeld1.jpg)

This is a motion activated speaker system. It plays a sound file from a SD card when the
PIR (passive infared) sensor detects motion.

![post-image]({{site.url}}/assets/seinfeld2.jpg)

It uses an Arduino, PIR sensor, SD card reader, and an amplifier circuit. When the PIR sensor
detects motion, it sends a high signal that is then read by the Arduino. The Arduino then
randomly selects a WAV sound file from the SD card and sends it to the op-amp circuit.
The sound is played through a pair of 8 ohm speakers. I've placed capacitors on across the power rails to filter out unwanted noise and static. There is a potentiometer for volume control.

<iframe width="720" height="405" src="https://www.youtube.com/embed/1ws9EWa5-Jk" frameborder="0" allowfullscreen></iframe>
