---
title: "Constrained Tree Automata"
collection: portfolio
image: "/images/TATA.png"
description: "Automata that can compute syntactic equalities and disequalities in trees."
---

Étude de classes d’automates calculant sur des arbres de rang borné, étiquetés par des symboles d’un alphabet fini, étendus par des contraintes et différentes applications de ces formalismes.



Une des premières extensions des automates d’arbres considérée [61, 70] consiste en l’ajout de contraintes locales qui testent, lors de chacune des transitions, des égalités (isomorphismes) et diségalités entre des sous arbres voisins (i.e. à distance bornée). Les modèles correspondants ont été introduits comme outils de décision dans le cadre de la démonstration automatique de théorèmes, pour leur lien avec des propriétés de non-linéarité de variables dans les systèmes de réécriture de termes. J’ai travaillé durant ma thèse et immédiatement après sur des problèmes de décision du vide (le langage d’arbres défini par un automate donné est-il vide) pour différentes classes d’automates d’arbres à contraintes locales [60, 59], avec pour aboutissement principal la résolution de la question de la complexité exacte du problème de la réductibilité inductive [57, 14]. Plus tard, nous avons infirmé [10] une conjecture ancienne sur la décision du vide pour une classe plus large de tels automates, nommés automates de réduction (voir [61]).

Nous avons étudié une extension de ces formalismes où les contraintes locales s’évaluent modulo des théories équationnelles [46, 10]. Représentant ces automates comme des ensembles de clauses de Horn, nous utilisons un calcul de paramodulation avec des stratégies appropriées (basique, ordonnée, avec sélection) pour établir la terminaison des algorithmes de décision. Auparavant [55], nous avions appliqué une approche similaire à des automates d’arbres avec des contraintes modulo des théories équationnelles plus restrictives, dites plates, en utilisant un autre calcul de superposition.

Une autre approche pour étendre les automates d’arbres est de leur ajouter des contraintes globales, qui sont testées en une seule fois, à la fin d’un calcul de l’automate sur un arbre, et consistent en une combinaison de tests d’égalité et diségalité entre des sous-arbres à des positions définies durant le calcul de l’automate. Une différence fondamentale avec les contraintes locales évoquées ci-dessus est que la distance entre les positions testées est arbitraire. La première classe d’automates d’arbres de ce type a été introduite sous le nom de [TAGED](https://hal.archives-ouvertes.fr/hal-00526987). Nous avons étudié une sous-classe des TAGED dite d’automates d’arbres rigides [39, 9] qui possède de bonnes propriétés de décision et d’expressivité. Nous avons de plus résolu le problème de la décidabilité du vide pour un modèle étendant strictement les TAGED [35, 7] avec en particulier des contraintes arithmétiques et des contraintes similaires aux contraintes de clés unaires dans les bases de données.

Enfin, nous avons proposé [44, 11] une classe d’automates d’arbres (dits visibles à mémoire) étendus par une mémoire auxiliaire contenant un arbre, dont l’expressivité se situe entre les automates d’arbres standard et les grammaires d’arbres hors-contexte. Contrairement à ces dernières, les automates d’arbres visibles à mémoire définissent une classe de langages close par intersection et complément, généralisant les automates de [nested words](https://doi.org/10.1145/1516512.1516518).



3. Originalité et difficulté / Originality and difficulty

Les deux problèmes théoriques de la complexité de la réductibilité inductive et de la décidabilité du vide pour la classe TAGED étaient considérés comme difficiles dans la communauté, sont restés ouverts pendant des années et ont fait l’objet de plusieurs thèses avant que nous les résolvions.



4. Validation et impact / Validation and impact

Les modèles de [60, 59, 55] d’une part et [46, 10], [39, 9] d’autre part, trouvent des applications respectivement en déduction automatique (cf [57, 14, 42, 8, 49, 38] et l’implantation de [55] dans le dans le système SPASS, section 3 du formulaire 5), et en vérification logique de protocoles de sécurité, (cf [9] et le paragraphe TACE, section 3 du formulaire 5).

Les automates de la classe TAGED ont été introduits par Emmanuel Filiot (efiliot@ulb.ac.be, +32 2 650 58 27), Jean-Marc Talbot et Sophie Tison (@univ-lille1.fr, +33 3 59 35 87 14) en lien avec la décision de la satisfiabilité pour la logique spatiale TQL dans laquelle on peut exprimer des requêtes sur documents XML. Leurs extensions de [35, 7] sont également bien adaptés à l’analyse de schémas XML: problèmes de satisfiabilité, d’inclusion ou d’équivalence de schémas.



## Diffusion / Dissemination

Outre les publications citées plus haut, dans des conférences [60, 59, 57, 46, 55, 39, 42, 49, 38, 35, 44] ou revues [14, 10, 9, 8, 11, 7] internationales, j’ai contribué au livre en ligne TATA [61], considéré comme une référence dans le domaine de la théorie des automates d’arbres et leurs applications et utilisé dans l’enseignement de cette discipline.
