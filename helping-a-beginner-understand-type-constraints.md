
newmountain [2:42 PM]  
Would it be possible for someone to walk me through this code line by line?

[2:42]  
 ```
import Control.Monad.State
fib n = flip evalState (0,1) $ do
  forM [0..(n-1)] $ \_ -> do
    (a,b) <- get
    put (b,a+b)
  (a,b) <- get
  return a
```

[2:43]  
I really want to wrap my head around the state monad and I’m having trouble connecting haskellbook to real world use cases speficially for the monad chapters (state, reader, and transformers).

[2:44]  
So I am looking for some dead-simple examples and applications of each.

[2:44]  
Background is Python and NodeJS dev who has written a decent amount of Elm code.

[2:46]  
I got it from the haskell wiki and it’s supposed to be the haskell version of this python code:
```
{- def fib(n):
      a, b = 0, 1
      for _ in xrange(n):
          a, b = b, a + b
      return a  -}
```

[2:48]  
An explanation of flip evalstate puts and gets for a five year old would be very much appreciated. :wink:

[3:07]  
So evalState takes a State s a -> s -> a

[3:08]  
Which in this example:
```
import Control.Monad.State
fib n = flip evalState (0,1) $ do
  forM [0..(n-1)] $ \_ -> do
    (a,b) <- get
    put (b,a+b)
  (a,b) <- get
  return a
```

[3:08]  
Is just a vanilla tuple that we wrap into a state monad?

[3:09]  
Even more basic question, from where should I start reading this. I understand the lines, but no idea how they execute.

haskellandchill [3:09 PM]  
well maybe try the type signature first

[3:10]  
give `fib :: ?`

[3:10]  
evalState does more than just wrap the tuple

[3:11]  
> Evaluate a state computation with the given initial state and return the final value, discarding the final state.

[3:11]  
from looking it up in hasekell.org/hoogle

newmountain [3:12 PM]  
I’m sorry. Looking at types still doesn’t help me understand what’s going on as I learn these things.

haskellandchill [3:12 PM]  
ok so first, what is the type of `fib`?

newmountain [3:12 PM]  
I know that’s sacrilege in the Haskell community and I apologize.

haskellandchill [3:13 PM]  
you use `n` with `n-1`

newmountain [3:13 PM]  
Right, so fib takes a Num which gets fed into the for loopish thing.

haskellandchill [3:14 PM]  
so let’s start with that

[3:14]  
`fib :: Num n => n -> …`

newmountain [3:14 PM]  
forM :: (Monad m, Traversable t) => t a -> (a -> m b) -> m (t b)

haskellandchill [3:14 PM]  
woa don’t get ahead of yourself

newmountain [3:14 PM]  
Got it.

[3:14]  
Ok

haskellandchill [3:15 PM]  
what does `fib` return?

[3:15]  
and I don’t mean the monad `return`

newmountain [3:15 PM]  
a num n?

[3:15]  
I’m trying to type it into ghci now.

haskellandchill [3:15 PM]  
so `fib :: Num n => n -> n`

newmountain [3:16 PM]  
Yes.

haskellandchill [3:16 PM]  
now how does that constrain the monad you are using?

newmountain [3:16 PM]  
Confirming in editor, but that is my expectation.

haskellandchill [3:16 PM]  
`evalState :: State s a -> s -> a` that’s the function you are returning as `n` (edited)

[3:17]  
so `evalState :: Num n => State s n -> s -> n` and you can keep attacking the problem piece by piece

[3:21]  
make sure you understand the distinction between value `n` in `fib n` and type level `Num n` we are talking about

newmountain [3:24 PM]  
fib :: (Enum a, Num c, Num a) => a -> c

[3:24]  
Let’s pass in a 6 for argument’s sake.

[3:25]  
flip will operate on evalState (0,1). evalState (0,1) is curried and waiting for a second argument from the $ do.

[3:26]  
do puts it into a monad context.

[3:27]  
forM takes a traversable a (a list from 0 ..(n-1) - in this case 6 and a function which is curried waiting for a second argument from the $ do.

[3:27]  
and that function is get an (a,b) and put a (b, a+b) back.

[3:28]  
then get that (a,b) tuple and return the a.

[3:28]  
give that to evalState and flip it (take the a).

[3:29]  
Is that a correct understanding of what is going on?

haskellandchill [3:41 PM]  
`fib :: (Enum a, Num c, Num a) => a -> c` where did you get this?

[3:42]  
`flip evalState s` will take the `State s a` from the `do` block (edited)

[3:43]  
ghc will infer the most general type signature, that’s not always helpful

[3:43]  
it’s often nicer to write your own type signature to simplify

newmountain [3:45 PM]  
I got that from ghci

[3:46]  
I can put a type header on it myself to constrain further. It should just be Num a => a -> a

[3:48]  
I recompiled with header: fib :: (Enum a, Num a) => a -> a

[3:50]  
the enum seems to come from the list generator
```:t \x -> [0..x]
\x -> [0..x] :: (Enum t, Num t) => t -> [t]
```

haskellandchill [3:50 PM]  
yeah you can just pick a concrete type

[3:50]  
like `Int`

newmountain [3:50 PM]  
Ok

haskellandchill [3:51 PM]  
`Int` has instances for typeclasses `Enum` and `Num`

newmountain [3:51 PM]  
Cool. So now
```fib :: Int -> Int ```

haskellandchill [3:52 PM]  
give me the signature for `flip evalState`

[3:52]  
that’s your next step, with the concrete types filled in based on the tuple you use

newmountain [3:53 PM]  
```:t (flip evalState (0,1) )
(flip evalState (0,1) ) :: (Num t, Num t1) => State (t, t1) c -> c```

haskellandchill [3:54 PM]  
same thing, let’s use `Int` instead of `Num` typeclass

newmountain [3:54 PM]  
Right so :: State(Int, Int) a -> a

haskellandchill [3:55 PM]  
and you know what `a` is

newmountain [3:55 PM]  
so (0,1) is just a throwaway plug?

haskellandchill [3:55 PM]  
because you are returning it and you know what fib returns

[3:55]  
it’s your state

[3:55]  
you are using a tuple as state

newmountain [3:55 PM]  
Got it.

[3:56]  
But in reading through haskellbook, it seems like state is always a tuple?

haskellandchill [3:56 PM]  
you need to do all the excercices in haskellbook

[3:56]  
you must have gotten ahead of yourself because you don’t understand polymorphism

[3:56]  
`State s a`, `s` is polymorphic

[3:57]  
it’s not “always a tuple"

[3:57]  
you can specialize it to be a tuple

[3:57]  
or whatever

newmountain [3:57 PM]  
I know I do. It’s just hard to stay motivated as the advanced chapters become increasingly detached from reality. I’m trying to connect it to something real so it will stick.

haskellandchill [3:57 PM]  
GO TO JAIL: Go directly to Jail. Do not pass Go. Do not collect $200.

newmountain [3:58 PM]  
I’m sorry. I’m not worthy.

haskellandchill [3:58 PM]  
it’s not about being worthy (edited)

[3:59]  
I just spent a good chunk of time helping you, and I expect you to put in the work

newmountain [3:59 PM]  
I will. I appreciate your time and I will put in more work. (edited)
