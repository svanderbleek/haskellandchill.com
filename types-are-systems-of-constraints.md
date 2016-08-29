Application induces one of the simplist systems of constraints

```
f : A -> A
a : A
u : A
u = f a
```

This is a solved system, we can introduce variables to create a solvable system

```
f : A -> A
a : A
u : ?
u = f a
=>
u : (A -> A) A
u : A
```

or

```
f : ? -> A
a : A
u : A
u = f a
=>
f : (? -> A) A
f : A -> A
```

