For simple type T

```
data T a
  = T a a
```

There are several subtly law violating ways to implement Applicative

```
instance Applicative T where
  pure a =
    T a a
  T f _ <*> T a b =
    T (f a) (f a)
```

Violates interchange

```
instance Applicative T where
  pure a =
    T a a
  T f g <*> T a b =
    T (g a) (f a)
```

Violates interchange and composition

```
instance Applicative T where
  pure a =
    T a a
  T f g <*> T a b =
    T (f a) (g a)
```

Works
