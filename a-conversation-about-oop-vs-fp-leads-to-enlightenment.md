
sagar [10:47 AM]  
why is that, why is OOP trash

katychuang [10:48 AM]  
excellent question

[10:49]  
I’ve been told FP and OOP are different paradigms

[10:52]  
I’m going to butcher a quote from a talk by Evie so I’m going to paraphrase… She said something like when you work with OOP you create lots of objects and rules on how they should interact and yet somehow end up having to touch each other a lot and inappropriately

[10:53]  
On the other hand FP (especially Haskell) is like working with shapes, like that baby shape fitting toy where you focus more on fitting the type parameters correctly

[10:56]  
I think of programming as building a piping system. FP (especially strongly typed FP) makes it more idiot proof because the connectors are more obvious. But I don’t know if my mental model fits for the breakdown of OOP to FP… Clojure is a dynamically typed FP language for example

sagar [10:57 AM]  
interesting

pedrofurla [10:58 AM]  
katychuang where that paraphrasing from?

katychuang [10:58 AM]  
from Evie, she gave a lightning talk months ago

sagar [10:58 AM]  
because I want to start coding professionally,and I'm working for a company and they're happy to let me do intern stuff for their JS & Python so I was reading those but it was like >_>

[10:58]  
Haskell I find much more appealing I don't know why

[10:59]  
They have scala here too which seems like a reasonable middle ground but all the scala programmers here are ex java and keep giving me java examples or talking about the jvm

m [10:59 AM]  
i've done production level java

[10:59]  
and it's a goddamn jungle

pedrofurla [10:59 AM]  
I good way to see what *I think* you are trying to say is by writing an interpreter in OO vs FP

katychuang [10:59 AM]  
*nod* I personally wouldn’t call OOP trash, a lot of companies use OOP and they make lots of money… and also have huge teams and a lot of documentation. It’s just gooey-er to work with

pedrofurla [11:00 AM]  
m: it’s a jungle out there

katychuang [11:00 AM]  
haha

m [11:00 AM]  
The problem is once the Java structure gets bloated with enough objects and inheritance rules

sagar [11:00 AM]  
java is just absurd. right from syntax and the whole class system. seems like a roundabout way of doing things.

m [11:00 AM]  
it becomes hard to really build on

katychuang [11:00 AM]  
jenga

sagar [11:00 AM]  
that's actually one of the key projects this quarter lol

m [11:00 AM]  
^^^

[11:00]  
Jenga is the nail on the head

pedrofurla [11:01 AM]  
more like the Cthulhu lair

katychuang [11:01 AM]  
it’s nice to work with the reliability haskell provides. cabal on the other hand is not so reliable :slightly_smiling_face:

m [11:02 AM]  
The appeal to me was watching the fluidity of someone programming in Haskell

[11:02]  
it had an elegance to it

katychuang [11:03 AM]  
oh yes. i was sold on the Maybe type

m [11:03 AM]  
i was sold on not making folders of class files

katychuang [11:03 AM]  
haha that’s a good one also

[11:04]  
the brevity was a breath of fresh air

horrorcheck [11:04 AM]  
I really like OOP…. I just like FP too

katychuang [11:06 AM]  
:smiley:

horrorcheck [11:06 AM]  
(that doesn’t mean I’m going to use Scala — I like hotdogs and ice cream but I’m not eating hot dog-flavored ice cream)

katychuang [11:06 AM]  
haha good analogy

haskellandchill [11:09 AM]  
OOP has cool stories, FP has math

[11:09]  
also you can provide a reasonable formal semantics for OOP in FP

katychuang [11:10 AM]  
@sagar sometimes people are biased. obviously we all love haskell in here lol (edited)

sagar [11:10 AM]  
lol

haskellandchill [11:10 AM]  
I did OOP for 6 years, that’s my bias

katychuang [11:10 AM]  
@haskellandchill in one language or multiple OOP languages? (edited)

sagar [11:11 AM]  
Scala isYUGE though omg

[11:11]  
for monies

haskellandchill [11:11 AM]  
Ruby, with a heavy Smalltalk influence

sagar [11:11 AM]  
and career etc

haskellandchill [11:11 AM]  
Scala is a good career choice :thumbsup:

m [11:11 AM]  
thank Java for that @sagar lol

haskellandchill [11:12 AM]  
I personally can’t stand Scala, but lots of good books written for it

m [11:12 AM]  
it's taaaaainted

haskellandchill [11:12 AM]  
incidental complexity, subtyping (ew)

[11:13]  
subtyping with contravariance :boom:

pedrofurla [11:13 AM]  
we do Scala where i work, and I assure you we only have hotdogs

katychuang [11:13 AM]  
haha

[11:14]  
@haskellandchill those words.. :whoosh:

pedrofurla [11:14 AM]  
@haskellandchill yep, that’s why we stick only with the hotdogs

haskellandchill [11:14 AM]  
Haskell is far behind Scala in libraries, that’s very true

pedrofurla [11:14 AM]  
yah, but most scala libraries aren’t great or are just plain bad java libraries

haskellandchill [11:15 AM]  
¯\_(ツ)_/¯

[11:15]  
I’m trying to be nice

m [11:15 AM]  
being nice is overrated

[11:15]  
i think scala has a horrendous type system

[11:16]  
now i'll be nice

haskellandchill [11:16 AM]  
well… it’s important, these are peoples livelihoods, it can get emotional

[11:16]  
I almost got kicked out of a conference so I’m adjusting my approach

pedrofurla [11:16 AM]  
subtyping and parametricity has a lot of potential for really big mess

m [11:16 AM]  
goes back to what @haskellandchill said about incidental complexity

pedrofurla [11:16 AM]  
@haskellandchill by saying scala sucks?

haskellandchill [11:16 AM]  
also I’m not as funny as I think I am and it’s the internet

pedrofurla [11:17 AM]  
well Scala sucks

haskellandchill [11:17 AM]  
just talking about programming languages :innocent:

katychuang [11:17 AM]  
hmm… would it be better to try to keep conversation in here fairly conducive to learning haskell rather than flaming other languages?

m [11:17 AM]  
yes

haskellandchill [11:17 AM]  
definitely :thumbsup: (edited)

m [11:18 AM]  
this is more random appropriate

katychuang [11:18 AM]  
so what are these big words that were dropped in here

sagar [11:18 AM]  
:fire: :fire_engine:

haskellandchill [11:18 AM]  
if you’re learning Haskell you don’t need to know about subtyping

sagar [11:18 AM]  
CONTRAVARIANCE good god.

katychuang [11:18 AM]  
contravariance? i’ve never heard of that

haskellandchill [11:18 AM]  
contravariance is important

[11:18]  
if you know Functor you can discuss (edited)

pedrofurla [11:18 AM]  
-variance

m [11:19 AM]  
parametricity is a good one

haskellandchill [11:19 AM]  
```
a -> b -> f a -> f b
a -> b -> f b -> f a
```
(edited)

pedrofurla [11:19 AM]  
covariance is the first

haskellandchill [11:19 AM]  
first is covariant, second is contravariant

pedrofurla [11:19 AM]  
contra- is the se...

haskellandchill [11:20 AM]  
yup, usually you don’t say covariant, just normal functor

pedrofurla [11:20 AM]  
but the variance thing in Scala is relating to subtyping and type parameters

haskellandchill [11:20 AM]  
yeah but as we are Haskell focused, we can just ignore all that :smile:

[11:20]  
which is awesome less stuff to learn

pedrofurla [11:21 AM]  
`A <: B`, `F[A] <: F[B]`

haskellandchill [11:21 AM]  
god no please no

pedrofurla [11:21 AM]  
`A <: B`, `F[B] <: F[A]`

[11:21]  
heheh

haskellandchill [11:21 AM]  
any way if anyone isn’t solid on reading haskell type signatures

[11:22]  
you have an `a`, a `b`, and a `f a`

[11:22]  
you get an `f b`

katychuang [11:22 AM]  
i remember it taking a while to learn how to read haskell type signatures :smiley:

haskellandchill [11:22 AM]  
thats normal functor

[11:22]  
you have an `a`, a `b`, and a `f b`

katychuang [11:22 AM]  
`f a` and `f b` are functions btw

haskellandchill [11:22 AM]  
you get a `f a`, that’s contra

[11:22]  
`f` is a type level function and `a` is a type

katychuang [11:23 AM]  
oh right that confused me

pedrofurla [11:23 AM]  
type constructor, please

m [11:23 AM]  
:whoosh:

haskellandchill [11:23 AM]  
`f a` is `f` applied to `a`

[11:23]  
I prefer the perspective of type level functions

pedrofurla [11:23 AM]  
a applied to f

[11:23]  
the arguments are what are applied

haskellandchill [11:23 AM]  
huh?

pedrofurla [11:24 AM]  
`f a`, a applied to f

haskellandchill [11:24 AM]  
we usually say a function is applied to its arguments

[11:24]  
but either way

pedrofurla [11:24 AM]  
nopes

haskellandchill [11:24 AM]  
no problem boss :wink:

katychuang [11:25 AM]  
type constructor = type level functions? is that the conclusion

pedrofurla [11:25 AM]  
omg, you are right, @haskellandchill https://en.wikipedia.org/wiki/Function_application

haskellandchill [11:25 AM]  
I know I’m right

[11:25]  
thanks :slightly_smiling_face:

[11:25]  
a type constructor is a kind of type level function

[11:25]  
there are others

[11:26]  
don’t need to go into all the type level stuff, it can get complex quick and haskell isn’t the best language to express things there

[11:26]  
key takeaway is you have functions from values to values

[11:27]  
and also functions from types to types

[11:27]  
Haskell gives you a very nice lambda calculus for both

[11:28]  
it’s hard for beginners to see where you are working with values, and where you are working with types, but it is crucial to learn the distinction

[11:28]  
lots of Haskell examples use the same letter for the type and value so it’s easy to get confused

[11:29]  
 ```
name :: type level lamba calculus
name value level lambda calculus
```

katychuang [11:32 AM]  
i’m confused again

m [11:32 AM]  
:whoosh:

haskellandchill [11:43 AM]  
that just means I failed :disappointed: best done with a whiteboard

[11:44]  
`I`
```
f :: a -> …
f a = …
```
(edited)

[11:44]  
those `a`’s mean different things

[11:44]  
`II`
```
f :: f a -> …
f a = …
```
(edited)

[11:44]  
those `f`’s mean different things

[11:45]  
it *is* confusing

[11:45]  
but it is also elegant

[11:45]  
you need to have the concept of a type judgement

[11:47]  
in `I` we have judgment `a:a`

[11:47]  
in `II` we have judgement `a:f a`

[11:47]  
the `a` before `:` is a value

[11:48]  
after `:` the `a` is a type

[11:48]  
`value:type` is a type judgement

m [11:48 AM]  
i think that makes more sense

sagar [11:50 AM]  
what are we judging

katychuang [11:50 AM]  
i don’t understand the part where you said “type judgement” - is the compiler making judgements?

sagar [11:51 AM]  
this is *very* useful

haskellandchill [11:51 AM]  
anyone can make a judgement

[11:51]  
you can do haskell by hand

[11:51]  
the compiler checks our judgements

[11:51]  
and infers judgements when we are not explicit

sagar [11:51 AM]  
oh

haskellandchill [11:51 AM]  
this is called type checking and type inference, respectively

sagar [11:51 AM]  
is that like type casting

haskellandchill [11:51 AM]  
no

sagar [11:51 AM]  
like implicitly it assumes a type

haskellandchill [11:52 AM]  
type casting does not exist in Haskell

sagar [11:52 AM]  
if a type isn't specified (edited)

haskellandchill [11:52 AM]  
it is unsafe

[11:52]  
it’s inference, not casting

[11:52]  
you infer a type, then check your inference

[11:52]  
with casting you force a type from another type

sagar [11:52 AM]  
ok interesting

[11:52]  
what's a good 101 on this inference stuff

haskellandchill [11:52 AM]  
doesn’t exist

sagar [11:53 AM]  
LOL

[11:53]  
but interesting distinction

haskellandchill [11:53 AM]  
Proofs and Types

[11:53]  
but it’s more advanced

[11:53]  
by Jean-Yves Girard, not beginner friendly

sagar [11:53 AM]  
so - just for mental models sake - inference is like casting except nothing is cast, it is infered and cheked and if the check fails then no compile

haskellandchill [11:53 AM]  
inference is not like casting

sagar [11:53 AM]  
where "inference" is the compiler going "oh this variable might be of x type" ?

haskellandchill [11:54 AM]  
not really

sagar [11:54 AM]  
hmm ok *erases mental blackboard*

haskellandchill [11:54 AM]  
first you say ok it is of type `x`

[11:54]  
where `x` is a type variable

sagar [11:54 AM]  
so `int x` 

> note: sagar incorrectly used a value level variable in `int x` not a type variable

> a type variable in sagar's notation would be `x value-variable-name`

haskellandchill [11:54 AM]  
then you use unification to constrain the concrete type of type variable `x`

[11:55]  
unification is a tool from logic

[11:55]  
you get two sides of an equation

[11:55]  
for example

[11:55]  
`Int = x`

[11:55]  
then you can infer type variable `x` is concrete type `Int`

katychuang [11:56 AM]  
-- this is how I read it
```
name :: [type level] [lamba calculus]
name [value level] [lambda calculus]
```
-- this is what I think you mean
```
name :: a -- type level lamba calculus
name = name -- value level lambda calculus (returns value)
```

haskellandchill [11:56 AM]  
ok thanks @katychuang let me clarify

[11:56]  
```
name :: [type level lamba calculus]
name [value level lambda calculus]
```

katychuang [11:56 AM]  
aha!

[11:57]  
so not exactly haskell syntax just yet

haskellandchill [11:57 AM]  
I’m talking at a meta level

[11:57]  
very informally

katychuang [11:57 AM]  
ahh got it

haskellandchill [11:58 AM]  
@sager if you want to know more and are comfortable with Haskell syntax I can point you to some examples

[11:58]  
er @sagar

sagar [11:58 AM]  
this is great

haskellandchill [11:58 AM]  
it’s fun to work through type constraint unification

[11:58]  
a few Haskell books have chapters on it that are very instructive

sagar [11:59 AM]  
i don't think i'm that comfortable yet, i just finished the lambda calculus stuff. I have an undergrad in electronics engineering from over 10 years ago so i'm pretty happy in mathland, programming land not so much unless we're working with PLC's

haskellandchill [11:59 AM]  
ok, yes learning to hold off on advanced things is key

[11:59]  
you can’t just try and learn everything, it’s overwhelming

katychuang [11:59 AM]  
I feel like I need a brief refresher on unification - where is it from, do mathematicians use it?

haskellandchill [11:59 AM]  
unification comes from logic, it is the basis of something like Prolog

sagar [12:00 PM]  
the first chapter of the book took me back to like 11th grade heh functions, domains etc

haskellandchill [12:00 PM]  
https://en.wikipedia.org/wiki/Unification_(computer_science)

[12:00]  
wikipedia page is very good

sagar [12:00 PM]  
when i am better at it - @haskellandchill would you like to collaborate on a 101 medium blog post

haskellandchill [12:00 PM]  
certainly

sagar [12:00 PM]  
awesome

haskellandchill [12:01 PM]  
I was going to edit some of this into “A Conversation About …” something ha

katychuang [12:01 PM]  
:+1: :+1:

[12:01]  
i see a bunch of greek letters on that wikipedia page

haskellandchill [12:01 PM]  
yup

[12:02]  
> For example, using x,y,z as variables, the singleton equation set { cons(x,cons(x,nil)) = cons(2,y) } is a syntactic first-order unification problem that has the substitution { x ↦ 2, y ↦ cons(2,nil) } as its only solution. The syntactic first-order unification problem { y = cons(2,y) } has no solution over the set of finite terms; however, it has the single solution { y ↦ cons(2,cons(2,cons(2,...))) } over the set of infinite trees. The semantic first-order unification problem { a⋅x = x⋅a } has each substitution of the form { x ↦ a⋅...⋅a } as a solution in a semigroup, i.e. if (⋅) is considered associative; the same problem, viewed in an abelian group, where (⋅) is considered also commutative, has any substitution at all as a solution. The singleton set { a = y(x) } is a syntactic second-order unification problem, since y is a function variable. One solution is { x ↦ a, y ↦ (identity function) }; another one is { y ↦ (constant function mapping each value to a), x ↦ (any value) }.
(edited)

sagar [12:02 PM]  
i didn't know the word ofr it was unification  i always called it resolving an expression

[12:02]  
from high school stuff

haskellandchill [12:02 PM]  
that’s a good section to try and understand, let me know if you have questions

katychuang [12:04 PM]  
it’s a challenge to read. i think in pictures and this is all text

haskellandchill [12:04 PM]  
yea I want to do visualizations

[12:05]  
it’s ok to accept you can’t aren’t prepared for the formalism and move on

[12:05]  
that wikipedia page isn’t going anywhere :smile:

katychuang [12:05 PM]  
It’s cool that John Alan Robinson came up with the unification algorithm, contributing to foundations of automated theorem proving. That gives some context

[12:06]  
Now I see unification is important as far as having a premise that the machine can compute the logic (I assumed it was a given that computers can compute as a millennial)

[12:06]  
So yes, moving on :slightly_smiling_face:

pedrofurla [12:10 PM]  
wow, the conversation changed drastically
