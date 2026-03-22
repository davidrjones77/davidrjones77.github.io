---
layout: post
title:  "Beyond the Strange"
date:   2026-03-19 08:25:15 -0400
categories: infinite_series, special_functions, analysis, dynamical_systems
katex: True
---
## Recap
In the last post we proved the convergence of the following sum, which is both infinite and infinitely recursive (see below).  
This sum is defined when $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$.<br>
For all such values $z$, this sum converges to 1.

$$\LARGE 1 = \sum^{\infty}_{a=0} \frac{z}{(z+a)\left(z+a\sum^{\infty}_{b=0} \frac{z}{(z+b)\left(z+b+\sum^{\infty}_{c=0} \frac{z}{(z+c)(z+c+...)}\right)}\right)}$$

<br>
## On Reflection (Recursion)?
Recall from the last post that the convegence of the strange sum was a consequence of applying a limiting argument to the following theorem (***<font color="purple">Corollary 1</font>*** in our last post).
> ***<font color="purple">Theorem 1</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin
> \Z_{\leq0}$.</font>
> <font color="black"><br><br> 
> Then $$\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}=1$$</font><br>

The observation was that since 1 appears twice in the equation, you can recurse the summation expression to arbitrary (in fact infinite) depth, to striking effect.

But let's face it - this is a bit of a parlor trick.<br>
For any convergent series whose expression contains its own value, we can re-write that expression as an infinite recursion.<br>

It is true that infinitely nested expressions are unusual in mathematics.<br>
Most that appear in textbooks diverge, or require careful considerations to make sense.<br>
But in this case, once you see how the trick is done, it appears to be just a curious and amusing puzzle - a way to perplex your friends and colleagues.

Is there anything more to say?<br>
As it turns out, yes - a lot more.

Let's start by observing that our strange sum takes an "outside-in" perspective - we start from ***<font color="purple">Theorem 1</font>*** and recurse inward.

Can we recurse outward?<br>
Sure - consider <center>$$T(w) = \sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+w)}.$$</center>

Our ***<font color="purple">Theorem 1</font>*** says $T(1) = 1$, and we can recurse outwardly with expressions of the form <center>$$...T(T(T(1)))...=1$$</center><br>
We know the value will always be 1, and a similar limiting argument shows that this holds in the infinite case.

We can think of 1 as a *fixed point* of $T(w),$ that is - an argument which the function gives back as an output.

<br>
## Enter the Digamma
One thing we did not point out in the last article is a curious coincidence having to do with the domain of our results: $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$.

It turns out the *Gamma* function and related *polygamma* functions also have this domain.<br>
Is that a coincidence?<br>
Well, let's see.




