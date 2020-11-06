# Chapter 2 Exercise

## Exercises of 2.5 Subsequences and the Bolzano-Weierstrass Theorem

> **Exercise 2.5.1.** Give an example of each of the following, or argue that such a request is impossible.
> (a) A sequence that has a subsequence that is bounded but contains no subsequence that converges.
> (b) A sequence that does not contain 0 or 1 as a term but contains subsequences converging to each of these values.
> (c) A sequence that contains subsequences converging to every point in the infinite set $\{1,1 / 2,1 / 3,1 / 4,1 / 5, \ldots\}$
> (d) A sequence that contains subsequences converging to every point in the infinite set $\{1,1 / 2,1 / 3,1 / 4,1 / 5, \ldots\},$ and no subsequences converging to points outside of this set.

**Proof.**

(a) Impossible by Bolzano-Weierstrass Theorem.

(b) Consider the sequence given by
$$
a_n =  
\begin{cases}
\frac{1}{n+1} & \text{if n is odd} , \\
1 - \frac{1}{n + 1} & \text{if n is even}.
\end{cases}
$$
Then $a_{2n} \to 1$ and $a_{2n-1} \to 0$.

(c) Consider the sequence 
$$
1 \\
1, \frac{1}{2} \\
1, \frac{1}{2}, \frac{1}{3}\\
1, \frac{1}{2}, \frac{1}{3}, \\
\cdots \\
1,\frac{1}{2}, \frac{1}{3} , \cdots, \frac{1}{n}, \\
\cdots.
$$
(d) Impossible. Because there must exist a subsequence who converges to zero while zero is not in this set.

> **Exercise 2.5.2.** Decide whether the following propositions are true or false, providing a short justification for each conclusion.
> (a) If every proper subsequence of $\left(x_{n}\right)$ converges, then $\left(x_{n}\right)$ converges as well.
> (b) If $\left(x_{n}\right)$ contains a divergent subsequence, then $\left(x_{n}\right)$ diverges.
> (c) If $\left(x_{n}\right)$ is bounded and diverges, then there exist two subsequences of $\left(x_{n}\right)$ that converge to different limits.
> (d) If $\left(x_{n}\right)$ is monotone and contains a convergent subsequence, then $\left(x_{n}\right)$ converges.

**Proof.**

(a) True. Consider the proper subsequence $(x_{n+1})$, i.e., $(x_2, x_3, \cdots)$. If it converges, then $(x_n)$ also converges.

(b) True. Suppose $(x_n)$ converges, then all of its subsequence must be convergent, which contradicts the assumption. Hence $(x_n)$ diverges.

(c) True. Since $(x_n)$ is bounded, there exists a subsequence $(x_{n_k})$ which converges, say to $a$. Since $(x_n)$ diverges, by definition of convergence, there exists $\delta \gt 0$ such that for all $N \in \mathbf{N}$, there exists $n \gt N$ such that
$$
\vert x_{n_k} - a \vert \ge \delta.
$$
In particular, there exists a subsequence $(x_{m_k})$ such that
$$
\vert x_{m_k} - a \vert \ge \delta,
$$
for all $k \in \mathbf{N}$. As a subsequence of a bounded sequence, $(x_{m_k})$ is bounded and hence by Bolzano-Weierstrass Theorem it has a convergent subsequence $(x_{r_k})$. But because $\vert x_{r_k} - a \vert \ge \delta$ for all $k \in \mathbf{N}$, by Order Limit Theorem, we also have $\vert \lim x_{r_k} - a \vert \ge \delta$. Therefore, we have found two subsequences $(x_{m_k})$ and $(x_{r_k})$ converge to different limits.

(d) True. Assume $(x_n)$ is increasing and the subsequence $(x_{n_k})$ converges to $a$. Since $(x_{n_k})$ is increasing, we have $x_{n_k} \le a$ for all $k \in \mathbf{N}$. Moreover, for any $n \in \mathbf{N}$, we can find $k$ such that $n_k \gt n$, then
$$
x_n \le x_{n_k} \le a,
$$
i.e., $(x_n)$ is also bounded above by a.

Now, we show that $\lim x_n = a$.

Let $\epsilon \gt 0$ be given. Since $\lim x_{n_k} = a$, there exists $m$ such that for all $k \gt m$, we have 
$$
\vert x_{n_k} - a \vert \lt \epsilon.
$$
As $x_{n_k} \le a$, we have 
$$
- \epsilon \lt x_{n_k} - a \le 0.
$$
Then for any $l \gt n_{m+1}$, we have
$$
-\epsilon \lt x_{n_{m+1}} - a \le x_l - a \le 0.
$$
This implies
$$
\vert x_l - a \vert \le \epsilon.
$$
Hence $\lim x_n = a$, as desired.

> **Exercise 2.5.3. **(a) Prove that if an infinite series converges, then the associative property holds. Assume $a_{1}+a_{2}+a_{3}+a_{4}+a_{5}+\cdots$ converges to a limit $L$ (i.e., the sequence of partial sums $\left(s_{n}\right) \rightarrow L$ ). Show that any regrouping of the terms
> $$
> \left(a_{1}+a_{2}+\cdots+a_{n_{1}}\right)+\left(a_{n_{1}+1}+\cdots+a_{n_{2}}\right)+\left(a_{n_{2}+1}+\cdots+a_{n_{3}}\right)+\cdots
> $$
> leads to a series that also converges to $L$.
> (b) Compare this result to the example discussed at the end of Section 2.1 where infinite addition was shown not to be associative. Why doesn't our proof in (a) apply to this example?

**Proof.**

(a) Since the partial sum of the regrouping series $s_{n_k}$ is a subsequence of $s_n$, and $s_n$ converges to $L$, we have $s_{n_k}$ converges to $L$ as well.

(b) Becuase $\sum_{n=1}^{\infty}(-1)^n$ is not convergent, the condition does not hold.



> **Exercise 2.5.4.** The Bolzano-Weierstrass Theorem is extremely important, and so is the strategy employed in the proof. To gain some more experience with this technique, assume the Nested Interval Property is true and use it to provide a proof of the Axiom of Completeness. To prevent the argument from being circular, assume also that $\left(1 / 2^{n}\right) \rightarrow 0 .$ (Why precisely is this last assumption needed to avoid circularity?)

**Proof.**

Let $A$ be a non-empty bounded above set. 

Given $a_n \in A$ and an upper bound $M_n$ of $A$, let $x_n = \frac{1}{2}(a_n + M_n)$. If $x_n$ is an upper bound of $A$, then let $a_{n+1} = a_n$ and $M_{n+1} = x_n$. If not, choose $a_{n+1} \in [x_n, M_n]$ and let $M_{n+1} = M_n$. Now consider the intervals $I_n = [a_n, M_n]$. They are nested closed intervals and by Nested Interval Property, there exists at least one point $x \in \mathbf{R}$ contained in every $I_n$. Furthermore, $x$ is unique since the length of $I_n = \frac{(M_1 - a_1)}{2^{n-1}}$ converges to 0. It just remains to show $x = \sup A$.

To show $x$ is an upper bound of $A$, suppose there is some $a \in A$ such that $x \lt a$, then there is an $n$ such that $M_n \lt a$, which is impossible since $M_n$ is an upper bound of $A$. 

To show $x$ is the smallest upper bound, suppose there exists an upper bound $y \lt x$, then again there is an $n$ such that $a_n \gt y$, which is impossible.

Therefore, $x = \sup A$.

The assumption $(1/2^n) \to 0$ is needed here because Nested Interval Property does not imply Archimedean Property and we need the Archimedean Property to ensure $\left(1 / 2^{n}\right) \rightarrow 0$.



> **Exercise 2.5.5.** Assume $\left(a_{n}\right)$ is a bounded sequence with the property that every convergent subsequence of $\left(a_{n}\right)$ converges to the same limit $a \in \mathbf{R}$. Show that $\left(a_{n}\right)$ must converge to $a$.

**Proof.**

Assume the contrary that $(a_n)$ does not converge to $a$, then there exists $\epsilon \gt 0$ such that for all $N$, there is $n \gt N$ with $\vert a_n - a \vert \ge \epsilon$.

Now choose $n_1 \gt 0$ such that $\vert a_{n_1} - a \vert \ge \epsilon$. Next choose $n_2 \gt n_1$ such that $\vert a_{n_2} - a \vert \ge \epsilon$.

More precisely, assume we have already chosen $n_k$ such that $n_1 \lt n_2 \lt \cdots \lt n_k$ and $\vert a_{n_k} - a \vert \ge \epsilon$, then choose $n_{k+1}$ such that $\vert a_{n_{k+1}} - a \vert \ge \epsilon$.

Thus we have built a subsequence, but it's not necessarily convergent. However, since itself is a bounded sequence, it has a convergent subsequence by Bolzano-Weierstrass Theorem. This subsequence cannot converge to $a$, because each of its term $a_{n_{k_l}}$ satisfies $\vert a_{n_{k_l}} - a \vert \ge \epsilon$. We have reached a contradiction and hence $(a_n)$ must converge to $a$.



> **Exercise 2.5.6.** Use a similar strategy to the one in Example 2.5.3 to show $\lim b^{1 / n}$ exists for all $b \geq 0$ and find the value of the limit. (The results in Exercise 2.3.1 may be assumed.)

**Proof.**

If $b = 0$, then $b^{1/n} = 0$ for all $n$. Hence $\lim b^{1/n} = 0$.

If $b \ge 1$, then we have
$$
b \ge b^{1/2} \ge b^{1/3} \ge \cdots \ge b^{1/n} \ge \cdots \ge 1.
$$
Therefore, $(b^{1/n})$ is decreasing and bounded below. Hence by MCT, $\lim b^{1/n}$ exists. Let $\lim b^{1/n} = x$. By Order Limit Theorem, we also have $x \ge 1$.

Since $(b^{1/2n})$ is a subsequence of $(b^{1/n})$, then by Theorem 2.5.2, $\lim b^{1/2n} = x$.

Since $b^{1/2n}\cdot b^{1/2n} = b^{1/n}$, by Algebraic Limit Theorem, we have
$$
x^2 = x.
$$
Hence $x = 0$ or $x = 1$. But $x \ge 1$. Hence $x = 1$, i.e., $\lim b^{1/n}=1$.

If $b \le 1$, then $1/b \ge 1$. Hence $\lim (1/b)^{1/n} = 1$ by the above. Since $(1/b)^{1/n} = 1/b^{1/n}$, by Algebraic Limit Theorem, we have
$$
\lim b^{1/n} = \frac{1}{\lim (1/b)^{1/n}} = 1.
$$
Therefore $\lim b^{1/n} = 1$ if $b \neq 0$ and $\lim b^{1/n} = 0$ if $b = 0$.



> **Exercise 2.5.7.** Extend the result proved in Example 2.5.3 to the case $|b|<1 ;$ that is, show $\lim \left(b^{n}\right)=0$ if and only if $-1<b<1$.

**Proof.**

$(\Longrightarrow)$: suppose $\lim b^n = 0$. Then $\lim \vert b^n\vert = 0$. We argue by contradiction. Suppose otherwise $\vert b \vert \ge 1$, then
$$
1 \le \vert b \vert \le \vert b \vert^2 \le \vert b \vert^3 \le \cdots.
$$
Hence the sequence $(\vert b \vert^n)$ is increasing.

If it is not bounded, then $(\vert b \vert^n)$ diverges, contradicting with $\lim \vert b^n \vert = 0$.

If it is bounded, then by MCT, it converges. Moreover, by Order Limit Theorem, we have
$$
\lim \vert b^n \vert \ge 1,
$$
which again contradicts with $\lim \vert b^n \vert = 0$.

Therefore the assumption $\vert b \vert \ge 1$ is impossible. Hence $\vert b \vert \lt 1$.

$(\Longleftarrow)$: suppose $-1 \lt b \lt 1$, then $\vert b \vert \lt 1$. Then by Example 2.5.3, $\lim \vert b \vert^n = 0$ (it is clear that it is true for $b=0$). Since $\vert b \vert^n = \vert b^n \vert$, we also have $\lim \vert b^n \vert = \lim \vert b \vert^n = 0$. Moreover, 
$$
-\vert b^n \vert \le b^n \le \vert b^n \vert,
$$
by Squeeze Theorem, $\lim b^n = 0$.



> **Exercise 2.5.8.** Another way to prove the Bolzano-Weierstrass Theorem is to show that every sequence contains a monotone subsequence. A useful device in this endeavor is the notion of a peak term. Given a sequence $\left(x_{n}\right),$ a particular term $x_{m}$ is a peak term if no later term in the sequence exceeds it; i.e., if $x_{m} \geq x_{n}$ for all $n \geq m$
> (a) Find examples of sequences with zero, one, and two peak terms. Find an example of a sequence with infinitely many peak terms that is not monotone.
> (b) Show that every sequence contains a monotone subsequence and explain how this furnishes a new proof of the Bolzano-Weierstrass Theorem.

**Proof.**

(a) Zero peak term: $x_n = n$.

 One peak term: $x_1 = 2$ and $x_n = 1 - \frac{1}{n}$ for $n \ge 2$, then $x_1$ is the only peak term.

Two peak term: $x_1 = 2, x_2 = \frac{3}{2}$ and $x_n = 1 - \frac{1}{n}$ for $n \ge 3$, then $x_1$ and $x_2$ are peak terms.

Infinitely many peak terms that is not monotone: $x_n = (-1)^n (1 + \frac{1}{n})$.

(b) If the sequence $(x_n)$ has infinitely many peak terms, then take the subsequence of peak terms. It is clear this subsequence is decreasing and bounded by assumption. It follows from the MCT that this subsequence converges.

If the sequence $(x_n)$ has only finitely many peak terms. Let $x_N$ be the last peak term. Take $n_1 = N + 1$, since $x_{n_1}$ is not a peak term, there exists $n_2 \gt n_1$ such that $x_{n_2} \gt x_{n_1}$. Again since $x_{n_2}$ is not a peak term, there exists $n_3 \gt n_2$ such that $x_{n_3} \gt x_{n_2}$. Continuing this process, we find a subsequence $(x_{n_k})$ who is increasing. Since by assumption the subsequence is bounded, it follows from MCT that this subsequence converges.



> **Exercise 2.5.9.** Let $\left(a_{n}\right)$ be a bounded sequence, and define the set
> $S=\left\{x \in \mathbf{R}: x<a_{n}\right.$ for infinitely many terms $\left.a_{n}\right\}$
> Show that there exists a subsequence $\left(a_{n_{k}}\right)$ converging to $s=\sup S .$ (This is a direct proof of the Bolzano-Weierstrass Theorem using the Axiom of Completeness.)

**Proof.**

First note that $S$ is not empty since $(a_n)$ is bounded by some number $M \gt 0$ and we can choose $x = -M - 1$, which satisfies the condition that $x \lt a_n$ for infinitely man terms $a_n$.

Moreover, $S$ is bounded above since every element in $S$ is less than $M$. Hence by Axiom of Completeness, $\sup S$  exists. Denote $s = \sup S$. 

Since $s - \frac{1}{2}$ is not an upper bound of $S$, there exists $x_1 \in S$ such that 
$$
s - 1 \lt x_1.
$$
But by definition of $S$, there exists $a_{n_1}$ such that
$$
s - 1 \lt x_1 \lt a_{n_1}.
$$
Again, since $s - \frac{1}{2^2}$ is not an upper bound of $S$, there exists $n_2 \gt n_1$ such that 
$$
s - \frac{1}{2^2} \lt a_{n_2}.
$$
In general, we can always choose some $n_k \gt n_{k-1}$ such that 
$$
s - \frac{1}{2^k} \lt a_{n_k}.
$$
We will show this subsequence $(a_{n_k})$ converges to $s$. Suppose not, then there exists some $\epsilon \gt 0$ such that for all $N \in \mathbf{N}$ there exists a $k \ge N$ such that 
$$
\vert a_{n_k} - s \vert \gt \epsilon.
$$
So there exists a subsequence of $(a_{n_k})$ such that no term is contained in $[s - \epsilon, s + \epsilon]$. Moreover, by the construction of $(a_{n_k})$, there exists some $N \in \mathbf{N}$ such that
$$
s - \epsilon \lt s - \frac{1}{2^N} \le s - \frac{1}{2^k} \lt a_{n_k},
$$
for all $k \ge N$.  This means $a_{n_k}$ is contained in $(s-\epsilon, \infty)$ for large enough $k$.

Therefore, we can find a subsequence of $(a_{n_k})$ that each term is contained in $(s + \epsilon, \infty)$. This implies $s + \epsilon \in S$, which contradicts the fact that $s = \sup S$. Hence the sequence $(a_{n_k})$ converges to $s$.



##  Exercises of 2.6 The Cauchy Criterion

> **Exercise 2.6.1.** Supply a proof for Theorem 2.6.2.

**Proof.**

Let $\epsilon \gt 0$ be given. Then since $(x_n)$ converges to $x$, there exists $N\in \mathbf{N}$ such that $\vert x_n - x \vert \lt \frac{\epsilon}{2}$, for every $n \ge N$. Then, for every $n, m \ge N$, we have
$$
\vert x_n - x_m \vert \le \vert x_n - x \vert + \vert x - x_m \vert \lt \epsilon.
$$
Hence $(x_n)$ is Caucy.



> **Exercise 2.6.2.** Give an example of each of the following, or argue that such a request is impossible.
> (a) A Cauchy sequence that is not monotone.
> (b) A Cauchy sequence with an unbounded subsequence.
> (c) A divergent monotone sequence with a Cauchy subsequence.
> (d) An unbounded sequence containing a subsequence that is Cauchy.

**Proof.**

(a) For example, $x_n = (-1)^n (\frac{1}{n})$.

(b) Impossible since Cauchy sequence is bounded.

(c) Impossible. If a monotone sequence has a Caucy subsequence, then such a sequence has a convergent sequence. By **Exercise2.5.2(d)** this sequence converges.

(d) For example, $x_n = (1, 0, 2, 0, 3, 0, \cdots)$.



> **Exercise 2.6.3.** If $\left(x_{n}\right)$ and $\left(y_{n}\right)$ are Cauchy sequences, then one easy way to prove that $\left(x_{n}+y_{n}\right)$ is Cauchy is to use the Cauchy Criterion. By Theorem 2.6.4, $\left(x_{n}\right)$ and $\left(y_{n}\right)$ must be convergent, and the Algebraic limit Theorem then implies $\left(x_{n}+y_{n}\right)$ is convergent and hence Cauchy.
> (a) Give a direct argument that $\left(x_{n}+y_{n}\right)$ is a Cauchy sequence that does not use the Cauchy Criterion or the Algebraic limit Theorem.
> (b) Do the same for the product $\left(x_{n} y_{n}\right)$.

**Proof.**

(a) Let $\epsilon \gt 0$ be given, then there exists $N_1, N_2 \in \mathbf{N}$ such that 
$$
\vert x_n - x_m \vert \lt \frac{\epsilon}{2},
$$
for every $n, m \ge N_1$ and 
$$
\vert y_n - y_m \vert \lt \frac{\epsilon}{2},
$$
for every $n, m \ge N_2$.

Let $N = \max\{N_1, N_2\}$. For all $n, m \ge N$, by the triangle inequality we have
$$
\begin{aligned}
\left|\left(x_{n}+y_{n}\right)-\left(x_{m}+y_{m}\right)\right| &=\left|\left(x_{n}-x_{m}\right)+\left(y_{n}-y_{m}\right)\right| \\
& \leqslant\left|x_{n}-x_{m}\right|+\left|y_{n}-y_{m}\right| \\
&<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon.
\end{aligned}
$$
Hence $(x_n + y_n)$ is a Cauchy sequence.

(b) Let $\varepsilon>0$ be arbitrary. Since $\left(x_{n}\right)$ and $\left(y_{n}\right)$ are Cauchy sequences, they are bounded. Hence there exist $M>0$ such that $\left|x_{n}\right|<M$ and $\left|y_{n}\right|<M$ for all $n \in \mathbf{N}$. Since $\left(x_{n}\right)$ and $\left(y_{n}\right)$ are Cauchy sequences, there exist $N_{1}, N_{2} \in \mathbf{N}$ such that
$$
\left|x_{n}-x_{m}\right|<\frac{\varepsilon}{2 M},
$$
for all $n, m>N_{1}$ and
$$
\left|y_{n}-y_{m}\right|<\frac{\varepsilon}{2 M},
$$
for all $n, m>N_{2}$
Let $N=\max \left\{N_{1}, N_{2}\right\} .$ For all $n, m>N,$ then by triangle inequality we have
$$
\begin{aligned}
\left|x_{n} y_{n}-x_{m} y_{m}\right| &=\left|x_{n} y_{n}-x_{m} y_{n}+x_{m} y_{n}-x_{m} y_{m}\right| \\
& \leqslant\left|x_{n} y_{n}-x_{m} y_{n}\right|+\left|x_{m} y_{n}-x_{m} y_{m}\right| \\
&=\left|y_{n}\right|\left|x_{n}-x_{m}\right|+\left|x_{m}\right|\left|y_{n}-y_{m}\right| \\
&<M \cdot \frac{\varepsilon}{2 M}+M \cdot \frac{\varepsilon}{2 M}=\varepsilon.
\end{aligned}
$$
Hence $\left(x_{n} y_{n}\right)$ is a Cauchy sequence.



> **Exercise 2.6.4.** Let $\left(a_{n}\right)$ and $\left(b_{n}\right)$ be Cauchy sequences. Decide whether each of the following sequences is a Cauchy sequence, justifying each conclusion.
> (a) $c_{n}=\left|a_{n}-b_{n}\right|$
> (b) $c_{n}=(-1)^{n} a_{n}$
> (c) $c_{n}=\left[\left[a_{n}\right]\right],$ where $[[x]]$ refers to the greatest integer less than or equal to $x$.

**Proof.**

(a) Notice that
$$
\Big\vert \vert a_n - b_n \vert- \vert a_m - b_m \vert \Big\vert \le \Big \vert (a_n-b_n) - (a_m - b_m) \Big \vert \le \Big\vert a_n - a_m \Big\vert + \Big\vert b_m - b_n \Big \vert.
$$
Hence $(c_n)$ is a Cauchy sequence.

(b) False. Counterexample: Let $a_n \equiv 1$, then $c_n = (-1)^n$ which is not a Cauchy sequence.

(c) False. Counterexample: Let $a_n = (-1)^n \frac{1}{n}$, then 
$$
c_n = 
\begin{cases}
0 , &\text{if} \; n \; \text{is even},  \\
-1 ,& \text{if} \; n \; \text{is odd}.
\end{cases}
$$
Therefore, $(c_n)$ diverges and hence not Cauchy.



> **Exercise 2.6.5.** Consider the following (invented) definition: A sequence $\left(s_{n}\right)$ is pseudo-Cauchy if, for all $\epsilon>0,$ there exists an $N$ such that if $n \geq N,$ then $\left|s_{n+1}-s_{n}\right|<\epsilon$
> Decide which one of the following two propositions is actually true. Supply
> a proof for the valid statement and a counterexample for the other.
> (i) Pseudo-Cauchy sequences are bounded.
> (ii) If $\left(x_{n}\right)$ and $\left(y_{n}\right)$ are pseudo-Cauchy, then $\left(x_{n}+y_{n}\right)$ is pseudo-Cauchy as well.

**Proof.**

(i) False.Counterexample: Let $(s_n)$ be the partial sum of the harmonic series:
$$
s_n = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n}.
$$
Let $\epsilon \gt 0 $ be given. Take $N \gt \frac{1}{\epsilon}$, then for all $n \gt N$, we have
$$
\vert s_{n+1} - s_n \vert = \frac{1}{n+1} \lt \frac{1}{N} \lt \epsilon.
$$
Hence $(s_n)$ is pseudo-Cauchy but not bounded.

(ii) True. Notice that by Triangular Inequality, we have
$$
\Big\vert (x_{n+1} + y_{n+1}) - (x_n + y_n) \Big\vert \le \Big\vert x_{n+1} - x_n \Big\vert + \Big\vert y_{n+1} - y_n \Big\vert.
$$

> **Exercise 2.6.6.** Let's call a sequence $\left(a_{n}\right)$ quasi-increasing if for all $\epsilon>0$ there exists an $N$ such that whenever $n>m \geq N$ it follows that $a_{n}>a_{m}-\epsilon$.
>
> (a) Give an example of a sequence that is quasi-increasing but not monotone or eventually monotone. 
>
> (b) Give an example of a quasi-increasing sequence that is divergent and not monotone.
>
> (c) Is there an analogue of the Monotone Convergence Theorem for quasi-increasing sequences? Give an example of a bounded, quasi-increasing sequence that doesn't converge, or prove that no such sequence exists.

**Proof.**

(a) First, notice that convergent sequences are quasi-increasing, so we want the sequence to oscillate. For example, let $a_n = (-1)^n(\frac{1}{n})$.

(b) Consider the sequence 
$$
a_n = 
\begin{cases}
n, & \text{when} \; n \; \text{is odd}, \\
a_{n-1} - \frac{1}{n}, & \text{when} \; n \; \text{is even.}
\end{cases}
$$
It's like a **zigzag increasing path** which diverges to infinity (since it has a subsequence that diverges). 

To see it is not monotone, notice that if $n$ is odd, then we have
$$
\begin{align}
a_n &= n,\\
a_{n+1} &= n - \frac{1}{n+1}, \\
a_{n+2} &= n + 2.
\end{align}
$$
Thus, $a_{n+1} \lt a_n \lt a_{n+2}$. Similarly, if $n$ is even, then
$$
\begin{align}
a_{n} &= n - 1 - \frac{1}{n}, \\
a_{n+1} &= n + 1, \\
a_{n+2} &= n + 1 - \frac{1}{n+2}.
\end{align}
$$
Thus, $a_n \lt a_{n+2} \lt a_{n+1}$.

In both cases, we see $(a_n)$ is not monotone.

To see it is quasi-increasing, we will first show 
$$
a_{n+k} \gt a_n,
$$
for every $k \gt 1$. 

If $n$ is odd, then $a_n = n$ and


$$
a_{n+k} =
\begin{cases}
n + k, & \text{if} \; k \; \text{is even}, \\
n + k - 1 - \frac{1}{n+k,} & \text{if} \; k \; \text{is odd}.
\end{cases}
$$
Thus $a_{n+k} \gt a_n$. 

If $n$ is even, then $a_n = n - 1 - \frac{1}{n}$ and
$$
a_{n+k} =
\begin{cases}
n + k - 1 - \frac{1}{n+k}, & \text{if} \; k \; \text{is even}, \\
n + k, & \text{if} \; k \; \text{is odd}.
\end{cases}
$$
Thus $a_{n+k} \gt a_n$ as well.

Therefore, we only need to consider two concecutive terms.

Given $\epsilon \gt 0$, choose $N \gt \frac{1}{\epsilon}$, then for every $m \ge N$ and $n = m+1$, we have

either
$$
a_n - a_m =  -\frac{1}{n} \gt -\frac{1}{N} \gt -\epsilon,
$$
if $n$ is even, or
$$
a_n - a_m = n - ((n - 2) - \frac{1}{n-1}) = 2 + \frac{1}{n-1} \gt -\epsilon
$$
 if $n$ is odd.

In both cases, $a_n \gt a_m -\epsilon$ holds and we are done.

(c) Yes, a bounded quasi-increasing sequence must be convergent. We prove by contradiction. Suppose $(a_n)$ is a bounded quasi-increasing sequence that diverges.

By **Exercise 2.5.2 (c)**, $(a_n)$ has two subsequences that converge to two different limits. We will denote these by $(a_{n_k})$ and $(a_{n_j})$, where $a_{n_k} \to a$ and $a_{n_j} \to b$, and we know $a \neq b$.

Without loss of generality, suppose that $a \gt b$. Let $\epsilon \gt 0$ such that $\epsilon \lt \frac{a-b}{3}$. This implies 
$$
a - b \gt 3 \epsilon \implies a -2\epsilon \gt b + \epsilon.
$$
Since $a_{n_k} \to a$, there exists some $K\in\mathbf{N}$ such that 
$$
\vert a_{n_k} - a \vert \lt \epsilon,
$$
for every $k \ge K$. In particular, 
$$
a - \epsilon \lt a_{n_k}.
$$
Since $(a_n)$ is quasi-increasing, there is some $N\in\mathbf{N}$ such that if $n \gt m \ge N$, then
$$
a_n \gt a_m - \epsilon,
$$
for the particular $\epsilon$ that we declared above.

Let $k\in\mathbf{N}$ be sufficiently large that $k \ge K$ and $n_k \ge N$, then we know 
$$
a_{n_k} \gt a - \epsilon.
$$
Let $j \in\mathbf{N}$ such that $n_j \gt n_k$. Then, by quasi-increasingness of the whole sequence $(a_n)$, since $n_j \gt n_k \ge N$, we know that
$$
a_{n_j} \gt a_{n_k} - \epsilon \gt a - 2\epsilon \gt b + \epsilon.
$$
In other words, after a certain point in the subsequence $(a_{n_j})$, the terms of of $(a_{n_j})$ stay bounded away from $b$ by a distance of at least $\epsilon$. This contradicts the assumption that $(a_{n_j})$ converges to $b$. Thus, $(a_n)$ must converge.



> **Exercise 2.6.7.** Exercises 2.4.4 and 2.5.4 establish the equivalence of the Axiom of Completeness and the Monotone Convergence Theorem. They also show the Nested Interval Property is equivalent to these other two in the presence of the Archimedean Property.
> (a) Assume the Bolzano-Weierstrass Theorem is true and use it to construct a proof of the Monotone Convergence Theorem without making any appeal to the Archimedean Property. This shows that BW, AoC, and MCT are all equivalent.
> (b) Use the Cauchy Criterion to prove the Bolzano-Weierstrass Theorem, and find the point in the argument where the Archimedean Property is implicitly required. This establishes the final link in the equivalence of the five characterizations of completeness discussed at the end of Section 2.6 .
> (c) How do we know it is impossible to prove the Axiom of Completeness starting from the Archimedean Property?

**Proof.**

(a) Assume $(a_n)$ is increasing and bounded above. 

Let $\epsilon \gt 0$ be given.

By BW, there is a subsequence $(a_{n_k})$ of $(a_n)$ that converges, say to $a$. Since the subsequence is also increasing, we have 
$$
a_{n_k} \le a,
$$
for every $k\in\mathbf{N}$ otherwise it will not converge to $a$. Then, by definition of convergent sequence, there exists $K \in \mathbf{N}$ such that 
$$
\vert a_{n_k} - a \vert \lt \epsilon, 
$$
for every $k \ge K$. Hence, we have
$$
a - \epsilon \lt a_{n_k} \le a,
$$
for every $k \ge K$.

Choose $N = n_K$, then for every $n \ge N$, there exist $k_1, k_2 \ge K$ such that 
$$
n_{k_1} \le n \lt n_{k_2}.
$$
Then 
$$
a - \epsilon \lt a_{n_{k_1}} \le a_n \le a_{n_{k_2}} \le a \lt a + \epsilon.
$$
This implies $\vert a_n - a \vert \lt \epsilon$ and we are done.

(b) This is pretty much like the proof in Theorem 2.5.5.

Let $(a_n)$ be a bounded sequence so that there exists $M \gt 0$ such satisfying $\vert a_n \vert \le M$ for all $n \in \mathbf{N}$. Bisect the closed interval $[-M, M]$ into two closed intervals $[-M, 0]$ and $[0, M]$. Now, it must be that at least one of these closed intervals contains an infinite number of the terms in the seuqnce $(a_n)$. Select a half for which this is the case and label that interval as $I_1$. Then, let $a_{n_1}$ be some term in the sequence $(a_n)$ satisfying $a_{n_1} \in I_1$.

Next, we bisect $I_1$ into closed intervals of equal length, and let $I_2$ be a half that again contains an infinite number of terms of the origin sequence. Because there are an infinite number of terms from $(a_n)$ to chose from, we can select an $a_{n_2}$ from the original sequence with $n_2 \gt n_1$ and $a_{n_2} \in I_2$. In general, we construct the closed interval $I_k$ by taking a half of $I_{k-1}$ containing an infinite number of terms of $(a_n)$ and then select $n_k \gt n_{k-1} \gt \cdots \gt n_2 \gt n_1$ so that $a_{n_k} \in I_k$.

We want to argue that $(a_{n_k})$ is a Cauchy sequence and hence convergent. To this end, notice that the length of $I_k$ is $\frac{M}{2^{k-1}}$, so given any $\epsilon \gt 0$, we can choose $ K\in\mathbf{N}$ such that $\frac{M}{2^{K-1}} \lt \epsilon$  (**by Archimedean Property!**) .Then for every $k, l \ge K$, we know $a_{n_k} \in I_k \subseteq I_K$ and $a_{n_l} \in I_l \subseteq I_K$, and hence
$$
\vert a_{n_k} - a_{n_l} \vert \lt \frac{M}{2^{K-1}} \lt \epsilon,
$$
as desired.

(c) To my understand, Archimedean Property only means $\mathbf{N}$ is unbounded in $\mathbf{R}$. It cannot capture two numbers whose distance is less than 1,  and hence cannot fill the gap between $\mathbf{Q}$ and $\mathbf{R}$. This is not rigorous though, and it is only my intuitive explanation.



## Exercises of 2.7 Properties of Infinite Series

> **Exercise 2.7.1.** Proving the Alternating Series Test (Theorem 2.7.7) amounts to showing that the sequence of partial sums
> $$
> s_{n}=a_{1}-a_{2}+a_{3}-\cdots \pm a_{n}
> $$
> converges. (The opening example in Section 2.1 includes a typical illustration of $\left.\left(s_{n}\right) .\right)$ Different characterizations of completeness lead to different proofs.
> (a) Prove the Alternating Series Test by showing that $\left(s_{n}\right)$ is a Cauchy
> sequence.
> (b) Supply another proof for this result using the Nested Interval Property (Theorem 1.4.1).
> (c) Consider the subsequences $\left(s_{2 n}\right)$ and $\left(s_{2 n+1}\right),$ and show how the Monotone Convergence Theorem leads to a third proof for the Alternating Series Test.

**Proof.**

(a) Note that $s_1 = a_1 \ge 0$, and that $s_2 = a_1 - a_2 \ge 0$, and $s_2 \le s_1$.

For one more step, $s_3 = a_1 - a_2 + a_3 = s_2 + a_3 \ge s_2$, but also $s_3 = s_1 - (a_2 - a_3) \le s_1$. Thus
$$
0 \le s_2 \le s_3 \le s_1.
$$
In general, we can prove the following claims by induction:

1. All the partial sums $s_n$ of the series are non-negative.
2. All the partial sums are $\le$ the first term $a_1$.
3. The even-indexed partial sums form an increasing sequence.
4. The odd-indexed partial sums form a decreasing sequence.
5. Each even-indexed partial sum is $\le$ all the odd-indexed partial sums.

Now, to prove $(s_n)$ is Cauchy, let $\epsilon \gt 0$ be given. We want to find $N \in \mathbf{N}$ such that
$$
\vert s_n - s_m \vert = \vert a_{m+1} - a_{m+2} + a_{m+3} - \cdots \pm a_n \vert \lt \epsilon,
$$
for every $n \gt m \ge N$.

Apply (1) to the alternating series starting, not with $a_1$, but with $a_{m+1}$, the absolute value on the right-hand side of the above equation can be removed,
$$
\vert s_n - s_m \vert = a_{m+1} - a_{m+2} + a_{m+3} - \cdots \pm a_n
$$
Moreover, by viewing $\vert s_n - s_m \vert$ as the partial sum of an alternating series starting with $a_{m+1}$, we can apply (2) to get 
$$
\vert s_n - s_m \vert \le a_{m+1}.
$$
Now because $a_n$ decreases to 0, we can find $N \in \mathbf{N}$ such that $a_n \lt \epsilon$ for every $n \ge N$. Thus
$$
n \gt m \ge N \implies \vert s_n - s_m \vert \lt \epsilon,
$$
thus, the sequence of partial sums $(s_n)$ is Cauchy and therefore convergent.

(b) Define $I_n = [s_{2n}, s_{2n-1}]$, then by (3)-(5), we have a nested closed intervals
$$
I_1 \supseteq I_2 \supseteq I_3 \supseteq \cdots.
$$
By Nested Interval Property, there exists $L \in \cap_{k=1}^{\infty}I_k$, and since the length of $I_n$ is $\vert I_n\vert =s_{2n-1} - s_{2n} = a_{2n} \to 0$, we know $L$ is unique (prove by contradiction). Now, we only need to show $s_n \to L$.

Let $\epsilon \gt 0$ be given, there exists $N \in \mathbf{N}$ such that 
$$
\vert I_n \vert = s_{2n-1} - s_{2n} \lt \epsilon,
$$
for every $n \ge N$. Since $L$ is in the intersection of all $I_n$s, we have
$$
L \in I_n = [s_{2n}, s_{2n-1}],
$$
for every $n \ge N$. This implies
$$
\vert s_{2n} - L \vert \le \vert I_n \vert \lt \epsilon,
$$
and 
$$
\vert s_{2n-1} - L \vert \le \vert I_n \vert \lt \epsilon,
$$
for every $n \ge N$. Hence, $(s_{2n}) \to L$ and $(s_{2n-1}) \to L$, which implies $(s_n) \to L$.

(c) The sequence $(s_{2n})$ is inceasing and bounded above by every odd term of $(s_n)$, hence by MCT, it converges to a limit $L_1$. And the sequence $(s_{2n+1})$ is decreasing and bounded below by every even term of $(s_n)$, hence it converges to a limit $L_2$. Moreover, by Algebraic Limit Theorem, 
$$
L_2 - L_1 = \lim s_{2n+1} - \lim s_{2n} = \lim (s_{2n+1} - s_{2n}) = \lim a_{2n+1} = 0.
$$
Hence, $(s_{2n}) \to L$ and $(s_{2n-1}) \to L$, which implies $(s_n) \to L$.



> **Exercise 2.7.2.** Decide whether each of the following series converges or diverges:
> (a) $\sum_{n=1}^{\infty} \frac{1}{2^{n}+n}$
> (b) $\sum_{n=1}^{\infty} \frac{\sin (n)}{n^{2}}$
> (c) $1-\frac{3}{4}+\frac{4}{6}-\frac{5}{8}+\frac{6}{10}-\frac{7}{12}+\cdots$
> (d) $1+\frac{1}{2}-\frac{1}{3}+\frac{1}{4}+\frac{1}{5}-\frac{1}{6}+\frac{1}{7}+\frac{1}{8}-\frac{1}{9}+\cdots$
> (e) $1-\frac{1}{2^{2}}+\frac{1}{3}-\frac{1}{4^{2}}+\frac{1}{5}-\frac{1}{6^{2}}+\frac{1}{7}-\frac{1}{8^{2}}+\cdots$

**Proof.**

(a) Since 
$$
0 \le \frac{1}{2^n + n} \le \frac{1}{2^n},
$$
and $\sum_{n=1}^\infty\frac{1}{2^n}$ converges, by comparison test, $\sum_{n=1}^{\infty} \frac{1}{2^{n}+n}$ converges.

(b) Since
$$
0 \le \frac{\vert \sin(n) \vert}{n^2} \le \frac{1}{n^2},
$$
and $\sum_{n=1}^{\infty}\frac{1}{n^2}$ converges, by comparison test, $\sum_{n=1}^{\infty} \frac{\vert\sin (n)\vert}{n^{2}}$ converges. By Absolute Convergence Test, $\sum_{n=1}^{\infty} \frac{\sin (n)}{n^{2}}$ converges as well.

(c) This series can be written as $\sum_{n=1}^{\infty}(-1)^{n+1}(\frac{n+1}{2n})$, and beacuse $(-1)^{n+1}(\frac{n+1}{2n})$ does not converge to 0, the series diverges.

(d) If the series converges, then the partial sum sequence $(s_n)$ is bounded. However, observe that $s_4 \gt 1 + \frac{1}{4}$, $s_7 \gt 1 + \frac{1}{4} + \frac{1}{7}$, and in general
$$
s_{3m+1} \gt \sum_{k=0}^{m}\frac{1}{3k+1}.
$$
Since $\sum_{k=0}^{\infty} \frac{1}{3 k+1}$ diverges, this shows that $(s_n)$ is not bounded, so the series diverges.

(d) The series can be written as $\sum_{n=1}^{\infty}[\frac{1}{2n-1} - \frac{1}{(2n)^2}]$. It cannot be convergent otherwise we would have
$$
\begin{align}
\sum_{n=1}^{\infty}\frac{1}{2n-1} 
&= \sum_{n=1}^{\infty}\left[\frac{1}{2n-1} - \frac{1}{(2n)^2} + \frac{1}{(2n)^2}\right] \\
&= \sum_{n=1}^{\infty}\left[\frac{1}{2n-1} - \frac{1}{(2n)^2}\right] + \sum_{n=1}^{\infty}\frac{1}{(2n)^2}
\end{align}
$$
is convergent, which is a contradiction. Hence, the series diverges.



> **Exercise 2.7.3.** (a) Provide the details for the proof of the Comparison Test (Theorem 2.7.4) using the Cauchy Criterion for Series.
> (b) Give another proof for the Comparison Test, this time using the Monotone Convergence Theorem.

**Proof.**

(a) Let $\epsilon \gt 0$ be given, then from the Cauchy Criterion for Series, there exists $N \in \mathbf{N}$ such that 
$$
\vert b_{m+1} + b_{m+2} + \cdots + b_n \vert \lt \epsilon,
$$
for every $n \gt m \ge N$. But
$$
\vert a_{m+1} + a_{m+2} + \cdots + a_n \vert \le \vert b_{m+1} + b_{m+2} + \cdots + b_n \vert
$$
since $0 \le a_k \le b_k$ for all $k \in \mathbf{N}$, it follows that
$$
\vert a_{m+1} + a_{m+2} + \cdots + a_n \vert \lt \epsilon.
$$
Therefore, $\sum_{k=1}^{\infty}a_k$ converges.

(b) Since $\sum_{k=1}^{\infty}b_k$ converges, the partial sum sequence $(s_n)$ is bounded. But
$$
0 \le a_k \le b_k,
$$
for every $k \in \mathbf{N}$, the partial sum sequence $(s_{n}^{\prime})$ of $\sum_{k=1}^{\infty}a_k$ is  bounded above. Moreover, $(s_{n}^{\prime})$ is increasing since $a_k$ is non-negative. By MCT, $(s_n^{\prime})$ converges and hence $\sum_{k=1}^{\infty}a_k$ converges.



> **Exercise 2.7.4.** Give an example of each or explain why the request is impossible referencing the proper theorem(s).
> (a) Two series $\sum x_{n}$ and $\sum y_{n}$ that both diverge but where $\sum x_{n} y_{n}$ converges.
> (b) A convergent series $\sum x_{n}$ and a bounded sequence $\left(y_{n}\right)$ such that $\sum x_{n} y_{n}$ diverges.
> (c) Two sequences $\left(x_{n}\right)$ and $\left(y_{n}\right)$ where $\sum x_{n}$ and $\sum\left(x_{n}+y_{n}\right)$ both converge but $\sum y_{n}$ diverges.
> (d) A sequence $\left(x_{n}\right)$ satisfying $0 \leq x_{n} \leq 1 / n$ where $\sum(-1)^{n} x_{n}$ diverges.

**Proof.**

(a) Let $\sum x_n = \sum\frac{1}{n}$ and $\sum y_n = \sum \frac{1}{n}$, but $\sum x_n y_n = \sum \frac{1}{n^2}$ converges.

(b) Let $\sum x_n = \sum (-1)^{n+1}\frac{1}{n}$ and $y_n = (-1)^{n+1}$, but $\sum x_n y_n = \sum\frac{1}{n}$ diverges.

(c) Impossible, by Algebraic Limit Theorem for Series, 
$$
\sum y_n = \sum((x_n + y_n) - x_n) = \sum (x_n + y_n) - \sum x_n
$$
is convergent.

(d) Let $(x_n) = (0, 1/2, 0, 1/4, 0, 1/6, \cdots)$, then clearly $0\le x_n \le 1/n$. Note that $(2x_n)=(0, 1, 0, 1/2, 0, 1/3,\cdots)$, so the series $\sum 2x_n$ diverges, which implies, by the Algebraic Limit Theorem, that $\sum x_n$ diverges as well. Note that $(-1)^n x_n = x_n$ , and therefore $\sum (-1)^n x_n$ diverges as well.



> **Exercise 2.7.5.** Now that we have proved the basic facts about geometric series, supply a proof for Corollary 2.4.7.

**Proof.**

Corollary 2.4.7 states:

> The series $\sum_{n=1}^{\infty}1/n^p$ converges if and only if $p \gt 1$.

Notice that 
$$
2^n \cdot \frac{1}{(2^n)^p} = 2^{(1-p)n} \lt 1 \iff p \gt 1,
$$
i.e.,  the geometric series $\sum 2^{(1-p)n}$ converges if and only if $p \gt 1$. By Cauchy Condensation Test, $\sum 1/n^p$ converges if and only if $p \gt 1$.

> **Exercise 2.7.6.** Let's say that a series subverges if the sequence of partial sums contains a subsequence that converges. Consider this (invented) definition for a moment, and then decide which of the following statements are valid propositions about subvergent series:
> (a) If $\left(a_{n}\right)$ is bounded, then $\sum a_{n}$ subverges.
> (b) All convergent series are subvergent.
> (c) If $\sum\left|a_{n}\right|$ subverges, then $\sum a_{n}$ subverges as well.
> (d) If $\sum a_{n}$ subverges, then $\left(a_{n}\right)$ has a convergent subsequence.

**Proof.**

(a) False. Let $a_n=1$ for all $n \in \mathbf{N}$, then the partial sum $s_n = n$. It is clear that no subsequence of $(s_n)$ converges since $(s_n)$ is not bounded. Hence $\sum a_n$ does not subverges .

(b) True. If $\sum a_n$ converges, then the partial sum sequence $(s_n)$ converges and hence bounded. By BW Theorem, it has a convergent subsequence.

(c) True. Note the partial sum sequence $(s_n)$ of $\sum \vert a_n \vert$ is increasing and it has a convergent subsequence. By **Exercise 2.5.2(d)**, $(s_n)$ converges. Hence $\sum \vert a_n \vert$ converges. By Absolute Convergence Test, $\sum a_n$ converges and hence subverges.

(d) False. Let $a_{2 n}=n$ and $a_{2 n-1}=-n,$ then the partial sum $s_{2 n}$ satisfies
$$
s_{2 n}=0.
$$
Therefore, $\sum a_{n}$ subverges. However, no subsequence of $\left(a_{n}\right)$ is bounded. Hence, no subsequence of $\left(a_{n}\right)$ is convergent.



> **Exercise 2.7.7.**  (a) Show that if $a_{n}>0$ and $\lim \left(n a_{n}\right)=l$ with $l \neq 0,$ then the series $\sum a_{n}$ diverges.
> (b) Assume $a_{n}>0$ and $\lim \left(n^{2} a_{n}\right)$ exists. Show that $\sum a_{n}$ converges.

**Proof.**

(a) Since $\lim (na_n) = l \neq0$, there exists $N \in \mathbf{N}$ such that 
$$
\vert n a_n - l \vert \lt l/2,
$$
for every $n \ge N$. This means 
$$
na_n \gt \frac{l}{2} \gt 0 \implies a_n \gt \frac{l}{2n} \gt 0,
$$
for every $n \ge N$. Since $\sum 1/n$ diverges, by comparison test, we know $\sum a_n$ diverges as well.

(b) Since $\lim n^2 a_n$ exists, the sequence $(n^2 a_n)$ is bounded, so there exists $M \gt 0$ such that
$$
0 \lt n^2 a_n \le M \implies 0 \lt a_n \lt \frac{M}{n^2}.
$$
Since $\sum \frac{1}{n^2}$ converges,  by comparison test, $\sum a_n$ converges.

> **Exercise 2.7.8.** Consider each of the following propositions. Provide short proofs for those that are true and counterexamples for any that are not.
>
> (a) If $\sum a_{n}$ converges absolutely, then $\sum a_{n}^{2}$ also converges absolutely.
> (b) If $\sum a_{n}$ converges and $\left(b_{n}\right)$ converges, then $\sum a_{n} b_{n}$ converges.
> (c) If $\sum a_{n}$ converges conditionally, then $\sum n^{2} a_{n}$ diverges.

**Proof.**

(a) True. Since $\sum a_n$ converges absolutely, $\lim \vert a_n \vert = 0$. Hence $(\vert a_n \vert)$ is bounded, so there exists $M \gt 0$ such that $\vert a_n \vert \le M$ for all $n \in \mathbf{N}$.

Since $\sum M\vert a_n \vert$ converges and $0 \le a_n^2 \le M \vert a_n \vert$, by comparison test, $\sum a_n^2$ converges.

(b) False. Let $a_n = b_n = \frac{(-1)^n}{\sqrt{n}}$, then $\sum a_n$ converges by alternating series test and $\lim b_n = 0$, but $\sum a_n b_n = \sum \frac{1}{n}$ diverges.

(c) True. We prove it by contradiction. Suppose $\sum n^2 a_n$ converges, then $\lim n^2 a_n = 0$ and hence $(n^2 a_n)$ is bounded. Thus there exists $M \gt 0$ such that $\vert n^2 a_n \vert \le M$, which implies
$$
\vert a_n \vert \le \frac{M}{n^2}.
$$
Since $\sum \frac{M}{n^2}$ converges, $\sum \vert a_n \vert$ converges as well by comparison test. However, this contradicts the fact that $\sum a_n$ converges conditionally. Hence $\sum n^2 a_n$ diverges.



> **Exercise 2.7.9 (Ratio Test).** Given a series $\sum_{n=1}^{\infty} a_{n}$ with $a_{n} \neq 0,$ the Ratio Test states that if $\left(a_{n}\right)$ satisfies
> $$
> \lim \left|\frac{a_{n+1}}{a_{n}}\right|=r<1
> $$
> then the series converges absolutely.
> (a) Let $r^{\prime}$ satisfy $r<r^{\prime}<1 .$ Explain why there exists an $N$ such that $n \geq N$ implies $\left|a_{n+1}\right| \leq\left|a_{n}\right| r^{\prime}$
> (b) Why does $\left|a_{N}\right| \sum\left(r^{\prime}\right)^{n}$ converge?
> (c) Now, show that $\sum\left|a_{n}\right|$ converges, and conclude that $\sum a_{n}$ converges.

**Proof.**

(a) Since $\lim \vert \frac{a_{n+1}}{a_n}\vert = r \lt 1$, there exists $N \in \mathbf{N}$ such that
$$
\bigg\vert \vert \frac{a_{n+1}}{a_n} \vert- r \bigg\vert \lt r^{\prime} - r,
$$
for every $n \ge N$. This implies for all $n \ge N$,
$$
\vert \frac{a_{n+1}}{a_n} \vert - r \lt r^{\prime}-r \implies \vert \frac{a_{n+1}}{a_n} \vert \lt r^{\prime}.
$$
Hence for all $n \ge N$, we have
$$
\vert a_{n+1} \vert \le r^{\prime} \vert a_n \vert.
$$
(b) Since $\vert r^{\prime} \vert \lt 1$, we have $\sum (r^{\prime})^n$ converges. Hence by Algebraic Limit Theorem, $\left|a_{N}\right| \sum\left(r^{\prime}\right)^{n}$ converges as well.

(c) By (a),  if $k \ge N$ , then we have
$$
\vert a_k \vert \le r^{\prime} \vert a_{k-1} \vert \le (r^{\prime})^2 \vert a_{k-2}\vert \le \cdots \le (r^{\prime})^{k-N} \vert a_N \vert.
$$
Since $\sum (r^{\prime})^n$ converges, there exists $N_1 \in \mathbf{N}$ such that 
$$
(r^{\prime})^{m+1} + \cdots + (r^{\prime})^n \lt  \frac{(r^{\prime})^N}{\vert a_N \vert} \epsilon,
$$
for every $n \gt m \ge N_1$.

Let $M = \max\{N, N_1\}$, then for every $n \gt m \ge M$, we have
$$
\begin{align}
\vert a_{m+1} \vert + \cdots + \vert a_n \vert 
&\le (r^{\prime})^{m+1-N}\vert a_N \vert + \cdots + (r^{\prime})^{n-N} \vert a_N \vert \\
&= \frac{\vert a_N \vert}{(r^{\prime})^N}((r^{\prime})^{m+1} + \cdots + (r^{\prime})^n) \\
&\lt \frac{\vert a_N \vert}{(r^{\prime})^N} \cdot \frac{(r^{\prime})^N}{\vert a_N \vert} \epsilon = \epsilon.
\end{align}
$$
Therefore, $\sum \vert a_n \vert$ is Cauchy and converges, which implies $\sum a_n$ converges.

> **Exercise 2.7.10 (Infinite Products).** Review Exercise 2.4.10 about infinite products and then answer the following questions:
> (a) Does $\frac{2}{1} \cdot \frac{3}{2} \cdot \frac{5}{4} \cdot \frac{9}{8} \cdot \frac{17}{16} \cdots$ converge?
> (b) The infinite product $\frac{1}{2} \cdot \frac{3}{4} \cdot \frac{5}{6} \cdot \frac{7}{8} \cdot \frac{9}{10} \cdots$ certainly converges. (Why?) Does it converge to zero?
> (c) In $1655,$ John Wallis famously derived the formula
> $$
> \left(\frac{2 \cdot 2}{1 \cdot 3}\right)\left(\frac{4 \cdot 4}{3 \cdot 5}\right)\left(\frac{6 \cdot 6}{5 \cdot 7}\right)\left(\frac{8 \cdot 8}{7 \cdot 9}\right) \cdots=\frac{\pi}{2}
> $$
> Show that the left side of this identity at least converges to something. (A complete proof of this result is taken up in Section 8.3)​

**Proof.**

Recall Exercise 2.4.10, it would be convenient to express the infinite product as
$$
\prod_{n=1}^{\infty}\left(1+a_{n}\right)=\left(1+a_{1}\right)\left(1+a_{2}\right) \cdots .
$$
(a) Yes. It is clear that $a_n = \frac{1}{2^{n-1}}$ and $\sum a_n$ converges, by Exercise 2.4.10 (b), $\prod_{n=1}^{\infty} (1 + a_n)$ converges.

(b) Because the sequence of partial products $(p_m)$ is decreasing and bounded below by 0, by MCT, it converges. 

To show it converges to 0, it suffices to show the product of their reciprocals diverges. Express the reciprocal as follows:
$$
\frac{2}{1} \cdot \frac{4}{3} \cdot \frac{6}{5} \cdots=\prod_{n=1}^{\infty}\left(1+a_{n}\right).
$$
Here $a_n = \frac{1}{2n-1}$ and $\sum a_n$ diverges. Hence, by Exercise 2.4.10(b), 
$$
\frac{2}{1} \cdot \frac{4}{3} \cdot \frac{6}{5} \cdots
$$
diverges to infinity. Therefore, the original infinite product series converges to 0.

(c) Yes. Since each term can be expressed as
$$
\frac{(2n)^2}{(2n-1)(2n+1)} = 1 + \frac{1}{4n^2-1},
$$
we have $a_n = \frac{1}{4n^2-1}$ and $\sum a_n$ converges. Hence by Exercise 2.4.10(b), the infinite product series converges.



> **Exercise 2.7.11.** Find examples of two series $\sum a_{n}$ and $\sum b_{n}$ both of which diverge but for which $\sum \min \left\{a_{n}, b_{n}\right\}$ converges. To make it more challenging, produce examples where $\left(a_{n}\right)$ and $\left(b_{n}\right)$ are strictly positive and decreasing.

**Proof.**

Consider the following example:
$$
a_n = (1, 0, 1/2, 0, 1/3, 0, 1/4, \cdots) = 
\begin{cases}
0,& \; \text{if} \; n \; \text{is even},\\
\frac{2}{n+1},& \; \text{if} \; n \; \text{is odd}.
\end{cases}\\
b_n = (0, 1, 0, 1/2, 0, 1/3, 0, 1/4, \cdots) = 
\begin{cases}
\frac{2}{n},& \; \text{if} \; n \; \text{is even},\\
0,& \; \text{if} \; n \; \text{is odd}.
\end{cases}
$$
Then $\sum a_n$ and $\sum b_n$ both diverge because $a_n$ and $b_n$ both contain the harmonic sequence as a subsequence. However, $\min\{a_n, b_n\} = 0$ for all $n \in \mathbf{N}$, hence $\sum \min\{a_n, b_n\}$ certainly converges.

For the challenge part, I take the example from: https://math.stackexchange.com/questions/12986/find-examples-of-two-series-sum-a-n-and-sum-b-n-both-of-which-diverge-but?noredirect=1&lq=1

Let 
$$
\sum a_n = \overline{\frac{1}{1^2}} + \frac{1}{2^2} + \overline{\frac{1}{3^2} + \frac{1}{3^2} + \frac{1}{3^2}} + \frac{1}{6^2} + \frac{1}{7^2} + \cdots + \frac{1}{14^2} + \overline{\frac{1}{15^{2}}+\frac{1}{15^{2}}+\cdots+\frac{1}{15^{2}}}+\cdots
$$
and 
$$
\sum b_n = \frac{1}{1^2} + \underline{\frac{1}{2^2}} + \frac{1}{3^2} + \frac{1}{4^2} + \frac{1}{5^2} + \underline{\frac{1}{6^2} +\frac{1}{6^2} + \cdots + \frac{1}{6^2} } + \frac{1}{15^2} + \frac{1}{16^2} + \cdots + \frac{1}{71^2} + \cdots.
$$
Notice that each group of repeated terms has a sum $S \ge \frac{1}{4}$, which implies neither the partial sums of $\sum a_n$ nor $\sum b_n$ is bounded and hence diverges. However, $\sum \min\{a_n, b_n\} = \sum \frac{1}{n^2}$ converges.



> **Exercise 2.7.12 (Summation-by-parts).** Let $\left(x_{n}\right)$ and $\left(y_{n}\right)$ be sequences, let $s_{n}=x_{1}+x_{2}+\cdots+x_{n}$ and set $s_{0}=0 .$ Use the observation that $x_{j}=s_{j}-s_{j-1}$ to verify the formula
> $$
> \sum^{n}_{j=m} x_{j} y_{j}=s_{n} y_{n+1}-s_{m-1} y_{m}+\sum^{n}_{j=m} s_{j}\left(y_{j}-y_{j+1}\right)
> $$

**Proof.**
$$
\begin{align}
\sum_{j=m}^{n}x_j y_j &= \sum_{j=m}^{n}(s_j - s_{j-1})y_j = \sum_{j=m}^n s_j y_j - \sum_{j=m}^{n}s_{j-1}y_j  \\
&= \sum_{j=m}^n s_j(y_j - y_{j+1}) + \sum_{j=m}^{n}s_j y_{j+1} - \sum_{j=m}^n s_{j-1}y_j \\
&= \sum_{j=m}^{n}s_j(y_j - y_{j+1}) + \sum_{j=m}^{n}s_j y_{j+1} - \sum_{j=m-1}^{n-1}s_j y_{j+1} \\
&= \sum_{j=m}^{n}s_j(y_j - y_{j+1}) + s_ny_{n+1} - s_{m-1}y_m.
\end{align}
$$

> **Exercise 2.7.13 (Abel's Test)**. Abel's Test for convergence states that if the series $\sum_{k=1}^{\infty} x_{k}$ converges, and if $\left(y_{k}\right)$ is a sequence satisfying
> $$
> y_{1} \geq y_{2} \geq y_{3} \geq \cdots \geq 0
> $$
> then the series $\sum_{k=1}^{\infty} x_{k} y_{k}$ converges.
> (a) Use Exercise 2.7.12 to show that
> $$
> \sum_{k=1}^{n} x_{k} y_{k}=s_{n} y_{n+1}+\sum_{k=1}^{n} s_{k}(y_{k}-y_{k+1}),
> $$
> where $ s_{n}=x_{1}+x_{2}+\cdots+x_{n}$.
>
> (b) Use the Comparison Test to argue that $\sum_{k=1}^{\infty} s_{k}\left(y_{k}-y_{k+1}\right)$ converges absolutely, and show how this leads directly to a proof of Abel's Test.

**Proof.**

(a) By Exercise 2.7.12, 
$$
\sum_{k=1}^n x_k y_k = s_n y_{n+1} - s_0 y_1 + \sum_{k=1}^ns_k(y_k - y_{k-1}) = s_{n} y_{n+1}+\sum_{k=1}^{n} s_{k}(y_{k}-y_{k+1}).
$$
(b) Since $\sum x_n$ converges, the partial sums $s_n$ of $\sum x_n$ is bounded, i.e., $\vert s_n \vert \le M$ for some $M \gt 0$. Then
$$
\vert s_k (y_k - y_{k+1}) \vert \le M \vert y_k - y_{k-1}\vert,
$$
for every $k \in \mathbf{N}$. 

Next we will show $\sum \vert y_n -y_{n-1}\vert$ converges. This is because its partial sums
$$
t_n = \vert y_1 - y_2\vert + \vert y_2 - y_3 \vert + \cdots + \vert y_n - y_{n+1}\vert = y_1 - y_{n+1},
$$
which converges to $y_1 - \lim y_n$ (note $y_n$ converges by MCT).

Thus by comparison test, $\sum_{k=1}^{\infty}s_k(y_k -y_{k+1})$ converges absolutely and hence converges. Moreover, $\lim (s_n y_{n+1})$ exists by Algebraic Limit Theorem. Therefore, the partial sums ($\sum_{k=1}^n x_k y_k$) converges.



> **Exercise 2.7.14 (Dirichlet's Test).** Dirichlet's Test for convergence states that if the partial sums of $\sum_{k=1}^{\infty} x_{k}$ are bounded (but not necessarily convergent $),$ and if $\left(y_{k}\right)$ is a sequence satisfying $y_{1} \geq y_{2} \geq y_{3} \geq \cdots \geq 0$ with $\lim y_{k}=0$ then the series $\sum_{k=1}^{\infty} x_{k} y_{k}$ converges.
> (a) Point out how the hypothesis of Dirichlet's Test differs from that of Abel's Test in Exercise $2.7 .13,$ but show that essentially the same strategy can be used to provide a proof.
> (b) Show how the Alternating Series Test (Theorem 2.7.7) can be derived as a special case of Dirichlet's Test.

**Proof.**

(a) Abel's test requires $\sum x_n$ converges, which is stronger than the requirement of Dirichlet's test for $\sum x_n$ only being bounded. However, it only needs $(y_n)$ being non-negative and decreasing while Dirichlet's test in addition needs $(y_n)$ to converge to 0.

To prove Dirichlet's test, notice that 
$$
\vert s_k (y_k - y_{k+1}) \vert \le M \vert y_k - y_{k-1}\vert,
$$
stills holds because the partial sums of $\sum x_n$ are bounded. $\sum \vert y_n - y_{n-1}\vert$ converges because $\lim y_n$ exists. Hence by comparison test, $\sum\vert s _k(y_k - y_{k+1})\vert$ converges and hence $\sum s_k(y_k - y_{k+1})$ converges.  Moreover, $\lim( s_ny_{n+1}) = 0$ because ($s_n$) is bounded and $\lim y_n = 0$.

Therefore, $\sum x_n y_n$ converges.

(b) Observing the alternating series $\sum_{n=1}^{\infty}(-1)^{n+1}a_n$, we can find that the partial sums of $\sum_{n=1}^{\infty}(-1)^{n+1}$ are bounded and $(a_n)$ decreasing to 0. Hence by Dirichlet's test, it converges.

## 2.8 Double Summations and Products of Infinite Series

> **Exercise 2.8.1.** Using the particular array $\left(a_{i j}\right)$ from Section 2.1, compute $\lim _{n \rightarrow \infty} s_{n n} .$ How does this value compare to the two iterated values for the sum already computed?

**Proof.**
$$
s_{nn} = -[2 - (\frac{1}{2})^{n-1}] \to -2, 
$$
as $n\to \infty$. However,
$$
\begin{align}
\sum_{i=1}^{\infty}\left(\sum_{j=1}^{\infty}a_{ij}\right) &= \sum_{i=1}^{\infty}(0) = 0,\\
\sum_{j=1}^{\infty}\left(\sum_{i=1}^{\infty} a_{i j}\right)&=\sum_{j=1}^{\infty}\left(\frac{-1}{2^{j-1}}\right)=-2.
\end{align}
$$

> **Exercise 2.8.2.** Show that if the iterated series
> $$
> \sum_{i=1}^{\infty} \sum_{j=1}^{\infty}\left|a_{i j}\right|
> $$
> converges (meaning that for each fixed $i \in \mathbf{N}$ the series $\sum_{j=1}^{\infty}\left|a_{i j}\right|$ converges to some real number $b_{i},$ and the series $\sum_{i=1}^{\infty} b_{i}$ converges as well $),$ then the iterated series
> $$
> \sum_{i=1}^{\infty} \sum_{j=1}^{\infty} a_{i j}
> $$
> converges.

**Proof.**

Since $\sum_{j=1}^{\infty} a_{ij}$ converges absolutely, $\sum_{j=1}^{\infty}a_{ij}$ converges. Denote $b_i^{\prime} = \sum_{j=1}^{\infty}a_{ij}$ and $b_i = \sum_{j=1}^{\infty}\vert a_{ij} \vert$, then
$$
-b_i = -\sum_{j=1}^{\infty}\vert a_{ij} \vert \le b_i^{\prime}=\sum_{j=1}^{\infty}a_{ij}  \le \sum_{j=1}^{\infty}\vert a_{ij} \vert = b_i.
$$
So
$$
0 \le \vert b_i^{\prime}\vert \le b_i.
$$
Since $\sum_{i=1}^{\infty}b_i$ converges, by comparison test, $\sum_{i=1}^{\infty}\vert b_i^{\prime}\vert$ converges as well and hence $\sum_{i=1}^{\infty}b_i^{\prime}$ converges as desired.



> **Theorem 2.8.1.** Let $\left\{a_{i j}: i, j \in \mathbf{N}\right\}$ be a doubly indexed array of real numbers. If
> $$
> \sum_{i=1}^{\infty} \sum_{j=1}^{\infty}\left|a_{i j}\right|
> $$
> converges, then both $\sum_{i=1}^{\infty} \sum_{j=1}^{\infty} a_{i j}$ and $\sum_{j=1}^{\infty} \sum_{i=1}^{\infty} a_{i j}$ converge to the same value. Moreover,
> $$
> \lim _{n \rightarrow \infty} s_{n n}=\sum_{i=1}^{\infty} \sum_{j=1}^{\infty} a_{i j}=\sum_{j=1}^{\infty} \sum_{i=1}^{\infty} a_{i j},
> $$
> where $s_{n n}=\sum_{i=1}^{n} \sum_{j=1}^{n} a_{i j}$.

**Proof.**

Define 
$$
t_{mn} = \sum_{i=1}^m\sum_{j=1}^n \vert a_{ij} \vert.
$$


> **Exercise 2.8.3.** (a) Prove that $\left(t_{n n}\right)$ converges.
> (b) Now, use the fact that $\left(t_{n n}\right)$ is a Cauchy sequence to argue that $\left(s_{n n}\right)$
> converges.

Proof of Exercise 2.8.3.

(a) Notice that
$$
t_{nn} = \sum_{i=1}^n\sum_{j=1}^n \vert a_{ij} \vert \le \sum_{i=1}^n \sum_{j=1}^{\infty}\vert a_{ij}\vert \le \sum_{i=1}^{\infty} \sum_{j=1}^{\infty}\vert a_{ij}\vert ,
$$
and $(t_{nn})$ is increasing, by MCT, $(t_{nn})$ converges.

(b) Notice that for any $n \gt m$, we have
$$
\begin{align}
\vert s_{nn} - s_{mm} \vert 
&= \left\vert \sum_{i=1}^m\sum_{j=m+1}^{n} a_{ij} + \sum_{i=m+1}^{n}\sum_{j=1}^{m} a_{ij}  + \sum_{i=m+1}^{n}\sum_{j=m+1}^{n} a_{ij}\right\vert \\
&\le \sum_{i=1}^m\sum_{j=m+1}^n\vert a_{ij} \vert +\sum_{i=m+1}^{n}\sum_{j=1}^{m} \vert a_{ij} \vert + \sum_{i=m+1}^{n}\sum_{j=m+1}^{n} \vert a_{ij} \vert \\
&= \vert t_{nn} - t_{mm} \vert.
\end{align}
$$
Since $(t_{nn})$ is a Cauchy sequence, the above deduction implies $(s_{nn})$ is also a Cauchy sequence and hence converges.



We can now set 
$$
S = \lim_{n \to \infty} s_{nn}.
$$
In order to prove the theorem, we must show that the two iterated sums converges to this same limit. We will first show that
$$
S = \sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{ij}.
$$
Because $\{t_{mn}: m, n \in \mathbf{N}\}$ is bounded above, we can let
$$
B = \sup\{t_{mn}:m, n \in \mathbf{N}\}.
$$

> **Exercise 2.8.4** (a) Let $\epsilon \gt 0$ be arbitrary and argue that there exists an $N_1 \in \mathbf{N}$ such that $m, n \ge N_1$ implies $B -\frac{\epsilon}{2}\lt t_{mn} \le B$.
>
> (b) Now, show that there exists an $N$ such that
> $$
> \vert s_{mn} - S \vert \lt \epsilon
> $$
> for all $m, n\ge N$.

Proof of Exercise 2.8.4.

(a) There exists $m_1, n_1 \in \mathbf{N}$ such that 
$$
B - \frac{\epsilon}{2} \lt t_{m_1 n_1} \le B.
$$
Let $N_1 = \max\{m_1, n_1\}$. Since $(t_{mn})$ is increasing both on $m$ and $n$, we have
$$
B - \frac{\epsilon}{2} \lt t_{m_1 n_1} \le t_{mn} \le B,
$$
for every $m, n \ge N_1$.

(b) Without loss of generality, let $n \gt m \ge N$, then
$$
\begin{align}
\vert s_{mn} - S \vert &= \vert s_{mn} - s_{mm} + s_{mm} - S  \vert \\
&\le \vert s_{mn} - s_{mm} \vert + \vert s_{mm} - S \vert \\
&= \left\vert \sum_{i=1}^m\sum_{j=m+1}^n a_{ij}\right\vert + \vert s_{mm} - S \vert \\
&\le \sum_{i=1}^m\sum_{j=m+1}^n \vert a_{ij}\vert + \vert s_{mm} - S \vert \\
&= \vert t_{mn} - t_{mm} \vert + \vert s_{mm} - S \vert.
\end{align}
$$
In part (a), if we take $m=n \ge N_1$, then both $t_{mm}$ and $t_{mn}$ are between $B - \frac{\epsilon}{2}$ and $B$, which implies 
$$
\vert t_{mn} - t_{mm} \vert \lt \frac{\epsilon}{2}.
$$
Because $(s_{nn})$ converges to $S$, we can pick $N_2 \in \mathbf{N}$ such that
$$
\vert s_{mm} - S \vert \lt \frac{\epsilon}{2},
$$
for every $m \ge N_2$.

Setting $N = \max\{N_1, N_2\}$, we can conclude that 
$$
\vert s_{mn} - S \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} =\epsilon,
$$
for every $n \gt m \ge N$.



For the moment, consider $m\in \mathbf{N}$ to be fixed and write $s_{mn}$ as 
$$
s_{m n}=\sum_{j=1}^{n} a_{1 j}+\sum_{j=1}^{n} a_{2 j}+\cdots+\sum_{j=1}^{n} a_{m j}.
$$
Our hypothesis guarantees that for each fixed row $i$, the series $\sum_{j=1}^{\infty}a_{ij}$ converges absolutely to some real number $r_i$.

> **Exercise 2.8.5.** (a) Show that for all $m \geq N$
> $$
> \left|\left(r_{1}+r_{2}+\cdots+r_{m}\right)-S\right| \leq \epsilon
> $$
> Conclude that the iterated sum $\sum_{i=1}^{\infty} \sum_{j=1}^{\infty} a_{i j}$ converges to $S$.
> (b) Finish the proof by showing that the other iterated sum, $\sum_{j=1}^{\infty} \sum_{i=1}^{\infty} a_{i j}$ converges to $S$ as well. Notice that the same argument can be used once it is established that, for each fixed column $j,$ the sum $\sum_{i=1}^{\infty} a_{i j}$ converges to some real number $c_{j}$.

Proof of Exercise 2.8.5.

(a) If we think of $m$ as fixed and $n$ as the limiting variable, then the Algebraic Limit Theorem can be applied to the finite number of components of 
$$
s_{m n}=\sum_{j=1}^{n} a_{1 j}+\sum_{j=1}^{n} a_{2 j}+\cdots+\sum_{j=1}^{n} a_{m j}
$$
to conclude that
$$
\lim_{n\to \infty}s_{mn} = r_1 + r_2 + \cdots + r_m.
$$
Moreover, if $m,n \ge N$, then we have
$$
-\epsilon \lt s_{mn} - S \lt \epsilon.
$$
Taking $n \to \infty$ and apply the Order Limit Theorem we find
$$
-\epsilon \le (r_1 + r_2 + \cdots + r_m) - S \le \epsilon,
$$
for every $m \ge N$. Hence, given any $\epsilon \gt 0$, we have produced an $N \in \mathbf{N}$ such that
$$
\vert (r_1 + r_2 + \cdots + r_m) - S \vert \le \epsilon,
$$
for every $m \ge N$. Therefore, $\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_{ij} = S$.

(b) It suffices to prove that $\sum_{i=1}^{\infty}\vert a_{ij}\vert$ converges. Recall that $b_i = \sum_{j=1}^{\infty}\vert a_{ij} \vert$, so 
$$
\vert a_{ij}\vert \le b_i,
$$
for $i, j \in \mathbf{N}$. Since $\sum_{i=1}^{\infty}b_i$ converges, by Comparison Test, $\sum_{i=1}^{\infty}\vert a_{ij}\vert$ converges.



One final common way of computing a double summation is to sum along diagonals where $i+j$ equals a constant. Given a doubly indexed array $\{a_{ij}:i, j \in \mathbf{N}\}$, let
$$
d_2 = a_{11}, d_3 = a_{12} + a_{21}, d_4 = a_{13} + a_{22} + a_{31},
$$
and in general set
$$
d_k = a_{1, k-1} + a_{2, k-2} + \cdots + a_{k-1, 1}.
$$
Then, $\sum_{k=2}^{\infty}d_k$ represents another reasonable way of summing over every $a_{ij}$ in the array.

> **Exercise 2.8.6.**  (a) Assuming the hypothesis-and hence the conclusion-of Theorem 2.8.1, show that $\sum_{k=2}^{\infty} d_{k}$ converges absolutely.
> (b) Imitate the strategy in the proof of Theorem 2.8.1 to show that $\sum_{k=2}^{\infty} d_{k}$ converges to $S=\lim _{n \rightarrow \infty} s_{n n}$.

**Proof.**

(a) Let $u_n = \sum_{k=1}^n \vert d_k \vert$, we need to show $(u_n)$ converges. But
$$
u_n = \sum_{k=1}^n\vert d_k \vert \le \sum_{i=1}^n\sum_{j=1}^n \vert a_{ij}\vert = t_{nn},
$$
for every $n \in\mathbf{N}$. Since $(t_{nn})$ converges and hence bounded, we see $(u_n)$ is bounded. Clearly $(u_n)$ is increasing and hence by MCT, it converges.

(b) Let $\epsilon \gt 0$ be given. We need to find $N$ such that $n\ge N$ implies $\vert \sum_{k=2}^{n}d_k - S \vert \lt \epsilon$. By hypothesis, $(s_{nn}) \to S$, so choose $N_1$ so that
$$
\vert s_{nn} - S \vert \lt \frac{\epsilon}{2},
$$
for all $n \ge N_1$.

We have also proved $(t_{nn})$ converges, so there exists $N_2$ such that
$$
\vert t_{nn} - t_{mm} \vert \lt \frac{\epsilon}{2},
$$
for all $n \gt m \ge N_2$.

Set $N = \max\{N_1, 2N_2\}$, then for $n \ge N$,
$$
\begin{aligned}
\left|\sum_{k=2}^{n} d_{k}-S\right| &=\left|\sum_{k=2}^{n} d_{k}-s_{n n}+s_{n n}-S\right| \\
& \leq\left|\sum_{k=2}^{n} d_{k}-s_{n n}\right|+\left|s_{n n}-S\right| \\
&<\left|\sum_{k=2}^{n} d_{k}-s_{n n}\right|+\frac{\epsilon}{2}.
\end{aligned}
$$
Because $n \ge 2N_2$, the partial sum $\sum_{k=1}^nd_k$ along diagonals contains every term in the square sum $s_{N_2N_2}$. It follows that
$$
\vert s_{nn} - \sum_{k=2}^n d_k \vert \le \vert t_{nn} - t_{N_2N_2}\vert \lt \frac{\epsilon}{2}.
$$
Putting it altogether, we have
$$
\left|\sum_{k=2}^{n} d_{k}-S\right|<\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon,
$$
for all $n \ge N$ and we can conclude that $\sum_{k=2}^{\infty}d_k =S$.



> **Exercise 2.8.7. ** Assume that $\sum_{i=1}^{\infty} a_{i}$ converges absolutely to $A,$ and $\sum_{j=1}^{\infty} b_{j}$ converges absolutely to $B$.
>
> (a) Show that the iterated sum $\sum_{i=1}^{\infty} \sum_{j=1}^{\infty}\left|a_{i} b_{j}\right|$ converges so that we may apply Theorem 2.8.1.
> (b) Let $s_{n n}=\sum_{i=1}^{n} \sum_{j=1}^{n} a_{i} b_{j},$ and prove that $\lim _{n \rightarrow \infty} s_{n n}=A B .$ Conclude
> that
> $$
> \sum_{i=1}^{\infty} \sum_{j=1}^{\infty} a_{i} b_{j}=\sum_{j=1}^{\infty} \sum_{i=1}^{\infty} a_{i} b_{j}=\sum_{k=2}^{\infty} d_{k}=A B
> $$
> where, as before, $d_{k}=a_{1} b_{k-1}+a_{2} b_{k-2}+\cdots+a_{k-1} b_{1}$

**Proof.**

(a) Let $\sum_{i=1}^{\infty}\vert a_i \vert = L$ and $\sum_{j=1}^{\infty}\vert b_j \vert = M$. Then for each fixed $i \in \mathbf{N}$, the Algebraic Limit Theorem allows us to write $\sum_{j=1}^{\infty}\vert a_i b_j \vert = \vert a_i \vert \sum_{j=1}^{\infty} \vert b_j \vert$. So
$$
\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}\vert a_i b_j \vert = \sum_{i=1}^{\infty}\left(\vert a_i \vert \sum_{j=1}^{\infty}\vert b_j \vert \right) = \sum_{i=1}^{\infty} (\vert a_i \vert \cdot M) = M \cdot \sum_{i=1}^{\infty} \vert a_i \vert =M L.
$$
(b) Note that
$$
\sum_{i=1}^{n}\sum_{j=1}^{n} a_{i} b_{j}  = \left(\sum_{i=1}^n a_i \right) \cdot \left(\sum_{j=1}^n b_j \right),
$$
thus by Algebraic Limit Theorem
$$
\lim_{n \to \infty} s_{nn} = A B.
$$
From part (a) we know that $\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}\vert a_i b_j \vert$ converges, so we can use Theorem 2.8.1 to conclude that
$$
\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}a_i b_j = \sum_{j=1}^{\infty}\sum_{i=1}^{\infty}a_i b_j = \sum_{k=2}^{\infty} d_k = \lim_{n \to \infty} s_{nn} = AB.
$$
 