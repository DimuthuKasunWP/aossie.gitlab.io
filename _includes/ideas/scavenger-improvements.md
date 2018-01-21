
## Scavenger

### Idea: Proof Search Improvements

#### Description

**Note: due to low mentoring capacity for this project this year, we will only accept very strong students with lots of experience in Scala and logic, who are able to work well independently.**

Scavenger is a new theorem prover (implemented in 2016 and 2017) based on the [Conflict Resolution](https://arxiv.org/pdf/1602.04568v1.pdf) calculus, which generalizes conflict-driven clause learning ([CDCL](https://en.wikipedia.org/wiki/Conflict-Driven_Clause_Learning)) to first-order logic. 

Although it currently has a proof search strategy that is believed to be complete, it is clear that there are still many things that could be improved:

1. we could use indexing techniques to reduce the number of unification attempts.
2. we should not reset the set of decision literals after every conflict. Instead, we should try to back-track non-chronologically, as SAT-solvers do.
3. to circumvent the problem that, in contrast to the propositional case, unit-propagation does not always terminate in the first-order case, we currently interleave decisions and propagations, iteratively deepening the length of propagations. We could try other approaches as well. We could, for instance, iteratively deepen the depth of terms allowed in propagations.
4. there are fragments of first-order logic (such as the effectively propositional Bernays-Schönfinkel fragment) for which first-order unit-propagation always terminates. We could investigate specialized proof search strategies for this easier fragment.



#### Requirements

For this project, we are looking for a student with:

- excellent knowledge of Scala.

- excellent knowledge of logic.


#### Mentors

Daniyar Itegulov, Bruno Woltzenlogel Paleo




