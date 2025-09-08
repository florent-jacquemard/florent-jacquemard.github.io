---
title: "Tree-Structured Representations of Timed Data"
collection: portfolio
image: "/images/TSM.png"
description: "A hierarchical Abstract Intermediate Representation of Music Notation"
---

This abstract model of digital musical score is used as an intermediate representation in applications related to the processing of written music. Its principle is that, like in symbolic music notation, durations are defined hierarchically, be recursive division of time-spans.

In Computer Science, timings are generally represented by numerical values: floating point numbers or integers when expressed in number of clock ticks. This is in particular the case for digital formats for storing music performances, whether audio, spectrograms, or MIDI files (discrete sets of events assigned with a start time and duration).

Written music notation is however a symbolic format, where notes’ durations are expressed with a small set of symbols, corresponding to durations defined by successive divisions (whole notes, half notes etc) and combined with some constructions (ties, dots, tuplets…). The digital encodings of music scores, either text or XML, are also symbolic. However, they structure their musical content essentially sequentially, despite the hierarchical organisation of the written music content in common notation (with horizontal and vertical grouping of events). 

In the IR that we are proposing, implemented on the [TSM library](soft/2022-TSM), the temporal data of written music content is represented in the form of DAGs (shared node trees), whose branches correspond to divisions of time intervals. Such tree-like representations are common in the fields of musicological analysis and musical composition assistance tools (see e.g. these articles published at [MCM](2015-06-01-A-Structural-Theory-of-Rhythm-Notation-based-on-Tree-Representations-and-Term-Rewriting), [MEC](2015-05-01-Towards-an-Equational-Theory-of-Rhythm-Notation), [TENOR](2017-05-01-Generating-equivalent-rhythmic-notations-based-on-rhythm-tree-languages) or in the [IFIP WG 1.6 on term rewriting](publication/2014-07-01-Rhythm-Tree-Rewriting)). In the case of our model, they allow the use of formal tools such as rewriting or formal languages formalisms for processing and reasoning on digital musical scores.

The Tree-structured Score Model (TSM) is available as a C++ library and a Python module. It allows the construction of digital musical scores, their transformation, and is used as a central Intermediate Representation in various music processing problems, such as automated music transcription, or music score transformation or comparison.  It also offers facilities for evaluating musical notation complexity and similarity measures. It can be exported into several XML music encodings such as MEI and MusicXML (work of Clément Buon for the latter).



## RA 24

`TSM` is an abstract tree-structured model of digital musical score, used as an intermediate representation in applications related to the processing of written music.

**functional**

Available as a C++ library and a Python module, `TSM` allows the construction of musical score models, their transformation and export to XML encodings. It also offers facilities for evaluating musical notation complexity and similarity measures.

The `TSM` C++ code is currently integrated into the git repository of the `qparse` transcription tool for which it was originally designed, but it is standalone and shall be migrated to an independent repository.



**scientific**

`TSM` offers a structured model of written musical data, whose temporal dimension is in an intermediate representation between the real values used in acoustics and the symbolic representations of conventional Western musical notation. More precisely, temporal information is represented in the form of DAGs (shared node trees), whose branches correspond to divisions of time intervals.

Such tree-like representations are common in the fields of musicological analysis and musical composition assistance tools.

In the case of `TSM`, they allow the use of formal tools such as rewriting or formal languages for processing and reasoning on digital musical scores.



## RA 23

the Tree-structured Score Model (TSM) is used as a central Intermediate Representation (IR) in various music processing problems, such as automated music transcription (AMT). Some additions in this IR, related in particular to voice separation, chords and ornaments, and a new index of the tree content permitted important gain in efficiency for computation and transformation, by rewriting, of music scores in this IR.

These developments have also enabled a redesign of the export procedure of the IR into the XML MEI encoding (for music score), and Clément Buon has written during his M1 internship in June and July a new exporter into the MusicXML encoding.









Hierarchical representations of music scores
transient / IR
tree-structured



