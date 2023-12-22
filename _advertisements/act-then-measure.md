---
layout: page
title: 'Act-Then-Measure'
description: 'Reinforcement learning for partially observable environments with active measuring'
date: 2023-07-09
tags: reinforcement-learning uncertainty-partial-information
keywords:
    - Learning for planning and scheduling
    - Partially observable and unobservable domains
    - Uncertainty and stochasticity in planning and scheduling 
thumbnail: https://raw.githubusercontent.com/lava-lab/ATM/main/assets/teaser.gif
thumbnail_width: 20%
---

Ever wondered when you should inspect the engine of your car? Or how often an electricity provider should check their cables to minimize outages and maintenance costs? Or how often should a drone use its battery-draining GPS system to keep an accurate idea of its positions? What connects these problems is one core question: **Is the extra information from a measurement worth its cost?**

In our recent work, we try to solve such problems quickly by making a distinction between _control actions_ (which affect the environment) and _measuring actions_ (which give us information). For the first, we take into account uncertainty about the current situation but ignore it when predicting the future, which makes our method faster. For the second, we describe a novel method to determine when we can rely on our predictions, and when we should measure to eliminate uncertainty instead.

Interested in how it performs? Have a look at our [ICAPS paper](https://ojs.aaai.org/index.php/ICAPS/article/view/27197) {% cite Krale2023act  -f papers %} to find out!


#### References

{% bibliography --cited --file papers %}
