
## Scavenger

### Idea: Parallel Theorem Proving

#### Description

Scavenger is a new theorem prover (implemented in 2016) based on the [Conflict Resolution](https://arxiv.org/pdf/1602.04568v1.pdf) calculus, which generalizes conflict-driven clause learning ([CDCL](https://en.wikipedia.org/wiki/Conflict-Driven_Clause_Learning)) to first-order logic. 

An interesting fact about the Conflict Resolution calculus is that there seems to be a natural way to parallelize it according to the [actor model](https://en.wikipedia.org/wiki/Actor_model) of concurrency. Suppose that there are N predicate symbols in a problem. We could have M actors, each an "expert" in N/M predicate symbols. Actors communicate with each other primarily by sending clauses to each other. When an actor A receives a clause "P1(X^1_1,...,X^1_j1) or ... or Pk(X^k_1,...,X^k_jk)" it should make decisions/assumptions to eliminate the literals that do not belong to its expertise domain. For example, if P1 does not belong to the expertise domain of A, it should decide "not P1(X^1_1,...,X^1_j1)". 
When A derives a new conflict-driven learned clause containing only literals outside its domain of expertise, it sends this clause to another actor.

The idea is to mimick how humans solve problems socially: we specialize in certain topics, and when a problem is outside the topics of our expertise, we make assumptions (e.g. unproved beliefs about the truth of a conjecture) about the problem and we check our assumptions with other people who are experts in the topics of our assumptions.

We foresee two potential challenges in this approach:

1. It is not yet clear whether proof search remains complete when the search is split across many actors. We must ensure that clauses are distributed in a way that guarantees that all derivable clauses are eventually derivable.
2. After a while during the proof search, the load could become unequally distributed across all the actors. For instance, if some predicate symbols occur rarely in the problem, an actor specializing in those predicate symbols will eventually become idle. To prevent this, the domains of expertise of actors could be dynamic. Idle actors should seek to expand their domains of expertise, whereas overloaded actors should seek to reduce their domains of expertise.


The implementation should use Scala's Akka library for actor-based concurrency.


#### Requirements

For this project, we are looking for a student:

- with experience in Scala (or with solid programming skills in other object-oriented and functional programming languages and willing to learn Scala).

- with firm knowledge of logic (especially first-order logic, unification)

- with experience in concurrency (preferably, though not exclusively, in Akka)

- willing to do performance regression tests (with Scalameter) and experiments to evaluate how helpful the parallelization is.

- with technical creativity to fill the gaps and formulate the idea described above in a mathematically precise way.


#### Mentors

Daniyar Itegulov, Bruno Woltzenlogel Paleo




