---
updated_at: 2026-10-26T16:11:13.282-04:00
edited_seconds: 1370
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
Next: [[20 — The Fundamental Theorem of Calculus]]
> [!quote] Recommended Reading 
> Section 4.2 of the Stewart Textbook
> [[17— Optimization, Antiderivatives and Sigma Notation]]

> [!caution] Note
> We already did a small portion of this section in the previous lecture, particularly with [[18 — Areas and Distances#Sampling Points]]. 


--- 
# Lecture Notes

## Definite Integrals (LEC) 
Recall that from the previous note that we can define the definite integral of a function between an interval as: 
$$
\lim_{ ||P|| \to 0 } \sum_{i=1}^{N} f(x^*_{i})\Delta x_{i}
$$
We can formally define this as the following: 

> [!theorem] Reimann Sum Definition of a Definite Integral (LEC)
> If $f$ is a function defined on a closed interval $[a,b]$, let $P$ be a partition of $[a,b]$ with partitions of points $x_{0},x_{1},x_{2},\dots x_{n}$, where $a<x_{1}<x_{2}<\dots<x_{n}=b$. 
> 
> We choose sampling points $x^{*}_{i}$ in a partition $[x_{i-1},x_{i}]$, and let $\Delta x_{i}=x_{i}-x_{i-1}$ (our partition width). Let $||P||=\text{max}(\Delta x_{i})$ (by definition of a norm). Then the definite integral of $f$ from $a$ to $b$ is defined as the following: 
> $$\int _{a}^{b}f(x) \, dx = \lim_{ ||P|| \to 0 } \sum_{i=1}^{N} f(x^{*}_{i})\Delta x_{i}$$
> **If** the limit on the right exists. If the limit *does* exist, then $f$ is called integrable in $[a,b]$. 
> > In this notation:
> > * $f(x)$ is called the integrand. 
> > * $a,b$ are the lower and upper limits of integration respectively. 
> >
> > The process of evaluating this Integral is termed as *integration*.
> 
> > The term on the right is termed as the Reimann Sum; that is: 
> > $$\sum_{i=1}^{N} f(x^{*}_{i})\Delta x_{i}$$
> > Is the Reimann Sum of our function.

Note that a Definite Integral **resolves as some number**. It is *independent* of whatever $x$ is (as it is the sum of the areas under the curve). If an area of the curve exists under the $x$ axis, we denote that area as negative, and the corresponding area of the function under the graph is the sum of all positive/negative areas. 

Consider that our limit is *also* present within this definition of the Integral. To be rigorous, then we define now the precise definition of the Integral: 

Take the following: 
$$
\int _{a}^{b}f(x) \, dx =I
$$
This implies that $\forall\epsilon>0,\,\exists\delta>0$ such that: 
$$
\left|I-\sum_{i=1}^{N} f(x^{*}_{i})\Delta x_{i}\right| < \epsilon
$$
For all partitions of $P$ if $[a,b]$ with $||P||<\delta$, and all possible choices of $x^{*_{i}}\in[x_{i-1},x_{i}]$. 
### Example (Precise Integral Definition) 
Take the following function: $f(x)=x^3, x\in[0,1]$. 

Consider now the lower sum: $S_{n}^{L}$; that is we set up $x^{*}_{i}$ as the lower estimate. Consider now the $S_{n}^U$ as the upper sum, where our sampling point is equal to using sampling points as the higher estimate, then: 
$$
S_{n}^{L} \leq I \leq S_{n}^U
$$
We now need to find values for our lower sum and upper sum. 

Finding the upper sum, we define a uniform partition of $\Delta x=\frac{1}{n}$, and $x^{*}_{i}=x_{i}=\frac{i}{n}$ (taking the upper bound), then: 

$$
\begin{align}
S_{n}^U & =\sum_{i=1}^{N} (x_{i}^*)^3 \frac{1}{n} = \sum_{i=1}^{N} \frac{i^3}{n^4}  \\
 & =\frac{1}{n^4}\sum_{i=1}^{N} i^{3} = \frac{1}{n^4}\left[ \frac{n(n+1)}{2} \right]^2  \\
 & =\frac{(n^2+2n+1)}{4n^2}
\end{align}
$$

Choosing the under estimate / lower sum, we now use the same uniform partition, but we take the left hand endpoint, that is $x^{*}_{i }=x_{i-1} = \frac{i-1}{n}$;  then: 
$$
\begin{align}
S_{n}^{L} & =\sum_{i=1}^{N} (x^{*}_{n})^{3} \frac{1}{n} =\sum_{i=1}^{N} \left[ \frac{i-1}{n} \right]^3 \frac{1}{n} \\
 & =\sum_{i=0}^{N-1} \frac{i^3}{n^4} = \frac{1}{n^4}\sum_{i=0}^{N-1} i^3 \\
 & =\frac{1}{n^4}\left[ \sum_{i=1}^{N} i^3-n^3 \right]  & \text{Subtracting the last term} \\
 & =\frac{1}{n^{4}}\left[ \left( \frac{n(n+1)}{2} \right)^2 - n^{3} \right] = \frac{n^2+2n+1}{4n^2} - \frac{1}{n}
\end{align}
$$
Then taking the distance between $S^{L}_{n}$ and $S^{U}_{n}$, taking the following: 
$$
|S_{n}^{L}-S_{n}^{U}|=\left|\frac{n^2+2n+1}{4n^2} - \frac{1}{n} - \frac{(n^2+2n+1)}{4n^2}\right| = \frac{1}{n}
$$
From our above definition, then $\delta=\frac{1}{n}=\implies\delta=\epsilon$, and then prove as usual.

### Integration Bounds
Consider now the following case: How do we consider this, when our upper bound is lower than our lower bound? 
$$
\int ^{1}_{3}f(x) \, dx =?
$$
In this case, if $a>b$ in $\int _{a}^{b} f(x)\, dx$, then this is equal to $-\int_{b}^{a}f(x)\,dx$ (since we traverse the $x$-axis backwards). 

Consider as well if $a=b$; then: 
$$\int _{a}^{a}f(x) \, dx =0$$

## Existence of Integrals 
The question still exists is that: How can we prove that the Reimann Sum limit exists? 

Since the Reimann Sum partitions up our function into infinitely small partitions; then we know that as long as our function is *continuous* on an interval $[a,b]$, then our function is **guaranteed to be integrable** on $[a,b]$. (The proof of this is left as an exercise to the next term). 

### Piecewise Continuity
We define the concept of Piecewise Continuity as the following: 

> [!theorem] Piecewise Continuity
> Only a **finite** number of **jump** discontinuities exist. In this case, for the same closed interval, that function is **also integrable**. (In this case, we take the integral with respects to the bounds of either function as a piecewise expression). 

Other discontinuity types *may* or may not be integrable. The following two definitions above however guarantee integrability. 
## Calculating Integrals
Our definition for the definition of the Definite integral works for $x^{*}_{i}$ and $\Delta x$ will work for any means that we define them. For ease: 

* Regular Partition: $\Delta x = \Delta x_{1} =\Delta x_{2} = \frac{b-a}{n}$
* $x^{*}_{i}$ as the *right-hand endpoint*: $x^{*}_{i}=a + i\Delta x = a+\frac{i(b-a)}{n}$. Where $a$ is the lower bound of the definite integral. 

This lets us use a simpler definition of the Reimann sum for our calculations. 

For instance, take the following: 
$$
\int _{0}^{3}(x^3-5x) \, dx 
$$
Setting up our Integral Definition, then: 

$$
\begin{align}
\int _{0}^{3}(x^3-5x) \, dx   & =\lim_{ n \to \infty } \sum_{i=1}^{N} f\left( a+\frac{i(b-a)}{n} \right) \frac{b-a}{n} \\
 & =\lim_{ n \to \infty }\frac{3}{n}\left[  \sum_{i=1}^{N} \left[ \left( \frac{3i}{n} \right)^3 - 5\left( \frac{3i}{n} \right) \right] \right] \\
 & =\lim_{ n \to \infty } \frac{3}{n}\left[ \frac{27}{n^3}\sum_{i=1}^{N} i^3 - \frac{15}{n}\sum i \right] \\
 & =\lim_{ n \to \infty } \left[ \frac{81}{n^4}\left[ \frac{n(n+1)}{2} \right]^2 - \frac{45(n)(2n+1)}{2n^2} \right] \\
 & =\lim_{ n \to \infty } \left[ \frac{81}{4}\left( 1+\frac{1}{n} \right)^2 - \frac{45}{2}\left( 1+\frac{1}{n} \right) \right]  & \text{Step *}\\
 & =\frac{81}{4} - \frac{45}{2 }=-\frac{9}{4}
\end{align}
$$
For Step \*, exercise is left to the reader as to the algebra behind this. 

### Integral Properties
Recall that an Integral is a *limit*. Thus all the limit laws apply as per usual (refer to them at [[07 — Limit Laws]]): 

$$
\begin{align}
\int _{a}^{b}c \, dx  & = c(b-a) &  c \text{ is a constant} \\
\int _{a}^{b}f(x)\pm g(x) \, dx  & =\int _{a}^{b}f(x) \, dx \pm\int _{a}^{b}g(x)\,dx \\
\int _{a}^{b}cf(x) \, dx  & =c\int _{a}^{b}f(x)\,dx \\ 
\int _{a}^{b}f(x) \, dx  & =\int _{a}^{z}f(x) \, dx + \int _{z}^{b}f(x) \, dx \tag{bound property}
\end{align}
$$
They also have the following order properties. Letting $a\leq b$, and unless otherwise stated, $a\leq x\leq b$: 
$$
\begin{align}
f(x)\geq 0, & \implies \int _{a}^{b}f(x)  \, dx \geq 0 \\
f(x)\geq g(x), & \implies \int_{a}^{b}f(x)\,dx \geq \int _{a}^{b}g(x) \, dx    \\
m \leq f(x) \leq M ,  & \implies m(b-a)\leq \int_{a}^{b}f(x)\,dx \leq M(b-a) \tag{note 1}\\
\left|\int_{a}^{b}f(x)\,dx\right|  & \leq \int_{a}^{b}|f(x)|\,dx \tag{note 2}
\end{align}
$$
* Note 1: This means that the area of the rectangle defined by the max value of the function, will always be greater than or equal to the area of the function, which will always be greater than or equal to the area of the rectangle defined by the smallest value of the function.
	* This is a very powerful function, as you realize that when taking the limit, this allows us to use Squeeze Theorem to prove some integrals. 
* Note 2: Arises from how signs are propagated within integrals: 
$$
\begin{align}
|\int_{a}^{b}f(x)\,dx  & = |A_{1}-A_{2}| \\
\int_{a}^{b}|f(x)|\,dx & =|A_{1}| + |A_{2}|
\end{align}
$$



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
\sum^n_{i=1}i^2 =& = \frac{n(n+1)(2n+1)}{6} \tag{Sum 1.6} \\
\sum^n_{i=1}i^3  & = \left[ \frac{n(n+1)}{2} \right]^2 \tag{Sum 1.7}
\end{align}
$$

Evaluating Definite Integrals is very similar to how we approached limit laws, that being that we want to get the function that we are taking a definite integral of into a form where we can apply one of the following theorems / sums above in order to gain a better sum as to what they are. 

### The Midpoint Rule 
Note that, while we defined in the definition of a definite integral through the Reimann sum as us taking the sum with the sampling point being the middle of the function; that is taking $x_{i} = \frac{1}{2}(x_{i-1}+x_{i})$ and working it out from there. 

## Definite Integral Properties
A Definite Integral follows the following general properties; mostly stemming from the Sum Properties arising from above; although more of them arise from a graphical intuition of the concept of Integrals being the area under a graph. 
$$
\begin{align}
\int _{a}^b c~dx  & = c(b-a) \\
\int_{a}^{b}[f(x)\pm g(x)]~dx & =\int_{a}^b f(x)~dx \pm \int_{a}^b f(g)~dx  \\
\int_{a}^b cf(x)~dx & =c\int_{a}^b f(x)~dx
\end{align}
$$

Note that integrals also has the following property with respects to how we define their bounds: 
$$
\int_{a}^b f(x) ~dx = -\int_{b}^a f(x)~dx
$$
Since $\Delta x = \frac{b-a}{n}$, then $-\Delta x = \frac{a-b}{n}$; and since our integral is in concept defined by the Reimann sum of the function; then this holds true. From this, note that if the bounds are the same, then $\Delta x=0$, then:
$$
\int_{a}^{a}f(x)~dx =0
$$
We can also combine integral bounds: 
$$
\int_{a}^b f(x)~dx + \int_{b}^cf(x)~dx = \int_{a}^c f(x)~dx
$$
Consider this as the equivalent to us adding together both areas under a graph; which are both present / connected to each other at the $b$ boundary. 

The following comparison properties are also true: 
$$
\begin{align}
\implies f(x) \geq 0 ~\text{for}~a\leq x\leq c  & \implies \int_{a}^b f(x)~dx \geq 0 \\
\implies f(x) \geq g(x)~\text{for}~a\leq x\leq b  & \implies \int_{a}^b f(x)~dx \geq \int_{a}^b g(x)~dx \\
\implies m \leq f(x) \leq M~\text{for}~a\leq x\leq b & \implies m(b-a)\leq \int^b_{a}f(x)~dx\leq M(b-a)
\end{align}
$$
Note that the second property states that an order is preserved if we take an integral over an inequality; thus we can prove the last one by simply taking the integral across all of the terms present in the first inequality and using our constant integral rule above to evaluate $\int m$ and $\int M$ as $m(b-a)$ and $M(b-a)$. 