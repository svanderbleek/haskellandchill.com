# Loops

Let's talk about loops. We are going to approach the problem very generally and build our machinery as we go.

# Iteration and Recursion

We can describe a loop iteratively or recursively.

```
a(i) = i
f(a, i) = a(i) * a(i - 1)
```

```
f(n > 0) = n * f(n - 1)
f(0) = 1
```

Recursion can be described with reuse of a function through name,
which requires operational concepts to treat rigourously, or through fixpoints, which
require only a mind-bendingly simple bit of theory.

# Fixpoints
