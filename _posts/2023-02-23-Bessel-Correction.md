---
title: "Bessel's Correction - Why Sample Variance Should Be Divided By N-1"
date: 2023-01-28
mathjax: true
toc: true
categories:
  - Study
tags:
  - Statistics
---

In this post, I would display a brief and short proof of the Bessel's Correction, which is a formula of an unbiased estimator for the population variance. After this post, readers will comprehend the reason behind the denominator in the sample variance formula (which is $N-1$ rather than $N$). 

# **Introduction**
In every introductory statistics course, students learn how to compute the sample moments (usually the fisrt and second moments or the mean and variance respectively). The sample mean is familiar to derive. Let us present some notations using for this post. Suppose that $X = \\{X_1, X_2, \dots, X_{n} \\}$ be a sample of $n$ i.i.d random variabels where i.i.d stands for identically and independently distributed. The sample mean $\bar{X}$ is calculated as

$$\bar{X} = \frac{1}{n} \sum_{i = 1}^{n} X_{i}. \tag{1} $$ 

Concerning the sample variance, we are often told to divide the sum of the squared difference between the realized values of each random variables and the sample mean by $n-1$ instead of $n$.

$$ s^2 = \frac{1}{n-1} \sum_{i = 1}^{n} (X_{i} - \bar{x}). \tag{2}$$

The above rectification is sometimes called Bessel's correction (this is a jargon!). It can be easily shown by computational experiment that if repeat multiple times the simulation of the sample variance using Bessel's correction, it will be approximately idential to the population variance (of course since we are conducting experiment, it is reasonable to assume that the population variance is known). Hence, the idea of the proof revolves around the unbiased property of an estimator. 

We will give a formal definition of unbiased estimator:

**Definition (Unbiased estimator)** Given an estimator $\hat{\theta}$ of a parameter $\theta$, the quantity $\operatorname{Bias} [\hat{\theta}] = \mathbb{E}[\hat{\theta}] - \theta$ is the *bias* of the estimator $\hat{\theta}$. If the bias is zero, i.e., $\mathbb{E}[\hat{\theta}] = 0$ the estimator $\hat{\theta}$ is unbiased. 

To put it simply and specific to our case, let $s^2$ and $\sigma^2$ be the sample variance and population variance respectively. An unbiased estimator of the population variance must statisfy the following condition:

$$ \mathbb{E} [s^2] - \sigma^2 = 0 \Leftrightarrow \mathbb{E} [s^2] = \sigma^2. \tag{3} $$
