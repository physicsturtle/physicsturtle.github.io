---
layout: page
title: Tensors
course: test
unit: unit1
permalink: /test/tensors/
---

### Introduction
Most people, when they hear of tensors for the first time, are given a definition along the lines of "a tensor is an object whose components transform between coordinate systems $x$ to $x'$ according to the rule:

$$T^{\prime\alpha}_\beta = \frac{\partial x^{\prime \alpha}}{\partial x^\gamma}\frac{\partial x^\delta}{x^{\prime\beta}} T^\gamma_\delta."$$

This so-called "definition" has many problems. 
1. What is an "object"?
2. If this is a transformation rule for tensor components, then what is a tensor?
3. What are these $\alpha,\beta,\gamma,\delta$ indices?
4. What is the difference between an upper and a lower index?

Not only is this mess not the formal definition of a tensor understood by mathematicians, it doesn't function as a definition even to one who has deep familiarity with the field. It is a consequence of the formal definition of a special case of tensor, nothing more, nothing less.

To properly understand what a tensor is, and where the above "definition" comes from, we will have to take a step back into some mathematical abstraction, and encounter some definitions that seem too abstract to have to do with anything physical. Trust me when I say that if you simply memorize the abstract definitions, when we get to the concrete consequences of the definitions the rules are not difficult to work with, and before long will become second nature. 

### Definitions
Tensors have all to do with linear algebra, and nothing to do with calculus. We start with 

<div class="definition">
Definition: Let $V$ be a vector space over the field $\mathbb{F}$  and $V^*$ be its covector space. Then a *$(p,q)$ tensor over $V$* is a multi-linear map

$$T : \underbrace{V^*\times\cdots\times V^*}_{p\,\text{times}} \times \underbrace{V\times\cdots\times V}_{q\,\text{times}} \to \mathbb{F}.$$
</div>

If $\\{ e_i\\}$ is a basis for $V$, and $\\{\epsilon^j\\}$ is the corresponding dual basis for $V^*$, then we can define the components of a tensor with respect to this choice of basis. Suppose $T$ is a $(p,q)$ tensor over $V$, then its components are

$$T^{i_1 \dots i_p}_{j_1\dots i_q} = T(\epsilon^{i_1},\dots,\epsilon^{i_p},e_{j_1},\dots, e_{j_q})$$
