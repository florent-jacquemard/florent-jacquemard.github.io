---
title: "Music Score Comparison based on a Tree-structured Intermediate Representation"
authors: 'Florent Jacquemard, Xiaobo Wang'
collection: publications
category: conferences
permalink: /publication/2025-09-21-Music-Score-Comparison-based-TSM
date: 2026-09-21
venue: 'Fourth International Conference on Computational and Cognitive Musicology (ICCCM)'
hal: 'https://inria.hal.science/view/index/docid/5659654'
citation: 'Florent Jacquemard and Xiaobo Wang &quot; PMusic Score Comparison based on a Tree-structured Intermediate Representation &quot; Fourth International Conference on Computational and Cognitive Musicology (ICCCM), 2026.'
---

abstract: 
We propose an algorithm for the comparison of digital music scores based on an intermediate representation, structured as labeled directed acyclic graphs (DAG). Inspired by the former formalism of rhythm trees, these DAGs encode the metric and rhythmic structure of a score using a hierarchical representation of the information related to time. Given two score files in encodings such as MEI or MusicXML, after conversion into DAGs, our procedure calculates jointly: (i) a list of differences, localised by time positions in the input scores (ii) a time distance - cumulated duration of time intervals where scores differ (iii) an edit distance based on attributes of notational elements not related to time, called surface distance. The comparison is performed first bar-wise, by aligning equal bars, then by a recursive descent in sub-DAGs representing different bars, stopping as soon as the labels differ. The advantages of this approach are efficiency (linear time complexity of the recursive descent) and accuracy: we can associate ad-hoc difference codes to each pair of labels of DAG nodes (the exact list of codes can be adapted to use-cases), providing more explicit feedback than the basic ins/del/replace operations used for edit-distances. This approach can be applied e.g. to comparative corpus studies in musicology, or to versioning in the context of score edition, or for the preparation of corpora. As a proof of concept, we propose two demos based on different versions of a corpus of piano sonata, and transcriptions of monophonic soli on the same jazz standard by different performers.
