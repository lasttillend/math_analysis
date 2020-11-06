# Chapter 1 Exercise 1.2 ~ 1.4

## Exercises of 1.2 Some Preliminaries

**E.x. 1.2.1** (a) Prove that $\sqrt{3}$ is irrational. Does a similar argument work to show $\sqrt{6}$ is irrational? 

(b) Where does the proof of Theorem 1.1.1 break down if we try to use it to prove $\sqrt{4}$ is irrational?

**Proof:**

(a) Suppose that $\sqrt{3}$ is rational, then it can be written as
$$
\sqrt{3} = \frac{p}{q},
$$
where $p$ and $q$ are integers with no common factors. If we square both sides, then
$$
\begin{align}
p^2 &= 3q^2 \\
2q^2 &= p^2 - q^2 = (p+q)(p-q).
\end{align}
$$
If $q$ is even, then $p^2 = 3q^2$ is even, which implies $p$ is even. However, this is impossible since $p$ and $q$ have no common factors. So $q$ must be odd and so does $p$. Write $p=2n+1$ and $q=2m+1$, then
$$
\begin{align}
p + q &= 2(n + m + 1) \\
p - q &= 2(n - m),
\end{align}
$$
which implies
$$
\begin{align}
2q^2 &= 2(n+m+1)\cdot2(n-m) \\
q^2 &= 2(n+m+1)(n-m).
\end{align}
$$
The above equation means $q$ is even, a contradiction. 

Now we proceed to show $\sqrt{6}$ is irrational:

Similarly,
$$
p^2 = 6 q^2.
$$
Thus, $p$ must be even. Write $p = 2m$ and substitute into the above equation:
$$
\begin{align}
4m^2 &= 6q^2  \\
2m^2 &= 3q^2  \\
2(m+q)(m-q) &= q^2.
\end{align}
$$
Therefore, $q$ must be even, a contradiction.

(b) We assume that $\sqrt{4} = \frac{p}{q}$ and square both sides and get
$$
p^2 = 4q^2.
$$
Since $4$ divides RHS, it must divide LRH. Since $4$ is perfect square, $p$ need not be of form $p=4r$ (it can be of form $p=2r$) for some integer $r$ . This is where Theorem 1.1.1 breaks down.



**E.x. 1.2.2.** Show that there is no rational number $r$ satisfying $2^r = 3$.

**Proof:** Suppose on the contrary that there is some rational number $r=\frac{p}{q}$, where $q\ne0$ satisfying the equation, then
$$
2^\frac{p}{q} =3.
$$
Taking $q$-th power of both sides, we get $2^p=3^q$. We have reach a contradition here, since the LHS must be even and RHS must be odd.



**E.x. 1.2.3.** 

Decide which of the following represent true statements about the nature of sets. For any that are false, provide a specific example where the statement in question does not hold.

(a) If $A_{1} \supseteq A_{2} \supseteq A_{3} \supseteq A_{4} \cdots$ are all sets containing an infinite number of elements, then the intersection $\bigcap_{n=1}^{\infty} A_{n}$ is infinite as well.
(b) If $A_{1} \supseteq A_{2} \supseteq A_{3} \supseteq A_{4} \cdots$ are all finite, nonempty sets of real numbers, then the intersection $\bigcap_{n=1}^{\infty} A_{n}$ is finite and nonempty.
$(\mathrm{c}) A \cap(B \cup C)=(A \cap B) \cup C$
(d) $A \cap(B \cap C)=(A \cap B) \cap C$
$(\mathrm{e}) A \cap(B \cup C)=(A \cap B) \cup(A \cap C)$

**Proof:**

(a) False. Counterexample: $A_n=[0, \frac{1}{n}]$.

(b) True. 

The cardinality of each set $A_n$ forms a non-increasing sequence:
$$
\vert A_1 \vert \ge \vert A_2 \vert \ge ...
$$
Each $\vert A_n \vert \gt 0$ and $A_1$ is finite. So this is a non-increasing sequence bounded below by 0 but none of them is zero. Hence there must be some $N\in \mathbb{N}$ such that $\vert A_n \vert = \vert A_N \vert$ for all $n \ge N$ (otherwise, $\vert A_n \vert$ will decrease to be less than 0). This gives 
$$
\bigcap_{n=1}^{\infty} A_n = A_N,
$$
which is finite and non-empty.

(c) False. Counterexample: $A=\{1\}, B=\{2\}, C=\{3\}$.

(d) True.

(e) True.



**E.x. 1.2.4. ** Produce an infinite collection of sets $A_1, A_2, A_3, \cdots$ with the property that every $A_i$ has an infinite number of elements, $A_i \cap A_j = \empty$ for all $i\ne j$, and $\cup_{i=1}^{\infty} A_i = \mathbb{N}$.

**Proof:** 

Partition $\mathbb{N}$ in a diagonal way as
$$
\begin{array}{ccccc}
1 & 3 & 6 & 10 & \dots \\
2 & 5 & 9 & \dots & \\
4 & 8 & \dots & & \\
7 & \dots & & &
\end{array}
$$
We may take $A_1$ as all numbers in the first row, $A_2$ on the second row, and so on. Then 
$$
\bigcup_{n=1}^{\infty} A_n = \mathbb{N}.
$$
Since each number is written only once, there is no intersection between two rows, i.e., $A_i \cap A_j = \empty$ for all $i\neq j$.



**E.x. 1.2.5 (De Morgan's Laws).** Let $A$ and $B$ be subsets of $\mathbb{R}$.

(a) if $x \in (A \cap B)^c$ , explain why $x\in A^c \cup B^c$. This shows that $(A \cap B)^{c} \subseteq A^{c} \cup B^{c}$.

(b) Prove the reverse inclusion $(A \cap B)^{c} \supseteq A^{c} \cup B^{c},$ and conclude that $(A \cap B)^{c}=A^{c} \cup B^{c}$.

(c) Show $(A \cup B)^{c}=A^{c} \cap B^{c}$ by demonstrating inclusion both ways.

**Proof:**

(a) If $x\in (A \cap B)^c$, then $x$ is neither in $A$ nor $B$, which exactly means $x\in A^c \cup B^c$ .

(b) Suppose $x\in A^c \cup B^c$, then either $x \in A^c$ or $x \in B^c$. Assume $x \notin (A \cap B)^{c}$, then $x$ must be both in $A$ and $B$, which is a contradiction. Thus, it must be the case that $x \in (A \cap B)^{c}$.

(c) 

(i) $(A \cup B)^{c} \subseteq A^{c} \cap B^{c}$

If $x \in (A \cup B)^{c}$, then $x$ cannot be in the union of $A$ and $B$, which means $x$ cannot be in $A$ nor $B$. Thus, $x \in A^c$ and $x \in B^c$, i.e., $x \in A^c \cap B^c$.

(ii) $(A \cup B)^{c} \supseteq A^{c} \cap B^{c}$

If $x \in A^c \cap B^c$, then $x \notin A$ and $x \notin B$, which means $x$ is neither in $A$ nor $B$, and hence, it is in the complementary $(A \cup B)^{c}$.



**E.x. 1.2.6** (a) Verify the triangle inequality in the special case where $a$ and $b$ have the same sign.
(b) Find an efficient proof for all the cases at once by first demonstrating $(a+b)^{2} \leq(|a|+|b|)^{2}$
(c) Prove $|a-b| \leq|a-c|+|c-d|+|d-b|$ for all $a, b, c,$ and $d$
(d) Prove $\| a|-| b|| \leq|a-b| .$ (The unremarkable identity $a=a-b+b$ may be useful.)

**Proof:**

(a) 

(i) $a\ge 0, b \ge 0$
$$
\vert a + b \vert = a + b = \vert a \vert + \vert b \vert.
$$
(ii) $a \le 0, b \le 0$
$$
\vert a + b \vert = -(a + b) = \vert a \vert + \vert b \vert.
$$
Thus, the triangle inequality is verified when $a$ and $b$ have the same sign.

(b) Use triangle inequality twice:
$$
\begin{align}
\vert a - b \vert &= \vert (a - c + c - d) + d - b \vert  \\
&\le \vert (a - c + c - d) \vert + \vert d - b \vert  \\
& \le \vert a - c \vert + \vert c - d \vert + \vert d - b \vert.
\end{align}
$$
(c) Since $a = a - b + b$, we have
$$
\vert a \vert = \vert a - b + b \vert \le \vert a - b\vert + \vert b \vert.
$$
Thus,
$$
\vert a \vert - \vert b \vert \le \vert a-b \vert.
$$
Similarly, use identity $b = b - a + a$ to get
$$
\begin{align}
\vert b \vert &\le \vert b - a \vert + \vert a \vert \\
\implies \vert a \vert - \vert b \vert &\ge - \vert a-b \vert.
\end{align}
$$
Therefore,
$$
\| a|-| b|| \leq|a-b|.
$$


**E.x. 1.2 .7** Given a function $f$ and a subset $A$ of its domain, let $f(A)$ represent the range of $f$ over the set $A ;$ that is, $f(A)=\{f(x): x \in A\}$
(a) Let $\left.f(x)=x^{2} . \text { If } A=[0,2] \text { (the closed interval }\{x \in \mathbf{R}: 0 \leq x \leq 2\}\right)$ and $B=[1,4],$ find $f(A)$ and $f(B) .$ Does $f(A \cap B)=f(A) \cap f(B)$ in this case? Does $f(A \cup B)=f(A) \cup f(B)$ ?
(b) Find two sets $A$ and $B$ for which $f(A \cap B) \neq f(A) \cap f(B)$
(c) Show that, for an arbitrary function $g: \mathbf{R} \rightarrow \mathbf{R},$ it is always true that $g(A \cap B) \subseteq g(A) \cap g(B)$ for all sets $A, B \subseteq \mathbf{R}$
(d) Form and prove a conjecture about the relationship between $g(A \cup B)$ and $g(A) \cup g(B)$ for an arbitrary function $g$

**Proof:** 

(a) $f(A)=[0, 4], f(B) = [1, 16], f(A \cap B) = [1, 4], f(A \cup B) = [0, 16]$

In this example, $f(A \cap B)=f(A) \cap f(B)$ and $f(A \cup B)=f(A) \cup f(B)$.

(b) Let $f(x) = x^2, A=[-1, 0), B = (0, 1]$, then $f(A \cap B) = \empty$ but $f(A) \cap f(B) = (0, 1]$.

(c) Suppose $y \in g(A \cap B)$, then there exists $x \in A \cap B$ such that $g(x) = y$. So $y \in g(A)$ and $y \in g(B)$, which exactly means $y \in g(A) \cap g(B)$ and hence the result holds.

(d) Conjecture: $g(A) \cup g(B) = g(A \cup B)$.

(i) $g(A) \cup g(B) \subseteq g(A \cup B)$: 

Let $y \in g(A) \cup g(B)$. Suppose $y \notin g(A)$, then $y$ must be in $g(B)$, so there exists $x \in B \subseteq A \cup B$ such that $g(x) = y$. It follows that $y \in g(A \cup B)$.

(ii) $g(A) \cup g(B) \supseteq g(A \cup B)$:

Let $y \in g(A \cup B)$, then there exists $x \in A \cup B$ such that $g(x) = y$. If $x \in A$, then $y \in g(A)$ and, if $x \notin A$, then $x$ must be in $B$, which implies $y \in g(B)$. In both cases, $y \in g(A) \cup g(B)$.



**Exercise 1.2.8.** Here are two important definitions related to a function $f:$ $A \rightarrow B .$ The function $f$ is one-to-one $(1-1)$ if $a_{1} \neq a_{2}$ in $A$ implies that $f\left(a_{1}\right) \neq$ $f\left(a_{2}\right)$ in $B .$ The function $f$ is onto if, given any $b \in B,$ it is possible to find an element $a \in A$ for which $f(a)=b$. Give an example of each or state that the request is impossible:
(a) $f: \mathbf{N} \rightarrow \mathbf{N}$ that is $1-1$ but not onto.
(b) $f: \mathbf{N} \rightarrow \mathbf{N}$ that is onto but not $1-1$
(c) $f: \mathbf{N} \rightarrow \mathbf{Z}$ that is $1-1$ and onto.

**Proof:**

(a) $f(n) = 2n$.

(b) $f(n) = \lceil \frac{n}{2} \rceil$.

(c) $f(n)=(-1)^n \lfloor \frac{n}{2} \rfloor$.



**Exercise 1.2.9.** Given a function $f: D \rightarrow \mathbf{R}$ and a subset $B \subseteq \mathbf{R},$ let $f^{-1}(B)$ be the set of all points from the domain $D$ that get mapped into $B ;$ that is, $f^{-1}(B)=\{x \in D: f(x) \in B\} .$ This set is called the preimage of $B$.

(a) Let $f(x) = x^2$. If $A$ is the closed interval [0, 4] and $B$ is the closed interval $[-1, 1]$, find $f^{-1}(A)$ and $f^{-1}(B)$. Does $f^{-1}(A \cap B)=f^{-1}(A) \cap f^{-1}(B)$ in this case? Does $f^{-1}(A \cup B)=f^{-1}(A) \cup f^{-1}(B)$?

(b) The good behavior of preimages demonstrated in (a) is completely general. Show that for an arbitrary function $g: \mathbf{R} \rightarrow \mathbf{R},$ it is always true that $g^{-1}(A \cap B)=g^{-1}(A) \cap g^{-1}(B)$ and $g^{-1}(A \cup B)=g^{-1}(A) \cup g^{-1}(B)$ for
all sets $A, B \subseteq \mathbf{R}$.

**Proof:**

(a) 

$f^{-1}(A)=[-2, 2]$ and $f^{-1}(B) = [-1, 1]$. In this example, 
$$
f^{-1}(A \cap B) = [-1, 1] = f^{-1}(A) \cap f^{-1}(B) \\
f^{-1}(A \cup B) = [-2, 2] = f^{-1}(A) \cup f^{-1}(B).
$$
(b) 

$g^{-1}(A \cap B)=g^{-1}(A) \cap g^{-1}(B)$:
$$
\begin{align}
x \in g^{-1}(A \cap B) &\iff g(x) \in A \cap B \\
&\iff g(x) \in A  \; \text{and} \; g(x) \in B \\
&\iff x \in g^{-1}(A) \; \text{and} \; x \in g^{-1}(B)\\
&\iff x \in g^{-1}(A) \cap g^{-1}(B).
\end{align}
$$
$g^{-1}(A \cup B)=g^{-1}(A) \cup g^{-1}(B)$:
$$
\begin{align}
x \in g^{-1}(A \cup B) &\iff g(x) \in A \cup B \\
&\iff  g(x) \in A  \; \text{or} \; g(x) \in B \\
&\iff x \in g^{-1}(A) \; \text{or} \; x \in g^{-1}(B)\\
&\iff x \in g^{-1}(A) \cup g^{-1}(B).
\end{align}
$$


**Exercise 1.2.10**. Decide which of the following are true statements. Provide a short justification for those that are valid and a counterexample for those that are not:
(a) Two real numbers satisfy $a<b$ if and only if $a<b+\epsilon$ for every $\epsilon>0$.
(b) Two real numbers satisfy $a<b$ if $a<b+\epsilon$ for every $\epsilon>0$.
(c) Two real numbers satisfy $a \leq b$ if and only if $a<b+\epsilon$ for every $\epsilon>0$.

**Proof:**

(a) and (b) are false, for a counterexample, consider $a=b=1$, then $a \lt b + \epsilon$ for every $\epsilon \gt 0$, but $a$ is not less than $b$.

(c) is true.

 ($\Longrightarrow$) : this direction is obvious.

($\Longleftarrow$): Assume the contrary that $a \gt b$, then if we take $\epsilon_0 = \frac{a-b}{2} \gt 0$, we will obtain
$$
a \gt \frac{a+b}{2} = b + (\frac{a-b}{2}) = b + \epsilon_0,
$$
which is  a contradiction and hence $a \le b$. 

**Note:** (c) is also true if "$a \lt b + \epsilon$" is changed to "$a\le b+\epsilon$ ".



**Exercise 1.2 .11.** Form the logical negation of each claim. One trivial way to do this is to simply add "It is not the case that..." in front of each assertion. To make this interesting, fashion the negation into a positive statement that avoids using the word "not" altogether. In each case, make an intuitive guess as to whether the claim or its negation is the true statement.
(a) For all real numbers satisfying $a<b,$ there exists an $n \in \mathbf{N}$ such that $a+1 / n<b$
(b) There exists a real number $x>0$ such that $x<1 / n$ for all $n \in \mathbf{N}$
(c) Between every two distinct real numbers there is a rational number.

**Proof:**

(a) 

negation: There exist two real numbers $a$ and $b$ satisfying $a \lt b$, but $a + 1/n \ge b$ for all $n \in \mathbf{N}$.

The origin claim is true.

(b)

negation: For every real number $x \gt 0$, there exists $n \in \mathbf{N}$ such that $x \ge 1/n$.

The negation of the origin claim is true.

(c)

negation: There are two distinct real numbers which has no rational number between them.

The origin claim is true.



**Exercise 1.2 .12.** Let $y_{1}=6,$ and for each $n \in \mathbf{N}$ define $y_{n+1}=\left(2 y_{n}-6\right) / 3$
(a) Use induction to prove that the sequence satisfies $y_{n}>-6$ for all $n \in \mathbf{N}$
(b) Use another induction argument to show the sequence $\left(y_{1}, y_{2}, y_{3}, \ldots\right)$ is decreasing.

**Proof:**

(a) Base case $n = 1$: $y_1 = 6 \gt -6$.

Inductive step: assume $y_n \gt -6$ is true, we need to show $y_{n+1} \gt -6$. By the recurrence formula
$$
y_{n+1} = \frac{2y_n - 6}{3} \gt \frac{2 \cdot (-6) - 6}{3} = -6.
$$
By induction, the claim is true for all $n \in \mathbf{N}$.

(b) Base case $n=1$: $y_2=2 \lt y_1$.

Inductive step: assume $y_n \gt y_{n+1}$ is true, then by the recurrence formula
$$
y_{n+2} = \frac{(2y_{n+1}-6)}{3} \lt \frac{(2y_{n}-6)}{3}=y_{n+1}.
$$
By induction, the claim is true for all $n \in \mathbf{N}$ and hence the sequence $\left(y_{1}, y_{2}, y_{3}, \ldots\right)$ is decreasing.



**Exercise 1.2.13.** For this exercise, assume Exercise 1.2.5 has been successfully completed.
(a) Show how induction can be used to conclude that
$$
\left(A_{1} \cup A_{2} \cup \cdots \cup A_{n}\right)^{c}=A_{1}^{c} \cap A_{2}^{c} \cap \cdots \cap A_{n}^{c}
$$
for any finite $n \in \mathbf{N}$
(b) It is tempting to appeal to induction to conclude
$$
\left(\bigcup_{i=1}^{\infty} A_{i}\right)^{c}=\bigcap_{i=1}^{\infty} A_{i}^{c}
$$
but induction does not apply here. Induction is used to prove that a particular statement holds for every value of $n \in \mathbf{N},$ but this does not imply the validity of the infinite case. To illustrate this point, find an example of a collection of sets $B_{1}, B_{2}, B_{3}, \ldots$ where $\bigcap_{i=1}^{n} B_{i} \neq \emptyset$ is true for every $n \in \mathbf{N},$ but $\bigcap_{i=1}^{\infty} B_{i} \neq \emptyset$ fails.

(c) Nevertheless, the infinite version of De Morgan’s Law stated in (b) is a

valid statement. Provide a proof that does not use induction.

**Proof:**

(a) Base case $n=1$: obvious.

Inductive step: assume $\left(A_{1} \cup A_{2} \cup \cdots \cup A_{n}\right)^{c}=A_{1}^{c} \cap A_{2}^{c} \cap \cdots \cap A_{n}^{c}$ holds. By Exercise 1.2.5
$$
\begin{align}
\left(A_{1} \cup A_{2} \cup \cdots \cup A_{n+1}\right)^{c} 
&= \left((A_{1} \cup A_{2} \cup \cdots \cup A_{n}) \cup A_{n+1}\right)^{c} \\
&=\left(A_{1} \cup A_{2} \cup \cdots \cup A_{n}\right)^{c} \cap A_{n+1}^c \\
&= A_{1}^{c} \cap A_{2}^{c} \cap \cdots \cap A_{n}^{c} \cap A_{n+1}^c.
\end{align}
$$
By induction, the claim is true for all $n \in \mathbf{N}$.

(b) Let $B_i = (1, 1+\frac{1}{i})$ , then 
$$
\bigcap_{i=1}^n B_i = (1, 1 + \frac{1}{n}) \neq \empty \quad \forall \; n \in \mathbf{N}, \\
\bigcap_{i=1}^{\infty}B_i = \empty.
$$
(c)
$$
\begin{align}
x \in \left(\bigcup_{i=1}^{\infty} A_{i}\right)^{c} 
&\iff x \notin \bigcup_{i=1}^{\infty} A_{i} \\
&\iff x \notin A_i \; \forall i \in \mathbf{N} \\
&\iff x \in A_i^c \; \forall i \in \mathbf{N} \\
&\iff x \in \bigcap_{i=1}^{\infty}A_i^c.
\end{align}
$$

## Exercises of 1.3 The Axiom of Completeness

**Exercise 1.3.1.** (a) Write a formal definition in the style of Definition 1.3.2 for the infimum or greatest lower bound of a set.

(b) Now, state and prove a version of Lemma 1.3.8 for greatest lower bounds.

**Proof:**

(a) **Def**. A real number $l$ is the greatest lower bound for a set $A \subseteq \mathbf{R}$ if it meets the following two criteria:

(i) $l$ is a lower bound for $A$;

(ii) if $b$ is a lower bound for $A$, then $ l \ge b$.

(b) **Lemma**. Assume $l \in \mathbf{R}$ is a lower bound for a set $A \subseteq \mathbf{R}$. Then, $l=\inf A$ if and only if, for every choice of $\epsilon \gt 0$, there exists an element $a \in A$ satisfying $a \lt l + \epsilon$.

($\Longrightarrow$) Suppose $l=\inf A$ and given $\epsilon \gt 0$, then $l + \epsilon \gt l$ is not a lower bound for $A$. Thus, there exists  an element $a \in A$ satisfying $a \lt l + \epsilon$.

($\Longleftarrow$) Assume $l$ is an upper bound with the property that no matter how $\epsilon \gt 0$ is chosen, $l + \epsilon$ is no longer a lower bound for $A$. This implies that if $b$ is any number greater than $l$, then $b$ is not a lower bound. Thus, if $b$ is a lower bound for $A$, then $l \ge b$ and hence $l = \inf A$.



**Exercise 1.3.2.** Give an example of each of the following, or state that the request is impossible.
(a) A set $B$ with $\inf B \geq \sup B$
(b) A finite set that contains its infimum but not its supremum.
(c) A bounded subset of $\mathbf{Q}$ that contains its supremum but not its infimum.

**Proof:**

(a) Take $B = \{1\}$, then $\inf B = \sup B = 1$. Therefore $\inf B \geq \sup B$.

(b) Impossible. Because every finite set has maximum and minimum element and they are supremum and infimum respectively in this case.

(c) Take
$$
A = \{x \in \mathbf{Q}: \sqrt{2} \lt x \le 2\},
$$
then $\sup A = 2 \in A$ but $\inf A = \sqrt{2} \notin A$.



**Exercise 1.3.3.** (a) Let $A$ be nonempty and bounded below, and define $B=$ $\{b \in \mathbf{R}: b \text { is a lower bound for } A\} .$ Show that $\sup B=\inf A$
(b) Use (a) to explain why there is no need to assert that greatest lower bounds exist as part of the Axiom of Completeness.

**Proof:**

(a) $B$ is non-empty and bounded above since every element in $A$ is a upper bound for $B$. Thus, $\sup B$ exists. Write $s = \sup B$.

If $s$ is not a lower bound for $A$, then there exists $x\in A$ such that $x \lt s$. Let $\epsilon_0 = \frac{s - x}{2} \gt 0$, then there exists $b \in B$ such that
$$
b \gt s - \epsilon_0 = \frac{s+x}{2} \gt x,
$$
which implies $b$ is not a lower bound for $A$, a contradiction. Thus, $s$ must be a lower bound for $A$.

To show $s$ is the greatest lower bound for $A$, let $l$ be a lower bound for $A$, then  $l \in B$, which implies
$$
l \le s
$$
since $s$ is an upper bound for $B$. Therefore, $s$ is the greatest lower bound for $A$, i.e., $\inf A$ exists and 
$$
\inf A = \sup B.
$$
(b) From (a) we see that if $A$ is bounded below then the greatest lower bound exists which is equivalent to axiom of completeness.



**Exercise 1.3.4.**  Let $A_1, A_2, A_3, \cdots$  be a collection of nonempty sets, each of which is bounded above.

(a) Find a formula for $\sup \left(A_{1} \cup A_{2}\right) .$ Extend this to $\sup \left(\bigcup_{k=1}^{n} A_{k}\right)$
(b) Consider $\sup \left(\bigcup_{k=1}^{\infty} A_{k}\right) .$ Does the formula in (a) extend to the infinite case?

**Proof:** 

(a) For any $n \in \mathbf{N}$, if $A_1, A_2, \cdots, A_n$ are nonempty bounded sets then
$$
\sup \left(A_{1} \cup A_{2} \cup \ldots \cup A_{n}\right)=\max \left\{\sup A_{1}, \ldots, \sup A_{n}\right\}.
$$
We use induction to show this. For $n = 1$, this holds trivially. Let $A_1, A_2$ be nonempty bounded sets, we will show
$$
\sup(A_1 \cup A_2) = \max \{\sup A_1, \sup A_2\}.
$$
Since $A_1$ and $A_2$ are bounded above, for all $x \in A_1$, $x \le a_1$ for some $a_1$ and for all $y \in A_2$, $y \le a_2$ for some $a_2$. This shows for all $z \in A_1 \cup A_2$, $z \le \max\{a_1, a_2\}$ so $A_1 \cup A_2$ is bounded above hence the supremum exists.

Without loss of generality, assume $\sup A_1 \le \sup A_2$. Since $A_2 \subseteq A_1 \cup A_2$, we have $\sup A_2 \le \sup(A_1 \cup A_2)$. Let $z \in A_1 \cup A_2$.

Then either $z \in A_1$ or $z \in A_2$ or both. In any case, we get $z \le \sup A_2$ hence $\sup A_2$ is an upper bound for $A_1 \cup A_2$. By the definition of supremum, $\sup (A_1 \cup A_2) \le \sup A_2$ with which gives
$$
\sup \left(A_{1} \cup A_{2}\right)=\sup A_{2}.
$$
Therefore,
$$
\sup(A_1 \cup A_2) = \max \{\sup A_1, \sup A_2\}
$$
holds.

To extend this result, assume
$$
\sup \left(A_{1} \cup A_{2} \cup \ldots \cup A_{n}\right)=\max \left\{\sup A_{1}, \ldots, \sup A_{n}\right\}
$$
is true, then for $n + 1$, we have
$$
\begin{align}
\sup(A_1 \cup A_2 \cup \cdots \cup A_n \cup A_{n+1}) 
&= \sup((A_1 \cup A_2 \cup \cdots \cup A_n )\cup A_{n+1})  \\
&= \max\{\sup(A_1 \cup A_2 \cup \cdots \cup A_n ), \sup A_{n+1}\} \\
&=\max\{\max\{A_1, \cdots, A_n\}, A_{n+1}\} \\
&= \max\{A_1, A_2, \cdots, A_{n+1}\}.

\end{align}
$$
Hence this is true for all $n \in \mathbf{N}$.

(b) This formula does not extend to the infinite case. Consider $A_n=\{n\}$, then each $A_n$ is nonempty and bounded above, however $\bigcup_{n=1}^{\infty}A_n$ is not bounded above and hence does not have a least upper bound. Meanwhile, $\max\{1, 2, 3, \cdots\}$ does not exist either.



**Exercise 1.3.5.** As in Example $1.3 .7,$ let $A \subseteq \mathbf{R}$ be nonempty and bounded above, and let $c \in \mathbf{R} .$ This time define the set $c A=\{c a: a \in A\}$
(a) If $c \geq 0,$ show that $\sup (c A)=c \sup A$
(b) Postulate a similar type of statement for sup $(c A)$ for the case $c<0$

**Proof:**

(a) 

If $c = 0$, then $\sup(cA) = 0 =c \sup A$. 

Now assume $c \gt 0$. Since $A$ is nonempty and bounded above, there exists $M \in \mathbf{R}$ such that $a \le M$ for all $a \in A$. Because $c \gt 0$, the set $cA$ is nonempty and bounded above and hence $\sup (cA)$ exists. Write $s = \sup A$, then
$$
ca \le cs,
$$
for every $a \in A$, which implies $cs$ is an upper bound for $cA$. 

Now let $\epsilon \gt 0$, then there exists some $a_0 \in A$ such that
$$
a_0 \gt s - \frac{\epsilon}{c},
$$
which implies
$$
ca_0 \gt cs - \epsilon.
$$
Therefore, $cs=c \sup A$ is the least upper bound of the set $cA$.

(b)

**Proposition **. If $c \lt 0$ and $A$ is non-empty and bounded from below, then $\sup (cA) = c\inf A$.

**Proof of the Proposition**: Since $c$ is negative and $A$ is bounded below,  $cA$ is bounded above and hence $\sup (cA)$ exists. Write $l= \inf A$, then 
$$
l \le a 
$$
for every $a \in A$, which implies
$$
cl \ge ca.
$$
 Thus, $cl$ is an upper bound of the set $cA$.

Now let $\epsilon \gt 0$ be given, then there exists some $a_0 \in A$ such that
$$
a_0 \lt l + \left(\frac{\epsilon}{-c}\right),
$$
then 
$$
ca_0 \gt cl -\epsilon.
$$
Therefore, $cl = c\inf A$ is the least upper bound of the set $cA$.



**Exercise 1.3.6.** Given sets $A$ and $B,$ define $A+B=\{a+b: a \in A \text { and } b \in B\}$ Follow these steps to prove that if $A$ and $B$ are nonempty and bounded above $\operatorname{then} \sup (A+B)=\sup A+\sup B$
(a) Let $s=\sup A$ and $t=\sup B .$ Show $s+t$ is an upper bound for $A+B$
(b) Now let $u$ be an arbitrary upper bound for $A+B,$ and temporarily fix $a \in A .$ Show $t \leq u-a$
(c) Finally, show $\sup (A+B)=s+t$
(d) Construct another proof of this same fact using Lemma 1.3.8

**Proof:**

(a) Since $A$ and $B$ are bounded above, there exist $M_1$ and $M_2$ such that
$$
a \le M_1\\
b \le M_2,
$$
for every $a \in A$ and $b \in B$. Thus,
$$
a + b \le M_1 + M_2
$$
and hence $A+B$ is bounded above.

(b) Since $u$ is an upper bound for $A+B$ and $a\in A$ is fixed, we have
$$
a + b \le u
$$
for every $b\in B$. It follows that $b \le u - a$, which implies $u - a$ is an upper bound for set $B$ and hence $t \le u - a$.

(c) By (b) 
$$
a \le u - t,
$$
for every $a \in A$, which means $u-t$ is an upper bound for set $A$, and hence
$$
s \le u - t,
$$
i.e., $s + t \le u$. Therefore, $\sup (A + B) = s + t$.

(d) Let $\epsilon \gt 0$ be given, then there exists $a_0\in A$ and $b_0 \in B$ such that 
$$
a_0 \gt s - \frac{\epsilon}{2}  \\
b_0 \gt t - \frac{\epsilon}{2},
$$
then 
$$
a_0 + b_0 \gt s + t - \epsilon.
$$
Therefore, by Lemma 1.3.8 $\sup (A+B)=s+t$ holds.



**Exercise 1.3.7.** Prove that if $a$ is an upper bound for $A,$ and if $a$ is also an element of $A,$ then it must be that $a=\sup A$.

**Proof:**

Since $a$ is an upper bound for $A$, $a \ge \sup A$. Moreover, $a$ is also an element of $A$ implies $a \le \sup A$ since $\sup A$ is an upper bound for $A$. Therefore, $a = \sup A$.



**Exercise 1.3.8.** Compute, without proofs, the suprema and infima (if they exist $)$ of the following sets:
(a) $\{m / n: m, n \in \mathbf{N} \text { with } m<n\}$
(b) $\left\{(-1)^{m} / n: m, n \in \mathbf{N}\right\}$
(c) $\{n /(3 n+1): n \in \mathbf{N}\}$
(d) $\{m /(m+n): m, n \in \mathbf{N}\}$

**Proof:**

(a) $\sup A=1, \inf A =0$  

(b) $\sup A=1, \inf A= -1$

(c) $\sup A=1/3, \inf A= 1/4$

(d) $\sup A=1, \inf A=0$



**Exercise 1.3 .9**
(a) If $\sup A<\sup B,$ show that there exists an element $b \in B$ that is an upper bound for $A$.
(b) Give an example to show that this is not always the case if we only assume
$\sup A \leq \sup B$.

**Proof:**

(a) Define $\epsilon_0 = \frac{\sup B - \sup A}{2} \gt 0$, then there exists $b \in B$ such that 
$$
b \gt \sup B - \epsilon_0=\frac{\sup B + \sup A}{2} \gt \sup A,
$$
so $b$ is an upper bound for $A$.

(b)  Let $A = [0, 1], B = [0, 1)$, then $\sup A = \sup B = 1$ but there is no element in $B$ which is an upper bound for $A$.



**Exercise 1.3.10 (Cut Property).** The Cut Property of the real numbers is the following:

If $A$ and $B$ are nonempty, disjoint sets with $A \cup B=\mathbf{R}$ and $a<b$ for all $a \in A$ and $b \in B,$ then there exists $c \in \mathbf{R}$ such that $x \leq c$ whenever $x \in A$ and
$x \geq c$ whenever $x \in B$
(a) Use the Axiom of Completeness to prove the Cut Property.

(b) Show that the implication goes the other way; that is, assume $\mathbf{R}$ possesses the Cut Property and let $E$ be a nonempty set that is bounded above. Prove sup $E$ exists.

(c) The punchline of parts (a) and (b) is that the Cut Property could be used in place of the Axiom of Completeness as the fundamental axiom that distinguishes the real numbers from the rational numbers. To drive this point home, give a concrete example showing that the Cut Property is not a valid statement when $\mathbf{R}$ is replaced by $\mathbf{Q}$.

**Proof:**

(a) Since $a \lt b$ for all $a \in A$ and $b \in B$, $A$ is bounded above and hence $\sup A$ exists. Let $c = \sup A$, then 
$$
x \le c,
$$
for all $x \in A$, and 
$$
c \le x,
$$
for all $x \in B$ since every element in $B$  is an upper bound for $A$ and $c$ is the least upper bound. Therefore, $c=\sup A$ satisfies the requirement.

Note: $\inf B$ also exists and $\inf B = \sup A=c$.

(b) Define $B=\{x\in \mathbf{R}: x \; \text{is an upper bound for} \; E \}$ and $A = \mathbf{R} - B$, then $A$ and $B$ are non-empty disjoint sets with $A \cup B= \mathbf{R}$. 

To see $a \lt b$ for every $a \in A$ and every $b \in B$, notice that if $a \in A$, then $a$ is not an upper bound for $E$, which means there exists $e \in E$ such that $e \gt a$. However, $b \in B$ is an upper bound for $E$, i.e., 
$$
b \ge e \gt a.
$$
Next, we show $c$ is an upper bound for $E$. By the cut property, there exists $c \in \mathbf{R}$ such that $x \le c$ for every $x \in A$ and $c \le x$ for every $x \in B$, so $c$ is an upper bound for $A$ and lower bound for $B$. Then, $c$ must be an upper bound for $E$, because if there were $e \in E$ with $e \gt c$, then $\frac{e+c}{2}$ cannot be in $B$ since it's less than $e$ so it must be in $A$, but this contradicts the fact that $c$ is an upper bound for $A$.

Finally, suppose $u$ is an upper bound for $E$, then $u \in B$ and hence 
$$
c \le u
$$
holds. Therefore, $c$ is the least upper bound for $E$.  

(c) Consider $A = \{x \in \mathbf{Q}: x \lt \sqrt{2} \}$ and $B = \{x \in \mathbf{Q}: x \gt \sqrt{2} \}$, then $A$ and $B$ are nonempty and disjoint with  $A \cup B = \mathbf{\mathbf{Q}}$. However, there is no rational number $q$ such that $x \le q$ if $x \in A$ and $x \ge q$ if $x \in B$. To see this, suppose it were to exist, then either $q \lt \sqrt{2}$ or $q \gt \sqrt{2}$. Suppose $q \lt \sqrt{2}$, then there exists another rational number $r$ between $q$ and $\sqrt{2}$, so $r \in A$ and $q \lt r$ which contradicts $x \le q$ for every $x \in A$. Similarly,  $q \gt \sqrt{2}$ also reaches a contradiction.



**Exercise 1.3.11.** Decide if the following statements about suprema and infima are true or false. Give a short proof for those that are true. For any that are false, supply an example where the claim in question does not appear to hold.
(a) If $A$ and $B$ are nonempty, bounded, and satisfy $A \subseteq B,$ then $\sup A \leq$ $\sup B$
(b) If $\sup A<\inf B$ for sets $A$ and $B,$ then there exists a $c \in \mathbf{R}$ satisfying $a<c<b$ for all $a \in A$ and $b \in B$
(c) If there exists a $c \in \mathbf{R}$ satisfying $a<c<b$ for all $a \in A$ and $b \in B,$ then $\sup A<\inf B$.

**Proof:**

(a) True. Let $s =\sup A$ and $t = \sup B$, then $t$ is an upper bound for $A$ since $A \subseteq B$, hence $s \le t$.

(b) True. Let  $c = \frac{\sup A + \inf B}{2} $ , then
$$
\sup A \lt c \lt \inf B.
$$
Hence, 
$$
a \le \sup A \lt c \lt \inf B \le b,
$$
for every $a \in A$ and $b \in B$.

(c) False. Take $A = \{x \in \mathbf{R}: x \lt \sqrt{2}\}$ and $B = \{x \in \mathbf{R}: x \gt \sqrt{2}\}$, then 
$$
a \lt \sqrt{2} \lt b,
$$
for all $a \in A$ and $b \in B$. However, $\sup A = \inf B = \sqrt{2}$.



## Exercises of 1.4 Consequences of Completeness

**Exercise 1.4.1.** Recall that $\mathbf{I}$ stands for the set of irrational numbers.
(a) Show that if $a, b \in \mathbf{Q},$ then $a b$ and $a+b$ are elements of $\mathbf{Q}$ as well.
(b) Show that if $a \in \mathbf{Q}$ and $t \in \mathbf{I},$ then $a+t \in \mathbf{I}$ and $a t \in \mathbf{I}$ as long as $a \neq 0$
(c) Part (a) can be summarized by saying that $\mathbf{Q}$ is closed under addition and multiplication. Is $\mathbf{I}$ closed under addition and multiplication? Given two irrational numbers $s$ and $t,$ what can we say about $s+t$ and $s t$?

**Proof:**

(a) Since $a, b \in \mathbf{Q}$, they can be written as
$$
a = \frac{m}{n}, b = \frac{q}{p},
$$
then 
$$
a b = \frac{mq}{np}, a + b = \frac{pm + qn}{np},
$$
so $ab$ and $a + b$ both are elements of $\mathbf{Q}$.

(b) If $a + t \notin \mathbf{I}$  , then $a + t$ is a rational number and hence
$$
t = (a + t) + (-a) \in \mathbf{Q}
$$
by (a), which is a contradiction. Similarly, $a t \in \mathbf{I}$ as long as $a \neq 0$.

(c) $\mathbf{I}$ is not closed under addition and multiplication, for example, $\sqrt{2} + (-\sqrt{2})=0$, $0 \cdot \sqrt{2} = 0$. Given two irrational numbers, their sum and product are not necessarily irrational.



**Exercise 1.4.2.** Let $A \subseteq \mathbf{R}$ be nonempty and bounded above, and let $s \in \mathbf{R}$ have the property that for all $n \in \mathbf{N}, s+\frac{1}{n}$ is an upper bound for $A$ and $s-\frac{1}{n}$ is not an upper bound for $A .$ Show $s=\sup A$.

**Proof:**

First, we show $s$ must be an upper bound for $A$. Assume the contrary that $s$ is not an upper bound for $A$, then $\exists a_0 \in A$ such that
$$
a_0 \gt s.
$$
We can choose $n_0$ large enough such that
$$
\frac{1}{n_0} \lt a_0 - s.
$$
Then since $s + \frac{1}{n_0}$ is an upper bound for $A$, it follows that
$$
a_0 \le s + \frac{1}{n_0} \lt s + a_0 -s = a_0,
$$
which is a contradiction, so $s$ is an upper bound for $A$.

Next, to show $s$ is the least upper bound for $A$, let $\epsilon \gt 0$ be given. Then $\exists n^\prime \in \mathbf{N}$ such that 
$$
\frac{1}{n^\prime} \lt \epsilon,
$$
then 
$$
s - \epsilon \lt s - \frac{1}{n^\prime} \lt s.
$$
By assumption, $s - \frac{1}{n^\prime}$ is not an upper bound for $A$, so $s - \epsilon$, which is even smaller, cannot be an upper bound for $A$ either. 

Theirfore, $s = \sup A$ as desired.



**Exercise 1.4.3.** Prove that $\bigcap_{n=1}^{\infty}(0,1 / n)=\emptyset .$ Notice that this demonstrates that the intervals in the Nested Interval Property must be closed for the conclusion of the theorem to hold.

**Proof:**

Suppose $\bigcap_{n=1}^{\infty}(0,1 / n)\neq \emptyset$, then there is some number $a \in \bigcap_{n=1}^{\infty}(0,1 / n)$. It follows that
$$
0 \lt a \lt \frac{1}{n},
$$
for every $n \in \mathbf{N}$. This contradicts the Archemedean Property and hence the set must be empty.



**Exercise 1.4.4.** Let $a<b$ be real numbers and consider the set $T=\mathbf{Q} \cap[a, b]$ Show sup $T=b$.

**Proof:**

First, it is obvious that $T$ is non-empty and bounded above and hence $\sup T$ exists. Since $T$ contains all rational numbers between $a$ and $b$,  $b$ is an upper bound for $T$. 

Now let $\epsilon \gt 0$ be given, then by Density of $\mathbf{Q}$ in $\mathbf{R}$, there is some rational number $q$ in between $b - \epsilon$ and $b$. So $q \in T$ and $q \lt b$, which means $b$ is the least upper bound for $T$.



**Exercise 1.4.5.** Using Exercise 1.4.1, supply a proof for Corollary $1.4 .4 \mathrm{by}$ considering the real numbers $a-\sqrt{2}$ and $b-\sqrt{2}$.

**Proof:**

By Density of $\mathbf{Q}$ in $\mathbf{R}$, there is some rational number $r$ such that
$$
a - \sqrt{2} \lt r \lt b - \sqrt{2}.
$$
Then by Exercise 1.4.1, $r + \sqrt{2}$ is a irrational number which lies between $a$ and $b$.



**Exercise 1.4.6.** Recall that a set $B$ is dense in $\mathbf{R}$ if an element of $B$ can be found between any two real numbers $a<b .$ Which of the following sets are dense in $\mathbf{R} ?$ Take $p \in \mathbf{Z}$ and $q \in \mathbf{N}$ in every case.
(a) The set of all rational numbers $p / q$ with $q \leq 10$
(b) The set of all rational numbers $p / q$ with $q$ a power of 2
(c) The set of all rational numbers $p / q$ with $10|p| \geq q$

**Proof:**

(a) No. Take $a = \frac{1}{100}$ and $b = \frac{2}{100}$.

(b) Yes. Let $a \lt b$ and take $n$ such that $b - a \gt \frac{1}{2^n}$, then
$$
2^n b - 2^n a \gt 1.
$$
So there exists an integer $s$ such that
$$
2^n a \lt s \lt s^n b.
$$
Hence we get 
$$
a \lt \frac{s}{2^n} \lt b.
$$
This shows the set given is dense in $\mathbf{R}$.

(c) No. Given $10 \vert p \vert \ge q$, we have
$$
\frac{p}{q} \ge \frac{1}{10} \; \text{or} \; \frac{p}{q} \le -\frac{1}{10}.
$$
So take $a = -\frac{1}{100}$ and $b = \frac{1}{100}$ , then there exists no $p/q$ in the given set which is also between $a$ and $b$.



**Exercise 1.4 .7.** Finish the proof of Theorem 1.4 .5 by showing that the assumption $\alpha^{2}>2$ leads to a contradiction of the fact that $\alpha=\sup T$.

**Proof:**

Write 
$$
\begin{aligned}\left(\alpha-\frac{1}{n}\right)^{2} &=\alpha^{2}-\frac{2 \alpha}{n}+\frac{1}{n^{2}} \\ &>\alpha^{2}-\frac{2 \alpha}{n}.
\end{aligned}
$$
Since $\alpha^2 \gt 2$,  we can choose $n_0$ large enough such that
$$
\alpha^2 - \frac{2 \alpha}{n_0} \gt 2.
$$
This implies $\alpha -\frac{1}{n_0}$ is an upper bound for $T$, which contradicts the fact that $\alpha$ is the least upper bound for $T$.



**Exercise 1.4.8.** Give an example of each or state that the request is impossible. When a request is impossible, provide a compelling argument for why this is the case.
(a) $\mathrm{Two}$ sets $A$ and $B$ with $A \cap B=\emptyset, \sup A=\sup B, \sup A \notin A$ and
$\sup B \notin B$
(b) A sequence of nested open intervals $J_{1} \supseteq J_{2} \supseteq J_{3} \supseteq \cdots$ with $\bigcap_{n=1}^{\infty} J_{n}$ nonempty but containing only a finite number of elements.
(c) A sequence of nested unbounded closed intervals $L_{1} \supseteq L_{2} \supseteq L_{3} \supseteq \cdots$ with $\bigcap_{n=1}^{\infty} L_{n}=\emptyset .$ (An unbounded closed interval has the form $[a, \infty)=$ $\{x \in R: x \geq a\} .)$
(d) A sequence of closed (not necessarily nested) intervals $I_{1}, I_{2}, I_{3}, \ldots$ with the property that $\bigcap_{n=1}^{N} I_{n} \neq \emptyset$ for all $N \in \mathbf{N},$ but $\bigcap_{n=1}^{\infty} I_{n}=\emptyset$

**Proof:**

(a) Possible. Take $A = (0, 1) \cap \mathbf{Q}$ and $B = (0, 1) \cap \mathbf{Q}^C$. Then $A \cap B=\empty$ , $\sup A =\sup B = 1$, and $\sup A \notin A$ and $\sup B \notin B$.

(b) Possible. Take $J_n = (-\frac{1}{n}, \frac{1}{n})$, then $J_1 \supseteq J_2 \supseteq \cdots$ with $\cap_{n=1}^{\infty} J_n = \{0\}$.

(c) Possible. Take $L_n = [n, \infty]$, then $L_{1} \supseteq L_{2} \supseteq L_{3} \supseteq \cdots$ and $\bigcap_{n=1}^{\infty} L_{n}=\emptyset .$

(d) Impossible. If $\cap_{n=1}^{\infty}I_n = \empty$, then consider $A_N = \cap_{n=1}^N I_n$, for $N \in \mathbf{N}$, which form a non-empty nested closed intervals. By Nested Interval Property, $\cap_{N=1}^{\infty}A_N \neq \empty$, but
$$
\bigcap_{n=1}^{\infty} I_n = \bigcap_{N=1}^{\infty} A_N,
$$
since $\cap_{N=1}^M A_N = A_M = \cap_{n=1}^M I_n$ for all $M$.  So
$$
\bigcap_{n=1}^{\infty} I_n \neq \empty,
$$
which is a contradition.