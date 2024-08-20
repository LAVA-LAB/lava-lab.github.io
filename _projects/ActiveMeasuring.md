---
layout: page
title: Delayed Observations
description: Deciding the value of information in Markov decision processes
img: assets/img/projects/Magnefied.jpg
importance: 1
category: open
---

In reinforcement learning and planning problems, we often assume agents can observe their state for free, but this is often unrealistic. For example, inspections of machinery might require hiring (expensive) personnel, or constantly using a robot's sensors might unnecessarily drain its battery.

Active-measure MDPs (AM-MDPs) are a framework where we instead assume the agent mustdeliberately take a costly *measuring action* in order to determine its current state. In an RL setting, such costly measurements are useful both for *learning* an accurate representation of your environment, as well as for *computing* a better policy. Although methods for solving AM-MDPs exist, many focus on only one of these two benefits.

In this project, we aim to combine or improve existing methods of solving AM-MPDs, such that they both cheaply learn a model as well as plan good policies for them.

**During the project, you will:**
* Learn about reinforcement learning in general and AM-MDPs in particular;
* Extend our existing (Python) code with better exploration polcies.

**References:**

1. Colin Bellinger, Mark Crowley, Isaac Tamblyn (2020). Active Measure Reinforcement Learning for Observation Cost Minimization.
2. Merlijn Krale, Thiago D. Simão and Nils Jansen (2023). Act-then-measure: reinforcement learning for partially observable environments with active measuring.
3. Colin Bellinger, Mark Crowley and Isaac Tamblyn (2023). Learning in POMDPs is Sample-Efficient with Hindsight Observability

*Supervisors:* [Merlijn Krale Msc](https://mkrale.com/), [Dr. Thiago D. Simão](https://tdsimao.github.io/) and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)