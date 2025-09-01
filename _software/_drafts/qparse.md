# qparse



**tokenization**

we proposed in 2024 a method for building a formal correspondence between subsets, called tokens, of discrete events in a given music performance recorded as a MIDI sequence, and the associated music notation symbols, such as notes, rests, chords, and ornaments. Our tokenization procedure is integrated with an algorithm for music transcription based on parsing wrt a weighted tree grammar. 



DRAFT 



The transcription procedure is based on a prior language model  of musical scores

describing the prefered music notations.

In contrast to other tools using on sequential models (Markov chains), our language model (weighted tree automata) is hierarchical, allowing to take into account the deep structure of common Western rhythm notation (musical meter, rhythms beaming **etc**).

Such languages can be built using several methods, in particular they can be learned from corpora, for a transcription in a given notational style.

