Data constructor changing functor:

```
T a
  = T1 a
  | T2 a

instance Functor T where
  fmap :: (a -> b) -> T a -> T b
  fmap f (T1 a) =
    T2 (f a)
```

Why is it wrong? Because

```
fmap :: (for all t. for all a. (for all a. a -> a) -> t a -> t a)
fmap id :: (for all t. for all a. t a -> t a)
id :: (for all t. for all a. t a -> t a)
=>
fmap id ~ id
```

But

```
fmap id (T1 a)
= T2 a
\= T1 a
=>
fmap id \~ id
```
