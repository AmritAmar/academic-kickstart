---
title: Marching Squares with p5.js
summary: A look at the marching squares algorithm.
tags:
- Personal
date: "2021-08-16"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Left

links:
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

The [marching squares algorithm](https://en.wikipedia.org/wiki/Marching_squares) is a computer graphics algorithm for creating contours/boundaries based on underlying grid values. It's a really fascinating algorithm with tons of uses in procedural generation. It's also really simple to implement! This implementation uses [OpenSimplex Noise](https://en.wikipedia.org/wiki/OpenSimplex_noise).

Note: the page can be slow when loading these simulations so it's better to look at them individually (and checkout the various settings you can tinker with): (1) [non-interpolated](https://editor.p5js.org/AmritAmar/sketches/N1bVTxCUP), (2) [interpolated](https://editor.p5js.org/AmritAmar/sketches/haLE8EfC7), (3) [metaballs](https://editor.p5js.org/AmritAmar/sketches/JfDKSnAHy).

{{< p5js N1bVTxCUP 722 750 >}}

I first started with a non-interpolated version of the algorithm to see all the possible boundaries in action. If you go into the [editor](https://editor.p5js.org/AmritAmar/sketches/N1bVTxCUP), you can enable and disable various settings to see the distribution below or the squares. You can also take a snapshot of it and use it in 2D world generation (such as generating cave structures). 

{{< p5js haLE8EfC7 722 750 >}}

The [interpolated version](https://editor.p5js.org/AmritAmar/sketches/haLE8EfC7) makes everything look much smoother and natural. Using the interpolated version and adding shapes instead of noise, we can use the marching squares algorithm to generate [Metaballs](https://en.wikipedia.org/wiki/Metaballs)!

{{< p5js JfDKSnAHy 722 750 >}}