# Loops

Let's talk about loops. We are going to approach the problem very generally and build our machinery as we go.

# Iteration and Recursion

We can describe a loop iteratively or recursively.

```
a i = i
f (a, i) = a i * a (i - 1)
```

```
f (n > 0) = n * f (n - 1)
f 0 =  1
```

Iteration follows our intuition for looping. We take a set of instructions and repeat them
until we reach a desired condition. The instructions are a function of arguments that we may
transform with each iteration.

Recursion is more general than iteration and describes instructions that can depend on the results of additional
iterations. When recursion only depends on the previous iteration it is the same as the iterative method of argument transformation until a condition is met.

Recursion can be described with reuse of a function through name,
which requires operational concepts to treat rigourously, or through fixpoints, which
require only a mind-bendingly simple bit of theory.

# Fixpoints

To work in theory of fixpoints we need the concept of an ordering, the simple intuition for the positive integers under `<` is sufficient. An arbitrary set can be mapped into an ordered set using a function, these functions can then be ordered based on their values at each element of the domain.

```
f < g ~ forall x. f x < g x
```

Functions can also be ordered by the set of values they are defined on using subset relations over the domain.

```
f < g ~ x. f x < y. f y
```
