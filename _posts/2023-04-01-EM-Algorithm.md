---
title: "Expectation-Maximization"
date: 2023-04-01
mathjax: true
toc: true
categories:
  - Study
tags:
  - Bayesian
  - Machine Learning
  - Statistics
---

Currently, I am interested in doing some researchs on Poisson mixture model and its application on
modeling count data and it's a good time to revise the Expectation-Maximization (EM) algorithm. This optimization technique is extremely useful when we have to 
deal with latent variable models (for example, number of mixture components in the mixture model). The underlying idea is that we will maximize the complete log 
likelihood instead of the usual log likelihood. Furthermore, EM algorithm alleviate the computational difficulty related to this complete-data log likelihood by 
iteratively construct and optimize a tight lower bound. Before delving into details, it's worth noting that EM algorithm has a close connection with variational 
inference and it lays a foundation on Variational Inference (VI); thereby, I also write a brief [introduction](https://callmequant.github.io/study/variational-inference/) on Variational Inference for anyone interested.

# Introduction
*Expectation Maximization* algorithm, or EM for short, is a common approach to tackle the *maximum likelihood estimations* (MLE) for any probabilistic models
containing latent variables. Consider a probabilistic model settings in which the observed variables are denoted by $X$ with observed values $\lbrace x_1, \dots, x_N \rbrace$ 
and all latent variables by $Z$. The parameters of the model are succintly denoted by $\theta$. To perform maximum likelihood inference, we need to derive the (log) likelihood $\operatorname{log} p(X \mid \theta)$. However, since 
