---
updated_at: 2026-09-28T21:24:16.227-04:00
edited_seconds: 480
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 11
Lecture Date: 2026-10-02
Week: 4
Created: September 27th 2026, 12:09:30 pm
---
Hub: [[ESC194 Hub]]
Previous: [[10 — Differentiation Formulas and Applied Derivatives]]
Next: N/A 
> [!quote] Recommended Reading 
> Stewart Textbook: 2.4-2.6
--- 
# Lecture Notes
# Pre-Lecture Notes
## Trigonometric Derivatives
Trigonometric Derivatives can be generally obtained from the Differentiation Formulas that we derived in our previous note, as well as some angle sum identities. For this segment, we will take the derivative of $\sin(x)$: 
$$
\begin{align}
f(x) &= \sin(x) \\
f'(x) &= \lim_{ h \to 0 } \frac{\sin(x+h)-\sin(x)}{h} \\
&= \lim_{ h \to 0 } \frac{\sin (x)\cos(h) + \sin(h)\cos(x) - \sin(x)}{h} \\
&=\lim_{ h \to 0 } \frac{\sin (x)\cos(h) - \sin(x)+ \sin(h)\cos(x) }{h}  \\
&= \lim_{ h \to 0 } \sin(x) \frac{\cos(h)-1}{h} + \lim_{ h \to 0 } \frac{\sin(h)\cos(x)}{h} \\
&= \sin(x) \lim_{ h \to 0 } \frac{\cos(h)-1}{h} + \cos(x)\lim_{ h \to 0 } \frac{\sin(h)}{h} &\lim_{ h \to 0 } \frac{\cos(h)-1}{h} =0 &&\lim_{ h \to 0 } \frac{\sin(h)}{h}=1\\ \\
&=\sin(x)(0) + \cos(x)(1)  \\
&=\cos(x)
\end{align}
$$
Note that the two limits that we have shown on the right will be proved in their respective subsection: 

### Special Trigonometric Limits 

> The following holds true: 
> $$\lim_{ x \to 0 } \frac{\sin(x)}{x} = 1$$

> [!theorem]- *Proof*
> Take the following diagram: 
> ![[11 — Trigonometric, Chain and Implicit Differentiation-1790605672585.webp]]
> Where $\theta$ is within $0<\theta< \frac{\pi}{2}$, And where $|BC| = |OB|\sin\theta = \sin\theta$. Note that in this case, $\text{arc BA} = \theta r = \theta$
> From here, we can tell that:$$\begin{align}|BC| < |AB| &< \text{arc AB} \\\sin\theta &< \theta \\\frac{\sin\theta}{\theta} &< 1 \end{align}$$
> Note that we now extend the tangent lines from $A$ and $B$, when note that $\text{arc AB} < |DA| = |OA|\tan\theta = \tan\theta$
> Then we have the set of following relations: 
> $$\begin{align}\frac{\sin\theta}{\theta} < 1\\\theta < \tan\theta \implies \theta < \frac{\sin\theta}{\cos\theta}\end{align}$$
> From here: $$\begin{align}\theta &< \frac{\sin\theta}{\cos\theta}  \\\implies \cos\theta &< \frac{\sin\theta}{\theta}  \\\implies \cos\theta &< \frac{\sin\theta}{\theta} <1 \\\lim_{ \theta \to 0 } \cos\theta &< \lim_{ \theta \to 0 }  \frac{\sin\theta}{\theta} < \lim_{ \theta \to 0 } 1 & \text{Following from Squeeze Theorem, then} \\\implies \lim_{ \theta \to 0 } \frac{\sin\theta}{\theta} &= 1\end{align}$$


> The following also holds true: 
$$
> \lim_{ x \to 0 } \co
$$
