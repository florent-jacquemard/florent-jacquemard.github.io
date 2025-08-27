---
name: qparse 
link: https://gitlab.inria.fr/qparse/qparselib
duration: 2017 &mdash; Present
sources: https://gitlab.inria.fr/qparse/qparselib
organization: Inria
---

qparse is a C++ library for automated music transcription.

It converts a symbolic musical performance, 
given as a sequence of musical events with arbitrary dates and durations 
(typically an unquantified [MIDI file](https://www.midi.org/specifications-old/item/standard-midi-files-smf)),
into a structured music score.
Several output formats are possible, 
including [MEI](http://music-encoding.org/about/)
and [Lilypond](http://lilypond.org).

The transcription procedure is based on a prior language model 
of musical scores
describing the prefered music notations.
In contrast to other tools using on sequential models (Markov chains), 
our language model (weighted tree automata) is hierarchical,
allowing to take into account 
the deep structure of common Western rhythm notation
(musical meter, rhythms beaming *etc*).
Such languages can be built using several methods, 
in particular they can be learned from corpora, 
for a transcription in a given notational style.

Transcription then works by parsing the input against the language model.
It chooses a optimal output score according to criteria 
of fitness to input and conformity to the prior language.
Several models of performances are available
for evaluating the fitness of score to input events,
including stochastic models and models based on tropical algebra. 
The transcription can be performed offline, on an input file recording a performance, 
but also online, given an input stream (*e.g.* from a MIDI keyboard),
thanks to the efficient Dynamic Programming algorithms for parsing.

