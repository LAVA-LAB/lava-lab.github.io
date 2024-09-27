---
layout: page
title: Memory in RL
description: Memory architectures in reinforcement learning
img: assets/img/9.jpg
importance: 1
category: open
---

**Background:** Reinforcement learning (RL) is the prevalent framework for the control of agents in high-dimensional environments. In realistic domains, such environments are partially observable, for instance, because the agent needs to act based on vision or sensory inputs or requires reasoning over past actions [1]. It is known that agents require memory to act optimally in partially observable environments. In deep RL, various architectures have been proposed to enable agents with memory, such as recurrent neural networks [2]. However, there is still much progress to be made in (1) how to balance the short- and long-term memory of the agent, (2) how to accurately represent the history of observations of the agent's environment, and (3) how to learn efficiently with memory.

**Project:** You can test new memory architectures for (deep) RL algorithms, such as the newly introduced xLSTM [3], and compare it to existing architectures or look into developing a (specialised) architecture to accommodate memory. Your supervisors can supply you with existing code from which you can start working.

Affinity with or the motivation to learn about Markov decision processes and reinforcement learning is a big plus. Starting this project can easily lead you to a bachelor/master thesis and possibly to a scientific publication. Please feel free to reach out to maris.galesloot@ru.nl for any questions.

[1] Recurrent model-free RL can be a strong baseline for many POMDPs. ICML 2022. Ni, Eysenbach, and Salakhutdinov.

[2] Learning belief representations for partially observable deep RL. ICML 2023. Wang, Li, Klassen, Icarte, and McIlraith. 

[3] xLSTM: Extended Long Short-Term Memory. arXiv 2024. Maximilian Beck, Korbinian Pöppel, Markus Spanring, Andreas Auer, Oleksandra Prudnikova, Michael Kopp, Günter Klambauer, Johannes Brandstetter, Sepp Hochreiter.

*Supervisors:* [Maris Galesloot MSc](https://marisgg.github.io/), and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)
