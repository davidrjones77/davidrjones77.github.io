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

> <font color="purple"> ***Simple Question:***  <font color="black">*When can we express the reciprocal of a whole number as a sum of reciprocals of whole numbers?*

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


It would seem at this point we can conjecture an answer to our  <font color="purple">***Simple Question.***

><font color="purple">  ***Conjecture 1***
><font color="black">  Let $n \in \mathbb{N}$. 
> <font color="black"> 
> Then $$\frac{1}{n} = \frac{1}{n+1} + \frac{1}{n(n+1)}$$
> <font color="purple"> ***Proof*** 
> <font color="black">  $$\begin{align*}  \frac{1}{n} = \frac{1(n+1)}{n(n+1)} = \frac{n + 1}{n(n+1)}  = \frac{n}{n(n+1)} + \frac{1}{n(n+1)} = 
> \frac{1}{n+1} + \frac{1}{n(n+1)}  \end{align*}$$

So we have an answer to our  <font color="purple"> ***Simple Question*** -  <font color="black">*the reciprocal of any whole number $n$ can be expressed as the sum of reciprocals of whole numbers.*
Moreover, we now know a formula for that sum - our curiosity has rewarded us with information we weren't initially looking for.

But hang on - is there anything special about the 1 in the numerator?
And did our proof take advantage of anything intrinsic to whole numbers?
In other words, we should be able to generalize our result (taking care to restrict $b$ to prevent division by zero).
Let's do that.

> <font color="purple"> ***Theorem 1*** 
> <font color="black"> Let $a, b \in \mathbb{C}$, where $b \notin \{-1, 0\}$. 
> <font color="black"> 
> Then $$\frac{a}{b} = \frac{a}{b+1} + \frac{a}{b(b+1)}$$
> <font color="purple">  ***Proof*** 
> <font color="black">   $$\begin{align*}  \frac{a}{b} &= \frac{a(b+1)}{b(b+1)} = \frac{ab + a}{b(b+1)}  = \frac{ab}{b(b+1)} + \frac{a}{b(b+1)} = 
> \frac{a}{b+1} + \frac{a}{b(b+1)} \end{align*}$$

## Expanding Terms
But why stop at two terms?
After all, the terms on the right hand side of  <font color="purple">***Theorem 1***  <font color="black">are just fractions having complex numbers as numerator and denominator, and so may be expanded according to  <font color="purple">***Theorem 1***.
 <font color="black">We should be able to expand terms on the right hand side of  <font color="purple">***Theorem 1***  <font color="black">as many times as we like, and we know the form such terms should take.

Let's generalize  <font color="purple">***Theorem 1*** <font color="black"> to a sum of $n$ terms, where $n$ is a whole number.
Again, we must restrict $b$ to prevent division by zero.

We use the notation $\N_{0\leq n}$ to indicate the set of  non negative integers from $0$ to $n$, for some $n \in \N$.

>  <font color="purple"> ***Theorem 2***
>  <font color="black"> Let $n \in \N.$ Let $a, b \in \mathbb{C}$, where $b \notin \{-m \vert m \in \N_{0\leq n}\}$. 
> <font color="black"> 
> Then $$\frac{a}{b} = \frac{a}{b+n} + \sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)}$$
> <font color="black"> 
>  <font color="purple">***Proof***
> <font color="black"> We give a proof by induction.
> <font color="black"> 
> Let $P(n)$ be the claim $\frac{a}{b} = \frac{a}{b+n} +
> \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}.$
> 
> <font color="blue">*Base case:*</font> <font color="black"> Letting $n=1,$ we have by  <font color="purple">***Theorem 1*** <font color="black">   $$\begin{align*}  &&\frac{a}{b} &= \frac{a}{b+1} + \frac{a}{b(b+1)} \\ \\  \rightarrow && \frac{a}{b} &= \frac{a}{b+1} +
> \sum^0_{i=0} \frac{a}{(b+i)(b+i+1)} \\ \\   \rightarrow && \frac{a}{b}
> &= \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}  
> \end{align*}$$  <font color="black">   Thus $P(1)$ is true.   
>  
>  <font color="blue">*Inductive step:*</font>  <font color="black"> Assume $P(n)$ is true for some fixed, arbitrary $n.$
> <font color="black">  
> Then by <font color="purple">***Theorem 1***</font> and the <font
> color="red">inductive hypothesis</font>,   $$\begin{align*}  &&
> \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &= \sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} + \frac{a}{(b+n)(b+n+1)} \\ \\  \rightarrow &&
> \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &=\sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \color{black}{+} \color{purple}{\frac{a}{b+n}-
> \frac{a}{b+n+1}} \\ \\  \rightarrow && \sum^{n}_{i=0}
> \frac{a}{(b+i)(b+i+1)} &= \color{red}{\frac{a}{b}- \frac{a}{b+n}}
> \color{black} + \frac{a}{b+n}- \frac{a}{b+n+1} \\ \\    \rightarrow &&
> \frac{a}{b}  &=  \frac{a}{b+n+1}+  \sum^{(n+1)-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\   \rightarrow && &P(n+1)  \end{align*}$$
> <font color="black"> Thus $P(n)$ is true for all $n \geq 1$.

## Taking a Limit

But why stop at $n$ terms?
If we can expand our sum to *arbitrarily* (i.e. *fintely*) many terms, surely we can expand to *infinitely* many terms.

With fractions having real numerators and denominators, this would be straightforward.
But we'd rather not lose generality - we'd like to expand our sum to infinitely many terms while staying within the more general domain of complex numbers.

So let's take a limit at infinity while staying within the domain of complex numbers.
We'll need to use two facts about complex limits, which are proved in the **Appendix** at the end of this post.

> <font color="purple">  ***Theorem 3***
>   <font color="black">Let $a, b \in \mathbb{C}$, where $b \notin
> \Z_{\leq0}$. 
> <font color="black">  
> Then $$\frac{a}{b} = \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}$$
> 
> <font color="purple"> ***Proof*** 
>  <font color="black">By the definition of infinite series and limits, and by  <font color="purple">***Theorem 2***,  <font color="black"> we have  $$\begin{align*}   \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}&=\lim_{n \to \infty}\sum^{n}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\   &=\lim_{n \to \infty}\sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\  &=\lim_{n \to \infty}\left[\frac{a}{b} -
> \frac{a}{b+n} \right] \\ \\   \end{align*}$$ <font color="black">  But by  <font color="purple">***Lemma A.2 (see Appendix)***  <font color="black">$$\lim_{n \to \infty}
> \left|\frac{a}{b+n}\right|=0$$ and by  <font color="purple">***Lemma A.3 (see Appendix)*** <font color="black">
> $$\lim_{n \to \infty} \left|\frac{a}{b+n}\right|=0 \iff \lim_{n \to
> \infty} \frac{a}{b+n}=0$$ and so $$\lim_{n \to
> \infty}\left[\frac{a}{b} - \frac{a}{b+n} \right]=\frac{a}{b}$$ thus
> $$\frac{a}{b} = \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}$$

## Special Cases
Where does this leave us?

***Theorem 3*** tells us that the ratio of any 2 complex numbers can be expressed as an infinite series, and gives us the form of that infinite series.

Although the theorem restricts $b$ from being a non-positive integer, this is not a problem, since $\frac{a}{b}$ can always be expressed as $\frac{-a}{-b}$, and thus the only practical restriction is that $b \neq 0$. 

It's natural to look for simplifying special cases of  <font color="purple">***Theorem 3***. 
 <font color="black">First, let's give the special case of $\frac{a}{b}=1$.

>  <font color="purple"> ***Corollary 1***
>   <font color="black"> Let $z \in \mathbb{C}$, where $z \notin
> \Z_{\leq0}$. 
> <font color="black"> 
> Then $$\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}=1$$
> <font color="purple">  ***Proof***
>  <font color="black">By  <font color="purple">***Theorem 3***  <font color="black">we have $$1 = \frac{z}{z}=\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}$$

<br>But we can simplify further, and take $z = 1$.
This leaves us with a rather satisfying infinite series, which you may have seen before.

Although we didn't set out looking for this result, it came to us nonetheless.<br><br>



> <font color="purple"> ***Corollary 2***
>  <font color="black"> $$\sum^{\infty}_{n=0} \frac{1}{(n+1)(n+2)}=\frac{1}{1\cdot2}+\frac{1}{2\cdot3}+\frac{1}{3\cdot4}+\dots=1$$
> 
> 
> <font color="purple"> ***Proof***
>  <font color="black">By  <font color="purple">***Corollary 1*** <font color="black"> we have  $$1 = \frac{1}{1}=\sum^{\infty}_{n=0}
> \frac{1}{(1+n)(1+n+1)}=\sum^{\infty}_{n=0} \frac{1}{(n+1)(n+2)}$$

## From Infinity...to Beyond?
Consider the expression in  <font color="purple">***Corollary 1***  <font color="black">again: $$1 = \sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}$$

Conventionally, this equality tells us that the infinite series on the right hand side converges to 1.

But it also tells us that we can expand 1 into an infinite series, namely an infinite series containing 1.
In other words, this equality can be viewed recursively - we can interpret the series on the right hand side as containing itself, infinitely!

So, why stop at an infinite series if you can have an infinitely recursive infinite series?

Intuitively, it seems there shouldn't be a reason why the recursive form of  <font color="purple">***Corollary 1***  <font color="black">should not hold, so let's write it out and prove it as a corollary.

Handling the recursive aspect of our new expression will require some subtlety.

>  <font color="purple"> ***Corollary 3***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$. 
> 
>  <font color="black"> Then $$\LARGE 1=\sum^{\infty}_{a=0}
> \frac{z}{(z+a)\left(z+a+\sum^{\infty}_{b=0}
> \frac{z}{(z+b)\left(z+b+\sum^{\infty}_{c=0}
> \frac{z}{(z+c)(z+c+...)}\right)}\right)}$$
> 
> 
>  <font color="purple"> ***Proof***
>  <font color="black">For a fixed, arbitrary $n \in \N,$ we make the following definitions.
> Define $f_n()=1.$
> Define $f_{i}()=\sum^{\infty}_{k=0}
> \frac{z}{(z+k)(z+k+f_{i+1}())},$ where $i \in \N, i \lt n.$
> Define $f_\infty() =\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty}
> \\ \mathllap{n} \to \mathrlap{\infty}}} f_i().$
>
> <font color="black"> To prove the theorem, it suffices to show $f_\infty()=1.$
> 
>  <font color="black"> We first prove $f_i()=1$ for all $i$ such that $i \lt n,$ for all $n.$
> 
>  <font color="black"> We give a proof by induction. 
> 
> <font color="black">  Let $P(n)$ be the claim $f_i()=1$ for all $i$ such that $i \lt n.$
> 
> \
>  <font color="blue"> *Base case:*
>  <font color="black">  $P(1)$ is vacuously true.
> 
>  \
>  <font color="blue">*Inductive step:* 
>  <font color="black"> Assume $P(n-1)$ is true for some fixed, arbitrary $n \gt 1.$   
>
> <font color="black">Then $f_{i}()=1$ for all $i$ such that $i \lt n-1.$  
> 
> <font color="black"> But by our definitions and  <font color="purple">***Corollary 1***<font color="black">,  we have $$f_{n-1}() =
> \sum^{\infty}_{k=0} \frac{z}{(z+k)(z+k+f_{n}())}=\sum^{\infty}_{k=0}
> \frac{z}{(z+k)(z+k+1)}= 1$$
> 
>  <font color="black">This shows $P(n-1) \rightarrow P(n)$ for some fixed, arbitrary $n \gt
> 1.$
> 
>   <font color="black">Thus $P(n)$ is true for all $n \geq 1$.    
>
> <font color="black">That is, $f_i()=1$ for all $i$ such that $i \lt n,$ for all $n.$ 
> 
>  <font color="black"> To conclude the proof, we have
> $$f_\infty()=\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty}
> \\ \mathllap{n} \to \mathrlap{\infty}}}
> f_i()=\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty} \\
> \mathllap{n} \to \mathrlap{\infty}}} 1=1$$

## Conclusion
Since the right hand side of <font color="purple"> ***Corollary 3***<font color="black"> corresponds to our original "strange sum," we now know the answer to the perplexing question asked at the outset: 

Our strange sum is defined whenever $\Omega$ is not a non-positive integer, 

But $z$ can be any other complex number whatsoever, and the right hand side will converge to 1!






## Appendix
This appendix serves as a side quest in the proof of ***Theorem 3***.

When $a,b\in\R$ and $n \in \N$, it's obvious that $$\lim_{n \to \infty}\left[\frac{a}{b} - \frac{a}{b+n} \right]=\frac{a}{b}. \ \ \ \ \color{blue}(1)$$

But for the proof of ***Theorem 3***, we need to show this for $a,b\in\mathbb{C}$.

It suffices to show $$\lim_{n \to \infty}\frac{a}{b+n} =0, \ \ \ \ \color{blue}(2)$$ but (as we will demonstrate) showing $$\lim_{n \to \infty}\left|\frac{a}{b+n}\right| =0, \ \ \ \ \color{blue}(3)$$ suffices.

We're going to need to represent a ratio of complex numbers as the sum of ratios of complex numbers, so let's derive that.

><font color="black"> ***Lemma A.1*** 
> Let $a,b,c,d \in \R$.
> Then $$\frac{a+bi}{c+di} = \frac{ac+bd}{c^2+d^2} + \frac{bc-ad}{c^2+d^2}i$$
> ***Proof*** $$\begin{align*}  &&\left(\frac{a+bi}{c+di}\right)\left(\frac{c-di}{c-di}\right) &=
> \frac{ac+bci-adi+bd}{c^2+d^2}  \\ \\ &&  &=
> \frac{ac+bd+bci-adi}{c^2+d^2}  \\ \\ &&  &= \frac{ac+bd}{c^2+d^2} +
> \frac{bci-adi}{c^2+d^2} \\ \\ && &= \frac{ac+bd}{c^2+d^2} +
> \frac{bc-ad}{c^2+d^2}i  \end{align*}$$

Let's use this to prove $\color{blue}(3)$, and then we'll show that $\color{blue}(3)$ implies $\color{blue}(2)$.

> <font color="black">***Lemma A.2*** 
> Let $a,b,c,d \in \R$  and let $n \in \N.$
> Then $$\lim_{n \to \infty} \left| \frac{a+bi}{c+di+n} \right|=0$$
> 
> <font color="black">***Proof*** 
> Let $c' = c+n.$ By ***Lemma A.1,*** we have $$\begin{align*}  && \frac{a+bi}{c+di+n}&=\frac{ac'+bd}{c'^2+d^2} +
> \frac{bc'-ad}{c'^2+d^2}i \\ \\ && \rightarrow \left|
> \frac{a+bi}{c+di+n} \right|  &=
> \sqrt{\left(\frac{ac'+bd}{c'^2+d^2}\right)^2 +
> \left(\frac{bc'-ad}{c'^2+d^2}\right)^2} \\ \\ && &=  \sqrt{\frac{
> a^2c'^2+2abdc'+b^2d^2}{\left(c'^2+d^2\right)^2} +
> \frac{b^2c'^2-2abdc'+a^2d^2}{\left(c'^2+d^2\right)^2}} \\ \\ && &= 
> \sqrt{\frac{\left(a^2+b^2\right)c'^2+\left(a^2+b^2\right)d^2}{\left(c'^2+d^2\right)^2}}
> \\ \\ && &= 
> \sqrt{\frac{\left(a^2+b^2\right)\left(c'^2+d^2\right)}{\left(c'^2+d^2\right)^2}}
> \\ \\ && &=  \sqrt{\frac{a^2+b^2}{c'^2+d^2}}   \\ \\ && &= 
> \sqrt{\frac{a^2+b^2}{\left(c+n\right)^2+d^2}} \\ \\ && \lim_{n \to
> \infty} \sqrt{\frac{a^2+b^2}{\left(c+n\right)^2+d^2}}&=0 \\ \\
> \rightarrow && \lim_{n \to \infty} \left| \frac{a+bi}{c+di+n} \right|
> &=0  \end{align*}$$

\
This proves $\color{blue}(3)$.
Let's show that $\color{blue}(3)$ implies $\color{blue}(2)$.


> <font color="black">***Lemma A.3***
> Let $\{z_n\}$ be a sequence such that $z_n \in \mathbb{C}.$ 
> Then $$\lim_{n \to \infty} \left| z_n \right|=0 \iff
> \lim_{n \to \infty} z_n =0 $$
> 
> <font color="black">***Proof***
> Recall the formal definition of a limit of a (real or complex) sequence:$$\lim_{n \to \infty} x_n = x \iff \forall
> \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall n\in
> \mathbb {N} \left(n\geq N\implies |x_{n}-x|<\varepsilon
> \right)\right)\right)$$ 
> We have $$\begin{align*}  && \lim_{n \to
> \infty} \left| z_n \right| = 0 &\iff \forall \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall n\in \mathbb {N} \left(n\geq N\implies \left|\left|z_{n}\right|-0\right|<\varepsilon
> \right)\right)\right) \\  && &\iff \forall \varepsilon >0\left(\exists
> N\in \mathbb {N} \left(\forall n\in \mathbb {N} \left(n\geq N\implies
> \left|z_n\right|<\varepsilon \right)\right)\right)  \\  && &\iff
> \forall \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall
> n\in \mathbb {N} \left(n\geq N\implies
> \left|z_{n}-0\right|<\varepsilon \right)\right)\right)  \\  && &\iff
> \lim_{n \to \infty} z_n =0 \\  \end{align*}$$

Thus  $\color{blue}(3)$ implies $\color{blue}(2)$.

But as we've noted at the start of this ***Appendix***, $\color{blue}(2)$ suffices to show $\color{blue}(1)$, which was the goal we were trying to accomplish.

Side quest complete!
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA3ODM1NTg2OCwxMDMwNjYwODU0LDU5Mj
QzNTcxNSwxNDk5NDkzNzIwLDExMjMyOTcxMDcsMTE4NjIwMTQ0
LC0xODk4ODYxOTA3LC0xOTY0NTY5MjYzLDY3NTE1OTY4LC04OD
YyNjQzMDgsLTk5NDc3ODcxMSw1NDk2NDAzNzEsLTc4NzM4OTA4
MCwtMTQ4MjE5ODY4LDc2MjYwNTQwMCwtMjEzMTg2MTc5MCwtNj
YzODU4NTczLC0xMzYxODI3MDAxLC0zNzI0OTYxMDMsLTUwOTgw
MTY1MV19
-->