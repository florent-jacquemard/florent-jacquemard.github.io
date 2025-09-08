---
title: "Test and Verification of Realtime Interactive Music Systems"
collection: portfolio
domain: 'music'
researchtype: application
image: "/images/AscoTest-tight-global.png"
description: "Automated generation of test sets for functional reliability and temporal predictability."
---
Supervision of the development of a platform for conformance testing of the real-time Interactive Music System (IMS) 
[Antescofo](../../software/2012-antescofo/), as part of Clément Poncelet's PhD (2013-2015).

This system is used in a real-time context, in mixed music concerts involving instrumentalists and electronic devices. This use can therefore be described as *semi-critical* in that failure is not acceptable.

The general objective of this work is to provide techniques and tools to assist both programmers of mixed music music scores (i.e. composers) 
and the developers of the system itself in predicting statically the behaviour of the IMS (more specifically, 
the problems of functional reliability and temporal predictability) in response to every possible musician input. 
It should be outlined that the former are generally not experts in real-time programming, 
and we aim at giving them a clear view of what will be the outcome of the score that they are writing,  
and what are the limits of what is playable by the system. 
These verifications cannot be done manually because of the amount of unpredictable human interactions 
and timing constraints (for audio computations) involved.

We have built a framework for automated timed conformance testing, 
based on 
- a formal definition of the semantics of the language (DSL) of mixed music scores, 
- advanced symbolic state exploration techniques (model checking).

There are two main use cases of this framework:
1. Test of Antescofo on a given real score, in a context of the preparation of a concert. 
2. Test on toy scores in order to debug some particular feature of the system.

This work has been presented in the following publications:
- [JNMR'16](../../publication/2016-01-01-An-Automatic-Test-Framework-for-Interactive-Music-Systems) 
- [SCP'16](../../publication/2016-01-01-Model-Based-Testing-for-Building-Reliable-Realtime-Interactive-Music-Systems) 
- [ACM SAC'15](../../publication/2015-04-01-Model-Based-Testing-of-an-Interactive-Music-System)
- [ICMC/SMC'14](../../publication/2014-09-01-Test-Methods-for-Score-Based-Interactive-Music-Systems)

