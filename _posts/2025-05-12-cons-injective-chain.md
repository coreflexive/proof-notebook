---
layout: post
title: "Injectivity Chain via `cons` and Transitivity"
date: 2025-05-12
tags: [lists, injectivity, transitivity, structured derivation]
---

### Goal

Here's a theorem about lists:

\\[
\forall (X : \text{Type})\, (x\, y\, z : X)\, (l\, j : \text{list}\ X),\ 
  x :: y :: l = z :: j \land j = z :: l \Rightarrow x = y
\\]

I'll show you my handwritten proof which uses the injectivity of the `cons` constructor for polymorphic lists.  Each data type has its own injection theorem, so when we say `injection` in a proof assistant like Coq, we get the the version appropriate to the type we're consuming.  This being an informal (handwritten) proof, we need to be clear about what injection means for our _particular_ proof.  For polymorphic lists, we would state the theorem informally. Perhaps we would write this:

\\[
 \[ x :: l = y :: j \Rightarrow x = y \wedge l = j\]
\\]

Let's not get to deep into the meaning of the square-brackets.  It means for us that the variables are universally quantified and implies that they all have the correct type.  Now for the proof.

![Handwritten proof]({{ site.baseurl }}/assets/2025-05-12_cons-injective-chain.jpg)

### Summary

We show that two nested `cons`-list equalities imply `x = y`, by:
1. Applying constructor injectivity on the head of the list.
2. Using transitivity to align the inner tail terms.
3. Applying constructor injectivity again.
4. Finishing with transitivity to reach the goal.

### Commentary

This derivation highlights how list constructor injectivity and transitivity work together to support layered reasoning.
