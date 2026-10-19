---
updated_at: 2026-10-19T12:00:33.640-04:00
edited_seconds: 1850
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 17
Lecture Date: 2026-10-19
Week: 7
---
Hub: [[ESC194 Hub]]
Previous: [[15 — Summary of Curve Sketching]], [[16 — Linear Approximation and Differentials]]
Next: [[18 — Areas and Distances]]
> [!quote] Recommended Reading 
> Stewart Section 3.7, 3.9
> [[10 — Differentiation Formulas and Applied Derivatives]], [[11 — Trigonometric, Chain and Implicit Differentiation]]
--- 

# Lecture Notes
## Optimization (LEC) 
Optimization problems generally follow the same following pattern. We often want to try and relate a system of related mathematical expressions as a set of known variables (and or their differentials) , then follow our approaches from [[12 — Related Rates, Min and Max Values]] in order to find the possible max/min values present. 
1. Understand the problem being presented (what are we trying to find, maximize, or minimize?) 
2. Draw a diagram (helps a lot).
3. Introduce variables for quantities of interest (+label clearly on the diagram that we defined in section 2) 
4. Solve mathematical relationships between properties present. 
	1. Note that you may find that quantities of interest may depend on more than one variable. 
	2. More than one relationship may be required; and or the knowledge of the differential may be required knowledge. 
5. Find maximum and minimum values of the quantity of interest. 

For instance: 
> Let us say that we want a poster to have a total area of $240~cm^2$, with $1~cm$ margins on the bottom and sides, and a $2~cm$ margin on the top. What dimensions of poster will give the largest printed area? 

> [!ila]  In Lecture Addendum
> Consider that using logic, we can bound the intervals of values that $\ell$ could take; (or even $h$) within some closed bound. From here, we could use the closed interval method to also analyze the function. 

We can intuitively define the following terms: 
$$
\begin{align}
A_{ext}  & = \ell h   =240 \\
A_{int} & =(\ell-2)(h-3) 
\end{align}
$$
We want to maximize $A_{int}$, we can define $\ell$ as $\ell=\frac{240}{h}$; then: 
$$
\begin{align}
A_{int}  & = \left( \frac{240}{h}  - 2\right)(h-3)  \\
 & =240  - \frac{3(240)}{h} -2h+6 =-\frac{720}{h} -2h + 246
 \end{align}
$$
Differentiating this to find possible maximums: 
$$
A'_{int}=\frac{720}{h^2} - 2 = 0
$$
Then: 
$$
\begin{align}
A'_{int} = \frac{720}{h^2} =2 \\
\frac{h^2}{720}  & = \frac{1}{2} \\
 h^2& =360 \\
 h  & =\pm \sqrt{ 360 }=6\sqrt{ 10 } \approx 19~cm
\end{align}
$$
We can plug in this value for $h$ into our original term (note that we did not consider the negative root, as it did not make sense). Note that we also did not consider $h=0$, as it would both not make sense, and it is also not included in the domain of the original function being differentiated. 

We also take a note to see that our term for $h$ has to be bounded from $[3,77]$; thus from here we could bound and determine the end points over the closed interval method. We know that $6\sqrt{ 10 }$ would be our maximum point for this case; then taking the original area expression, then: 
$$
\begin{align}
240  & = \ell*6\sqrt{ 10 } \\
\ell  & = 4\sqrt{ 10 }
\end{align}
$$
## Antiderivatives (LEC) 
Recall how we define the concept of the derivative as the instantaneous rate of change (or slope) of the function given at a certain point. Antiderivatives ask us to think about if, given how a function changes (it's slope), can I work backwards to find the shape of the original function? 

We define antiderivatives as the following: 
> [!theorem] Antiderivative (LEC) 
> A function $F(x)$ is called **an** antiderivative for $f$ on an open interval $I$ if: 
> $$F'(x) = f(x)~ \forall x\in I$$
> > [!caution] Note
> > Antiderivatives are not unique; as for any Antiderivative, we can add some arbitrary constant at the end; as this would still satisfy our definition of the antiderivative of a function. 
> 

For instance for the above definition: $$f(x)=x^2 \implies F(x) = \frac{1}{3}x^3$$
Note that we can define this in terms of a trigonometric function. 

Consider now finding the antiderivative of the function below with the additional following information: 
$$
f(x) = \frac{x+1}{\sqrt{ x }}~,F(1)=5
$$
Taking the antiderivative of this; then: 
$$
\begin{align}
f(x)  & = \frac{x}{\sqrt{ x }} + \frac{1}{\sqrt{ x }} = \sqrt{ x  }+x^{-1/2} & \text{Taking inverse power rule...} \\
F(x) & = \frac{2}{3}x^{3/2} + 2x^{1/2} +C
\end{align}
$$
Since we know $F(1)=5$, then $F(1) = \frac{2}{3}+2+C = 5 \implies C=\frac{7}{3}$, then we can **fully specify** antiderivative: 
$$
F(x)=\frac{2}{3}x^{3/2} + 2x^{1/2} + \frac{7}{3}
$$
This expression is fully specified. Note that $F(1)$ is considered a (boundary condition), as it defines the behavior of our function at a certain point. 
### Higher Derivatives
Considering now higher derivatives; then: 
$$
f''(x) = 20x^3 + 12x^2 + 4
$$
What is the original function? Taking the reverse power rule twice, then: 
$$
\begin{align}
f'(x)  & = 5x^4 + 4x^3 + 4x + C_{1} \\
f(x) & =x^5 + x^4 + 2x^2 +C_{1}x + C_{2} 
\end{align}
$$
Note that from here, we have two unknown constants. We actually need the boundary conditions for $f'(x)$ and $f(x)$ at a certain points $C_{1},C_{2}$. 
## Sigma Notation (LEC) 
> [!quote] Recommended Reading 
> Stewart Textbook Appendix E, Section 4.1, 4.2

> Sigma Notation
> If $a_{m}, a_{m+1},\dots,a_{n}$ are eal numbers, and $m,n$, where $m\leq n$, then we denote the following: 
> $$S=\sum_{i=m}^n a_{i}=a_{m} + a_{{m+1}} + \dots+a_{n} $$
> In this context, we consider $i$ as the index of summation. 

Summations can be represented in multiple ways; since we have control as to how a sum is being indexed, we can manipulate our definition of $i$ in order to represent sums in a more usable method. For instance, take the following function: 

$$
\sum_{i=2}^n i^3 = 2^3 + 3^3 + \dots + (n-1)^3 + n^3
$$
Consider; we could also define this as the following: 
$$
\sum_{j=1}^{n-1} (j+1)^3 = 2^3 + 3^3 +\dots + n^3
$$
That is, we can manipulate the bounds of the sum, as long as the corresponding function is adjusted with respects to a term. The following theorems are useful for working with sums: 

$$
\begin{align}
\sum_{i=m}^n\alpha*a_{i}  & =\alpha\sum_{i=m}^na_{i} & \alpha~\text{is a constant} \tag{1.1} \\
\sum_{i=m}^na_{i}\pm b_{i} & =\sum_{i=m}^na_{i} \pm\sum_{i=m}^nb_{i}\tag{1.2,1.3} \\
\sum_{i=1}^n 1  & =n  \tag{1.4}\\
\sum_{i=1}^n \alpha & =an \tag{1.5}\\
\sum_{i=1}^ni & =\frac{n(n+1)}{2}\tag{1.6} \\
\sum_{i=1}^ni^2 & =\frac{n(n+1)(2n+1)}{6} \tag{1.7} \\
\sum_{i=1}^ni^3 & =\left[ \frac{n(n+1)}{2} \right]^2 \tag{1.8} \\
\sum_{i=m}^ni^4  & =\frac{n(n+1)(2n+1)(3n^2+3n-1)}{30 (?)}
\end{align}
$$


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

> [!theorem] Power Rule 
> From $f(x) = x^n, f'(x)=nx^{n-1}$ Then the antiderivative of $f(x)=x^n$ is:$$f(x) = x^n, \int f(x) dx = \frac{x^{n+1}}{n+1} + C$$
> Note this is only true if and only if $n\neq -1$. 
> > In this case, $f(x)=x^{-1}, F(x) = \ln|x| +C$. 

> [!theorem] Differentiation Rules 
> The Sum Rule natively applies with antidifferentiation, as well as the constant rule. 
> > Constant Rule:
> > $$f(x)=c, F(x) = cx + C$$

> [!theorem] Trigonometric Rules
> Essentially reverse the direction of your differentiation of the trig functions. 
> $$\begin{array}{cc|c}\text{ Function} && \text{Corresponding Antiderivative} \\\cos(x) &  & \sin(x) \\\sin(x) &  & -\cos(x) \\\sec^2(x) &  & \tan(x) \\\sec(x)\tan(x) &  & \sec(x)\end{array}$$
> That is, you know that the derivative of $\sin$ is $\cos$, therefore the antiderivative of $\cos$ is $\sin$. Same logic applies for the rest; since the **antiderivative when differentiated returns the original function**. 

## Sigma Notation
Sigma Notation is the discrete version of its more well known sibling, ($\int$) the one for Integration. Sigma notation is defined as the following: 
$$
\sum _{x=m}^na_{i} = \underbrace{a_{m} + a_{m+1}  + a_{m+2} + \dots + a_{n}}_{\text{Some set of numbers (can be from a function)}}
$$
From this definition, we can derive some very useful theorems for analysis. The following below are trivial theorems and the proof is left as an exercise to the reader.  
$$
\begin{align}
\sum_{x=1}^n 1 &= n \tag{Theorem 2.1} \\
\sum_{x=m}^nca_{i} &= c\sum_{x=m}^na_{i} \tag{Theorem 2.2} \\
\sum^n_{x=m}a_{i}+b_{i} & = \sum_{x=m}^na_{i} + \sum ^n_{x=m}b_{i} \tag{Theorem 2.3} \\
\sum^n_{x=m}a_{i}-b_{i} & = \sum_{x=m}^na_{i} - \sum ^n_{x=m}b_{i} \tag{Theorem 2.4} 
\end{align}
$$
We will now detail some more theorems which may be useful for analysis. 

> [!theorem] *Theorem 2.5*
> Prove the following formula for the sum of the first $n$ integers: 
> > $$\sum^n_{i=1}i = \frac{n(n+1)}{2}$$
> 
> > [!caution]- *Proof*
> > Define the sum of this statement as some value $S$, that is $S=1+2+3+\dots+n-1+n$. Writing them in ascending and descending order gives us: $$\begin{align}S &= 1+2+3+\dots+n-1+n \\S &= n + n-1 + n-2 + \dots + 3+2+1 \\\end{align}$$
> > Summing these up gives us the following: $$\begin{align}2S &=\underbrace{ (n+1) + (n+1) + \dots +(n+1)}_{n \text{ times}} \\\sum _{i=1}^n= S &= \frac{n(n+1)}{2}\end{align}$$

> [!theorem] *Theorem 2.6*
> Prove the following formula for the sum of the *squares* of the first $n$ integers. 
> > $$\sum^n_{i=1}i^2 = 1 + 2^2 + 3^3 + \dots + n^2 = \frac{n(n+1)(2n+1)}{6}$$
> 
> > [!caution]- Proof 
> > We will prove this through Induction.
> > * We will first show that $n=1$ holds true for the formula $\frac{n(n+1)(2n+1)}{6} = 1*2*3 =1$, which holds.
> > * We now assume that this holds true for some $n=k$, that is $\frac{k(k+1)(2k+1)}{6}$. 
> > 
> > We now need to prove this for $n=k+1$: $$\begin{align}\sum_{i=1}^{k+1}i^2 &= \underbrace{1^2 + 2^2 + \dots + k^2}_{\text{Equivalent to }n=k} + (k+1)^2\\&=\frac{k(k+1)(2k+1)+6(k+1)^2}{6}  \\&= (k+1) \frac{k(2k+1)+6(k+1)}{6} \\&=(k+1)\frac{2k^2+k+6k+6}{6} \\&=(k+1)\frac{2k^2+7k+6}{6}  \\&=(k+1)\frac{(2k+3)(k+2)}{6}  \\&=\frac{(k+1)((k+1)+1)(2(k+1)+1)}{6}\end{align}$$
> > Therefore, this identity holds. 

> Theorem 2.7 
> Prove the following formula for the sum of the *cubes* of the first $n$ integers. 
> $$\sum^n_{i=1}i^3 = \left[ \frac{n(n+1)}{2} \right]^2$$
> > Proof 
> > Left as an exercise to the reader. 

Note that limits can be applied in combination with Sigma Notation (though normally, we evaluate what the Sigma notation evaluates to, then we apply our limits from there). 
