Weird Functor

```
T c d
  = C c
  | D d

instance Functor (T c) where
  fmap :: (a -> b) -> f a -> f b
  fmap f (D a) =
    A (f a)
```

Why?

```
fmap :: (for all a. a -> a) -> f a -> f a
fmap _ t = t
```

But

```
fmap id (D d) \= D d
```
