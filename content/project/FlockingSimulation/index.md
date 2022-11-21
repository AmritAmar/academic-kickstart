---
title: Flocking Simulation using p5.js
summary: A mini-project to explore steering behaviors.
tags:
- Personal
date: "2021-07-06"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Left

links:
url_code: "https://editor.p5js.org/AmritAmar/sketches/OIqXlIiqS"
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
This was a tiny project I made a couple of years ago in an graphics/simulation class to explore steering behaviours from [Craig Reynolds' Boids](https://www.red3d.com/cwr/boids/). I made it initially in C++ but ported it to p5.js. It's a pretty cool simulation to show emergent behavior from simple rules; super mesmerizing to watch!

{{< p5js OIqXlIiqS 722 800 >}}

Use the sliders to adjust:

- Alignment (how strongly the boids align the to the average direction of other boids in the vicinity)

- Cohesion (how strongly the boids go to the average position of other boids in the vicinity)

- Separation (how strongly the boids avoid each other in the vicinity)