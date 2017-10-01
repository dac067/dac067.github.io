---
layout: post
title:  "IoTea Drink Dispenser"
date: 2017-06-22
categories: [front, electronics]
thumbnail: pump2.jpg
---

![post-image]({{site.url}}/assets/pump2.jpg)

<h4>The Art of Product Engineering</h4>

In Winter and Spring quarter 2017, I enrolled in a new pilot class called "The Art of Product Engineering". It was a 2-quarter class that aimed to introduce Electrical Engineering students to the software and business side of product development. The goal of this course was to strategically develop a product with the customer experience in mind, instead of rushing a product that is ultimately unwanted and unwarranted.   

For the first quarter, we focused on learning Python in a series of 12 assignments. We also had labs in which we utilized the Raspberry Pi to read data from sensors and implement basic programs. For the first quarter final project, we learned HTML/CSS to build and deploy a simple website that queries an online/MySQL database for RPi sensor data.

![post-image]({{site.url}}/assets/pump1.jpg)

In the second term, we were introduced to business practices such as market research, customer journey map, revenue models, job stories, etc. We were to use these business practices to develop an Internet-of-Things product in a mock startup environment. My team and I came up with the "IoTea". It is essentially a bartending robot that dispenses mixed drinks via a mobile/web application. The application would have a database of drinks with the corresponding recipe to make it. To make a drink, the user would fill the IoTea pod containers with the necessary ingredients, select the drink from the application, and press the dispense button. The IoTea prototype would then turn on a Peristaltic pump that would siphon the necessary ingredient amount from the pods into the user's cup.    

![post-image]({{site.url}}/assets/pump4.jpg)

IoTea was build from a Raspberry Pi, 2 pumps, 2 motor drivers, and a 20v power supply. The Raspberry Pi would host a local web site that would operate as the app interface, displaying recipes and information. When the user initiates a dispense command, the Raspberry Pi would send PWM signals to the motor drivers, which would run the pumps. The pumps would run for a calculated amount of time, which corresponded to the amount of liquid needed.

Since we had no budget for this project, we resorted to using whatever free materials we could find. We were not able to acquire an actual liquid pump, so we 3d printed a peristaltic pump and used rubber tubing that I had leftover from previous projects. The pump
operates by squeezing the rubber tubing in a circular rotation, creating suction that would pull up liquid from the pod. Since the pumps operated on 12v, we had to step down our 20v power supply. We ran the power supply to a 15 volt regulator chip, which would then be connected to a 12 volt regulator chip. The frame was made from laser-cut acrylic. The pump supports were laser-cut from plywood.

![post-image]({{site.rul}}/assets/pump3.jpg)

For our final presentation, we did a Customer Journey map, competition analysis, personas, etc.
Here is a link to our powerpoint.
https://docs.google.com/presentation/d/154Sc6w_vb3orhJCIFGjVx0dz_aLIm3kgE25RuFR66yA/edit?usp=sharing

<iframe width="720" height="450" src="https://www.youtube.com/embed/_mpTIehHUXA" frameborder="0" allowfullscreen></iframe>
