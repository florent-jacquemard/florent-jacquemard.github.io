---
name: TSMdiff
begindate: 2026-01-01
enddate: 2026-12-31
sources: https://tsm-diff-lbd-7a7e2a.gitlab.io
permalink: /software/2026-TSMdiff
organization: Inria
---

TSM-diff is a new procedure for comparing digital music scores in various encoding such as [MusicXML](https://www.musicxml.com) or [MEI](https://music-encoding.org), based on a graph-structured abstract intermediate representation called Tree Score Model ([TSM](software/2022-TSM)).

Given two scores, after conversion into TSM, our procedure calculates jointly: 

- a list of differences, localised by time positions in the input scores;
- a time distance: cumulated durations of time intervals where scores differ;
- an edit distance, called surface distance, based on notational attributes not related to time. 

The two latter metrics are normalised and combined into a similarity distance between scores.

Our approach builds on two previous tools  [score-diff](software/2019-scorediff), was developed by Francesco Foscarin during his PhD and its fork [musicdiff](https://github.com/gregchapman-dev/musicdiff)  by Greg Chapman. The most crucial difference is a change in the intermediate representation of score content used for comparison: the two above tools are based on unstructured [Music21](https://music21.org) streams, whereas we use the new representation TSM structured as labelled directed acyclic graphs (DAGs), inspired by [rhythm trees](https://support.ircam.fr/docs/om/om6-manual/co/RT.html).

These DAGs encode the metrical and rhythmic structure of a score, in the sense that, 
roughly speaking, every branching corresponds to the division of a musical time interval.
More specifically, the nodes of the DAG are labelled with basic events (notes, rests, etc.) for leaf nodes, 
and, for inner nodes, with functions that associate several sub-intervals (one per child) 
with a time interval. In this way, we can associate a time interval with each node of the DAG. 

The computation proceeds first bar-wise, aligning equal bars with a *Longest Common Subsequence*,   
and then *matching* the voices inside differing bars, with a dedicated algorithm. The next crucial step is the comparison of the content of two voices, performed by a *recursive parallel descent* into the two sub-DAG representations. The descent stops as soon as the labels diverge. In this case, a new difference is added to the list, the duration of the involved intervals is added to the time distance, and the surface distance is also updated with an edit distance between the sequence of attributes not related to time in the leaves under these nodes.

The original purpose of the TSM-diff approach to comparing musical scores is *version management* in the context of editing music notation, or the *creation and maintenance of corpora* for musicological studies, 
for example to identify duplicate or similar scores. It can also be applied to *comparative corpus studies* in musicology. The similarity distance computed could also be useful for the *evaluation* of  transcription or OMR procedures, for comparing the outcome with a reference XML score. 
