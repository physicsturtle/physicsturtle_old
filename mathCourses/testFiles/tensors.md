---
layout: page
title: Tensors
course: test
unit: unit1
permalink: /test/tensors/
---

Let $V$ be a vector space over the field $\mathbb{F}$  and $V^*$ be its covector space. Then a $(p,q)$ tensor over $V$ is a multi-linear map

$$T : \underbrace{V^*\times\cdots\times V^*}_{p\,\text{times}} \times \underbrace{V\times\cdots\times V}_{q\,\text{times}} \to \mathbb{F}.$$

If $\\{ e_i\\}$ is a basis for $V$, and $\\{\epsilon^j\\}$ is the corresponding dual basis for $V^*$, then we can define the components of a tensor with respect to this choice of basis. Suppose $T$ is a $(p,q)$ tensor over $V$, then its components are

$$T^{i_1 \dots i_p}_{j_1\dots i_q} = T(\epsilon^{i_1},\dots,\epsilon^{i_p},e_{j_1},\dots, e_{j_q})$$
