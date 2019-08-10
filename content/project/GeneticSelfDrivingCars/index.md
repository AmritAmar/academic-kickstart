---
title: Genetic Self-Driving Cars
summary: A project I made to explore neuroevolution.
tags:
- Personal
- AI
date: "2018-12-15"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Center

links:
- icon: github
  icon_pack: fab
  name: Github
  url: https://github.com/AmritAmar/GeneticSelfDrivingCars
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

This is a project I did to learn about Neural Networks and Genetic Algorithms. We create a neural network to drive a car and then use genetic algorithms to train and find the best weights for the neural network. The network takes in 6 inputs and outputs the acceleration and steering of the car.

Here, we see all the cars beginning to get initialized with a random neural network. They are pretty dumb.

![FG](https://raw.githubusercontent.com/AmritAmar/GeneticSelfDrivingCars/master/Gifs/FirstGen.gif)

In the editor, this is the information that cars get (as shown by the yellow lines).

![NN](https://raw.githubusercontent.com/AmritAmar/GeneticSelfDrivingCars/master/Gifs/NNView.gif)

By generation 22, we have a car that can finish the whole track (albeit not smoothly)!

![BC](https://raw.githubusercontent.com/AmritAmar/GeneticSelfDrivingCars/master/Gifs/BestCar.gif)

On average, it takes about 22 generations to train the neural network fully.

The neural network has 6 input nodes:

- current speed
- distance of closest obstacle from the left side (max 10m)
- distance of closest obstacle from the right side (max 10m)
- distance of closest obstacle from the front (max 10m)
- distance of closest obstacle from the front-left side (max 10m)
- distance of closest obstacle from the front-right side (max 10m)

There is 1 hidden layer, consisting of 5 nodes. There is 1 output layer, consisting of 2 nodes:

- Acceleration (-1 to 1)
- Steering (-1 to 1)

I use tanH as my activation function.

There are 3 main scripts:

- CarController: this is the script for a car. Has a neural network that drives the car.
- CarManager: manager for the population of cars
- NeuralNetwork: holds the neural network code
- GeneticAlgorithmController: performs the selection process of the algorithm
The program works as follows:

The input and hidden layer nodes have both a weight and a bias, that is randomly generated for the population of cars (default 10). They are then simulated as generation 1 on the race track. After all the cars crash or 60 seconds, the algorithm chooses the best 2 cars (based on displacement from starting point) and then creates the next generation of cars by combining the best 2 cars genes (randomly selecting between the 2 or a combination thereof). There is an option that allows us to keep the best 2 cars in the next generation or to generate all new cars in the population from the parents (i.e. the parents die). The next generation is then simulated and so on.