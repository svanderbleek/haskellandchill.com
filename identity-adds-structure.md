Semigroup allows easy instances due to lack of identity

Always left:

```
instance Semigroup t where
  a <> _ = a
```

Always right:

```
instance Semigroup t where
  _ <> b = b
```

By requiring

```
0 <> b = b
a <> 0 = a
```
