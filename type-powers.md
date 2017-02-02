## Java 2020

Generics did not always exist in Java. Having them increases what you can express about the relationships between types. As Java continues to advance it may soon add the ability to express deeper type relationships. I want to discuss what we have now for types in Java and what it gives us while highlighting what we may have in the future and the type powers that will give us.

## Concrete Types

We are pretty comfortable with concrete types and the kind of errors they prevent. You can avoid writing tests that you would have to write in a dynamic language thanks to compile time checking.

```
public T {}
```

```
interface I {
   T f(T t); 
}
```

### Argument Against

> Type models do not specify behavior. The correctness of your type model has no bearing on the correctness of the behavior you have specified. At best the type system will prevent some mechanistic failures of representation (e.g. Double vs. Int); but you still have to specify every single bit of behavior; and you still have to test every bit of behavior.

Concrete types don't specify behavior, especially in the presence of null, which acts as a value of every type.

```
public Integer f(Integer i) {}

f(null); // :(
```

But we can do more.

## Generic Types - Type Variables

> What if programmers could actually express their intent, and mark a list as being restricted to contain a particular data type? This is the core idea behind generics.

Generic types let us take the familar idea of a variable and use it at the type level. The variables themselves can be thought of having a type at a level higher as we will discuss later. Allowing a variable is a form of quantification, specifically saying for all possible types. We can constrain the types available by using additional syntax.

### for all interface

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

### for all class

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

### for all interface over class

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

### for all constrained

```
T<? extends I>
```


## More Power

Unfortunately today's Java can't express type variables that can be applied to other types, but we can straightforwardly talk about it using Java syntax.

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

## Super powers

We can transform a tree to a list many ways, these transformations of T<A> to L<A> are structure changing transformations that preserve values. We express this using invariants we expect the transformation to preserve.

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

## Arguing Types

> Types impose coupling.  f(Int) is coupled to Int.  f(o) is only coupled to operations of o.
