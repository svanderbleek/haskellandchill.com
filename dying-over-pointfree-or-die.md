Sandy Vanderbleek [5:12 PM]  
@amar47shah it’s really trippy that `sum . map :: (Num [b], Foldable ((->) [a])) => (a -> b) -> [b]`

[5:12]  
that part of your talk violated my intuition, I know my intuition is wrong but still puzzling it out

Sandy Vanderbleek [5:38 PM]  
```sum :: (Num a, Foldable t) => t a - > a
map :: (a' -> b') -> [a'] -> [b']
. :: (a'' -> b'') -> (b'' -> c) -> (a'' -> c)
```
creates constraints
```t a ~ b''
a ~ c
((->) [a']) ~ b'' — the crazy part
```
(edited)

[5:40]  
then sum becomes
```((->) [a'] -> [a']
```
which I didn’t know `[]` has a num instance, but I suppose it is `length`

