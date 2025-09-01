# TSM

Hierarchical representations of music scores
transient / IR
tree-structured



In CS, timings are generally represented by numerical values:  floating point numbers of integers when expressed in number of clock ticks.

This is in particular the case in digital representations of music performances, be it digital audio formats, spectrograms, or the discrete MIDI, where notes assigned an start time, duration, pitch and velocity.



Written music notation however is a symbolic format, where notes’ durations are expressed with a small set of symbols, corresponding to durations defined by successive divisions (whole notes, half notes etc) and combined with some constructions (ties, dots, tuplets…).

It is also the case of the multiple digital representations of music scores, either text or XML. Despite hierarchical definition of symbols’ durations and groupings… representation of durations in current encoding is essentially sequential (unstructured).



We propose an IR …



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