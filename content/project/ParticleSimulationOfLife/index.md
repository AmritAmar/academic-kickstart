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
  url: https://github.com/AmritAmar/ParticleSimulationOfLife
url_code: ""
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

This is a C++ implementation of a particle system. The project simulates particles in a 'box' and assigns random forces between different types of particles. Interestingly, certain behaviors arise that are 'life-like' from these rules. The particles interact with each other arising in behaviors that mimic cell behavior.

The way this simulation works is that each particle type has a certain force associated with another particle type. Sometimes force can attract, sometimes it repels. The force is stronger the closer the two particles are, but after a certain point, they do not affect each other. The randomization of these forces leads to a number of interesting behaviors. I highly encourage people to create their own PSimulations!

In the example below, I simulate a 'glider' world, where particles form gliders and fly around the boxed world. It's mesmerising to see how a few simple rules between particles causes this.

![Glider Boxed](https://github.com/AmritAmar/ParticleSimulationOfLife/raw/master/Glider%20Boxed.gif)

I was inspired by this from an Evolution Class I took at Cornell where I read the theories of biologist Lynn Margulis. I was further inspired to create my own implementation from Jeffrey Ventrella's [Clusters](http://www.ventrella.com/Clusters/), which has examples in both the browser and in augmented reality. Furthermore, I also drew inspiration from [this study](http://zool33.uni-graz.at/artlife/PPS). The main idea, from [Lynn Margulis](https://evolution.berkeley.edu/evolibrary/article/history_24) is that all organisms naturally gravitate to other kinds of organisms, and likewise are repelled by different organisms. These particles experience attractions and repulsions with other particles of different colors. They cluster into social pods, or scatter and flee, often mimicking biological behaviors. Clusters shapeshift and exchange parts of their identities, much like the tiny organisms that came together in early evolution to form symbiotic unions.

In this example, I simulate a unboxed world that creates medium clusters. This leads to a roaming behaviour by these clusters all around the map!

![Medium Clusters Unboxed](https://github.com/AmritAmar/ParticleSimulationOfLife/raw/master/Clusters%20Unboxed.gif)
