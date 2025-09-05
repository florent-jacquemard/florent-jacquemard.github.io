---
title: "Rewrite-Based Verification of XML Updates"
authors: 'Florent Jacquemard, Michael Rusinowitch'
collection: publications
category: conferences
permalink: /publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates
date: 2010-07-01
venue: 'In the proceedings of 12th international ACM SIGPLAN symposium on Principles and practice of declarative programming (PPDP)'
paperurl: 'https://doi.org/10.1145/1836089.1836105'
hal: 'https://inria.hal.science/inria-00578916'
citation: 'Florent Jacquemard,  Michael Rusinowitch, &quot;Rewrite-Based Verification of XML Updates&quot; In the proceedings of 12th international ACM SIGPLAN symposium on Principles and practice of declarative programming (PPDP), 2010.'
---

abstract:
We propose a model for XML update primitives of the W3C XQuery Update Facility as parameterized rewriting rules of the form: "insert an unranked tree from a regular tree language L as the first child of a node labeled by a". For these rules, we give type inference algorithms, considering types defined by several classes of unranked tree automata. 
These type inference algorithms are directly applicable to XML static typechecking, which is the problem of verifying whether, a given document transformation always converts source documents of a given input type into documents of a given output type. 
We show that typechecking for arbitrary sequences of XML update primitives can be done in polynomial time when the unranked tree automaton defining the output type is deterministic and complete, and that it is EXPTIME-complete otherwise. 
We then apply the results to the verification of access control policies for XML updates. We propose in particular a polynomial time algorithm for the problem of local consistency of a policy, that is, for deciding the non-existence of a sequence of authorized update operations starting from a given document that simulates a forbidden update operation.