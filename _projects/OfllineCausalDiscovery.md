---
layout: page
title: Offline Causal Discovery
description: Causal Discover with Online Interaction for Data Augmentation
img: assets/img/projects/Ripple.jpg
importance: 1
category: open
---

In offline reinforcement learning, an agent learns a policy from a previously gathered dataset. However, for large environments, this dataset is often very sparse, which makes it hard to determine how certain policies would perform.
Recently, Urpi et al. [1] proposed a method of extending the dataset based on causal relations between actions and features. However, this method depends on the available data, which is limited. 
That is, the data may be sufficient to infer only a subset of the causal relationships in the environment.
In this project, we look at a setting where a dataset is already present, but our agent is able to expand this dataset by exploration. How should the causal relations that the agent has already discovered alter its behavior?

**During the project, you will:**

* Learn about offline and causal RL;
* Write (Python) code to alter & apply these method for our setting.

**References:**

1. Urpı́, N. A., Bagatella, M., Vlastelica, M., and Martius, G. (2024). Causal action influence aware counterfactual data augmentation. ICML.
2. Ross, S., and Bagnell, D. (2010). Efficient reductions for imitation learning. AISTATS, 661–668.

*Supervisors:* [Merlijn Krale Msc](https://mkrale.com/), [Dr. Thiago D. Simão](https://tdsimao.github.io/) and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)
