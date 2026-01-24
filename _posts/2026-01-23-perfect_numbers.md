## Even Perfect Numbers and the Euclid-Euler theorem

Let $a \in \mathbb{N}$. I denote the sum of the positive divisors of $a$ by $\sigma (a)$, so for example, $\sigma(6) = 1 + 2 + 3 + 6 = 12$. We call $a$ *perfect* if $\sigma(a) = 2a$, that is if $a$ is equal to the sum of its proper divisors. The purpose of this post is to prove the *Euclid-Euler theorem*, which completely characterises even perfect numbers. The inspiration for this post comes from a project sheet on the same theorem which is part of the MT4519 Number Theory course here at St Andrews.

**Theorem 1 (Eulid-Euler)** Let $a \in \mathbb{N}$ be even. Then $a$ is a perfect number if and only if $a$ can be written in the form $a = (2^{p-1}) (2^p - 1)$, where $2^p - 1$ is prime.

Throughout this post, I will assume the multiplicative property of $\sigma$: if $a$ and $b$ are coprime, then $\sigma(ab) = \sigma(a) \sigma(b)$. We begin by establishing a couple of basic facts about $\sigma$:

**Claim 1** For any $p \in \mathbb{N}$, we have $p$ is prime if and only if $\sigma(p) = p + 1$.

*Proof.* If $p \in \mathbb{N}$ is prime, then the positive divisors of $p$ are precisely $1$ and $p$. It follows that $\sigma(p) = p + 1$. Conversely, if $p > 1$ is not prime, then $p$ has some positive divisor $1 < d < p$, so $\sigma(p) \ge 1 + p + d > 1 + p$. Finally $\sigma(1) = 1 \ne 1 + 1$, so we are done. $\blacksquare$

**Claim 2** For any prime $p$ and $k \in \mathbb{N}$, we have

\[ \sigma(p^k) = \frac{p^{k+1} - 1}{p - 1}.\]

*Proof.* The set of positive divisors of the integer $p^k$ is precisely $\{ p^a \mid 0 \le k \le a \} = \{1, p, p^2, \dots, p^k\}$, so it follows that

\[ sigma(p^k) = 1 + p + p^2 + \dots + p^k = \frac{p^{k+1} - 1}{p-1},\]

as claimed. $\blacksquare$

**Claim 3** For any coprime $a$, $b \in \mathbb{N}$, we have $\sigma(ab) = \sigma(a) \sigma(b)$; that is, $\sigma$ is a multiplicative function.

*Proof.* 

Having collected these facts, we are in a good position to approach the proof of **Theorem 1**.

*Proof of Theorem 1.* We will first prove the converse, which was known by Euclid. Suppose that $a = (2^{p-1})(2^p - 1)$, where $2^p - 1$ is prime. Since $a$ is even, we may assume that $p \ge 2$. First, notice that $2^{p-1}$ and $2^p - 1$ are coprime: this is true since the only prime dividing $2^{p - 1}$ is $2$, meanwhile $2^p - 1$ is odd so has no factor of $2$. Therefore,

$$ \sigma (a) = \sigma(2^{p-1}) \sigma(2^p - 1) = (2^p - 1)(2^p) = 2 \cdot (2^{p-1})(2^p - 1) = 2a $$

so $a$ is perfect.

The forward direction was not known by Euclid: it was proven by Euler in the 18th Century. The proof I will give here uses similar elementary means to the converse direction.

Suppose $a$ is an even perfect number. By the Fundamental Theorem of Arithmetic, we can write $a$ uniquely as $a = 2^k x$, for some natural number $k$ and odd number $x$. Notice that $2^k$ and $x$ are coprime, so $\sigma(a) = \sigma (2^k) \sigma(x) = (2^{k+1} - 1) \sigma(x)$ by the multiplicative propery of $\sigma$, and using Claim 2. By assumption, $a$ is a perfect number, so $\sigma(a) = 2a = 2^{k+1} x$. It follows that

$$ (2^{k+1} - 1) \sigma(x) = 2^{k+1} x,$$

and so $\sigma(x) = 2^{k+1} y$, where

$$ y = \frac{x}{2^{k+1} - 1}. $$

By rearranging this definition of $y$, we can obtain the equation $x = y (2^{k + 1} - 1) = 2^{k+1} y - y = \sigma(x) - y$, which leads us to $\sigma(x) = x + y$. We now argue that $y \mid x$. This is true by virtue of the fact that $x = y(2^{k+1} - 1)$. Moreover, $y < x$ because $2^{k + 1} - 1 > 1$. Suppose for a contradiction that $y > 1$. Then $\sigma(x) \ge 1 + y + x > x + y$, which gives the contradiction we wanted. It follows that $y = 1$, and so $\sigma(x) = x + 1$, therefore $x$ is prime by Claim 1.

From this, it follows that $a$ can be written in the form $(2^{p-1})(2^p - 1)$, where $2^p - 1$ is prime, as claimed. $\blacksquare$

Famously, not much is known about odd perfect numbers. It is not even known whether they exist. It is also not known whether there are infinitely many perfect numbers: by virtue of the Euclid-Euler theorem, this is equivalent to knowing whether there are infinitely many Mersenne primes.

