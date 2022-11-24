---
layout: page
title: safe transfer RL
description: transfer in reinforcement learning with safety constraints
img: assets/img/projects/safe_transfer.png
importance: 2
category: open
---

Often we need some knowledge about the safety dynamics to ensure safety during learning {% cite DBLP:conf/atal/SimaoJS21 %}.
One can precompute unsafe behavior and mask unsafe actions using a so-called shield {% cite DBLP:conf/concur/0001KJSB20 %}, or start from an initially safe baseline policy and gradually improve its performance while remaining safe {% cite DBLP:conf/icml/AchiamHTA17 %}.
However, this approach may require many interactions with the environment before it finds a reasonable policy.

This project investigate a setting where the agent can learn in a source task before it is deployed in the target task {% cite yang2022training %}.
The goal is to speed up learning on a target task while ensuring safety.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path=page.img title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    How to train a policy in a source task such that it can learn quickly and safely_ how to solve the target task?
</div>



