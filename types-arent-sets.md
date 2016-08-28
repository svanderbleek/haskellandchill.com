## Types and bits

A simple concept of a type is directly related to the values that inhabit it.
This is the bit-sequence concept of type familar to those who
have done something like assembly.

```
01011001
```

These bits could be a `string` or `int` depending on how we interpret them. Let's label the bits `i`
and assign type `int`.

```
i:int.01011001
> i
> 24
```

Contrast that with `string`.

```
s:string.01011001
> s
> 'a'
```

Extrapolating from this you can say the `string` type is all bits that can be interpretted as strings.

```
a:string.01011001
> a
> 'a'
b:string.11100000
> b
> 'b'
c:string.00100111
> c
> 'c'
... and so on ...
```

To formalize:

```
string ~ {b|b:string.bit-sequence}
```

Or the type `string` is all `string` labeled bit-sequences.

It seems then that a type is a collection of values. If we only had constant expressions of values
that would be accurate. `string` or `int` would be the set of all possible bit configurations with their respective type labels.
But this is a boring world where nothing happens.

## Types and functions

Introducing functions changes this. Functions are types that exchange values of one type for another. With functions types can no longer be seen as sets. What are they then?
A function assigns an output to an input when the input is of an acceptable type for the function. For me to say I have a function from `int` to `string`
is to make the assertion that I can receive an `int` value and provide a `string` value in return.

```
a:int->string.'a'
> a 1
> 'a'
```

So function `a:int->string` has type `int->string` and asserts it returns type `string` when given an `int`.
We can see the internals of the constant function `a` here but often this is not the case, we just have the opaque assertion.

```
f:int->string.[hidden]
```

What is the nature of this assertion? It is not a concrete set
but an abstraction. The abstraction is a way of dealing with our ignorance of the actual function definition.

For example we don't know that the function even terminates. We expect `f 1` (`f` applied to `1`) to be of type `string` but we may never finally receive the
asserted string.

```
(f 1):string
> f 1
... waits forever ...
```

Clearly `f 1` is not a bit string, but it is of type `string`. This is how we move beyond the concept of sets and into domains.
This is the beginning of type theory.

## PostScript

Can we get to this concept another way? Certainly. If we consider parsing our constant bit values.

```
i:int.1010011101001...
```

The ellipses denote that we have parsing still to do. We don't know if we will ever finish parsing so a similar argument results (parsing can also be seen again as a function `f:bit->int`). Sets become something more interesting when we introduce computation, which contains the idea of termination. Types then abstract computability and we can develop an algebra of types as an algebra of computability. The abstraction we make with types is similar to abstractions like probability, we invent a tangible concept for something intangible and indeterminate; ie a probablity distribution. This is abstraction as reification, introducing a new conceptual level where ideas are values that can be manipulated directly.
