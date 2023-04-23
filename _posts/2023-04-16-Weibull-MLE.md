---
title: "Maximum Likelihood Estimator for Two Parameters Weibull Distribution"
date: 2023-04-16
mathjax: true
toc: true
categories:
  - Study
tags:
  - Statistics
  - Parametric Estimation
---
I came across this problem by chance when practicing for my Master's entrance exam. In this post, I will derive the *maximum likelihood estimators* (MLE) for the Weibull distribution with two parameters. For maximum likelihood estimation, I will have a different to discuss some basic concepts of this parametric estimation technique that is used extensively in many subfields of statistics. 

# **Introduction**
Before deriving the MLE for Weibull distribution, it is unusual not to introduce some characterisitics of this distribution. Weibull distribution is a *continuous* probability distribution characterized by two parameters, $\alpha$ and $\beta$ respectively. These parameters are also called the shape and the scale parameters that is skewed (left- or right- skewed data can be captured via the **shape** parameter.


# MLE for Weibull distribution
Suppose that we observe a random sample $\lbrace x_1, x_2, \dots, x_{n} \rbrace$ from $X$ following a Weibull distribution with probability density function 

$$p(x \lvert \alpha, \beta) = \left(\frac{\alpha}{\beta^\alpha}\right) x^{\alpha - 1} \exp{-\left(\frac{x}{\beta}\right)^2}, \quad x > 0 \tag{1}$$

We can reparameterize the above formula in terms of $ \alpha - 1 $:

$$p(x \lvert \alpha, \beta) = \left(\frac{\alpha}{\beta}\right) \left(\frac{x}{\beta}\right)^{\alpha - 1} \exp{-\left(\frac{x}{\beta}\right)^2}, \quad x > 0 \tag{2}$$

The likelihood function is written (assumed that the realizations of random variable $X$ is i.i.d):

$$
\begin{align*}
\mathcal{L}(x_1, x_2, \dots, x_n \lvert \alpha, \beta) & = \prod_{i=1}^{n} \left(\frac{\alpha}{\beta}\right) \left(\frac{x}{\beta}\right)^{\alpha - 1} \exp{-\left(\frac{x}{\beta}\right)^2} \\
& = \left(\frac{\alpha}{\beta}\right)^{n} \left(\frac{1}{\beta}\right)^{n(\alpha - 1)} \left(\prod_{i=1}^{n} x_i\right)^{\alpha - 1} \operatorname{exp} \Bigg\lbrace -\sum_{i=1}^{n} \left(\frac{x_i}{\beta}\right)^{\alpha} \Bigg\rbrace \\
& = \alpha^{n} \beta^{-n\alpha} \operatorname{exp} \Bigg\lbrace (\alpha - 1) \sum_{i=1}^{n} \operatorname{ln}(x_i) - \sum_{i=1}^{n} \left(\frac{x_i}{\beta}\right)^{\alpha} \Bigg\rbrace. \tag{3}
\end{align*}
$$

The log-likelihood function is derived by taking the log of Eq.(3), denoted as $\mathcal{l}(x_1, \dots, x_n \lvert \alpha, \beta)$:

$$\mathcal{l}(x_1, \dots, x_n \lvert \alpha, \beta) \coloneqq \operatorname{ln}(x_1, \dots, x_n \lvert \alpha, \beta) = n\operatorname{ln}(\alpha) - n\alpha \operatorname{ln}(\beta) + (\alpha - 1) \sum_{i=1}^{n} \operatorname{ln}(x_i) - \sum_{i=1}^{n} \left(\frac{x_i}{\beta}\right)^{\alpha}. \tag{4}$$

The MLE for $\alpha$ and $\beta$ can be obtained via the following conditions:

$$ \frac{\partial \mathcal{l}(X \lvert \alpha, \beta)}{\partial \alpha)} = 0 \quad \frac{\partial \mathcal{l}(X \lvert \alpha, \beta)}{\partial \beta)} = 0.$$

First, we will derive the MLE for the scale parameter $\beta$:

$$\frac{\partial \mathcal{l}(X \lvert \alpha, \beta)}{\partial \beta} = -\frac{n \alpha}{\beta} + \sum_{i=1}^{n} \left(\frac{x_i}{\beta}\right)^\alpha \left(\frac{\alpha}{\beta}\right) = -\frac{n \alpha}{\beta} + \left(\frac{\alpha}{\beta^{\alpha + 1}}\right) \sum_{i=1}^{n} x_{i}^{\alpha} \overset{\star}{=} 0. \tag{5}$$

Multiplying both sides at the $\star$ part of Eq.(5) by $\beta^{\alpha + 1}$ and discard the common term $\alpha$ raises:

$$-n\beta^{\alpha} + \sum_{i=1}^{n} x_{i}^{\alpha} = 0 \Rightarrow \beta_{\text{MLE}} = \Biggl(\frac{\displaystyle \sum_{i=1}^{n} x_{i}^{\alpha}}{n}\Biggr)^{\frac{1}{\alpha}} \quad (\ast \ast).$$

To be continued!







