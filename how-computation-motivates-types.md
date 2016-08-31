Let's start with a finite alphabet.

```
{a,b,c..}
```

We can form sentences with this alphabet.

```
cdabc
```

And we can name sentences.

```
s. cdaa
f. dbba
```

These sentences are unchanging. 
We want to be able to react to inputs by forming sentences based on inputs. 
We can do this through lambda abstraction, naming parameters for our sentences.

```
f a. a
f a. b
f a. aa
```

Now we have a basic notion of computation. Take

```
f a. b
```

This computes the sentence `b` for any input. Take

```
f a. bab
```

This computes the sentence `bab`. Let's use `f` by application. We apply `f` to `c`.

```
f a. bab
=>
[1] f c
[2] bcb
```

These are simple one-step computations. We can introduce more dynamism by allowing inputs be computations and utilizing self-application.

```
f g. g b
=>
[1] f f
[2] f b
[3] b b
```
