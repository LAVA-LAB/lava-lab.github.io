---
layout: page
title: Delayed Observations
description: Solving Markov Decision Processes with delayed observations
img: assets/img/projects/Clock.jpg
importance: 1
category: open
---

In reinforcement learning and planning , we often assume agents immediately observe their current state, but this is often unrealistic. For example, in robotics, sensors may have processing delays, or in economics the effect on the market may only be noticeable after a while.
To address this, research has looked into extending MDPs (a very common framework for planning problems) with delays. For example, Altman [1] propose an exact method which expands the state-space, while Derman et al. [4] instead propose to use a neural network to predict the current state and use this for planning. However, the former scales poorly when delay increases, while the latter only works well when the environment is (approximately) deterministic.
In this project, we aim to find methods that scale better to high delays, but that can still compute robust policies for  stochastic environments.
During the project, you will:

* Learn how to solve (PO)MDPs using reinforcement learning;
* Write (Python) code to alter & apply these method for our setting.

**References**

1. Eitan Altman and Philippe Nain (1992).Closed-loop control with delayed information.
2. Thomas J. Walsh, Ali Nouri, Lihong Li and Michael L. Littman(2009). Learning and planning in environments with delayed feedback.
3. Mridul Agarwal, Vaneet Aggarwal (2021). Blind Decision Making: Reinforcement Learning with Delayed Observations.
4. Esther Derman, Gal Dalal, Shie Mannor (2023). Acting in Delayed Environments with Non-Stationary Markov Policies.

*Supervisors:* [Merlijn Krale Msc](https://mkrale.com/), [Dr. Thiago D. Simão](https://tdsimao.github.io/) and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)


