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


**How can we use this function to simulate an unbiased coin flip?**

This question focuses a little more on probability theory than it does on programming principles.

Let's think about some probabilities...
If we flip the coin once, our two outcomes are H (Heads) or T (Tails). 
If we flip the coin twice in a row, we have four outcome (HH, TT, TH and HT)

For a single coin flip….
P(H) = Probability of landing on heads = p
P(T) = Probability of landing on tails = (p-1)

For two coins flipped in a row:
P(HH) = P(H) * P(H) = p x p
P(TT) = P(T) * P(T) = (1-p) * (1-p)
P(TH) = P(T) * P(H) = p * (1-p)
P(HT) = P(H) * P(T) = p * (1-p)

We can notice something interesting about these probabilities. Can you spot it?

Notice how P(HT) = P(TH). this is true regardless of what the bias is (99/1, 50/50, etc...)

We can now use this information to create an unbiased coin flip by flipping a coin twice!
Since P(HH) != P(TT), we don't really care about when we land on the same side twice.
What we will do is simply wait for a result of TH or HT (Coin lands once on each side)

Then, we will simply return TH = T and HT = T (or vice versa)

