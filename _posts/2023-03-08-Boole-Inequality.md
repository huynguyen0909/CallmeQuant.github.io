---
title: "Boole's Inequality"
date: 2023-03-08
mathjax: true
toc: true
categories:
  - Study
tags:
  - Probability theory
---


In this post, I will introduce Boole's Inequality, an upperbound on the probability of occurrence of at least one of a countable number of events under the context of individual chances of each event.  In some senses, Boole's inequality is so straightforward and often emerges as a definitely compelling inequality for any finite or countable set of events. The attractive point of this inequality is due to its weakly required assumptions, that is, Boole's inequality does not require *independence*. Hence, it is a useful methods when we are working with collection of events.

# **A short proof**
Boole's inequality can be stated formally as follows:

**Boole's inequality**. *If* $A_1, A_2, \dots, A_{n}$ are finite events in a probability space $\Sigma$, then 

$$ P(\bigcup_{i=1}^n A_i) \le \sum_{i=1}^n P(A_i) $$

*Moreover, for countable events* $A_1, A_2, \dots,$ *then,*

$$ P(\bigcup_{i=1}^\infty A_i) \le \sum_{i=1}^\infty P(A_i) $$
