
rightfold [2:23 PM]  
I'm going to try proving that odd(x) /\ odd(y) -> odd(xy)

[2:23]  
I have an idea of how to do it

matthieubulte [2:24 PM]  
that's the spirit, then come back to us with a proof and we'll comment it

haskellandchill [2:24 PM]  
ah yes, that’s a good proof to tackle

matthieubulte [2:24 PM]  
or write your proof in coq and stay alone in your cave because you won't need us anymore ;)

rightfold [2:25 PM]  
In Coq it's probably a single builtin word

matthieubulte [2:25 PM]  
refl

[2:25]  
kidding

haskellandchill [2:25 PM]  
odd(x) -> x = 2m + 1

rightfold [2:26 PM]  
I got to the point where I have to prove that xy = 4ab + 2a + 2b + 1 but that shouldn't be hard

haskellandchill [2:26 PM]  
well it does equal that

[2:27]  
you need to prove that expression is odd

rightfold [2:27 PM]  
Right :P

haskellandchill [2:27 PM]  
it’s rearrangement :wink:

rightfold [2:27 PM]  
Which is just: addition of equal ints is an equal int, and 1+equal Int is odd

haskellandchill [2:28 PM]  
you can do it algebraically (edited)

rightfold [2:28 PM]  
s/equal/even

matthieubulte [2:28 PM]  
see , you call it rearrangement, some other call it associativity+commutativity+distributivity

[2:29]  
both proofs are fine, but you pick the level of formalism you want

haskellandchill [2:29 PM]  
I used distributivity :smile:

[2:30]  
I’m pretty good at algebraic proofs, which is why I suck at set theory/category theory/topology/other stuff (edited)

matthieubulte [2:31 PM]  
well, I guess algebra is large enough for you to find happiness

rightfold [2:32 PM]  
Algebra is great

haskellandchill [2:32 PM]  
it’s not I’m terribly unhappy, I try to do haskell by hand

rightfold [2:32 PM]  
Only thing I really don't like is geometry

haskellandchill [2:32 PM]  
I’m hopeful to tackle Algebra of Programming, maybe next year :upside_down_face:

rightfold [2:34 PM]  
I'm interested in linear logic

matthieubulte [2:46 PM]  
@rightfold: show us your proofs

rightfold [2:46 PM]  
I'm watching a tv baking show now :p

[2:46]  
I'll continue in an hour or so

rightfold [3:24 PM]  
@matthieubulte @haskellandchill I got it (edited)

[3:25]  
http://mathurl.com/hkye7d3.png (8KB)


[3:26]  
Could probably be more compact

[3:29]  
Also TIL multiplying two odd numbers yields an odd number :v

[3:29]  
I only just now realise that I never knew this

haskellandchill [3:30 PM]  
uh

[3:30]  
why did you multiply by two?

rightfold [3:30 PM]  
to define `c`

haskellandchill [3:30 PM]  
you overly complicated 7-9

rightfold [3:30 PM]  
and to have `+ 2` (edited)

haskellandchill [3:31 PM]  
you don’t want `+ 2`,  you want `+ 1` (edited)

[3:31]  
and you already had it :wink:

rightfold [3:31 PM]  
ok imagine I didn't do that

haskellandchill [3:31 PM]  
`4ab +2a + 2b`

rightfold [3:31 PM]  
7. let 2c = 4ab + 2a + 2b
8. xy = 2c + 1

[3:32]  
ah right :slightly_smiling_face:

haskellandchill [3:32 PM]  
haha yes!

rightfold [3:32 PM]  
well this is  kind of silly

[3:32]  
there's no proof that c is an integer

[3:32]  
hmm

haskellandchill [3:32 PM]  
no you need more

[3:32]  
`2c = 4ab + 2a + 2b` is wrong

[3:32]  
well not wrong, but you need to show that

[3:33]  
show what `c` is

rightfold [3:33 PM]  
4ab + 2a + 2b is an int because adding and multiplying ints yields an int

[3:34]  
and it's even because adding even numbers is even

haskellandchill [3:34 PM]  
ok sure

[3:34]  
that’s a little roundabout but works

[3:34]  
I would factor out the `2`

rightfold [3:34 PM]  
I suppose you can defer to other proofs if the axioms are too primitive

[3:34]  
but that's less fun

haskellandchill [3:34 PM]  
`2c = 2(2ab + a + b)`

rightfold [3:34 PM]  
hmm

haskellandchill [3:35 PM]  
`c = 2ab + a + b`
