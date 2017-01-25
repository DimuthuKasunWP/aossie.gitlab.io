
## Computational Philosophy

### Idea: Formalization of Ontological, Cosmological and Pantheistic Arguments

#### Description

More than 300 years ago, when computers as we know today didn't even exist, Leibniz pioneered the idea of automated reasoning, with his ideas of *characteristica universalis* and *calculus ratiocinator*. He famously said:

    "If controversies were to arise, there would be no more need of disputation between two philosophers than between two accountants. For it would suffice to take their pencils in their hands, to sit down with their slates and say to each other (with a friend as witness, if they liked): Let us calculate." (Translation by Russell)

Today we finally have the necessary automated deduction technology to achieve Leibniz's dream, but it has rarely been applied to philosophy as originally intended by Leibniz. This is unfortunate. As Leibniz himself put it:

    "I find that most people who take pleasure in the mathematical sciences shrink away from metaphysics, because they find light in the former but darkness in the latter. [...] Yet it seems to me that light and certainty are more needed in metaphysics than in mathematics itself, because mathematical matters carry their own tests and verification with them, this being the strongest reason for success in mathematics. But in metaphysics we lack this advantage entirely." -- Leibniz (On the Correction of Metaphysics and the Concept of Substance, 1694)
 
Recently, however, there has been a surge of interest in the application of automated reasoning to metaphysics. Notable works include the [formalization of Anselm's ontological argument](http://mally.stanford.edu/cm/ontological-argument/) by E. N. Zalta and P. E. Oppenheimer in 2011 and [formalizations of several variants of Gödel's ontological argument](https://www.gitlab.com/aossie/ComputationalPhilosophy) by C. Benzmüller and B. Woltzenlogel Paleo since 2013.

These works not only are interesting from a philosophical and historical perspective, but they also provide challenging benchmarks for testing theorem provers. As some of these arguments rely on non-standard logics, formalizing them also requires embedding these non-standard logics into the standard logics used by current theorem provers. These embeddings are a useful infra-structure reusable in other philosophical and non-philosophical projects relying on the same logics.

In this project idea, we would like to expand our previous work with (a subset of) the following formalizations:

1. *Caramuel's Proof of God's Non-Existence* (Easy): This proof is discussed in detail (and in formal logic) in the paper "Ontological Proofs of Existence and Non-Existence" by Petr Hájek in Studia Logica in 2008. It would be the first proof of non-existence in our collection.
2. *Leibniz's First Cosmological Proof* (Easy): This proof is discussed precisely in natural language in one of Leibniz's earliest papers, "Dissertation on the Art of Combinations" (1966), chapter 1.
3. *Formalization of Salamucha's Logical Analysis of St. Thomas Aquina's ex Motu arguments* (Intermediate): This logical analysis is available in chapter 1 of Salamucha's book [Knowledge and Faith](https://books.google.com.au/books?id=ptm1xOmPl3AC&printsec=frontcover&source=gbs_ge_summary_r&cad=0#v=onepage&q&f=false). The analysis is done in a modern logic, but with unusual notation.
4. *Formalization of Simulation Arguments* (Hard): These are metaphysical arguments concluding that we are probably living inside a computer simulation. An interesting modern variant is [Nick Bostrom's Simulation Argument](http://www.simulation-argument.com/simulation.html) (which has a [vulnerability and a patch](http://www.simulation-argument.com/patch.pdf)). Formalization of this argument seems conceptually harder than the formalizations in our previous works, because it seems to rely on arithmetical reasoning.
5. *Spinoza's Pantheistic Proof* (Very Hard): more than 300 years ago, Spinoza offered an unusual proof of God's existence in the first chapter of his [Ethics](http://www.gutenberg.org/files/3800/3800-h/3800-h.htm) book. The chapter and the proof are long, and written in a semi-formal style. A formal logical analysis seems hard. What is interesting in this proof is that Spinoza has a pantheistic notion of God, in which God and Nature seem to be identified with each other.

If you are interested in this project idea, please choose a (possibly improper) subset of the formalizations above and provide a realistic timeline in your proposal. Depending on how many slots we receive from Google, we might be able to accept more than one student, to work on disjoint subsets.

We recommend reading our [papers and talk slides](https://gitlab.com/aossie/ComputationalPhilosophy/tree/master) and having a look on the files and lecture notes of the [Computational Metaphysics course](http://www.inf.fu-berlin.de/users/lex/lehre/compmeta/).


#### Requirements

For this project, we are looking for a student with:

- good knowledge of logic (especially higher-order logic and the Isabelle proof assistant)

- a deep interest in philosophy



#### Mentors

Christoph Benzmüller, Bruno Woltzenlogel Paleo




