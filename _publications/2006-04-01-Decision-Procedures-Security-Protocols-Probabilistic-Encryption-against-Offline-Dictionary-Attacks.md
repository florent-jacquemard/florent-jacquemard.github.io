---
title: "Decision Procedures for the Security of Protocols with Probabilistic Encryption against Offline Dictionary Attacks"
authors: 'Stéphanie Delaune and Florent Jacquemard'
collection: publications
category: manuscripts
permalink: /publication/2006-04-01-Decision-Procedures-Security-Protocols-Probabilistic-Encryption-against-Offline-Dictionary-Attacks
date: 2006-04-01
venue: 'Journal of Automated Reasoning, 36(1-2):85-124, 2006'
paperurl: 'https://doi.org/10.1007/s10817-005-9017-7'
hal: 'https://inria.hal.science/inria-00578855'
citation: 'Stéphanie Delaune and Florent Jacquemard, &quot;Decision Procedures for the Security of Protocols with Probabilistic Encryption against Offline Dictionary Attacks&quot; In Journal of Automated Reasoning, 36(1-2):85-124, 2006.'
---

abstract:
We consider the problem of formal automatic verification of cryptographic protocols when some data, like poorly chosen passwords, can be guessed by dictionary attacks. 
First, we define a theory of these attacks and propose an inference system modeling the deduction capabilities of an intruder. This system extends a set of well-studied deduction rules for symmetric and public key encryption, often called Dolev–Yao rules, with the introduction of a probabilistic encryption operator and guessing abilities for the intruder. Then, we show that the intruder deduction problem in this extended model is decidable in PTIME. 
The proof is based on a locality lemma for our inference system. This first result yields to an NP decision procedure for the protocol insecurity problem in the presence of a passive intruder. In the active case, the same problem is proved to be NP-complete: we give a procedure for simultaneously solving symbolic constraints with variables that represent intruder deductions. 
We illustrate the procedure with examples of published protocols and compare our model to other recent formal definitions of dictionary attacks.