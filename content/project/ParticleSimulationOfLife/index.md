---
title: A Particle Simulation of Life
summary: A project I made to explore the theories by biologist Lynn Margulis.
tags:
- Personal
- AI
date: "2018-11-15"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Center

links:
- icon: github
  icon_pack: fab
  name: Github
  url: https://github.com/AmritAmar/ParticleSimulationOfLifeJS
url_code: "https://editor.p5js.org/AmritAmar/sketches/-L9i8L96T"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

This is a JS implementation of a particle system. The project simulates particles in a 'box' and assigns random forces between different types of particles. Interestingly, certain behaviors arise that are 'life-like' from these rules. The particles interact with each other arising in behaviors that mimic cell behavior. 

This simulation works by having each particle type have a certain force associated with another particle type. Sometimes the force can attract, sometimes it repels. The force is stronger the closer the two particles are, but after a certain point, they do not affect each other. The randomization of these forces leads to a number of interesting behaviors. You can play with the simulation in the widget below!

You can control the number of particles (and click to add more of a certain type), the interaction radius controls the distance at which particles interact with each other (a global variable here), and a few other options. Feel free to edit the code and try out other values in the [web code editor](https://editor.p5js.org/AmritAmar/sketches/-L9i8L96T).

{{< p5js -L9i8L96T 724 804 >}}

I was inspired by this from an Evolution Class I took at Cornell where I read the theories of biologist Lynn Margulis. I was further inspired to create my own implementation from Jeffrey Ventrella's [Clusters](http://www.ventrella.com/Clusters/), which has examples in both the browser and in augmented reality. Furthermore, I also drew inspiration from [this study](http://zool33.uni-graz.at/artlife/PPS) and [HackerPoet](https://github.com/HackerPoet/) and his [Particle-Life Video](https://www.youtube.com/watch?v=Z_zmZ23grXE). The main idea, from [Lynn Margulis](https://evolution.berkeley.edu/evolibrary/article/history_24) is that all organisms naturally gravitate to other kinds of organisms, and likewise are repelled by different organisms. These particles experience attractions and repulsions with other particles of different colors. They cluster into social pods, or scatter and flee, often mimicking biological behaviors. Clusters shapeshift and exchange parts of their identities, much like the tiny organisms that came together in early evolution to form symbiotic unions.