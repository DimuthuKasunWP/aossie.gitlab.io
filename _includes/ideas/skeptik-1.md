
## Skeptik

### Idea: Performance, Performance!

#### Description

Although Skeptik's proof compression algorithms are very efficient (usually linear in the length of proofs), Skeptik suffers from a few performance bottlenecks, which prevent it from being applied to huge proofs, such as the [wikipedia-sized proof](https://www.newscientist.com/article/dn25068-wikipedia-size-maths-proof-too-big-for-humans-to-check/) related to [Erdős Discrepancy Problem](http://cgi.csc.liv.ac.uk/~konev/SAT14/). This project idea aims to solve these bottlenecks. In particular, we have identified the following critical performance issues:

1. Skeptik currently uses Scala's combinator parsing library, which is convenient but not efficient. 

2. Skeptik calls [DRAT-Trim](http://www.cs.utexas.edu/~marijn/drat-trim/) to convert DRUP proofs to resolution proofs in the [TraceCheck format](trace-check format), and then parses the resolution proof. When parsing the resolution proof, it needs to figure out the order of resolution steps in every resolution chain. This is currently done in a naive way.

In this project idea, we would like to:

1. Use other more efficient parsing frameworks. Some possibilities include packrat parsing and any parsing framework for Java, since Scala is fully compatible with Java.

2. Invent and implement a more efficienct method to figure out the order of resolution steps in resolution chains, in order to parse resolution proofs. One possibility would be to implement reverse unit propagation, as DRUP and DRAT proof checkers do. Another possibility would be to implement a new *DRAT to Resolution* converter that would output ordered chains.

Besides these critical performance issues that we have already identified, we would appreciate any other form of performance improvement. We believe, for instance, that choosing better collection data structures (e.g. parallel collections) could easily make Skeptik faster.

We would consider this project idea successful if we could parse the above-mentioned Erdős discrepancy proof.

#### Requirements

For this project, we are looking for a student:

- experienced in Scala

- possibly with some knowledge of C++ as well

- experienced in writing efficient parsers (in Scala or in Java)

- willing to profile the performance of Skeptik (with tools such as YourKit) and do performance regression tests (using libraries such as Scalameter)

- with basic knowledge of propositional logic, SAT-solving and the resolution calculus (these topics can be easily learned in the Handbook of Satisfiability, in Wikipedia and in the internet in general).



#### Mentors

Adrián Rebola-Pardo, Bruno Woltzenlogel Paleo


