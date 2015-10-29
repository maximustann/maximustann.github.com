---
layout: post
title: "Principle Component Analysis"
description: ""
category: "Mach"
tags: ["Machine Learning"]
---
{% include JB/setup %}

The idea of a **principle component** is that it is a direction in the data with the largest variation. The
algorithm first centres the data by substracting off the mean, and then chooses the direction with the 
largest variation and places an axis in that direction, and then looks at the variation that remains and finds
another axis that is orthogonal to the first and covers as much of the remaining variation as possible. It then
iterates this until it has run out of possible axes. The end result is that all the variation is along the axes
of the coordinate set, and so the covariance matrix is diagonal - each new variable is uncorrelated with every
variable except itself. Some of the axes that are found last have very little variation, and so they can be removed
without affecting the variability in the data.

<!--more-->

Relation with the Multi-layer Perceptron

We mentioned autoencoder in the MLP section. The auto-associative MLP (autoencoder) actually computes something 
very similar to the PCA of the data in the hidden nodes, and this is one of the ways that we can understand what 
the network is doing.

If you use a more complicate MLP network with four layers of neurons instead of two. We use it as an autoencoder,
what will the middle hidden layer look like then?

1. First layer is computing some non-linear transformation of the data,
2. Second layer (bottleneck) is computing the PCA of those non-linear functions,
3. Third layer reconstructs the data,
4. Fourth layer display them.

So the network is still doing PCA, just on a non-linear version of the inputs. This might be useful, since 
now we are not assuming that the data are linearly separable.
