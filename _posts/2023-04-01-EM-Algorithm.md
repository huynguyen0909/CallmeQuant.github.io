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
and all latent variables by $Z$. The parameters of the model are succintly denoted by $\theta$. To perform maximum likelihood inference, we need to derive the (log) likelihood $\operatorname{log} p(X \mid \theta)$. However, since our data generating process comprises some latent variables $Z$, we have to include them in our log likelihood function (although we have not truly observed them). It can be done through marginalizing these variables out

$$
\operatorname{log} p(X \mid \theta) = \sigma_{Z} \operatorname{log} p(X, Z \mid \theta). \tag{1}
$$

The issue related to Eq.1 is the intractability as the number of values that our hidden variables can take increases. For example, suppose the *Gaussian Mixture Model* (GMM) with $N$ observations whose the latent variables - the number of clusters can take on one of values from $M$ clusers. This results in $M^N$ terms in Eq.1. 

And here comes the boom! Expectation-Maximization or EM ([Dempster et al., 1977](Dempster, A. P., Laird, N. M., & Rubin, D. B. (1977). Maximum likelihood from incomplete data via the EM algorithm. Journal of the Royal Statistical Society. Series B (Methodological), 1–38.)) delivers a appropriate solution to address this problem. The underlying assumption is that the direct optimization of the log likelihood $\operatorname{log}p(X\ mid \theta)$ is more challenging than maximizing the *complete-data log likelihood* $\operatorname{log}p(X, Z \mid \theta)$ in some statistical problems. Additionally, as we have discussed earlier, the *complete-data log likelihood* is also intractable; thereby, EM constructs a lower bound on that likelihood function and iterativel optimize that lower bound. We will see later the EM algorithm always converges to a local maximum of $p(X \mid \theta).




