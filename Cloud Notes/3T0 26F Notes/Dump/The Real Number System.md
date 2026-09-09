---
updated_at: 2026-09-09T11:18:41.963-04:00
edited_seconds: 800
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 1
Date: 2026-09-10
Week: 1
---
To Hub: [[ESC194 Hub]]
Previous: N/A
Next: 
> [!warning] Note
> This note was primarily based on the Supplemental (Sections 1; and 2.1-2.7.)
> A good amount of it *was* transcribed from the actual like; document; although it's now here in obsidian so it should be easier to work with.
> **This note is generally meant to be a quick refresher on the axioms and general definitions of $\mathbb{R}$ for this course.**
--- 

# The Real Number System
The Real Number System (otherwise known as $\mathbb{R}$) is the primary* (excluding $\mathbb{C}$) number system that we will be using for the purposes of ESC194H1. Before performing Calculus however; we should have a rigorous understanding for the underlying principles of $\mathbb{R}$. 
## Field Axioms 
> This section and the following one are meant to be skimmed; but they also should give you an understanding for why some identities don't really exist within $\mathbb{R}$; such as $\infty$ and $\frac{1}{0}$. 

$\mathbb{R}$ will have two main arithmetic operations; that being *addition* and *multiplication*. These operations solely operate on an ordered set of two numbers $a$ and $b$ (or $(a,b)$) to produce another number. 

> [!axiom] Axiom 1
> **Communicative Law: ** For every ordered pair $a$, $b \in \mathbb{R}$
> $$a+b=b+a \text{ and } ab=ba$$

> [!axiom] Axiom 2
> **Associative Law** : For every ordered triple $a,b,c \in \mathbb{R}$: 
> $$(a+b)+c = (a+c)+b \text{ and } (ab)c = (ac)b$$

> [!axiom] Axiom 3
> **Distributive Law**: For each triple $x,y,z\in \mathbb{R}$: 
> $$a(b+c) = ab + ac \text{ and } (a+b)c = ac + bc $$

> [!axiom] Axiom 4
> **Identities**: There exists two distinct real numbers with the following identities: 
> $$0+x = x + 0 = x$$
> $$1*x = x * 1 = x$$

> [!axiom] Axiom 5
> **Inverses**: For each $x\in \mathbb{R}$; there exists a unique additive inverse denoted by $-x$, such as to allow the following: $$x + (-x) = (-x) + x = 0$$
> For each $x\in \mathbb{R},x \neq 0$; there exists a **unique** multiplicative inverse denoted by $\frac{1}{x}$ or $x^-1$; for which $$x * x^{-1} = x^{-1}*x = 1$$

> [!note] Note
> From Axiom 5; we can easily define subtraction ($a-b = a+(-b)$) and division ($a\div b = a * (\frac{1}{b})$)

> [!note] Note 2
> Axiom 5 also let's us define exponentials trivially. 
### Axiom 5.1 - Exclusion of 0
Note that Axiom 5 explicitly denies the inclusion of a multiplicative inverse (or; division) by zero. If we attempt to do so; we end up with some difficulties. 

For the purposes of this to leave it as an exercise; try to prove how $a*0 = 0$. 

> [!axiom]- Proof 
> Take Axiom 5; essentially stating that for every number in $\mathbb{R}$; there must exist a means for it to equal $1$; or in other words; $ab=1$, $a,b\in \mathbb{R}$ has a solution. 
> To show that we can't include $0$ in this Axiom; let's take Axiom 3 and 4. Let $a,b,c,x \in\mathbb{R}$
> $$a(b+c) = ab + ac $$
> $$0+x = x + 0 = x $$
> If we let $x=0$ and sub it in as $b+c$ then: 
> $$a(0+0) = a*0+ a*0  = a*0$$
> Apply Axiom 5 by adding the inverse of $a*0$ into both sides: $$a*0+ a*0 + (-(a*0))  = a*0 + (-(a*0))$$
> By definition from Axiom 5: 
> $$a*0= 0$$
> For any $a\in \mathbb{R}$; there does not exist any means to multiply $0$ to obtain 1; thus requiring it's exclusion from the definition of Axiom 5 and $\mathbb{R}$. 
## Order Axioms
There exists 3 main Order Axioms within $\mathbb{R}$. For the sake of brevity, assume $a,b,c \in \mathbb{R}$. 
> [!axiom] Axiom 6
> **Trichotomy Law** - $a\neq b$: 
> $$a<b \text{ or } b < a$$ 
> only **one** of these can be true at any given time. 

> [!axiom] Axiom 7
> **Transitivity**
> $$a<b \land b<c \implies a <c$$

> [!axiom] Axiom 8 & 9 
> 
> $$a < b \implies a+c < b + c$$
> $$0<c, a < b, ac < bc$$

From here we can generally define our other inequality symbols: 
* $a > b$ if $b < a$
* $a \geq b$ if $b < a \lor b=a$
* $a \leq b$ if $b \geq a$
## Inequalities
The following are useful inequality properties to know. Proofs are attached. 

1. $a \leq b \iff b-a \geq 0$
2. $a=b \iff a\leq b \land b \leq a$
3. 