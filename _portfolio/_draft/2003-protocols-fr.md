---
title: "Spécification et vérification de protocoles cryptographiques"
collection: portfolio
domain: 'tata'
researchtype: application
image: "/images/500x300.png"
description: "Short description of portfolio item number 1"
---

Spécification et vérification de protocoles cryptographiques



Les protocoles cryptographiques décrivent les messages échangés par des agents dans un environnement hostile et composés à l’aide de primitives cryptographiques. Ils sont généralement décrits dans la littérature scientifique à l’aide d’une notation semi-formelle, dite langage Alice-Bob, où sont spécifiées le contenu des messages entre les acteurs du protocole (agents). On peut voir cette syntaxe comme une représentation textuelles de Message Sequence Charts utilisés entre autres dans les RFCs. Ce langage est simple et concis pour décrire le déroulement global d’un protocole mais néanmoins ambigu et occulte les opérations locales de chacun des agents.

Nous avons implanté une procédure de compilation de spécifications Alice-Bob en règles de réécriture multi-ensemblistes décrivant précisément les opérations des agents pour l’analyse des messages reçus et la construction des messages envoyés et les facultés des attaquants. La traduction de ce langage intermédiaire en format d’entrée (clauses de Horn) pour le démonstrateur daTac, puis d’autres outils par la suite, permet une vérification formelle des protocoles à l’aide de procédures de narrowing. L’ensemble, présenté à  [LPAR'00](https://inria.hal.science/inria-00099161v1) [24] forme le système [CASRUL](https://florent-jacquemard.github.io/software/1999-CASRUL/), dont la première version a été écrite à cette époque, et qui a ensuite été un composant du projet Européen [AVISS](https://memsic.ccsd.cnrs.fr/UNIV-BM-THESE/inria-00100915v1) et de son successeur [AVISPA](https://avispa-project.org).

Plus tard, j’ai travaillé avec Stéphanie Delaune sur des problèmes similaires  ([CSF'04](https://doi.ieeecomputersociety.org/10.1109/CSFW.2004.1310728), [UNIF'04](https://people.irisa.fr/Stephanie.Delaune/PUBLICATIONS-HTML/b2hd-dj-unif2004.html), [CCS'04](https://doi.org/10.1145/1030083.1030121), [JAT'06](https://doi.org/10.1007/s10817-005-9017-7)), améliorant en particulier l’approche de CASRUL (narrowing) par l’ajout de symboles destructeurs explicites définis par des théories équationnelles et l’application de la stratégie basique pour le narrowing (dans le sens où ce dernier modèle permet de détecter plus d’attaques).

Ce dernier modèle a aussi motivé des études de modèles d’[automates d’arbres à contraintes](portfolio/1996-CTATA/) [21 , 5,  16, 4], et dans un registre bien différent des [calculs de membranes](https://doi.org/10.1007/3-540-29937-8_10). L’idée est intuitivement que les automates permettent de caractériser l’ensemble (infini) des messages pouvant être échangés par un protocole. Le modèle d'automates de ([IJCAR'06](https://doi.org/10.1007/11814771_45), [JAL'08](publication/2008-01-01-Tree-automata-with-equality-constraints-modulo-equational-theories) améliore celui de [CCS'04](https://doi.org/10.1145/1030083.1030121) [23] et la procédure de décision de la satisfiabilité pour ces modèles d’automates est une généralisation du narrowing basique des équations aux clauses de Horn.



## Personal contribution

J’ai conduit le premier développement de CASRUL avec Michael Rusinowtich et Laurent Vigneron au sein de
l’équipe Protheo à Nancy. Lors de la suite des événements (création de l’EPI Cassis, projets Européens AVISS puis AVISPA, développement dans ce cadre) je n’était malheureusement plus à Nancy... Les travaux avec Stéphanie Delaune ont été conduits dans le cadre du démarrage de sa thèse au sein de l’EPI Secsi et du projet RNTL Prouvé.

[16, 4] sont des travaux de thèse de Camille Vacher, dans le cadre d’un contrat Cifre avec France Télécom.



## Originality and difficulty
À notre connaissance, l’activité autour de CASRUL est la première sur la modélisation et la vérification symbolique de protocoles cryptographique à l’Inria, un thème qui est devenu très actif par la suite, avec en particulier les EPI Cassis et Secsi. Ce travail a marqué le début d’une évolution vers des outils formels permettant une analyse automatiques de protocoles réels, apportant par rapport aux approche existantes plus d’automaticité et des abstraction nettement moins fortes, parmettant le passage de modèles à nombre fini d’états (comme Casper, de G. Lowe, basé sur le model checker FDR) à un nombre infini d’états.

CASRUL a été l’un des premier compilateur de protocoles en notation Alice-Bob. Cette approche est encore
utilisée actuellement, en raison de la popularité de ce format. L’article [24] a été abondamment cité, y compris récemment dans le cadre de travaux de Giuseppe Castagna sur les session types.



##  Validation and impact
De l’avis de Michael Rusinowitch, le développement de CASRUL peut être considéré comme le point de départ de la création de l’EPI Cassis au centre Nancy et du projet Européen AVISS (à la soumission duquel j’ai participé) et de son successeur AVISPA.



## Dissemination
La page de CASRUL est accessible à http://www.loria.fr/equipes/cassis/softwares/casrul/ http://www.loria.fr/equipes/cassis/softwares/casrul/ et contient des lien sur les projet Européens mentionnés.





- [ ] [2] https://hal.science/hal-00340140
  https://doi.org/10.1007/3-540-29937-8_10

  Olivier Michel and Florent Jacquemard 
  An analysis of a public key protocol with membranes 
  In Applications of Membrane Computing, Natural Computing Series, pages 283–302. Springer, 2006.

- [ ] [4] https://florent-jacquemard.github.io/publication/2011-02-01-Rigid-Tree-Automata-and-Applications
  Florent Jacquemard, Francis Klay, and Camille Vacher 
  Rigid tree automata and applications 
  Inf. Comput., 209(3):486–512, 2011.

- [ ] [5] https://florent-jacquemard.github.io/publication/2008-01-01-Tree-automata-with-equality-constraints-modulo-equational-theories
  Florent Jacquemard, Michaël Rusinowitch, and Laurent Vigneron 
  Tree automata with equality constraints modulo equational theories 
  Journal of Logic and Algebraic Programming, 75(2):182–208, April 2008.

- [ ] [7] https://inria.hal.science/inria-00578855
  https://doi.org/10.1007/s10817-005-9017-7

  Stéphanie Delaune and Florent Jacquemard 
  Decision Procedures for the Security of Protocols with Probabilistic Encryption against Offline Dictionary Attacks 
  Journal of Automated Reasoning, 36(1-2):85-124, 2006.

- [ ] [16] https://florent-jacquemard.github.io/publication/2009-04-01-Rigid-Tree-Automata

  Florent Jacquemard, Francis Klay, and Camille Vacher 
  Rigid tree automata 
  In Proceedings of the 3rd International Conference on Language and Automata Theory and Applications (LATA’09), volume 5457 of Lecture Notes in Computer Science, pages 446–457, Tarragona, Spain, April 2009. Springer.

- [ ] [21] https://hal.science/inria-00579011

  https://doi.org/10.1007/11814771_45
  Florent Jacquemard, Michaël Rusinowitch, and Laurent Vigneron 
  Tree automata with equality constraints modulo equational theories 
  In Proceedings of the 3rd International Joint Conference on Automated Reasoning (IJCAR’06), volume 4130 of Lecture Notes in Artificial Intelligence, pages 557–571, August 2006. Springer-Verlag.

- [ ] [23] https://inria.hal.science/inria-00579012

  https://doi.org/10.1145/1030083.1030121
  Stéphanie Delaune and Florent Jacquemard
  A decision procedure for the verification of security protocols with explicit destructors 
  In Proceedings of the 11th ACM Conference on Computer and Communications Security (CCS’04), pages 278–287, October 2004. ACM Press.

- [ ] [24] https://inria.hal.science/inria-00099161v1
  Florent Jacquemard, Michaël Rusinowitch, and Laurent Vigneron 
  Compiling and verifying security protocols
  In Proceedings of the 7th international conference on Logic for programming and automated reasoning (LPAR), LPAR’00, pages 131–160, Berlin, Heidelberg, 2000. Springer-Verlag.

- [ ] [37] https://people.irisa.fr/Stephanie.Delaune/PUBLICATIONS-HTML/b2hd-dj-unif2004.html

  Stéphanie Delaune and Florent Jacquemard 
  Narrowing-based constraint solving for the verification of security protocols 
  In Proceedings of the 18th International Workshop on Unification (UNIF’04), Cork, Ireland, July 2004.

- [ ] [38] https://inria.hal.science/inria-00579014v1
  https://doi.ieeecomputersociety.org/10.1109/CSFW.2004.1310728

  Stéphanie Delaune and Florent Jacquemard
  A theory of dictionary attacks and its complexity 
  In Proceedings of the 17th IEEE Computer Security Foundations Workshop (CSFW’04), pages 2–15, June 2004. IEEE Computer Society Press.

