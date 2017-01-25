
## Scavenger

### Idea: Equality Reasoning

#### Description

Scavenger is a new theorem prover (implemented in 2016) based on the [Conflict Resolution](https://arxiv.org/pdf/1602.04568v1.pdf) calculus, which generalizes conflict-driven clause learning ([CDCL](https://en.wikipedia.org/wiki/Conflict-Driven_Clause_Learning)) to pure first-order logic *without equality*. This year we would like to extend Scavenger to first-order logic *with equality*. We would like to explore three ways of doing that:

1. simply add instances of equality axioms (reflexivity, symmetry, transivity and congruence) to the problem and/or during proof search. This would be conceptually straightforward and relatively easy to implement, although it probably wouldn't be very efficient. Nevertheless, because proof search in conflict resolution is more restricted than in resolution, we expect that reasoning with equality axioms in conflict resolution would not be as inefficient as it is in resolution.
2. incorporate paramodulation rules (possibly with ordering restrictions) in the unit propagation.
3. combine conflict resolution with a [first-order generalization of congruence closure](https://members.loria.fr/HBarbosa/papers/barbosa2016-extended.pdf). [Congruence Closure](https://www.cs.upc.edu/~oliveras/espai/papers/IC.pdf) is an algorithm widely used by [SMT-solvers](http://www.cs.nyu.edu/~barrett/pubs/BKM14.pdf,https://people.eecs.berkeley.edu/~sseshia/pubdir/SMT-BookChapter.pdf) to reason about conjunctions of *ground* (i.e. variable-free) equality literals. This algorithm has recently been extended to deal with equality literals *with variables*, and therefore a combination with Scavenger is potentially fruitful.


#### Requirements

For this project, we are looking for a student:

- experienced in Scala (or with solid programming skills in other object-oriented and functional programming languages and willing to learn Scala).

- firm knowledge of logic (especially first-order logic, unification, paramodulation, resolution, congruence closure)

- willingness to take calculated risk. This is a research-intensive project idea, and the idea might not work at the end. Tolerance to failure, persistence and technical creativity to find solutions to unforeseen problems are needed.



#### Mentors

Haniel Barbosa, Pascal Fontaine, Bruno Woltzenlogel Paleo




