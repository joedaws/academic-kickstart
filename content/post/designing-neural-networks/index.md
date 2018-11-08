+++
title = "Designing Neural Networks"
date = 2018-11-07T15:23:38-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Joseph Daws"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["machine-learning","neural-networks"]
categories = []

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

# The architecture of a network depends on its application

In practice, the design of neural networks is linked to their 
desired application. For instance, neural networks used for image
classification typically involve 
[convolutional kernels](https://en.wikipedia.org/wiki/Convolutional_neural_network)
which extract local features. To my knowledge there is no clear
theoretical justification of this choice of architecture. However,
since there are successful image processing methods which
exploit local and global image information simulaneously in a similar
way to convolutional layers in a neural network, .e.g.,
[LDMM](ftp://ftp.math.ucla.edu/pub/camreport/cam16-04.pdf) and
[NONLOCAL MEANS](https://ieeexplore.ieee.org/document/1467423).

When designing a network to approximate a function it is therefore 
reasonable for the architecture of a proposed network to 
depend on a particular function approximation scheme. 
This choice also allows one to take advantage of the large body 
of theoretical work describing methods to 
approximate functions (of various levels of smoothness and dimension).
I'm currently analyzing a network based on polynomial approximation of
high-dimensional functions. 

Check this post in the near future for 
some prelimary numerical results of this network.

