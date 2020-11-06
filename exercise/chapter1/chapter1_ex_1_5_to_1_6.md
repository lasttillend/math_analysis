# Chapter 1 Exercise 1.5 ~ 1.6

## Exercises of 1.5 Cardinality

> **Exercise 1.5.1.** Finish the following proof for Theorem 1.5 .7 Assume $B$ is a countable set. Thus, there exists $f: \mathbf{N} \rightarrow B,$ which is $1-1$ and onto. Let $A \subseteq B$ be an infinite subset of $B .$ We must show that $A$ is countable. 
>
> Let $n_{1}=\min \{n \in \mathbf{N}: f(n) \in A\} .$ As a start to a definition of $g: \mathbf{N} \rightarrow A$.$\operatorname{set} g(1)=f\left(n_{1}\right) .$ Show how to inductively continue this process to produce a $1-1$ function $g$ from $\mathbf{N}$ onto $A$.

**Proof.**

For $k \ge 1$, define 
$$
n_{k+1} = \min \left\{n \in \mathbf{N}: f(n) \in A - \bigcup_{j=1}^k g(j) \right\}, \\
g(k+1) = f(n_{k+1}).
$$
then $g$ is one-to-one since $f$ is. To see $g$ is onto, let $x \in A$, then there exists $n^* \in \mathbf{N}$ such that $f(n^*) = x$ since $f$ is onto. This means there are at most $n^*$ terms in $A$ which were chosen by our construction before $x$ is to be chosen . Hence, as long as we exhaust these terms, as our construction does, the next term we pick is exactly $x$. Therefore, $g$ is a $1-1$ function from $\mathbf{N}$ onto $A$.

---

> **Exercise 1.5.2.** Review the proof of Theorem $1.5 .6,$ part
> (ii) showing that $\mathbf{R}$ is uncountable, and then find the flaw in the following erroneous proof that $\mathbf{Q}$ is uncountable:
>
> Assume, for contradiction, that $\mathbf{Q}$ is countable. Thus we can write $\mathbf{Q}=$ $\left\{r_{1}, r_{2}, r_{3}, \ldots\right\}$ and, as before, construct a nested sequence of closed intervals with $r_{n} \notin I_{n} .$ Our construction implies $\bigcap_{n=1}^{\infty} I_{n}=\emptyset$ while NIP implies $\bigcap_{n=1}^{\infty} I_{n} \neq \emptyset .$ This contradiction implies $\mathbf{Q}$ must therefore be uncountable.

**Proof.**

Unlike $\mathbf{R}$, $\mathbf{Q}$ does not have NIP, so we cannot apply it here.

---

> **Exercise 1.5.3.** Use the following outline to supply proofs for the statements in Theorem 1.5.8
> (a) First, prove statement (i) for two countable sets, $A_{1}$ and $A_{2}$. Example 1.5.3 (ii) may be a useful reference. Some technicalities can be avoided by first replacing $A_{2}$ with the set $B_{2}=A_{2} \backslash A_{1}=\left\{x \in A_{2}: x \notin A_{1}\right\} .$ The point of this is that the union $A_{1} \cup B_{2}$ is equal to $A_{1} \cup A_{2}$ and the sets $A_{1}$ and $B_{2}$ are disjoint. (What happens if $B_{2}$ is finite?)
> Now, explain how the more general statement in (i) follows.
> (b) Explain why induction cannot be used to prove part (ii) of Theorem 1.5.8 from part (i).
> (c) Show how arranging $\mathbf{N}$ into the two-dimensional array
> $$
> \begin{array}{cccccc}
> 1 & 3 & 6 & 10 & 15 & \cdots \\
> 2 & 5 & 9 & 14 & \cdots & \\
> 4 & 8 & 13 & \cdots & & \\
> 7 & 12 & \cdots & & & \\
> 11 & \cdots & & & &
> \end{array}
> $$
> leads to a proof of Theorem 1.5.8 (ii).

**Proof.**

(a) Define $B_2 = A_2 \backslash A_1 = \{x \in A_2: x \notin A_1 \}$, then $A_1 \cup B_2 = A_1 \cup A_2$.

If $B_2$ is finite, i.e., $B_2 = \{b_1, b_2, \cdots, b_N \}$ for some $N \in \mathbf{N}$. Since $A_1$ is countable, there is a one-to-one and onto function $f:\mathbf{N}\to A_1$, then we can define function $g: \mathbf{N} \to A_1 \cup A_2$ by
$$
g(n)=\left\{\begin{array}{ll}b_n, & 1 \le n \le N \\ f(n-N), &n \gt N.\end{array}\right.
$$
Then $g$ is one-to-one and onto and hence $A_1 \cup A_2$ is countable.

Now consider the case if $B_2$ is infinite, then $B_2 \subseteq A_2$ is countable since $A_2$ is countable. So there is a one-to-one and onto function $g:\mathbf{N} \to B_2$. Then we can define function $h:\mathbf{N} \to A_1 \cup A_2$ by alternating between $f$ and $g$ on odd and even terms, that is,
$$
h(n)=\left\{\begin{array}{ll}
f((n+1) / 2), & \text { if } n \text { is odd } \\
g(n / 2), & \text { if } n \text { is even }.
\end{array}\right.
$$
We can see $h$ is one-to-one and onto and hence $A_1 \cup A_2$ is countable.

By induction, it follows that $\bigcup_{i=1}^n A_i$ is countable for every $n \in \mathbf{N}$.

(b) Induction cannot be used here because induction only gives us that for every finite case, the finite union of countable sets is countable

(c) Let $A_1, A_2, A_3, \cdots$ be countable collection of sets. We redefine
$$
A_1 = A_1, A_2 = A_2 \backslash A_1,
$$
and 
$$
A_n = A_n \backslash \bigcup_{k=1}^{n-1} A_k
$$
recursively. If there exists $N \in \mathbf{N}$ such that $A_n = \empty$ for all $n \ge N$ then this reduces to finite union which can be shown using induction. If any of $A_k$ is finite then, we drop it as union of finite and countable is countable. Thus we get countable collection $A_1, A_2, A_3, \cdots$ that is countably infinite and disjoint pairwise. Then there exists one-to-one and onto function
$$
f_n: \mathbf{N} \rightarrow A_n
$$
for each $n \in \mathbf{N}$. Now arrange $\mathbf{N}$ as follows:
$$
\begin{array}{cccccc}
1 & 3 & 6 & 10 & 15 & \cdots \\
2 & 5 & 9 & 14 & \cdots & \\
4 & 8 & 13 & \cdots & & \\
7 & 12 & \cdots & & & \\
11 & \cdots & & & &
\end{array}
$$
Let $B_1 = \{1, 3, 6, \cdots\}$, $B_2 = \{2, 5, 9, \cdots\}$, $B_3 = \{4, 8, 13, \cdots \} \cdots$ Since each $B_n \subseteq \mathbf{N}$ for all $n \in \mathbf{N}$, they are countable and there exists one-to-one and onto function $g_n: \mathbf{N} \rightarrow B_n$.

For any $n \in \mathbf{N}$, let $A_n = \{a_{nk}:k \in \mathbf{N}\}$ as $f_n(k) = a_{nk}$ and $B_n = \{b_{nk}: k \in \mathbf{N}\}$ as $g_n(k) = b_{nk}$.

Define, for each $n \in \mathbf{N}, h: B_n \rightarrow A_n$ by $h(b_{nk}) = a_{nk}$. Since $b_{nk}$ and $a_{nk}$ are distinct for each pair $(n, k)$, the function $h$ is one-to-one. Also for each $a_{nk}$ there exists $b_{nk}$ such that $h(b_{nk}) = a_{nk}$ so $h$ is onto.

Now 
$$
h: \bigcup_{n=1}^{\infty} B_{n} \rightarrow \bigcup_{n=1}^{\infty} A_{n}
$$
is one-to-one since for each $n \in \mathbf{N}, A_n, B_n$ are disjoint pairwise. But $\cup_{n=1}^{\infty} B_n = \mathbf{N}$ thus we get one-to-one and onto function $h$ such that
$$
h: \mathbf{N} \rightarrow \bigcup_{n=1}^{\infty} A_{n}
$$
so $\bigcup_{n=1}^{\infty}A_n$ is countable.



> **Exercise 1.5.4**
> (a) Show $(a, b) \sim \mathbf{R}$ for any interval $(a, b)$
> (b) Show that an unbounded interval like $(a, \infty)=\{x: x>a\}$ has the same cardinality as $\mathbf{R}$ as well.
> (c) Using open intervals makes it more convenient to produce the required $1-1,$ onto functions, but it is not really necessary. Show that [0,1)$\sim(0,1)$ by exhibiting a $1-1$ onto function between the two sets.

**Proof.**

(a) Define $f: (a, b) \rightarrow (-\frac{b-a}{2},  \frac{b-a}{2})$ by $f(x) = x - \frac{a+b}{2}$, then $f$ is one-to-one and onto. Define $g: (-\frac{b-a}{2},  \frac{b-a}{2}) \rightarrow (-1, 1)$ by $g(x) = \frac{2x}{b-a}$, then $g$ is also one-to-one and onto. By Example 1.5.4, $(-1, 1) \sim \mathbf{R}$, so there is some one-to-one and onto function $h:(-1, 1) \rightarrow \mathbf{R}$. Take composition of $f, g$ and $h$, we can obtain a one-to-one function $\theta:(a, b) \rightarrow \mathbf{R}$, and hence $(a, b) \sim \mathbf{R}$.

(b) Define $f:(a, \infty) \rightarrow \mathbf{R}$ by $f(x) = x - \frac{1}{x - a}$, we will show $f$ is one-to-one and onto.

Suppose $f(x_1) = f(x_2)$, then 
$$
\begin{align}
x_1 - \frac{1}{x_1 -a} &= x_2 - \frac{1}{x_2 -a} \\
\implies x_2 - x_1 &=\frac{1}{x_2 - a} - \frac{1}{x_1 -a} = \frac{x_1 - x_2}{(x_1 - a)(x_2 - a)}.
\end{align}
$$
So either $x_2 - x_1 = 0$ or $-1 = \frac{1}{(x_1 - a)(x_2 - a)}$, but $x_1$ and $x_2$ are larger than $a$, so the second case is impossible. Hence, we have $x_1 = x_2$ holds and $f$ is one-to-one.

Now let $c \in \mathbf{R}$, then
$$
x-\frac{1}{x-a}=c
$$
gives
$$
x = \frac{a + c \pm \sqrt{a^2 + c^2 - 2ac + 4}}{2} = \frac{a+c \pm \sqrt{(a - c)^2 + 4}}{2}.
$$
If $c \gt a$, then
$$
x = \frac{a + c + \sqrt{(a - c)^2 + 4}}{2} \gt \frac{a + c + \sqrt{(a - c)^2}}{2} = c,
$$
so $x \in (a, \infty)$.

If $c = a$, then
$$
x = a + 1 \in (a, \infty).
$$
If $c \lt a$, then
$$
x = \frac{a + c + \sqrt{(a - c)^2 + 4}}{2} \gt \frac{a + c + \sqrt{(a - c)^2}}{2} = a,
$$
so $x \in (a, \infty)$. 

Therefore, $f$ is onto.

(c) Let $x_1, x_2, x_3, \cdots$ be a strictly decreasing infinite sequence or strictly increasing sequence on $(0, 1)$. Let $f: [0, 1) \rightarrow (0, 1)$ be a function defined by
$$
f(0) = x_1, f(x_n) = x_{n+1}
$$
and for all $x \in (0, 1) \backslash \{x_1, x_2, x_3, \cdots\}$,
$$
f(x) = x.
$$
Then $f$ ​is one-to-one and onto.



> **Exercise 1.5.5**
> (a) Why is $A \sim A$ for every set $A ?$
> (b) Given sets $A$ and $B$, explain why $A \sim B$ is equivalent to asserting $B \sim A$.
> (c) For three sets $A, B,$ and $C,$ show that $A \sim B$ and $B \sim C$ implies $A \sim C$ These three properties are what is meant by saying that $\sim$ is an equivalence relation.

**Proof.**

(a) Because the identity map $I: A \rightarrow A$ is one-to-one and onto, $A \sim A$ holds.

(b) $A \sim B$ means there exists some one-to-one and onto function $f: A \rightarrow B$. This implies that the inverse function $f^{-1}: B \rightarrow A$ exists and $f^{-1}$ is one-to-one and onto, so $B \sim A$.

(c) Suppose $A \sim B$ and $B \sim C$ then there exists one-to-one and onto functions $f: A \rightarrow B$ and $g: B \rightarrow C$. For every $a \in A$, define $h: A \rightarrow C$ by $h(a) = (g \circ f)(a)$. As $f$ and $g$ are one-to-one and onto, so is their composition $h$ and hence $A \sim C$.



> **Exercise 1.5.6**
> (a) Give an example of a countable collection of disjoint open intervals.
> (b) Give an example of an uncountable collection of disjoint open intervals, or argue that no such collection exists.

**Proof.**

(a) For example, let $A_n= (n, n + 1)$, then $\{A_n:n \in \mathbf{N} \}$ is a countable collection of disjoint open intervals.

(b) This is impossible. Every collection of disjoint open intervals in $\mathbf{R}$ is countable because we can always choose a rational number in each of them and rationals are countable.



>**Exercise $1.5.7.$** Consider the open interval $(0,1),$ and let $S$ be the set of points in the open unit square; that is, $S=\{(x, y): 0<x, y<1\}$
>(a) Find a $1-1$ function that maps (0,1) into, but not necessarily onto, $S$. (This is easy.)
>(b) Use the fact that every real number has a decimal expansion to produce a $1-1$ function that maps $S$ into $(0,1) .$ Discuss whether the formulated function is onto. (Keep in mind that any terminating decimal expansion such as .235 represents the same real number as $.234999 \ldots .$
>
>The Schröder-Bernstein Theorem discussed in Exercise 1.5.11 can now be applied to conclude that $(0,1)\sim S$.

**Proof.**

(a) Define $f:(0, 1) \rightarrow S$ by
$$
f(x) = (x, \frac{1}{2}),
$$
then $f$ has the desired property.

(b) Suppose $(x, y) \in S$ and $x, y$ have the decimal expansion $0.d_1d_2d_3\cdots$ and $0.e_1e_2e_3\cdots$ respectively. Since some real numbers have two decimal expansions as the hint pointed out, we use the one that terminates, padded with zeroes, so that $\frac{1}{2}$ will be represented by $0.5000\cdots$, not by $0.4999\cdots$. 

Now, with no ambiguity, we can define the function $f:S \rightarrow (0, 1)$ by
$$
f(x, y) = 0.d_1e_1d_2e_2d_3e_3\cdots,
$$
then $f$ maps $S$ into $(0, 1)$.

To see $f$ is not onto, consider the number $\frac{1}{11}$, which has decimal expansion like $0.909090\cdots$. For $f$ to map some point  $(x, y)$  to this particular number, $y$ must be $0$, which is not in $(0, 1)$. Hence, $f$ cannot be onto.



> **Exercise1.5.8.** Let $B$ be a set of positive real numbers with the property that adding together any finite subset of elements from $B$ always gives a sum of 2 or less. Show $B$ must be finite or countable.

**Proof**. 

Suppose $B$ has infinitely many elements. For each $n \in \mathbf{N}$, let
$$
B_n = \{b \in B: b \gt \frac{2}{n} \} \subset B.
$$
Then $B_n$ cannot have more than $n - 1$ distinct elements, otherwise, the sum of $n$ distinct elements in $B_n$ would be greater than 2.

But 
$$
B = \bigcup_{n \in \mathbf{N}}B_n.
$$
Since $\mathbf{N}$ is countable and each $B_n$ is finite, $B$ is countable.



> **Exercise 1.5.9**. A real number $x \in \mathbf{R}$ is called algebraic if there exist integers $a_{0}, a_{1}, a_{2}, \ldots, a_{n} \in \mathbf{Z},$ not all zero, such that
> $
> a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{1} x+a_{0}=0
> $
> Said another way, a real number is algebraic if it is the root of a polynomial with integer coefficients. Real numbers that are not algebraic are called transcendental numbers. Reread the last paragraph of Section 1.1. The final question posed here is closely related to the question of whether or not transcendental numbers exist.
> (a) Show that $\sqrt{2}, \sqrt[3]{2},$ and $\sqrt{3}+\sqrt{2}$ are algebraic.
> (b) $\operatorname{Fix} n \in \mathbf{N},$ and let $A_{n}$ be the algebraic numbers obtained as roots of polynomials with integer coefficients that have degree $n .$ Using the fact that every polynomial has a finite number of roots, show that $A_{n}$ is countable.
> (c) Now, argue that the set of all algebraic numbers is countable. What may we conclude about the set of transcendental numbers?

**Proof.**

(a) For $\sqrt{2}$ and $\sqrt{3}$:
$$
\sqrt{2}: x^2 - 2 = 0 \\
\sqrt{3}: x^3 - 2 = 0.
$$
As for $\sqrt{3}+\sqrt{2}$, we have 
$$
(x-(\sqrt{2}+\sqrt{3}))(x+(\sqrt{2}+\sqrt{3}))=x^{2}-(5+2 \sqrt{6})
$$
and 
$$
(x^2 -(5 + 2 \sqrt{6}))(x^2 - (5 - 2\sqrt{6}))=x^4-10x^2+1=(x^2-5)^2-24.
$$
Hence $\sqrt{2}+\sqrt{3}$ is root of equation $(x^2-5)^2-24 = 0$ and therefore, it is algebraic.

(b) For each $k \in \mathbf{N}$, consider the $n$ degree polynomial with $\sum_{i=0}^n \vert a_i\vert \le k$. Let $A_{nk}$ be the set of algebraic numbers obtained as roots of such polynomials. Then $A_{nk}$ is finite since there are only finite different values for $a_i$ and roots of polynomials are finite. But we have
$$
\bigcup_{k=1}^{\infty} A_{nk} = A_n.
$$
Since each $A_{nk}$ is countable, $A_n$ must be countable.

(c) The set of all algebraic number is given by
$$
\bigcup_{n=1}^{\infty} A_n.
$$
Since each $A_n$ is countable, the countable union must also be countable.

Because $\mathbf{R}$ can be decomposed as algebraic and transcendental and we have just proved algebraic numbers are countable, transcendental numbers must be uncountable.



> **Exercise 1.5.10**
> (a) Let $C \subseteq[0,1]$ be uncountable. Show that there exists $a \in(0,1)$ such that $C \cap[a, 1]$ is uncountable.
> (b) Now let $A$ be the set of all $a \in(0,1)$ such that $C \cap[a, 1]$ is uncountable, and set $\alpha=\sup A .$ Is $C \cap[\alpha, 1]$ an uncountable set?
> (c) Does the statement in (a) remain true if "uncountable" is replaced by "infinite"?

**Proof.**

(a) Assume the contrary that for every $a \in (0, 1)$, $C \cap [a, 1]$ is countable. Consider the sequence $a_n = \frac{1}{n} \in (0, 1)$, for $n \in \mathbf{N}$. Then 
$$
C \cap [\frac{1}{n}, 1]
$$
is countable for every $n \in \mathbf{N}$, so
$$
\bigcup_{n=1}^{\infty}\left(C\cap \left[\frac{1}{n}, 1\right] \right) = C \cap \bigcup_{n=1}^{\infty}\left[\frac{1}{n}, 1\right] = C \cap (0, 1]
$$
is also countable.

But 
$$
\begin{align}
C&=C \cap [0, 1] = C \cap \left((0, 1]\cup \{0\}\right) \\
&= (C \cap (0, 1] ) \cup (C \cap \{0\}) \\
&\subseteq (C \cap (0, 1] ) \cup \{0\}
\end{align}
$$
which implies $C$ is countable, a contradiction. 

(b) Since $C \cap [\alpha+\frac{1}{n}, 1]$ is countable for every $n \in \mathbf{N}$ and
$$
C \cap[\alpha, 1] \subseteq\left(\bigcup_{n=1}^{\infty}\left(C \cap\left[\alpha+\frac{1}{n}, 1\right]\right)\right) \cup\{\alpha\},
$$
$C \cap[\alpha, 1]$ is also countable.

(c) No. Take $C = \{\frac{1}{n}: n \in \mathbf{N} \}$, then for any $a \in (0, 1)$, there exists $n \in \mathbf{N}$ such that $\frac{1}{n} \lt a$, so
$$
C \cap [a, 1]
$$
is finite. 



> **Exercise 1.5.11** (Schröder-Bernstein Theorem). Assume there exists a
> $1-1$ function $f: X \rightarrow Y$ and another $1-1$ function $g: Y \rightarrow X .$ Follow the steps to show that there exists a $1-1,$ onto function $h: X \rightarrow Y$ and hence $X \sim Y$ The strategy is to partition $X$ and $Y$ into components
> $$
> X=A \cup A^{\prime} \quad \text { and } \quad Y=B \cup B^{\prime}
> $$
> with $A \cap A^{\prime}=\emptyset$ and $B \cap B^{\prime}=\emptyset,$ in such a way that $f$ maps $A$ onto $B,$ and $g$ $\operatorname{maps} B^{\prime}$ onto $A^{\prime}$
> (a) Explain how achieving this would lead to a proof that $X \sim Y$
> (b) $\operatorname{Set} A_{1}=X \backslash g(Y)=\{x \in X: x \notin g(Y)\}$ (what happens if $A_{1}=\emptyset ?$ ) and inductively define a sequence of sets by letting $A_{n+1}=g\left(f\left(A_{n}\right)\right) .$ Show that $\left\{A_{n}: n \in \mathbf{N}\right\}$ is a pairwise disjoint collection of subsets of $X,$ while $\left\{f\left(A_{n}\right): n \in \mathbf{N}\right\}$ is a similar collection in $Y$
> (c) Let $A=\bigcup_{n=1}^{\infty} A_{n}$ and $B=\bigcup_{n=1}^{\infty} f\left(A_{n}\right) .$ Show that $f$ maps $A$ onto $B$
> (d) $\operatorname{Let} A^{\prime}=X \backslash A$ and $B^{\prime}=Y \backslash B .$ Show $g$ maps $B^{\prime}$ onto $A^{\prime}$

**Proof.**

I only get an informal visual proof: the blue parts on the left are $A_n$s  and they are mapped onto the blue parts on the right. Similarly, the orange parts  on the right, which constitute $B^{\prime}$ in the question, are mapped onto the orange part on the left.

![1.5.11](/Users/Apple/notes/Math/Analysis/my article/understanding_analysis_notes/exercise/chapter1/1.5.11.jpeg)

## Exercises of 1.6 Cantor’s Theorem

> **Exercise 1.6 .1.** Show that (0,1) is uncountable if and only if $\mathbf{R}$ is uncountable. This shows that Theorem 1.6 .1 is equivalent to Theorem 1.5.6

**Proof.**

Define the function $f:(0, 1) \rightarrow \mathbf{R}$ by 
$$
f(x)=\tan \left(\pi x-\frac{\pi}{2}\right),
$$
then $f$ is one-to-one and onto. Hence, $(0, 1) \sim \mathbf{R}$. 



> **Exercise 1.6.2**
> (a) Explain why the real number $x=. b_{1} b_{2} b_{3} b_{4} \ldots$ cannot be $f(1)$
> (b) Now, explain why $x \neq f(2),$ and in general why $x \neq f(n)$ for any $n \in \mathbf{N}$
> (c) Point out the contradiction that arises from these observations and conclude that (0,1) is uncountable.

**Proof.**

(a) Because $a_{11} \neq b_1$.

(b) Because $a_{nn} \neq b_n$ for every $n \in \mathbf{N}$.

(c) We have produced a real number $x$ which cannot be mapped onto by $f$. This is a contradiction to the fact that $f$ is onto.



> **Exercise 1.6.3.** Supply rebuttals to the following complaints about the proof of Theorem 1.6.1
> (a) Every rational number has a decimal expansion, so we could apply this same argument to show that the set of rational numbers between 0 and 1 is uncountable. However, because we know that any subset of Q must be countable, the proof of Theorem 1.6.1 must be flawed.
> (b) Some numbers have two different decimal representations. Specifically, any decimal expansion that terminates can also be written with repeating 9's. For instance, $1 / 2$ can be written as .5 or as $.4999 \ldots .$ Doesn't this cause some problems?

**Proof.**

(a) Note that  $x$ is irrational, so applying the same argument here is invalid.

(b ) The only numbers in $(0,1)$ with two decimal representations are those with one representation ending in an infinite string of nines and the other in an infinite string of zeroes, but by our construction of $b_n$ it is either 2 or 3. Hence, we are not creating a different decimal of the same number and there is no ambigluity here.



> **Exercise 1.6.4.** Let $S$ be the set consisting of all sequences of 0 's and 1 's. Observe that $S$ is not a particular sequence, but rather a large set whose elements are sequences; namely,
> $$
> S=\left\{\left(a_{1}, a_{2}, a_{3}, \dots\right): a_{n}=0 \text { or } 1\right\}.
> $$
> As an example, the sequence $(1,0,1,0,1,0,1,0, \ldots)$ is an element of $S,$ as is the sequence $(1,1,1,1,1,1, \ldots)$.
>
> Give a rigorous argument showing that $S$ is uncountable.

**Proof.**

Suppose $S$ were countable, then we may write 
$$
\begin{array}{l}
s_{1}=\left(a_{11}, a_{12}, a_{13}, \ldots\right) \\
s_{2}=\left(a_{21}, a_{22}, a_{23}, \ldots\right) \\
s_{3}=\left(a_{31}, a_{32}, a_{33}, \ldots\right) \\
\cdots
\end{array}
$$
Now, let
$$
r_{n}=\left\{\begin{array}{ll}
1 & \text { if } a_{n n}=0 \\
0 & \text { if } a_{n n}=1
\end{array}\right. ,
$$
and take 
$$
r = (r_1, r_2, r_3, \cdots),
$$
then $r \in S$ but $r \neq s_n$ for every $n$, a contradiction.



> **Exercise 1.6.5**
> (a) Let $A=\{a, b, c\} .$ List the eight elements of $P(A) .$ (Do not forget that $\emptyset$ is considered to be a subset of every set.)
> (b) If $A$ is finite with $n$ elements, show that $P(A)$ has $2^{n}$ elements.

**Proof.**

(a) $P(A)=\{\emptyset, \{a\}, \{b\}, \{c\}, \{a, b\}, \{a, c\}, \{b, c\}, \{a, b, c\}\}$.

(b) Every element of $A$ can either be picked or not picked, so $P(A)$ has $2^n$ elements.



> **Exercise 1.6.6**
>
> (a) Using the particular set $A=\{a, b, c\}$, exhibit two different 1-1 mappings from $A$ into $P(A)$.
>
> (b) Letting $C=\{1, 2, 3, 4\}$, produce an example of a 1-1 map $g:C \rightarrow P(C)$.
>
> (c) Explain why, in parts (a) and (b), it is impossible to construct mappings that are onto.

**Proof.**

(a) Define $f_1: A \rightarrow P(A)$ by
$$
f_1(x) = \{x\}, \forall x \in A.
$$
Define $f_2:A \rightarrow P(A)$ by
$$
f_2(x) = A - \{x\}, \forall x \in A.
$$
(b) Define $g: C \rightarrow P(C)$ by
$$
g(x) = \{x\}, \forall x \in \{1, 2, 3, 4\}.
$$
(c) Because the sets in parts (a) and (b) are all finite (suppose n elements) and their power power sets have $2^n$ elements which have much more elements.



> **Exercise 1.6.7.** Return to the particular functions constructed in Exercise 1.6.6 and construct the subset $B$ that results using the preceding rule. In each case, note that $B$ is not in the range of the function used.

**Proof.**

For the function $f_1$, $B=\emptyset$ and it is not equal to $f_1(a)$ for any $a \in A$.

For the function $f_2$, $B=\{a, b, c\}$ and it is not equal to $f_2(a)$ for any $a \in A$.

The case for function $g$ is similar to the function $f_1$.



> **Exercise 1.6.8.** (a) First, show that the case $a^{\prime} \in B$ leads to a contradiction.
>
> (b) Now, finish the argument by showing that the case $a^{\prime} \notin B$ is equally unacceptable.

**Proof.** 

(a) If $a^{\prime} \in B$, then $a^{\prime} \notin f(a^{\prime})=B$, which is a contradiction.

(b) If $a^{\prime} \notin B$, then $a^{\prime} \in f(a^\prime)=B$, which is also a contradiction.



> **Exercise 1.6.9** Using the various tools and techniques developed in the last two sections (including the exercises from Section 1.5), give a compelling argument showing that $P(\mathbf{N}) \sim \mathbf{R}$.

**Proof.**

Since $\mathbf{R} \sim (0, 1)$, we will show that $(0, 1) \sim P(\mathbf{N})$. We will show that there exists $f:(0, 1) \rightarrow P(\mathbf{N})$ and $g: P(\mathbf{N}) \rightarrow (0, 1)$ which are one-to-one. Then Schroder-Bernstein theorem tells us that $(0, 1) \sim P(\mathbf{N})$.

Existence of one-to-one function $f:(0, 1) \rightarrow P(\mathbf{N})$.

If $x \in (0, 1)$, then $x=0.a_1a_2a_3\cdots$, where $a_n \in \{0, 1, \cdots, 9\}$ and not equal to zero for all $n \in \mathbf{N}$. To avoid the ambiguity of two decimal representation of the same number, we choose the representation ending with infinite string of zeroes. Define $f:(0, 1) \rightarrow P(\mathbf{N})$ by
$$
f(x) = \{a_1, 10a_2, 10^2a_3, \cdots\}.
$$
Now $f$ is one-to-one since $x_1 \neq x_2$ implies $x_1$ differ from $x_2$ at least at one place (say at $i$-th place ), then $10^{i-1}a_{1i} \neq 10^{i-1}a_{2i}$, so $f(x_1) \neq f(x_2)$. Hence $f$ is one-to-one.

Existence of one-to-one function $g:P(\mathbf{N}) \rightarrow (0, 1)$.

Let $x \in P(\mathbf{N})$. Define $g(x)=0.b_1b_2b_3\cdots$, where $b_n=2$ if $n \in x$ and $b_n = 3$ if $n \notin x$. Then $g$  is one-to-one.

To see this, suppose $x_1 \neq x_2$, then there is some $n \in x_1$ such that $n \notin x_2$, so $b_n=2$ in decimal expansion of $g(x_1)$ and $b_n=3$ for $g(x_2)$. Hence $g(x_1) \neq g(x_2)$.



> **Exercise 1.6.10.** As a final exercise, answer each of the following by establishing a $1-1$ correspondence with a set of known cardinality.
> (a) Is the set of all functions from \{0,1\} to $\mathbf{N}$ countable or uncountable?
> (b) Is the set of all functions from $\mathbf{N}$ to \{0,1\} countable or uncountable?
> (c) Given a set $B,$ a subset $\mathcal{A}$ of $P(B)$ is called an antichain if no element of $\mathcal{A}$ is a subset of any other element of $\mathcal{A} .$ Does $P(\mathbf{N})$ contain an uncountable antichain?

**Proof.**

(a) Let $S=\{f:(f(0), f(1)) \subset \mathbf{N} \times \mathbf{N}\} .$ Define $g: \mathbf{N} \times \mathbf{N} \rightarrow S$ by
$$
g(n, m) = f
$$
if $f(0) = n$, $f(1) = m$. Then $g$ is one-to-one and onto.

To see $g$ is one-to-one: if $(n_1, m_1) \neq (n_2, m_2)$, then $g(n_1, m_1)\neq g(n_2, m_2)$ since it would map to functions which maps $\{0, 1\}$ to different values.

To see $g$ is onto: for any $f\in S$, $f(\{0, 1\})=\{f(0), f(1)\}$, so $g(f(0), f(1))=f$.

Meanwhile, 
$$
\mathbf{N} \times \mathbf{N} = \bigcup_{n=1}^{\infty}\bigcup_{k=1}^{\infty}\{(n, k)\} \sim \mathbf{N}.
$$
Hence 
$$
\mathbf{N} \sim \mathbf{N} \times \mathbf{N} \sim S.
$$
Therefore $S$ is countable.

(b) Let
$$
S = \{f: f(n) \in \{0, 1\}, n \in \mathbf{N}\}.
$$
Suppose $S$ were countable, then we can write
$$
\begin{array}{l}
f_{1}(\mathbf{N})=\left\{f_{1}(1), f_{1}(2), f_{1}(3), \ldots\right\} \\
f_{2}(\mathbf{N})=\left\{f_{2}(1), f_{2}(2), f_{2}(3), \ldots\right\} \\
f_{3}(\mathbf{N})=\left\{f_{3}(1), f_{3}(2), f_{3}(3), \ldots\right\} \\
\cdots
\end{array}
$$
Define function $g:\mathbf{N} \rightarrow \{0, 1\}$ by $g(n) \neq f_n(n)$. Then $g \neq f_n$ for any $n \in \mathbf{N}$, which is a contradiction. 

(c) Let
$$
S = \{(a_1, a_2, a_3, \cdots): a_n \in \{0, 1\}\}.
$$
Define $f:S \rightarrow P(\mathbf{N})$ by
$$
f(s) = \{b_1, b_2, b_3, \cdots\},
$$
where $b_k= 2k$ if $a_k=0$ and $b_k=2k-1$ if $a_k=1$. Now $f$ is one-to-one since $s_1 \neq s_2$ implies $a_{1k} \neq a_{2k}$ for some $k \in \mathbf{N}$ so $b_{1k}$ and $b_{2k}$ differ accordingly (being odd or even accordingly).

Now $f(S)$ is an anti chain since $s_1 \neq s_2$ implies $f(s_1)$ differs from  $f(s_2)$ at certain position by an element so neither includes the other. Thus $f(S)$ is an antichain. Since $S$ is uncountable by Exercise 1.6.4, $S \sim f(S)$ so $f(S)$ is an uncountable antichain in $P(\mathbf{N})$.