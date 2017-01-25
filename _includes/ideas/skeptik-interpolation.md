## Skeptik

### Idea: Interpolation from proofs

#### Description

[Craig interpolants](https://en.wikipedia.org/wiki/Craig_interpolation) are one of the main theoretical concepts used in software and hardware verification. Many different interpolation systems exist. The huge majority of them work by taking a resolution proof as input and performing some operations recursively on the proof tree. However, nowadays SAT solvers do not produce resolution proofs, but a rather different kind of certificate called DRAT proofs. Therefore, to obtain an interpolant, the DRAT proof must be transformed into a resolution proof, which in general is very costly.

The goal of this project is to generate Craig interpolants from DRUP proofs, and possibly extend this framework to generate interpolants from DRAT proofs.
This would involve:

1. Extract the relevant information from a DRAT proof, including resolution chains for RUPs, and proofs of resolvents for RATs. This involves implementing a proof checking library with unit propagation.

2. Reconstruct a resolution proof using this information. In presence of RATs, the proof may become extremely large, and so it cannot be expected to be stored in memory, and the implementation must take this into account.

3. Implement an interpolation system for resolution proofs, such as McMillan's.

This project would be considered successful if interpolants can be obtained from CNF problems that are efficiently solved only by SAT solvers with inprocessing.

#### Requirements

For this project, we are looking for a student:

- experienced in C++

- possibly with some knowledge of Scala as well

- experienced with SAT solving or automated theorem provers

- with basic knowledge of propositional logic, SAT-solving and the resolution calculus (these topics can be easily learned in the Handbook of Satisfiability, in Wikipedia and in the internet in general).



#### Mentors

Adrián Rebola-Pardo, Bruno Woltzenlogel Paleo


