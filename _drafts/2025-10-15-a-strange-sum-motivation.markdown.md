---
layout: post
title:  "A Strange Sum - Motivation"
date:   2025-10-15 20:09:15 -0400
categories: infinite_series
---
# A Strange Sum - Motivation
## Recap
In the last post, I presented a strange sum (see below).
Are there values of omega for which this expression is mathematically defined?
If so, for which values of omega does this sum converge?
$$\LARGE \sum^{\infty}_{a=0} \frac{\color{red}\Omega}{(\color{red}\Omega\color{black}+a)\left(\color{red}\Omega\color{black}+a\sum^{\infty}_{b=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+b)\left(\color{red}\Omega\color{black}+b+\sum^{\infty}_{c=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+c)(\color{red}\Omega\color{black}+c+...)}\right)}\right)}$$

## Motivation
Where does this expression come from?
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
 \frac{1}{n} = \frac{1(n+1)}{n(n+1)} = \frac{n + 1}{n(n+1)}  = \frac{n}{n(n+1)} + \frac{1}{n(n+1)} =  \frac{1}{n+1} + \frac{1}{n(n+1)} \ \ \ \blacksquare
\end{align*}$$
So we have an answer to our ***Simple Question*** - *the reciprocal of any whole number $n$ can be expressed as the sum of reciprocals of whole numbers.*
Moreover, we now know a formula for that sum - our curiosity has rewarded us with information we weren't initially looking for.

But hang on - is there anything special about the 1 in the numerator?
And did our proof take advantage of anything intrinsic to whole numbers?
In other words, we should be able to generalize our result (taking care to restrict $b$ to prevent division by zero).
Let's do that.

***Theorem 1***
Let $a, b \in \mathbb{C}$, where $b \notin \{-1, 0\}$. 

Then $$\frac{a}{b} = \frac{a}{b+1} + \frac{a}{b(b+1)}$$

***Proof***
  $$\begin{align*}
 \frac{a}{b} &= \frac{a(b+1)}{b(b+1)} = \frac{ab + a}{b(b+1)}  = \frac{ab}{b(b+1)} + \frac{a}{b(b+1)} =  \frac{a}{b+1} + \frac{a}{b(b+1)} \ \ \ \blacksquare
\end{align*}$$

### Expanding Terms
But why stop at two terms?
After all, the terms on the right hand side of ***Theorem 1*** are just fractions having complex numbers as numerator and denominator, and so may be expanded according to ***Theorem 1***.
We should be able to expand terms on the right hand side of ***Theorem 1*** as many times as we like, and we know the form such terms should take.
Can we generalize ***Theorem 1*** to a sum of $n$ terms, where $n$ is a whole number?

 ***Corollary 1***
Let $n \in \N_{\geq1}.$
Let $a, b \in \mathbb{C}$, where $b \notin \{-m \vert m \in \N_{0\leq n}\}$. 

Then $$\frac{a}{b} = \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}$$

***Proof***
We give a proof by induction.

Let $P(n)$ be the claim $\frac{a}{b} = \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}.$

<font color="blue">*Base case:*</font>
Letting $n=1,$ we have by ***Theorem 1*** 
 $$\begin{align*}
 &&\frac{a}{b} &= \frac{a}{b+1} + \frac{a}{b(b+1)} \\ \\
 \rightarrow && \frac{a}{b} &= \frac{a}{b+1} + \sum^0_{i=0} \frac{a}{(b+i)(b+i+1)} \\ \\
  \rightarrow && \frac{a}{b} &= \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)} 
 \end{align*}$$ 

 Thus $P(1)$ is true. 
 \
\
<font color="blue">*Inductive step:*</font>
 Assume $P(n)$ is true for some fixed, arbitrary $n.$

Then by the <font color="red">inductive hypothesis</font> and <font color="blue">***Lemma 1.3.9***</font>, 
 $$\begin{align*}
 && \sum^{(n+1)-1}_{i=0} \frac{a}{(b+i)(b+i+1)} &= \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)} + \color{blue}{\frac{a}{(b+n)(b+n+1)}} \\ \\
 \rightarrow && \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &= \color{red}{\sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}} \color{black}{+} \color{blue}{\frac{a}{b+n}- \frac{a}{b+n+1}} \\ \\
 \rightarrow && \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &= \color{red}{\frac{a}{b}- \frac{a}{b+n}} \color{black} + \frac{a}{b+n}- \frac{a}{b+n+1} \\ \\ 
  \rightarrow && \frac{a}{b}  &=  \frac{a}{b+n+1}+  \sum^{(n+1)-1}_{i=0} \frac{a}{(b+i)(b+i+1)} \\ \\
 \end{align*}$$

 Thus $P(n)$ is true for all $n \geq 1$.








<!--stackedit_data:
eyJoaXN0b3J5IjpbNTgxNTI2Nzg2LDIwNzMxMjU3ODYsLTEzMj
Y0NTc4NTIsNzYzOTIyNTM0LDE3NjUwNzg2NjEsNDk5NDk4NTQ2
LC0yMDcwMTA1LDk2Mzk3MDY4MSwxNDIyODMwMjExXX0=
-->