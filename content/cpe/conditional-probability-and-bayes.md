---
title: "Conditional Probability and Bayes"
description: "Skeleton notes for conditional probability and Bayes' theorem"
date: 2020-11-18
author: LM
summary: "The Bayesian view of probability is quite objective and also more general than the frequentist's view. It doesn't rely on repeatition of events."
tags:
  - Bayesian
  - Bayes's Theorem
  - Conditional Probability
references:
  - name: "Association Rules"
    link: https://datumorphism.leima.is/wiki/pattern-mining/association-rules/
  - name: "Bayes' theorem @ Wikipedia"
    link: https://en.wikipedia.org/wiki/Bayes%27_theorem#/media/File:Bayes%27_Theorem_2D.svg
  - name: "Ross, S. M. (2014). Introduction to Probability and Statistics for Engineers and Scientists. Elsevier."
    link: https://doi.org/10.1016/C2013-0-19397-X
  - name: "Naive Bayes"
    link: "https://datumorphism.leima.is/wiki/machine-learning/bayesian/naive-bayesian/"
---

> one of the most important concepts in all of probability theory — that of conditional probability.
>
> -- Sheldon M. Ross

## Topics

- Association Rules
- Conditional Probability
- Naive Bayes

## Association Rules

[Association Rules](https://datumorphism.leima.is/wiki/pattern-mining/association-rules/)

$$
\text{Milk} \Rightarrow \text{Croissant} [ \text{support} = 2/5, \text{confidence} = 2/3  ]
$$

- A measure of co-occurrence

## Prize in Boxes

Three boxes M, N, O:
- Only one of them refers to a prize.
- The participant claims one of them, e.g., M.
- The host removes one of the empty boxes (N) from the other two boxes (N, O).
- Now we have only two candidate boxes for the participants, M, O.
- The participant is asked to reclaim a box.

Question:
- Should the participant switch?


## Frequentist vs Bayesian

Frequentists:
- Probability is based on the repetition of events.
- Without repetition, the probability is unknown.
- Events are random.
- Make predictions based on probabilities.
- Relies on NHST to validate our models.

Bayesian:
- Probability is objective (educated guess). It is a conceptual tool to describe our degree of certainty.
- Probability is **not necessarily** a one-to-one map of occurrences of events.
- Data (such as a previous reoccurring event) is used to update our beliefs.
- Parameters of models are random.


## Joint Probability

Joint Probability
$$
P(A\cap B)
$$
also denoted as $P(A, B)$

Examples of joint probabilities:

- $P(A, B)=0$: Event $A$ and event $B$ are so different that they will never happen together. In this case, $P(A\cup B) = P(A) + P(B)$.
- $P(A, B) = P(A)P(B)$: $A$ and $B$ are independent of each other.
- $P(A) + P(B) = 1$.

## Conditional Probability and Bayes's Theorem

$P(A\vert B)$: the probability of event $A$ if event $B$ occurred.
- It's a rescaling/(re)normailization of $P(A)$: $P(A\cap B) = P(A\vert B)P(B)$;
- We didn't specify $A$ and $B$: $P(B\cap A) = P(B\vert A)P(A)$ also holds;
- Apply $P(A\cap B) = P(B \cap A)$: $P(A\vert B)P(B) = P(B\vert A)P(A)$


In
{{<m>}}
\begin{equation}P(A\vert B) = \frac{P(B\vert A)P(A)}{P(B)}\end{equation}
{{</m>}}

- $P(A)$: prior
- $P(A\vert B)$: posterior
- $P(B\vert A)$: likelihood

$A\to H$ (A theory) & $B\to D$ (some data points)
- $P(H\vert D) = \frac{P(D\vert H)P(H)}{P(D)}$

## Solutions to the Prize in Boxes Problem

- $P(\text{Win}\vert \text{Switch}, \text{Wrong Box}) = 1$: The participant made a wrong choice at the first attempt, then switched.
- $P(\text{Win}\vert \text{Switch}, \text{Right Box}) = 0$
- $P(\text{Win}\vert \text{NoSwitch}, \text{Wrong Box})=1$
- $P(\text{Wrong Box}) = 2/3$
- $P(\text{Right Box}) = 1/3$
- $P(\text{Win}\vert \text{Switch})$: We will solve this.

Applying Bayes' theorem,

{{<m>}}
\begin{align}
P(\text{Win}\vert \text{Switch})
=& P(\text{Win}\vert \text{Switch}, \text{Wrong Box}) P(\text{Wrong Box}) + P(\text{Win}\vert \text{Switch}, \text{Right Box}) P(\text{Right Box}) \\
=& 2/3 \nonumber
\end{align}
{{</m>}}


{{<m>}}
\begin{align}
P(\text{Win}\vert \text{NoSwitch})
=& P(\text{Win}\vert \text{NoSwitch}, \text{Wrong Box}) P(\text{Wrong Box}) + P(\text{Win}\vert \text{NoSwitch}, \text{Right Box}) P(\text{Right Box}) \\
=& 1/3 \nonumber
\end{align}
{{</m>}}


We update our probability perception when we have new data.


## Rare Disease


We are about to test for a rare disease:

- Prevalence: $P(D) = 0.001$
- Test method: $P(+\vert D) = 0.99$
- Test method: $P(+\vert H) = 0.005$

The positive rate for a random person is

$$
P(+) = P(+\vert D)P(D) + P(+\vert H) P(H) = 0.006.
$$

If a test is positive, the probability of the person being test has the disease is

{{<m>}}
P(D\vert +) = \frac{P(+\vert D) P(D)}{P(+)} = 0.99\times 0.001/0.006 = 0.165.
{{</m>}}

{{<m>}}
P(H\vert +) = \frac{P(+\vert H) P(H)}{P(+)} = 0.005\times (1-0.001)/0.006 = 0.8325.
{{</m>}}


## Naive Bayes

[Naive Bayes](https://datumorphism.leima.is/wiki/machine-learning/bayesian/naive-bayesian/)