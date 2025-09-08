---
title: "Specification and verification of security protocols"
collection: portfolio
domain: 'tata'
researchtype: application
description: "former research topic (1999-2005)"
---

Security protocols describe messages exchanged by agents in a hostile environment and composed using cryptographic primitives. They are sometimes described in scientific literature using a semi-formal notation known as Alice-Bob language, which specifies the content of messages between protocol actors (agents). This syntax can be seen as a textual representation of Message Sequence Charts used in RFCs, among other places. This language is simple and concise for describing the overall flow of a protocol, but it is nevertheless ambiguous and obscures the local operations of each agent.

We have implemented a procedure for compiling Alice-Bob specifications into multi-set rewriting rules that precisely describe the operations of agents for analyzing received messages and constructing sent messages, as well as the capabilities of attackers. The translation of this intermediate language into input format (Horn clauses) for the daTac demonstrator, and subsequently for other tools, enables formal verification of protocols using narrowing procedures. 
The whole system, presented at [LPAR'00](https://inria.hal.science/inria-00099161v1), forms the 
[CASRUL](/software/1999-CASRUL/) system,
the first version of which was written at that time and which subsequently became a component of the European 
[AVISS](https://memsic.ccsd.cnrs.fr/UNIV-BM-THESE/inria-00100915v1) and its successor [AVISPA](https://avispa-project.org).

Later, I worked with Stéphanie Delaune on similar problems 
([CSF'04](https://doi.ieeecomputersociety.org/10.1109/CSFW.2004.1310728), 
 [UNIF'04](https://people.irisa.fr/Stephanie.Delaune/PUBLICATIONS-HTML/b2hd-dj-unif2004.html), 
 [CCS'04](https://doi.org/10.1145/1030083.1030121), 
 [JAT'06](https://doi.org/10.1007/s10817-005-9017-7)), 
 improving in particular the CASRUL approach (narrowing) by adding explicit destructive symbols defined by equational theories and applying the basic strategy for narrowing (in the sense that this latter model allows more attacks to be detected).

This latter model also inspired studies of [constrained tree automata](/portfolio/00-CTATA/), and, in a very different vein, 
[membrane computations](https://doi.org/10.1007/3-540-29937-8_10). 
Intuitively, the idea is that automata can be used to characterize the (infinite) set of messages that can be exchanged by a protocol. 
The automata model of 
([IJCAR'06](https://doi.org/10.1007/11814771_45),
 [JAL'08](/publication/2008-01-01-Tree-automata-with-equality-constraints-modulo-equational-theories) 
improves on that of 
[CCS'04](https://doi.org/10.1145/1030083.1030121), 
and the satisfiability decision procedure for these automata models is a generalization of basic narrowing for equations to Horn clauses.

