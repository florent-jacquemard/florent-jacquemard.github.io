---
title: "Symbolic Weighted Automata"
collection: portfolio
image: "/images/SWA-crop.png"
description: "Study of classes of automata and transducers processing words and trees over infinite (or large) alphabet and returning a weight value in a demoting. Application to quantitative parsing."
---

We have studied several classes of symbolic weighted formalisms:
- automata (swA), 
- transducers (swT) and 
- visibly pushdown extensions (swVPA, swVPT). 

They combine the respective extensions of their symbolic and weighted counterparts, 
quantitative language models over infinite alphabets
...
allowing a quantitative evaluation of words or nested words over a large or infinite input alphabet.

Properties have been shown, such as of closure by composition, the computation of transducer-defined distances between nested words and languages, and we have also proposed a PTIME 1-best search algorithm for swVPA. 

These results are applied to solve in PTIME a variant of parsing over infinite alphabets called
*quantitative parsing*.

We illustrate this approach with a motivating use case in automated music transcription.