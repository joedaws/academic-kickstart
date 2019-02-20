+++
title = "Networks with Binary Tree Architecture"
date = 2019-01-14T11:36:57-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Joseph Daws"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["neural-networks","network-architecture","machine-learning"]
categories = ["Neural-Networks"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

## Binary Trees

Binary trees are both interesting from a purely graph theorectic point of view
as well as in application. 
Their usefulness is evident by their wide use as a [model][2]
for organization in a wide variety of applications. 
For example, they are used to describe directory 
hierachies in file systems, to store data so that it may be effeciently
queried and to describe and organize the possible game states 
such as all possible chess matches. 

In this article we will discuss a class of functions which 
is composed of compositions of simpler functions whose
interaction is described by a binary tree. Consider
the following diagram of a binary tree.

INSERT DIAGRAM

This graph corresponds to the function
$H:\mathcal{R}^d \rightarrow \mathcal{R}$ given by

$$
H(x\_1,\dots,x\_d) := h\_{\nu\_0}(h\_{\nu\_{1}}(x\_1,x\_2),
                                  h\_{\nu\_{2}}(x\_3,x\_4))
$$

some functions are compositions of other functions
have a so-called binary tree structure. 

## Polynoials as Products
An example of a polynomial with locally hierarchical compositional structure 
was considered by [Poggio et al.][1]. 
They consider the polynomial 
$$ Q(x\_1,x\_2,\dots,x\_N) $$

Polynomials can be written as the product of
complex numbers of the form $(x\_i - r\_j)$.

## Locally Hierarchical Basis Functions

Review the theory of Poggio et al for describing the 
expressibility of binvary tree neural networks.

Of course, all of this can be generalized to a $k-ary$ tree, i.e., 
a tree where each node has at most $k$ children.


[1]:https://arxiv.org/abs/1611.00740
[2]:https://en.wikipedia.org/wiki/Tree_structure
