---
title: "Unique Normalization for Shallow TRS"
authors: 'Guillem Godoy,  Florent Jacquemard'
collection: publications
category: conferences
permalink: /publication/2009-06-01-Unique-Normalization-for-Shallow-TRS
date: 2009-06-01
venue: 'In the proceedings 20th International Conference on Rewriting Techniques and Applications (RTA), Springer LNCS vol 5595'
paperurl: 'https://doi.org/10.1007/978-3-642-02348-4_5'
hal: 'https://inria.hal.science/inria-00578959'
citation: 'Guillem Godoy,  Florent Jacquemard, &quot;Unique Normalization for Shallow TRS&quot; In the proceedings of 20th International Conference on Rewriting Techniques and Applications (RTA), Springer LNCS vol 5595, 2009.'
---

abstract:
Computation with a term rewrite system (TRS) consists in the application of its rules from a given starting term until a normal form is reached, which is considered the result of the computation. The unique normalization (UN) property for a TRS R states that any starting term can reach at most one normal form when R is used, i.e. that the computation with R is unique. We study the decidability of this property for classes of TRS defined by syntactic restrictions such as linearity (variables can occur only once in each side of the rules), flatness (sides of the rules have height at most one) and shallowness (variables occur at depth at most one in the rules). We prove that UN is decidable in polynomial time for shallow and linear TRS, using tree automata techniques. 
This result is very near to the limits of decidability, since this property is known undecidable even for very restricted classes like right-ground TRS, flat TRS and also right-flat and linear TRS. We also show that UN is even undecidable for flat and right-linear TRS. The latter result is in contrast with the fact that many other natural properties like reachability, termination, confluence, weak normalization, etc. are decidable for this class of TRS.