---
title: Exploring Simple 3D Rendering using p5.js
summary: A fun mini-project to explore the bare-bones of ray tracing and rendering.
tags:
- Personal
date: "2021-01-11"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Left

links:
url_code: "https://editor.p5js.org/AmritAmar/sketches/-Bn98qSOP"
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

{{< p5js rHQ8azreR 722 722 >}}

This was a tiny project I made as a primer to explain rendering to a younger cousin of mine! In the sketch above, I cast rays from a randomly moving point and check whether there is a line-line intersection with any of the walls. If there is (and it is the closest), we use that point as an anchor to draw the ray to. This is basic version of how shadows and lighting is done in 2D games.

{{< p5js -Bn98qSOP 704 1500 >}}

In the next sketch, I rendered the rays cast out to a simple 3D scene. Each ray create a 'slice' of the view camera (there aren't that many which is why it isn't smooth). The box size and color brightness decreases with distance (using the inverse square law). On the top of the sketch window, you can change the FOV. I thought about making boxes instead of lines but I really like how the lines look with higher FOVs and create some weird illusions.

This was a simple look into writing a really quick renderer and simple ray tracer. During college I wrote a ray-tracing engine for an graphics project so doing this bare-bones implementation was pretty interesting. 