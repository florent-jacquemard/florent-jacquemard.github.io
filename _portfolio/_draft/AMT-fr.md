---
title: "Automated Music Transcription"
collection: portfolio
image: "/images/AMT.png"
description: "Conversion of a performance into music notation."
---



La transcription musicale est la conversion, vers une partition, d’une performance. Lorsque cette dernière est donnée sous forme discrète, séquentielle (une suite de notes avec hauteurs exactes mais dates et durées approximatives appelée *piano roll*); on parle de transcription MIDI-to-score. Ce cas est particulièrement intéressant dans le cadre de l’édition de partitions, la représentation piano roll correspondant au format  [MIDI](https://midi.org)  en sortie des claviers musicaux électroniques. Elle est aussi le format cible des outils de transcription musicale traitant des signaux audio (transcription dite audio-to-MIDI), avec lesquels les approches MIDI-to-score sont donc complémentaires, dans la perspective d’une transcription globale (audio-to-score).

Nous développons une [approche](publication/2019-06-01-A-Parse-based-Framework-for-Coupled-Rhythm-Quantization-and-Score-Structuring) fondée langages formels pour la transcription MIDI-to-score, reposant sur une représentation hiérarchique de la notation musicale similaire aux arbres de rythme (voir ces articles présentés à [MCM](2015-06-01-A-Structural-Theory-of-Rhythm-Notation-based-on-Tree-Representations-and-Term-Rewriting), [MEC](2015-05-01-Towards-an-Equational-Theory-of-Rhythm-Notation), [TENOR](2017-05-01-Generating-equivalent-rhythmic-notations-based-on-rhythm-tree-languages) or in the [IFIP WG 1.6 on term rewriting](publication/2014-07-01-Rhythm-Tree-Rewriting)), suivant le principe de définition proportionnelle des durées en musique (1 blanche = 2 noires, 1 noire = 2 croches etc). Un automate d’arbres pondéré décrit un modèle a priori de notation, associant à chaque arbre de rythme une valeur de complexité notationnelle, dans un semi-anneau commutatif. Cet automate peut être appris sur un corpus de partitions par des techniques d’inférence grammaticale ([SMC 2019](publication/2019-05-01-Modeling-and-Learning-Rhythm-Structure)). Étant donnée une performance séquentielle, non-structurée, en entrée, un algorithme dit de 1-best-parsing recherche un arbre de parsing minimisant à la fois sa valeur de complexité dans le langage a priori et l’écart par rapport à la performance du rythme correspondant. À partir de cet arbre de parsing est construite une représentation intermédiaire (IR) dans le modèle TSM qui nous développons. Après un certain nombre de post-traitements, en particulier par réécriture, la IR est convertie en une partition musicale dans un encodage XML.



## Development

Le développement en C++ de la procédure de transcription décrite succinctement ci-dessus (librairie [qparse](software/2017-qparse/)) a débuté à l’Inria Paris en 2017 et s'est poursuivi en collaboration avec les équipes de Philippe Rigaux au Cedric/CNAM et de Masahiko Sakai à l’Université de Nagoya ([bourse Yamaha](projects/2017-Yamaha/) et [projet JSPS](projects/2020-JSPS/) avec le JAIST). 

Une [approche antérieure](2016-09-01-A-Supervised-Approach-for-Rhythm-Transcription-Based-on-Tree-Series-Enumeration), préliminaire à qparse en terme d’efficacité et fonctionnalités, a été développée avec Adrien Ycart et Jean Bresson à l’Ircam en 2015-16 (bibliothèque LISP [RQ](software/2016-RQ/) pour OpenMusic). [RQ](software/2016-RQ/) est [orientée](2017-07-01-Interactive-Music-Transcription-based-on-Rhythm-Tree-Languages) vers l’aide à la composition, offrant une approche interactive où l’utilisateur se voit proposer des solutions de transcription énumérées de manière ordonnée, grâce à une interface graphique intégrée à OpenMusic.  Le développement de RQ a débuté durant le Master recherche d’Adrien Ycart en 2015 à l’Ircam, ce dernier ayant assuré l’essentiel du développement, en co-supervision avec Jean Bresson (développeur principal d’OpenMusic), et s’est poursuivit avec un projet interne ([UPI](projects/2016-RQ/)) de l’Ircam sur le sujet.



## Originality and difficulty

La transcription est l’un des défis les plus anciens et difficiles de l’informatique musicale, a l’origine de nombreux sujets de recherche en Music Information Retrieval (MIR). À ce jour, il n’a pas été trouvé de solution totalement satisfaisante.

La principale originalité de notre démarche MIDI-to-score est la production directe de partitions musicales structurées (dans des encodages XML). La plupart des autres approches (en particulier les approches signal prenant en entrée des fichiers audio) produisent en effet des séquences d’événements MIDI avec timestamps quantifiés (ou non-quantifiés dans le cas audio-to-MIDI), la structuration de la partition en sortie étant alors déléguée à un éditeur de partitions grand public (Musecore ou Finale), ce qui implique des corrections manuelles souvent importantes. 

Notre approche procède par *parsing* (conversion d'une séquence non structurée vers une structure d'arbre), traitant de manière couplée les deux étapes ci-dessus de quantification des durées et structuration de la notation, évitant des propagations d’erreurs, pour des résultats plus pertinents en particulier dans le cas de rythmes complexes. Un autre avantage du parsing est d’établir des relations globales, entre des événements arbitrairement distants, typiquement liées à la structure métrique. Cette vue long terme manque aux modèles statistiques séquentiels.

Cette approche s'appuie en particulier sur une [représentation intermédiaire](soft/2022-TSM) abstraite de la notation musicale sous forme arborescente, et la théorie des langages formels  (automates d’arbres pondérés) pour appréhender la structure profonde de la notation musicale.  Pour résumer grossièrement, [qparse](software/2017-qparse/)) transcrit par parsing de l’entrée séquentielle par rapport à un modèle de langage a priori hiérarchique,  décrivant un style de notation musicale préférée. 



## Validation

Des évaluations de qparse ont été réalisées sur une base de partitions constituée d’extraits monophoniques (une seule note à la fois) du répertoire classique3, de complexité rythmique variable. Elles ont démontré des temps de traitement rapides (de l’ordre de 100 ms pour une partition d’une page) et de bons résultats, en particulier dans le cas de rythmes complexes, d’appoggiatures (grace-notes) et de silences, des caractéristiques qui ont tendance à mettre en difficulté d’autres systèmes, notament commerciaux. 

Batterie...



## Dissemination

[RQ](software/2016-RQ/) a été évalué par des compositeurs, et enseigné en cursus de composition à l’Ircam et utilisé pour l’écriture de pièces, comme par exemple dans cette création d’Alessandro Ratoci pour le Festival de Ravenne 2016. 

[qparse](software/2017-qparse/) est actuellement un ensemble de prototypes en ligne de commande. Un projet à terme est son intégration, sous forme de plugin, dans un logiciel d’édition de partitions (Sibelius, Dorico ou le logiciel libre MuseScore...) ou bien un DAW.

