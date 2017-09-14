Hello everyone and thank you all for being here.

I know all of you, but just in case, my name is Gaspar and I'll be talking about
the main points of my bachelor's thesis which I carried out in the past year.

This was done under the supervision of my former differential geometry professor, Xavier Gràcia.

Right now I'll briefly describe the idea behind SDG, but it's best
understood by actually seeing the theory developed, so I won't spend
much time on general explanations.

Now, I will say that a large part of the motivation behind SDG is
somewhat inaccessible to those not involved in *algebraic* geometry.
Since at least the beginning of the last century, algebraic geometry has
made its home within category theory. Many of the constructs in SDG
reflect those developments (toposes originated in alg. geo.). What I'm trying
to say is that what I'm about to describe as the goal of SDG is far from the
entire picture. One would need to study alg. geo. and cat. th. more intensively
to see that picture.

Nevertheless, we can say that SDG attempts to work with the classical
constructs of DG from an axiomatic standpoint. All of the backdrop of coordinate
frames is dropped, and we start directly with geometric considerations.

----

Without further ado, let us go through the structure of the talk.

We begin with some introductory theory. As anyone who will eventually study differential
geometry studies calculus, so we begin with single variable calculus.

Immediately we will run into problems interpreting the axioms naively.
There we describe why topos theory is necessary.

From there we make a big jump to microlinear objects, which will be our "manifolds".
As with classical manifolds, we'll construct the tangent bundle and, consequently, 
tangent vectors.

Now I know that you all know what a derivative is, but I'll include a description
just to give some context.

In particular, the interpretation that is useful to consider now is the one we see here.
We have a linear (affine) expression, followed by terms that decrease asymptotically as
"h" squared.

----

We'll now recreate that axiomatically. We begin with R, our smooth line. In case there's
any doubt, yes, R is intended to be the synthetic version of R.

So far we haven't said what R is. A precise definition will be given later. For now let
us require our first axiom, **R is a an algebra over Q**.

----

The next part is where things start to "synthetic".

Recall the idea of "negligible quadratic terms", or terms in the 1st degree Taylor
expansion which are "very small" for small increments. Instead we will posit the
existence of elements of R which actually square to zero.

In a ring, we can always define this set. In a field or more generally a domain,
it is always equal to the set with one element, that element being zero.

Our first axiom was rather simple, but this one will be more defining.
It's referred to as the Kock-Lawvere axiom, after Bill Lawvere and Anders Kock
both of whom are principle figures in the development of SDG. It says: \*read slide\*

That is, every map from D to R is linear, modulo a translation (we could say
that every... is affine). This represents the notion that elements of D are so small
that their increments can only produce linear changes.

----

We can now define derivatives. \*read slide\*. Notice, there's no restriction on f, we will comment on this later.

----

The KL axiom will imply that there exist unique a and b with...

\*read slide\*

This naturally leads to defining...

----

...giving us the first degree Taylor expansion, in synthetic terms.
F of x plus d is literally equal to...

You may (or even should) be thinking that, well, that's very nice and all,
but it's not very remarkable seeing as we just made it up. Furthermore, assuming
we could derive results (not new results, but perhaps derive them more elegantly)
in this "formal calculus", then there is still no link between them and the rest
of mathematics, in particular standard calculus.

We will address this problem later on. Very briefly, essentially what one needs to
do is to produce a *model* of the axioms within "normal" mathematics. What does that
mean? Well, for practical purposes we can say it means within ZF(C) set theory. This
is, after all, how we prove that any object-with-properties "exists" in mathematics.
When we say "let a group be..." we shortly after prove that the axioms are consistent
by producing an example of a group. In the case of SDG it's simply more complicated.

----

Back to derivatives, let's look at an easy example.

\*read slide\*

The terms with powers of d greater than or equal to two all vanish,
and we're left with the expression...

By uniqueness of b (blackboard?), f'(x) = nx^(n-1).

----

So, again, how are we able to do this? I mentioned earlier that we have to give a model
for the axioms, but the axioms themselves have also been stated in a somewhat
nebulous way. We'll now go into a *bit* more detail, but only slightly so.

First of all, we have to leave the category of sets. This is simply a fact - SDG
has no models in the category of sets (this has been proven). Of course,
it's not typical to mention explicitly, at least in classical geometry, that
one is working in the category of sets. But it is so. When we write things such as
"x belonging to A", these phrases can be interpreted in terms of morphisms
(which are just functions) in the category of sets.

We have to weaken logic to only constructive logic. We haven't done it but it's
a simple exercise to "prove" that R = 0, if the KL axiom holds. The catch is that
the crucial step in the proof assumes the truth of the law of the excluded middle,
or that for any prop. p, either p is true or not p is true.

Toposes are where we want to be, or more generally "cartesian closed categories".
Luckily, one can work in a topos very much in the same way as one works with sets.
This is what we are doing right now. Every phrase, formula, etc. has a meaning in
terms of the objects and morphisms of a topos (e.g. x\\in A).

In other words objects of a topos behave like sets. Indeed, one prime example of
a topos is the category of sets. I don't want to get into too much detail, but
I'll read a helpful quote from Anders Kock:

\*read quote slide\*

----

With that out of the way, let's move on to some more interesting geometry.
The goal of this last part of the talk is to define microlinear objects,
and see how they are like abstracted versions of manifolds.

Again, here the fully precise definition of microlinearity requires many
categorical preliminaries and definitions. Instead we look at one consequence
that will be of use here. It starts with defining "2-infinitesimals".
We define them because, a priori, there is no reason to believe that
the product of two infinitesimals is always zero. This is a problem,
because it means that the sum of two infinitesimals is not an infinitesimal
(which aligns with intuition, no matter how small something is surely by adding
it enough times you will get somewhere).

(blackboard?)

----

The property of microlinear objects that we are interested in is the following.

\*read slide\*

In fact, in Kock's book a slightly generalized version of this (n vars.) was
given as microlinearity, and it was called "infinitesimal linearity". Every map
from a tiny enough set (hence "micro") is linear, in the sense that it is defined
by it's values on the axes or on "basis elements".

----

So, back to microlinear objects. They are the new "manifolds", and one way in which
this is reflected is that we can talk about tangent vectors, and they do form a vector
space.

----

Synthetic tangent vectors are... well, I find them quite elegant, because *classically*
they are equivalence classes of paths (one version of them) through a point which
have the same velocity. In this case, our "interval" is so small, that each path defines
a single tangent vector.

\*read slide\*

They are literally infinitesimal paths through p. That which we always think of is true
in this language. This has more consequences as we'll refer to shortly.

For now, the tangent space at p is defined as the set of all tangent vectors to p.

----

Each T_pM is an R-module, given by the following.

\*read slide\*

To define the sum of two tangent vectors, we need to invoke microlinearity.

\*read slide\*

Thus, the sum of t_1 and t_2 is simply the action of following each of them
in equal part. A linear combination such as (blackboard) is following t_1, and
t_2 twice as fast.

These operations define a module structure, but obviously we won't go through
all of the details. One proof we will carry out is proving that the zero we mentioned
is in fact the neutral element, because it highlights yet again the role of microlinearity

----

\*read slide\*

----

With that we may move on to the tangent bundle, which as one expects if
they're coming from geometry, is just the collection of all tangent spaces.
In other words, it is the set of all functions from D to M.

Since it is the tangent *bundle*, it has a projection onto the original space
given by...

----

Moving on, we define vector fields in the most natural way possible which is
as sections of the previously defined tangent bundle. \*read slide\*

Two things: \*read slide\*

----

Our final examination of the theory of SDG will be that of flows (induced by
vector fields). Recall that (classic flow def. on blackboard). Keep that there
for now.

A quick reminder on function sets:

\*read slide\*

----

The tangent bundle is just a function set, and by the property we just mentioned,
a vector space is equivalent to a map...

Writing the same symbol is technically an abuse of notation, but it's extremely
common and very convenient.
