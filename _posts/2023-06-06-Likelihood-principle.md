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

**Likelihood principle** *The information brought by an observation* $x$ *about* $\theta$
*is entirely contained in the likelihood function* $l(\theta \lvert x)$. *Moreover,
if* $x_1$ *and* $x_2$ *are two observations depending on the same prarameter* $\theta$, *such that there exists a constant* $c$ *statisfying*

$$l_1(\theta \lvert x_1) = cl_2(\theta \lvert x_2)$$
*for every* $\theta$, *then they bring the same information about* $\theta$ *and must lead to 
identical inferences.*

In other words, the Likelihood principle states that all the pertinent information eliciting through experiment in the process of 
making inferences or decisions about the states of the nature must be given only by the *likelihood function*. As a result, it is worth noting that Likelihood principle only valid under two scenarios:

i.  The *same* parameter $\theta$ must be included in the inference.

ii. $\theta$ consists of all the uncertainty of the model. In the next section, I will illustrate a classical example (D. V. Lindley and Phillips 1976) of the failure of frequentist approach in satisfying the Likelihood principle, whereas the Bayesian framework naturally obeys this principle since it is conditional on the observed data and neutralize all the possible unknown factors inside this likelihood model.

# A Paradoxical Experiment
As I introduced earlier, the example constructed by Lindley and Phillips (1976) is a typical settings of the major shortcoming of classical statistics framework. Imagine an experiment is conducted by tossing a coin 12 times independently and observe 9 heads together with 3 tails. We construct a hypothesis about our interested bias parameter $\theta$ (the true probability of heads) in a following manner: The null hypothesis $H_0: \theta = \frac{1}{2}$ versus the alternative hypothesis: $H_1 = \theta > \frac{1}{2}$. The inadequate given information leads us to two different choices for sampling distribution (determined through the joint distribution of all observation conditioned on $\theta$):

1. **Binomial** Given $12$ independently fixed tosses, we denote $X$ to be a random variable representing the number of heads observed in those $12$ trials. Then, $X \sim \operatorname{Bin}(12, \theta)$ and 
and the likelihood function is given by

$$\mathcal{L}_{\operatorname{Binom}}(\theta) = \binom{n}{x} \theta^{x} (1- \theta)^{n - x} = \binom{12}{9} \theta^9 (1- \theta)^3. \tags{1}$$

2. **Negative Binomial** If we see our experiment set in a different view, we could reason that data was collected via tossing the coin until the *third tail* appeared. Thus, the random variable $X$ here implied the number of heads required before the $r$ events (or our experiment succeeds). Then $X \sim \operatorname{NegBin}(r=3, \theta)$

$$\mathcal{L}_{\operatorname{NegBin}}(\theta) = \binom{r + x - 1}{x} \theta^{x} (1-\theta)^{r} = \binom{11}{9} \theta^{9} (1-\theta)^3. \tags{2}$$




