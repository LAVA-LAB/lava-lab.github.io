---
layout: page
title: Constrained Multi-agent RL
description: Reinforcement learning for multiple agents under cost constraints
img: assets/img/projects/FishSwarm.jpg
importance: 1
category: open
---

**Background:** Many modern problems, such as the optimisation of cellular networks, can be formulated as a multi-agent system with cost constraints [1]. Using this formulation, we can use machine learning methods, such as _multi-agent reinforcement learning_, to find the optimal performance for the agents. Because of the rapid increase of complexity when many agents are involved, we often need to distribute the optimisation problem in a graphical structure that models (sparse) interactions between the agents. Existing techniques exist to optimise an unconstrained multi-agent problem given a graph [2]. However, it remains an open problem to efficiently formulate and optimise in a distributed manner while satisfying constraints.

**Project:** You will work on (multi-agent) reinforcement learning algorithms, such as Monte Carlo tree search, under cost constraints [3]. In particular, we are interested in determining if we can also decompose the optimisation objective using the graph, given that we must satisfy a maximum budget of expected costs. You can analyse the problem theoretically and/or extend the aforementioned (existing) algorithms. In the latter case, your supervisors can supply you with existing code from which you can start working.

Affinity with or the motivation to learn about Markov decision processes and reinforcement learning is a big plus. Starting this project can easily lead you to a bachelor/master thesis and possibly to a scientific publication. Please feel free to reach out to maris.galesloot@ru.nl for any questions.

[1] Albin Larsson Forsberg, Alexandros Nikou, Aneta Vulgarakis Feljan, Jana Tumova. Network Parameter Control in Cellular Networks through Graph-Based Multi-Agent Constrained Reinforcement Learning. IEEE, 2023.

[2] Maris Galesloot, Thiago D. Simão, Sebastian Junges, Nils Jansen. Factored Online Planning in Many-Agent POMDPs. AAAI, 2024.

[3] Jongmin Lee, Geon-hyeong Kim, Pascal Poupart, Kee-Eung Kim. Monte-Carlo Tree Search for Constrained POMDPs. NeurIPS, 2018.

*Supervisors:* [Maris Galesloot MSc](https://marisgg.github.io/), [Dr. Thiago D. Simão](https://tdsimao.github.io/), and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)
