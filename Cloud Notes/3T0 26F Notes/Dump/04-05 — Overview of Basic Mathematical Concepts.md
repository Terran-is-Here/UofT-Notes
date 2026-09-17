---
updated_at: 2026-09-17T14:34:19.890-04:00
edited_seconds: 1160
course:
tags:
  - ESC194H1
"Lecture #": 4
Lecture Date: 2026-09-14
Week: 2
created:
Created: September 14th 2026, 11:05:13 am
---
Previous: [[02 — The Real Number System]], 
Next: [[05 — The Limit of a Function]]

> [!caution] Note
> This note was primarily written based on in-lecture content; since we don't really have any content / context from any materials pertaining to this; and I didn't really know what readings would be preferred for it :shrugs: 

> [!quote] Relevant Textbook Entries
> I think it should be the Stewart Textbook (1.1 - 1.3 and 1.5)..? Though I could be wrong.
> This is *also* predominantly Section 2 of the [[ESC194F Supplement 1 Sept 2026.pdf|Supplement]]; and Addendum D in the Textbook. 


--- 

# Pre-Lecture Notes
No pre-lecture notes are directly available. 

# Lecture Notes
## Absolute Value 
> [!theorem] Definition of Absolute Value
> Absolute Value is defined as the following: 
> $$|a| = \begin{cases}-a: a \leq 0 \\a>0\end{cases}$$
> This can also be derived as taking the *positive definition* of a square root with a term of $x^2$: 
> $$\sqrt{ x } >0 \implies \sqrt{ x^2 } > 0 \implies \sqrt{ x^2 } = |x|$$

## Infinity
> [!theorem] $\infty$ is Not In $\mathbb{R}$
> Take the following: Let $a,b,c\in \mathbb{R}$: 
> $$a+b = a+c \implies b =c$$
> Note that for Infinity: 
> $$\infty = \infty + 4 = \infty + 3$$
> Letting $\infty\in \mathbb{R}$ implies: 
> $$0 = 4 = 3$$
> Which cannot be true; ergo $\infty \not\in \mathbb{R}$.
> > I mean sure it works? I can put down a more rigorous one I guess here later. 

## Intervals 
We can define a general set of Intervals: 
> [!theorem] Closed Intervals 
> $$[a,b] \implies \forall x, a\leq x\leq b$$
> 

> [!theorem] Open Intervals
> $$(a,b) \implies \forall x, a < x < b$$
> Note, that the concept of "exhaustion" can apply into this; as we can progressively get closer to our endpoints without directly reaching them. 

> [!theorem] Half Open/Closed
> $$[a,b) \implies \forall x, a\leq x< b$$
> $$(a,b] \implies \forall x, a< x\leq b$$
> Note for infinity; all $\infty$-based bounds will have an *open* interval / bracket; as we cannot directly include it within $\mathbb{R}$. 

## Functions
Generally; a function is a *rule*; which assigns a number in a set (the "domain") to a **unique number in another set** (the "range"): That is; while multiple numbers can map to the same number in the range, the reverse cannot be true. 

> [!theorem] Algebraic Functions
> An algebraic function is a function that generally maps a set of inputs (notated as the domain) to a set of outputs (the outputs). For algebraic functions; these are defined by our familiar equations: 
> $$f(x) = x^2 +1$$
> Let our input set be defined as $A$, and our output set be defined as $B$; functions therefore generally: 
> $$f(A)  \mapsto B$$
> Where the set $A$ is defined as the domain, and the set $B$ is defined as the range. $A$ defines the valid values that our function can input; and $B$ defines the valid outputs that our function can provide. 
> 
> Note that the normal notation is to often refer to $y$ as the dependent, and $x$ as the independent variable. 

Note that functions do not need to be inherently *well-behaved* to be considered as a function, such as piecewise functions: 
$$f(x) = \begin{cases}
x^2 : x \neq 3\\
0: x =3
\end{cases}$$
Where this causes a *hole* at $x=3$; where our function jumps to $0$. 

### Expressions
Note that *some* algebraic expressions may not be considered as a function: 
$$\frac{x^2}{a^2} + \frac{y^2}{b^2}=1$$
Where one can get two answers for the respective value of the function; thus not giving us a function

In general; we can test this by using the *vertical-line test*. You should know how this works anyways. 
### Intervals 
We can define a function as *increasing* on an interval $I$, if:
$$f(x_{1}) < f(x_{2}) \land x_{1} < x_{2} \land x_{1},x_{2} \in I$$
Conversely; we can also define a function as decreasing if: 
$$f(x_{1}) > f(x_{2}) \land x_{1} > x_{2} \land x_{1},x_{2} \in I$$

Note that functions can only increase or decrease over an interval. 
### Even and Odd
> [!theorem] Even Functions
> $$\forall x \in A, f(x): A \mapsto B \to f(x) = f(-x)$$
>  A function is only even if $f(x) = f(-x)$, i.e. functions symmetric over $y$-axis. 

> [!theorem] Odd Functions
> $$\forall x \in A, f(x): A \mapsto B \to f(x) = -f(x)$$
> A function is only odd if $f(x) = -f(x)$, i.e. the function is symmetric over the $x$-axis. 
### Function Composition
We can notate function composition as: 
$$f \circ g(x) = f(g(x))$$
That is; $g(x) = y$ for some $f(y) = z$ for instance. Whatever that *nested* function inside is equivalent to is plugged in as it's respective domain into the other function. 

> Note that for $f \circ g(x)$: the *range* of $g(x)$ is plugged as the *domain* of $f(x)$. 

### Inequalities and Equalities 
For more info on these, see [[02 — The Real Number System]]. 

> [!theorem] Basic Arithmetical Theorem (BAT) 
> One can Add, Subtract, Multiply and Divide both sides of a **true** statement by the same factor (except $\frac{1}{0}$) and obtain another **true** statement. 
> 
> This effectively preserves our operations mainly for Inequalities. 
> > Note that multiplying / dividing by a negative number requires us to reverse the "direction" of our inequalities. 

The BAT is equivalent to Theorems O.3 and O.4. 
#### Statements 
Statements resolve into a true/false statement: such as $1+3=4$ and $2 <6$ are statements. 

Statements do not include *specifications* for values; such as a set of values or a singular value for a variable.

#### Inequalities with Variables
Take the following example: 
> What set is defined by the inequality of $-2(x-3) > 12$, that is, what values of x satisfy this inequality? 

We can do some basic algebra to solve for this: 
$$(x-3) < -6$$
$$x < -3$$
Therefore, $x\in (-\infty, -3)$. In general, for inequalities with variables; we seek to solve for a set/range of values that *that* respective variable must be in order for it to be true.

Take the following: 
> What set is defined by $5(x^2-x-6)>0$? 

We can do some basic algebra to isolate; 
$$(x^2-x-6) > 0$$
$$(x+2)(x-3)>0$$
We know that $x=-2,3 \to f(x)=0$. We simply just need to solve for the regions in which this function is *positive* (normally via a test table/sign table and testing values), where this is true when $x\in(-\infty,-2)\cup(3,\infty)$. 

How about reciprocals? take the following: 
> What set is defined by $\frac{x-1}{x+1}>1$? 

One method we can solve this is by solving it in terms of cases. Take $x+1 >0 \implies x>-1$
$$x-1 > x+1 \implies -1>1$$
This *cannot* ever be true, ergo this case is never true. Take $x+1<0 \implies x<-1$; implying $x$ is negative; thus: 
$$x-1 < x+1$$
$$-1 < 1$$
This statement is always true; ergo the only solution set for this problem is $x\in (-\infty,-1)$. 

The other case we can solve for is by moving everything to one side: 
$$\frac{x-1}{x+1}-1 >0 $$
$$\frac{x-1}{x+1}-\frac{x+1}{x+1} >0 $$
$$\frac{-2}{x+1}>0$$
From here, we can solve for cases for the sign of this; i.e. the sign of $(x+1)$. We know this will be true if $x+1<0 \implies x<-1$, getting us the same solution set of $x\in (-\infty, -1)$

Take the following: 
> What set is defined by $$\frac{2x+8}{x^2+8x+7}$$

We can factor this: 
$$\frac{2(x+4)}{(x+1)(x+7)}>0$$
We have to now consider once more using the sign table the following inequality of $(x+4)(x+1)(x+7)>0$. Solve for roots and work from there on a sign table to find values of $x$ that are positive, giving us the solution set of $x\in(-7,-4)\cup(-1,\infty)$.



#### Proving Inequalities
Given that: 
> $0 \leq a\leq b$, show that $$\frac{a}{1+a}\leq \frac{b}{1+b}$$

Since $a \land b\geq 0$, they are positive, ergo our denominators are positive, meaning that we can cross-multiply: 
$$a(1+b) \leq b(1+a)$$
$$a + ab \leq b + ab$$
Ergo, $a \leq b$. The rule of thumb for proofs is that they should be reversible operations, that is using the result, we can return to our original basis, and vice-versa; 
$$a \leq b =a + ab \leq b + ab = a(1+b) \leq b(1+a) \implies \frac{a}{1+a} \leq \frac{b}{1+b}$$
This is only true if and only if $a$ and $b$ are strictly positive; that is $0\leq a\leq b$. 

Given that: 
> $$x<0 \implies \sqrt{\frac{ x }{x+1}} <\sqrt{ \frac{x+1 }{x+2}}$$

We will first square both sides; giving us: 
$$\frac{x}{(x+1)}< \frac{x+1}{x+2}$$
Cross multiply and cancel: 
$$x(x+2) < (x+1)^2 \implies x^2 + 2x < x^2 + 2x + 1 \implies 0<1$$
This ends with an inherently true statement. Note that squaring is only defined for inequalities as:
> Given $a < b$, $$a^2 < b^2 \iff|a| < |b|$$. 
#### Absolute Value Inequalities
The main concept for Absolute Value Inequalities is that, as we break up our inequality into cases; the resulting set of inequalities / values must also comply with that original case. 

### Intro to Epsilon-Delta

Take the following inequality (Very closely linked to [[06 — Precise Limit Definition]]). 
$$|x-4| < 10^{-100}$$
Note that graphically; this means that we are looking for a value of $x$ in the range of $\{ 4-10^{-100},4+10^{-100} \}$; that is some tiny range around $x$. Consider this as: 

$$|x-c| <\delta$$
This now means a range between $(c-\delta,c+\delta)$. Consider that if $0 < |x-c| < \delta \implies x\neq c$! 

Now, consider the following inequality: 
$$|y-L| < \epsilon \to |f(x) - L| <\epsilon$$
This now means a range of $y$ values from $(L-\epsilon,L+\epsilon)$. 

For instance: Find the following: 
> $$\left|\frac{x}{x+2}\right| < 1$$

Note that since our absolute values can be distributed, then: 
$$|x| < |x+2|$$
We can solve via cases: 
* $x > 0 \implies |x| = x, x>0 \implies x+2 >2>0 \implies |x+2| = x+2 \to 0<2$ (Which leads us to say that for $x>0$, all values of $x$ hold.)
* $x<0 \implies |x| = -x$
	* $x+2 > 0 \implies |x+2| = x+2 \implies -x < x+2 \implies -2x < 2 \implies x>-1$
	* $x+2 < 0 \implies |x+2| = -(x+2) \implies -x < -x-2 \implies 0 < -2$ which isn't true. 
Our solution set is therefore: $x\in (-1,\infty)$
