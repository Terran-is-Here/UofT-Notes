---
updated_at: 2026-11-19T14:50:43.029-05:00
edited_seconds: 1200
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Lecture Date: 2026-11-19
Week:
Created: November 15th 2026, 6:00:40 pm
---
Hub: [[ESC194 Hub]]
Previous: [[27 —  The Natural Exponential]]
Next: [[29 — Inverse Trigonometric Functions]]

> [!quote] Recommended Reading 
> Section 6.4\* of the Stewart Textbook. 
--- 
# Lecture Notes
## General Exponentials (LEC) 
Recall our Logarithm Properties: 
$$
\ln x^{p/q} = \frac{p}{q}\ln x
$$
Raising this to the exponent, we find that: 
$$
e^{\ln x^{p/q}} = e^{p/q*\ln(x)} = x^{p/q}
$$
We now define the following: 
> [!theorem] Definition of General Exponents
> $$x^{z} = e^{z\ln x}$$
> Where $x>0$, and $z$ is irrational. 

For instance: 
$$
3^{\sqrt{ 2 }} = e^{\sqrt{ 2 }\ln 3}
$$

Due to being defined in terms of our $e$ (natural exponential) we find that this follows the same similar properties as previous exponent laws, and will not be rewritten for the sake of brevity. 

### General Power Rule & Differentiating (LEC)
From here, we can actually start defining the power rule in a general context. Recall that previously, we only stated it for rational numbers. We will now generalize it for any number in $\mathbb{R}$. 

$$
\frac{d}{dx}x^{r} = rx^{r-1}
$$
The proof is: 
$$
\begin{align}
x^{r}  & = e^{r\ln x} \\
\frac{d}{dx} e^{r\ln x} = e^{r\ln x} \frac{r}{x} =x^{r} * \frac{r}{x}  & = rx^{r-1}
\end{align}
$$
As desired. Chain rule can also be expressed as the following: 
$$
u^{r} = ru^{r-1} \frac{du}{dx}
$$
Where the companion integrals can now be expressed as: 
$$
\int x^{r} \,dx = \frac{x^{r+1}}{r+1} + C \iff r\neq -1, x>0
$$
#### Examples
Consider now the following example: 
$$
\begin{align}
I & = \int \frac{x}{(x^{2}+1)^{\sqrt{ 2 }}}\,dx  & u=x^{2}+1, du=2x \\
 & = \frac{1}{2}\int \frac{1}{u^{\sqrt{ 2 }}} = \frac{1}{2}\left[ \frac{1}{1-\sqrt{ 2 }}u^{1-\sqrt{ 2 }} \right] + C
\end{align}
$$

Consider now: 
$$
f(x) = x^{x}, f'(x) = ?
$$
Note: 
$$
\begin{align}
x^{x}  & = e^{x\ln x} \\
\frac{d}{dx}e^{x\ln x} & = e^{x \ln x} \left( x  * \frac{1}{x} + \ln(x) \right) = x^{x}(1+\ln(x))
\end{align}
$$
### General Bases
Noting that from our definition, if we have some arbitrary base, then: 
$$
p^{x} = e^{x\ln p}
$$
Then: 
$$
\frac{d}{dx}e^{x\ln p} = e^{x \ln p} \ln p = p^{x}\ln p
$$
### Chain Rule 
Note as well that with chain rule, then: 
$$
\frac{d}{dx}p^{u} = \frac{d}{dx}e^{u\ln p} = p^{u}\ln p \frac{du}{dx}
$$
For instance: 
$$
\frac{d}{dx} 2^{3x^{2}} = 2^{3x^{2}}\ln(2)6x
$$

Consider now the following example: 
$$
y = 2^{1/(x-1)}
$$
Differentiating this: 
$$
\begin{align}
e^{\ln 2 / (x-1)} \\
\frac{d}{dx}e^{\ln 2 / (x-1)} = e^{\ln 2 / (x-1)} \frac{\ln 2 (-1)}{(x-1)^{2}} = -2^{1/(x-1)} \frac{\ln_{2}}{(x-1)^{2}}
\end{align}
$$

### Integrating
We can integrate by taking the inverse of our differentiation formula, as is expected: 
$$
\int p^{x}\,dx = \frac{p^{x}}{\ln p} + C \iff p\neq 1, p>0
$$
#### Examples
For instance, take the following: 
$$
\begin{align}
S  & = \int 3x^{2}7^{-5x^{3}}\,dx  & u = -5x^{3}, du=-15x^{2}\,dx \\
 & =\int -\frac{1}{5}7^{u} = -\frac{1}{5}\int 7^{u}\,du  \\
 & = -\frac{1}{5}\left[ \frac{7^{u}}{\ln(u)} \right] + C = -\frac{7^{-5x^{3}}}{5 \ln(7)}+C
\end{align}
$$
## General Logarithms
We can extend the concept of a Logarithm from the following: 
$$
f(x) = \frac{\ln x}{\ln p}, g(x) = p^{x}
$$
Note that $f(g(x))$ gives us the following: 
$$
f(g(x)) = \frac{x \ln p}{\ln p} = x
$$
And: 
$$
g(f(x)) = p^{\ln(x)/\ln(p)} = e^{\ln(p) * \ln(x)/\ln (p)} = e^{\ln(x)} = x
$$
Thus we define: 
$$
\log_{p}(x) = \frac{\ln(x)}{\ln(p)}
$$
Where $p>0, p\neq 1$ as per usual, where: 
$$
\log_{p} p^{x} = x
$$
### Examples
For instance, consider the following: 
$$
\log_{10} 100 = \frac{\ln(10^{2})}{\ln(10)} = 2
$$
 as expected.

$$
\ln_{2}(32) = \frac{\ln(2^{5})}{\ln(2)} = \frac{5\ln{2}}{\ln2} = 5
$$
as expected. 

### Derivative
We define the derivative of the general Logarithmic Function as the following: 
$$
\begin{align}
\frac{d}{dx}\log_{p}(x) = \frac{d}{dx} \frac{\ln x}{\ln p} = \frac{1}{x\ln p}
\end{align}
$$
Note that for arbitrary values of $p$, this defines the base. Recall that we originally defined the logarithm function as the integral of $\int \frac{1}{x}$ from $1 \to x$. 
### Chain Rule 
We can define the chain rule as the following from our above definition: 
$$
\frac{d}{dx}\log_{p}(u) = \frac{1}{u \ln(p)} \frac{du}{dx}
$$
For instance: 
$$
\frac{d}{dx}\log_{7}(2x^{3}-x) = \frac{1}{(2x^{3}-x)\ln_{7}}(6x^{2}-1)
$$
## Estimating the Value of $e$
Recall that: 
$$
\ln(x) = \int_{1}^{x} \frac{1}{t}\,dt
$$
by definition. Let $x=1 + \frac{1}{n}$, thus: 
$$
\begin{align}
\ln\left( 1 + \frac{1}{n} \right)  & = \int_{1}^{1 + 1/n} \frac{1}{t} \,dt < \int_{1}^{1+1/n}1 \,dt & \frac{1}{t} < \frac{1}{1} \implies \int_{a}^{b} \frac{1}{t}\,dt < \int_{a}^{b} 1 \,dt \\
 \ln\left( 1+\frac{1}{n} \right)& =\int_{1}^{1+1/n} \frac{1}{t} \,dt < \frac{1}{n} \\[1.5em]
 e^{\ln(1+1/n)} & < e^{1/n} \\
 \left( 1 + \frac{1}{n} \right)^{n}  & < e
\end{align}
$$
Consider now that: 
$$
\begin{align}
\ln\left( 1+\frac{1}{n} \right)  & = \int_{1}^{1+1/n} \frac{1}{t}\,dt > \int_{1}^{1+1/n} \frac{1}{1+\frac{1}{n}}\,dt  & \frac{1}{t} < \frac{1}{1+\frac{1}{n}}  \\
 & =\ln\left( 1+\frac{1}{n} \right) > \frac{1}{n+1} \\
 & =1+\frac{1}{n}> e^{1/(n+1)}  \\
 & =\left( 1+\frac{1}{n} \right)^{n+1} > e
\end{align}
$$
We see now that: 
$$
\left( 1+\frac{1}{n} \right)^{n} <e < \left( 1+\frac{1}{n} \right)^{n+1}
$$
Consider testing values of $n$: 
* $n=1 \implies 2 < e < 4$
* $n=2 \implies 2.25 < e < 3.375$
* $n  = 3 \implies 2.59 < e < 2.85$
* $n=10^{6} \implies 2.718280 < e < 2.1718283$
* Note how as $n \to \infty$, this approximation approaches $e$, or in other words: 

$$
\lim_{ n \to \infty }  \left( 1+\frac{1}{n} \right)^{n} = e
$$




---
# Pre-Lecture Notes
## General Exponentials and Logarithms
Recall that we defined the following as our cancellation expressions pertaining to the concept of natural logarithms and their corresponding exponential equivalents: 

$$
\begin{align}
\ln(e^{x}) = x \\
e^{\ln(x)} = x
\end{align}
$$

Thus, we find that: 

$$
b^{r} = e^{r\ln(b)} = e^{\ln(b^{r})}
$$

From here, we derive the definition of the general Exponential: 
> [!theorem] General Exponential
> We let the following be the notation that we shall use for the definition of a General Exponential as the following: 
>
> $$b^{r} = e^{r\ln(b)}$$

Consider now that this allows us to extend some of the exponent laws that we derived earlier. 

> [!theorem] Property 1
>
> $$b^{x+y}=b^{x}b^{y}$$
> >
> > [!axiom]- Proof 
> >
> > Consider that with our definition, we find that: $$b^{x+y} = e^{(x+y)\ln(b)} = e^{x\ln(b) + y\ln(b)} = e^{\ln(b^{x}) + \ln(b^{y})} = e^{\ln(b^{x}b^{y})} = b^{x}b^{y}$$

> [!theorem] Property 2
>
> $$b^{x-y} = \frac{b^{x}}{b^{y}}$$
> >
> > [!axiom]- Proof 
> > Consider that with our definition we find that:
> >
> > $$e^{(x-y)\ln(b)}=e^{x\ln(b)-y\ln(b)} = \frac{e^{\ln(b^{x})}}{e^{\ln(b^{y})}} = \frac{b^{x}}{b^{y}}$$
> >
> > As was desired. 

> [!theorem] Property 3
>
> $$(b^{x})^{y} = b^{xy}$$
> >
> > [!axiom]- Proof 
> > Consider that with our definition, we find that: 
> >
> > $$(b^{x})^{y}= e^{y\ln(b^{x})} = e^{xy\ln(b)} = b^{xy}$$
> >
> > As is desired. 

> [!theorem] Property 4
>
> $$(ab)^{x}=  a^{x}b^{x}$$
> >
> > [!axiom]- Proof 
> > Consider that with our definition, we find that: 
> >
> > $$ab^{x} = e^{x\ln ab} = e^{x(\ln(a)+\ln(b))} = e^{x\ln (a) + x\ln(b)} = a^{x}b^{x}$$
 As is desired. 

## Differentiation
From our definition above: 

$$
b^{x} = e^{x\ln(b)}
$$

We correspondingly find the associated derivative of our function as: 

$$
\frac{d}{dx}b^{x} = \frac{d}{dx}e^{x\ln(b)} = \ln(b)e^{x\ln(b)} = b^{x}\ln(b)
$$

> Derivative of the General Exponential
>
> $$\frac{d}{dx}b^{x} = b^{x}\ln(b)$$

Note that this gives us another way to see the perspective of the derivative of $e^{x}$, $\frac{d}{dx}e^{x} = e^{x}\ln(e) = e^{x}$, from the property that $\ln(e) = 1$. 
### Integration
Corresponding from the derivative of the General Exponential, we find that: 

$$
\int b^{x}\,dx = \frac{b^{x}}{\ln(b)} + C
$$

### General Power Rule
Consider now that we defined $b^{x}$ for any arbitrary $x$, thus we can now prove the power rule for any value of $x$: 

$$
\begin{align}
y  & =x^{n} \\
\ln|y| & =n\ln|x|  & \text{use logarithmic differentiation} \\
\frac{y'}{y} & =\frac{n}{x} & \frac{d}{dx}\ln|f(x)|=  \frac{1}{x}dx \\
y^{'}  & =\frac{ny}{x} = \frac{nx^{n}}{x} =nx^{n-1} \\
\end{align}
$$

As is defined for the general power rule; we can now use it for any value of $x$. 

## General Logarithms
Similarly, we note that if $f(x)=b^{x}$, $b>0,b\neq1$, we find that $b^{x}$ is bijective, thus an inverse exists and is defined as the logarithmic function with respects to base $b$ as the following: 

$$
\boxed{\log_{b}y =x \iff y = b^{x}}
$$

Noting that the cancellation equations thus become: 

$$
b^{\log_{b}y}= y\\
\log_{b}(b^{y}) = y
$$

The laws of this function are similar to the function above; and can be found with the same cancellation equations as above. 

### Change of Base
We note that we can now express a logarithm as a term of a change of base from the following expression: 

$$
\begin{align}
b^{y} & =x & \text{take ln}  \\
\ln(b^{y})  & =\ln(x) \\
y\ln(b)  & =\ln(x) \\
y  & =\frac{\ln(x)}{\ln(b)}
\end{align}
$$

Thus, we can find the corresponding term in the exponent by taking the quotient between the natural logarithms of the bases present in the expression. Consider now using our alternative notation, thus we see that: 

$$
\begin{align}
b^{y} & =x \\
\log_{b}(b^{y}) = y\log_{b}(b) = y   &= \log_{b}(x)  \\
\frac{\ln(x)}{\ln(b)} & =\log_{b}(x)
\end{align}
$$

As we can back substitute in the identity we found earlier back into our expression.
## Deriving the Value of $e$
Recall that if $f(x) = \ln(x)$, then $f'(x) = \frac{1}{x}$, where $f'(1)=1$, using this as a limit, we find that: 

$$
\begin{align}
f'(1)  & = \lim_{ h \to 0 } \frac{f(1+h)-f(1)}{h} = \lim_{ x \to 0 }  \frac{f(1+x) - f(1)}{x} & f(x) = \ln(x) \\
 & =\lim_{ x \to 0 }  \frac{\ln(1+x)-\ln(1)}{x} \\
 & =\lim_{ x \to 0 }  \frac{\ln(1+x)}{x} = \lim_{ x \to 0 }  \frac{1}{x}\ln(1+x)  \\
 & =\lim_{ x \to 0 } \ln((1+x)^{1/x})=1
\end{align}
$$

Noting this, we find now that: 

$$
\begin{align}
e = e^{1}  & = e^{\lim_{ x \to 0 } \ln(1+x)^{1/x}} \\
 & =\lim_{ x \to 0 } e^{\ln(1+x)^{1/x}} = \lim_{ x \to 0 } (1+x)^{1/x} = e
\end{align}
$$

Alternatively, set $n=\frac{1}{x}$, then $x= \frac{1}{n}$, and as $x \to 0, n \to \infty$, resulting in the more familiar limit below: 

$$
e = \lim_{ n \to \infty } \left( 1 + \frac{1}{n} \right)^{n}
$$

. 