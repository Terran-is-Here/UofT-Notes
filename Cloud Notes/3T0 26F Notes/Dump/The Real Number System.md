---
updated_at: 2026-09-09T13:11:57.741-04:00
edited_seconds: 1570
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

> [!axiom] Axiom F.1
> **Communicative Law: ** For every ordered pair $a$, $b \in \mathbb{R}$
> $$a+b=b+a \text{ and } ab=ba$$

> [!axiom] Axiom F.2
> **Associative Law** : For every ordered triple $a,b,c \in \mathbb{R}$: 
> $$(a+b)+c = (a+c)+b \text{ and } (ab)c = (ac)b$$

> [!axiom] Axiom F.3
> **Distributive Law**: For each triple $x,y,z\in \mathbb{R}$: 
> $$a(b+c) = ab + ac \text{ and } (a+b)c = ac + bc $$

> [!axiom] Axiom F.4
> **Identities**: There exists two distinct real numbers with the following identities: 
> $$0+x = x + 0 = x$$
> $$1*x = x * 1 = x$$

> [!axiom] Axiom F.5
> **Inverses**: For each $x\in \mathbb{R}$; there exists a unique additive inverse denoted by $-x$, such as to allow the following: $$x + (-x) = (-x) + x = 0$$
> For each $x\in \mathbb{R},x \neq 0$; there exists a **unique** multiplicative inverse denoted by $\frac{1}{x}$ or $x^-1$; for which $$x * x^{-1} = x^{-1}*x = 1$$

> [!note] Def F.1
> From Axiom 5; we can easily define subtraction ($a-b = a+(-b)$) and division ($a\div b = a * (\frac{1}{b})$)

> [!note] Definition F.2
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
> [!axiom] Axiom O.1
> **Trichotomy Law** - $a\neq b$: 
> $$a<b \text{ or } b < a$$ 
> only **one** of these can be true at any given time. 

> [!axiom] Axiom O.2
> **Transitivity**
> $$a<b \land b<c \implies a <c$$

> [!axiom] Axiom O.3 & O.4
> Preservation of the Addition Operation
> $$a < b \implies a+c < b + c$$
> Preservation of the Multiplication Operation
> $$0<c, a < b, ac < bc$$
> (Can be derived from the other axioms but it's fundamental enough as is; see Theorem 1.5)

From here we can generally define our other inequality symbols (Definitions O.1 to O.3 respectively).
* $a > b$ if $b < a$
* $a \leq b$ if $a<b \lor b=a$
* $a \geq b$ if $b \leq a$
## Inequalities
The following are useful inequality theorems to know. 

Template: 
```
> [!theorem] ...
> $$$$
> > [!axiom] ...
> > $$$$
```

> [!theorem] Theorem 1.1
> $$a \leq b \iff b-a \geq 0$$ 
> Hint: Directionality. 
> > [!axiom]- Proof
> > Using definition O.3, reverse the direction: 
> > $$b \geq a $$
> > Use Axiom O.3, F.5 to add $(-a)$ to both sides: 
> > $$b+(-a) \geq a + (-a)$$
> > $$b-a \geq 0$$ Q.E.D

> [!theorem] Theorem 1.2 
> $$a=b \iff a\leq b \land b \leq a$$
> Hint: It can't be both. 
> > [!axiom]- Proof
> > For this case, we will use Definition O.2 for this (though Theorem O.1 also applies)
> > $$a\leq b \implies a = b \lor a < b $$
> > $$b\leq a \implies b = a \lor b < a $$
> > Both states of $b<a$ and $a<b$ cannot be true at the same time. Therefore $a=b$. 

> [!theorem] Theorem 1.3
> $$a \leq b \land c \leq d \implies a+c \leq b+d$$
> Hint: How can you combine the bounds of two inequalities? 
> > [!axiom]- Proof
> > For this case; we shall separately apply Axiom O.3 separately across both: 
> > $$a +c\leq b+ c$$
> > $$c +b \leq d + b$$
> > Note that we can now use Axiom O.2 on this: 
> > $$a+c \leq b+c \land c+b \leq d+b \implies a+c \leq d+b$$
 
> [!theorem] Theorem 1.4
> $$a \leq b \implies -b \leq a$$
> Hint: Adding things...
> > [!axiom]- Proof
> > Use Axiom O.3 and F.5. 
> > $$a + (-b) + (-a)\leq b + (-b) + (-a)$$
> > $$-b \leq -a $$
> > This theorem is useful for proving other theorems. 
> 

> [!theorem] Theorem 1.5
> $$a \leq b \land c > 0 \implies ca \leq cb$$
> Hint: Signs. 
> > [!axiom]- Proof
> > Use Theorem 1.1: 
> > > Using definition O.3, reverse the direction: 
> > > $$b \geq a $$
> > > Use Axiom O.3, F.5 to add $(-a)$ to both sides: 
> > > $$b+(-a) \geq a + (-a)$$
> > > $$b-a \geq 0$$ 
> > 
> > Since $(b-a)$ must be positive; and $c$ is positive; signs are preserved; ergo..????
> > $$cb -ca \geq 0$$
> > Using Axiom O.3 again we get
> > $$cb \geq ca$$
> > Reversing the direction; then: 
> > $$ca \geq cb$$
> 

> [!theorem] Theorem 1.6 
> $$a \leq b \land c < 0 \implies ca \geq cb$$
> Hint: 1.5. 
> > [!axiom]- Proof
> > Use Axiom O.3 on our c term: 
> > $$c + (-c) < (-c)$$
> > $$0< -c$$
> > Reverse the direction of the inequality:
> > $$-c > 0$$
> > Use Theorem 1.5 (with a different sign): 
> > > Using definition O.3, reverse the direction: 
> > > $$b \geq a $$
> > > Use Axiom O.3, F.5 to add $(-a)$ to both sides: 
> > > $$b+(-a) \geq a + (-a)$$
> > > $$b-a \geq 0$$ 
> > 
> > Distribute $(-c)$ across our terms: 
> > $$-cb + ca \geq 0$$
> > Using Axiom O.3 again we get: 
> > $$ca \geq ^{3}$$

> [!theorem] Theorem 1.7
> $$0 < a \leq b \implies 0 < \frac{1}{b} \leq \frac{1}{a}$$
> > [!axiom] ...
> > $$$$