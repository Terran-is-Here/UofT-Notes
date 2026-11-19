---
updated_at: 2026-11-18T23:23:22.572-05:00
edited_seconds: 650
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Lecture Date: 2026-11-19
Week:
Created:  November 15th 2026, 6:00:40 pm
---
Hub: [[ESC194 Hub]]
Previous: [[27 —  The Natural Exponential]]
Next: [[29 — Inverse Trigonometric Functions]]

> [!quote] Recommended Reading 
> Section 6.4\* of the Stewart Textbook. 
--- 
# Lecture Notes

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