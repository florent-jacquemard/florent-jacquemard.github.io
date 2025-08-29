---
title: "Pitch Spelling Jazz Lead Sheets and Solo Transcriptions"
authors: 'Augustin Bouquillard, Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2025-11-03-Pitch-Spelling-Jazz-Lead-Sheets-and-Solo-Transcriptions
date: 2025-11-03
venue: 'Proceedings of the 17th International Symposium on Computer Music Multidisciplinary Research (CMMR)'
paperurl: 'https://works.hcommons.org/records/ts2pj-n8q68'
citation: 'Augustin Bouquillard and Florent Jacquemard &quot; Pitch Spelling Jazz Lead Sheets and Solo Transcriptions &quot; In Proceedings of the 17th International Symposium on Computer Music Multidisciplinary Research (CMMR), 2025.'
---
abstract: 
We present an algorithm for pitch spelling tailored for written jazz music.
Receiving some input in a MIDI-like format, including information about note heights 
(expressed in semitones from a reference lowest note) and boundaries of bars (measures), 
it estimates appropriate note names, 
one global key signature, 
and one local scale for each bar.

These related pieces of information are jointly assessed in two optimization steps. In a first "modal" step, one likely scale is guessed for each bar, by minimizing the number of accidentals that shall be printed in the engraved score, in a best-path search. Then, in a second "tonal" step, these local scales are used for estimating the key signature that would give the best note spelling on the whole piece.

We report successful experiments on a set of lead sheets from the Real Book 
as well as transcriptions of Jazz solo recordings and basslines.

Our procedure is originally designed for an application to music transcription, in particular the construction of digital collections of written jazz soli from audio recordings, in the context of musical analysis, teaching and cultural heritage preservation.
Moreover, we have defined for its purpose new distances between various common jazz scales which might be of some interest in musicological studies.