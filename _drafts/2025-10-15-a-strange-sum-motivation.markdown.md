---
layout: post
title:  "A Strange Sum - Motivation"
date:   2025-10-15 20:09:15 -0400
categories: infinite_series
---

Recall in the last post, I presented a strange sum (see below).
Are there values of omega for which this expression is mathematically defined?
If so, for which values of omega does this sum converge?
$$\LARGE \sum^{\infty}_{a=0} \frac{\color{red}\Omega}{(\color{red}\Omega\color{black}+a)\left(\color{red}\Omega\color{black}+a\sum^{\infty}_{b=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+b)\left(\color{red}\Omega\color{black}+b+\sum^{\infty}_{c=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+c)(\color{red}\Omega\color{black}+c+...)}\right)}\right)}$$
Let's call this sum $\sum^\infty_\Omega$.

### Motivation
Where did this expression come from?
I was initially interested in a much simpler question.

***Simple Question:*** *When can we express the reciprocal of a whole number as a sum of reciprocals of whole numbers?*

In other words, for which whole numbers $n$ can we write $\frac{1}{n}=\frac{1}{n'}+\frac{1}{n''}$?
(Here, $n'$ and $n''$ are also whole numbers.)

The first thing you might notice is $\frac{1}{1}=\frac{1}{2}+\frac{1}{2}$.
So far, so good!

Continuing the pattern, you might try  $\frac{1}{2}=\frac{1}{3}+x$ and solve for $x.$
We have   $$\begin{align*}
&& x&=\frac{1}{2}-\frac{1}{3} \\  \\
\rightarrow && x&=\frac{3}{6}-\frac{2}{6} \\ \\
\rightarrow && x&=\frac{1}{6} \\ \\
\rightarrow && \frac{1}{2}&=\frac{1}{3}+\frac{1}{6}\\ \\
\end{align*}$$ Thus $\frac{1}{2}=\frac{1}{3}+\frac{1}{6}$, and continuing this approach we find $\frac{1}{3}=\frac{1}{4}+\frac{1}{12}$.


It would seem at this point we can conjecture an answer to our ***Simple Question.***

***Conjecture 1***
Let $n \in \mathbb{N}$, where $n \neq 0$. 

Then $$\frac{1}{n} = \frac{1}{n+1} + \frac{1}{n(n+1)}$$
***Proof***
  $$\begin{align*}
 \frac{1}{n} &= \frac{1(n+1)}{n(n+1)} = \frac{n + 1}{n(n+1)}  = \frac{n}{n(n+1)} + \frac{1}{n(n+1)} =  \frac{1}{n+1} + \frac{1}{n(n+1)}
\end{align*}$$







<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc5ODc5NjExMiwxNzY1MDc4NjYxLDQ5OT
Q5ODU0NiwtMjA3MDEwNSw5NjM5NzA2ODEsMTQyMjgzMDIxMV19

-->