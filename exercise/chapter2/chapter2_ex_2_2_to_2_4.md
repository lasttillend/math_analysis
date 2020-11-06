# Chapter 2 Exercise

## Exercises of 2.2 The Limit of a Sequence

> **Exercise 2.2.1.** What happens if we reverse the order of the quantifiers in Definition 2.2.3 ?
>
> Definition: A sequence $\left(x_{n}\right)$ verconges to $x$ if there exists an $\epsilon>0$ such that for all $N \in \mathbf{N}$ it is true that $n \geq N$ implies $\left|x_{n}-x\right|<\epsilon$
>
> Give an example of a vercongent sequence. Is there an example of a vercongent sequence that is divergent? Can a sequence verconge to two different values? What exactly is being described in this strange definition?

**Proof.**

"Vercongent" is equivalent to "bounded".

If $(x_n)$ is bounded, then there exists some $M \gt 0$ such that $\vert x_n \vert \lt M$ for all $n \in \mathbf{N}$. Hence, the sequence vercongers to 0. Moreover, it vercongers to any real number $x$, as $\vert x_n - x \vert \le \vert x_n \vert + \vert x \vert \lt M + \vert x \vert$ for any $n \in \mathbf{N}$.

If $(x_n)$ vercongers to $x$ and let $\epsilon \gt 0$ be the constant of vercongence. Let $N=1$ in the definition of vercongence, one has that for any $n \in \mathbf{N}$,
$$
\vert x_n \vert \le \vert x_n - x \vert + \vert x \vert \lt \epsilon + \vert x \vert.
$$
Hence, $(x_n)$ is bounded.



> **Exercise 2.2.2.** Verify, using the definition of convergence of a sequence, that the following sequences converge to the proposed limit.
> (a) $\lim \frac{2 n+1}{5 n+4}=\frac{2}{5}$
> (b) $\lim \frac{2 n^{2}}{n^{3}+3}=0$
> (c) $\lim \frac{\sin \left(n^{2}\right)}{\sqrt[3]{n}}=0$

**Proof.**

(a) Let $\epsilon \gt 0$ be given. Choose $N \in \mathbf{N}$ such that $N \gt \frac{3}{25\epsilon}$ , then for any $n \ge N$,
$$
\left\vert \frac{2n+1}{5n+4} - \frac{2}{5} \right\vert = \frac{3}{5(5n+4)} \lt \frac{3}{5 \cdot 5n} \lt \epsilon.
$$
(b) Let $\epsilon \gt 0$ be given. Choose $N \in \mathbf{N}$ such that $N \gt \frac{2}{\epsilon}$, then for any $n \ge N$,
$$
\left\vert \frac{2n^2}{n^3+3} - 0 \right\vert = \frac{2n^2}{n^3+3} \lt \frac{2n^2}{n^3} = \frac{2}{n} \lt \epsilon.
$$
(c) Let $\epsilon \gt 0$ be given. Choose $N \in \mathbf{N}$ such that $N \gt \frac{1}{\epsilon^3}$, then for any $n \ge N$,
$$
\left\vert \frac{\sin(n^2)}{\sqrt[3]{n}} - 0 \right\vert = \frac{\vert\sin(n^2) \vert}{\sqrt[3]{n}} \lt \frac{1}{\sqrt[3]{n}} \lt \epsilon.
$$


> **Exercise 2.2.3.** Describe what we would have to demonstrate in order to disprove each of the following statements.
> (a) At every college in the United States, there is a student who is at least seven feet tall.
> (b) For all colleges in the United States, there exists a professor who gives every student a grade of either $\mathrm{A}$ or $\mathrm{B}$.
> (c) There exists a college in the United States where every student is at least six feet tall.

**Sol.**

(a) Find a college in the United States where every student is shorter than seven feet.

(b) Find a college in the United States where every professor gives some students a grade which is neither A nor B.

(c) Show that in every college in the United States we can find at least one student whose height is less than six feet.



> **Exercise 2.2.4.** Give an example of each or state that the request is impossible. For any that are impossible, give a compelling argument for why that is the case.
> (a) A sequence with an infinite number of ones that does not converge to one.
>
> (b) A sequence with an infinite number of ones that converges to a limit not equal to one.
> (c) A divergent sequence such that for every $n \in \mathbf{N}$ it is possible to find $n$ consecutive ones somewhere in the sequence.

**Proof.**

(a) $x_n=(-1)^n, n \in \mathbf{N}$.

(b) Impossible. Suppose $x_n$ converges to $L \neq 1$. Then for $\epsilon_0 =  \vert L - 1 \vert \gt 0$, there exists $N \in \mathbf{N}$ such that $n \ge N$ implies 
$$
\vert x_n - L\vert \lt \epsilon_0 = \vert L - 1 \vert.
$$
However, since there are infinitely many ones in $x_n$, there must be some $n_0 \ge N$ such that $x_{n_0} = 1$, which is a contradiction.

(c) Define $x_n =1$ if $n$ is not a perfect square, and $x_n = n$ if $n$ is a perfect square.



> **Exercise 2.2.5.** Let $[[x]]$ be the greatest integer less than or equal to $x .$ For example, $[[\pi]]=3$ and $[[3]]=3 .$ For each sequence, find $\lim a_{n}$ and verify it with the definition of convergence.
> (a) $a_{n}=[[5 / n]]$
> (b) $a_{n}=[[(12+4 n) / 3 n]]$
> Reflecting on these examples, comment on the statement following Definition 2.2.3 that "the smaller the $\epsilon$ -neighborhood, the larger $N$ may have to be."

**Proof.**

(a) Claim: $\lim a_n = 0$.

Let $\epsilon \gt 0$ be given. Choose $N \in \mathbf{N}$ such that $N \gt \frac{5}{\epsilon}$, then for any $n \ge N$, 
$$
\left\vert [[\frac{5}{n} - 0]] \right\vert = [[\frac{5}{n}]] \le \frac{5}{n} \lt \epsilon.
$$
(b) Claim: $\lim a_n = 1$.

Let $\epsilon \gt 0$ be given. Choose $N\in \mathbf{N}$ such that $N \gt 6$, then for any $n \ge N$,
$$
\left \vert [[\frac{12+4n}{3n}]] - 1 \right \vert = \left \vert [[\frac{4}{3} + \frac{4}{n}]] - 1 \right\vert = \vert 1 - 1 \vert = 0 \lt \epsilon.
$$
The statement still holds here. In the second example, we have directly chosen $N$ such that the difference is exactly zero, which is sufficient but not necessary.



> **Exercise 2.2.6.** Prove Theorem 2.2.7. To get started, assume $\left(a_{n}\right) \rightarrow a$ and also that $\left(a_{n}\right) \rightarrow b .$ Now argue $a=b$.

**Proof.**

Suppose the contrary that $a \neq b$, then take $\epsilon_0 = \frac{\vert a-b\vert}{2} \gt 0$. By definition, there exists $N \in \mathbf{N}$ such that $n \ge N$ implies both
$$
\vert a_n - a \vert \lt \epsilon_0,
$$
and 
$$
\vert a_n - b \vert \lt \epsilon_0
$$
hold, which cannot be true since 
$$
\vert a - b \vert \le \vert a - a_n \vert + \vert a_n -b \vert \lt 2 \epsilon_0 = \vert a - b \vert
$$
is a contradiction.



> **Exercise 2.2.7.** Here are two useful definitions:
> (i) A sequence $\left(a_{n}\right)$ is eventually in a set $A \subseteq \mathbf{R}$ if there exists an $N \in \mathbf{N}$ such that $a_{n} \in A$ for all $n \geq N$.
> (ii) A sequence $\left(a_{n}\right)$ is frequently in a set $A \subseteq \mathbf{R}$ if, for every $N \in \mathbf{N},$ there exists an $n \geq N$ such that $a_{n} \in A$
> (a) Is the sequence $(-1)^{n}$ eventually or frequently in the set \{1\}$?$
> (b) Which definition is stronger? Does frequently imply eventually or does eventually imply frequently?
> (c) Give an alternate rephrasing of Definition $2.2 .3 \mathrm{B}$ using either frequently or eventually. Which is the term we want?
> (d) Suppose an infinite number of terms of a sequence $\left(x_{n}\right)$ are equal to 2.​ Is $\left(x_{n}\right)$ necessarily eventually in the interval (1.9,2.1)$?$ Is it frequently in (1.9, 2.1)?

**Proof.**

(a) The sequence $(-1)^n$ is frequently in the set $\{1\}$.

(b) The first definition is stronger. Eventually implies frequently.

(c)

> **Redefinition of 2.2.3B**: A sequence $(a_n)$ converges to a real number $a$ if for every positive number $\epsilon$,  $(a_n)$ is eventually in the $\epsilon$-neighborhood of $a$. 

(d) Take $x_n = 2(-1)^n$, then there are infinitely many 2's in $(x_n)$. Obviously, $x_n$ is only frequently in (1.9, 2.1) but not eventually.



> **Exercise 2.2.8.** For some additional practice with nested quantifiers, consider the following invented definition:
>
> Let's call a sequence $\left(x_{n}\right)$ zero-heavy if there exists $M \in \mathbf{N}$ such that for all $N \in \mathbf{N}$ there exists $n$ satisfying $N \leq n \leq N+M$ where $x_{n}=0$.
> (a) Is the sequence $(0,1,0,1,0,1, \ldots)$ zero heavy?
> (b) If a sequence is zero-heavy does it necessarily contain an infinite number of zeros? If not, provide a counterexample.
> (c) If a sequence contains an infinite number of zeros, is it necessarily zero-heavy? If not, provide a counterexample.
> (d) Form the logical negation of the above definition. That is, complete the sentence: A sequence is not zero-heavy if $\ldots$

**Proof.**

(a) Yes. We can take $M = 2$ as every consecutive two terms in $(x_n)$ contains a 0.

(b) Yes, a zero-heavy sequence must contain infinite number of zeros.  If it only contains a finite number of zeros, say for some $N \in \mathbf{N}, x_{n} \neq 0$ for all $n \geq$ $N$, then for any $M \in \mathbf{N},$ there does not exist $n$ satisfying $N \leq n \leq N+M$ for which $x_{n}=0$.

(c) No. Consider the sequence $(a_n)$ defined as $a_n=0$ whenever $n=2^k$ for some $k \in \mathbf{N}$ and 1 otherwise. Then given any $M \in \mathbf{N}$, we may choose $k \gt \log_2(M + 1)$ so that
$$
2^{k+1} - (2^k + 1) \gt M,
$$
and so, given the construction of the sequence, if $n \in \{2^k + 1, (2^{k} + 1) + 1, \cdots, (2^k+1)+M\}$, then we have
$$
a_n \neq 0.
$$
Hence, it is not zero-heavy.

(d) A sequence $(x_n)$ is not zero-heavy if for every $M \in \mathbf{N}$, there exists $N \in \mathbf{N}$ such that $x_n \neq 0$ for every $N \le n \le N + M$.

## Exercises of 2.3 The Algebraic and Order Limit Theorems

> **Exercise 2.3.1.**  Let $x_{n} \geq 0$ for all $n \in \mathbf{N}$.
> (a) If $\left(x_{n}\right) \rightarrow 0,$ show that $(\sqrt{x_{n}}) \rightarrow 0$.
> (b) If $\left(x_{n}\right) \rightarrow x,$ show that $(\sqrt{x_{n}}) \rightarrow \sqrt{x}$

**Proof.**

(a) Let $\epsilon \gt 0$ be given. Since $x_n$ converges to 0, there is some $N \in \mathbf{N}$ such that 
$$
x_n \lt \epsilon^2,
$$
for every $n \ge N$. This implies 
$$
\sqrt{x_n} \lt \epsilon,
$$
for every $n \ge N$. So $(\sqrt{x_n}) \rightarrow 0$.

(b) If $x=0$, then it falls to the case of problem (a). 

Suppose $x \neq 0$. Let $\epsilon \gt 0$ be given. Then there is some $N \in \mathbf{N}$ such that 
$$
\vert x_n - x \vert \lt \sqrt{x} \cdot \epsilon,
$$
for every $n \ge N$. Because $x_n \ge 0$, it follows that
$$
\vert \sqrt{x_n} - \sqrt{x} \vert = \frac{\vert x_n - x \vert}{\sqrt{x_n} + \sqrt{x}} \le \frac{\vert x_n - x \vert}{\sqrt{x}} \lt \epsilon,
$$
for every $n \ge N$. Therefore, $(\sqrt{x_{n}}) \rightarrow \sqrt{x}$.



> **Exercise 2.3.2.** Using only Definition $2.2 .3,$ prove that if $\left(x_{n}\right) \rightarrow 2,$ then
> (a) $\left(\frac{2 x_{n}-1}{3}\right) \rightarrow 1$
> (b) $\left(1 / x_{n}\right) \rightarrow 1 / 2$
> (For this exercise the Algebraic limit Theorem is off-limits, so to speak.)

**Proof.**

(a) Let $\epsilon \gt 0$ be given, then there is some $N \in \mathbf{N}$ such that 
$$
\vert x_n - 2 \vert \lt \frac{3}{2} \epsilon,
$$
for every $n \ge N$. Then
$$
\left\vert \frac{2 x_{n}-1}{3} - 1 \right\vert = \frac{2}{3} \vert x_n - 2 \vert \lt \epsilon,
$$
for every $n \ge N$.

(b) Let $\epsilon \gt 0$ be given. Since $x_n$ converges  to 2, there is some $N_1 \in \mathbf{N}$ such that
$$
\vert x_n - 2 \vert \lt 1,
$$
for every $n \ge N_1$. This implies
$$
\vert x_n \vert \gt 1,
$$
for every $n \ge N_1$.

We can also choose $N_2 \in \mathbf{N}$ such that
$$
\vert x_n - 2 \vert \lt 2 \epsilon,
$$
for every $n \ge N_2$.

Let $N = \max\{N_1, N_2\}$, then for every $n \ge N$, we have
$$
\vert \frac{1}{x_n} - \frac{1}{2} \vert = \frac{\vert x_n - 2 \vert}{2 \vert x_n \vert } \lt \frac{\vert x_n - 2 \vert}{2} \lt \epsilon.
$$
Hence, $\left(1 / x_{n}\right) \rightarrow 1 / 2$.



> **Exercise 2.3.3 (Squeeze Theorem).** Show that if $x_{n} \leq y_{n} \leq z_{n}$ for all $n \in \mathbf{N},$ and if $\lim x_{n}=\lim z_{n}=l,$ then $\lim y_{n}=l$ as well.

**Proof.**

Let $\epsilon \gt 0$ be given. Then there is some $N \in \mathbf{N}$ such that 
$$
\vert x_n - l \vert \lt \epsilon, \\
\vert z_n - l \vert \lt \epsilon
$$
for every $n \ge N$. It follows that
$$
l - \epsilon \lt x_n \le y_n \le z_n \lt l + \epsilon,
$$
i.e., 
$$
\vert y_n - l \vert \lt \epsilon,
$$
for every $n \ge N$. This shows $y_n$ also has limit $l$.



> **Exercise 2.3.4** Let $(a_n) \rightarrow 0$, and use the Algebraic Limit Theorem to compute each of the following limits (assuming the fractions are always defined):
>
> (a) $\lim \left(\frac{1+2 a_{n}}{1+3 a_{n}-4 a_{n}^{2}}\right)$
> (b) $\lim \left(\frac{\left(a_{n}+2\right)^{2}-4}{a_{n}}\right)$
> (c) $\lim \left(\frac{\frac{2}{a_{n}}+3}{\frac{1}{a_{n}}+5}\right)$

**Proof.**

(a) By Algebraic Limit Theorem, the limit is 1

(b) Since
$$
\frac{(a_n + 2)^2 - 4}{a_n} = a_n + 4, 
$$
and $(a_n)$ approches 0, we have the limit as 4.

(c) Since
$$
\frac{\frac{2}{a_{n}}+3}{\frac{1}{a_{n}}+5} = \frac{2 + 3a_n}{1 + 5 a_n},
$$
and $(a_n)$ approches 0, we have limit as 2.



> **Exercise 2.3.5.** Let $\left(x_{n}\right)$ and $\left(y_{n}\right)$ be given, and define $\left(z_{n}\right)$ to be the "shuffled" sequence $\left(x_{1}, y_{1}, x_{2}, y_{2}, x_{3}, y_{3}, \ldots, x_{n}, y_{n}, \ldots\right) .$ Prove that $\left(z_{n}\right)$ is convergent if and only if $\left(x_{n}\right)$ and $\left(y_{n}\right)$ are both convergent with $\lim x_{n}=\lim y_{n}$

**Proof.**

$(\Longrightarrow)$: Suppose$(z_n)$ converges to $L$. By the definition of $(z_n)$, we have
$$
x_n = z_{2n-1}, y_n = z_{2n},
$$
i.e., $(x_n)$ and $(y_n)$ are just sequence of odd and even terms of $(z_n)$, respectively. So they converges to $L$ as well.

$(\Longleftarrow)$: Suppose $(x_n)$ and $(y_n)$ both converge to the same limit $L$. Since $z_n = x_{(n+1)/2}$ if $n$ is odd and $z_n = y_{n/2}$ if $n$ is even, if $n$ is sufficiently large, then both $x_{(n+1)/2}$ and $y_{n/2}$ will be close to $L$, which means $z_n$ will be close to $L$.



> **Exercise 2.3.6.** Consider the sequence given by $b_{n}=n-\sqrt{n^{2}+2 n} .$ Taking $(1 / n) \rightarrow 0$ as given, and using both the Algebraic limit Theorem and the result in Exercise $2.3 .1,$ show $\lim b_{n}$ exists and find the value of the limit.

**Proof.**

We can write $b_n$ as 
$$
b_n = n - \sqrt{n^2 + 2n} = \frac{-2n}{n+\sqrt{n^2 +2n}} = \frac{-2}{1 + \sqrt{1 + \frac{2}{n}}},
$$
then since $\frac{1}{n} \to 0$, by Algebraic limit theorem and the result in Exercise 2.3.1, the limit of $b_n$ exists and is -1.

> **Exercise 2.3.7.** Give an example of each of the following, or state that such a request is impossible by referencing the proper theorem(s):
> (a) sequences $\left(x_{n}\right)$ and $\left(y_{n}\right),$ which both diverge, but whose sum $\left(x_{n}+y_{n}\right)$ converges;
> (b) sequences $\left(x_{n}\right)$ and $\left(y_{n}\right),$ where $\left(x_{n}\right)$ converges, $\left(y_{n}\right)$ diverges, and $\left(x_{n}+y_{n}\right)$ converges;
>
> (c) a convergent sequence $\left(b_{n}\right)$ with $b_{n} \neq 0$ for all $n$ such that $\left(1 / b_{n}\right)$ diverges;
> (d) an unbounded sequence $\left(a_{n}\right)$ and a convergent sequence $\left(b_{n}\right)$ with $\left(a_{n}-b_{n}\right)$ bounded;
> (e) two sequences $\left(a_{n}\right)$ and $\left(b_{n}\right),$ where $\left(a_{n} b_{n}\right)$ and $\left(a_{n}\right)$ converge but $\left(b_{n}\right)$ does not.

**Proof.**

(a) Possible, e.g., $x_n = (-1)^n$ and $y_n = (-1)^{n+1}$ both diverges but their sum $x_n + y_n$ is the constant zero sequence, which obviously converges.

(b) Impossible. If $x_n + y_n$ converges, then $y_n = (x_n + y_n) - x_n$ must be convergent by the Algebraic Limit Theorem. However, this leads to a contradiction.

(c) Possible, e.g., $b_n = \frac{1}{n}$, which converges to 0, however, $\frac{1}{b_n} = n$ diverges.

(d) Impossible. Because convergent sequences are bounded, it follows that
$$
\vert a_n \vert = \vert (a_n - b_n) + b_n \vert \le \vert a_n - b_n \vert + \vert b_n \vert
$$
is bounded, which is a contradiction.

(e) Possible, e.g.,  $a_n = \frac{1}{n}$ and $b_n = (-1)^n$.



> **Exercise 2.3.8.** Let $\left(x_{n}\right) \rightarrow x$ and let $p(x)$ be a polynomial.
> (a) Show $p\left(x_{n}\right) \rightarrow p(x)$
> (b) Find an example of a function $f(x)$ and a convergent sequence $\left(x_{n}\right) \rightarrow x$ where the sequence $f\left(x_{n}\right)$ converges, but not to $f(x)$

**Proof.**

(a) Suppose $p(x)=a_0 + a_1 x + a_2 x^2 + \cdots + a_px^p$, then by Algebraic Limit Theorem, we have
$$
\begin{align}
\lim p(x_n) &= \lim (a_0 + a_1 x_n + a_2 x_n^2 + \cdots + a_px_n^p) \\
&=\lim a_0 + \lim a_1 x_n + \lim a_2 x_n^2 + \cdots + \lim a_p x_n^p \\
&= a_0 + a_1 x + a_2 x^2 + a^p x^p \\
&= p(x).
\end{align}
$$
(b) Define $f:[0,\infty) \to \mathbf{R}$ by
$$
f(x)= \begin{cases}
0, & x=0 \\
1, & x \gt 0
\end{cases},
$$
and $x_n = \frac{1}{n}$. Then $x_n \to 0$ and $f(x_n)$ converges to 1, not $f(0)=0$. 



> **Exercise 2.3.9.** (a) Let $\left(a_{n}\right)$ be a bounded (not necessarily convergent) sequence, and assume $\lim b_{n}=0 .$ Show that $\lim \left(a_{n} b_{n}\right)=0 .$ Why are we not allowed to use the Algebraic limit Theorem to prove this?
> (b) Can we conclude anything about the convergence of $\left(a_{n} b_{n}\right)$ if we assume that $\left(b_{n}\right)$ converges to some nonzero limit $b ?$
> (c) Use (a) to prove Theorem $2.3 .3,$ part $($ iii $),$ for the case when $a=0 .$

**Proof.**

(a) Let $\epsilon \gt 0$ be given. Since $a_n$ is bounded, there exists some $M \gt 0$ such that
$$
\vert a_n \vert \le M,
$$
for every $n \in \mathbf{N}$. Since $b_n$ has limit 0, we know there is some $N \in \mathbf{N}$ such that 
$$
\vert b_n \vert \lt \frac{\epsilon}{M},
$$
for every $n \ge N$. Then,
$$
\vert a_n b_n \vert \lt M \cdot \frac{\epsilon}{M} = \epsilon,
$$
for every $n \ge N$, hence $a_nb_n$ converges to 0.

The reason why we cannot use Algebraic Limit Theorem here is that $a_n$ is not convergent.

(b) No, e.g., take $a_n = (-1)^n$ and $b_n = 1 + \frac{1}{n} \to1$, however, $a_n b_n$ does not converge because the limits of odd terms and even terms do not match.

(c) Since $b_n$ is convergent, it is bounded. By part (a),
$$
\lim (a_n b_n) = 0.
$$

> **Exercise 2.3.10.** Consider the following list of conjectures. Provide a short proof for those that are true and a counterexample for any that are false.
> (a) If $\lim \left(a_{n}-b_{n}\right)=0,$ then $\lim a_{n}=\lim b_{n}$
> (b) If $\left(b_{n}\right) \rightarrow b,$ then $\left|b_{n}\right| \rightarrow|b|$
> (c) If $\left(a_{n}\right) \rightarrow a$ and $\left(b_{n}-a_{n}\right) \rightarrow 0,$ then $\left(b_{n}\right) \rightarrow a$
> (d) If $\left(a_{n}\right) \rightarrow 0$ and $\left|b_{n}-b\right| \leq a_{n}$ for all $n \in \mathbf{N},$ then $\left(b_{n}\right) \rightarrow b$

**Proof.**

(a) False, limit may not even exist!

(b) True. Because $\left\vert \; \vert b_n \vert - \vert b \vert \; \right\vert \le \vert b_n - b \vert$ and $b_n$ converges to $b$.

(c) True. Use Algebraic Limit Theorem.

(d) True. Use Squeeze Theorem.

> **Exercise 2.3.11** (**Cesaro Means**). (a) Show that if $\left(x_{n}\right)$ is a convergent sequence, then the sequence given by the averages
> $$
> y_{n}=\frac{x_{1}+x_{2}+\cdots+x_{n}}{n}
> $$
> also converges to the same limit.
> (b) Give an example to show that it is possible for the sequence $\left(y_{n}\right)$ of averages to converge even if $\left(x_{n}\right)$ does not.

**Proof.**

(a) Let $\epsilon \gt 0$ be given. Since $x_n$ converges to $x$, it must be bounded. Hence there exists $M \gt 0$ such that $\vert x_n - x \vert \le M$ for all $n \in \mathbf{N}$. Again, since $x_n$ converges to $x$, there exists $N_0 \in \mathbf{N}$ such that 
$$
\vert x_n - x \vert \lt \frac{\epsilon}{2},
$$
for all $n \gt N_0$.

If we take an integer $N = \max \{N_0, \frac{2N_0M}{\epsilon}\}$, then for $n \gt N$, we have
$$
\begin{align}
\vert y_n - x \vert &= \left\vert \frac{1}{n} \sum_{k=1}^n (x_k - x) \right\vert \\ 
&\le \frac{1}{n} \sum_{k=1}^n \vert x_k - x \vert \\
&= \frac{1}{n} \sum_{k=1}^{N_0} \vert x_k - x \vert + \frac{1}{n} \sum_{k=N_0 + 1}^n \vert x_k - x \vert \\
&\lt \frac{1}{n} N_0 \cdot M + \frac{1}{n} (n - N_0) \cdot \frac{\epsilon}{2} \\
&\le \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon.
\end{align}
$$
Therefore, $y_n$ converges to $x$ as well.

(b) Take $x_n = (-1)^n$, then $x_n$ does not converge but $y_n \to 0$.



> **Exercise 2.3.12.** A typical task in analysis is to decipher whether a property possessed by every term in a convergent sequence is necessarily inherited by the limit. Assume $\left(a_{n}\right) \rightarrow a,$ and determine the validity of each claim. Try to produce a counterexample for any that are false.
>
> (a) If every $a_{n}$ is an upper bound for a set $B,$ then $a$ is also an upper bound for $B$.
>
> (b) If every $a_{n}$ is in the complement of the interval $(0,1),$ then $a$ is also in the complement of (0,1).
>
> (c) If every $a_{n}$ is rational, then $a$ is rational.

**Proof.**

(a) True. Take an element $b \in B$, since every $a_n$ is an upper bound for $B$, we have
$$
\vert b \vert \le a_n,
$$
for every $n \in \mathbf{N}$. So by the **Order Limit Theorem**,  we have
$$
\vert b \vert \le a.
$$
Since $b$ is chosen arbitrarily, we see that $a$ is an upper bound for $B$.

(b) True. Assume on the contrary that $a \in (0, 1)$. Take $\epsilon_0 = \min \{\frac{a}{2}, \frac{1-a}{2}\} \gt 0$, then there exists $N \in \mathbf{N}$ such that
$$
\vert a_n - a \vert \lt \epsilon_0,
$$
for every $n \gt N$. However, this means 
$$
a_n \in (0, 1),
$$
for every $n \gt N$, which is a contradiction. Hence our assumption cannot be true. Thus $a$ must be in the complement of $(0, 1)$.

(c) False. To give a counterexample, we can use Theorem 1.4.3. For any $n \in \mathbf{N}$, we can find a rational number $a_n$ such that
$$
\sqrt{2} \lt a_n \lt \sqrt{2}  + \frac{1}{n}.
$$
Hence $(a_n) \to a = \sqrt{2}$, which is an irrational number.



> **Exercise 2.3.13 (Iterated Limits).** Given a doubly indexed array $a_{m n}$ where $m, n \in \mathbf{N},$ what should $\lim _{m, n \rightarrow \infty} a_{m n}$ represent?
> (a) Let $a_{m n}=m /(m+n)$ and compute the iterated limits
> $$
> \lim _{n \rightarrow \infty}\left(\lim _{m \rightarrow \infty} a_{m n}\right) \quad \text { and } \quad \lim _{m \rightarrow \infty}\left(\lim _{n \rightarrow \infty} a_{m n}\right).
> $$
> Define $\lim _{m, n \rightarrow \infty} a_{m n}=a$ to mean that for all $\epsilon>0$ there exists an $N \in \mathbf{N}$ such that if both $m, n \geq N,$ then $\left|a_{m n}-a\right|<\epsilon$
> (b) Let $a_{m n}=1 /(m+n) .$ Does $\lim _{m, n \rightarrow \infty} a_{m n}$ exist in this case? Do the two iterated limits exist? How do these three values compare? Answer these same questions for $a_{m n}=m n /\left(m^{2}+n^{2}\right)$
> (c) Produce an example where $\lim _{m, n \rightarrow \infty} a_{m n}$ exists but where neither iterated limit can be computed.
> (d) Assume $\lim _{m, n \rightarrow \infty} a_{m n}=a,$ and assume that for each fixed $m \in \mathbf{N}$ $\lim _{n \rightarrow \infty}a_{m n} = b_{m} .$ Show $\lim _{m \rightarrow \infty} b_{m}=a$
> (e) Prove that if $\lim _{m, n \rightarrow \infty} a_{m n}$ exists and the iterated limits both exist, then all three limits must be equal.

 

**Proof.**

(a) 
$$
\lim_{n\to\infty}\left(\lim_{m \to \infty}a_{mn} \right) = \lim_{n\to\infty}1 = 1, \\
\lim_{m\to\infty}\left(\lim_{n \to \infty}a_{mn} \right) = \lim_{m\to\infty}0 = 0. \\
$$
(b) Yes, $\lim _{m, n \rightarrow \infty} a_{m n}$ exists.

Let $\epsilon \gt 0$ be given. Take an integer $N \gt \frac{1}{2\epsilon}$, then for every $m, n \ge N$, we have

$m + n \gt \frac{1}{\epsilon}$, and hence $\vert \frac{1}{m+n} - 0 \vert \lt \epsilon$. Thus, $\lim _{m, n \rightarrow \infty} a_{m n} = 0$.

For this example, the two iterated limits both exist and are equal to 0. We see that these three values are equal.

Now, consider the sequence $a_{m n}=m n /\left(m^{2}+n^{2}\right)$. 
$$
\lim_{n\to\infty}\left(\lim_{m \to \infty}a_{mn} \right) = \lim_{n\to\infty}0 = 0, \\
\lim_{m\to\infty}\left(\lim_{n \to \infty}a_{mn} \right) = \lim_{m\to\infty}0 = 0. \\
$$


However, $\lim _{m, n \rightarrow \infty} a_{m n}$ does not exist. To show this, assume it does exist. Let $\epsilon \gt 0$ be given, then there exists $N \in \mathbf{N}$ such that for every  $m, n \ge N$, we have
$$
\vert a_{mn} - a \vert  \lt \epsilon.
$$
If we take $m = n \ge N$, then
$$
\vert a_{nn} - a \vert = \vert \frac{1}{2} - a \vert \lt \epsilon.
$$
Since $\epsilon$ is arbitrarily given, it follows that $a$ must be $\frac{1}{2}$.

Similarly, if we take $m = 2n \ge N$, then
$$
\vert a_{2n,n} - a \vert = \vert \frac{2}{5} - a \vert \lt \epsilon.
$$
This implies $a = \frac{2}{5}$. However, the limit must be unique if it exists. We have reached a contradiction here and we are done.

(c) Take
$$
a_{mn} = \frac{(-1)^n}{m} + \frac{(-1)^m}{n},
$$
then $\lim _{m, n \rightarrow \infty} a_{m n} = 0$ but neither iterated limit exists.

(d) Let $\epsilon \gt 0$ be given. Since $\lim _{m, n \rightarrow \infty} a_{m n}=a,$ there exists $N \in \mathbf{N}$ such that

for every $m, n \ge N$, we have
$$
\vert a_{mn} - a \vert \lt \frac{\epsilon}{2}.
$$
For each fixed $m \in \mathbf{N}$, there exists $N_0 \in \mathbf{N}$ such that for every $n \ge N_0$, we have
$$
\vert a_{mn} - b_m \vert \lt \frac{\epsilon}{2}.
$$
Take $n = \max\{N, N_0\}$, then for every $m \ge N$, we have
$$
\vert b_m - a \vert = \vert b_m - a_{mn} + a_{mn} - a \vert \le \vert b_m - a_{mn} \vert + \vert a_{mn} - a \vert \lt \epsilon.
$$
This shows $\lim _{m \rightarrow \infty} b_{m}=a$.

(e) Since the iterated limit $\lim _{m \rightarrow \infty}\left(\lim _{n \rightarrow \infty} a_{m n}\right)$ exists, $\lim _{n \rightarrow \infty} a_{m n}$ also exists and by previous problem,
$$
\lim _{m, n \rightarrow \infty} a_{m n}=\lim _{m \rightarrow \infty}\left(\lim _{n \rightarrow \infty} a_{m n}\right).
$$
Similarly,
$$
\lim _{m, n \rightarrow \infty} a_{m n}=\lim _{n \rightarrow \infty}\left(\lim _{m \rightarrow \infty} a_{m n}\right).
$$

## Exercises of 2.4 The Monotone Convergence Theorem and a First Look at Infinite Series

> **Exercise 2.4.1**
> (a) Prove that the sequence defined by $x_{1}=3$ and
> $$
> x_{n+1}=\frac{1}{4-x_{n}}
> $$
> converges.
>
> (b) Now that we know $\lim x_{n}$ exists, explain why lim $x_{n+1}$ must also exist and equal the same value.
>
> (c) Take the limit of each side of the recursive equation in part (a) to explicitly compute $\lim x_{n}$

**Proof.** 

(a) We will first show $(x_n)$ is strictly decreasing by induction. As for the base case, $x_1 <x_2$ holds. Suppose that 
$$
3=x_1 \gt x_2 \gt \cdots \gt x_{n-1} \gt x_n,
$$
then 
$$
x_{n} - x_{n+1} = \frac{1}{4-x_{n-1}} - \frac{1}{4-x_{n}} = \frac{x_{n-1} - x_{n}}{(4 - x_{n-1})(4 - x_{n})} \gt 0.
$$
Hence, by induction $x_n \gt x_{n+1}$ holds for all $n \in \mathbf{N}$.

Next, we will show $(x_n)$ is bounded. Since $x_n \lt 4$ for all $n \in \mathbf{N}$, we have $x_{n+1} = \frac{1}{4-x_n} \gt 0$. Hence the sequence is bounded.

Therefore, the sequence $(x_n)$ converges by the Monotone Convergence Theorem.

(b) Limit exists means that the sequence eventually falls into any $\epsilon-$neighborhood of the limit. Shifting the indices does not change the eventual behavior of the sequence, i.e., the new sequence would eventually still be in any $\epsilon-$neighborhood of the limit (the same limit as the origin sequence).

(c) Taking the limit of each side of the recursive equation, we get by Algebraic Limit Theorem that
$$
\lim x_{n}=\lim x_{n+1}=\frac{1}{4-\lim x_{n}}.
$$
Solving it we get that $\lim x_n = 2 \pm \sqrt{3}$. But by Order Limit Theorem we know that the limit must be less than 3 since it is decreasing. Hence $\lim x_n = 2 - \sqrt{3}$.

> **Exercise 2.4.2**
> (a) Consider the recursively defined sequence $y_{1}=1$
> $$
> y_{n+1}=3-y_{n}
> $$
> and set $y=\lim y_{n} .$ Because $\left(y_{n}\right)$ and $\left(y_{n+1}\right)$ have the same limit, taking the limit across the recursive equation gives $y=3-y .$ Solving for $y,$ we conclude $\lim y_{n}=3 / 2$
> What is wrong with this argument?
> (b) This time set $y_{1}=1$ and $y_{n+1}=3-\frac{1}{y_{n}} .$ Can the strategy in (a) be applied to compute the limit of this sequence?

**Proof.**

(a) The sequence $(y_n)$ does not converge since $y_n = (1, 2, 1, 2, \cdots)$, so we cannot take limit here.

(b) Yes. By induction $(y_n)$ is strictly increasing, and to see it is bounded, notice that $y_n \gt 0$ for all $n \in \mathbf{N}$ and hence $y_{n+1} = 3 - \frac{1}{y_n} \lt 3$. By Monotone Convergence Theorem again, $(y_n)$ is convergent.

Now, we take the limit for both sides and get
$$
\lim y_n = 3 - \frac{1}{\lim y_n}.
$$
Hence, $\lim y_n = \frac{3 \pm \sqrt{5}}{2}$. Since $y_n \gt 1$, its limit must be greater than or equal to 1 and hence $\lim y_n = \frac{3 + \sqrt{5}}{2}$.

> **Exercise 2.4.3.**
> (a) Show that
> $$
> \sqrt{2}, \sqrt{2+\sqrt{2}}, \sqrt{2+\sqrt{2+\sqrt{2}}}, \ldots
> $$
> converges and find the limit.
> (b) Does the sequence
> $$
> \sqrt{2}, \sqrt{2 \sqrt{2}}, \sqrt{2 \sqrt{2 \sqrt{2}}}, \ldots
> $$
> converge? If so, find the limit.

**Proof.**

(a) Define $x_1 = \sqrt{2}$ and $x_{n+1} = \sqrt{2 +x_n}$, then by induction $x_n \lt 2$. Next, we show $(x_n)$ is increasing by induction. 

First, $x_1 \lt x_2$ holds. Suppose 
$$
\sqrt{2} = x_1 \lt x_2 \lt \cdots \lt x_{n-1} \lt x_n,
$$
then
$$
x_{n+1} - x_{n} = \sqrt{2 + x_n} - \sqrt{2 + x_{n-1}} = \frac{x_n - x_{n-1}}{\sqrt{2 + x_n} + \sqrt{2 + x_{n-1}}} \gt 0.
$$
Hence, by induction $(x_n)$ is inceasing. 

Since $0 \lt x_n \lt 2$, this sequence is also bounded.the  By Monotone Convergence Theorem $\lim x_n$ exists. Taking the limit of both sides of $x_{n+1}=\sqrt{2+x_{n}}$, we have
$$
\lim x_n = \sqrt{2 + \lim x_n}.
$$
Hence $\lim x_n = 2$.

(b) Yes. Define $x_1 = \sqrt{2}$ and $x_{n+1} = \sqrt{2 x_n}$ then by induction $x_n \lt 2$. Use induction again, we can show $(x_n)$ is increasing. Since $0 \lt x_n \lt 2$, the sequence is also bounded. By Monotone Convergence Theorem $\lim x_n$ exists. Taking the limit of both sides of $x_{n+1} = \sqrt{2 x_n}$, we have
$$
\lim x_{n}=\sqrt{2 \lim x_{n}}.
$$
Hence $\lim x_n = 2$.



> **Exercise 2.4.4.**
>
> (a) In Section 1.4 we used the Axiom of Completeness $($ AoC $)$ to prove the Archimedean Property of $\mathbf{R}$ (Theorem 1.4.2$) .$ Show that the Monotone Convergence Theorem can also be used to prove the Archimedean Property without making any use of AoC.
> (b) Use the Monotone Convergence Theorem to supply a proof for the Nested Interval Property (Theorem 1.4.1) that doesn't make use of AoC.
>
> These two results suggest that we could have used the Monotone Convergence Theorem in place of AoC as our starting axiom for building a proper theory of the real numbers.

**Proof.**

(a) Assume, for contradiction, that $\mathbf{N}$ is bounded above, i.e., there exists a real number $M \gt 0$ such that 
$$
n \le M,
$$
for every $n \in \mathbf{N}$. The sequence $x_n = n$ is monotonically increasing and bounded, and hence by MCT, it converges, say to $\alpha$.

Since $\lim x_n = \alpha$, there exists $N \in \mathbf{N}$ such that
$$
\vert n - \alpha \vert \lt \frac{1}{2},
$$
for every $n \gt N$. In particular,  take $n = N + 1$ and $n = N + 2$, then
$$
\vert N + 1 - \alpha \vert \lt \frac{1}{2}, \\
\vert N + 2 - \alpha \vert \lt \frac{1}{2}.
$$
Hence
$$
\vert N + 1 - \alpha \vert + \vert N + 2 - \alpha \vert \lt 1.
$$
On the other hand, by triangular inequality, we have
$$
\vert N + 1 - \alpha \vert + \vert N + 2 - \alpha \vert \ge \vert N + 1 - \alpha - (N + 2 - \alpha) \vert = 1.
$$
Hence we have reached a contradiction. Thus part (a) is proved.

(b) The sequence $(a_n)$ is monotonically increasing and bounded, thus it is convergent, say to $\alpha$. By the proof of MCT, we have $a_n \le \alpha$ for every $n \in \mathbf{N}$. Moreover, given arbitrary $m \in \mathbf{N}$, we have $a_n \le b_m$ for every $n \in \mathbf{N}$. By Order Limit Theorem, we have $\alpha \le b_m$ for every $m \in \mathbf{N}$. Therefore, we have $a_n \le \alpha \le b_n$ for every $n \in \mathbf{N}$. Hence $\alpha \in \cap_{n=1}^{\infty}I_n$, and the intersection is not empty.



> **Exercise 2.4.5 (Calculating Square Roots).** Let $x_{1}=2,$ and define
> $$
> x_{n+1}=\frac{1}{2}\left(x_{n}+\frac{2}{x_{n}}\right)
> $$
> (a) Show that $x_{n}^{2}$ is always greater than or equal to $2,$ and then use this to prove that $x_{n}-x_{n+1} \geq 0 .$ Conclude that $\lim x_{n}=\sqrt{2}$.
>
> (b) Modify the sequence $(x_n)$  so that it converges to  $\sqrt{c}$ .

**Proof.**

(a) By Arithmetic-Geometric inequality, we have
$$
x_{n+1}=\frac{1}{2}\left(x_{n}+\frac{2}{x_{n}}\right) \ge \frac{1}{2} \cdot 2 \cdot \sqrt{x_n \cdot \frac{2}{x_n}} = \sqrt{2}.
$$
Moreover, $x_1 = 2 \gt \sqrt{2}$, hence $x_n \ge \sqrt{2}$ for every $n \in \mathbf{N}$. This implies $x_n^2 \ge 2$ for every $n \in \mathbf{N}$. To show $x_n - x_{n+1} \ge 0$, we calcualte 
$$
x_n - x_{n+1} = x_n - \frac{1}{2}(x_n + \frac{2}{x_n}) = \frac{1}{2}(x_n - \frac{2}{x_n}) = \frac{x_n^2 - 2}{x_n} \ge 0.
$$
Hence, the sequence $(x_n)$ is decreasing. Since it is also bounded (between 2 and $\sqrt{2}$), by MCT, we have that $\lim x_n = x$ exists. Taking limit of both sides of the recursive definition of $(x_n)$, we obtain
$$
x = \frac{1}{2}(x + \frac{2}{x}).
$$
Solving the above equation, we obtain $\lim x_n = x = \sqrt{2}$.

(b) Let $x_1 = \sqrt{c} + 1$ (any number greater than $\sqrt{c}$ is fine), and define $x_{n+1} = \frac{1}{2}(x_n + \frac{c}{x_n})$.



> **Exercise 2.4.6 (Arithmetic-Geometric Mean).**
>
> (a) Explain why $\sqrt{x y} \leq$ $(x+y) / 2$ for any two positive real numbers $x$ and $y .$ (The geometric mean is always less than the arithmetic mean.)
> (b) Now let $0 \leq x_{1} \leq y_{1}$ and define
> $$
> x_{n+1}=\sqrt{x_{n} y_{n}} \quad \text { and } \quad y_{n+1}=\frac{x_{n}+y_{n}}{2}
> $$
> Show $\lim x_{n}$ and $\lim y_{n}$ both exist and are equal.

**Proof.**

(a) Since
$$
(\frac{1}{2}(x + y))^2 - (\sqrt{xy})^2 = (\frac{1}{2}(x - y))^2 \ge 0,
$$
and $x, y$ are positive, we have that
$$
\sqrt{xy} \le \frac{1}{2}(x + y).
$$
(b) We show by induction that $0 \le x_n \le x_{n+1} \le y_{n+1} \le y_n$. 

Base case $n=1$:

By part (a), we have
$$
x_2 = \sqrt{x_1y_1} \le \frac{x_1 + y_1}{2} = y_2.
$$
Since $x_1 \le y_1$, we also have
$$
x_1 \le \sqrt{x_1y_1} = x_2,
$$
and
$$
y_2 = \frac{x_1 + y_1}{2} \le y_1.
$$
Hence the base case is proved.

Induction step: 

Suppose that $0 \le x_n \le x_{n+1} \le y_{n+1} \le y_n$. By repeating the case for $n=1$, we can show that $0 \le x_{n+1} \leq x_{n+2} \le y_{n+2} \le y_{n+1}$.

Hence the sequence $(x_n)$ is increasing while $(y_n)$ is decreasing. Moreover, they are also bounded. Hence, by MCT, $\lim x_n$ and $\lim y_n$ both exist. Taking limit on both sides of $y_{n+1} = \frac{x_n + y_n}{2}$, we get
$$
\lim y_n = \frac{\lim x_n + \lim y_n}{2}.
$$
Therefore, $\lim x_n = \lim y_n$.



> **Exercise 2.4.7 (Limit Superior)**. Let $\left(a_{n}\right)$ be a bounded sequence.
> (a) Prove that the sequence defined by $y_{n}=\sup \left\{a_{k}: k \geq n\right\}$ converges.
> (b) The limit superior of $\left(a_{n}\right),$ or $\lim \sup a_{n},$ is defined by
> $$
> \limsup a_{n}=\lim y_{n}
> $$
> where $y_{n}$ is the sequence from part (a) of this exercise. Provide a reasonable definition for lim inf $a_{n}$ and briefly explain why it always exists for any bounded sequence.
> (c) Prove that $\lim \inf a_{n} \leq \limsup a_{n}$ for every bounded sequence, and give an example of a sequence for which the inequality is strict.
> (d) Show that $\lim \inf a_{n}=\limsup a_{n}$ if and only if $\lim a_{n}$ exists. In this case, all three share the same value.

**Proof.**

(a) By definition, we have $y_n \ge a_k$ for all $k \ge n$. In particular, $y_n \ge a_k$ for all $k \ge n+1$. Therefore $y_n$ is an upper bound of $\{a_k : k \ge n + 1 \}$. By definition of sup, we have that $y_n \ge y_{n+1}$. Hence the sequence $(y_n)$ is decreasing. Since $(a_n)$ is bounded, there exists $M \in \mathbf{R}$ such that $a_n \ge M$ for all $n \in \mathbf{N}$. Since $y_n \ge a_n$, we have $y_n \ge M$ for all $n \in \mathbf{N}$. Therefore, $(y_n)$ is bounded. By MCT, the sequence $(y_n)$ converges.

(b) Let $x_n = \inf \{a_k: k \ge n\}$. Similarly to part (a), this sequence is increasing and bounded. Hence by MCT, the sequence $(x_n)$ converges. Define limit inferior as :
$$
\lim \inf a_n = \lim x_n.
$$
(c) Since 
$$
x_n \le a_n \le y_n,
$$
for all $n \in \mathbf{N}$, by Order Limit Theorem, we have
$$
\lim \inf a_n = \lim x_n \le \lim y_n = \lim \sup a_n.
$$
Let $a_n = (-1)^n$, then 
$$
\lim \sup a_n = 1, \lim \inf a_n = -1.
$$
Hence the inequality is strict.

(d) $(\Longrightarrow)$:

By part (c) we have
$$
x_n \le a_n \le y_n,
$$
for all $n \in \mathbf{N}$. Moreover, 
$$
\lim x_n = \lim \inf a_n = \lim \sup a_n = y_n.
$$
By Squeeze Theorem, we see that $\lim a_n$ exists as well and 
$$
\lim a_n = \lim \inf a_n = \lim \sup a_n.
$$
$(\Longleftarrow)$:

Let $\epsilon \gt 0$. Since $\lim a_n = a$, there exists $N \in \mathbf{N}$ such that for all $n \gt N$ we have
$$
a - \epsilon \lt a_n \lt a + \epsilon.
$$
Now taking $n \gt N$, for all $k \ge n$, we also have $a_k \lt a + \epsilon$. Hence $a+\epsilon$  is an upper bound of $\{a_k: k \ge n\}$. Thus $y_n \le a + \epsilon$. Note that we also have
$$
y_n \ge a_n \gt a - \epsilon.
$$
Therefore,
$$
a - \epsilon \lt y_n \le a + \epsilon \implies \vert y_n - a \vert \le \epsilon,
$$
for all $n \gt N$. Hence $\lim y_n = a$, namely $\lim \sup a_n = \lim a_n$. Similarly, we can show that $\lim x_n =\lim \inf a_n = \lim a_n$.



> **Exercise 2.4.8.** For each series, find an explicit formula for the sequence of partial sums and determine if the series converges.
> (a) $\sum_{n=1}^{\infty} \frac{1}{2^{n}}$
> (b) $\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$
> (c) $\sum_{n=1}^{\infty} \log \left(\frac{n+1}{n}\right)$
> (In $(\mathrm{c}), \log (x)$ refers to the natural logarithm function from calculus.)

**Proof.**

(a) The partial sum $s_m = 1 - \frac{1}{2^m}$ is increasing and $s_m \lt 1$. By MCT, the sequence is convergent. Moreover,
$$
s = \lim_{n\to \infty} (1 - \frac{1}{2^m}) = 1.
$$
(b) Note that $\frac{1}{n(n+1)}=\frac{1}{n}-\frac{1}{n+1},$ the partial sum is given by
$$
\begin{aligned}
s_{m} &=\frac{1}{1 \cdot 2}+\frac{1}{2 \cdot 3}+\cdots+\frac{1}{m(m+1)} \\
&=\left(1-\frac{1}{2}\right)+\left(\frac{1}{2}-\frac{1}{3}\right)+\cdots+\left(\frac{1}{m}-\frac{1}{m+1}\right) \\
&=1+\left(-\frac{1}{2}+\frac{1}{2}\right)+\cdots+\left(-\frac{1}{m}+\frac{1}{m}\right)-\frac{1}{m+1} \\
&=1-\frac{1}{m+1}
\end{aligned}
$$
Therefore the partial sum is less than $1 .$ Thus the sequence is bounded and, by MCT, convergent. Moreover the limit is
$$
s=\lim _{m \rightarrow \infty}\left(1-\frac{1}{m+1}\right)=1.
$$
(c) Since $\log (\frac{n + 1}{n}) = \log (n+1) - \log (n)$, we have
$$
\begin{align}
s_m &= \log\frac{2}{1} + \log\frac{3}{2} + \cdots + \log\frac{m+1}{m}\\
&= (\log 2  - \log1) + (\log 3  - \log 2) + \cdots + (\log (m+1)  - \log m) \\
&= \log(m+1) - \log 1 = \log(m + 1).
\end{align}
$$
Therefore the partial sum is not bounded. Hence the sequence is divergent.



> **Exercise 2.4.9.** Complete the proof of Theorem 2.4.6 by showing that if the series $\sum_{n=0}^{\infty} 2^{n} b_{2^{n}}$ diverges, then so does $\sum_{n=1}^{\infty} b_{n} .$ Example 2.4.5 may be a useful reference.

**Proof.**

Let $s_m$ be the partial sum of $\sum_{n=1}^{\infty} b_{n}$ and $\tilde{s}_k$ the partial sum of $\sum_{n=0}^{\infty} 2^{n} b_{2^{n}}$. Then 
$$
\begin{align}
s_{2^k} &= b_1 + b_2 + (b_3 + b_4) + (b_5 + \cdots + b_8) + \cdots + (b_{2^{k-1}} + \cdots + b_{2^k}) \\
&\gt b_1 + b_2 + (b_4 + b_4) + (b_8 + \cdots +b_8) + \cdots + (b_{2^k} + \cdots + b_{2^k}) \\
&= b_1 + b_2 + 2 b_4 + 4 b_8 + \cdots + 2^{k-1} b_{2^k}.
\end{align}
$$
If we multiply $s_{2^k}$ by 2, then
$$
\begin{align}
2 \cdot s_{2^k} &= 2 b_1 + 2 b_2 + 4 b_4 + 8 b_8 + \cdots + 2^k b_{2^k} \\
&\ge b_1 + 2 b_2 + 4 b_4 + 8 b_8 + \cdots + 2^k b_{2^k} = \tilde{s}_k.
\end{align}
$$
Since $\tilde{s}_k$ is not bounded above, we know that $s_m$ is not bounded above. Therefore, $s_m$ diverges, namely $\sum_{n=1}^{\infty} b_{n}$ diverges.



> **Exercise 2.4.10 (Infinite Products).** A close relative of infinite series is the infinite product
> $$
> \prod_{n=1}^{\infty} b_{n}=b_{1} b_{2} b_{3} \cdots
> $$
> which is understood in terms of its sequence of partial products
> $$
> p_{m}=\prod_{n=1}^{m} b_{n}=b_{1} b_{2} b_{3} \cdots b_{m}.
> $$
> Consider the special class of infinite products of the form
> $$
> \prod_{n=1}^{\infty}\left(1+a_{n}\right)=\left(1+a_{1}\right)\left(1+a_{2}\right)\left(1+a_{3}\right) \cdots, \quad \text { where } a_{n} \geq 0
> $$
> (a) Find an explicit formula for the sequence of partial products in the case where $a_{n}=1 / n$ and decide whether the sequence converges. Write out the first few terms in the sequence of partial products in the case where $a_{n}=1 / n^{2}$ and make a conjecture about the convergence of this sequence.
> (b) Show, in general, that the sequence of partial products converges if and only if $\sum_{n=1}^{\infty} a_{n}$ converges. (The inequality $1+x \leq 3^{x}$ for positive $x$ will be useful in one direction. $)$

**Proof.**

(a) We compute the partial product
$$
p_m = (1 + 1)(1 + \frac{1}{2})\cdots(1+\frac{1}{n}) = 2 \cdot \frac{3}{2} \cdot \frac{4}{3} \cdots \frac{m+1}{m} = m + 1.
$$
Hence this sequence is divergent.

If $a_n = \frac{1}{n^2}$, then $p_1 = 2, p_2 = \frac{5}{2}, p_3 = \frac{25}{9}$. It should be convergent.

(b) $(\Longrightarrow)$:

Suppose that the partial product is convergent, then $(p_m)$ is bounded. Notice that
$$
p_m = (1 + a_1)(1 + a_2)\cdots(1 + a_m) \ge 1 + a_1 + a_2 + \cdots  a_m = 1 + s_m.
$$
Therefore, the partial sum $s_m$ is also bounded. It is clear that $s_m$ is increasing. Therefore, by MCT, $(s_m)$ converges. Namely, $\sum_{n=1}^{\infty} a_{n}$.

$(\Longleftarrow)$:

By the inequality $1+x \le 3^x$, we have
$$
p_m = (1 + a_1)(1 + a_2)\cdots(1+a_m) \le 3^{a_1} \cdot 3^{a_2} \cdots 3^{a_m} = 3^{a_1 + \cdots + a_m}.
$$
Since $\sum_{n=1}^{\infty} a_{n}$ converges, the partial sum $s_m = \sum_{n=1}^ma_m$ is bounded. Therefore, the partial product $p_m$ is bounded. It is clear that $(p_m)$ is increasing. Therefore, by MCT, $(p_m)$ converges.

