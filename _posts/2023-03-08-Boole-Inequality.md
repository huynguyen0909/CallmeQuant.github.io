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

**Boole's inequality**. *If* $A_1, A_2, \dots, A_{n}$ *are finite events in a probability space* $\Omega$, *then*

$$ P\Bigg(\bigcup_{i=1}^n A_i\Bigg) \le \sum_{i=1}^n P(A_i) $$

*Moreover, for countable events* $A_1, A_2, \dots,$ *then,*

$$ P\Bigg(\bigcup_{i=1}^\infty A_i\Bigg) \le \sum_{i=1}^\infty P(A_i) $$

We will prove this inequality by two approaches: by mathematical induction and by measure theory

## *First approach: Mathematical induction*
Suppose that a probability space $\Omega$ contains a countable collection of events $A_1, A_2, \dots, A_{n}, \dots$, then

For the case n = 1, we have 

$$P(A_1) \leq P(A_1)$$

For the case $n=2$, it is trivial to show that

$$P(A_1 \cup A_2) \leq P(A_1) + P(A_2)$$

Since $P(A_1 \cup A_2)  = P(A_1) + P(A_2) - P(A_1 \cap A_2)$

We assume that the inequality holds for the case $n$, 

$$ P \Bigg(\bigcup_{i=1}^n A_i\Bigg) \le \sum_{i=1}^n P(A_i) $$

Then,

$$
\begin{align}
P \Bigg(\bigcup_{i=1}^{n+1} A_i\Bigg) &= P\Bigg(\bigcup_{i=1}^n A_i\Bigg) + P(A_{n+1}) - \underset{P\Bigg(\bigcup_{i=1}^n A_i \cap A_{n+1}\Bigg)}{\geq 0} \\
&= 

\end{align}
$$





