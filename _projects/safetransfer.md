---
layout: page
title: safe transfer RL
description: transfer in reinforcement learning with safety constraints
img: assets/img/projects/safe_transfer.png
importance: 2
category: open
---

#### Motivation

Safety is a paramount challenge for the deployment of autonomous agents in real-world applications.
In particular, ensuring safety while the agents are still learning may require considerable prior knowledge {% cite DBLP:conf/concur/0001KJSB20 DBLP:conf/atal/SimaoJS21 %}.
A possible walk-around is to pre-train the agent in a similar environment, called the _source task_ (⋄), where it can behave unsafely, such as a simulator or a laboratory, and then deploy it in the actual environment, called the _target task_ (⊙), once it has learned how to act safely.


#### Challenge
Previous work has shown that it is possible to safely transfer an agent from a source task that preserves the safety dynamics of the target task~{% cite yang2022training %}.
However, this assumption may be too strong for real-world applications.
Building high-fidelity simulators require extensive and meticulous engineering.
Furthermore, small differences in the dynamics of the source and target task can be amplified as the agent interacts multiple times with the environment, leading to performance degradation in the target task.

#### Goal
This project investigates how to transfer an agent from a source task to a (potentially adversarial) target task while maintaining the same safety guarantees.
The goal is to speed up learning on a different target task while ensuring safety.
In other words, this project investigates how to robustly make a safe transfer.


#### Main tasks
This project will build on the results from a previous ELLIS fellowship project {% cite Hogewind2023safe %} and a codebase that is already available.
The main tasks of the project involve:

- <i class="fas fa-book"></i>  Literature review and formulation of the problem statement.
- <i class="fas fa-robot"></i> Training Safe RL agents, such as SAC-Lagrangian.
- <i class="fas fa-code"></i>  Implement new methods to improve the robustness of the safe RL agents after the transfer.
- <i class="fas fa-flask"></i> Designing experiments to evaluate the safety of the transfer.


Access [lava-lab.org/projects/safetransfer](http://lava-lab.org/projects/safetransfer/) for more details.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path=page.img title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    How to train a policy in a source task such that it can learn quickly and safely learn how to solve the target task?
</div>



