## Java 2020

In a few years Java may add higher-order type feature. This is what that future may look like.

## Simple Today

```
public T {}
```

```
interface I {
   T function(T t); 
}
```

```
interface I<A> {
  A function(A a);
```

```
public S<T> {
  T function(T);
}
```

```
interface I<S<T>> {
  S<T> function(S<T> s);
}
```

# The Future

```
interface F<S<T>> {
  S<B> functor(S<A> a);
}
```

```
interface N<B<T>, A<T>> { 
  B<T> natural(A<T> a);
}
```

```
public S1<T> {}
public S2<T> {}

public P implements N<S1<T>, S2<T>> {
  S2<T> natural(S1<T> s1) {}
}
```
