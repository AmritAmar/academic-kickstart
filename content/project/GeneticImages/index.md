---
title: Genetic Images
summary: A project I made for CS 4701 (Practicium in Artificial Intelligence).
tags:
- Cornell
- AI
date: "2018-05-10"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Left

links:
- icon: github
  icon_pack: fab
  name: Github
  url: https://github.com/AmritAmar/GeneticImages
url_code: ""
url_pdf: "https://drive.google.com/file/d/18TFZThbFswRllVY08Np8gfi7XHtzdqvD/view"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

This is a project I made for my Artificial Intelligence Class under the Team "Real Intelligence". It is a image generation program that uses primitive shapes to generate images using genetic algorithms.

Our intention was to complete a project exploring the concept of genetic algorithms within artificial intelligence. Genetic Algorithms use the concept of natural selection to find a minima to a function. In this case, the genetic algorithm tries to replicate a picture using only primitive shapes and tries to bring the generated picture as close to the real picture as possible. 

To generate the image, we can adjust the number of shapes, the mutation rate, and the types/combinations of shapes to use in the generated image:
- Circles (mutate the position, radius, color)
- Ellipses (mutate the position, width, height, color)
- Rectangles (mutate the position, width, height, color)
- Pixels (n-pixels long squares, mutate the pixel position, color)
- n-sided polygons

Our implementation focuses on using a single-parent. This means that during each generation, only one picture is used to create all the children. A parent is replaced when one of the children has a better fitness score (or worse, rather). Our fitness function work by comparing the child to the original image pixel by pixel. 

The pseudocode for our genetic algorithm is as follows:

1. Generate a random image based on user-defined configurations, mainly number of shapes and types of shapes to use. Every ‘individual’ image has a ‘DNA’ that is a collection of shapes. These shapes are randomly generated and are assigned random colors. This individual image’s fitness score is also calculated here.
2. We then generate a new image with a certain mutation rate. This new image will have random differences from the parent image (differences ranging from changing the shapes’ position or dimensions to changing the shapes’ color).
3. The new image is then compared with the original image. We then compare the new image’s fitness score with the parent’s fitness score. If the image’s fitness score is lower than that of the parent image (i.e, there is less error in this image, thus the new image is closer to the original picture than the parent image), then we update the parent image to be the new image. If the fitness score is higher than the parent’s score, then we simply keep the same parent for the next generation.
4. Go to part 2 and repeat until fitness score of the parent is 0.

### Example 1: Eiffel Tower:
#### Target Picture:
![EFOG](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/eiffel2.png)
#### Starting the Algorithm:
![EF1](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/EiffelStart.gif)
#### After a bit of time:
![EF2](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/EiffelMedium.gif)
#### After a long time:
![EF3](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/EiffelEnd.gif)

Notice how the sky gradient is captured by the generated picture, simply by the adjustment of the alpha of overlapping shapes!

Over time, the error in the generated images decreases. Of course, this happens over thousands of generations. As we used our program with a multitude of images, we noticed that some shapes converge to target images better than other shapes. For the full evaluation, check out our [report](https://drive.google.com/file/d/18TFZThbFswRllVY08Np8gfi7XHtzdqvD/view).

### Example 2: Mona Lisa:
#### Target Picture:
![EFOG](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/mona_lisa.jpg)
#### Starting the Algorithm:
![EF1](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/MonaBegin.gif)
#### After a bit of time:
![EF2](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/MonaMedium.gif)
#### After a long time:
![EF3](https://raw.githubusercontent.com/AmritAmar/GeneticImages/master/Gifs/MonaEnd.gif)

Surprisingly, the algorithm seems to capture the background really well! Of course, facial features will take quite a while to develop as there is not much of a pixel difference from this image and one with facial features.
