---
layout: page
title:  safely transferring reinforcement learning agents under adversarial attacks
# description: safely transferring reinforcement learning agents under adversarial attacks
img: assets/img/projects/safe_transfer.png
importance: 2
category: open
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path=page.img title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    How to train a policy in a source task such that it can learn quickly and safely how to solve the target task?
</div>



#### Motivation
Safety is a paramount challenge for the deployment of autonomous agents.
In particular, ensuring safety while an agent is still learning may require considerable prior knowledge {% cite Carr2023 DBLP:conf/atal/SimaoJS21 %}.
A workaround is to pre-train the agent in a similar environment, called the _source task_ (⋄), where it can behave unsafely, and deploy it in the actual environment, called the _target task (⊙)_, once it has learned how to act safely.
Such situations are common when we train the agent on a simulator or laboratory before deploying it into the real world.

#### Challenge
Previous work has shown that it is possible to safely transfer an reinforcement learning (RL) agent from a source task that preserves the safety dynamics of the target task {% cite yang2022training %}.
However, this assumption may be too strong for real-world applications.
Building high-fidelity simulators require extensive and meticulous engineering.
Furthermore, small differences in the dynamics of the source and target tasks can be amplified as the agent interacts multiple times with the environment, leading to performance degradation in the target task.


#### Goal
This project investigates how to transfer an agent from a source task to a different target task while maintaining the same safety guarantees.
In other words, this project investigates how to robustly perform safe transfers.


#### Overview
A potential approach is to train the agent in the source task  under adversarial attacks to increase the robustness of the transfer.
The project builds on the results from a previous ELLIS fellowship project {% cite Hogewind2023safe %} and the resulting codebase ([https://github.com/LAVA-LAB/safe-slac](https://github.com/LAVA-LAB/safe-slac)).

The main tasks are:

- :book:  Literature review and formulation of the problem statement.
- :robot: Training Safe RL agents, such as SAC-Lagrangian.
- :computer:  Implement new methods to improve the robustness of the safe RL agents after the transfer.
- :microscope: Designing experiments to evaluate the safety of the transfer.

#### Learn more
Access [http://lava-lab.org/projects/safetransfer/](http://lava-lab.org/projects/safetransfer/) for more details.

