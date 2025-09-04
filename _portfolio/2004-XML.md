---
title: "Verification of XML data processing systems"
collection: portfolio
domain: 'tata'
researchtype: application
image: "/images/hedges.png"
description: "Regular Model Checking with Hedge Automata and Rewriting"
---

We studied problems related to the verification of XML transformations and navigation languages, based on tree automata formalisms.



## Regular Model Checking and Type Verification

Regular model checking is a method for formally verifying systems by systematically exploring a (very large) space of reachable configurations using symbolic representations: each configuration is represented by a word or a tree, and the set of reachable configurations by an automaton. In some cases, the latter can be obtained by calculating the closure (or inverse closure, or over-approximations) of an initial (or target) language by applying rewriting rules representing the transitions of the system.

In order to apply this method to the formal verification of XML transformations, we study [[RTA'08](publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting)] variants of [hedge automata](https://inria.hal.science/hal -03367725), computing on unbounded-rank trees labeled in a finite alphabet (modelling XML documents), and the transformation of their languages by corresponding rewriting systems, in particular so-called context-free systems (see [LATA'13](publication/2013-04-01 -Rewrite-Closure-and-CF-Hedge-Automata)) (their rules taking the form of productions of context-free tree grammars) and their symmetrical counterparts. 

In addition, we extend ([PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates)) these rules for rewriting trees of unbounded rank by type constraints in order to model atomic XML document update operations (renaming, insertion, deletion, replacement) as specified in the W3C [XQuery Update Facility](https://www.w3.org/TR/xquery-update-30/) (XQUF) standard. We have established **type verification** results ([PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates) and [JCSS'16](publication/2016-01-01 -One-variable-context-free-hedge-automata)) for arbitrary iterations of these operations (closure and inverse closure by rewriting), using an iterative construction algorithm for hedge automata and context-free hedge automata. 

We are also studying [[FroCoS'11](publication/2011-10-01-Controlled-Term-Rewriting), [CADE'15](publication/2015-08-01-Term-Rewriting-with-Prefix-Context-Constraints-and-Bottom-Up-Strategies)] an extension of term rewriting systems with constraints on rule application positions, as models for XML transformations. 

There are many results in type verification for XML transformations, generally dealing with a single application of a transformation written in a language such as XSLT or a top-down pass of a tree transducer. The originality, and a source of difficulty, of the approaches in [[RTA'08](publication/2008-01-01-Closure-of-Hedge-Automata-Languages-by-Hedge-Rewriting), [PPDP'10](publication/2010-07-01-Rewrite-Based-Verification-of-XML-Updates)] is that we consider arbitrary numbers of iterations of atomic update rules at arbitrary positions in the trees. 

The above verification techniques have also proven relevant for verifying the **consistency of access control policies** defined by sets of rules. This problem is generally undecidable. We have identified a decidable case (local consistency), which is moreover polynomial in time.

This theoretical work has been applied in bilateral projects with Tunisian universities ([ISCC'09](publication/2009-07-01-Automatic-Verification-of-Conformance-of-Firewall-Configurations-to-Security-Policies), [ComNet'10](publication/2010-11-01-XML-Access-Control-from-XACML-to-Annotated-Schemas)), and the [ARC Inria Access](projects/#ACCESS) project. 

The rewriting of unbounded-rank trees is an original formalism, relevant for modelling and verifying XML document transformations, which deserves further study, following developments in the theory of rewriting systems applied to bounded-rank trees.



## Data Trees

Data trees are a more detailed representation of XML documents, with labeling using both symbols in a finite alphabet (representing XML markers or tags) and data in an infinite domain (representing attribute values or textual content). 

We proposed ([LMCS'16](publication/2016-01-01-FO21-on-data-trees-data-tree-automata-and-branching-vector-addition-systems)) a model of automata computing on such trees, and proved a 1-1 correspondence with a significant fragment of the XPath navigation standard: the FO2 fragment (<, +1, ∼) fragment of 2-variables formulas of first-order logic on data trees — the predicates < and +1 are for navigating trees, while ∼ is used to compare data. The correspondence is established via a model of counter automata extending BVASS (Branching Vector Addition Systems with States), a formalism for verifying concurrent programs.

These results are based on previous work by Luc Segoufin et al. on the data word model (instead of trees), which is considered a reference in Web data theory. It should be noted that the above article establishes a result of inter-reduction of decision problems, with decision remaining an open problem that generalizes the problem of decidability in BVASS, the latter being considered very difficult.

