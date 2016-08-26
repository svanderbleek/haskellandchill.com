
my dad told me an interesting interview question that would trip up some people that might think they have a strong math background

[5:29]  
the question was:

[5:30]  
why does `-1 * -1 = 1` ?

jonschoning [5:30 PM]  
because we said so

lightandlight [5:30 PM]  
Because groups?

risto [5:31 PM]  
@lightandlight with the intercept :stuck_out_tongue:

[5:31]  
but you would probably have to explain your answer :slightly_smiling_face:

jonschoning [5:31 PM]  
a 'why' question in mathematics actually keeps rolling back until we get to axioms

haskellandchill [5:32 PM]  
yeah u would say what properties of `*` and `-` you want and why that is the result

risto [5:33 PM]  
@haskellandchill that's a very haskell and chill answer :sunglasses:

lightandlight [5:36 PM]  
I don't actually know the group laws from memory haha

haskellandchill [5:47 PM]  
`-` is inverse of `+` which `*` distributes with id `1`:
```
-1 + 1 = 0
-1 * 1 = -1
-1 * 0 = 0
-1 * (-1 + 1) = -1 * 0 = 0
-1 * (-1 + 1) = -1 * -1 + -1 * 1 = -1 * -1 + -1
-1 * -1 + -1 = 0 
=>  -1 * -1 = 1
```
(edited)

[5:47]  
damn

nickacosta [5:47 PM]  
what just happened.  That's better :slightly_smiling_face: (edited)

lightandlight [5:48 PM]  
I was wrong, group doesnt give you these laws

[5:48]  
Its ring

sleepynate [5:48 PM]  
joined #general

haskellandchill [5:52 PM]  
eh I still have it wrong lol

dk [5:53 PM]  
sounds like a great way to reject 99% of your interviewee pool

haskellandchill [5:56 PM]  
it’d be fun on a whiteboard

[5:56]  
it can be done better, for a more general result

[5:57]  
I used all concrete elements (edited)

lightandlight [5:57 PM]  
Show `-1 * b = -b`

risto [5:58 PM]  
@haskellandchill I think you're on the right track though, it has to do with distribution of multiplication

jonschoning [5:59 PM]  
Multiplication is division by the reciprocal, and anything over itself is 1.. qed. (edited)

lightandlight [5:59 PM]  
First, prove `-a * b = -(a * b)` (edited)

jonschoning [5:59 PM]  
Since there are many many ways to show this, there is no one special way

risto [6:04 PM]  
Negative one times any number is equal to the additive inverse of that number.

[6:04]  
`-1 * x = (-x)`

lightandlight [6:04 PM]  
PROVE IT

risto [6:05 PM]  
lol

[6:05]  
@jonschoning
> a 'why' question in mathematics actually keeps rolling back until we get to axioms

lightandlight [6:06 PM]  
I thought you wanted a proof hah

[6:06]  
> Show `-1 * b = -b`

haskellandchill [6:08 PM]  
which axioms is the question

[6:08]  
reverse mathematics

[6:08]  
finding minimal sets of axioms

risto [6:08 PM]  
I thought what I wrote was one of the definitions for that operation in algebra

[6:08]  
I'm not a math whiz but I'm working on it :stuck_out_tongue:

haskellandchill [6:10 PM]  
Subsystems of Second Order Arithmetic is an interesting book

[6:11]  
> given a theorem `tau` of ordinary mathematics, what is the weakest natural subsystem `S(tau)` of `Z sub(2)` in which `tau` is provable?
(edited)

[6:12]  
it’s kind of specific ha

risto [6:12 PM]  
nice
