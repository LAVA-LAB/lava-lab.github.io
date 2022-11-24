---
layout: page
title: RNN for uPOMDPs
description: Verifiable RNN-Based Policies for Uncertain POMDPs
img: assets/img/projects/rnn_upomdp.jpg
importance: 1
category: open
---

Recurrent neural networks (RNNs) {% cite DBLP:journals/neco/HochreiterS97 %} are an effective representation of policies for partially observable Markov Decision Processes (POMDPs){% cite DBLP:journals/ai/KaelblingLC98 %}.
However, a major drawback of RNN-based policies is the difficulty to formally verify behavioural specifications, e.g. with regard to reachability and expected cost. 
In previous work, we proposed to insert a quantized bottleneck network (QBN) to the RNN that learns a mapping from the latent memory states to quantized vectors, which enables the extraction of a finite-state controller (FSC) representation of the RNN {% cite DBLP:journals/jair/Carr0T21%}.
This FSC, together with a POMDP model description, constitutes a policy-induced Discrete-Time Markov Chain (DTMC) that allows us to use efficient formal verification methods. 
For the scenarios in which the FSC fails to satisfy the behavioural specification, the verification method generates diagnostic information in the form of critical examples.
These critical examples can be used to re-train the RNN and extract an updated FSC.

In this project, we are interested to investigate the synthesis of policies with formally verified satisfaction of behavioural specifications in uncertain POMDPs (uPOMDPs) {% cite DBLP:conf/ijcai/Suilen0CT20 DBLP:conf/aaai/Cubuktepe0JMST21 %}, where the uncertainty is expressed by polynomial parameterizations of the transition and/or observation probabilities. 
The uPOMDP describes a set of possible POMDPs that can be used to express imperfect knowledge of the environment, e.g. because the POMDP is an abstraction of real-world dynamics.
Our goal is to learn and extract an FSC that has the best worst-case performance among all possible instantiations of the uPOMDP.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path=page.img title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    
</div>



