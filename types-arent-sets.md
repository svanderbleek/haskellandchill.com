## Types and bits

A simple concept of types directly relates a type to the set of values that inhabit that type.
This is the bit-sequence concept of types.

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

Extrapolating from this you can say the `string` type is all possible bits that are be interpretted as strings.

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

Or the type `string` is equivalent all bit-sequences labelled with type `string`.

It seems then that a type is a collection of labelled values. If we only had constant expressions of values
that would be accurate. `string` or `int` would be the set of all possible bit configurations with their respective type labels.
But this is a boring world where nothing happens.

## Types and functions

Introducing functions changes this. Functions are compound types that exchange values of one type for values of another type. A naive view of functions is that of a fully specified mapping between sets, assigning each element in the input set to an element in the output set.

A function assigns an an output value of the output type when the input value is of the input type for the function. This assignment can be interpreted as an assertion about types. When I say that I have a function from `int` to `string`
I also make the assertion that I can receive an arbitrary `int` value and provide a determinate `string` value in return.

```
a:int->string.'a'
> a 1
> 'a'
```

So function `a:int->string` has type `int->string` and thus asserts that it returns type `string` when given an `int`. Since `a` simply returns the `string` `'a'` for all inputs we say this assertion is true.
This is a special case because we can see the internals of `a`, but often this is not the case. We more generally have just the opaque assertion the function implies.

```
f:int->string.[hidden]
```

What is the nature of this assertion? We can feed the function an input and check the result, but what if we don't receive a result? Should we also represent this as elment of the type set `string`?

For example we don't know that the function even terminates. We expect `f 1` (`f` applied to `1`) to be of type `string` but we may never finally receive the
asserted string.

```
(f 1):string
> f 1
... waits forever ...
```

Clearly `f 1` is not a bit string, but it is of type `string` by definition. As there are many ways we can inhabit the possibility of providing a value of type `string`, including those ways that do not actually provide a value, there is no concrete set of values to support the type `string`. We can model this condition in many ways, including the same labelled sets used earlier with extra values representing computation and extra structure to handle these indeterminate values, or we can deal with types directly as their own abstraction. We abstract from sets of values to the concept of types. This is how we move beyond sets and into domains. This is the beginning of type theory.

## Postscript

Can we get to this concept another way? Certainly. If we consider parsing our constant bit values.

```
i:int.1010011101001...
```

The ellipses denote that we have parsing still to do. We don't know if we will ever finish parsing so a similar argument results (parsing can also be seen as a function `f:bit->int`). Sets become something more interesting when we introduce computation, which contains the idea of termination. Types then abstract computability and we can develop an algebra of types as an algebra of computability. 

The abstraction we make with types is similar to abstractions like probability. We invent an abstraction for something intangible and indeterminate then manipulate it through the abstraction. A probability distrubtion over outcomes can stand in for outcomes in statements about outcomes, like that an outcome is less than a certain value.

```
X < 5
```

Where `X` is a random variable. This is different from `x < 5` where `x` is a single, fixed outcome with no additional structure.

This is abstraction as reification, introducing a new conceptual level where ideas are values that can be manipulated directly. Types are what we call our abstraction of values that our programs take as input and produce as results.
