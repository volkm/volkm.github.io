---
layout: page
title: Probabilistic model checking
description: Model checking of Markov models
importance: 1
category: research
citations: true
img: assets/img/model_checking.png
---

Probabilistic model checking allows to analyses Markov models such as discrete-time Markov chains (DTMC), Markov decision processes (MDP), continuous-time Markov chains (CTMC) and Markov automata (MA).
Model checking allows to answer questions such as "what is the probability that the nuclear power plants has a critical failure within 50 years?" or "what is the optimal strategy to minimize energy consumption in a satellite while still performing the required tasks?".

## Storm
I am a main developer and maintainer of the <a href="https://www.stormchecker.org/">Storm model checker</a> {% cite DBLP:journals/sttt/HenselJKQV22 %}.
Storm is state-of-the-art for probabilistic model checking as witnessed in the Quantitative Verification Competition (<a href="https://qcomp.org/competition/2020/">QComp</a>).
Storm supports many input formats, algorithms, and queries from the literature, and is used by a growing number of other researcher and tools.
