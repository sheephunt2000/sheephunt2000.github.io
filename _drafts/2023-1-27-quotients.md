---
layout: post
title: What's a quotient?
author: Stephen Hu
date: 2023-1-27
categories: quotient
---

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

When someone goes through a pile of Skittles trying to separate it, we might go through one by one and place each one into smaller piles, each of one color. We can write one of these smaller piles as $\lbrace x\in\text{Skittles}\mid x\text{ is green} \rbrace$ or in other words, $\lbrace x\in\text{Skittles}\mid x\sim\text{a green Skittle} \rbrace$ . In general, this is known as an **equivalence class**. 

**Definition:** Given some element $a$ in $S$, the ***equivalence class*** under some equivalence relation $\sim$ is the set $\lbrace x\in S\mid x\sim a \rbrace$. It is denoted by $[a]$ or $\bar{a}$. 

**Examples:** The Skittles example from before. A mathematical example would be to consider congruence of shapes, which is an equivalence relation on the set of all shapes. An equivalence class of a shape $A$ would be the set of all shapes congruent to $A$. 

You might notice that this partitions the set into subsets. Let's introduce a separate concept. 

#### Partitions

**Definition:** A ***partition*** of a set $S$ is a collection of subsets of $S$, denoted by $P$, such that 

- none of the subsets are empty (i.e. $\varnothing\not\in P$)
- the union of all of the elements of $P$ equals $S$. In other words, $P$ *covers* $S$.  (i.e. $\bigcup_{A\in P}A=S$). (Recall that each element of $P$ is itself a subset of $S$.) 
- the elements of $P$ are disjoint from each other. (i.e. for $A,B\in P$, it is true that $A\cap B=\varnothing$.)

In other words, a ***partition*** of $S$ is a collection of non-empty subsets such that $S$ is the *disjoint union* of the subsets. 

**Examples:** If $S=\lbrace 1,2,3,4,5\rbrace$, then $P=\lbrace\lbrace 1,2 \rbrace,\lbrace 3 \rbrace,\lbrace 4,5 \rbrace\rbrace$ is a partition of $S$. If $S$ is a bag of Skittles, then the collection $$P=\lbrace\text{green Skittles}, \text{orange Skittles}, \text{yellow Skittles}, \text{red Skittles}, \text{purple Skittles}\rbrace$$ is a partition of $S$. 

You may have noticed that $P$ is simply the collection of equivalence classes of $S$ under the equivalence relation $\sim$ defined earlier. This is not a coincidence! 

**<u>Theorem:</u>** Equivalence relations and partitions are *the same thing*! More formally, given a set $S$, a partition $P$ of $S$ defines an equivalence relation on $S$, and an equivalence relation $\sim$ on $S$ defines a partition of $S$. 

**<u>Proof:</u>** Give this one a try on your own; it is not too complicated! I promise. Once you figure out what the appropriate partition or equivalence relation is, all that is needed is to verify the axioms. 

This is one of my favorite theorems in all of mathematics. It's a very fundamentally simple concept to state and to prove, but much of mathematics can be derived from this idea. This includes the idea of a quotient, which we can finally define. 

**Definition:** Given a set $S$ and an equivalence relation $\sim$, the ***quotient set of $S$ under $\sim$*** is the collection of all equivalence classes of $S$ under $\sim$. This partition is often denoted by $S/{\sim}$. 

#### Clock math

How can we use this idea to build some new math? Well, you may be familiar with the idea of *modular arithmetic*. For instance, if it's 11 PM and I ask you what time it'll be 6 hours from now, you'd say 5 AM. Implicitly, we're all familiar with doing math "mod 12," that is 

- motivation
- equivalence relations/partitions
- they're the same
- mod equivalence relation
- Z/nZ is an example of a....
- quotient group
- quotient vector space? quotient topological space? quotient modules? that into ideals? field of fractions?
- tensors???




[^1]: According to Wikipedia, the relation and the set together is called a [setoid](https://en.wikipedia.org/wiki/Setoid). I've never heard this terminology before, but it's really funny so I thought I'd at least mention it here. 