---
layout: post
title: "Boltzmann machine"
description: ""
category: "Mach"
tags: ["Machine Learning"]
---
{% include JB/setup %}

**The key idea of restricted Boltzmann machine:**

> A restricted Boltzmann machine which
consists of a layer of stochastic binary "visible"
units that represent binary input data connected
to a layer of chochastic binary hidden units that learn 
to model significant nonindependencies between the visible units.

There are undirected connections between visible and hidden units but no visible-visible or hidden-hidden
connections.

An RBM is type of Markov random field (MRF) but differs
from most of MRFs in several ways: it has a bipartite
connectivity graph, it does not usually share weights
between different units, and a subset of the variables
are unobserved, even during training.

