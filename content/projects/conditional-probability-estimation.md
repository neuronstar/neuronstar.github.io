---
title: "Conditional Probability Estimation"
images:
  - "/covers/projects/cpe.svg"
categories:
  - Machine Learning
  - Statistics
tags:
  - Probability
  - Estimation Theory
summary: "Understand models to estimate conditional probabilities"
fields:
date: 2020-11-03
status: In Progress
sections:
  - cpe
draft: false
---


{{< message class="danger" title="Current Topic" >}}

Our Current Topic is Deep Learning for Time Series.

Here is a preliminary list of papers to be discussed.

| Topics | Paper |
|-----|-----|
| Review | [Time Series Forecasting With Deep Learning: A Survey](https://arxiv.org/abs/2004.13408) |
| Review | ["Gneiting T, Katzfuss M. Probabilistic Forecasting. Annu Rev Stat Appl. 2014;1: 125–151. doi:10.1146/annurev-statistics-062713-085831"](https://www.annualreviews.org/doi/abs/10.1146/annurev-statistics-062713-085831) |
| Uncertainty | [Conformal Time-series Forecasting](https://proceedings.neurips.cc/paper/2021/hash/312f1ba2a72318edaaa995a67835fad5-Abstract.html) |
| Uncertainty | [Probabilistic Forecasting: A Level Set Approach](https://www.amazon.science/publications/probabilistic-forecasting-a-level-set-approach) |
| Probabilistic | [Autoregressive Dernoising Diffusion Models for Mutivariate Probablistic Forecasting](https://arxiv.org/abs/2101.12072) |
| Probabilistic | [DeepAR: Probabilistic Forecasting with Autoregressive Recurrent Networks](https://arxiv.org/abs/1704.04110) |
| Probabilistic | [Probabilistic Time Series Forecasting with Implicit Quantile Networks](https://arxiv.org/abs/2107.03743) |
| Probabilistic | [Multivariate Probabilistic Time Series Forecasting via Conditioned Normalizing Flows](https://arxiv.org/abs/2002.06103) |
| Probabilistic | [Probabilistic Time Series Forecasting with Structured Shape and Temporal Diversity](https://arxiv.org/abs/2010.07349) |
| Probabilistic | [Deep Factors for Forecasting](https://arxiv.org/abs/1905.12417) |
| Transformer | [(TFT) Temporal Fusion Transformers for Interpretable Multi-horizon Time Series Forecasting](https://arxiv.org/abs/1912.09363) |
| AE | [Recurrent Neural Filters: Learning Independent Bayesian Filtering Steps for Time Series Prediction](https://arxiv.org/abs/1901.08096) |
| ? | [N-BEATS: Neural basis expansion analysis for interpretable time series forecasting](https://arxiv.org/abs/1905.10437) |
| Causal Inference | [Causal Inference for Time series Analysis: Problems, Methods and Evaluation](https://arxiv.org/abs/2102.05829) |
| Evaluation | [Random Noise vs State-of-the-Art Probabilistic Forecasting Methods : A Case Study on CRPS-Sum Discrimination Ability](https://arxiv.org/abs/2201.08671) |
| Evaluation | [An introduction to multivariate probabilistic forecast evaluation](https://www.sciencedirect.com/science/article/pii/S2666546821000124) |
| Evaluation | [Evaluating Probabilistic Forecasts with scoringRules](https://www.jstatsoft.org/article/view/v090i12) , [Scoring Rules for Continuous Probability Distributions](https://www.jstor.org/stable/2629907) |
| Traditional Method | [Forecasting: Principles and Practice](https://otexts.com/fpp2/) |
| Preprocessing | [Time Series Data Augmentation for Deep Learning: A Survey](https://arxiv.org/abs/2002.12478) |


{{< /message >}}


## When and How

The discussions are hosted online in Lark/Wechat.

- [Lark](https://www.feishu.cn/) is our primary communication channel.
- Wechat is mostly for our backup plans.

If you would like to be part of the party, please create a post here on [GitHub discussions](https://github.com/neuronstar/seminar-discussions/discussions/categories/papers-please).

The discussions are mostly in Chinese.

### When

This is a bi-weekly meetup.

There are two different ways to keep track of the upcoming events:

1. add this ics to your calendar.
   - [Calendar ics url](https://outlook.live.com/owa/calendar/00000000-0000-0000-0000-000000000000/8455418e-3cff-4bcd-aa40-34b06bce6053/cid-68E8EF2C5F954378/calendar.ics): Add this ICS to your calendar app to follow the upcoming events.
2. If you would like to add individual events by yourself, use the "**Add to Calendar**" button on the specific event page.
   - Here is the button: {{< figure src="../assets/add-to-calendar-demo.png" >}}



As a preview of the events, here is a calendar web page for the upcoming events ([Calendar Page](https://outlook.live.com/owa/calendar/00000000-0000-0000-0000-000000000000/8455418e-3cff-4bcd-aa40-34b06bce6053/cid-68E8EF2C5F954378/index.html)):


{{< iframe url="https://outlook.live.com/owa/calendar/00000000-0000-0000-0000-000000000000/8455418e-3cff-4bcd-aa40-34b06bce6053/cid-68E8EF2C5F954378/index.html" >}}



### Rules

- Everyone shall get their chance to lead the discussion.
- The first principle is to understand the content. Interrupt and ask any questions to make sure we all understand the content well.



## Why this Topic

Conditional probability estimation is one of the most fundamental problems in statistics.

- Conditional probability estimation is frequently used in solving both real life and academic problems. One is likely to encounter this problem at some point of their life.
- If you are inferring, you are probably using conditional probabilities. It is a perspective.
- There are many models and methods to estimate the conditional probability. We can learn about and from these models and methods.
- We need a universal model to solve this problem for productivity. A universal model for this task will save us a lot of time and energy.
- Many machine learning methods are based on conditional probabilities.
  - Many classifiers
  - Bayesian networks
  - ...


## What is Our Approach

- Read and Discuss
- Apply on toy problems


### Reading List and References

We will update this list on our way forward. [Here is a partial list of references](/cpe/00.references/).

{{< card title="Initial Proposal (Outdated)" >}}

As a start this is an outline of what should be covered.

- What is the conditional probability?
  - Sampling theory
  - Bayes
  - Representation of a conditional probability
- Statistical methods to estimate the conditional probability
  - The list is enormous. We will only concentrate on the basics.
- Tree-based
  - Tree as "clustering" method
  - Application on the bike-sharing problem
- NN-based
  - NN as feature transformations
  - Application on the bike-sharing problem
- EM Methods
- Variational Methods
- Normalizing Flow
- To be added as we learn more about it

{{< /card >}}


{{< card title="oy Problems (Outdated)" >}}

We have prepared dataset that can be used both for classification problems and regression problems.

- [Bike-sharing data](https://1drv.ms/u/s!AtL-RuK9jxYZaxakx4KhPPbBR50?e=8EQxtg)

{{< /card >}}


## Tools

- Timezone conversions: [World Clock](https://www.worldtimebuddy.com/?qm=1&lid=1816670,12,5,8&h=12&date=2021-9-4&sln=14.5-16&hf=0)

