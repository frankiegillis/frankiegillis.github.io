## From Metrics to Topologies

**Theorem 1.** Let $(X, d)$ and $(Y, d')$ be a metric spaces, and let $f \colon X \to Y$ be a function. Then, $f$ is continuous if and only if, for every open set $U \subseteq Y$, the set $f^{-1}(U)$ is open in $X$.

*Proof.* $(\Rightarrow)$ Suppose that $f$ is continuous, and let $U \subset Y$ be open. Pick any $x_0 \in f^{-1}(U)$. Since $U$ is open, we can find $\epsilon > 0$ such that the open ball $B_{d'}(f(x_0), \epsilon) \subseteq U$. Plugging this value of $\epsilon$ into our continuity definition for $f$, we find that there exists $\delta > 0$ such that, if $x \in X$ with $d(x, x_0) < \delta$, then $d'(f(x), f(x_0)) < \epsilon$. Therefore, for any $x \in B_d(x_0, \delta)$, we have $f(x) \in B_{d'}(f(x_0, \epsilon) \subseteq U$. It follows that $x \in f^{-1}(U)$, and so $B_d(x_0, \delta) \subseteq f^{-1}(U)$. Since $x_0$ was arbitrary, $f^{-1}(U)$ is open.

$(\Leftarrow)$ Now suppose that, for any open set $U \subseteq Y$, the set $f^{-1}(U)$ is open in $X$.
