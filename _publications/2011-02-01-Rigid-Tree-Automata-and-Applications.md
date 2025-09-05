---
title: "Rigid Tree Automata and Applications"
authors: 'Florent Jacquemard, Francis Klay, Camille Vacher'
collection: publications
category: manuscripts
permalink: /publication/2011-02-01-Rigid-Tree-Automata-and-Applications
date: 2011-02-01
venue: 'Information and Computation 209 (3),'
paperurl: 'https://doi.org/10.1016/j.ic.2010.11.015'
hal: 'https://inria.hal.science/inria-00578820'
citation: 'Florent Jacquemard,  Francis Klay,  Camille Vacher, &quot;Rigid Tree Automata and Applications.&quot; Information and Computation 209 (3), 2011.'
---

abstract:
We introduce the class of Rigid Tree Automata (RTA), an extension of standard bottom-up automata on ranked trees with distinguished states called rigid. Rigid states define a restriction on the computation of RTA on trees: RTA can test for equality in subtrees reaching the same rigid state. RTA are able to perform local and global tests of equality between subtrees, non-linear tree pattern matching, and some inequality and disequality tests as well. 
Properties like determinism, pumping lemma, Boolean closure, and several decision problems are studied in detail. In particular, the emptiness problem is shown decidable in linear time for RTA whereas membership of a given tree to the language of a given RTA is NP-complete. 
Our main result is the decidability of whether a given tree belongs to the rewrite closure of an RTA language under a restricted family of term rewriting systems, whereas this closure is not an RTA language. This result, one of the first on rewrite closure of languages of tree automata with constraints, is enabling the extension of model checking procedures based on finite tree automata techniques, in particular for the verification of communicating processes with several local non rewritable memories, like security protocols. 
Finally, a comparison of RTA with several classes of tree automata with local and global equality tests, with dag automata and Horn clause formalisms is also provided.