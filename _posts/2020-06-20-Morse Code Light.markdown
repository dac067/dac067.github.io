---
layout: post
title: "Morse Code Light"
date: 2020-06-20
categories: [front, electronics, art]
thumbnail: morseLight.jpg
---

![post-image]({{site.url}}/assets/morseLight.jpg)

This is a solar powered light that is programmed to pulse a morse code message. It is inspired by the blinking lamp in the movie Parasite.

The lantern is programmed to pulse multiple messages, such as
"HOME"
"NO FUTURE"
"ASHES TO" (ashes to ashes to ashes...)
and more.

The phrase is selected randomly upon nightfall and repeats until morning or until the battery is depleted.

This is made from an Arduino Nano, boost converter, and a solar garden light from Home Depot.

I connected the garden lamp to a boost converter, which boost the voltage to 5V. This 5V powers an Arduino Nano, which drives a BJT switch circuit and ultimately the LED light.

![post-image]({{site.url}}/assets/morseLight2.jpg)

<iframe width="560" height="315" src="https://www.youtube.com/embed/v0rmaSmdrUs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
