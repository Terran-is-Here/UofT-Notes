---
updated_at: 2026-11-23T11:33:22.090-05:00
edited_seconds: 1570
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 30
Lecture Date: 2026-11-23
Week: 11
Created: November 20th 2026, 11:19:57 am
---
Hub: [[ESC180 Hub]]
Previous: [[29 — Inverse Trigonometric Functions]]
Next: [[31 —Differentials and Separable Equations]]
> [!quote] Recommended Reading 
> Section 6.8 of the Stewart Textbook
> [[13 — Mean Value Theorem, Linear Approximations and Differentials#Cauchy's Mean Value Theorem]] (as we use it for the proof of l\`Hospital's rule). 

> [!caution] Note
> This note's pre-lecture notes have not been fully written at the time that we got to this lecture in the sequence. 
> L\`Hospital's Rule is notated as  LHoR for this note (the apostrophe and escaping the formatting was annoying) 

--- 
# Lecture Notes
## LHoR (LEC) 
Take the following example of a limit that we had proved earlier: 

$$
\lim_{ x \to 0 } \frac{\sin x}{x} =?
$$

We previously proved this through a geometric argument, but what if we didn't know that method? We note that this evaluates to $\to \frac{0}{0}$ as we take the limit. From here, we can actually use LHoR.

### LHoR (0/0)
> [!theorem] LHoR ($\frac{0}{0}$)
> If $f(x) \to0$, $g(x) \to0$ as $x\to \pm \infty$, or $x\to c$, or $x \to c^{\pm}$, then: 
>
> $$\lim_{ x \to c }  \frac{f'(x)}{g'(x)} = L \implies  \lim_{ x \to c }  \frac{f(x)}{g(x)} =L$$

Retaking our earlier expression then: 

$$
\lim_{ x \to 0 }  \frac{\sin x}{x} =?
$$

Letting $f(x) = \sin x \implies f'(x) = \cos(x)$, then $g(x) = x \implies g'(x) = 1$, then: 

$$
\lim_{ x \to 0 }  \frac{\cos(x)}{1} = 1 \implies \lim_{ x \to 0 }  \frac{\sin x}{x} = 1
$$

Consider now as well the following expression: 

$$
\begin{align}
\lim_{ x \to 0 }  \frac{\sin x}{\sqrt{ x }}  & \to 0  & \frac{d}{dx}\sin x = \cos x, \frac{d}{dx}\sqrt{ x} = \frac{1}{2\sqrt{ x }} \\
\lim_{ x \to 0 } 2\sqrt{ x }\sin x & = 0 \\
\lim_{ x \to 0 } 2\sqrt{ x }\sin x &  = 0 \implies \lim_{ x \to 0 } \frac{\sin x}{\sqrt{ x }} = 0
\end{align}
$$

Consider now the following expression: 

$$
\begin{align}
\lim_{ x \to 0 }  \frac{e^{x}-x-1}{3x^{2}}  & \to  \frac{0}{0}  & \frac{d}{dx}(e^{x}-x-1) = e^{x}-1, \frac{d}{dx}(3x^{2}) = 6x \\
\lim_{ x \to 0 }  \frac{e^{x}-1}{6x}  & \to \frac{0}{0} & \frac{d}{dx}(e^{x}-1) = e^{x}, \frac{d}{dx}(6x) = 6 \\
\lim_{ x \to 0 }  \frac{e^{x}}{6} = \frac{1}{6} \\
\lim_{ x \to 0 }  \frac{e^{x}}{6} =\frac{1}{6} \implies \lim_{ x \to 0 }  \frac{e^{x}-1}{6x} = \frac{1}{6} \implies \lim_{ x \to 0 }  \frac{e^{x}-x-1}{3x^{2}} = \frac{1}{6}
\end{align}
$$

Note that there are ways where this could go wrong, such as the following: 

$$
\begin{align}
\lim_{ x \to 0 }  \frac{x^{3}+x}{2+x-2\cos x}  & \to \frac{0}{0} & \frac{d}{dx}(x^{3}+x) = 3x^{2}+1, \frac{d}{dx}(2+x-2\cos(x)) = 1+2\sin x\\
\lim_{ x \to 0 } \frac{3x^{2}+1}{1+2\sin x}  & = \frac{1}{1} = 1 & \lim_{ x \to 0 } \frac{3x^{2}+1}{1+2\sin x} = 1 \implies \lim_{ x \to 0 }  \frac{x^{3}+x}{2+x-2x\cos(x)} = 1
\end{align}
$$

This one went right, but now consider the following case: 

$$
\begin{align}
\lim_{ x \to 0 } \frac{6x}{2\cos x}  & = \frac{0}{0} \\
\lim_{ x \to 0 }  \frac{6}{-2\sin x}  & = \pm \infty  & \text{wrong, l`Hospital Rule only works on Indeterminates.}\\
\lim_{ x \to 0 } \frac{0}{-2\cos x}
\end{align}
$$

### Proof — Cauchy MVT (LEC) 
Before we prove LHoR, we need to prove the Cauchy MVT first: 

The Cauchy MVT is very similar to the base MVT, in fact we use Rolle's Theorem to generalize it to a ratio of any functions. 
> Given two functions $f,g$  differentiable on $(a,b)$, and continuous on $[a,b]$, and $g' \neq0$ on $(a,b)$, then there must exist some number $r$ such that: 
>
> $$\frac{f'(r)}{g'(r)}= \frac{f(b)-f(a)}{g(b)-g(a)}$$

To prove this, consider Rolle's Theorem: 

$$
\begin{align}
\text{if } G(a) = G(b) = 0,  \\
\exists r\in(a,b) \to G'(r) = 0
\end{align}
$$

Let's define the following function $G(x)$

$$
G(x) = [g(b)-g(a)][f(x)-f(a)] - [g(x)-g(a)][f(b)-f(a)]\\
G(b)=G(a)=0
$$

Then simply differentiating this, then: 

$$
G'(x) = [g(b)-g(a)]f'(x) - g'(x)[f(b)-f(a)]
$$

We know that Rolle's Theorem applies onto this, then:

$$
\begin{align}
G(r) = 0  & = [g(b)-g(a)]f'(r) - g'(r)[f(b)-f(a)] \\
 \frac{f'(r)}{g'(r)} & = \frac{f(b)-f(a)}{g(b)-g(a)}
\end{align}
$$

Note that: 

$$
g'(c) = \frac{g(b)-g(a)}{b-a} \implies g'(x) \neq0 \implies g(b)-g(a) \neq0
$$

From this theorem, we can now prove LHoR. 
### l\`Hospital's Rule 
Consider the following, as $x\to c^{+}$, where: 

$$
\begin{align}
\lim_{ x \to c^{+} } f(x) \to 0 \\
\lim_{ x \to c^{+} } g(x) \to 0
\end{align}
$$

Where we note that $\frac{f'(x)}{g'(x)} \to L$. We want to prove that $\frac{f(x)}{g(x)} \to L$

Consider the interval where $[c,c+h]$, where we can apply the Cauchy MVT: 

$$
\begin{align}
x\in [c,c+h]  & \implies \exists c_{2} \in [c,c+h] \text{ s.t.} & \text{from cauchy MVT} \\
\frac{f'(c_{2})}{g'(c_{2})}  & = \frac{f(c+h)-f(c)}{g(c+h)-g(c)}  & g(c)=f(c) = 0\\
\frac{f'(c_{2})}{g'(c_{2})}  & =\frac{f(c+h)}{g(c+h)} & \text{taking } \lim_{ h \to 0 }  \\
\lim_{ h \to 0 }   & \implies \lim_{ c_{2} \to c }  \implies \\
\lim_{ h \to 0 } \frac{f'(c_{2})}{g'(c_{2})}  & = \frac{f'(c)}{g'(c)} = \lim_{ h \to 0 } \frac{f(c+h)}{g(c+h)} = \lim_{ x \to c^{+} } \frac{f(c)}{g(c)}\\
\implies \lim_{ x \to c^{+} } \frac{f(x)}{g(x)} & =\frac{f'(c)}{g'(c)} =L


\end{align}
$$

Note to extend this to infinity, then we simply set $x=\frac{1}{t}$, then $\lim_{ t \to 0 }$, and then solve from there as per usual. 
## LHoR For Infinities
> [!caution] Note
> From this point afterwards, this was written on 11-23. 

Consider the case of LHoR in the case of $\frac{\infty}{\infty}$, we can prove it by taking the following: 

Consider that if $f(x),g(x) \to \pm \infty$, as $x\to \pm \infty$ or $x\to c$ or $x \to c^{\pm}$ then: 
If $$\frac{f'(x)}{g'(x)} \to L$$
$$\implies \frac{f(x)}{g(x)} \to L$$
The proof of this extension of LHoR is left as a proof to the next term. 
### Example
For instance, take the following: 
$$
\begin{align}
\lim_{ x \to \infty } \frac{\ln x}{x} = \frac{\infty}{\infty} \\
\lim_{ x \to \infty } \frac{\frac{1}{x}}{1}  & = 0 & \implies \lim_{ x \to \infty } \frac{\ln x}{x} = 0
\end{align}
$$
Consider, why couldn't we simply take the reciprocal, then: 
$$
\begin{align}
\lim_{ x \to \infty }  \frac{\frac{1}{x}}{\frac{1}{\ln x}} = \frac{0}{0} \\
\lim_{ x \to \infty } \frac{-\frac{1}{x^{2}}}{x} = 
\end{align}
$$

Consider now the following case: 
$$
\begin{align}
\lim_{ x \to \infty }  \frac{x^{3}}{e^{x}} = \frac{\infty}{\infty} \\
\lim_{ x \to \infty } \frac{3x^{2}}{e^{x}}= \frac{\infty}{\infty}
\end{align}
$$
Note that here, we have to effectively perform LHoR three times. We will introduce the following notation to express this: 
$$
\lim_{ x \to \infty } \frac{x^{3}}{e^{x}} \stackrel{*}{=} \lim_{ x \to \infty }  \frac{3x^{2}}{e^{x}} \stackrel{*}{=} \lim_{ x \to \infty }  \frac{6x}{e^{x}} \stackrel{*}{=} \lim_{ x \to \infty } \frac{6}{e^{x}} = 0
$$
Where the $\stackrel{*}{=}$  indicator means that we use LHoR. The above result actually gives us the following: 

> Generally: 
> $$\lim_{ x \to \infty } \frac{x^{m}}{e^{x}} = 0$$
> For $m >0$ and $m$ being an integer. 

## Other Indeterminate Forms 
Consider now the following expression: 
$$
\lim_{ x \to 0^{+} } x^{x} =0^{0}
$$
What do we do in this case? we can express this as the exponential of the logarithm, that is: 
$$
\lim_{ x \to 0^{+} } x^{x} = \lim_{ x \to 0^{+} } e^{x\ln(x)}
$$
In this case, then we simply analyze the exponent: 
$$
\begin{align}
\lim_{ x \to 0^{+} } x^{x} & = \lim_{ x \to 0^{+} } e^{x\ln x}  \\
 & =e^{\lim_{ x \to 0^{}+ } x\ln x} \tag{1.1}\\
 & \implies \lim_{ x \to 0^{+} } x\ln x \\
 & =\lim_{ x \to 0^{+} } \frac{\ln x}{\frac{1}{x}}\stackrel{*}{=}\lim_{ x \to 0^{+} } \frac{\frac{1}{x}}{-\frac{1}{x^{2}}} = \lim_{ x \to 0^{+} } x = 0 \\
 & \implies \lim_{ x \to 0^{+} } e^{x\ln x} = e^{0} = 1
\end{align}
$$
* Note, that for $(1.1)$, we note that we can simply pull the limit into the exponential function, then evaluate from there. 
Then: 
$$
\lim_{ x \to 0^{+} } x^{x} = 1
$$

Consider now the following expression: 
$$
\lim_{ x \to \infty } (x+2)^{2/\ln(x)} = \infty^{0}
$$
Then exponentiating it, we find that: 
$$
\begin{align}
\lim_{ x \to \infty } (x+2)^{2/\ln(x)}  & = \lim_{ x \to \infty }  e^{\ln(x+2)^{2/\ln(x)}} \\
 & = \lim_{ x \to \infty } e^{\frac{2}{\ln(x)}\ln(x+2)} \\
 & \implies \lim_{ x \to \infty } \frac{2\ln (x+2)}{\ln(x)} \\
 & \stackrel{*}{=}\lim_{ x \to \infty }  \frac{\frac{2}{x+2}}{\frac{1}{x}} = \lim_{ x \to \infty } \frac{2x}{x+2}=\frac{\infty}{\infty} \\
 & \stackrel{*}{=}\lim_{ x \to \infty }  \frac{2}{1} = 2 \\
 & \implies \lim_{ x \to \infty } e^{\frac{2}{\ln((x))}\ln(x+2)} = e^{2} \\
 & \implies \lim_{ x \to \infty } (x+2)^{2/\ln (x)} = e^{2}
\end{align}
$$

Consider now the following problem: 

$$
\lim_{ x \to \infty } \left[ \sin\left( \frac{\pi}{x} + \frac{\pi}{2} \right) \right]^{x} = 1^{\infty}
$$
Then, taking the exponent, then: 
$$
\begin{align}
\lim_{ x \to \infty } \left[ \sin\left( \frac{\pi}{x}+\frac{\pi}{2} \right) \right]^{x}  & = \lim_{ x \to \infty } e^{\ln\left[ \sin\left(  \frac{\pi}{x} + \pi/2 \right)^{x} \right]} \\
 & \implies \lim_{ x \to \infty } x\ln\left[ \sin\left( \frac{\pi}{x} + \frac{\pi}{2} \right) \right] \\
 & = \lim_{ x \to \infty } \frac{\ln\left[ \sin\left( \frac{\pi}{x} + \frac{\pi}{2} \right) \right]}{\frac{1}{x}} = \frac{0}{0} \\
 & \stackrel{*}{=}\lim_{ x \to \infty }  \frac{\frac{\cos\left( \frac{\pi}{x} + \frac{\pi}{2} \right) \frac{\pi}{x}}{\sin\left( \frac{\pi}{x}+\frac{\pi}{2} \right)}}{\frac{-1}{x^{2}}} \\
 & = \lim_{ x \to \infty }  \frac{\cos\left( \frac{\pi}{x}+\frac{\pi}{2} \right)* \frac{\pi}{x}} {\sin\left( \frac{\pi}{x} + \frac{\pi}{2} \right)* -\frac{1}{x^{2}}} = \frac{0\pi}{1} = 0 \\
 & \implies \lim_{ n \to \infty } \left[ \sin\left( \frac{\pi}{x} + \frac{\pi}{2} \right) \right]^{x } =e^{0} = 1
\end{align}
$$




---
# Pre-Lecture Notes
## Indeterminate Forms
Consider the case in which we have a function such as the following: 

$$
f(x)=\frac{\ln(x)}{x-1}
$$

Where we want to find the following: 

$$
\lim_{ x \to 1 } f(x) = \lim_{ x \to 1 }  \frac{\ln(x)}{x-1} \to \frac{0}{0}
$$

We have an issue: If we wanted to find the value of such a function, where taking the limit results in something that we term as an *indeterminate* form. We now define the following as indeterminate forms *which we can analyze*. 
* $\frac{0}{0}$
* $\frac{\infty}{\infty}$
In terms of the means we analyze this, we now introduce the concept of l\`Hospital's Rule: 
## l\`Hospital's Rule 
l\`Hospital's Rule (noted from here as LHoR) is defined as the following: 

> [!theorem] LHoR
> Let $f,g$ be differentiable and $g'(x) \neq 0$ on an open interval $I$ that contains $a$ (except possibly at $a$), Suppose that: 
>
> $$\lim_{ x \to a } f(x) = 0, \lim_{ x \to a } g(x) = 0\text{ or }\\ \lim_{ x \to a } f(x) = \infty, \lim_{ x \to a } g(x) = \infty$$
>
> Or in other words, we have the following expression that evaluates into an indeterminate form as the ones that we have had above. 
>
> $$\lim_{ x \to a } \frac{f(x)}{g(x)} \to\frac{0}{0} \lor \lim_{ x \to a } \frac{f(x)}{g(x)} \to \frac{\infty}{\infty}$$
>
> Then we define that:
>
> $$\lim_{ x \to a } \frac{f'(x)}{g'(x)} = L \implies \lim_{ x \to a } \frac{f(x)}{g(x)} = L$$
>
> If the limit on the right side exists. 

In other words, it states that given a ratio of functions which, when the limit is taken, that they fall into an indeterminate form of $\frac{\infty}{\infty}$ or $\frac{0}{0}$, the limit of that ratio of functions is equal to the limit of the ratio of the derivatives of those functions. 
### Proof 
We can prove this by reconsidering the Mean Value Theorem from earlier. For the purpose of completeness, we will prove the necessary theorems that we need to prove that this rule holds true. **Note that this only proves $\frac{0}{0}$** (as the proof of $\frac{\infty}{\infty}$ is outside the scope of this course). 

Recall that the mean value theorem is defined as the following (see [[13 — Mean Value Theorem, Linear Approximations and Differentials#Mean Value Theorem|ESC194 (13)]]): 
> Mean Value Theorem
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists some point $c\in(a,b)$ such that: 
>
> $$\boxed{f'(c)=\frac{f(b)-f(a)}{b-a}}\tag{MVT}$$

Let us define this in terms of $h(x)$, where we let $h(x)$ be the following expression: 

$$
h(x) = f(x) - f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(x)-g(a))
$$

Evaluating this as $h(b),h(a)$ and taking the derivative: 

$$
\begin{align}
h(b)  & = f(b)-f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(b)-g(a)) \\
 & =f(b) - f(a) - f(b) +f(a) \\
 & = 0 \\
h(a)  & = f(a)-f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(a)-g(a)) \\
 & =0 \\
h'(x)  & = f'(x) - \frac{f(b)-f(a)}{g(b)-g(a)}g'(x)
\end{align}
$$

Note that we find, $h(b)=0,h(a)=0$, we know that there exists some value $h'(c), c\in[a,b]$ where $h'(c) = 0$, thus: 

$$
\begin{align}
h'(c) & =0 = f'(c) - \frac{f(b)-f(a)}{g(b)-g(a)}g'(c) \\
-f'(c) & = - \frac{f(b)-f(a)}{g(b)-g(a)}g'(c) \\
\frac{f'(c)}{g'(c)} & = \frac{f(b)-f(a)}{g(b)-g(a)}
\end{align}
$$

This is the Cauchy Mean Value Theorem, that is, $\exists c\in[a,b]$ such that this is true. From this, we can now actually prove LHoR. 

Consider the case when we have an indeterminate form of $\frac{0}{0}$, that is given two functions, we have the following: 

$$
\begin{align}
F(x) &  = \begin{cases}
f(x) & : x\neq a \\
0 & : x=a
\end{cases} \\
G(x) & =\begin{cases}
g(x) & :x\neq a \\
0 & : x=a
\end{cases}
\end{align}
$$

Note that $F$ is continuous in $A$, where $A=\{ x\in I |x\neq a\}$. The same applies for $G(x)$. Consider now that $x\in I$ and $x>a$, then $F,G$ are continuous on $x\in [a,x]$. From this, we note that $F,A$ is differentiable on $(a,x)$, thus following Cauchy's MVT, we find the following: 

$$
\begin{align}
\exists c  & \in (a,x) \text{ s.t.} \\
\frac{F'(c)}{G'(c)} & = \frac{F(x)-F(a)}{G(x)-G(a)} = \frac{F(x)}{G(x)} \\[2em]
 & \text{note, } x\to a^{+} \implies c \to a^{+} \\
\lim_{ c \to a^{+} }  \frac{F'(c)}{G'(c)} & = \lim_{ x \to a^{+} }  \frac{F(x)}{G(x)}  \implies \lim_{ c \to a^{+} }  \frac{f'(c)}{g'(c)} = \lim_{ x \to a^{+} }  \frac{f(x)}{g(x)} =L
\end{align}
$$

Similarly, defining $x<a$ where $F,A$ are now continuous on $[x,a]$, and therefore differentiable in $(x,a)$, then we find that the right hand limits also hold: 

$$
\begin{align}
   & \exists c\in(x,a) \text{ s.t } \\
\frac{F'(c)}{G'(c)} & = \frac{F(a)-F(x)}{G(a)-G(x)} = \frac{F(x)}{G(x)} \\[1.5em]
x\to a^{-}  & \implies c \to a^{-} \\
\implies \lim_{ c \to a^{-} } \frac{F'(c)}{G'(c)} = \lim_{ x \to a^{-} } \frac{F(x)}{G(x)} &  \implies \lim_{ c \to a^{-} } \frac{f'(c)}{g'(c)} = \lim_{ x \to a^{-} } \frac{f(x)}{g(x)}
\end{align}
$$

Noting that the right and left hand limits are equal, we thus find that: 

$$
\lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)} = \text{L}
$$

#### Extension
Consider now we can extend this if $x \to \infty$, we can express this as $x \to \frac{1}{t}$, where $t\to 0$, where this is finite value, thus: 

$$
\lim_{ x \to \infty } \frac{f(x)}{g(x)} = \lim_{ x \to \infty } \frac{f'(x)}{g(x)} \iff\lim_{ t \to 0 }  \frac{f\left( \frac{1}{t} \right)}{g\left( \frac{1}{t} \right)} = \lim_{ t \to 0 } \frac{f'\left( \frac{1}{t} \right)}{g'\left( \frac{1}{t} \right)} = L
$$
