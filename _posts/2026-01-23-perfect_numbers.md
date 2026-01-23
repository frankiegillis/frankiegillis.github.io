## Even Perfect Numbers and the Euclid-Euler theorem

Let $a \in \mathbb{N}$. We denote the sum of the positive divisors of $a$ by $\sigma (a)$, so for example, $\sigma(6) = 1 + 2 + 3 + 6 = 12$. We call $a$ *perfect* if $\sigma(a) = 2a$, that is if $a$ is equal to the sum of its proper divisors. The purpose of this post is to prove the *Euclid-Euler theorem*, which completely characterises even perfect numbers. The inspiration for this post comes from a project sheet on the same theorem which is part of the MT4519 Number Theory course here at St Andrews.

**Theorem 1 (Eulid-Euler)** Let $a \in \mathbb{N}$ be even. Then $a$ is a perfect number if and only if $a$ can be written in the form $a = (2^{p-1}) (2^p - 1)$, where $2^p - 1$ is prime.

We will begin by establishing some basic facts about $\sigma$. Throughout, we will assume the multiplicative property of $\sigma$: if $a$ and $b$ are coprime, then $\sigma(ab) = \sigma(a) \sigma(b)$.

**Claim 1** For any $a \in \mathbb{N}$, we have $a$ is prime if and only if $\sigma(a) = a + 1$.
*Proof.* If $a \in \mathbb{N}$ is prime, then its positive divisors are precisely $1$ and $a$. Hence $\sigma(a) = a+1$. Conversely, if $a > 1$ is not prime, then $a$ has some positive divisor $d \ne 1, a$, so $\sigma(a) \ge 1 + a + d > 1 + a$. Finally $\sigma(1) = 1 \ne 2$. $\qed$



We will first prove the converse, which was known to Euclid. Suppose that $a = (2^{p-1})(2^p - 1)$, where $2^p - 1$ is prime. Since $a$ is even, we may assume that $p \ge 2$. First, notice that $2^{p-1}$ and $2^p - 1$ are coprime: this is true since the only prime dividing $2^{p - 1}$ is $2$, meanwhile $2^p - 1$ is odd so has no factor of $2$. Therefore,

$$ \sigma (a) = \sigma(2^{p-1}) \sigma(2^p - 1) = (2^p - 1)(2^p) = 2 \cdot (2^{p-1})(2^p - 1) = 2a $$

so $a$ is perfect.


