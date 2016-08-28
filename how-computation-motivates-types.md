Let's start with a finite alphabet.

```
{a,b,c..}
```

We can form sentences with this alphabet.

```
cdabbbaaac
```

And we can name sentences.

```
s. cddddaa
f. dbba
```

These sentences are unchanging. 
We want to be able to react to inputs by forming sentences based on inputs. 
We can do this through lambda abstraction, naming parameters for our sentences.

```
s p. pa
s p r. asdpfasdr
f a. a
f a. b
```

Now we have a basic notion of computation.

```
f a. b
```

Computes the sentence `b` for any input. We haven't dealt with what using inputs in a sentence means either.

```
f a. bab
```

Computes the sentence `bab`. Let's try using `f` by introducing application. We apply `f` to `ccc` by juxtaposition.

```
[0] f a. bab
[1] f ccc
[2] bcccb
```

These are simple one-step computations. We can introduce more dynamism by allowing inputs to express computations.

```
[0] f g. g b
[1] f f
[2] f b
[3] b b
```
