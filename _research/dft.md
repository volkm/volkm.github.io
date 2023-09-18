---
layout: page
title: Dynamic fault trees
description: Static and dynamic fault tree analysis
importance: 2
category: research
citations: true
img: assets/img/dft_example.png
---

Fault trees are a common modelling formalism in reliability engineering.
They model how failures occur and propagate in a system, and eventually lead to a system failure.
Dynamic fault trees extend classical (static) fault trees and support more faithful modelling of spare management, functional dependencies and ordered failures.

## Efficient fault tree analysis
We developed several algorithms for DFT analysis based on probabilistic model checking and showed that our approaches perform significantly better than existing approaches {% cite DBLP:journals/tii/VolkJK18 %}.

## Industrial case studies
We showed the practical relevance of DFT analysis in several industrial case studies.
Together with BMW AG, we modelled a vehicle guidance systems for autonomous driving {% cite DBLP:journals/ress/GhadhabJKKV19 %} and found optimal partitionings of functions on hardware.
Together with researcher from railway engineering, we investigated the impact of infrastructure failures on the availability of train routes in German railway stations {% cite DBLP:journals/sttt/WeikVKN22 %}.
Together with Électricité de France, we analysed parts of a nuclear power plant {% cite DBLP:conf/prdc/KhanK0B19 %}.

