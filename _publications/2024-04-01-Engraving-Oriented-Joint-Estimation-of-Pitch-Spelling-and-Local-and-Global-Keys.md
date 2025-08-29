---
title: "Engraving Oriented Joint Estimation of Pitch Spelling and Local and Global Keys"
authors: 'Augustin Bouquillard, Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2024-04-01-Engraving-Oriented-Joint-Estimation-of-Pitch-Spelling-and-Local-and-Global-Keys
date: 2024-04-01
venue: 'Proceedings of International Conference on Technologies for Music Notation and Representation (TENOR)'
hal: 'https://inria.hal.science/hal-04458185v1'
bibtex: ''
citation: 'Augustin Bouquillard, Florent Jacquemard, &quot;Engraving Oriented Joint Estimation of Pitch Spelling and Local and Global Keys&quot; In the proceedings of International Conference on Technologies for Music Notation and Representation (TENOR), 2024.'
---
abstract: 
We revisit the problems of pitch spelling and tonality guessing with a new algorithm for their joint estimation from a MIDI file including information about the measure boundaries. Our algorithm does not only identify a global key but also local ones all along the analyzed piece. It uses Dynamic Programming techniques to search for an optimal spelling in term, roughly, of the number of accidental symbols that would be displayed in the engraved score. The evaluation of this number is coupled with an estimation of the global key and some local keys, one for each measure. Each of the three informations is used for the estimation of the other, in a multi-steps procedure. An evaluation conducted on a monophonic and a piano dataset, comprising 216 464 notes in total, shows a high degree of accuracy, both for pitch spelling (99.5% on average on the Bach corpus and 98.2% on the whole dataset) and global key signature estimation (93.0% on average, 95.58% on the piano dataset). Designed originally as a backend tool in a music transcription framework, this method should also be useful in other tasks related to music notation processing.