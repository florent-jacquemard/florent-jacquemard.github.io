---
title: "Term Rewriting with Prefix Context Constraints and Bottom-Up Strategies"
authors: 'Florent Jacquemard, Yoshiharu Kojima, Masahiko Sakai'
collection: publications
category: conferences
permalink: /publication/2015-08-01-Term-Rewriting-with-Prefix-Context-Constraints-and-Bottom-Up-Strategies
date: 2015-08-01
venue: 'Proceedings of 25th International Conference on Automated Deduction (CADE), Springer LNCS volume 9195'
paperurl: 'https://doi.org/10.1007/978-3-319-21401-6_9'
hal: 'https://inria.hal.science/hal-01149319'
citation: 'Florent Jacquemard, Yoshiharu Kojima, Masahiko Sakai, &quot;Term Rewriting with Prefix Context Constraints and Bottom-Up Strategies&quot; In the proceedings of 25th International Conference on Automated Deduction (CADE), LNCS volume 9195, 2015.'
---

abstract: 
We consider an extension of term rewriting rules with context constraints restricting the application of rewriting to positions whose prefix (i.e. the sequence of symbols from the rewrite position up to the root) belongs to a given regular language. This approach, well studied in string rewriting, is similar to node selection mechanisms in XML transformation languages, and also generalizes the context-sensitive rewriting. The systems defined this way are called prefix constrained TRS (pCTRS), and we study the decidability of reachability of regular tree model checking and the preservation of regularity for some subclasses. The two latter properties hold for linear and right-shallow standard TRS but not anymore when adding context constraints. 
We show that these properties can be restored by restricting derivations to bottom-up ones, and moreover that it implies that left-linear and right-ground pCTRS preserve regularity and have a decidable regular model checking problem.