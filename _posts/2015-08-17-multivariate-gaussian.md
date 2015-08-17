---
layout: post
title: "multivariate gaussian"
description: ""
category: "Mach"
tags: ["Machine Learning"]
---
{% include JB/setup %}

This post only shows the intuition of multivariate gaussian.
It does not contain any detailed explaination.

<!--more-->

You can use R or other language plot the multivariate gaussian:

	bivn <- mvrnorm(1000, mu = c(0, 0), Sigma = matrix(c(1, 0, 0, 1), 2))
	bivn.kde <- kde2d(bivn[,1], bivn[,2], n = 50)
	persp3D(bivn.kde$x, bivn.kde$y, bivn.kde$z, phi=20, theta=0)

![Imgur](http://i.imgur.com/tVbRPvF.png)

![Imgur](http://i.imgur.com/ce0u0PY.png)

![Imgur](http://i.imgur.com/UMR4ad5.png)

![Imgur](http://i.imgur.com/JK20Pmm.png)

![Imgur](http://i.imgur.com/OUzBqip.png)

![Imgur](http://i.imgur.com/MkjK0t2.png)

The last several pictures are coming from Andrew Ng's lecture.
