+++
title = "Designing Neural Networks"
date = 2018-11-07T15:23:38-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Joseph Daws"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["machine-learning","neural-networks"]
categories = ["Neural-Networks"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = "A single layer artificial neural network"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"
+++

# How to design a neural network for function approximaiton
> An artificial neural network (ANN) is a computational framework 
inspired by the interactions of neurons in the brain. 

In order to make sense of ANN's mathematically it is useful to 
characterize them both as functions and as graphs. 
The network can be interpreted as a mapping from $\mathbb{R}^d$ to 
$\mathbb{R}^k$ where $d$ is the number of inputs to the network and 
$k$ is the number of ouputs. The interactions between the constituent
functions that make up the network can be described by an
[directed acylic graph](https://en.wikipedia.org/wiki/Directed_acyclic_graph).
The associated graph can be used to analyze the complexity of the
network defined as the number of trainable parameters.
Simply put, a neural network can be characterized as a function consisting of
compositions and linear combinations of constituent functions called
__neurons__ which perform a computation of the form
$$ \sigma \left( \sum\_{i=1}^k w\_i \cdot x\_i  + b \right).$$

+ $x\_i$ -- The __inputs__ for the computation. 
  They could be the result of computations performed by other neurons or
  raw input.
+ $w\_i$ -- The __weight__ associated to the incoming data $x\_i$.
+ $\sigma$ -- A nonlinear function called the __activation function__.
+ $b$ -- A number called the __bias__ of the neuron.

## Nonlinear functions and graphs
Below is a simple example showing the dual characterization 
of a single hidden layer ANN. 

![single layer network](featured.png)
*A single hidden layer network with three neurons.*

## The architecture of a network depends on its application

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

