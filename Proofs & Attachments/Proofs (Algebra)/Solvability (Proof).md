
Let $G = G_{0}\supset G_{1}\supset\cdots\supset G_{n}$ be an abelian tower of $G$, the general idea is to refine each $G_{i}\supset G_{i+1}$, it is equivalent to show that there exists a cyclic tower between $G_{i} / G_{i+1}$ and $\{\overline{e}\}$ since quotient is a group homomorphism, and by taking the inverse, we recover a cyclic tower between $G_{i}$ and $G_{i+1}$. By the fact that $G_{i} / G_{i+1}$ is abelian, we see that it's sufficient to prove that if $G$ is abelian, then $G$ admits a cyclic tower.
We use induction on the order of $G$. If order is $1$, then $G = \{e\}$ and the conclusion is obvious. Now suppose for $n\leq k$ the statement is true, then for $n=k+1$, let ${} x\neq e {}$ be an element of $G$, let $G' = G / X$, then there exists a cyclic refinement in $G'\supset \{\overline{e}\}$, we can recover a cyclic tower in $G\supset X$, and by adding the tail term $\{e\}$, we get the desired cyclic tower, and the proof is done. ^828192

---

$\Rightarrow$: Let $G = G_{0}\supset G_{1}\supset\cdots\supset G_{r} = \{e\}$ is a tower of groups with $G_{i+1}$ normal in $G_{i}$ and such that $G_{i} / G_{i+1}$ is abelian. Let $H_{i} = H\cap G_{i}$, then ${} H_{i+1} {}$ is normal in $H_{i}$, and since we have an embedding from $H_{i} / H_{i+1}$ to $G_{i} / G_{i+1}$, $H_{i} / H_{i+1}$ is abelian, then $H$ is solvable. Also, consider the tower $G / H = G_{0} / H\supset G_{1} / H\supset \cdots\supset G_{r} / H = \{\overline{e}\}$, would like to show that $(G_{i} / H) / (G_{i+1}/ H)$ is abelian. Consider the map $G\to (G_{i} / H) / (G_{i+1} / H)$, then the kernel of it contains $G_{i+1}$, then by [[007 Second Isomorphism Theorem#^22beed|Second Isomorphism Theorem]], there is a embedding between $G_{i} / G_{i+1}$ and $(G_{i} / H) / (G_{i+1} / H)$, then by assumption, $(G_{i} / H) / (G_{i+1} / H)$ is abelian, thus $G / H$ is solvable.
$\Leftarrow$: Let $G / H = K_{0}\supset K_{1}\supset\cdots\supset\overline{e}$ be an abelian tower of $G / H$, and $H\supset H_{1}\supset\cdots\supset e'$ be an abelian tower of $H$. Consider map $\varphi: G\to G / H$, then claim that $\varphi^{-1}(K_{0})\supset\varphi^{-1}(K_{1})\supset\cdots\supset H\supset H_{1}\supset\cdots\supset e'$ is an abelian tower of $G$. Indeed if we consider map $\varphi^{-1}(K_{i})\to K_{i}/K_{i+1}$, its kernel contains $\varphi^{-1}(K_{i+1})$, then by Second Isomorphism Theorem, there exists a embedding between $\varphi^{-1}(K_{i}) / \varphi^{-1}(K_{i+1})$ and $K_{i} / K_{i+1}$, then by assumption, $\varphi^{-1}(K_{i}) / \varphi^{-1}(K_{i+1})$ is abelian, then $G$ is solvable. ^8a5d14

---

The idea is to prove that if $H,N$ are two subgroups in $S_{n}$ such that $N\lhd H$, and if $H$ contains every $3$ - cycles, $H / N$ is abelian. Then $N$ must contain all $3$ - cycles. Then we suppose we have an abelian tower with $\{e\}$ at the end, then replace $N$ with $\{e\}$, and we conclude that $\{e\}$ contains all $3$ - cycles, which is absurd.
In order to prove our claim, pick distinct $i,j,k,r,s$, and let $\sigma = (i, j, k)$, $\tau = (k, r, s)$. By direct calculation, $\sigma\tau\sigma^{-1}\tau^{-1} = (r, k, i)$. Here, notice that since $H / N$ is abelian, $h_{1}Nh_{2}N = h_{2}Nh_{1}N$, which would implies $h_{1}h_{2}h_{1}^{-1}h_{2}^{-1}\in N$, then we can say that $N$ contains all arbitrary $3$ - cycles. ^17e40b

---

**Proof of Normality**: Since $u\lhd U$, then ${} (u\cap V)\lhd (U\cap V) {}$, similarly with $(U\cap v)\lhd (U\cap V)$. 

---

Let the two towers be ${} G = G_{0}\supset G_{1}\supset\cdots\supset G_{r} = \{e\} {}$ and ${} G = H_{0}\supset H_{1}\supset\cdots\supset H_{s} = \{e\} {}$. Then define ${} G_{i,j} = G_{i+1}(H_{j}\cap G_{i}) {}$, and the refined tower is $G = G_{1,1}\supset G_{1,2}\supset\cdots\supset G_{1,s-1}\supset G_{2}=G_{2,1}\supset G_{2, 2}\supset\cdots\supset G_{r-1, 1}\supset\cdots\supset G_{r-1, s-1}\supset \{e\}$, and normality is guaranteed by butterfly lemma. Similarly, define $H_{i, j} = H_{j+1}(H_{j}\cap G_{i})$, and the tower is defined identically. By directly applying butterfly lemma, the isomorphism is obtained. ^d057e0

---

The first statement is a consequence of the second. Assume we've already proved the second statement, then we prove one by induction. Suppose for order $< n$, we have $G$ solvable, then for $G$ of order $n$, since it has non-trivial center $H$, consider $G / H$, which by induction has a abelian tower ending with $\{\overline{e}\}$, then lift this tower back to $G$ by canonical map $G\to G / H$.
To prove the second statement, use the [[009 Group Action#^c623d1|class formula]], where the group action is $G$ acting on itself via conjugation, then $|G| = |H| + \sum\limits|\frac{G}{\text{Stab}_{G}(x)}|$, where the sum is taken over $x$ such that $|\frac{G}{\text{Stab}_{G}(x)}|\neq 1$ (recall that $x\in H$ if and only if the orbit of $x$ is $x$), then given $p$ divides $G$, then $p$ divides $|H|$, thus concluding the proof. ^cabe9e

---

This is a test test test test 