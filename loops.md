# Loops

Let's talk about loops. We are going to approach the problem very generally and build our machinery as we go.

# Iteration and Recursion

We can describe a loop iteratively or recursively and for simple loops it is easy to see their equivalence.

```
f (n, s, 0) = f (n - 1, n * s, 0)
f (1, s, 0) = f (1, s, 1)
f (_, s, 1) = s
```

Here we iterate f repeatedly on a state `(Int, Int, Bool)` until we meet our condition and flip the `Bool` to signal completion, returning the accumulated `s` which is the factorial.Iteration follows our intuition for looping. We take a set of instructions and repeat them until we reach a desired condition. The instructions are a function of arguments that we may
transform with each iteration.

```
f n = n * f (n - 1)
f 0 = 1
```

Recursion is more general than iteration and describes instructions that can depend on the results of additional
iterations. When recursion only depends on the previous iteration it is the same as the iterative method of argument transformation until a condition is met.

Recursion can be described with reuse of a function through name,
which requires operational concepts to treat rigourously, or through fixpoints, which
require only a mind-bending but simple bit of theory.

# Fixpoints

To work in theory of fixpoints we need the concept of an ordering, the simple intuition for the positive integers under `<` is sufficient. We will overload this operator to mean subset or whichever ordering we are dealing with. We explicitly work with positive integers to give ourselves a well-founded base case, `0`; ie an element at the bottom of our ordering (for sets this is the empty set). 

An arbitrary domain can be mapped into an ordered codomain using a function `f : D -> O`, the class of these functions can then be ordered based on their values in the codomain over each point in domain.

```
f < g ~ forall x. (f x < g x)
```

Partial functions can also be ordered by the set of values they are defined on using subset relations over the domain.

```
f < g ~ (x. f x) < (y. f y)
```

We use `~` to denote a non-rigourous presentation of an is-equivalent definition, and `quantifier variable. condition` to do things like assert `forall`, `exists`, or collect simply collect all of `variable. conditition` such that the condition is met.
