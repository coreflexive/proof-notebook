---
layout: post
title: "Injectivity of the Successor Function"
date: 2025-05-12
tags: [peano, natural numbers, logic, injectivity]
---

![S_injective proof]({{ site.baseurl }}/assets/2025-05-12_s_injective.jpg)

### Summary

A structured derivation of the injectivity of `S`, showing how from `S n = S m` we conclude `n = m`.

### Commentary

I wanted to capture the logical content of constructor injectivity without relying on Coq's `injection` tactic. The structure reflects how I would teach this proof using universal quantification, assumption labeling, and visual separation of assumptions and goals.
