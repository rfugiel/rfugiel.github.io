---
layout: post
title: Two Flips are Better than One
---

Suppose you are given a function 'biased_coin()' that simulates a flip for a biased coin.

A regular coin should have a 50/50 chance of landing on either side. 
Our biased coin is not so fair. We don't know what the probability is.

We can assume 2 things about our biased coin:
  - The probability of landing on heads/tails is NOT 50/50 (That would make it unbiased)
  - The probability for either side is NOT 100% (The coin has at least some chance of landing on either side)


**How can we use this function to simulate an unbiased coin flip?***

This question focuses a little more on probability theory than it does on programming principles.

Let's call the probability of the biased coin landing on heads P.

P = Probability of the biased coin landing on heads
(1-P) = Probability of the biased coin landing on tails
