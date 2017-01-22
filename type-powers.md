## Java 2020

This is not the Java of Today.

## Warmup

```
public T {}
```

```
interface I {
   T f(T t); 
}
```

```
interface I<A> {
  A f(A a);
```


Interpretation:

```
for all A
interface I <A> {
  A f(A a);
}
```

```
public S<T> {
  T f(T);
}
```


Interpretation:

```
for all T
public S<T> {
  T f(T);
}
```

```
interface I<S<T>> {
  S<T> f(S<T> s);
}
```

Interpretation:

```
for all T
for all S<T>
interface I <S<T>> {
  S<T> f(S<T> s);
}
```

# Need More Power

```
interface F<S<T>> {
  S<B> functor(S<A> a);
}
```

Interpretation:

```
for all T
for all S<T>
interface F<S<T>> {
  for all A
  for All B
  S<B> functor(S<A> a);
}
```

```
interface N<B<T>, A<T>> { 
  B<T> natural(A<T> a);
}
```

Interpretation:

```
for all T
for all B<T>
for all A<T>
interface N<B<T>, A<T>> { 
  B<T> natural(A<T> a);
}
```

Example:

```
public S1<T> {}
public S2<T> {}

public P implements N<S1<T>, S2<T>> {
  S2<T> natural(S1<T> s1) {}
}
```
