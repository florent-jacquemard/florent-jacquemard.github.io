---
title: "Term Rewriting Systems"
collection: portfolio
domain: 'tata'
researchtype: theory
image: "/images/500x300.png"
description: "Decision problems in term rewriting, for automatic deduction and verification."
---

Pour un modèle de calcul Turing-complet comme la réécriture, il est naturel de se poser la question de la décidabilité (dans le cas général ou des cas particuliers) de certaines propriétés, comme l’accessibilité d’un terme donné à partir d’un autre par réécriture, la terminaison forte (toutes les suites de réécriture terminent) ou la confluence (deux suites de réécriture divergentes peuvent toujours converger vers un même terme).

La réductibilité inductive un des rares propriétés décidable pour tous les systèmes de réécriture. Cette propriété est centrale dans certaines approches pour la preuve automatique par récurrence, cf. fiche 5. Nous avons étudié avec Hubert Comon sa résolution par réduction à des problèmes de décision pour automates d’arbres avec contraintes locales [30] et établi sa complexité exacte (EXPTIME-complétude) dans [28, 9].

Par ailleurs, j’ai résolu par la négative les problèmes ouverts de la décidabilité de l’accessibilité et la confluence pour les systèmes de réécriture plats [8] par une réduction améliorée dans [22]. Nous avons montré avec Guillem Godoy [15], par des techniques d’automates d’arbres, que le problème de l’unicité des forme normales, qui exprime qu’un système de réécriture donné, vu comme une procédure de calcul, est fonctionnel, est décidable pour les systèmes plats et linéaire et indécidable pour les systèmes plats et linéaire à droite.

Le problème de l’_unification rigide_ a été introduit pour étendre les méthodes de preuves en logique du premier ordre avec égalité, telles que tableau et matings [GNRS92 GNRS92]. L’idée est que les variables des équations ne sont plus supposées quantifiées universellement comme dans les procédure d’unification classique en preuve et programmation logique, mais sont rigides, dans le sens où chaque variable ne peut être instanciée qu’une fois dans une preuve (elle est non réinscriptible, c’est à dire les différentes instanciations de variables dans une preuve doivent être cohérentes). Avec Harald Ganzinger, Margus Veanes et Véronique Cortier nous avons introduit le problème de l’accessibilité rigide qui généralise le précédent en orientant le sens d’application des équations (ce qui correspond en quelque sorte au passage d’un raisonnement équationnel à un calcul). Nous avons mené une étude approfondie de la frontière entre la décidabilité et l’indécidabilité des variantes simultanées ou non du problème [27, 25, 10], qui se révèle être plus difficile que l’unification rigide. Les cas de décidabilité ont été établis avec des techniques d’automates d’arbres.

De nombreux travaux traitent de la clôture de langages d’automates d’arbres standards par réécriture, une contribution de ma thèse étant [29]. Nous avons analysé avec Francis Klay et Camille Vacher [16, 4] la clôture des automates d’arbres rigides par réécriture, avec un algorithme de décision d’appartenance à cette clôture. Nous avons aussi étudié le problème du model checking régulier dans le cas de l’application de la réécriture avec des stratégies particulières. Avec Andrea Gascon et Guillem Godoy [33], nous montrons le résultat surprenant que l’application de la stratégie innermost, qui est l’analogue de l’appel par valeur dans les langages fonctionnels, donne de meilleurs résultats, vis à vis du model checking régulier, que la réécriture standard [8]: la clôture d’un langage d’automates d’arbres par un système de réécriture plat est un langage d’automates d’arbres avec des contraintes locales d’un type simple, ayant de bonnes propriétés. Nous avons aussi étudié avec Masahiko Sakai et Yoshiharu Kojima [11], à l’occasion d’un stage de ce dernier au LSV, le contrôle de la réécriture de termes par des conditions contextuelles exprimées par des automates d’arbres, c’est à dire la sélection des positions de réécriture à l’aide de calcul d’automates.



Le problème de la complexité exacte de la réductibilité inductive était considéré comme difficile dans les communauté de réécriture et déduction automatique et le résoudre a été un travail de longue haleine. Les résultats de [16, 4] sur la clôtures par réécriture sont à ma connaissance parmi les premier concernant des langages d’automates d’arbres à contraintes. Une raison dans le premier cas est l’incompatibilité entre les contraintes des automates qui testent des égalité syntaxiques, et la clôture modulo des règles de réécriture. Nous pensons qu’une bonne solution pour lever ce problème est l’utilisation de contraintes modulo des théories équationnelles, comme dans le formalisme clausal de [21, 5], présenter dans la précédente fiche. La clôture par application de la réécriture avec des stratégies particulières a de même été très peu étudiée avant les travaux mentionnés ci-dessus.



Les problèmes de l’accessibilité et de la confluence étaient conjecturés décidables pour les systèmes de réécriture plats avant [8]. La fermeture du problème (par la négative) a permis, de l’avis de collègues de la communauté, de débloquer des travaux et d’aller de l’avant vers d’autres problèmes.

L’étude de la réécriture contrôlée dans [11] a été motivée par les problèmes d’analyse d’updates et politiques de contrôle d’accès XML présentés dans la fiche 4, dans la mesure où en pratique, les positions d’application d’updates sont généralement sélectionnées par des expressions XPath [RCD+11]. C’est un sujet intéressant du point de vue des applications sur lequel il reste de nombreux problème à résoudre.





- [ ] [33]
  Closure of tree automata languages under innermost rewriting. 
  Adrià Gascón, Guillem Godoy, and Florent Jacquemard. 
  Proceedings of the 8th International Workshop on Reduction Strategies in Rewriting and Programming (WRS’08), volume 237 of Electronic Notes in Theoretical Computer Science,
  pages 23–38, Elsevier Science Publishers, 2008.