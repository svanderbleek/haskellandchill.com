# Loops

Let's talk about loops. We are going to approach the problem very generally and build our machinery as we go.

## Iteration and Recursion

We can describe a loop iteratively or recursively and for simple loops it is easy to see their equivalence.

```
i (n, f, 0) = (n - 1, n * f, 0)
i (1, f, 0) = (1, f, 1)
i (_, f, 1) = (_, f, 1)
```

Here we iterate `i` repeatedly on a state `(Int, Int, Bool)` until we meet our condition and flip `Bool` to signal completion, returning the accumulated factorial `f`. Iteration follows our intuition for looping. We take a set of instructions and repeat them until we reach a desired condition. The instructions are a function of arguments that we may
transform with each iteration.

```
f n = n * f (n - 1)
f 0 = 1
```

Recursion is more general than iteration and describes instructions that can depend on the results of additional
iterations. When recursion only depends on the previous iteration it is the same as the iterative method of argument transformation until a condition is met. Recursion can be modeled with iteration and there is an isomorphism that may be noncomputable.

Recursion can be described with reuse of a function through name, which requires operational concepts to treat rigourously, or through fixpoints, which require theory.

## Fixpoints

To work in theory of fixpoints we need the concept of an order, intuition for the positive integers under `<` is sufficient. We will use '<' to mean whichever order we are dealing with. We explicitly work with orders like the positive integers to give ourselves a well-founded base case like `0`. At the bottom of sets under subset order it would be the empty set). 

An arbitrary domain can be mapped into an ordered codomain using a function `f : D -> O`, the class of these functions can then be ordered based on their values in the codomain over each point in domain.

```
f < g ~ forall x. (f x < g x)
```

Partial functions can also be ordered by the set of values they are defined on using subset relations over the domain.

```
f < g ~ (x. f x) < (y. f y)
```

We use `~` to denote a definition, and `quantifier variable. condition` to do things like assert `forall`, `exists`, or  simply collect all when no quantifier is present.
