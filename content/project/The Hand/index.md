---
title: The Hand
summary: An IT Innovation project I made for the Botho College ICT Challenge, a national competition.
tags:
- Arduino
- Personal
date: "2014-09-21"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Center

links:
- icon: github
  icon_pack: fab
  name: Github
  url: https://github.com/AmritAmar/TheHand
url_code: ""
url_pdf: "https://github.com/AmritAmar/TheHand/raw/master/The%20Hand%20-%20Project%20Documentation%20by%20Amrit%20Amar%20and%20Tawanda%20Mulalu.pdf"
url_slides: ""
url_video: "https://www.youtube.com/watch?v=vL56RGWwA9o&list=PL3Lzx8hTbaGUeELkre6fPQB8pKLX65-ph"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

This is a hand that can be used to do a lot of things. The basic motive of the project is that the user will wear the control glove, and will be able to control the robotic hand using their movements. A close friend and I made a robotic animatronic hand that could potentially help save lives in the event of an accident in Mines, one of Botswana's main industries.

There are many uses for this such as Space Exploration and in the Mining Industry. Instead of using AI, that can't react to all situations in an environment, we can use robots, that are controlled by the user. Humans can react to sudden environmental changes and, using "The Hand", they can improvise and adapt.

For making the Project, we used an Arduino Leonardo, Flex Sensors and Servo Motors. The Arduino is a microprocessor that basically reads from code uploaded to it from a computer (C/C++ Code) and therefore through the use of Digital and Analog I/O pins, executes the code. Flex Sensors are Variable Resistors that change values depending on how much they are bent by. Servo Motors are precision DC motors that can be controlled to point to the exact angle from 0 to 180 Degrees.

What basically happens here is that the Flex Sensor readings are inputs through the Analog Pins. It is processed and mapped to a angle. The angle is then written to the Servo Motors, thus turning them and therefore moving the fingers. There are also two buttons that control a LED and a Speaker. On the breadboard, there is an LDR (Light dependent resistor) that basically measure the amount of light in a room. Using those values, it gives a green light or a yellow light. The Arduino can be used to do a lot of things!

In the future, we hope to develop a better working hand with all fingers working and an opposable thumb. This would allow us to hold things. The next stage of this project is to finish the hand and make sure it can pick up things.

We won first place at a National Competition (The Botho College ICT Linkz Challenge 2014) with this project. Thank you to everyone who helped out!

[A Video Demonstration can be found here](https://www.youtube.com/watch?v=TA5GpAQBzUY)
