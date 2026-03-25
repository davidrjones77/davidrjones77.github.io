---
layout: post
title:  "Beyond the Strange"
date:   2026-03-19 08:25:15 -0400
categories: infinite_series, special_functions, analysis, dynamical_systems
katex: True
---
## Recap
Our last post concluded with the following strange result:
> ***<font color="purple">Corollary 3</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$.</font><br>
> <font color="black">Then for finite recursion depth and infinite recursion depth with $\omega=1$ $$\LARGE 1=\sum^{\infty}_{a=0}
> \frac{z}{(z+a)\left(z+a+\sum^{\infty}_{b=0}
> \frac{z}{(z+b)\left(z+b+\sum^{\infty}_{c=0}
> \frac{z}{(z+c)(z+c+...)}\right)}\right)}$$</font>

The *omega point* ($\omega = 1$) condition of the infinite case corresponded to a hidden projective point obtained by extending the recursion process used in the proof of the finite case.<br>
Essentially, we took the abritrary finite case and extended it to an "infinite horizon," where the vanishing point at infinity corresponded to the value of the infinite series treated recursively, viz. the value 1.<br><br>
But questions remained.<br>
Is  $\omega = 1$ unique?<br>
Can we analyze this more systematically?

<br>
## On Reflection (Recursion)?
Recall from the last post that ***<font color="purple">Corollary 3</font>*** was a consequence of applying a limiting argument to ***<font color="purple">Corollary 1</font>***, which was stated as follows:
> ***<font color="purple">Corollary 1</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin
> \Z_{\leq0}$.</font>
> <font color="black"><br><br> 
> Then $$\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}=1$$</font><br>

Our "omega point" observation is hinting that we are looking at things the wrong way around.

What if we recurse outward instead of inward?<br>
Consider <center>$$T(\omega) = \sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+\omega)}.$$</center>

Our ***<font color="purple">Corollary 1</font>*** says $T(1) = 1$, and we can recurse outwardly with expressions of the form <center>$$...T(T(T(1)))...=1$$</center><br>
We know the value will always be 1, and a similar limiting argument shows that this holds in the infinite case.<br>
Let's give the proof of this.

We can think of 1 as a *fixed point* of $T(w),$ that is - an argument which the function gives back as an output.

<br>
## Enter the Digamma
One thing we did not point out in the last article is a curious coincidence having to do with the domain of our results: $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$.

It turns out the *Gamma* function and related *polygamma* functions also have this domain.<br>
Is that a coincidence?<br>
Well, let's see.




