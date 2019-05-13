+++
title = "Polynomials, Binary Trees and Gradient Descent"
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

# Nonlinear Approximation
As described in my previous [post](https://joedaws.github.io/post/designing-neural-networks/ "Neural Network Design")
Neural networks have emerged as a very powerful tool for constructing
nonlinear functions in high-dimensions. They are known to be very expressive
in the sense that the class of functions they can approximate is very wide. 
However, in order to cosntruct an approximation of a given function 
a very large number of network parameters must be determined.
This is espcially true for Deep Neural Networks (DNNs).
Because DNNs have many parameters and because the functions 
assocaited with solving tasks like image classification 
many be quite complicated, training can be very difficult.
Although many aspects of neural network are new (such as fast training algorithms
implementable on a GPU) their expressive power and ability to appoximate
has been considered for a long time, but I personally haven't seen 
many works which make explicit connections between the powerful 
results of classical approximation theory to expressibility results for
neural networks. Below is an outline of one way in which polynomial approximation
may be able to help networks approximate difficult function. By constructing
a network which can approximate a polynomial we can take advantage of
existing polynomial approximate results. On the other hand since
networks are so expressive, given a polynoial approximation,
we can generate a network which is first initialized to take on the behavior of
the polynomial, then trained to find an even better approximation.

## Polynomial Approximation
Polynomials are natural objects of interest in many different areas of mathematics. 
A generic degree $n$ polynomial $P\_n$ is often written 
$$ P\_n(x) = a\_0 + a\_1 x + a\_2 x^2 + \cdots + a\_n x^n. $$
Written in this way the polynomial $P\_n$ is completely characterized
by its coefficients $a\_i$ for $i=0,...,n$. 
Therefore, finding a suitable polynomial approximation is equivalent to 
identifying the correct coefficients. 

According to the fundamental theorem of algebra 
Suppose that you know a root of the polynomial $P$ is $r$. Then 
it is possible to write
$P(x) = (x-r)Q(x)$ in light of our observation about numbers and
since $x-r = 0$ when $x=r$ for some other polynomials $Q$. 
Iterating this process we can write polynonials as 
a product of $n$ numbers of the form $(x-r\_i)$ for $i=1,\dots,n$. 
This fact is known as the __Fundamental Theorem of Algebra__.
It is known that every degree $n$ polynomial can be written
$$ P\_n(x) = \Pi\_{i=1}^n (x - r\_i) $$
for $n$ complex numbers $r\_i$.
We now how two representations of $P\_n(x)$i. One written 
entirely as a linear combination of the powers of $x$ and the other
as products of affine functions $(x-r\_i)$. 
Each representation is equally valid and has its own usefulness.
There may also be other interesting representations of polynomials
which involve not only products and linear combinations but also
compositions of polynomials. 

[1]:https://arxiv.org/abs/1611.00740
[2]:https://en.wikipedia.org/wiki/Tree_structure
