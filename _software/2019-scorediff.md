---
name: scorediff
begindate: 2019-01-01
enddate: 2019-12-31
sources: https://github.com/fosfrancesco/music-score-diff
permalink: /software/2019-scorediff
organization: CNAM and Inria
---

A tool to compute the differences between two music scores, given in XML encoding 
([MusicXML](https://www.musicxml.com) or [MEI](https://music-encoding.org)),  
and visualize these differences side-to-side.

Our initial goal was to implement for music scores a utility similar to the Unix diff command for text files. 
Its purpose is to identify differences between two score files which are relatively similar (typically two versions of the same file), 
corresponding to the intuitive notion of difference. 

The comparison is performed at the granularity level of bars (bars are here the analagous, for scores, of lines of text files), using a Longest Common Subsequence (LCS) algorithm, 
and, in a second step, at the granularity level of notes or chords (the analoguous of characters in text files). 

The visualization is performed using Verovio and works for polyphonic scores and for multiple instruments. 

Straightforward applications are version control systems and collaborative music score edition, as well as speeding-up tasks that require human supervision, such as the visual inspection of the outcome of optical music recognition (OMR) systems.

The first version of this tool, [score-diff](https://github.com/fosfrancesco/music-score-diff), was developed by Francesco Foscarin during his PhD.
In this version, the comparison between bars involves the computation of dedicated edit-distances between strings and trees, based on an abstract model of score content used for disambiguating the content for XML score formats and also decoupling our approach from the exact file format. 
As a proof of concept, this tool has been applied to check differences in a real OMR dataset.
This work was presented in this [paper](publication/2019-11-01-A-diff-procedure-for-music-score-files) and this [demo](publication/2019-11-01-Computation-and-Visualization-of-Differences-between-two-XML-Music-Score-Files).

A second version [musicdiff](https://github.com/gregchapman-dev/musicdiff) (native Python3), has been written by Greg Chapman. 
As opposed to the above version, it is based solely on a string edit-distance (Levenshtein distance).

A new version based on the [Tree Score Model](soft/2022-TSM), 
a tree-structured Intermediate Representation of the music notation content of a score, 
is in preparation.

