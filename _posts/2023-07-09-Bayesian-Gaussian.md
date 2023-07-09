---
title: "Inference Gaussian Models: A Bayesian Approach"
date: 2023-06-14
mathjax: true
toc: true
categories:
  - Study
tags:
  -  Bayesian Inference
  -  Statistics
---

In this post, I will provide the Bayesian inference for one of the most 
fundamental and widely used models, the Normal models. The Gaussian distribution is 
pivotal to a majority of statistical modeling and estimating its parameters
is a common task in Bayesian framework. I will derive results for three important 
cases: estimating the mean $\mu$ with known variance $\sigma^2$, estimating 
the variance $\sigma^2$ given a known $\mu$, and estimating both $\mu$ and $\sigma^2$.
The first two cases are single-parameter problem, while the last one is multiparameter one.
Furthermore, I will derive the likelihood, the *conjugate* prior, and the posterior of 
three cases.

# Inference normal distribution with known variance


$$
\begin{align}
p(D \mid \mu, \sigma^2)
&= \prod_{n=1}^{N} p(x_n \mid \mu, \sigma^2) \\
&\triangleq \prod_{n=1}^{N} \Bigg( \frac{1}{(2 \pi \sigma^2)^{1/2}} \exp \Big\lbrace -\frac{1}{2 \sigma^2} (x_n - \mu)^2 \Big\rbrace \Bigg) \\
&= \frac{1}{(2 \pi \sigma^2)^{N/2}} \exp \Big\lbrace -\frac{1}{2 \sigma^2} \sum_{n=1}^{N} (x_n - \mu)^2 \Big\rbrace
\end{align}
$$
