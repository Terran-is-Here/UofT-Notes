---
updated_at: 2026-10-10T18:24:53.880-04:00
edited_seconds: 1120
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 16
Lecture Date: 2026-10-16
Week: 6
---
Hub: [[ESC194 Hub]]
Previous: [[15 — Summary of Curve Sketching]]
Next: N/A 
> [!quote] Recommended Reading 
> Stewart Section 3.7, 3.9
> [[10 — Differentiation Formulas and Applied Derivatives]], [[11 — Trigonometric, Chain and Implicit Differentiation]]
--- 

# Lecture Notes

---
# Pre-Lecture Notes
## Optimization
> [!quote] Recommended Reading 
> [[14 — Derivatives, Function Shape, Horizontal Asymptotes#First Derivative Test / 1DT]]
> [[12 — Related Rates, Min and Max Values]]

Optimization problems are problems where we want to find how to *maximize* or *minimize* something; or in other words: how do we find the absolute extremum of a function? We can primarily do this by adapting our First Derivative Theorem to expand over an entire interval:

> [!theorem] First Derivative Test (for absolute extremums): 
> If $f$ has a critical point at some value $c$; then: 
> * If $f'(x) <0$ for all values $x<c$, and $f'(c)>0$ for all values $c<x$, then $f(c)$ is the absolute minima of a function. 
> * If $f'(x) >0$ for all values $x<c$, and $f'(c)<0$ for all values $c<x$, then $f(c)$ is the absolute maxima of a function. 
>
> Note that these lines are essentially describing how the shape of a slope is like.

Note that for optimization problems, if possible, we still have to evaluate our endpoints if possible; though observations from the 1DT/2DT will also help to quickly show that evaluating endpoints is *not* necessary. 

Often however; we have cases where we have *two* equations to optimize; one equation being directly optimized and another offering a restraint to the problem. The general rule of thumb is to utilize the restraint equation to limit / restrain the corresponding function to be optimized. This is essentially similar to MCV4UR; just with some more proof/rigor behind it. 

## Antiderivatives 
Antiderivatives are effectively the inverse of differentiation, and are defined as the following expression below: 
> [!theorem] Antiderivatives
> If $F$ is an antiderivative of $f$, then: 
> $$F' = f$$
> That is, the derivative of an antiderivative of some function $f$ returns back that same function $f$. 

Note that the concept of taking an antiderivative also has an added component to it, a component that partially arises from the Mean Value Theorem. Recall that in [[13 — Mean Value Theorem, Linear Approximations and Differentials#^4698a8|Mean Value Theorem (13) > Corollary 1.1]] that $f'(x)=0, \forall x\in(a,b) \implies f(x)=C$; then: 

> [!theorem] Corollary 1.1
> If $f'(x)=g'(x) \forall x\in(a,b)$, then $f(x)-g(x)$ is constant on $(a,b)$, that is $f(x) = g(x)+c$. 
>
> > *Proof*
> > If $f'(x)=g'(x)$, define the function $L(x)=f(x)-g(x)$.
> >  $L'(x)=f'(x)-g'(x)=0 \implies L(x)=C$, then $f(x)-g(x) = C \implies f(x)=g(x)+C$

Note that we can extend this to the concept of Antiderivatives.

> [!theorem] Theorem 1.1
> Let $F(x),G(x)$ be the antiderivatives of some function $f$, $F(x) = G(x)+C$. 
>
> > *Proof* 
> > If $F(x),G(x)$ are antiderivatives of some function $f$, then $F'(x)=G'(x)=f$. 
> > Using the same set of logic as the corollary above, define a function $L(x) = F(x)-G(x)$.
> > $L'(x) = F'(x)-G'(x) = 0 \implies L(x)=C$, then $F(x)-G(x)=C$, which then shows that $F(x)=G(x)+C$. 
> 
> > Or, an Antiderivative of a function $f$ will always have some constant term $C$ on the end; which can be set to any arbitrary value. 

Note what Theorem 1.1 indicates: Taking the antiderivative of a function results in an *infinite* range of functions that have the same shape but are solely vertically translated from each other. Intuitively this makes sense; $F(x) = G(x) +C$, then with $F'(x)=G'(x)=f$, then $F'(x) = f(x)$, as $\frac{d}{dx}C=0$ for any constant. 

> Note, notation wise, the arbitrary constant that arises from antidifferentiation is always notated by some capital $C$. In terms of determining what value this is, we need to be given some $F(a)=d$ to calculate $C$ (or in other words, we need to have the value of the actual antiderivative at some point). 
### Antiderivative Formulas 
Antiderivative Formulas / Expressions arise from the concept that Antiderivatives differentiate back into their original function. 

> Power Rule 
> From $f(x) = x^n, f'(x)=nx^{n-1}$ Then the antiderivative of $f(x)=x^n$ is:$$f(x) = x^n, \int f(x) dx = \frac{x^{n+1}}{n+1} + C$$
> Note this is only true if and only if $n\neq -1$. 
> > In this case, $f(x)=x^{-1}, F(x) = \ln|x| +C$. 

> Differentiation Rules 
> The Sum Rule natively applies with antidifferentiation, as well as the constant rule. 
> > Constant Rule:
> > $$f(x)=c, F(x) = cx + C$$

> Trigonometric Rules
> Essentially reverse the direction of your differentiation of the trig functions. 
> $$\begin{array}{cc|c}\text{ Function} && \text{Corresponding Antiderivative} \\\cos(x) &  & \sin(x) \\\sin(x) &  & -\cos(x) \\\sec^2(x) &  & \tan(x) \\\sec(x)\tan(x) &  & \sec(x)\end{array}$$
> That is, you know that the derivative of $\sin$ is $\cos$, therefore the antiderivative of $\cos$ is $\sin$. Same logic applies for the rest; since the **antiderivative when differentiated returns the original function**. 

## Sigma Notation
Sigma Notation is the discrete version of its more well known sibling, the one for Integration. Sigma notation is defined as the following: 
$$
\sum _{x=m}^na_{i} = \underbrace{a_{m} + a_{m+1}  + a_{m+2} + \dots + a_{n}}_{\text{Some set of numbers (can be from a function)}}
$$
From this definition, we can derive some very useful theorems for analysis. The following below are trivial theorems and the proof is left as an exercise to the reader.  
$$
\begin{align}
\sum_{x=1}^n 1 &= n \tag{Theorem 2.1} \\
\sum_{x=m}^nca_{i} &= c\sum_{x=m}^na_{i} \tag{Theorem 2.2} \\
\sum^n_{x=m}a_{i}+b_{i} & = \sum_{x=m}^na_{i} + \sum ^n_{x=m}b_{i} \tag{Theorem 3.3} \\
\sum^n_{x=m}a_{i}-b_{i} & = \sum_{x=m}^na_{i} - \sum ^n_{x=m}b_{i} \tag{Theorem 3.4} 
\end{align}
$$
We will now detail some more theorems which may be useful for analysis. 

> *Theorem 3.5*
> Prove the following formula for the sum of the first $n$ integers: 
> > $$\sum^n_{i=1}i = \frac{n(n+1)}{2}$$
> 
> > *Proof*
> > Define the sum of this statement as some value $S$, that is $S=1+2+3+\dots+n-1+n$. Writing them in ascending and descending order gives us: $$\begin{align}S &= 1+2+3+\dots+n-1+n \\S &= n + n-1 + n-2 + \dots + 3+2+1 \\\end{align}$$
> > Summing these up gives us the following: $$\begin{align}2S &=\underbrace{ (n+1) + (n+1) + \dots +(n+1)}_{n \text{ times}} \\\sum _{i=1}^n= S &= \frac{n(n+1)}{2}\end{align}$$

> *Theorem 3.6*
> Prove the following formula for the sum of the *squares* of the first $n$ integers. 
> > $$\sum^n_{i=1}i^2 = 1 + 2^2 + 3^3 + \dots + n^2 = \frac{n(n+1)(2n+1)}{6}$$
> 
> > Proof 
> > We will prove this through Induction.
> > * We will first show that $n=1$ holds true for the formula $\frac{n(n+1)(2n+1)}{6} = 1*2*3 =1$, which holds.
> > * We now assume that this holds true for some $n=k$, that is $\frac{k(k+1)(2k+1)}{6}$. 
> > 
> > We now need to prove this for $n=k+1$: 

$$
\begin{align}
\sum_{i=1}^{k+1}i^2 &= \underbrace{1^2 + 2^2 + \dots + k^2}_{\text{Equivalent to }n=k} + (k+1)^2\\&=\frac{k(k+1)(2k+1)+6(k+1)^2}{6}  \\
&= (k+1) \frac{k(2k+1)+6(k+1)}{6} \\
&=(k+1)\frac{2k^2+k+6k+6}{6} \\
&=(k+1)\frac{2k^2+7k+6}{6}  \\
&=(k+1)\frac{2k^2+7k+6}{6} 
\end{align}
$$


