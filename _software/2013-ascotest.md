---
name: Antescofo realtime testing enrironment
duration: 2014 &mdash; 2017
organization: Inria, Ircam
main_dev: Clement Poncelet-Sanchez
---

This work was realized by Clement Poncelet-Sanchez during its phd,
in the context of the developpement of 
the score-based Interactive Music System (IMS)
[Antescofo](https://jacquema.gitlabpages.inria.fr/software/antescofo)
by team Mutant at Ircam.

The general objective 
is to provide techniques and tools to assist both programmers of 
mixed music scores (i.e. composers) and the developers of the system itself
in predicting statically the behavior of the IMS 
(more specificaly, the problems of
functional reliability and temporal predictability)
in response to every possible musician input. 
It should be outlined that the former are generally not experts in real-time programming, and we aim at giving them a clear view of what will be the outcome of the score that they are writing, 
and what are the limits of what is playable by the system. 
These verifications cannot be done manually 
because of the amount of unpredictable human interactions 
and timing constraints (for audio computations) involved.

We have built a framework for automated timed conformance testing, 
based on 
* a formal definition of the semantics of the language (DSL) of mixed music scores, 
* advanced symbolic state exploration techniques (model checking).

There are two main use cases of this framework:
1. Test of Antescofo on a given real score, in a context of the preparation of a concert. 
1. Test on toy scores in order to debug some particular feature of the system.

Our test framework contains various independent modules (altogether 18 000 locs), such as: 
* A frontend compiler of scores in Antescofo DSL into IR models, on the top of Antescofo Flex/Bison parser (13 000 C++ locs); 
* Command-line tools and scripts for convenience conversion and comparison of timed input and output traces including an adapter for online workflow; 
* Convenience Scripts for deployment of the [UPPAAL Suite](http://www.uppaal.org) in our workflow; 
* specific adapter function for the Antescofo Standalone version. 
Documentations are provided to permit an easy use and understanding of the framework.
