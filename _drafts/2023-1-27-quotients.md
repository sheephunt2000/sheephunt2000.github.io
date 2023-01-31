##	What's a quotient?

There's a lot of theorems that I've learned through my time as an undergraduate. One of my favorites, however, is still the one which taught me what a quotient is. Quotienting is one of those ideas which appears everywhere in math, but it's pretty confusing if you've never seen it before. I remember I tried learning about quotient groups for *ages* before it finally clicked, since it's a very subtle idea. 

####	What does it mean for things to be equal?

There was a kerfuffle on Twitter a while ago about how $2+2=4$ is not necessarily true. To most people, it probably seems like something obvious, and questioning things like this seems like questioning whether the Earth is round. However, it's not as obvious as it looks! Equality can be a nebulous concept if you really think about it. (Inspiration for the following comes from [this Reddit post.](https://www.reddit.com/r/learnmath/comments/1v4ktu/comment/ceoq3r1/?context=3)) Let's begin with a definition. 

**Definition: ** A relation $\sim$ on a set $S$ is called an ***equivalence relation***[^1] if it is 

- *reflexive*: for all $a\in S$, we have that $a\sim a$. 
- *symmetric*: for all $a,b\in S$, if $a\sim b$, then $b\sim a$. 
- *transitive*: for all $a,b,c\in S$, if $a\sim b$ and $b\sim c$, then $a\sim c$. 

Why is this important? Well, we want to capture some notion of two objects being "the same," even if they're not necessarily "equal." For instance, "is in the same grade" is an equivalence relation on the set of all Rutgers students. More formally, if we let $S$ be the set of all Rutgers students, we can say $A\sim B$ if students $A$ and $B$ are in the same grade. It is true that $\text{Stephen}\sim\text{Kevin}$, but $\text{Stephen}\not\sim\text{Enver}$.  Likewise, "is the same color" is an equivalence relation on the set of all Skittles. (Verify for yourself that both of these follow the axioms!) This is something that picky eaters often care about when eating Skittles. 

![organized skittles](https://i.redd.it/09e4dt426um51.jpg)

*A partition of Skittles*

When someone goes through a pile of Skittles trying to separate it, we might go through one by one and place each one into smaller piles, each of one color. This means that 

- motivation
- equivalence relations/partitions
- they're the same
- mod equivalence relation
- Z/nZ is an example of a....
- quotient group
- quotient vector space? quotient topological space? quotient modules? that into ideals? field of fractions?
- tensors???




[^1]: According to Wikipedia, the relation and the set together is called a [setoid](https://en.wikipedia.org/wiki/Setoid). I've never heard this terminology before, but it's really funny so I thought I'd at least mention it here. 