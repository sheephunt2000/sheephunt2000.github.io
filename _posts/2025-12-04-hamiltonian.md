---
layout: post
title: Random Facts 12/4/2025
slug: random-fact-12-4-2025
author: Iris Hu
date: 2025-12-04
categories: [til, grouptheory]
katex: true
---

Today was a good day - had a good brunch at [Madras Mantra](https://madrasmantra.com/) in Decatur, and went to Costco with a friend who got his very first membership! Mostly I wanted to talk about two interesting things I found out tonight while online that I'd like to write down for the benefit of no-one in particular. This is meant to be short, but we'll see what happens. 

## Fact 1: FTA through...what?

There's an aphorism misquoting Voltaire about the [fundamental theorem of algebra](https://en.wikipedia.org/wiki/Fundamental_theorem_of_algebra); mainly that it is neither truly fundamental, nor one of algebra. Indeed, all proofs that I'm aware of seem to appeal to some "non-algebraic" techniques. In undergrad, I saw proofs of this theorem in real analysis, complex analysis, algebraic topology, and differential topology. It was a recurring meme (theme?) in all of my courses. 

A natural question to ask is how algebraic can we make such a proof? Ian Stewart, in Chapter 23 of his Galois theory textbook, outlines a proof which I just discovered today. Here is the preface of this chapter. 

> In Chapter 2 we proved the Fundamental Theorem of Algebra, Theorem 2.4, using some basic point-set topology and simple estimates. It is also possible to give an 'almost' algebraic proof, in which the only extraneous information required is that every polynomial of odd degree over $\mathbb R$ has a real zero. This follows immediately from the continuity of polynomials over $\mathbb R$ and the fact that an odd degree polynomial changes sign somewhere between $-\infty$ and $+\infty$.
>
> We now present this almost-algebraic proof, which applies to a slight generalisation. The main property of $\mathbb R$ that we require is that $\mathbb R$ is an ordered field, with a relation $\leq$ that satisfies the usual properties. So we start by defining an ordered field. Then we develop some group theory, a far-reaching generalisation of Cauchy's Theorem due to the Norwegian mathematician Ludwig Sylow, about the existence of certain subgroups of prime power order in any finite group. Finally, **we combine Sylow's Theorem with the Galois correspondence to prove the main theorem, which we set in the general context of an 'algebraically closed' field.** (bolding mine)

Using Sylow theory and the Galois correspondence to prove FTA is probably the funniest thing I've ever heard of. Honestly, I wish I had heard about this in my time taking undergraduate algebra; this would've made an awesome final project. The Sylow theorems were the mic drop of finite group theory (Math 451) and Galois theory was the mic drop of field theory (Math 452). Using both of these to prove FTA? Sure, why not. 

The main outline of the proof is this: Stewart actually proves the following more general result. 

> **Theorem 23.12.** Let $K$ be an ordered field in which every positive element has a square root and every odd-degree polynomial has a zero. Then $K(i)$ is algebraically closed, where $i^2=-1$.

Since $\mathbb R$ satisfies these properties via some basic real analysis, we have our result. The only Sylow theorem that is actually needed in the proof is of the existence of a Sylow $p$-subgroup, which is used in the proof of the key lemma: 

> **Lemma 23.11.** Let $K$ be a field of characteristic zero, such that for some prime $p$ every finite extension $M$ of $K$ with $M\neq K$ has $[M:K]$ divisible by $p$. Then every finite extension of $K$ has degree a power of $p$. 

While this is a nice proof, the F in FTA seems admittedly even more suspicious.... these are highly non-trivial results!

(Stewart attributes this proof to Dedekind, with gaps which he fills via Galois theory.) 

## Fact 2: Normal subgroups are weird

It's a standard fact that all subgroups of an abelian group are normal. (No difference between a left and a right coset if everything commutes!) I wondered if the converse were true: if a group $G$ has only normal subgroups, is it abelian? This felt too good to be true, so I asked this out loud to my friend Sangjun. (I wondered if this were a silly question....) As Sangjun would tell me, it turns out this is actually not a silly question; the answer is no! Non-abelian groups which have all normal subgroups are called **Hamiltonian groups**. The easiest example of such a group, which were first studied by Dedekind in 1897, is the [quaternion group](https://en.wikipedia.org/wiki/Quaternion_group) $Q_8$. (Hence why Dedekind named this class of groups after the inventor of quaternions, William Rowan Hamilton.) Dedekind proved that all Hamiltonian groups contain $Q_8$ as a subgroup, and a few decades later Baer provided a complete classification: 

> **Theorem ([Baer, 1933](https://doi.org/10.1515/9783111561769-004)).** Every Hamiltonian group $G$ is of the form $$G=Q_8\times(\mathbb Z/2)^k\times D$$ for some non-negative integer $k$, where $D$ is a torsion abelian group with all elements of odd order. 

(Paywalled link, but can be bypassed via the usual means.) 

So in a sense, $Q_8$ is the "only" such non-abelian group with all normal subgroups; any other such group can be built out of $Q_8$ by adding on some abelian torsion, but not any additional non-abelian "components." 
