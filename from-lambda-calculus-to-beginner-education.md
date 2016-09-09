
katychuang [12:15 PM]  
The greek symbols are confusing me in chapter 1

sjsyrek [12:16 PM]  
Just lambda?

katychuang [12:17 PM]  
yes, I’m not fluent in lambda calculus

sjsyrek [12:17 PM]  
Neither am I. The lambda just means "anonymous function"

[12:17]  
It's like `lambda` in Python

[12:18]  
Or a closure

katychuang [12:18 PM]  
more words that I’m not familiar with

sjsyrek [12:18 PM]  
I could say "abstraction operator" but I doubt that helps

[12:19]  
Awesome so this reassures me that we'll have something to talk about in person!

[12:19]  
I put a few links to videos on the GitHub repo

[12:19]  
Re: lambda calculus

katychuang [12:19 PM]  
*nod* i could write an anonymous function in haskell and know what to expect it to do

[12:19]  
which is why i’m questioning why i need to know lambda calculus at the moment

sjsyrek [12:20 PM]  
I didn't want to learn it for awhile because it included the word "calculus" but fortunately the basics aren't too bad

[12:20]  
Yeah in `\x -> x + 1` the `\` is actually a lambda

[12:21]  
Missing its little foot (edited)

katychuang [12:21 PM]  
“Functional programming languages are all based on the lambda calculus. Some languages in this general category incorporate features into the language that aren’t translatable into lambda expressions. Haskell is a _pure_ functional language, because it does not."

sjsyrek [12:22 PM]  
LC is fundamental to computation and not just for Haskell. I think you'll find it interesting and it's only the one chapter

katychuang [12:22 PM]  
So if not directly translatable… then why are we going over lambda calculus?

sjsyrek [12:22 PM]  
Trust the book? :stuck_out_tongue_winking_eye:

katychuang [12:22 PM]  
I’m just curious how the concepts fit together

haskellandchill [12:22 PM]  
huh, lambda calc is directly translatable to Haskell

sjsyrek [12:22 PM]  
Maybe you misread it?

katychuang [12:22 PM]  
is it a typo?

haskellandchill [12:23 PM]  
you are misreading it

sjsyrek [12:23 PM]  
Haskell _is_ directly translatable

haskellandchill [12:23 PM]  
it does not include the features

[12:23]  
that are not directly translatable (edited)

sjsyrek [12:23 PM]  
You know they could have written that without so many negatives

katychuang [12:24 PM]  
thanks for the clarification! i mean i was taking it literally lol

sjsyrek [12:24 PM]  
LC is a language entirely comprised of functions

[12:24]  
So is Haskell. It's like LC with types and libraries and tools to make it actually useful and not just a mathematical abstraction

haskellandchill [12:25 PM]  
hrm math abstraction is useful :stuck_out_tongue:

sjsyrek [12:25 PM]  
But it doesn't have "extras"

haskellandchill [12:25 PM]  
actually useful, hrmpf

sjsyrek [12:25 PM]  
Not _just_ I said

katychuang [12:26 PM]  
so….. LC is an abstracted way to explain logical principles? as an intro before getting into syntactical sugar?

sagar [12:27 PM]  
that statement @katychuang is "some languages have features that can't be translated to LC. Haskell is considered pure, because it does not (have features that are *not* translatable)

haskellandchill [12:27 PM]  
Haskell has a type-level lambda calculus and a value-level lambda calculus, so that should be good motivation for wanting to learn lambda calculus, to write type signatures and function definitions

sagar [12:27 PM]  
I think i'm pretty good with the first chapter, the IRC community was very helpful

haskellandchill [12:27 PM]  
the thing about Lambda Calculus, is try some exercises

sagar [12:27 PM]  
its now writing it as programy

haskellandchill [12:27 PM]  
it’s a game of symbols first

[12:27]  
then you can look for deeper insight

sagar [12:28 PM]  
solve them by hand. best. can solve them together again at meetup.

sjsyrek [12:28 PM]  
@katychuang: I don't know if it's meant to do anything itself besides provide a model for computation

[12:28]  
@haskellandchill: good way to put it

haskellandchill [12:28 PM]  
@sjsyrek it is literally the syntax of type signatures and function definitions in haskell

sjsyrek [12:29 PM]  
When you understand the Y Combinator you will see the face of God

haskellandchill [12:29 PM]  
nah, you will understand that Y Combinator is pathological

[12:29]  
I guess god is pathological /shrug

sjsyrek [12:30 PM]  
No way understanding recursion is a big step for most people

haskellandchill [12:30 PM]  
untyped lambda calculus shows you what is dangerous about computation, and then the simply typed lambda calculus calms you

[12:30]  
let’s you sleep at night

sagar [12:30 PM]  
i do recursion but i feel like i glimpse only a little bit of it

sjsyrek [12:30 PM]  
Yeah well we do Haskell because we don't want to do Lisp

sagar [12:30 PM]  
my breakthrough program was the pascal triangle with generous help from a friend ofcourse

sjsyrek [12:31 PM]  
But I don't want to complicate things

haskellandchill [12:31 PM]  
using Lambda Calculus to understand recursion, actually complicates things

[12:31]  
because you don’t have your environment to simply call the named function again inside the definition

sjsyrek [12:32 PM]  
For me it was more like understanding how you can implement recursion entirely with functions

haskellandchill [12:32 PM]  
you can more easily understand recursion in assembly

sjsyrek [12:32 PM]  
I thought that was pretty interesting

haskellandchill [12:32 PM]  
yeah that, but it’s kind of like obsfucated recursion

[12:32]  
like the church encoding of numbers is kind of obsfucated numbers

[12:32]  
help me spell that word

sjsyrek [12:33 PM]  
@haskellandchill: I mean as far as discussing LC I want to avoid getting into esoteric subject matter too much. Assembly language? C'mon

[12:33]  
Church encoding is cool

haskellandchill [12:33 PM]  
then avoid recursion, I can’t recall what that chapter covers, I don’t think it brings up Y Combinator

[12:33]  
most important

sjsyrek [12:33 PM]  
Helps clarify enum a bit

haskellandchill [12:33 PM]  
lambda abstraction

sjsyrek [12:33 PM]  
Yes it did

[12:33]  
Does

haskellandchill [12:33 PM]  
beta reduction

[12:34]  
we need those two, nothing else for beginners

[12:34]  
well the book isn’t perfect

sjsyrek [12:34 PM]  
Y Combinator isn't that bad

haskellandchill [12:34 PM]  
it is

[12:34]  
it is terrible

sjsyrek [12:34 PM]  
:stuck_out_tongue: go start your own study group

haskellandchill [12:35 PM]  
I’m here to help :innocent:

sjsyrek [12:35 PM]  
You're just trolling. If you want to help let me set up a video feed during the meetings

[12:35]  
You can participate remotely

[12:36]  
Y Combinator throwdown

haskellandchill [12:36 PM]  
Looks like I need to adjust my approach, I am not intending to troll, though I often am, I am very serious here

sagar [12:36 PM]  
lol

sjsyrek [12:36 PM]  
While the newbies look aghast

sagar [12:36 PM]  
BETA REDUCTION - i like it because i understood it and got most of the exercises right

sjsyrek [12:36 PM]  
@haskellandchill: No it's OK now I'm trolling you

[12:37]  
Beta reduction is definitely the most important thing

haskellandchill [12:37 PM]  
I’d try and limit discussion of things like recursion for beginners

[12:37]  
lambda abstraction and beta reduction get you very far

sjsyrek [12:37 PM]  
Depends what's in the book and what people want to discuss. Not everyone will be a beginner

haskellandchill [12:38 PM]  
yes, might have to split into sections for groupwork, or something

sjsyrek [12:38 PM]  
I'm mostly a beginner anyway

[12:38]  
That's what we're doing

haskellandchill [12:38 PM]  
you’ve been warped though

[12:38]  
by fpchat

sjsyrek [12:38 PM]  
Small groups

[12:38]  
That's true

sagar [12:39 PM]  
i'm very happy to explain recursion using the pascal triangle in javascript or python cuz that's all i know :smile: :smile:

haskellandchill [12:39 PM]  
you have a mix of beginner and advanced in you, a dangerous mix :wink: (edited)

sjsyrek [12:39 PM]  
It'll be fine

[12:39]  
Though if I have to facilitate this thing I want to stick to the book and avoid giving people mixed messages

haskellandchill [12:40 PM]  
make sure you cater to beginners over making things for advanced

[12:40]  
they should get priority

sjsyrek [12:40 PM]  
You do know what I do for a living right?

haskellandchill [12:40 PM]  
judo?

sjsyrek [12:40 PM]  
:rage:

[12:40]  
Actually Aikido

[12:40]  
No I'm a university instructor

haskellandchill [12:40 PM]  
haha you’ve got this

sjsyrek [12:41 PM]  
I teach beginners beginner things all the time

haskellandchill [12:41 PM]  
do you tech undergrad?

sjsyrek [12:41 PM]  
But if someone wants something more advanced I don't say no. I meet them where they are

[12:41]  
Yes

haskellandchill [12:42 PM]  
it’s easy for these things to get sidetracked, programmers are a special breed (edited)

[12:42]  
special breed of cats, and you got to herd the cats

sjsyrek [12:43 PM]  
I'm already worried some people may find lambda calculus superfluous and I don't want to communicate that

[12:43]  
It'll be fine

[12:43]  
How could it not be?

[12:43]  
Everyone actually _wants_ to be there

[12:43]  
Do you have any idea how much easier that makes it?

[12:44]  
Try teaching Haskell to people who _ don't_ want to learn it and you'll have some inkling of my life

haskellandchill [12:44 PM]  
yes we’re lucky to not have to motivate Haskell

sjsyrek [12:44 PM]  
Programmers are at least motivated to learn. Maybe not all of them but anyone who's even bothering with Haskell must be

haskellandchill [12:45 PM]  
they are, but there’s something else… I’m not sure what it is. and there most likely will be push back on lambda calculus

sjsyrek [12:46 PM]  
I'm going to be optimistic

haskellandchill [12:47 PM]  
that’s why… you need me there :smile:

[12:47]  
next month :smile:

sjsyrek [12:47 PM]  
If people want to ignore LC or skip it or whatever that's their prerogative. All I can do is make my case like the book makes its case. At some point you have to trust the process. If people can't trust the process, well, nobody is forced to come do this and I'm not being paid for it

m [12:48 PM]  
i've never needed whoosh more than i do now

sagar [12:48 PM]  
I'm going to be there and happy to ask stupid questions if that helps

sjsyrek [12:48 PM]  
Please do

sagar [12:48 PM]  
it isn't hard

sjsyrek [12:48 PM]  
I don't want good hard questions I can't answer

sagar [12:49 PM]  
i know noobs feel fear, i don't because i used to do engg anyway so i don't care but people from non tech backgrounds don't even speak

[12:49]  
i make a lot of training material for our in house business people

sjsyrek [12:49 PM]  
But you know what all questions are fine because we'll figure them out together

[12:49]  
I'm not a developer

[12:49]  
I'm studying for a PhD in English

haskellandchill [12:50 PM]  
someone needs to give you a nice job offer so you can drop out

sjsyrek [12:50 PM]  
So fuck it let's all just be clueless nubs and OWN IT

[12:50]  
@haskellandchill: yes plz

m [12:50 PM]  
the jargon tends to throw me off

[12:50]  
and i start feeling :whoosh:

sjsyrek [12:50 PM]  
The Behance people seem pretty into it. Some smart people there too who will no doubt be able to help

m [12:51 PM]  
like im managing to advance and succeed professionally

haskellandchill [12:51 PM]  
yup so ask questions, and we can find the point

sjsyrek [12:51 PM]  
One of them runs the BabelJS project

m [12:51 PM]  
but in the grand scheme of things i've only been developing for a year

[12:51]  
so i have all of the dumb questions

[12:51]  
i got a programming job before i had a degree in it

sjsyrek [12:51 PM]  
@haskellandchill will be on call throughout the meeting to answer questions about monads

haskellandchill [12:51 PM]  
dumb questions are great, it’s the advanced questions that can derail things

[12:52]  
if you get advanced questions you can say, let’s handle that separately later

sjsyrek [12:52 PM]  
I don't really want to deal with "why should I do this?" questions

[12:52]  
Those are annoying

m [12:52 PM]  
yeah i'm not disinterested in learning things like LC

[12:53]  
it's mostly just an intimidation thing

sjsyrek [12:53 PM]  
A Haskell meetup I went to once was sort of derailed by a guy who objected to Haskell using linked lists instead of arrays

[12:53]  
Waste of time

sagar [12:53 PM]  
LOL

[12:53]  
that's the worst

[12:53]  
and those people don't even know it

sjsyrek [12:53 PM]  
At a Haskell meetup anyway. Imho. There should at least be a minimum of buy-in no? (edited)

m [12:53 PM]  
like why are you even there at that point

[12:54]  
"this language is not for me, cya"

sjsyrek [12:54 PM]  
I feel bad that the Meetup filled. I need to schedule a makeup session

m [12:54 PM]  
i am not surprised

[12:55]  
seemed like it got a lot of interest

sjsyrek [12:55 PM]  
It's like Aikido for me. It's not for everyone. So I don't try to convince people

m [12:55 PM]  
how long have you been studying? i did quite a few different disciplines in my day

sjsyrek [12:55 PM]  
Too long

[12:56]  
I'm older than @haskellandchill and he knew Lincoln

m [12:56 PM]  
hah

sagar [12:56 PM]  
lol

[12:56]  
even after RSVP let's see how many people show up

[12:56]  
i work in Chelsea so I'm headed straight after work

sjsyrek [12:57 PM]  
I'll be peeved if people RSVP then don't show but don't cancel

sagar [12:57 PM]  
i can't wait for the paperback of the haskellbook to come out

[12:57]  
i can't stand learning from pdf's for some reason

sjsyrek [12:57 PM]  
You don't like having the PDF side by side with your terminal?

haskellandchill [12:57 PM]  
well ppl will RSVP and no show, did you allow a little slack (not Slack) for that?

sjsyrek [12:58 PM]  
No. Behance said 20 max because they have a dozen of their own doing it

[12:59]  
Will have to play wait and see then modify the strategy if necessary

[12:59]  
Question is how many people will stick it out to the end

[12:59]  
OK getting off for now. Phone is dying

sagar [1:03 PM]  
I do but sometimes i also just want to read all the way through

[1:03]  
and then "work" on it again

katychuang [1:06 PM]  
sorry if my question about why LC was offensive earlier. I wanted to know how it fit w/ haskell; wasn’t trying to be a “why should I buy in” thing

[1:06]  
Like, whether to take it conceptually or literally

haskellandchill [1:07 PM]  
it wasn’t offensive

[1:07]  
it is actually both conceptual and literal

katychuang [1:08 PM]  
okay, good. the answers were clarifying

haskellandchill [1:08 PM]  
you have to get the literal parts through exercises

[1:08]  
and the literal parts are directly translatable to haskell

[1:08]  
and will help you write type signatures and function definitions

[1:09]  
the conceptual parts come after, and can help you think about computation in general

katychuang [1:09 PM]  
conceptual parts are the big words, right?

[1:09]  
like alpha equivalence, beta reduction (edited)

janaipakos [1:10 PM]  
joined #general

haskellandchill [1:10 PM]  
nope

[1:10]  
well alpha equivalence

sagar [1:10 PM]  
beta reduction is a shmancy way of saying resolve this expression i.e. cut it down to size

[1:11]  
alpha equivalence is - is *!:@#x the same as jkl@$@x

haskellandchill [1:11 PM]  
lambda abstraction and beta reduction are fancy words for the literal parts

sagar [1:11 PM]  
imu

haskellandchill [1:11 PM]  
alpha equivalence is more conceptual, but approachable, it’s renaming

[1:12]  
abstraction is like adding a variable

[1:12]  
reduction is like evaluating a function

[1:12]  
but they both relate to steps you can do with symbols

[1:12]  
which is why the exercises are so key

[1:13]  
it’s like, addition with numbers, you reduce `1 + 2` into `3`

m [1:13 PM]  
alpha equivalence doesn't scream approachable imo

haskellandchill [1:13 PM]  
renaming is approachable

[1:13]  
change name `x` to `y`

[1:13]  
`x + 1` is alpha equivalent to `y + 1`

sagar [1:14 PM]  
YES

[1:14]  
woo

katychuang [1:14 PM]  
does anyone use this name “alpha equivalence” in real life? lol

sagar [1:15 PM]  
now you will :smile:

haskellandchill [1:15 PM]  
and for fun, lambda abstraction is taking `1` to `x + 1`

[1:15]  
I do, what is real life

sagar [1:15 PM]  
haha ^ was about to say the same

m [1:16 PM]  
i think it's that computer science/developer divide where they aren't necessarily one and the same

katychuang [1:16 PM]  
at walmart, checking out: “can this coupon be applied alpha equivalent to both shampoo and conditioner?"

haskellandchill [1:16 PM]  
haha try it

m [1:16 PM]  
:joy:

haskellandchill [1:16 PM]  
might have to bump up to target

sagar [1:16 PM]  
is this coupon alpha equivalent to this other coupon

katychuang [1:17 PM]  
targét

haskellandchill [1:17 PM]  
at Dean & DeLuca, certainly

[1:19]  
can you beta reduce my coupon into the appropriate discount?

[1:19]  
haha this is a good metaphor

katychuang [1:19 PM]  
"you beta reduce like it’s your function"

haskellandchill [1:20 PM]  
and rap songs

[1:20]  
making scary sounding things fun, that’s how you do math education :smile:
