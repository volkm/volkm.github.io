---
layout: page
title: Parameter synthesis
description: Analysis of parametric Markov models
importance: 3
category: research
citations: true
---

Probabilistic model checking commonly assumes that the transition probabilities are precisely known.
This assumption, however, is often impractical in reality.
Parametric Markov models allow to represent these uncertain probabilities through parameters.
Analysis of parametric Markov models then aims to answer questions such as "for which parameter values does the specification hold?" or synthesize parameter values which lead to optimal performance.

We developed analysis techniques for parametric discrete-time Markov chains {% cite DBLP:conf/qest/JansenCVWAKB14 %} and provided tool support in Storm or the dedicated Prophesy tool {% cite DBLP:conf/cav/DehnertJJCVBKA15 %}.
We also developed an analysis approach for continuous-time Markov chains with transition rates sampled from a prior distribution. The approach employs sampling-based techniques and yields the most likely behavior of the model – with a given confidence {% cite DBLP:conf/cav/BadingsJJSV22 %}.

## Applications
We applied parameter synthesis to find the optimal bias for randomized distributed algorithms {% cite DBLP:journals/dc/VolkBKA22 %}.


