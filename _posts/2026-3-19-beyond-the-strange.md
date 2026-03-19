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
## Reflection
Recall from the last post that the convegence of the strange sum was a consequence of applying a limiting argument to the following theorem (***<font color="purple">Corollary 1</font>*** in our last post).
> ***<font color="purple">Theorem 1</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin
> \Z_{\leq0}$.</font>
> <font color="black"><br><br> 
> Then $$\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}=1$$</font><br>
