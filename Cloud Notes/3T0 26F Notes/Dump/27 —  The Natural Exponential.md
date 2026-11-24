---
updated_at: 2026-11-24T13:41:19.476-05:00
edited_seconds: 1060
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 27
Lecture Date: 2026-11-16
Week: 10
Created: November 11th 2026, 4:28:52 pm
---
Hub: [[ESC194 Hub]]
Previous:  [[26 — The Natural Logarithmic Function]]
Next: [[28 — General Logarithmic and Exponential Functions]]
> [!quote] Recommended Reading 
> Section 6.3\* of the Stewart Textbook (not 6.3, 6.3\*). 
> [[25 — Inverse Functions]]

--- 
# Lecture Notes
## Natural Exponentials (LEC)
Consider the following expression, that we have already defined earlier on: 

$$
e^{p/q} \implies \ln(e^{p/q}) = \frac{p}{q}
$$

Consider that we wanted the case previously when we defined CORA in which irrational numbers are also a part of the real numbers, that is $\exists q\in \mathbb{R}$, where: 

$$
\ln q = \pi \implies q = e^{\pi}
$$

Thus we define the following convention: 
> If $z$ is an irrational number, then $e^{z}$ is the unique number, where $\ln e^{z}=z$. 

We also define the following convention: 

$$
\exp(x) \equiv e^{x}, \forall x\in \mathbb{R}
$$

This is known as the natural exponential function. 
### Properties
1. $\ln e^{x}=x$, where $x\in \mathbb{R}$ (from the concept of inverse functions.) 
2. Consider from the graph and the domain of $\ln(x)$, $\ln(x) \forall x>0$, then we find that the range of $e^{x}$ is for all values greater than 0 for all x present in it's domain. 
	1. $e^{x}>0$
3. $e^{0}=1$, as $\ln(1)=0$ (inverse function concept). 
4. $\lim_{ x \to -\infty }e^{x}=0$ (from the graph of $e^{x})$.
	1. Consider that $\ln((x))$ has a vertical asymptote at the $x$ axis, thus our exponential would have one in the $y$ axis. 
5. $e^{\ln(x)}=x$ (inverse function concept) 
6. $e^{a+b}=e^{a}e^{b}$ (Derived from Logarithms, see Properties below.)
7. $e^{-b} = \frac{1}{e^{b}}$ (derived from logarithms)

## Differentiation 
We separate one of the more important properties of the exponential function: 

$$
\frac{d}{dx}e^{x} = e^{x}
$$

As: 

$$
\begin{align}
\ln e^{x}  & = x \\
\frac{d}{dx}\ln(e^{x}) & = \frac{d}{dx} x \\
\frac{1}{e^{x}}* (e^{x})'  & = 1 \\
\implies (e^{x})'   & =e^{x}
\end{align}
$$

We also consider that with chain rule, we thus find that: 

$$
\frac{d}{du}e^{u} = e^{u} \frac{du}{dx}
$$

For instance: 

$$
\frac{d}{dx} e^{kx} = ke^{kx}
$$

### Examples 
Take the following expression: 

$$
f(x) = x^{4}e^{-x}
$$

If we wanted to graph it, we note that the domain is defined for all $x$, where $f \geq 0$ for all $x$ present. Taking the first and second derivative to gain the properties of the graph, we find that: 

$$
\begin{align}
f'(x)  & = 4x^{3}e^{-x} + x^{4}(-1)e^{-x} = x^{3}e^{-x}(4-x) \\
 & \implies f'(x) = 0, x=0,4 \\
 & \implies f'<0  \iff x > 4 \\
 & \implies f' > 0 \iff 0<x<4 \\
 & \iff f' < 0 \iff x<0
\end{align}
$$

Thus, we find that: 

$$
\begin{align}
f(4)  & = 256e^{-4} \approx 4.7 &  \text{local max} \\
f(0)  & = 0  & \text{ local min}
\end{align}
$$

Taking the second derivative: 

$$
\begin{align}
f''(x)  & = x^{2}e^{-x}(x-6)(x-2) \\
 & \implies f'' = 0 \iff x=0,2,6  \\
 & \implies f'' > 0 \iff x>6   & \implies \text{concave up}\\
 & \implies f'' < 0 \iff 2<x<6  & \implies \text{concave down}\\
 & \implies f'' > 0 \iff x <  & \implies \text{concave up}
\end{align}
$$

Thus, $x=6$ and $x=2$ is a point of inflection. Following this information, we can now graph our function as desired. 

### Application
We can use exponentials when modelling some real-world scenarios, for instance in terms of the metabolism of the concentration of a piece of medication: 

$$
c(t) = At^{p}e^{-kt} 
$$

Holding true for $k>0$
## Integration
From our derivative property above, we note that: 

$$
\int e^{x}\,dx = e^{x} +C
$$

And from chain rule, then: 

$$
\int e^{g(x)}g'(x) \,dx = e^{g(x)}+C
$$

For instance; 

$$
\begin{align}
 & =\int \frac{xe^{ax^{2}}}{e^{ax^{2}}+1}\,dx & u=e^{ax^{2}}+1, du=2axe^{ax^{2}}\,dx \\
 & =\int \frac{1}{2au} \,du = \frac{1}{2a} \int \frac{1}{u}\,du \\
 & = \frac{1}{2a} \ln|e^{ax^{2}}+1| + C
\end{align}
$$

Take the following example: 

$$
\begin{align}
 & = \int_{0}^{\sqrt{ 2\ln 3 }} xe^{-x^{2}/2}\,dx   & u=e^{-x^{2}/2} \implies du = -xe^{-x^{2}/2}\,dx \\
 & x=0 \to u=0 \\
 & x =\sqrt{ 2\ln3 } \to u=-\ln 3 \\
 & =-\int_{0}^{-\ln 3}  e^{u} = -[e^{u}]_{0}^{-\ln(3)} = \left[ 1-\frac{1}{3} \right] = \frac{2}{3 }
\end{align}
$$
## Example
Show that: 
$$
e^{x}>1 +x \iff x>0
$$
Consider that: 
$$
e^{x} = 1 + \int_{0}^{x}e^{t}dt = 1 + e^{x}-1 = e^{x}
$$
Note that $e^{x}>1$, as if $x>0$: 
* $e^{0}=1$
* $\frac{d}{dx}e^{x} = e^{x} >0 \iff x>0$, thus function is increasing; thus it is always greater than one. 

Consider now that: 
$$
\begin{align}
1 + \int_{0}^{x} e^{t}\,dt >  \int_{0}^{x}1\,dt= 1+x \\
\implies e^{t}>1+x
\end{align}
$$
Consider now that: 
$$
e^{x} = 1 + \int_{0}^{x} e^{t}\,dt > 1 + \int_{0}^{x} (1+t) \,dt = 1 + x + \frac{x^{2}}{2}
$$
Then: 

$$
e^{x} > 1 + x  + \frac{x^{2}}{2}
$$
Consider now that we can repeat this again, thus: 
$$
e^{x} = 1 + \int_{0}^{x} e^{t}\,dt > 1 + \int_{0}^{x}1 + t + \frac{t^{2}}{2} = 1 + x + \frac{x^{2}}{2} + \frac{x^{3}}{6}
$$
Thus: 
$$
e^{x} > 1 + x + \frac{x^{2}}{2} + \frac{x^{3}}{6}
$$
By induction, we can see that: 
$$
e^{x} > 1 + x + \frac{x^{2}}{2!} + \frac{x^{3}}{3!} + \dots +\frac{x^{n}}{n!}
$$
> [!ila] Note
> This originates from the concept that order is preserved when taking the integral of a set of functions. 

---
# Pre-Lecture Notes
## The Natural Exponential
Consider the natural logarithm, which we have defined earlier as the integral of $\frac{1}{x}$ with respects to $1$ and $x$: 

$$
\ln(x) = \int_{1}^{x} \frac{1}{t}\,dt
$$

Recall that we noted that the first and second derivatives of this function imply that this function is constantly increasing within it's domain: 

$$
\begin{align}
\frac{d}{dx}\ln(x)  & = \frac{1}{x} & \forall x\in[0,\infty), \frac{d}{dx} >0  \\
\frac{d^{2}}{dx^{2}}\ln (x)  & =-\frac{1}{x^{2}} & \forall x\in[0,\infty), \frac{d^{2}}{dx^{2}} < 0 
\end{align}
$$

As such, we note that this function is therefore fully bijective within it's domain (one-to-one). Therefore, there must exist some corresponding inverse function; which we will denote as $\exp(x)$: 

$$\ln (y) = x \iff \exp(x) = y$$

Noting some of the earlier properties that we had with our natural logarithm and extending it to our inverse: 

$$\begin{align}\ln(1) = 0 \iff \exp(0) = 1  \\\ln(e) = 1 \iff \exp(1) = e\end{align}$$

And the corresponding cancellation equations are given to us by the usual: 

$$\exp(\ln(x)) = x\\\ln(\exp(x)) = x$$

Note that the above applies for all values within the range of $\ln(x)$, whereas the one below applies for all values within the range of $\exp(x)$. Note that $\ln(x)$ is not inherently defined for negative numbers. From these properties above, we can actually build an expression for the natural exponent. 

Take the following expression: 

$$
\begin{align}
\ln(e^{r}) = r\ln(e)  & = r \\
\ln(e^{r}) = r  & \implies \exp(r) = e^{r}
\end{align}
$$

Letting $r$ be any rational number; then: 

$$
\exp(x) = e^{x} \iff \ln(e^{x}) = x
$$

Thus the cancellation equations above become: 

$$
e^{\ln x} = x\\ \ln(e^{x}) =x
$$

### Properties
Natural Exponentials also share the following properties: 
* $e^{x+y}=e^{x}e^{y}$
  Proven by taking note that $\ln(e^{x}e^{y}) = \ln (e^{x})+\ln(e^{y})  =x+y \implies=e^{x+y}$, as is desired. 
* $e^{x-y} = \frac{e^{x}}{e^{y}}$
  Proven by taking note that $\ln(e^{x}e^{-y}) = \ln\left( \frac{e^{x}}{e^{y}} \right) = \ln(e^{x})-\ln(e^{y}) = x-y \implies e^{x-y}=\frac{e^{x}}{e^{y}}$
* $(e^{x})^{y} = e^{xy}$
  Proven by taking note that $\ln((e^{x})^{y})=y\ln(e^{x}) = xy \implies e^{xy}=(e^{x})^{y}$, as was desired. 
### Differentiating
Consider now, what would be the derivative of $e^{x}$? Let $f(x) =y= e^{x}$, then we note that $f^{-1}(y)=\ln(y)=x$ as per our differentiation formulas. 

Differentiating with respects to $\ln(y)$ gives us: 

$$
\begin{align}
\frac{d}{dx}\ln(y)  & =\frac{d}{dx}x \\
\frac{1}{y} \frac{dy}{dx}  & = 1 \\
\frac{dy}{dx}  & =y \implies \frac{dy}{dx}=e^{x}
\end{align}
$$

In other words, the derivative of $e^{x}$ is itself $e^{x}$. Note that extending this with the following leads to us using chain rule as per usual. 

$$\frac{d}{dx} e^{u(x)} =e^{u(x)} \frac{du}{dx}$$

## Integrating 
Since $\frac{d}{dx}e^{x} = e^{x}$, it follows suit that it's antiderivative is also some $e^{x}+C$, thus calculating integrals for such a function are trivial: 

$$
\int e^{x}dx = e^{x} + C
$$

Our other properties such as $u$ substitution apply as per usual: 

$$
\begin{align}
 & =\int x^{2}e^{x^{3}}dx & u=x^{3}, du = 3x^{2}dx \implies \frac{1}{3}du = x^{2}dx \\
 & =\int \frac{1}{3}e^{u}du  \\
 & =\frac{1}{3}[e^{u}] +C  \\
 & =\frac{1}{3}e^{x^{3}} + C
\end{align}
$$
