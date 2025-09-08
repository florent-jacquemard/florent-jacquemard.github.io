---
title: "Automation of Inductive Theorem Proving"
collection: portfolio
image: "/images/500x300.png"
description: "Short description of portfolio item number 1"
---



The purpose of Inductive Theorem Proving (ITP) is to establish the validity of conjectures in particular structures such as natural numbers, lists, and binary trees (referred to as initial models). This technique is widely used for the certification of critical applications in Computer Science and Artificial Intelligence. Inductive validity is undecidable in general,  and the automation of ITP has been investigated by the automated reasoning community for decades,  facing major challenges. 



Some ITP approaches, in the case of equational theories, work by attempting to derive an inconsistency from a set of equations and a conjecture, using general automatic deduction techniques (whose goal is to establish the validity of conjectures in all structures satisfying a theory). These automatic approaches do not use explicit recurrence schemes, so they are sometimes referred to as **inductionless induction** (see [this survey](https://www.oreilly.com/library/view/handbook-of-automated/9780444508133/B9780444508133500163_1.xhtml) for an overview of these techniques). Inductive reducibility, as property that [we have studied](portfolio/2010-CTATA/), is an example of criterion for inconsistency.

Another family of methods for automating ITP uses recurrence patterns that are computed automatically for proofs, like the systems RRL, SPIKE, PVS, ACL2, Isabelle, LEAN, Vampire... 
Generalizing a former idea from [Adel Bouhoula and Jean-Pierre Jouannaud](https://doi.org/10.1006/inco.2001.3036), with have proposed with the former at [IJACR'08](publication/2008-08-01-Automated-Induction-with-Constrained-Tree-Automata) a very general framework in which recurrence schemes are tree automata with local constraints. They are used in proofs as grammars, i.e., as tree generators replacing non-terminals, intuitively to move from case $n$ to case $n + 1$ in an induction step. These automata, computed automatically, recognize languages of terms in normal form (terms that can no longer be reduced by the rewriting system), which characterize, in the chosen framework, the initial model. They are also used in proofs as a decision tool for properties, similarly as inductionless induction procedures.

The above ITP procedure applies to specifications written in a highly expressive language: conditional constrained equational theories. It is presented as a set of inference rules whose soundness and refutational completeness is formally proved. Refutational completeness (every false conjecture will be disproved) is particularly useful for finding flaws in critical systems (as counter-examples).  The key to its generality, and the automation, is the use of constrained tree automata. The trade-off is that these procedures rely on decision problems for these automata models, which are not easy to establish and even more difficult to implement (see this [research topic](portfolio/2010-CTATA/)).

Adel Bouhoula and Miki Hermann have proposed a new ITP procedure at [IJCAI'24](https://doi.org/10.24963/ijcai.2024/361) that allows to perform 
inductive proofs in conditional unconstrained equational theories, by automatically detecting the divergence of proof traces and deriving a primal grammar and new lemmas that schematize the divergent traces, enabling the termination of the proof. The cornerstone of this procedure is the use of a new version of primal grammars which are based on primitive recursive functions, and represents the most general decidable schematization, with respect to description power, among all known schematizations. 
A first prototype of Inductive Theorem Prover based on this technique has been implemented in `C++` and has succeeded in proving automatically hundreds of examples from well known [ITP benchmarks](https://doi.org/10.48550/arXiv.cs/9604101), some of them otherwise failing with infamous theorem provers such as ACL2, Isabelle, PVS, RRL, SPIKE and LEAN.

We are know working together with the two above authors at the development of a Theorem Prover specialized for induction, scaling up the above prototype for handling conditional constrained equational theories instead of unconstrained ones. This requires the integration of the techniques based on Constrained Tree Automata presented above.  This shall represent a significant contribution to the field of automated reasoning  as our ITP tool could be used to complement existing automated and interactive proof systems  in order to leverage their performance. Indeed, initial experiments on ITP benchmarks show that induction proofs can be achieved with a high degree of automation promising future significant reductions in user interaction, hence in the time required to verify real-world critical software and systems. 









We also proposed, together with Adel Bouhoula, an adaptation of the above procedure that can be used in the context of cryptographic protocol verification, both to establish proofs (by recurrence) of protocol correctness and to derive attacks [34].

We have also proposed [36] and [3] a procedure for verifying the sufficient completeness of equation-based specifications, integrated into our framework for proof by recurrence.





In 1997, I implemented the construction of tree automata with constraints recognizing normal form terms as part of the construction of a recursive proof system based on the Maude rewriting logic language at SRI International in Stanford, as part of José Meseguer's team.





