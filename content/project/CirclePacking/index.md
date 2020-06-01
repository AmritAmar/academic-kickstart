---
title: Exploring Circle Packing using p5.js
summary: A fun mini-project because I like circles.
tags:
- Personal
date: "2020-04-20"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Left

links:
url_code: "https://editor.p5js.org/AmritAmar/sketches/oL0gKBOyS"
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

{{< p5js UVXX94iTP 704 704 >}}

This was a tiny project I made cause circles are cool! Wikipedia has a great explanation on how to [pack circles](https://en.wikipedia.org/wiki/Circle_packing). The source for circle packing is [here](https://editor.p5js.org/AmritAmar/sketches/UVXX94iTP) and for the image version, [here](https://editor.p5js.org/AmritAmar/sketches/oL0gKBOyS)! Feel free to try out different parameters and images in the browser (just change imgSource to point to another picture). Warning - can lag on really big images with different parameters!

{{< p5js oL0gKBOyS 704 750 >}}

The 3 sliders are for *counts per update* or how many circles are added every frame (1 - 100), *total circles* or max amount of circles on the screen (0 (= infinity) - 5000), and *total attempts* or the number of times we try to add a circle before we cut off the algorithm (100 - 2000), respectively. By default, the values are 10, 2500, 1000, but you can vary them!
