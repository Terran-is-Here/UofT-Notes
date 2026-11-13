---
updated_at: 2026-11-13T13:57:18.553-05:00
edited_seconds: 1490
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 26
Lecture Date: 2026-11-13
Week:
Created: November 11th 2026, 1:38:25 pm
---
Hub: [[ESC194 Hub]]
Previous: [[25 — Inverse Functions]] 
Next: [[27 —  The Natural Exponential]]
> [!quote] Recommended Reading 
> Section 6.2\* of Stewart. 
> Not to be confused with Section 6.2 normally. 
--- 
# Lecture Notes
## Logarithmic Functions 
We start with a definition: 
> [!theorem] Logarithmic Function Definition
> A logarithmic function is a *non-constant* differentiable function $f$, defined for $x\in \{ \mathbb{R},(0,\infty) \}$ such that for all $a>0$ and $b>0$, $f(a\cdot b) = f(a)+f(b)$. 

From this definition, we actually see that: 
> $$f(1) = 0$$
> > *Proof*
> > $$f(1*1) = f(1) + f(1) \implies f(1) = 2f(1) \implies f(1) = 0$$

> $$f\left( \frac{1}{x} \right)= -f(x)$$
> *Proof*
> > $$0 = f(1) = f\left( x\cdot \frac{1}{x} \right) = f(x) + f\left( \frac{1}{x} \right) \implies -f(x) = f\left( \frac{1}{x} \right)$$

> $$f\left( \frac{x}{y} \right) = f(x)-f(y)$$
> *Proof*
> > $$f\left( \frac{x}{y} \right) = f\left( x * \frac{1}{y} \right) = f(x) + f\left( \frac{1}{y} \right) \implies f\left( \frac{x}{y} \right) = f(x) - f(y)$$

> Property 4
> $$f'(x) = \frac{1}{x}f'(1)$$
> *Proof*
> > Consider the following expression, taking this from the limit definition, then: 

$$
\begin{align}
f'(x) & =\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} &   \text{let }x=1 \\
& =\lim_{ h \to 0 } \frac{f\left( 1+\frac{h}{x} \right)-f(1)}{h} & \text{let } k = \frac{h}{k} \\
& =\lim_{ h \to 0 } \frac{f\left( 1+\frac{h}{x} \right)-f(1)}{\frac{x*h}{x}} \\
& =\frac{1}{x}\lim_{ k \to 0 } \frac{f(1+k)-f(1)}{k}  & \text{Choose }f'(1) = 1 \\
f'(x)& = \frac{1}{x}f'(1)
\end{align}
$$
From our work above we actually find that using FToC, that: 
$$
f(x) = \int_{1}^{x} \frac{1}{t}\,dt = \ln(x)
$$
Note that our definition for what $f'(1)$ is actually determines what our logarithm's base is. 
### Properties
1. Note that $\frac{d}{dx}\ln(x) = \frac{1}{x}$. Since our function is defined for $x>0$, then our derivative is always increasing. 
2. Note that $\ln(x)$ is continuous due to it's differentiability. 
3. $\forall x>1, \ln(x) >0$ (From the concept that this is the area under the graph of $\frac{1}{x}$ from $(1,x)$). 
	1. For $0<x<1$, $\ln(x)<0$ from our integral property above as well.
4. $\ln(a\cdot b) = \ln(a) +  \ln(b)$ (From our defining statement, though we can prove it too.): 
   $$\frac{d}{dx}\ln(x), \frac{d}{dx}\ln(ax) \to \frac{1}{ax}a = \frac{1}{x}$$
   Noting that the derivative of $\ln(ax)$ and $\ln(x)$ share the same constant we note that taking the antiderivative gives us that: 
   $$\ln(ax) = \ln(x) + c\\x=1 \implies \ln(a) = \ln(1) + c \implies \ln(a) = C\\ \implies \ln(ax) = \ln (a) + \ln(x)$$
5. Rational Power Property $$\ln(x^{p/q}) = \frac{p}{q}\ln x$$
   Consider that $\ln(x^{3}) = \ln(x) + \ln(x) + \ln(x) = 3\ln(x)$. Consider now that $\ln(x) = \ln(x^{1/3}) + \ln(x^{1/3})+\ln(x^{1/3}) \implies \ln(x^{1/3}) = \frac{1}{3}\ln(x)$. 
   Thus, applying the chain rule:
   $$\frac{d}{dx}\ln(x^{p/q}) \to \frac{1}{x^{p/q}}* \frac{p}{1}x^{p/q-1} = \frac{\frac{p}{q}*1}{x} = \frac{d}{dx}\left[ \frac{p}{1}\ln(x) \right]$$
   Noting that they share the same antiderivative, we see that:
   $$\ln(x^{p/q}) = \frac{p}{q}\ln(x) + C$$
   Noting that $x=1$ implies $C=0$, thus $\ln(x^{p/q}) = \frac{p}{q} \ln(x)$. 
6. The *range* of $\ln(x)$ is $-\infty,+\infty$
   The proof for this can be done by first, imposing that $M>0$. Taking this M as a very large value, we can use a variant of $\epsilon-\delta$ to prove this, that is to show that :
   $\ln(x) >M$ for $x>x_{d}$. Taking the proof, note that:
   $$\ln(2) = \int_{1}^{2} \frac{dt}{t}>0$$
   Taking the property that for some $n$ in the real number, we can see that $n\ln(2) > M$. Thus we can set that $x_{d}=2^{n}$. Thus we see that: 
   $$\ln(x) > M \iff x>x_{d}=2^{n}$$
   When $n > \frac{M}{\ln2}$. Thus we find that $\lim_{ n \to \infty }\ln(x)=\infty$. 
	1. It is an exercise to the reader is to show that $\lim_{ x \to ^{+}0 }\ln(x) = -\infty$. 
7. From IVT, we can see that for some number $e$, $\ln(e) = 1$.
   Or in other words, $$\ln(e) = \int_{1}^{e} \frac{dt}{t} = 1$$
8. $$\ln(e^{p/q}) = \frac{p}{q}\ln(e) = \frac{p}{q}$$
   (As per our earlier properties) 
9. The convention is normally is $\ln(x) = \log_{e}(x)$.
10. Our function is concave down, but constantly increasing:
    $$\begin{align}
	\ln(x)' &= \frac{1}{x} > 0 &\forall x>0 \text{ per definition}\\
	\ln(x)''& = -\frac{1}{x^{}} < 0 
	\end{align}$$

### Differentiation
For extending this in terms of the chain rule, we see that: 
$$
\frac{d}{dx}\ln(u) = \frac{\frac{1}{u}du}{dx}
$$
As per our usual definitions, note that our $\ln(x)$ requires $x>0$, thus the domain of the corresponding function must comply with this as it's range. For instance, $\ln(1-2x^{2})$, then it's derivative is equivalent to: 
$$
\begin{align}
f(x)  & = \ln(1-2x^{2}) \\
f'(x) & =\frac{-4x}{1-2x^{2}}
\end{align}
$$
Noting that the restriction of this function are $1-2x^{2}>0$, or in other words, $-\frac{1}{\sqrt{ 2 }}<x< \frac{1}{\sqrt{ 2 }}$ is the domain of our function; noting that $f'(x)=0 \implies x=0$ as a local maximum. 

Consider now the following logarithm: 
$$
f(x) = \ln|x|
$$
Consider as it is an even function, and is equivalent to the following in terms of a piecewise function: 
$$
f(x) = \begin{cases}
\ln(x) & : x>0  \\
\ln(-x) & :x<0
\end{cases}
$$
Taking the derivative, we find that: 
$$
f'(x) = \begin{cases}
\frac{1}{x} & : x>0  \\
\frac{1}{-x}*-1 = \frac{1}{x} & : x<0
\end{cases}
$$
That is, $f(x) = \ln|x| \implies f'(x) = \frac{1}{x}$, noting that the integral of this function as per our FToC gives us that: 
$$
\int_{1}^{x} \frac{1}{x}dx = \ln|x| +C
$$
### Examples
For instance, take the following expression: 
$$
f(x) = \ln|1-2x^{2}|
$$
Note that this allows us now to see that we can allow arguments which would normally result in a negative. For instance, for $x^{2}> \frac{1}{2}$, then we get $\ln(2x^{2}-1)$, taking the derivative, we get the same one as earlier; taking a form very similarly shaped to an asymptote graph with two vertical asymptotes present at the same restrictions that we have defined earlier. 

---
# Pre-Lecture Notes
## The Natural Logarithmic Function
We define the Natural Logarithmic function as the following expression: 
$$
\ln x = \int_{1}^{x} \frac{1}{x}\,dx
$$
Or in other words, the area under the reciprocal expression $\frac{1}{x}$ from $x\in[1,x]$. Note that this form of integral was discussed within the Fundamental Theorem of Calculus (specifically, [[20 — The Fundamental Theorem of Calculus#^d40ade|FTC1, though both are in this link]], retaking it here): 
$$
\frac{d}{dx}\int_{a}^{x}f(t)\,dt = f(x)
$$
Then we see that: 
$$
\frac{d}{dx}\ln x = \frac{1}{x}
$$
Which is a *very useful expression for evaluating some properties of the natural logarithmic function.* 
### Properties of Ln(x) 
The textbook actually goes into a series of proofs pertaining to the nature of this function. For the purposes of this section, let $a,x$ and any other variables be positive numbers, and let $r$ be a rational number. 

> [!theorem]- Property 1: 
> $$\ln(xy)=  \ln(x) + \ln(y)$$
> > [!axiom]- *Proof.*
> > To prove this, first consider a function with any positive number $a$ that is some $\ln (ax)$, then taking the derivative of this gives us the following: 
> > $$\frac{d}{dx}\ln(ax) = \frac{1}{ax} \frac{d}{dx}(ax) = \frac{1}{ax}a = \frac{1}{x}$$
> > We note that $\ln (x)$ and $\ln(ax)$ share the same derivative, thus $\ln(ax)$ must differ by some **constant value**, that is: 
> > $$\ln (ax) = \ln(x) + C$$
> > Note that if $x=1$; then $\int_{1}^{1} \frac{1}{x}dx = 0$, and thus $\ln(1)=0$, then we get the following: 
> > $$\ln(a) = C$$
> > Thus we find that: 
> > $$\ln(ax) = \ln(x) + \ln(a)$$
> > Note that $a$ is any arbitrary positive number, substituting $a=y$ gets us our desired result. 

> [!theorem]- Property 2: 
> $$\ln\left( \frac{x}{y} \right)=\ln x-\ln y$$
> > [!axiom]- *Proof.*
> > Consider the earlier property that we proved earlier, that $\ln(ax) = \ln(x) + \ln(a)$. 
> > Taking $a=\frac{1}{y}$ then gives us the following if we consider the following expression: 
> > $$\begin{align}\ln(ay) &  = \ln (a) + \ln (y) \\\implies a=\frac{1}{y}  & \implies \\\ln\left( \frac{1}{y}y \right) & = \ln\left( \frac{1}{y} \right) + \ln y & \ln(1) = 0 \\0  & = \ln\left( \frac{1}{y} \right) + \ln(y) \\-\ln(y)  & =\ln\left( \frac{1}{y} \right)\end{align}$$
> > Then retaking our expression from earlier: 
> > $$\begin{align}\ln\left( \frac{x}{y} \right)  & + \ln(x)-\ln\left( \frac{1}{y} \right) \\& =\ln(x) - \ln (y)\end{align}$$
> > As desired from earlier. 

> [!theorem]- Property 3 
> $$\ln(x^{r})=r\ln x$$
> > [!axiom]- Proof
> > Consider the case of what this is implying: 
> >$$\ln(x^{r} = \underset{r \text{ times}}{a\times a\times a\times a})$$
> >Note that from our first property, we can extend it to an arbitrary length: $$\ln(abc) = \ln(a) + \ln(b) + \ln (c)$$
> > > Corollary
> > > Take $\ln(abc)$, then let $d=ab$, thus $\ln(dc) = \ln(d) + \ln(c) =\ln(ab) + \ln(c) =\ln(a)+\ln(b)+\ln (c)$
> > 
> > From this corollary, we can see that this is equivalent to our expression from above, then
> > $$\ln(x^{r}) = \underbrace{\ln(x) + \ln(x) + \dots + \ln(x)}_{r\text{ times}} = r\ln(x)$$
> > As is desired. 

From the properties above, we can now also solve for the corresponding *limit* properties of the function which are listed below: 

> $$\lim_{ x \to \infty }\ln(x) = \infty\\\lim_{ n \to ^{+}0 } \ln(x)=-\infty$$

> Proof of Limit Property 1
> Consider $x=2^{n}$, noting that $x\to \infty$ when $n \to \infty$, thus: 
> $$\lim_{ x \to \infty } \ln(x) = \lim_{ n \to \infty } \ln(2^{n}) = \lim_{ n \to \infty } n\ln(2) \implies \ln(2)\lim_{ n \to \infty }n$$
> Thus from this, we see that this would diverge into infinity. 

> Proof of Limit Property 2
> Consider $x=\frac{1}{n}$, where $x\to 0^{+}$ when $n \to \infty$, then: 
> $$\lim_{ x \to ^{+}0 } \ln(x) = \lim_{ n \to \infty } \ln\left( \frac{1}{n} \right) = -\lim_{ n \to \infty } \ln(n) = -\infty$$
> Note that last step relied on the statement that we derived in the earlier section (that is, the limit of a natural logarithm diverges into infinity when taking the limit). 

Consider as well the derivative properties of some $\ln (x)$: 
> Let $f(x) = \ln(x)$, then $\forall x>0$
> $$f'(x)=\frac{df}{dx} = \frac{1}{x}>0$$
> $$\frac{d^{2}f}{dx^{2}}=f''(x) = -\frac{1}{x^{2}}<0$$
> Which means that, for all values of $x\in[0,\infty)$, our parent function is *increasing* over an interval whilst being concave down. 

### Euler's Number
Note that $\ln(x)$ is continuous within a closed interval, and that it ranges from $-\infty,\infty$ within the interval of $[0^{+}, \infty)$. Thus from the Intermediate Value Theorem, there exists some value $c$ where $\ln(c) = 1$. This value is actually $e$, Euler's Number: 
$$
e \approx 2.718
$$
## Logarithmic Differentiation
Recall that $f(x)=\ln(x) \implies f'(x) = \frac{1}{x}$. From chain rule, then: 
$$
\frac{d}{dx}\ln(u) = \frac{1}{u} \frac{du}{dx}
$$
Or in Lagrange's Notation, we find that: 
$$
\frac{d}{dx}\ln(g(x)) = \frac{g'(x)}{g(x)}
$$
This is a very powerful tool of notation when combining this with our properties from above; we find that we can turn a complex expression of products and exponents into a simpler set of products and addition equations instead, something that we can analyze much more easier. 

Consider as well that we can take the logarithm on both sides of an expression; and take a derivative as per usual. Since $\ln$ makes it much easier to calculate some derivatives due to it's properties, we can also use it to simplify the derivative of an overall function. For instance, take the following function: 

$$
y = \frac{x^{3/4}\sqrt{ x^{2}+1 }}{(3x+2)^{3}}
$$
Taking the logarithm on both sides, we find that: 
$$
\ln y = \ln\left( \frac{x^{3/4}\sqrt{ x^{2}+1 }}{(3x+2)^{3}} \right)
$$
Expanding this out fully: 
$$
\begin{align}
\ln y  & = \ln(x^{3/4}\sqrt{ x^{2}+1 }) - \ln((3x+2)^{3}) \\
   & =\frac{3}{4}\ln x + \frac{1}{2}\ln(x^{2}+1) - 3\ln(3x+2) \\
\frac{d}{dx}\ln y & =\frac{d}{dx}\left[\frac{3}{4}\ln x + \frac{1}{2}\ln(x^{2}+1) - 3\ln(3x+2)\right] \\
\frac{1}{y} \frac{dy}{dx} & =\frac{3}{4x} + \frac{1}{2(x^{2}+1) } - \frac{3}{3x+2} \\
\frac{dy}{dx} & = y\left[ \frac{3}{4x} + \frac{1}{2(x^{2}+1)} - \frac{3}{3x+2} \right]  \\
 & =\left( \frac{x^{3/4}\sqrt{ x^{2}+1 }}{(3x+2)^{3}} \right)\left[ \frac{3}{4x} + \frac{1}{2(x^{2}+1)} - \frac{3}{3x+2} \right]
\end{align}
$$
The expansion from here is tedious, but most of the conceptual work has been finished. Note that when we perform differentiation in this method, we often have to take some term of chain rule on the left side; then correspondingly back substituting the original expression onto our derivative. 

## Logarithmic Integration
Consider now the function $f(x)$ as the following expression: 
$$
f(x) = \ln|x|
$$
Note that then, this is defined as the following expression: 
$$
f(x) = \begin{cases}
\ln x &:x\geq  0 \\
\ln(-x)  & : x<0
\end{cases}
$$
Thus, differentiating this gives us the following: 
$$
f'(x) = \begin{cases}
\frac{1}{x} : x\geq 0  \\
\frac{1}{x}: x < 0 
\end{cases}
$$
Note that since it's equivalent to $\frac{1}{x}$ in both, we find that: 
$$
\frac{d}{dx}\ln|x| = \frac{1}{x}
$$
Thus; 
$$
\boxed{\int \frac{1}{x}\,dx = \ln|x| + C}
$$
This has **major** implications for integration: We can now integrate functions which are now reciprocals! 
### Application
> A trivial example, consider the following integral: 
> $$\int_{1}^{e} \frac{\ln x}{x}\,dx$$

Using our properties and u-substitution, we find that:
$$\begin{align}&=\int_{1}^{e} \frac{\ln x}{x}\,dx & u = \ln x \implies du = \frac{1}{x}dx \\&=\int_{0}^{1}u\,du = \left[ \frac{u^{2}}{2} \right]^{1}_{0} = \frac{1}{2}\end{align}$$

> A more interesting example, consider the following integral: 
> $$\int \tan x \,dx$$

Expanding out that tangent expression: 
$$
\int \frac{\sin x}{\cos x}\,dx
$$
Thus: 
$$
\begin{align}
 & =\int \frac{\sin x}{\cos x}\,dx  & u = \cos x \implies du = -\sin x \,dx \\
 & =\int-\frac{1}{u}\,du = -\int \frac{1}{u}\,du \\
 & = -\ln|u| + C  \\
 & =-\ln|\cos x| + C  & \text{using log rules}\\
 & =\ln \left| \frac{1}{\cos x}\right|+C = \ln|\sec x| +C  \\
\end{align}
$$

