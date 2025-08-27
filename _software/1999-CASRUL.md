---
name: CASRUL
link: http://www.loria.fr/equipes/cassis/softwares/casrul/ 
duration: 1999 &mdash; 2000
organization: Inria Nancy, LORIA
---

I developped at Inria Nancy the first version of the system CASRUL,
a security protocol verification tool based on deduction rules.

This implements a procedure for compiling semi-formal protocol specifications into multiset rewrite rules describing precisely the operations of the agents for the analysis of the received messages and the construction of the sent messages, as well as the faculties of the attackers. 
The translation of this intermediate language into input format (Horn clauses) for the daTac theorem prover (developped by Laurent Vigneron), 
allows a formal verification of the protocols using first-order deduction procedures such as narrowing. 

The approach is presented in
[Compiling and verifying security protocols](https://link.springer.com/chapter/10.1007/3-540-44404-1_10), 
7th international conference on Logic for programming and automated reasoning LPAR’00, Springer LNAI 1955,
co authored with Michaël Rusinowitch and Laurent Vigneron 
-- see also <https://hal.inria.fr/inria-00072712/>.

This system CASRUL has later evolved into a tool-suite developed 
during the European projects
[AVISPA](http://www.avispa-project.org) 
and [AVANTSSAR](http://www.avantssar.eu).



