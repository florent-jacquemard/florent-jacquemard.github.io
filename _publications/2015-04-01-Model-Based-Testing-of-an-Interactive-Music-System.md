---
title: "Model Based Testing of an Interactive Music System"
authors: 'Clément Poncelet, Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2015-04-01-Model-Based-Testing-of-an-Interactive-Music-System
date: 2015-04-01
venue: 'In the proceedings of Proceedings of the 30th ACM/SIGAPP Symposium On Applied Computing (ACM SAC)'
paperurl: 'https://doi.org/10.1145/2695664.2695804'
hal: 'https://hal.science/hal-01097345'
citation: 'Clément Poncelet, Florent Jacquemard, &quot;Model Based Testing of an Interactive Music System&quot; In the proceedings of Proceedings of the 30th ACM/SIGAPP Symposium On Applied Computing (ACM SAC), 2015.'
---

abstract: 
The role of an interactive music system (IMS) is to accompany musicians during live performances, like a real musician. It reacts in realtime to audio signals from musicians, according to a timed specification called mixed score, written in a domain specific language. Such goals imply strong requirements of temporal reliability and robustness to unforeseen errors in input, yet not so much studied in the computer music community.

We present the application of model-based testing techniques and tools to a state-of-the-art IMS, including the following tasks: generation of relevant input data for testing (including timing values) following coverage criteria, computation of the corresponding expected output, according to the semantics of a given mixed score, black-box execution of the test data and verdict. Our method is based on formal models compiled directly from mixed scores, and passed, after conversion to timed automata, to the model-checker Uppaal. This fully automatic approach has been applied to real mixed scores used in concerts and the results obtained have permitted to identify bugs in the target IMS.