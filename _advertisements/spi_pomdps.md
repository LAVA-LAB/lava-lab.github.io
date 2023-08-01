---
layout: page
title: 'SPI-POMDPs'
description: 'Reliable offline reinforcement learning (RL) with partial observability'
date: 2023-02-04
tags: reinforcement-learning uncertainty-partial-information
keywords:
    - Offline Reinforcement Learning
    - Partial Observability
    - Reliability
    - Safety
thumbnail: https://raw.githubusercontent.com/lava-lab/spi_pomdp/main/assets/teaser.gif
thumbnail_width: "60%"
---

Limited memory is sufficient for reliable offline reinforcement learning (RL) with partial observability.

Safe policy improvement (SPI) aims to reliably improve an agent’s performance in an environment where only historical data is available. Typically, SPI algorithms assume that historical data comes from a fully observable environment. In many real-world applications, however, the environment is only partially observable. Therefore, we investigate how to use SPI algorithms in those settings and show that when the agent has enough memory to infer the environment’s dynamics, it can significantly improve its performance {% cite spi-pomdp -f papers %}.


#### References

{% bibliography --cited --file papers %}
