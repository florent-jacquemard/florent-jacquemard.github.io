---
title: "Symbolic Weighted Automata"
collection: portfolio
domain: 'tata'
researchtype: theory
image: "/images/SWA-crop.png"
description: "Quantitative language models computing over infinite alphabets."
---
We study of classes of automata and transducers processing words and trees over infinite (or large) alphabet and returning a weight value in a semiring,  and applications to quantitative parsing.

With Lydia Rodriguez-de la Nava, we have studied several classes of symbolic weighted formalisms:
- automata (swA), 
- transducers (swT) and 
- visibly pushdown extensions (swVPA, swVPT). 

They combine the respective extensions of their symbolic and weighted counterparts, allowing a quantitative evaluation of words or nested words over a large or infinite input alphabet.

Properties have been shown, such as of closure by composition, the computation of transducer-defined distances between nested words and languages, and we have also proposed a PTIME 1-best search algorithm for swVPA. 

[These results](publication/2022-06-01-Symbolic-Weighted-Language-Models-Quantitative-Parsing-and-Automated-Music-Transcription) are applied to solve in PTIME a variant of parsing over infinite alphabets called *quantitative parsing*. This problem, the above best search algorithm and composition properties are the base of the techniques that we are using in our work on [Automated Music Transcription](portfolio/2025-AMT/). 

