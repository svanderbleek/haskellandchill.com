## Types and bits

A simple concept of types directly relates a type to the set of values that inhabit that type.
This is the bit-sequence concept of types.

```
01011001
```

These bits could be a `string` or `int` depending on which type we assign them. Let's label it with type `int`.

```
01011001:int
> 24
```

Contrast that with `string`.

```
01011001:string
> 'a'
```

Extrapolating from this you can say the `string` type is all possible bit-sequences that are interpretted as strings.

```
01011001:string
> 'a'
11100000:string
> 'b'
00100111:string
> 'c'
... and so on ...
```

To formalize the type `string` is equivalent all bit-sequences labelled with type `string`.

```
string ~ {b|bit-sequence:string}
```

And the same for `int`.

```
int ~ {b|bit-sequence:int}
```

These sets can be put in one-to-one correspondence but the use of labels means they are completely different entities. Types have opaque representation. You can't compare `bit-sequence:int` and `bit-sequence:string` directly without cheating.

It seems then that a type is a collection of labelled values. If we only had fixed length expressions of values
that would be accurate. `string` or `int` would be the set of all possible bit configurations of finite size with their respective type labels. But this is a boring world where nothing happens.

## Types and functions

Introducing functions changes this. Functions are compound types that exchange values of one type for values of another type. A naive view of functions is that of a fully specified mapping between sets, assigning each value in the input set to a value in the output set.

Thus a function assigns an an output value of the output type when the input value is of the input type for the function. This assignment can be interpreted as an assertion about types. When I say that I have a function from `int` to `string`
I also make the assertion that I can receive an arbitrary `int` value and provide a determinate `string` value in return.

```
a i. 'a': int -> string
> a 1
> 'a'
```

Function `a i. 'a'` has type `int -> string`, asserting that it returns type `string` when given an `int`. Since `a` simply returns the `string` `'a'` for all inputs we can easily see that this assertion is true.
This is a special case because we can see the internals of `a`, but often this is not the case. We more generally have just the assertion the function type implies.

```
f i. [hidden]: int -> string
```

What is the nature of this assertion? We can feed the function an input and check the result, but what if we don't receive a result? Should we also represent this a value of the type-as-set `string`?

For example we don't know that the function even terminates. We expect `f 1` (`f` applied to `1`) to be of type `string` but we may never finally receive the
asserted string.

```
(f 1):string
> f 1
... waits forever ...
```

Clearly `f 1` is not a bit string, but it is of type `string` by definition. As there are many ways we can inhabit the possibility of providing a value of type `string`, including those ways that may not actually provide a value, there is no unstructured set of values to support the type `string`.

We can model this condition in many ways, including the labelled sets used earlier but with extra values representing indeterminate computations and extra structure on our mappings between sets that handle these indeterminate values; or we can deal with types directly as their own abstraction. Modeling with sets quickly gets out of hand when we try to represent the type of functions, that is the set of types corresponding to possible input and output assignments. 

We can't determine if a function has set membership in its type-as-set without evaluating all possible input values and checking the resulting output values. Crucially we don't know how long to wait for outputs after providing inputs. When we treat functions as type assertions we are no longer bothered by this, we simply call it an undecidable assertion in a modal logic, and treat in the type of our function as an assertion that can potentially be disproved and proved, but not proved in general. A modal logic is a logic with additional qualities of assertions other than truth-quality, such as decidability.

So we abstract from sets of values to the concept of types. By using types we can perform inferences about functions that don't rely on set membership but are composible statements in a logic. This is how we move beyond sets and into domains. This is the beginning of type theory.

## Postscript

The abstraction we make with types is similar to abstractions like probability. We invent an abstraction for something intangible and indeterminate then manipulate it through the abstraction. A probability distrubtion over outcomes can stand in for outcomes in statements about outcomes, like that an outcome is less than a certain value.

```
X < 5
```

Where `X` is a random variable. This is different from `x < 5` where `x` is a single, fixed outcome with no additional structure.

This is abstraction as reification, introducing a new conceptual level where ideas are values that can be manipulated directly. Types are what we call our abstraction of the relationship between values that our programs take as input and produce as results.
