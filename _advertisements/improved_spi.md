---
layout: page
title: ''
description: ''
date: 2023-08-23
tags: reinforcement-learning
keywords:
    - Offline reinforcement learning
    - Sample efficiency
    - Reliability
    - Safety
thumbnail: https://raw.githubusercontent.com/lava-lab/improved_spi/main/assets/teaser.gif?raw=true
thumbnail_width: "60%"
---

The available data is often limited in offline reinforcement learning. Current methods reliably manage to compute new policies that outperform the data collection policy. However, they might require prohibitive amounts of data. As we cannot collect more data, it is primordial to make the most out of the data available. Therefore, we develop a transformation of the underlying MDP with smaller bounds on the minimum amount of data required for improvement {% cite Wienhoft2023more -f papers %}. This allows offline RL algorithms to return better policies without losing reliability.


#### References

{% bibliography --cited --file papers %}
