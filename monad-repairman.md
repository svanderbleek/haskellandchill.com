Monad is wrong

```
a -> m a
```

I need to change `a` `b`

```
a -> m a
a -> b
=>
b -> m b
```

No it's more complex

```
a -> m b
b -> c
=>
c -> m c
```

Can't do this

```
a -> m b
a -> c
!=>
c -> m b
```

What I know

```
m a
=>
a -> m a

m m a -> m a

a -> m b ->
m a -> m b

a -> m b ->
b -> m c -> 
c -> m c
```
