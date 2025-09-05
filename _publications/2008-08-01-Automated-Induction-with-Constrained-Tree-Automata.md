---
title: "Automated Induction with Constrained Tree Automata"
authors: 'Adel Bouhoula, Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2008-08-01-Automated-Induction-with-Constrained-Tree-Automata
date: 2008-08-01
venue: 'In the proceedings of 4th International Joint Conference on Automated Reasoning (IJCAR), Springer LNAI vol. 5195'
paperurl: 'https://dx.doi.org/10.1007/978-3-540-71070-7_44'
hal: 'https://inria.hal.science/inria-00579004'
citation: 'Adel Bouhoula,  Florent Jacquemard, &quot;Automated Induction with Constrained Tree Automata&quot; In the proceedings of of 4th International Joint Conference on Automated Reasoning (IJCAR), Springer LNAI vol. 5195, 2008.'
---

abstract:
We propose a procedure for automated implicit inductive theorem proving for equational specifications made of rewrite rules with conditions and constraints. The constraints are interpreted over constructor terms (representing data values), and may express syntactic equality, disequality, ordering and also membership in a fixed tree language. Constrained equational axioms between constructor terms are supported and can be used in order to specify complex data structures like sets, sorted lists, trees, powerlists... 
Our procedure is based on tree grammars with constraints, a formalism which can describe exactly the initial model of the given specification (when it is sufficiently complete and terminating). They are used in the inductive proofs first as an induction scheme for the generation of subgoals at induction steps, second for checking validity and redundancy criteria by reduction to an emptiness problem, and third for defining and solving membership constraints. 
We show that the procedure is sound and refutationally complete. It generalizes former test set induction techniques and yields natural proofs for several non-trivial examples presented in the paper, these examples are difficult (if not impossible) to specify and carry on automatically with other induction procedures.