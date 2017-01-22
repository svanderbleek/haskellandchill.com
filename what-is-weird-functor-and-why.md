Weird Functor

```
T a
  = T1 a
  | T2 a

instance Functor T where
  fmap :: (a -> b) -> t a -> t b
  fmap f (T1 a) =
    T2 (f a)
```

Why?

```
fmap :: (for all t. for all a. (for all a. a -> a) -> t a -> t a)
fmap id :: (for all t. for all a. t a -> t a)
id :: (for all t. for all a. t a -> t a)
=>
fmap id ~ id
```

But

```
fmap id (T1 d) = T2 d \= T1 d
=>
fmap id \~ id
```
