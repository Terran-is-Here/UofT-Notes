---
updated_at: 2026-11-16T11:50:37.041-05:00
edited_seconds: 810
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 17
Lecture Date: 2026-11-16
Week:
---
Hub: [[ESC194 Hub]]
Previous:  [[26 — The Natural Logarithmic Function]]
Next: [[28 — General Logarithmitic and Exponential Functions]]
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
