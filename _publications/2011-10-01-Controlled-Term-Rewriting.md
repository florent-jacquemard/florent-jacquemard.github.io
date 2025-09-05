---
title: "Controlled Term Rewriting"
authors: 'Florent Jacquemard, Yoshiharu Kojima, Masahiko Sakai'
collection: publications
category: conferences
permalink: /publication/2011-10-01-Controlled-Term-Rewriting
date: 2011-10-01
venue: 'In the proceedings of Proceedings of the 8th International Symposium Frontiers of Combining Systems (FroCoS)'
paperurl: 'https://doi.org/10.1007/978-3-642-24364-6_13'
hal: 'https://inria.hal.science/hal-00643160'
citation: 'Florent Jacquemard, Yoshiharu Kojima, Masahiko Sakai, &quot;Controlled Term Rewriting&quot; In the proceedings of Proceedings of the 8th International Symposium Frontiers of Combining Systems (FroCoS), 2011.'
---

abstract:
Motivated by the problem of verification of imperative tree transformation programs, we study the combination, called controlled term rewriting systems (CntTRS), of term rewriting rules with constraints selecting the possible rewrite positions. These constraints are specified, for each rewrite rule, by a selection automaton which defines a set of positions in a term based on tree automata computations.

We show that reachability is PSPACE-complete for so-called monotonic CntTRS, such that the size of every left-hand-side of every rewrite rule is larger or equal to the size of the corresponding right-hand-side, and also for the class of context-free non-collapsing CntTRS, which transform Context-Free (CF) tree language into CF tree languages.

When allowing size-reducing rules, reachability becomes undecidable, even for flat CntTRS (both sides of rewrite rules are of depth at most one) when restricting to words (i.e. function symbols have arity at most one), and for ground CntTRS (rewrite rules have no variables).

We also consider a restricted version of the control such that a position is selected if the sequence of symbols on the path from that position to the root of the tree belongs to a given regular language. This restriction enables decision results in the above cases.