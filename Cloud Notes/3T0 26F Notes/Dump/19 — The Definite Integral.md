---
updated_at: 2026-10-18T22:27:30.514-04:00
edited_seconds: 300
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 19
Lecture Date: 2026-10-22
Week: 7
Created: October 18th 2026, 10:02:14 pm
---
Hub: [[ESC194 Hub]]
Previous: [[18 — Areas and Distances]]
Next: N/A
> [!quote] Recommended Reading 
> Section 4.2 of the Stewart Textbook
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Definite Integrals
Recall that we defined the following expressions for expressing the area below a graph as the sum of numerous rectangles, then taking the limit as the number of those rectangles approached infinity. 
$$A=\lim_{ n \to \infty } L_{n} = \lim_{ n \to \infty } \sum_{n=1}^N~f(x_{x})\Delta x$$
We can define this more acutely: 
> [!theorem] Definite Integrals
> Letting $f$ be a function defined for $[a,b]$; we can subdivide this interval into $n$ intervals of equal width $\Delta x = \frac{b-a}{n}$; letting $x_{0}=a$ and $x_{n}=b$ for a series of intervals defined by $x_{0},x_{1},\dots,x_{n}$, and letting $x_{1}^{*},x_{2}^{*},\dots,x_{n}^{*}$ being any sample points within this subintervals; that is $x_{i}^*$ lies within $(x_{i-1},x_{i})$, then the definite interval of $f$ from $a$ to $b$ is: 
> $$\int_{a}^b f(x)~dx =  \lim_{ n \to \infty } \sum_{n=1}^N~f(x^*_{x})\Delta x$$
>
> Where the precise definition of an integral is the following: 
> $$\begin{align}\forall\epsilon>0, \exists N \\\left|\int _{a}^{b}f(x)~dx-\sum ^{n}_{i=1}f(x_{i}^*)\Delta x  \right|<\epsilon \\\forall n>N\land \forall x_{i}^* \in[x_{i-1},x_{i}]\end{align}$$
> > Or, in one big summary; if we note that if we take the integral as the right-most end points; that is for some $x_{i}^*=x_{i}$; then:
> > $$\int _{a}^{b}f(x)~dx = \lim_{ n \to \infty } \sum_{i=1}^{n}f(x_{i})\Delta x$$
> > Where
> > $$\Delta x=\frac{b-a}{n}, x_{i}=a + i\Delta x$$

Note that the summation term that we had on the right side there is termed the *Reimann sum*. Note that if a function falls below the $x$ axis in this context; we define the area under those rectangles as negative. 

The following theorem thus follows this definition: 
> Theorem
> If $f$ is continuous on a closed interval $[a,b]$, or if $f$ has only a **finite** number of jump discontinuities, then $f$ is integrable on $[a,b]$; that is, the definite integral exists. 

## Evaluating Definite Integrals
Evaluating Definite Integrals under the Reimann Sum definition of a Definite Integral thus requires us to use the definitions of Sigma Notation, something that we have already tackled in depth in [[17— Optimization, Antiderivatives and Sigma Notation]]. These have been repasted onto here for quicker reference; although proofs are present on the corresponding page. 

$$
\begin{align}
\sum_{x=1}^n 1 &= n \tag{Sum 1.1} \\
\sum_{x=m}^nca_{i} &= c\sum_{x=m}^na_{i} \tag{Sum 1.2} \\
\sum^n_{x=m}a_{i}+b_{i} & = \sum_{x=m}^na_{i} + \sum ^n_{x=m}b_{i} \tag{Sum 1.3} \\
\sum^n_{x=m}a_{i}-b_{i} & = \sum_{x=m}^na_{i} - \sum ^n_{x=m}b_{i} \tag{Sum 1.4}  \\
\sum^n_{i=1}i  & = \frac{n(n+1)}{2}\tag{Sum 1.5} \\
\sum^n_{i=1}i^2 =& = \frac{n(n+1)(2n+1)}{6} \tag{Sum 1.6}
\end{align}
$$
