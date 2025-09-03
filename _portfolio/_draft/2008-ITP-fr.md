---
title: "Automation of Inductive Theorem Proving"
collection: portfolio
image: "/images/500x300.png"
description: "Short description of portfolio item number 1"
---



Le but de la preuve automatique par récurrence est d’établir la validité de conjectures dans des structures particulières comme les entiers naturels, les listes, arbres binaires (on parle de modèle initial). 



Certaines approches, dans le cas de théories équationnelles fonctionnent en essayant de dériver un défaut de cohérence d’un ensemble d’équations et une conjecture, utilisant des techniques de déduction automatique générales (dont le but est d’établir la validité de conjectures dans toutes les structures satisfaisant une théorie). Ces approches automatiques n’utilisent pas de schémas de récurrence explicite, aussi parle-t-on parfois de preuve récurrence sans récurrence (inductionless induction, voir [CL01] pour un survol de ces techniques). La réductibilité inductive [28, 9] est un critère de défaut de cohérence.

Une autre famille de méthode pour l’automatisation de la récurrence utilise pour les preuves des schémas de récurrence qui sont calculés automatiquement. C’est le cas du système RRL de Deepak Kapur ou Spike d’Adel Bouhoula et Michael Rusinowitch. Généralisant une idée de [BJ01 BJ01], nous avons proposé avec Adel Bouhoula [19 19] un cadre très général où les schémas de récurrences sont des automates d’arbres avec contraintes locales. Ils sont utilisés dans les preuves comme grammaires, c’est à dire en générateur d’arbres par remplacement de non-terminaux, intuitivement pour passer du cas n au cas n + 1 dans une étape de récurrence. Ces automates, calculés automatiquement, reconnaissent des langages de termes en forme normale (termes ne pouvant plus être réduits par le système de réécriture), qui caractérisent, dans le cadre choisi, le modèle initial. Ils sont utilisés de plus dans les preuves comme outil de décision pour des propriétés similaires aux défauts de cohérence.

Nous avons également proposé avec Adel Bouhoula une adaptation de la procédure ci-dessus qui peut être utilisée dans le cadre de la vérification de protocoles cryptographiques à la fois pour établir des preuves (par récurrence) de correction de protocoles ou pour dériver des attaques [34 34].

Nous avons proposé par ailleurs [36 36] et [3 3] une procédure de vérification de la complétude suffisante de spécifications équationnelles, intégrée dans notre cadre pour la preuve par récurrence.



Les procédures ci-dessus s’appliques à des spécifications écrites dans un langage très expressif, des systèmes de réécriture avec conditions et contraintes. La clé pour cette généralité est l’utilisation des automates d’arbres à contraintes. La contrepartie est que ces procédures reposent sur des problèmes de décision pour ces modèles d’automates qui ne sont pas facile à établir et encore plus diciles à implanter.



Des prototypes ont été réalisé lors des stages d’Hédi Benzina et Saoussen Ben Nasr à Cachan. L’implantation d’un véritable theorem prover par récurrence est une tâche beaucoup plus couteuse qui demanderai un investissement important sur ces sujets pendant une longue période. Sorin Stratulat, de l’université de Metz et membre associé de l’EPI Pareo à Nancy à pour projet d’implanter notre procédure dans le cadre d’une thèse en co-tutelle.



J’ai implanté en 1997 la construction d’automates d’arbres avec contraintes reconnaissant les termes formes normale dans le cadre de la construction d’un système de preuve par récurrence basé sur le langage de logique de réécriture Maude, au SRI International à Stanford, dans l’équipe de José Meseguer.