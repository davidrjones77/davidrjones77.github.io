---
layout: post
title:  "A Strange Sum, Developed"
date:   2025-10-18 15:35:15 -0400
categories: infinite_series
katex: True
---
## Recap
In the last post, I presented a strange sum (see below).  
Are there values of omega for which this expression is mathematically defined?  
If so, for which values of omega does this sum converge?  

$$\LARGE \sum^{\infty}_{a=0} \frac{\color{red}\Omega}{(\color{red}\Omega\color{black}+a)\left(\color{red}\Omega\color{black}+a\sum^{\infty}_{b=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+b)\left(\color{red}\Omega\color{black}+b+\sum^{\infty}_{c=0} \frac{\color{red}\Omega\color{black}}{(\color{red}\Omega\color{black}+c)(\color{red}\Omega\color{black}+c+...)}\right)}\right)}$$

<br>
## Motivation
Let's call the above expression $\sum^\infty_\Omega$.

Where does $\sum^\infty_\Omega$ come from?

I was initially interested in a much simpler question.

> ***<font color="purple">Simple Question</font>***: *<font color="black"> When can we express the reciprocal of a whole number as a sum of reciprocals of whole numbers?</font>*

In other words -  
For which whole numbers $n$ can we write $\frac{1}{n}=\frac{1}{n^\prime}+\frac{1}{n^{\prime\prime}}$, where $n^\prime$ and $n^{\prime\prime}$ are also whole numbers?

The first thing you might notice is $\frac{1}{1}=\frac{1}{2}+\frac{1}{2}$.  
So far, so good!

Continuing the pattern, you might try  $\frac{1}{2}=\frac{1}{3}+x$ and solve for $x.$  
We have  
<center>$$\begin{aligned}
&& x&=\frac{1}{2}-\frac{1}{3} \\  \\
\rightarrow && x&=\frac{3}{6}-\frac{2}{6} \\ \\
\rightarrow && x&=\frac{1}{6} \\ \\
\rightarrow && \frac{1}{2}&=\frac{1}{3}+\frac{1}{6}\\ \\
\end{aligned}$$</center>
Thus $\frac{1}{2}=\frac{1}{3}+\frac{1}{6}$, and continuing this approach we find $\frac{1}{3}=\frac{1}{4}+\frac{1}{12}$.


It would seem at this point we can conjecture an answer to our ***<font color="purple">Simple Question</font>***.

(We use the notation $\mathbb{N}$ to indicate the set of natural numbers *excluding* zero, i.e. the whole numbers, and $\mathbb{N}_0$ to indicate the set of natural numbers *including* zero.)

>***<font color="purple">Conjecture 1</font>***  
><font color="black">  Let $n \in \mathbb{N}$.<br><br></font>
><font color="black"> Then $$\frac{1}{n} = \frac{1}{n+1} + \frac{1}{n(n+1)}$$</font>
>***<font color="purple">Proof</font>***  
><font color="black"><center>$$\begin{aligned}  \frac{1}{n} = \frac{1(n+1)}{n(n+1)} = \frac{n + 1}{n(n+1)}  = \frac{n}{n(n+1)} + \frac{1}{n(n+1)} = 
> \frac{1}{n+1} + \frac{1}{n(n+1)}  \end{aligned}$$</center></font>

So we have an answer to our ***<font color="purple">Simple Question</font>*** - *the reciprocal of any whole number $n$ can be expressed as the sum of reciprocals of whole numbers.*  
Moreover, we now know a formula for that sum - our curiosity has rewarded us with information we weren't initially looking for.

But hang on - is there anything special about the 1 in each numerator?  
And did our proof take advantage of anything intrinsic to whole numbers?  
In other words, we can generalize our result (taking care to prevent division by zero).  
Let's do that.

> ***<font color="purple">Theorem 1</font>*** 
> <font color="black"> Let $a, b \in \mathbb{C}$, where $b \notin \{-1, 0\}$.<br><br></font>
> <font color="black"> Then $$\frac{a}{b} = \frac{a}{b+1} + \frac{a}{b(b+1)}$$</font>
> ***<font color="purple">Proof</font>*** 
> <font color="black"><center>$$\begin{aligned}  \frac{a}{b} &= \frac{a(b+1)}{b(b+1)} = \frac{ab + a}{b(b+1)}  = \frac{ab}{b(b+1)} + \frac{a}{b(b+1)} = 
> \frac{a}{b+1} + \frac{a}{b(b+1)} \end{aligned}$$</center>

<br>
## Expanding Terms
But why stop at two terms?  
After all, the terms on the right hand side of ***<font color="purple">Theorem 1</font>*** are just fractions having complex numbers as numerator and denominator, and so may be expanded according to ***<font color="purple">Theorem 1</font>***.  
We should be able to expand terms on the right hand side of ***<font color="purple">Theorem 1</font>*** as many times as we like, and we know the form such terms should take.

Let's generalize ***<font color="purple">Theorem 1</font>*** to a sum of $n$ terms, where $n$ is a whole number.  
Again, we must restrict $b$ to prevent division by zero.

We use the notation $\N_{0\leq n}$ to indicate the set of  non negative integers from $0$ to $n$ inclusive, for some $n \in \N_0$.

> ***<font color="purple">Theorem 2</font>***
> <font color="black"> Let $n \in \N.$ Let $a, b \in \mathbb{C}$, where $b \notin \{-m \vert m \in \N_{0\leq n}\}$.</font><br>
> <font color="black">Then $$\frac{a}{b} = \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}$$</font>
> ***<font color="purple">Proof</font>***
> <font color="black"> We give a proof by induction.<br><br>
> Let $P(n)$ be the claim $\frac{a}{b} = \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}.$</font><br>
> *<font color="blue">Base case</font>:* <font color="black"> Letting $n=1,$ we have by</font> ***<font color="purple">Theorem 1</font>***
> <font color="black"><center>$$\begin{aligned}  &&\frac{a}{b} &= \frac{a}{b+1} + \frac{a}{b(b+1)} \\ \\  \rightarrow && \frac{a}{b} &= \frac{a}{b+1} +
> \sum^0_{i=0} \frac{a}{(b+i)(b+i+1)} \\ \\   \rightarrow && \frac{a}{b}
> &= \frac{a}{b+n} + \sum^{n-1}_{i=0} \frac{a}{(b+i)(b+i+1)}  
> \end{aligned}$$</center></font>  <font color="black">Thus $P(1)$ is true.</font><br>
> *<font color="blue">Inductive step:</font>* <font color="black">Assume $P(n)$ is true for some fixed, arbitrary $n.$<br><br>
> Then by </font>***<font color="purple">Theorem 1</font>*** <font color="black">and the</font> <font color="red">inductive hypothesis $P(n)$</font>,
> <font color="black"><center>$$\begin{aligned}  &&
> \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &= \sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} + \frac{a}{(b+n)(b+n+1)} \\ \\  \rightarrow &&
> \sum^{n}_{i=0} \frac{a}{(b+i)(b+i+1)} &=\sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \color{black}{+} \color{purple}{\frac{a}{b+n}-
> \frac{a}{b+n+1}} \\ \\  \rightarrow && \sum^{n}_{i=0}
> \frac{a}{(b+i)(b+i+1)} &= \color{red}{\frac{a}{b}- \frac{a}{b+n}}
> \color{black} + \frac{a}{b+n}- \frac{a}{b+n+1} \\ \\    \rightarrow &&
> \frac{a}{b}  &=  \frac{a}{b+n+1}+  \sum^{(n+1)-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\   \rightarrow && &P(n+1)  \end{aligned}$$</center></font>
> <br><font color="black"> Thus $P(n)$ is true for all $n \geq 1$.

<br>
## Taking a Limit

But why stop at $n$ terms?  
If we can expand our sum to *arbitrarily* (i.e. *fintely*) many terms, surely we can expand to *infinitely* many terms.  

With fractions restricted to real numerators and denominators, this would be straightforward.  
But we'd rather not lose generality - we'd like to expand our sum to infinitely many terms while staying within the more general domain of complex fractions.  

So let's take a limit at infinity while staying within the domain of complex fractions.  
We'll need to use two facts about limits of sequences of complex fractions, which are derived in the **Appendix** at the end of this post.

> ***<font color="purple">Theorem 3</font>***
> <font color="black">Let $a, b \in \mathbb{C}$, where $b \notin \Z_{\leq0}$.</font><br>
> <font color="black">Then $$\frac{a}{b} = \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}$$</font>
> 
> ***<font color="purple">Proof</font>***<br><font color="black">
> By the definition of infinite series and limits, and by </font>***<font color="purple">Theorem 2</font>***<font color="black"> we have</font>
> <font color="black"><center>$$\begin{aligned}   \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}&=\lim_{n \to \infty}\sum^{n}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\   &=\lim_{n \to \infty}\sum^{n-1}_{i=0}
> \frac{a}{(b+i)(b+i+1)} \\ \\  &=\lim_{n \to \infty}\left[\frac{a}{b} -
> \frac{a}{b+n} \right] \\ \\   \end{aligned}$$</center></font><span></span><font color="black">
> But by </font>***<font color="purple">Lemma A.2</font>***<font color="black"> (see Appendix)</font><font color="black">
> $$\lim_{n \to \infty} \left|\frac{a}{b+n}\right|=0$$ and by </font>***<font color="purple">Lemma A.3</font>***<font color="black"> (see Appendix)
> $$\lim_{n \to \infty} \left|\frac{a}{b+n}\right|=0 \iff \lim_{n \to
> \infty} \frac{a}{b+n}=0$$ and so $$\lim_{n \to
> \infty}\left[\frac{a}{b} - \frac{a}{b+n} \right]=\frac{a}{b}$$ thus
> $$\frac{a}{b} = \sum^{\infty}_{n=0} \frac{a}{(b+n)(b+n+1)}$$

<br>
## Special Cases
***<font color="purple">Theorem 3</font>*** tells us that any complex fraction can be expressed as an infinite series, and gives us the form of that infinite series.

Although the theorem restricts $b$ from being a non-positive integer, this is not a problem, since $\frac{a}{b}$ can always be expressed as $\frac{-a}{-b}$, and thus the only practical restriction is that $b \neq 0$. 

It's natural to look for simplifying special cases of ***<font color="purple">Theorem 3</font>***.  
First, let's give the special case of $\frac{a}{b}=1$.

> ***<font color="purple">Corollary 1</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin
> \Z_{\leq0}$.</font>
> <font color="black"><br><br> 
> Then $$\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}=1$$</font><br>
> ***<font color="purple">Proof</font>***<br><font color="black">
> By </font>***<font color="purple">Theorem 3</font>*** <font color="black">we have $$1 = \frac{z}{z}=\sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}$$

But we can simplify further, and take $z = 1$.  
This yields a rather satisfying infinite series, which you may have seen before.

Although we didn't set out looking for this result, it came to us nonetheless.<br><br>



> ***<font color="purple">Corollary 2</font>***
>  <font color="black"> $$\sum^{\infty}_{n=0} \frac{1}{(n+1)(n+2)}=\frac{1}{1\cdot2}+\frac{1}{2\cdot3}+\frac{1}{3\cdot4}+\dots=1$$</font>
> 
> 
> ***<font color="purple">Proof</font>***<font color="black"><br>
> By </font>***<font color="purple">Corollary 1</font>*** <font color="black"> we have  $$1 = \frac{1}{1}=\sum^{\infty}_{n=0}
> \frac{1}{(1+n)(1+n+1)}=\sum^{\infty}_{n=0} \frac{1}{(n+1)(n+2)}$$</font>

<br>
## From Infinity...to Beyond?
Consider the expression in ***<font color="purple">Corollary 1</font>*** again:  
<center>$$1 = \sum^{\infty}_{n=0} \frac{z}{(z+n)(z+n+1)}$$</center>

Conventionally, this equality tells us that the infinite series on the right hand side converges to 1.

But it also tells us there exists an expansion of 1 into an infinite series, namely an infinite series itself containing 1.

In other words, this equality can be viewed recursively - we can interpret the series on the right hand side as containing itself, infinitely!

So, why stop at an infinite series if you can have an infinitely recursive infinite series?

Intuitively, it seems there shouldn't be a reason why the recursive form of ***<font color="purple">Corollary 1</font>*** should not hold, so let's write it out and prove it as a corollary.

We give a proof by induction that, for each $n \in \N,$ defines a set of functions which capture the right hand side of ***<font color="purple">Corollary 1</font>*** nested within itself $n-1$ times.

To prove the corollary, we define a double limit corresponding to the infinitely nested case, and show that this double limit converges to 1.

> ***<font color="purple">Corollary 3</font>***
> <font color="black"> Let $z \in \mathbb{C}$, where $z \notin \Z_{\leq0}$.</font><br>
> <font color="black">Then $$\LARGE 1=\sum^{\infty}_{a=0}
> \frac{z}{(z+a)\left(z+a+\sum^{\infty}_{b=0}
> \frac{z}{(z+b)\left(z+b+\sum^{\infty}_{c=0}
> \frac{z}{(z+c)(z+c+...)}\right)}\right)}$$</font>
> 
> 
> ***<font color="purple">Proof</font>***
> <font color="black">For a fixed, arbitrary $n \in \N,$ with $i \in \N, i \lt n$ we make the following definitions.<br>
> Define $f_n()=1.$<br>
> Define $f_{i}()=\sum^{\infty}_{k=0} \frac{z}{(z+k)(z+k+f_{i+1}())}.$<br><br>
> We define $f_\infty() =\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty}
> \\ \mathllap{n} \to \mathrlap{\infty}}} f_i().$</font><br>
>
> <font color="black"> To prove the theorem, it suffices to show $f_\infty()=1.$</font><br>
> 
> <font color="black"> We first prove $f_i()=1$ for all $i$ such that $i \lt n,$ for all $n.$</font><br>
> 
> <font color="black"> We give a proof by induction.</font><br>
> 
> <font color="black"> Let $P(n)$ be the claim $f_i()=1$ for all $i$ such that $i \lt n.$<br><br><br></font>
> *<font color="blue">Base case:</font>*
> <font color="black">$P(1)$ is vacuously true.</font><br><br>
> 
> *<font color="blue">Inductive step:</font>*<br>
> <font color="black"> Assume $P(n-1)$ is true for some fixed, arbitrary $n \gt 1.$</font><br>
>
> <font color="black">Then $f_{i}()=1$ for all $i$ such that $i \lt n-1.$</font><br><br><font color="black">
> But by our definitions and</font> ***<font color="purple">Corollary 1</font>***<font color="black">, we have 
> $$f_{n-1}() = \sum^{\infty}_{k=0} \frac{z}{(z+k)(z+k+f_{n}())}=\sum^{\infty}_{k=0}
> \frac{z}{(z+k)(z+k+1)}= 1$$</font><br>
> 
>  <font color="black">This shows $P(n-1) \rightarrow P(n)$ for some fixed, arbitrary $n \gt
> 1.$</font><br>
> 
> <font color="black">Thus $P(n)$ is true for all $n \geq 1$.</font><br>  
>
> <font color="black">That is, $f_i()=1$ for all $i$ such that $i \lt n,$ for all $n.$<br><br>
> 
> <font color="black">To conclude the proof, we have
> $$f_\infty()=\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty}
> \\ \mathllap{n} \to \mathrlap{\infty}}}
> f_i()=\lim\limits_{\substack{\mathllap{i} \to \mathrlap{\infty} \\
> \mathllap{n} \to \mathrlap{\infty}}} 1=1$$</font>

<br>
## Conclusion
Since the right hand side of ***<font color="purple">Corollary 3</font>*** corresponds to our original expression $\sum^\infty_\Omega$, we now know the answer to the domain and convergence questions asked at the outset.

> ***<font color="purple">A Strange Conclusion</font>***<font color="black">: Let $\Omega \in \mathbb{C}$, where $\Omega \notin \Z_{\leq0}$. Then $\sum^\infty_\Omega=1$.</font>

 
<br>

___

<br>
## Appendix
This appendix serves as a side quest for the proof of ***<font color="purple">Theorem 3</font>***.

When $a,b\in\R$ and $n \in \N$, it's obvious that <br><center>$$\lim_{n \to \infty}\left[\frac{a}{b} - \frac{a}{b+n} \right]=\frac{a}{b}. \ \ \ \ \color{blue}(1)$$</center>

But for the proof of ***<font color="purple">Theorem 3</font>***, we need to show this for $a,b\in\mathbb{C}$.

It suffices to show<br>
<center>$$\lim_{n \to \infty}\frac{a}{b+n} =0 \ \ \ \ \color{blue}(2)$$</center>
but, as we will demonstrate, showing<br>
<center>$$\lim_{n \to \infty}\left|\frac{a}{b+n}\right| =0 \ \ \ \ \color{blue}(3)$$</center> suffices as well.

To get started, we're going to need to represent a complex fraction as a complex number in standard form, so let's begin there.

This is one of the first formulas given in any textbook introduction to complex numbers, but we demonstrate it here both to keep the presentation self contained and to maintain an attitude of developing the results in this article from first principles.

>***<font color="purple">Lemma A.1</font>*** 
> <font color="black">Let $a,b,c,d \in \R$, where not both $c=0$ and $d=0$.</font><br>
> <font color="black">Then $$\frac{a+bi}{c+di} = \frac{ac+bd}{c^2+d^2} + \frac{bc-ad}{c^2+d^2}i$$</font><br>
> ***<font color="purple">Proof</font>***
> <font color="black"><center>$$\begin{aligned}  &&\left(\frac{a+bi}{c+di}\right)\left(\frac{c-di}{c-di}\right) &=
> \frac{ac+bci-adi+bd}{c^2+d^2}  \\ \\ &&  &=
> \frac{ac+bd+bci-adi}{c^2+d^2}  \\ \\ &&  &= \frac{ac+bd}{c^2+d^2} +
> \frac{bci-adi}{c^2+d^2} \\ \\ && &= \frac{ac+bd}{c^2+d^2} +
> \frac{bc-ad}{c^2+d^2}i  \end{aligned}$$</center></font>

We will use this to prove $\color{blue}(3)$, and then show that $\color{blue}(3)$ implies $\color{blue}(2)$.

> ***<font color="purple">Lemma A.2</font>*** 
> <font color="black">Let $a,b,c,d \in \R$  and let $n \in \N.$<br></font>
> <font color="black">If not both $c+n=0$ and $d=0,$ then $$\lim_{n \to \infty} \left| \frac{a+bi}{c+di+n} \right|=0$$</font>
> 
> ***<font color="purple">Proof</font>***<br><font color="black">Let $c' = c+n.$ By</font> ***<font color="purple">Lemma A.1</font>***<font color="black">, we have</font> 
> <font color="black"><center>$$\begin{aligned}  && \frac{a+bi}{c+di+n}&=\frac{ac'+bd}{c'^2+d^2} +
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
> \sqrt{\frac{a^2+b^2}{\left(c+n\right)^2+d^2}} & \color{blue}(4) \\ \\
> \end{aligned}$$</center></font><font color="black">But $$\lim_{n \to
> \infty} \sqrt{\frac{a^2+b^2}{\left(c+n\right)^2+d^2}}=0$$
> and so by</font> <font color="blue">(4)</font> <font color="black">we have $$\lim_{n \to \infty} \left| \frac{a+bi}{c+di+n} \right|
> =0$$</font>

\
This proves $\color{blue}(3)$.<br>
Let's show that $\color{blue}(3)$ implies $\color{blue}(2)$.


> ***<font color="purple">Lemma A.3</font>***
> <font color="black">Let $\{z_n\}$ be a sequence such that $z_n \in \mathbb{C}.$<br></font>
> <font color="black">Then $$\lim_{n \to \infty} \left| z_n \right|=0 \iff
> \lim_{n \to \infty} z_n =0 $$</font>
> 
> ***<font color="purple">Proof</font>***
> <font color="black">Recall the formal definition of a limit of a (real or complex) sequence:$$\lim_{n \to \infty} x_n = x \iff \forall
> \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall n\in
> \mathbb {N} \left(n\geq N\implies |x_{n}-x|<\varepsilon
> \right)\right)\right)$$<br>
> We have <center>$$\begin{aligned}  && \lim_{n \to
> \infty} \left| z_n \right| = 0 &\iff \forall \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall n\in \mathbb {N} \left(n\geq N\implies \left|\left|z_{n}\right|-0\right|<\varepsilon
> \right)\right)\right) \\  && &\iff \forall \varepsilon >0\left(\exists
> N\in \mathbb {N} \left(\forall n\in \mathbb {N} \left(n\geq N\implies
> \left|z_n\right|<\varepsilon \right)\right)\right)  \\  && &\iff
> \forall \varepsilon >0\left(\exists N\in \mathbb {N} \left(\forall
> n\in \mathbb {N} \left(n\geq N\implies
> \left|z_{n}-0\right|<\varepsilon \right)\right)\right)  \\  && &\iff
> \lim_{n \to \infty} z_n =0 \\  \end{aligned}$$</center>

Thus  $\color{blue}(3)$ implies $\color{blue}(2)$.

But as we've noted at the start of this **Appendix**, $\color{blue}(2)$ suffices to show $\color{blue}(1)$, which was the goal we were trying to accomplish.