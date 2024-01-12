---
title: An Algorithm For Success
published: true
layout: post
permalink: succes-algorithm
excerpt:  Regardless of what path you picked, always start with whatever step is most likely to fail next
image: /images/default.png
categories: entrepreneurship, inner-game
---

* Starting point: a well-defined goal. 
* Develop a [theory of change](http://www.aaronsw.com/weblog/theoryofchange). Work backwards from the goal, in concrete steps, to figure out what you can do to achieve it. There are always multiple paths.
* Use [simulated annealing](https://maximilian-weichart.de/posts/simulated-annealing/) as meta strategy. Pick one of the possible paths at random. Identify the step that is [most likely to fail](https://cs.stanford.edu/~jsteinhardt/ResearchasaStochasticDecisionProcess.html). Start here. 
* After each step, reevalute. Your options are either the next step on the current path or jumping to a different path you picked at random.
* Assign a likelihood to succeed to both paths given your current knowledge. Compare them but allow for jumps that seem worse with a certain probability. This makes sure you don't get stuck in local maxima prematurely.
* Regardless of what path you picked, always start with whatever step is most likely to fail next.
* Initially do big jumps at random (almost completely disregarding which path seems better).
* Then gradually reduce the "temperature". Only allow jumps to paths that are adjacent to your current path and reduce the probability to jumping to options that seem worse.