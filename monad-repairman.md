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

No it's different

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
