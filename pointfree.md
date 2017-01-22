explain

```
sum . map :: (Num [b], Foldable ((->) [a])) => (a -> b) -> [b]`
```

by definition

```
sum :: (Num a, Foldable t) => t a - > a
map :: (a' -> b') -> [a'] -> [b']
. :: (a'' -> b'') -> (b'' -> c) -> (a'' -> c)
```

creates constraints

```
t a ~ b''
a ~ c
((->) [a']) ~ b''
```

then sum becomes

```
((->) [a'] -> [a']
```

which I didn’t know `[]` has a num instance, but I suppose it is `length`
