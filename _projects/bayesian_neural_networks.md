---
layout: page
title: Bayesian neural networks
description: How to use climate models to infill records of the past
img: assets/img/infilling.png
importance: 1
category: current
---

TL;DR
We can use Bayesian neural networks to to infill gaps in histroical environmental datasets. It couples our best expert knowledge, ecoded within multiple climate models, and observations within a Bayesian framework to make histroic predictions where we once couldn't.

## Background
For years satellites and instruments both on the ground and in the air have measured the Earth's oceans, atmosphere and surface. Though these instruments allow us to build up a rich history of the changing planet they rarely provide a continuous uniterupted stream of data. Satellites have a finite lifetime, some instruments might only work in certain conditions or there just isn't enough funding to support these measurement projects. This can leave us with a patch work of observations from multiple sources that might not cover our spatial region of interest, or cover enough years to do some trend analysis. 

This raises the question of how can we fill in these data gaps.

**Images of gaps in data**

Now, if we had no knoweldge of the Earth's system and the gaps were really small we could do some simple interpolation, or a nearest neighbour fit. But what if the gaps were large? Perhaps there is no data for the entire southern hemisphere for one month. Maybe we could use something more sophisticated (Gaussian processes, neural networks) to learn how to model the data using a set of covariates. That may well give us a better answer. But we can do better because we have dozens of *process models* that give us sensible predictions based on the fundamental laws of physics and chemistry that they are built upon. We can use these predictions to help us fill in gaps.

## Bayesian neural networks
Neural networks are used throughout applied machine learning as scalable ways to learn non-linear functions. A downside of many neural network applications is that they don't consider uncertainty. You get a single value prediction rather than a distribution. This is fine for many applications, but when we're infilling data for important environmental applications, we need to know what range of values the infilled sections could take. We therefore need to make the neural network Bayesian.

So we said we wanted a distribution as an output, rather than a single prediction value...

There's a number of ways to do this (and )