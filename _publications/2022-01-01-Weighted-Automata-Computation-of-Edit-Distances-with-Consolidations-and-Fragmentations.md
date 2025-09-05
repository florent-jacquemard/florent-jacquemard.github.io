---
title: "Weighted Automata Computation of Edit Distances with Consolidations and Fragmentations"
authors: 'Mathieu Giraud, Florent Jacquemard'
collection: publications
category: manuscripts
permalink: /publication/2022-01-01-Weighted-Automata-Computation-of-Edit-Distances-with-Consolidations-and-Fragmentations
date: 2022-01-01
venue: 'Information and Computation, vol. 282'
paperurl: 'https://doi.org/10.1016/j.ic.2020.104652'
hal: 'https://inria.hal.science/hal-01857267'
citation: 'Mathieu Giraud, Florent Jacquemard, &quot;Weighted Automata Computation of Edit Distances with Consolidations and Fragmentations&quot; Information and Computation, vol. 282, 2022.'
---

abstract:
We study edit distances between strings, based on operations of character substitutions, insertions, deletions and additionally consolidations and fragmentations. The two latter operations transform a sequence of characters into one character and vice-versa. They correspond to the compression and expansion in Dynamic Time-Warping algorithms for speech recognition and are also used for the formal analysis of written music. 
Such edit distances are not computable in general for arbitrary rulesets. 
We propose weighted automaton constructions to compute an edit distance taking into account both consolidations and deletions, or both fragmentations and insertions. Assuming that the operation ruleset has a constant size, these constructions are polynomial into the lengths of the involved strings. 
We finally show that the optimal weight of sequences made of consolidations chained with fragmentations, in that order, is computable for arbitrary rulesets, and not computable if we reverse the order of fragmentations and consolidations.