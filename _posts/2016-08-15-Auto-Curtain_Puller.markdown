---
layout: post
title:  "Automatic Curtain Opener"
date: 2016-08-15
categories: [front, electronics]
thumbnail: curtain1.jpg
---
![post-image]({{site.url}}/assets/curtain1.jpg)

This is an automatic curtain opener that I made during summer 2016. It is powered by an DS3231 RTC chip, a micro servo motor, and Arduino.
At 8 AM, the servo spins clockwise and pulls the curtains open, letting natural light into the room. At 7 PM, the servo spins
counterclockwise and pulls the curtains closed.

![post-image]({{site.url}}/assets/curtain2.jpg)

The servo is attached to a pulley system. The pulley wheels are are pair of toy wheels with a groove. Dacron fishing wire connects the two pulleys. The curtain is clipped to the pulley string. It's very difficult to tension the string without it falling off or slipping.

The RTC chip has two alarms that trigger the interrupt pins of the Arduino. When the interrupt is triggered, the Arduino attaches the servo
and sends PWM signals for around 6 seconds. The micro servo was modified for continuous rotation. This was done by cutting off the stop tabs and super gluing the potentiometer to the 90 degree position.
The PWM signals then correspond to different directions:
<ul>
<li>0 degrees: counterclockwise</li>
<li>90 degrees: no movement</li>
<li>180 degrees: clockwise</li>
</ul>

There are counters in the code that keeps the state of the curtain so that the curtain doesn't close if it is already closed. There is a
button that triggers the servo open/close function "manually".

<iframe width="720" height="405" src="https://www.youtube.com/embed/VDPJnq4CG6A" frameborder="0" allowfullscreen></iframe>
