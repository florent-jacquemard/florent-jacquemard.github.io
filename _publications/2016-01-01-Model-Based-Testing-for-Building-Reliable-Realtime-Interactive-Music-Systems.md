---
title: "Model-Based Testing for Building Reliable Realtime Interactive Music Systems"
authors: 'Clément Poncelet, Florent Jacquemard'
collection: publications
category: manuscripts
permalink: /publication/2016-01-01-Model-Based-Testing-for-Building-Reliable-Realtime-Interactive-Music-Systems
date: 2016-01-01
venue: 'Science of Computer Programming 132(2)'
excerpt: 'Special Issue on Software Verification and Testing (SAC-SVT 2015)'
paperurl: 'https://doi.org/10.1016/j.scico.2016.08.002'
hal: 'https://hal.science/hal-01314969'
citation: 'Clément Poncelet, Florent Jacquemard, &quot;Model-Based Testing for Building Reliable Realtime Interactive Music Systems&quot; Science of Computer Programming 132(2), 2016.'
---

abstract:
The role of an Interactive Music System (IMS) is to accompany musicians during live performances, acting like a real musician.
It must react in realtime to audio signals from musicians, according to a timed high-level requirement called mixed score, 
written in a domain specific language. Such goals imply strong requirements of temporal reliability and robustness to unforeseen errors in input, 
yet not much addressed by the computer music community.

We present the application of Model-Based Testing techniques and tools to a state-of-the-art IMS, including in particular: 
offline and on-the-fly approaches for the generation of relevant input data for testing (including timing values), with coverage criteria, 
the computation of the corresponding expected output, according to the semantics of a given mixed score, 
the black-box execution of the test data on the System Under Test and the production of a verdict. 

Our method is based on formal models in a dedicated intermediate representation, 
compiled directly from mixed scores (high-level requirements), and either passed, to the model-checker [Uppaal](https://uppaal.org) (after conversion to Timed Automata) in the offline approach, 
or executed by a virtual machine in the online approach. 
Our fully automatic framework has been applied to real mixed scores used in concerts and the results obtained have permitted to identify bugs in the target IMS.