---
title: "A Theory of Dictionary Attacks and its Complexity"
authors: 'Stéphanie Delaune and Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2004-06-01-Theory-Dictionary-Attacks-Complexity
date: 2004-06-01
venue: 'Proceedings of the 17th IEEE Computer Security Foundations Workshop (CSFW), pages 2–15, IEEE Computer Society Press, 2004.'
paperurl: 'https://doi.ieeecomputersociety.org/10.1109/CSFW.2004.1310728'
hal: 'https://inria.hal.science/inria-00579014v1'
citation: 'Stéphanie Delaune and Florent Jacquemard, &quot;A Theory of Dictionary Attacks and its Complexity&quot; In Proceedings of the 17th IEEE Computer Security Foundations Workshop (CSFW), pages 2–15, IEEE Computer Society Press, 2004.'
---

abstract:
We consider the problem of automating proofs of cryptographic protocols when some data, like poorly chosen passwords, can be guessed by dictionary attacks. First, we define a theory of these attacks: we introduce an inference system modeling the guessing capabilities of an intruder. This system extends the classical Dolev-Yao rules. 
Using proof rewriting techniques, we show a locality lemma for our inference system which yields the PTIME-completeness of the deduction problem. 
This result is lifted to the simultaneous solving of intruder deduction constraints with variables. Constraint solving is the basis of a NP algorithm for the protocol insecurity problem in the presence of dictionary attacks, assuming a bounded number of sessions. 
This extends the classical NP-completeness result for the Dolev-Yao model. We illustrate the procedure with examples of published protocols. The model and decision algorithm have been validated on some examples in a prototype implementation.