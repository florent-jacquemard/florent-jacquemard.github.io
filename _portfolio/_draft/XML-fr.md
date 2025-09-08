---
title: "Verification of XML data processing systems"
collection: portfolio
domain: 'tata'
researchtype: application
image: "/images/hedges.png"
description: "Hedge Automata and Rewriting, Data Trees, Regular Model Checking, Type Verification"
---

We studied problems related to the verification of XML transformations and navigation languages, based on tree automata formalisms.



## Regular Model Checking and Type Verification

Le **model checking régulier** est une méthode pour la vérification formelle de systèmes, par exploration systématique d’un espace (très grand) de configurations atteignables, grâce à l’usage de représentations symboliques: chaque configuration est représentée par un mot ou un arbre, et l'ensemble des configurations atteignables par un automate. Ce dernier peut, dans certains cas, être obtenus par calcul de la clôture (ou clôture inverse, ou des sur-approximations) d’un langage initial (ou cible) par application de règles de réécriture représentant les transitions du système.

Afin d'appliquer cette méthode à la vérification formelle de transformations XML, nous étudions [[RTA'08](publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting)] des variantes d’[automates de haies](https://inria.hal.science/hal-03367725), calculant sur des arbres de rang non borné étiquetés dans un alphabet fini (modélisant des documents XML), et la transformation de leurs langages par des systèmes de réécriture correspondants, en particulier des systèmes dits hors-contexte (cf. [LATA'13](publication/2013-04-01-Rewrite-Closure-and-CF-Hedge-Automata))  (leurs règles ayant la forme de productions de grammaires d’arbres hors-contexte) et leurs symétriques. 

De plus, nous étendons ([PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates)) ces règles de réécriture d’arbres de rang non borné par des contraintes de types, afin de modéliser des opérations atomiques de mise à jour de documents XML (renommage, insertion, effacement, remplacement) telles que spécifiées dans le standard W3C [XQuery Update Facility](https://www.w3.org/TR/xquery-update-30/)  (XQUF). Nous avons établi des résultats de **vérification de type** ([PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates) et [JCSS'16](publication/2016-01-01-One-variable-context-free-hedge-automata)) pour des itérations arbitraires de ces opérations (clôture et clôture inverse par réécriture), par un algorithme de construction itératif d’automates de haies et automates de haies hors-contexte. 

Nous étudions par ailleurs [[FroCoS'11](publication/2011-10-01-Controlled-Term-Rewriting), [CADE'15](publication/2015-08-01-Term-Rewriting-with-Prefix-Context-Constraints-and-Bottom-Up-Strategies)] une extension des systèmes de réécriture de termes par des contraintes sur les positions d’application des règles, comme modèles de transformations XML. 

Il existe de nombreux résultats en vérification de type pour des transformations XML, traitant généralement d’une seule application d’une transformation écrite dans un langage comme XSLT ou d’une passe top-down de transducteur d’arbres. L’originalité, et une source de difficulté, des approches de [[RTA'08](publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting), [PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates)] est que nous considérons des itérations en nombre arbitraire de règles atomiques d’updates, à des positions arbitraires dans les arbres. 

Les techniques de vérification de type ci-dessus se sont aussi révélées pertinentes pour la vérification de la **cohérence de politiques contrôle d’accès** définies par des ensemble de règles. Ce problème est indécidable en général. Nous avons identifié un cas décidable (cohérence locale), qui plus est en temps polynomial.

Ces travaux théoriques ont fait l'objet d'applications dans des projets bilatéraux avec les universités Tunisiennes ([ISCC'09](publication/2009-07-01-Automatic-Verification-of-Conformance-of-Firewall-Configurations-to-Security-Policies), [ComNet'10](publication/2010-11-01-XML-Access-Control-from-XACML-to-Annotated-Schemas)) et le projet [ARC Inria Access](projects/#ACCESS). 

La réécriture d’arbres de rang non borné est un formalisme original, pertinent pour la modélisation et la vérification de transformations de documents XML, qui mériterait des études plus approfondies, suivant les développement de la théorie des systèmes de réécriture appliqués à des arbres de rang borné.





## Data trees

Les arbres de données sont une représentation plus fine des documents XML, avec un étiquetage à la fois par des symboles dans un alphabet fini (représentant des marqueurs ou balises XML) et des données dans un domaine infini (représentant des valeurs d’attributs ou des contenus textuels). 

Nous avons proposé ([LMCS'16](publication/2016-01-01-FO21-on-data-trees-data-tree-automata-and-branching-vector-addition-systems)) un modèle d’automates calculant sur de tels arbres, et prouvé une correspondance 1-1 avec un fragment significatif du standard de navigation XPath: le fragment FO2(<, +1, ∼) des formules à 2 variables de la logique du premier ordre sur les arbres de données – les prédicats < et +1 sont pour la navigation dans les arbres alors que ∼ sert à comparer les données. La correspondance est établie via un modèle d’automates à compteurs étendant les BVASS (Branching Vector Addition Systems with States), un formalisme pour la vérification de programmes concurrents.

Ces résultats s’appuient sur des travaux antérieurs de Luc Segoufin et al sur le modèle des mots de données (au lieu des arbres), ces travaux étant considérés comme des références dans la théorie des donnés Web. Il faut noter que l'article ci-dessus établit un résultat d’inter-réduction de problèmes de décision, la décision restant un problème ouvert qui généralise le problème de la décidabilité dans les BVASS, ce dernier étant considéré comme très difficile.







## source D 2012



Nous avons étudié dans le cadre du model checking régulier la réécriture d’arbres de rang non borné et avons montré avec Michael Rusinowitch [18] que des systèmes de réécriture dits hors-contexte (car leur règles ont la forme de production de grammaires d’arbres hors-contexte) transforment des langages d’automates d’arbres de rang non borné (appelés automates de haies [Mur99]) en une extension appelée automates de haies hors-contexte, et que le symétrique de ces systèmes de réécriture préserve les languages d’automates de haies.
De plus, nous avons proposé plus tard toujours avec Michael Rusinowitch [13] une extension des règles de réécriture d’arbres de rang non borné par des paramètres qui sont, intuitivement, des types représentant des ensembles infinis d’arbres (en fait des langages d’automates). Les règles de réécriture ainsi définies permettent de modéliser des opérations atomiques d’update de documents XML (renommage, insertion, effacement, remplacement) tels que spécifiés dans le standard W3C [XQuery Update Facility](https://www.w3.org/TR/xquery-update-30/) (XQUF). 
Nous avons établi des résultats d’inférence de type [13] pour des itérations arbitraires de ces opérations (clôture et clôture inverse par réécriture), par algorithme de construction itératifs d’automates de haies et automates de haies hors-contexte. Ces techniques nous permettent de vérifier des propriétés de cohérence de politiques de contrôle d’accès (en écriture) pour mises-à-jour de documents XML.
La vérification de politiques de sécurité a par ailleurs fait l’objet de plusieurs stages dans le cadre de projets
bilatéraux avec la Tunisie et d’une ARC Inria Access [17, 14].



Il existe de nombreux résultats sur la vérification de type pour des transformations XML. Ils traitent généralement d’une seule application d’une transformation écrite dans un langage comme XSLT ou d’une passe top-down de transducteur d’arbres. L’originalité de notre travail dans ce cadre (et une source de difficulté) est que nous considérons des applications itérées un nombre arbitraire de fois de règles atomiques d’updates (d’expressivité limitée individuellement), à des positions arbitraires dans les arbres.

Les résultats sur les primitives d’update XQUF [13] se sont révélés beaucoup plus difficiles à établir que ceux de notre travail théorique précédent sur la clôture par réécriture [18], bien que les règles de réécriture du modèle de [13] soient de forme beaucoup plus simple que les règles plus générales de [18]. La raison est, sans entrer dans les détails, que le traitement individuel des différents type de règles d’update n’est pas difficile, mais la combinaison des différents type d’opération devient très complexe. Il s’agit là selon moi d’un bon exemple de problème appliqué qui s’avère en réalité plus difficile à traiter qu’un problème théorique en apparence plus général!



L’approche de l’inférence de type dans ce cadre nous semble surtout pertinente pour la vérification de la cohérence de politiques contrôle d’accès définis par des ensemble de règles. Ce problème est indécidable en général, nous avons identifié un cas décidable (cohérence locale) qui plus est en temps polynomial.

La réécriture d’arbres de rang non bornés est sujet encore peu développé, comparativement à la réécriture de termes, et qui mériterait d’être plus étudié, considérant l’importance actuelle de la modélisation et du raisonnement sur les transformation de données XML (qui sont des arbres de rang non borné).



- [x] [13] https://inria.hal.science/inria-00578916/
  https://arxiv.org/abs/0907.5125
  https://doi.org/10.1145/1836089.1836105 
  Florent Jacquemard and Michaël Rusinowitch 
  Rewrite-based verification of XML updates 
  In Proceedings of the 12th ACM SIGPLAN International Symposium on Principles and Practice of Declarative Programming (PPDP), PPDP ’10, pages 119–130, New York, NY, USA, 2010. ACM.
  
- [x] [14] https://inria.hal.science/inria-00578884
  
  https://doi.org/10.1109/COMNET.2010.5699810
  
  Ryma Abbassi, Florent Jacquemard, Michael Rusinowitch, and Sihem Guemara El Fatmi 
  XML Access Control: from XACML to Annotated Schemas 
  Intl. Conf. on Communications and Networking (ComNet), pages 1-8, 2010.
  
- [x] [17] https://inria.hal.science/inria-00578926
  
  https://doi.org/10.1109/ISCC.2009.5202309
  
  Nihel Ben Youssef, Adel Bouhoula, and Florent Jacquemard 
  Automatic verification of conformance of firewall configurations to security policies 
  In Proceedings of the 14th IEEE Symposium on Computers and Communications (ISCC), pages 526–531. IEEE, 2009.
  
- [x] [18] https://inria.hal.science/inria-00329803
  
  https://florent-jacquemard.github.io/publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting
  
  Florent Jacquemard and Michaël Rusinowitch 
  Closure of Hedge-automata languages by Hedge rewriting
  In Proceedings of the 19th International Conference on Rewriting Techniques and Applications (RTA’08), volume 5117 of Lecture Notes in Computer Science, pages 157–171, July 2008. Springer.
  
- [x] [RCD+11] https://www.w3.org/TR/xquery-update-30/
  
  Jonathan Robie, Don Chamberlin, Michael Dyck, Daniela Florescu, Jim Melton, and Jérôme Siméon
  Xquery update facility 1.0
  Technical report, W3C, March 2011.





## final





## source: HC2021

 

Afin d’appliquer des procédures de model checking régulier (cf page 12) à la vérification formelle de transformations XML, nous étudions [41] des variantes d’automates de haies [61], calculant sur des arbres de rang non borné étiquetés dans un alphabet fini (modélisant des documents XML), et la transformation de leurs langages par des systèmes de réécriture correspondants, en particulier des systèmes dits hors-contexte [31] (leurs règles ayant la forme de productions de grammaires d’arbres hors-contexte) et leurs symétriques. De plus, nous étendons [36] ces règles de réécriture d’arbres de rang non borné par des contraintes de types, afin de modéliser des opérations atomiques de mise à jour de documents XML (renommage, insertion, effacement, remplacement) telles que spécifiées dans le standard W3C XQuery Update Facility (XQUF). Nous avons établi des résultats de vérification de type [36, 5] pour des itérations arbitraires de ces opérations (clôture et clôture inverse par réécriture), par un algorithme de construction itératif d’automates de haies et automates de haies hors-contexte. Ces techniques nous permettent de vérifier des propriétés de cohérence de politiques de contrôle d’accès (en écriture) pour mises-à jour de documents XML. La vérification de politiques de sécurité a par ailleurs fait l’objet de stages dans le cadre de projets bilatéraux avec la Tunisie [40, 37] et de l’ARC Inria Access cf page 7. 

Les arbres de données sont une représentation plus fine des documents XML, avec un étiquetage à la fois par des symboles dans un alphabet fini (représentant des marqueurs ou balises XML) et des données dans un domaine infini (représentant des valeurs d’attributs ou des contenus textuels). Nous avons proposé [4] un modèle d’automates calculant sur de tels arbres, et prouvé une correspondance 1-1 avec un fragment significatif du standard de navigation XPath: le fragment FO2(<, +1, ∼) des formules à 2 variables de la logique du premier ordre sur les arbres de données – les prédicats < et +1 sont pour la navigation dans les arbres alors que∼ sert à comparer les données. La correspondance est établie via un modèle d’automates à compteurs étendant les BVASS (Branching Vector Addition Systems with States), un formalisme pour la vérification de programmes concurrents.



Il existe de nombreux résultats en vérification de type pour des transformations XML, traitant généralement d’une seule application d’une transformation écrite dans un langage comme XSLT ou d’une passe top-down de transducteur d’arbres.

L’originalité et une source de difficulté de [41, 36] dans ce cadre est que nous considérons des itérations en nombre arbitraire de règles atomiques d’updates, à des positions arbitraires dans les arbres. Nous étudions par ailleurs [34, 24] une extention des systèmes de réécriture de termes par des contraintes sur les positions d’application des règles, comme modèles de transformations XML. Les résultats sur les primitives de XQUF [36] ont étés beaucoup plus difficiles à établir que ceux de notre travail théorique précédent sur la clôture par réécriture [41], bien que les règles du modèle de [36] soient en apparence plus simples que celles de [41]. En effet, si le traitement individuel de chaque type de règles d’update n’est pas difficile, la combinaison des différents types d’opérations devient très complexe, rendant le problème appliqué de [36] plus difficile à traiter que le problème théorique apparemment plus général de [41].

Les résultats de [4] s’appuient sur des travaux antérieurs de Luc Segoufin et al sur le modèle des mots de données (au lieu des arbres), ces travaux étant considérés comme des références dans la théorie des donnés Web. Il faut noter que [4] établit un résultat d’inter-réduction de problèmes de décision, la décision restant un problème ouvert qui généralise le problème de la décidabilité dans les BVASS, ce dernier étant considéré comme très difficile.



Les techniques de vérification de type se revèlent pertinentes pour la vérification de la cohérence de politiques contrôle d’accès définies par des ensemble de règles. Ce problème est indécidable en général. Nous avons identifié un cas décidable (cohérence locale), qui plus est en temps polynomial.
La réécriture d’arbres de rang non borné est un formalisme original, pertinent pour la modélisation et la vérification de transformations de documents XML, qui mériterait des études plus approfondies, suivant les développement de la théorie des systèmes de réécriture appliqués à des arbres de rang borné.



- Articles dans les conférences d’informatique théorique

- [x] [41] https://florent-jacquemard.github.io/publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting
  Closure of Hedge-Automata Languages by Hedge Rewriting, RTA'08
  
- [x] [31] https://florent-jacquemard.github.io/publication/2013-04-01-Rewrite-Closure-and-CF-Hedge-Automata

- [x] [34] https://florent-jacquemard.github.io/publication/2011-10-01-Controlled-Term-Rewriting
  Controlled Term Rewriting, FroCoS'11

- [x] [36] https://florent-jacquemard.github.io/publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates
  Rewrite-Based Verification of XML Updates, PPDP'10

- [x] [37] https://florent-jacquemard.github.io/publication/2010-11-01-XML-Access-Control-from-XACML-to-Annotated-Schemas

  ComNet'10

- [x] [40] https://florent-jacquemard.github.io/publication/2009-07-01-Automatic-Verification-of-Conformance-of-Firewall-Configurations-to-Security-Policies

  ISCC'09

- [x] [24] https://florent-jacquemard.github.io/publication/2015-08-01-Term-Rewriting-with-Prefix-Context-Constraints-and-Bottom-Up-Strategies
  Florent Jacquemard, Yoshiharu Kojima, Masahiko Sakai. 
  Term Rewriting with Prefix Context Constraints and Bottom-Up Strategies. 
  In 25th International Conference on Automated Deduction (CADE’15), Berlin, Germany, LNCS, Springer, 2015.
  
- [x] [61] https://inria.hal.science/hal-03367725
  Hubert Comon, Max Dauchet, Rémi Gilleron, Florent Jacquemard, Christoph Löding, Denis Lugiez, Sophie Tison, and Marc Tommasi
  Tree Automata Techniques and Applications. http://tata.gforge.inria.fr, 2007.



- articles revues d’informatique théorique
  
- [x] [4] 
  https://florent-jacquemard.github.io/publication/2016-01-01-FO21-on-data-trees-data-tree-automata-and-branching-vector-addition-systems
- [x] [5] 
  https://florent-jacquemard.github.io/publication/2016-01-01-One-variable-context-free-hedge-automata

