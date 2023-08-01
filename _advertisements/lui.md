---
layout: page
title: 'Linearly Updating Intervals'
description: ''
date: 2022-11-28
tags: uncertainty-partial-information
keywords:
    - Model Learning
    - Robust decision making
    - Exploration
    - Safety
thumbnail: https://raw.githubusercontent.com/lava-lab/luiaard/master/assets/lui.gif
thumbnail_width: "60%"
---

Did you ever ask yourself how to learn a model of a system that is changing? Or did you work with interval MDPs but had no clue where the intervals came from? Or did you wonder which models are robust against uncertainty? Well, we also did. Here's our first approach {% cite DBLP:journals/corr/abs-2205-15827 -f papers %}.

"Somewhere between a and b", this is a common and intuitive way to express uncertainty. We use interval MDPs to capture epistemic uncertainty in sequential decision-making problems. We propose LUI (Linearly Updating Intervals), which updates the intervals of the MDP directly, without relying on point estimates of probabilities. This method is robust against uncertainty and adapts quickly to new environment dynamics.

#### References

{% bibliography --cited --file papers %}
