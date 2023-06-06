---
title: "Likelihood Principle and A Paradoxical Example"
date: 2023-06-06
mathjax: true
toc: true
categories:
  - Study
tags:
  -  Statistics
---
In this post, I will demonstrate one of two fundamental principles that 
are applied to the procedures of Bayesian paradigm, the *Likelihood Principle*.
Naturally, Bayesian framework incorporates these principles without further 
stringent constraints. Likelihood principle arises as an intuitive of the way
we should conduct an experiment and absorb all uncertanties into the statistical 
model of the observations. 

# Likelihood Principle
The key element of the definition of Likelihood principle revolves around the notion
of *information*, which in a broad sense is considered to be the collection of all 
possible inferences on the unknown parameter $\theta$. I state the following formal 
definition (The Bayesian Choice, Chritian P. Robert, p.15):

**Likelihood principle** *The information brought by an observation $x$ about $\theta$
is entirely contained in the likelihood function $l(\theta \lvert x)$. Moreover,
if $x_1$ and $x_2$ are two observations depending on the same prarameter $\theta$, such 
that there exists a constant $c$ statisfying*

$$l_1(\theta \lvert $x_1) = cl_2(\theta \lvert x_2)$$
*for every $\theta$, then they bring the same information about $\theta$ and must lead to 
identical inferences.*
