---
layout: page
title: Belief Compression
description: Inexact compression of beliefs for scalable solving of POMDPs
img: assets/img/projects/Compress.jpg
importance: 1
category: open
---

When solving problems with partial observability, we often use so-called beliefs to represent the probability of our environment being in any state. However, when the number of states of a system increases, the number of possible beliefs can grow unmanageably large very quickly.
Previous work by Roy et al. [1] proposed using a variant of principal component analysis (EPCA, [2]) to reduce the dimensionality of the beliefs, thus increasing scalability. This method seems to perform well in many practical applications, despite its relatively simple compression and solving method.
In this project, we explore different methods of compressing the beliefs and/or finding better policies using the compressed beliefs.

**During the project, you will:**

* Learn about dimensionality reduction & POMDP planning algorithms;
* Write (Python) code to alter & apply these method for our setting.

**References:**

1. N. Roy, G. Gordon and S. Thrun (2005). Finding Approximate POMDP solutions Through Belief Compression.
2. Michael Collins, S. Dasgupta, Robert E Schapire (2001). A Generalization of Principal Components Analysis to the Exponential Family

*Supervisors:* [Merlijn Krale Msc](https://mkrale.com/), [Dr. Thiago D. Simão](https://tdsimao.github.io/) and [Prof. Dr. Nils Jansen](https://nilsjansen.org/)

