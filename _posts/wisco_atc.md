---
layout: post
title: Wisconsin Trading Platform
date: 2016-11-07 16:27:31
disqus: y
---


This semester, I've been helping my friend Sam work on a trading platform with a club he founded at the University of Wisconsin, Madison.

We're writing code to automate trading in the FOREX market. A couple things we've done:

1. Hosted our package so it works real-time, around the clock
2. Writen code to pull in and parse market data
2. Written code that runs benchmark macro analysis market indicators on the market data
3. Integrated our indicator outputs with the trading platform API to execute trades based on our analysis

---

### Moving forward
A couple things we're working on in the next couple months:

1. Pass indicators of the state of the market to a classifiers trained on when it's most beneficial to consult a particular market indicator
2. Pass the outputs from various indicators as features to a simple network trained on their respective results and the market outcome
3. Code up a more complex LSTM in tensorflow and throw it at the market indicator feature set.

---

Have ideas? Suggestions? Feel free to reach out at rileyedmunds@berkeley.edu
