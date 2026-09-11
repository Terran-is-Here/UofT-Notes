---
updated_at: 2026-09-11T14:53:45.228-04:00
edited_seconds: 4210
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 1
Date: 2026-09-10
Week: 1
---
To Hub: [[ESC194 Hub]]
Previous: [[01 — Introduction — Tangent and Velocity]]
Next: 
> [!warning] Note
> This note was primarily based on the Supplemental (Sections 1; and 2.1-2.7.)
> A good amount of it *was* transcribed from the actual like; document; although it's now here in obsidian so it should be easier to work with.
> **This note is generally meant to be a quick refresher on the axioms and general definitions of $\mathbb{R}$ for this course.**
--- 

# The Real Number System (Pre-Lecture Notes)
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
### Theorem 1.1 - Exclusion of 0
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
> For any $a\in \mathbb{R}$; there does not exist any means to multiply $0$ to obtain 1 ; thus requiring it's exclusion from the definition of Axiom 5 and $\mathbb{R}$. 

### Theorem 1.2 - Negative Numbers and Multiplication
Note that the system above does not explicitly define the concept of negative numbers and their role in multiplication; or more accurately; the effects of the additive inverse with the multiplication operation. 

As an exercise to future me; solve what a $PN$ and $NN$ result (Positive * Negative & Negative * Negative )
> [!note]- Lemma 1- Positive & Negative
> Take Theorem 1.1, let $a \in \mathbb{R}, a \geq 0$
> $$a 0 = 0$$
> Use Axiom F.4 and F.3 to break up $0$ into some value $(b - b)$; where $b \in \mathbb{R}$: 
> $$a(b+(-b)) = 0$$
> $$ab+ a * (-b) = 0$$
> We know from Axiom F.5 that for the above statement to be true ($n-k=0$); $k$ must be the additive inverse of $n$; or in other words $a*b = (-ab)$. 

> [!theorem]- Negative Multiplication / Theorem 1.2
> Take Theorem 1.1 again; let $a\in \mathbb{R}, a \geq 0$: 
> $$(-a)0 = 0$$
> Use Axiom F.4 and F.3 to break up $0$ to some value $(b + (-b))$; where $b\in \mathbb{R}, b\geq 0$: 
> $$(-a)(b+(-b)) = 0$$
> $$(-ab) + (-a) * (-b) = 0$$
> We know once again from Axiom F.5 that for the above statement to be true ($n-k = 0$);  $k$ must be the additive inverse of n; or in other words $-a * -b = ab$. 

### Square Root Definition
> [!axiom] Square Root
> Let $x\geq 0$. $\sqrt{ x }$ is a non-negative number $u$ such that $u^2=x$ (thus since $x\geq {0}$, $\sqrt{ x }\geq 0$). 

## Order Axioms
There exists 3 main Order Axioms within $\mathbb{R}$. For the sake of brevity, assume $a,b,c \in \mathbb{R}$. 
> [!axiom] Axiom O.1
> **Trichotomy Law** - $a\neq b$: 
> $$a<b \text{ or } b < a$$ 
> only **one** of these can be true at any given time. (That being that it is *equal to*, *less than*, or *greater than*)

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
### Intervals
From here; we can also define the concept of an interval in $\mathbb{R}$: 
* $[a,b] = \{x:a\leq x\leq b\}$ (Closed / *Inclusive* interval)
* $(a,b) = \{x:a < x < b\}$ (Open / *Exclusive* interval)
* $[a, +\infty] = \{x: a\leq x\}$ (undefined bound intervals)
Different combinations of these exist and should be trivial to derive. 
## Inequalities
The following are useful inequality theorems to know. 

Template: 
```
> [!theorem] Corollary...
> $$$$
> > [!axiom] ...
> > $$$$
```

> [!note] Corollary 1.1
> $$a \leq b \iff b-a \geq 0$$ 
> Hint: Directionality. 
> > [!axiom]- Proof
> > Using definition O.3, reverse the direction: 
> > $$b \geq a $$
> > Use Axiom O.3, F.5 to add $(-a)$ to both sides: 
> > $$b+(-a) \geq a + (-a)$$
> > $$b-a \geq 0$$ Q.E.D

> [!theorem] Corollary 1.2 
> $$a=b \iff a\leq b \land b \leq a$$
> Hint: It can't be both. 
> > [!axiom]- Proof
> > For this case, we will use Definition O.2 for this (though Theorem O.1 also applies)
> > $$a\leq b \implies a = b \lor a < b $$
> > $$b\leq a \implies b = a \lor b < a $$
> > Both states of $b<a$ and $a<b$ cannot be true at the same time. Therefore $a=b$. 

> [!theorem] Corollary 1.3
> $$a \leq b \land c \leq d \implies a+c \leq b+d$$
> Hint: How can you combine the bounds of two inequalities? 
> > [!axiom]- Proof
> > For this case; we shall separately apply Axiom O.3 separately across both: 
> > $$a +c\leq b+ c$$
> > $$c +b \leq d + b$$
> > Note that we can now use Axiom O.2 on this: 
> > $$a+c \leq b+c \land c+b \leq d+b \implies a+c \leq d+b$$
 
> [!theorem] Corollary 1.4
> $$a \leq b \implies -b \leq -a$$
> Hint: Adding things...
> > [!axiom]- Proof
> > Use Axiom O.3 and F.5. 
> > $$a + (-b) + (-a)\leq b + (-b) + (-a)$$
> > $$-b \leq -a $$
> > This theorem is useful for proving other theorems. 
> 

> [!theorem] Corollary 1.5
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

> [!theorem] Corollary 1.6 
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
> > $$ca \geq cb$$

> [!theorem] Corollary 1.7
> $$0 < a \leq b \implies 0 < \frac{1}{b} \leq \frac{1}{a}$$
> Hint: Communicative Law 
> > [!axiom]- Proof
> > We can safely ascertain that $a$ and $b$ are above 0; as $0<a$ and $a\leq b \implies 0<b$. Ergo we can safely divide across all terms. 
> > $$0 < a \leq b$$
> > Using F.5 & Theorem 1.5 (generally O.4) 
> > $$0 < a(a^{-1})(b^{-1}) \leq b(a^{-1})(b^{-1})$$ 
> > $$0 < \frac{1}{b} \leq \frac{1}{a}$$

> [!theorem] Corollary 1.8
> $$\forall x \in \mathbb{R},x^2 \geq 0$$
> Hint: Negative Number Multiplication
> > [!axiom]- Proof
> > We can prove this by breaking this up into three parts. We can take the trivial case using Theorem 1.1: 
> > $$x = 0; x^2 \geq 0 \to 0*0 \geq 0 \to 0\geq 0$$
> > For positive numbers; this is also trivial: 
> > $$x > 0; x^2 \geq 0 $$
> > For negative numbers; we can use Theorem 1.2. to show that this is also true: 
> > $$x < 0; -x > 0; (-x)^2 \geq 0 \to (-x)(-x) \geq 0 \to x^2 \geq 0$$. 


> [!theorem] Corollary 1.9
> $$a,b \in \mathbb{R}, 0 \leq ab$$
> $$a<b \iff a^2 < b^2$$
> $$a<b \iff \sqrt{ a } < \sqrt{ b }$$
> Hint: Break up and cancel out terms. 
> > [!axiom]- Proof (1) 
> > Taking the first one; we can use Axiom O.3 to rearrange it to a difference of squares: 
> > $$0 < b^2 - a^2$$
> > $$0 < (b-a)(b+a)$$
> > Using Corollary 1.6; we can cancel out our $(b+a)$ term. 
> > $$0 < (b-a)$$
> > Using Axiom F.5 and O.3: 
> > $$a < b$$
> 
> > [!axiom]- Proof (2)
> > Taking the second one; we can use Axiom O.3 to rearrange it 
> > $$0 < \sqrt{ b } - \sqrt{ a }$$
> > Note that $(\sqrt{ b } - \sqrt{ a }) = \frac{b-a}{(\sqrt{ b } + \sqrt{ a })}$; thus: 
> > $$0 <  \frac{b-a}{(\sqrt{ b } + \sqrt{ a })}$$
> > Using Corollary 1.6; we can cancel out our denominator term. 
> > $$0 < (b-a)$$
> > Using Axiom F.5 and O.3: 
> > $$a < b$$

> [!theorem] Corollary 1.10
> $$u,v \in \mathbb{R}, u\neq v, u<v$$
> $$0 < (x-u)(x-v) \iff x < u \lor x >v$$
> $$ 0 >(x-u)(x-v) \iff u<x<v$$
> Hint: How many cases are there? Divide and conquer. 
> > [!axiom]- Statement 1 Proof
> > Break up this section ($0 < (x-u)(x-v) \iff x < u \lor x >v$) into two lines; one for each inequality case: 
> > > If $x < u$: 
> > > $$0 < (x-u)(x-v) \iff x < u$$
> > > We can rearrange our base condition inequality into (via Axiom O.3): 
> > > $$x-u < 0 \implies (x-u) \text{ is -'ve}$$
> > > 
> > > 
> > > We can combine $x<u$ with $u<v$ using Axiom O.2: 
> > > $$x<v$$
> > > We can rearrange our base condition inequality into (via Axiom O.3): 
> > > $$x-v < 0 \implies (x-v)\text{ is -'ve}$$
> > 
> > > If $x > v$; we can follow the same logic as we did for the previous statement: 
> > > $$0 < (x-u)(x-v) \iff x >v$$
> > > $$x-v>0 \implies (x-v) \text{ is +'ve}$$
> > > $$x>v \to v < x \to\text{via O.2 }\to u < x \to 0<x-u \implies (x-u) \text{ is +'ve}$$
> 
> > [!axiom]- Statement 2 Proof 
> >  $$0 >(x-u)(x-v) \iff u<x<v$$
> >  The key here is to break up that triple inequality into two inequalities (using O.2): 
> >  $$u<x$$
> >  $$x < v$$
> >  We can rearrange these into our binomials: 
> >  $$0<x-u$$
> >  $$x-v < 0$$
> >  The first line implies that $(x-u)$ will be positive; whilst the second line implies that $(x-v)$ will be negative; hence this statement holds. 

> [!theorem] Corollary 1.11 (The Arithmetic-Geometric Means Inequality)
> $$a,b\in \mathbb{R} \land a,b \geq 0$$
> $$\sqrt{ ab } \leq \frac{a+b}{2}$$
> $$\sqrt{ ab } = \frac{a+b}{2}\iff a=b$$
> > [!axiom]- Proof
> > For the proof of this; we shall derive it. Since $a,b\geq 0$; then the following is also true (derived from Corollary 1.8): 
> > $$(a-b)^2\geq 0$$ 
> > Expand and collect like terms as per Theorem 1.2 : 
> > $$a^2 - 2ab + b^2 \geq 0$$
> > Use Axiom O.3 to add a term of $+4ab$ to both sides: 
> > $$a^2 + 2ab + b^2 \geq 4ab$$
> > Factor the left side: 
> > $$(a+b)^2 \geq 4ab$$
> > Take the square root of both sides (as per following our definition of a square root )
> > $$(a+b) \geq 2\sqrt{ ab }$$
> > Divide by 2 then reverse the inequality's direction: 
> > $$\frac{a+b}{2} \geq \sqrt{ ab }$$
> > $$\sqrt{ ab } \leq \frac{a+b}{2} $$
> > For the case when $a=b$; this simplifies down into a trivial case and is thus left to the reader. 

> [!theorem] Corollary 1.12 (The Cauchy-Schwarz Inequality)
> Let $a,b,c,u,v,w \in \mathbb{R}$ such that: 
> $$au + bv + cw \leq \sqrt{ a^2 + b^2 + c^2 } * \sqrt{ u^2 +v^2+w^2}$$
> This becomes an equality if and only if $a:b:c = u:v:w$. 
> > [!axiom]- Proof
> > I *did* get spoiled by this a bit so :shrugs: 
> > Square both sides: 
> > $$(au+bv+cw)^2 \leq(a^2+b^2+c^2)(u^2+v^2+w^2)$$
> > Move $(au+bv+cw)$ to the right via O.3: 
> > $$0 \leq (a^2+b^2+c^2)(u^2+v^2+w^2)-(au+bv+cw)^2 $$
> > Expand and collect like terms. Painfully.
> > $$a^2u^2+a^2v^2 + a^2w^2 + b^2u^2 + b^2v^2 + b^2w^2 + c^2u^2 + c^2v^2 + c^2 w^2 -(a^2u^2 + 2aubv + 2aucw +b^2v^2 + 2bvcw + c^2w^2  )$$
> > $$a^2v^2 + a^2w^2 + b^2u^2 + b^2w^2 + c^2u^2 + c^2v^2 + -(2aubv + 2aucw + 2bvcw)$$
> > $$a^2v^2 + a^2w^2 + b^2u^2 + b^2w^2 + c^2u^2 + c^2v^2 -2aubv - 2aucw - 2bvcw$$
> > Rearrange:
> > $$(a^2v^2 -2aubv+ b^2u^2)+ (a^2w^2 - 2aucw+  c^2u^2)+ (b^2w^2  - 2bvcw+ c^2v^2)$$
> > Factor all 3 trinomials present within: 
> > $$0\leq(av-bu)^2 + (aw-cu)^2 + (bw -cv)^2$$
> > Thus the equality can only be true if and only if: 
> > $$av = bu$$
> > $$aw=cu$$
> > $$bw=cv$$

### Inequalities with X and Y 
When considering inequalities with terms of both $x$ and $y$, we have to consider that we are now trying to find an inequality of a graph / slope (or in other words; the bounds are defined by functions in this instance and not pure static numbers )

## Absolute Value 
The concept of the Absolute Value is not inherently part of our Axioms; rather it is defined under the following definition: 

> [!theorem] Definition of Absolute Value 
>  $$x\in \mathbb{R}\text{ then }|x| = \begin{cases}
> x : x\geq 0\\
> -x : x < 0 \\
> \end{cases}$$

It thus also follows these following base properties (proofs included if required)

> [!theorem] Property A.1
> $$\forall x\in \mathbb{R}, |x| \geq 0$$
> In cases where $x \geq 0$; it simply returns a positive number. 
> In cases where $x < 0$; it returns the additive inverse of $x$ (with it being a negative number; then this is returns a positive number)

> [!theorem] Property A.2
> $$\forall x\in \mathbb{R}, -|x| \leq x \leq|x|$$
> Taking Property A.1; we know that $\forall x \in \mathbb{R}, |x| \geq {0}$ From Corollary 1.5; we can multiply this by -1 to get the following inequality: 
> $$-|x| \leq 0$$
> We can also reuse Property A.1; and we get the conclusion that $\forall x\in \mathbb{R}$ this holds true. 
> **This is a very useful property re-applicable for other identities**. 

> [!theorem] Property A.3
> $$c>0, |x| \leq c \iff -c \leq x\leq c$$
> We can break this problem up into two segments: solving Left to Right, and Right to Left: 
> > Assume that $|x| \leq c$ is true; then: 
> > $$x \leq c$$
> > $$-x \leq c \to -c \leq x$$
> > $$-c \leq x \leq c$$
> 
> We can also define this in the other direction by simply multiplying our entire inequalities by a term of $-1$. 
> **This is also another useful property re-applicable for other identities.**

### Triangle Inequality Theorem
> [!theorem]  The Triangle Inequality Theorem (Theorem A.1 / Property A.4)
> $$|a+b| \leq |a| + |b|$$
> We can use Property A.2 and A.3 for solving this. Note how we can define $a$ and $b$ as: 
> $$-|a| \leq a \leq |a|$$
> $$-|b| \leq b \leq |b|$$
> We can add / combine these inequalities together; giving us: 
> $$-(|a| + |b|) \leq a+b \leq |a| + |b|$$
> From A.3 we can simplify this into: 
> $$|a + b| \leq |a| + |b|$$
> (Using the first identity; that is the $|x| \leq c$)


> [!theorem] Property A.4
> $$\forall a,b\in \mathbb{R}, |ab| = |a| |b|$$
> We can solve this by breaking whatever the sign of the $ab$ expression inside is. Take the following cases: 
> > Case 1: 
> > $$a\geq 0, b<0$$
> > Then:
> > $$ab< 0 \implies |ab| = -ab$$
> > which means that:
> > $$-ab = (a)(-b) = |a||b|$$
> 
> > Case 2:
> > $$ a < 0, b < 0$$
> > Then: 
> > $ab > 0 \implies |ab|=ab \implies ab=|a||b|=|ab|$

## Other Axioms 
> [!axiom] Axiom Add.1
> $$p>0, \exists n\in \mathbb{Z} \text{ s.t. }pn > r, \text{ where } r\in \mathbb{R} $$
## Completeness of the Reals Axiom (CORA)
The Completeness of the Reals Axiom is a necessary Axiom to ensure the existence of a *continuum* of numbers. 
It is generally defined as: 
> "Every non-empty set of real numbers which has an upper bound, has a least upper bound."

> [!theorem] Definition of an Upper Bound
> A set of $\mathbb{R}$ defined by $s$ is *bounded above* if $\exists$ some number $M$ such that: 
> $x\leq M,\forall x \in S$; where $M$ is an "upper bound" for $s$. 
> 
> Or, briefly: 
>  $$s\subset \mathbb{R} \text{ has an upper bound if } \exists M \text{ s.t. } \forall x \in S, x \leq M$$

> [!axiom] Definition of a least upper bound: 
> A Least Upper Bound (or a lub, notated as $lub(s)$) is the smallest of all possible upper bounds. A Least Upper Bound (often notated m) exists if: 
> $$\exists m \text{ s.t. } \forall M, m\leq M$$
This has implications for what kind of numbers we can *include* in the $\mathbb{R}$ system; retake the definitions that we have for some number systems. 

### Rational Numbers
Rational numbers are defined as: 
$$
p,q \in \mathbb{Z}, q\neq0,\frac{p}{q}
$$
Or; a rational number by definition can be expressed as a ratio of two integers. 

### Algebraic Numbers
Algebraic Numbers are defined as any numbers that are a solution to a polynomial equation: 
$$
a_{n}x^n + a_{n-1}x^{n-1}\dots a_{1}x + a_{0} = 0
$$
Where $a_{n\dots}\in \mathbb{R}$. This include the solution of $x^2 = 2$ for instance. 

### Irrational Numbers
Something interesting occurs when we include the Algebraic numbers into the Real Number System; as well as using our CORA: Consider the following case: 
$$
x^2 = 2
$$
The solution of this equation is an *algebraic number*; but we can easily prove and show that no rational $x$ exists which can satisfy this condition.
>[!proof]-
$$x^2 = 2 $$
> Let's assume that $x$ is some rational number meaning that for $a,b\in \mathbb{Z}$, and $a,b$ in their lowest forms: 
> $$\frac{a}{b} = x$$
> Where $b\neq0$, then we can sub this in: 
> $$\left(\frac{a}{b}\right)^2 = 2$$
> $$\left(\frac{a^2}{b^2}\right) = 2$$
> $$ a^2 = 2b^2$$
> Since $a^2$ equals to some value multiplied by two; this implies that $a$ itself is some even numbers. Even numbers can be defined as being some value $2k$ where $k\in \mathbb{Z}$; then: 
> $$4k^2 = 2b^2$$
> $$2k^2 = b^2$$
> This then also implies that $b$ itself is some even number. If both $a$ and $b$ are even numbers; they must share a factor at minimum of $2$, meaning that we have reached a contradiction. $x^2=2$ therefore has no rational solutions. 

Since no rational $x$ can satisfy this condition; we can construct the following set: 
$$s = \{ x:x^2\geq 2, x\in\text{Rational Numbers} \}$$
Now, retake Axiom 9 / CORA; then we notice that since $\sqrt{ 2 }\not\in \text{ Rational Numbers}$; then the set above does not have a Least Upper Bound. The set of Rational Numbers do not conform to our Axiom 9; thus requiring us to include the Irrational Numbers within $\mathbb{R}$. 