---
layout: post
title: "Injectivity Chain via `cons` and Transitivity"
date: 2025-05-12 13:10:00
tags: [lists, injectivity, transitivity, structured derivation]
---

### Theorem

\[
\forall (X : \text{Type})\, (x\, y\, z : X)\, (l\, j : \text{list}\ X),\ 
  x :: y :: l = z :: j \land j = z :: l \Rightarrow x = y
\]

![Handwritten proof]({{ site.baseurl }}/assets/2025-05-12_cons_injective_chain.jpg)

### Summary

We show that two nested `cons`-list equalities imply `x = y`, by:
1. Applying constructor injectivity on the head of the list.
2. Using transitivity to align the inner tail terms.
3. Applying constructor injectivity again.
4. Finishing with transitivity to reach the goal.

### Commentary

This derivation highlights how list constructor injectivity and transitivity work together to support layered reasoning.
