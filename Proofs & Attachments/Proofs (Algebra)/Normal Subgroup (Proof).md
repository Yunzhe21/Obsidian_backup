
$H=f^{-1}(H')\leq G$, take $x\in G,\ h\in H$, prove that $xhx^{-1}\in H$
$f(xhx^{-1})=f(x)f(h)f(x)^{-1}\in H'$
Hence, $xhx^{-1}\in f^{-1}(H')$ ^d9419e

---

Since $\{e'\}\lhd G'\Longrightarrow ker(f)=f^{-1}(\{e^{-1}\})\lhd G$ ^cec921

---

First prove that $Z(G)\leq G$:
1). $e\in Z(G)$
2). If $z,z'\in Z(G)$, $zz'x=zxz'=xzz'\Longrightarrow zz'\in Z(G)$ 
3). If $z\in Z(G)$, WTS: $xz^{-1}=z^{-1}x$
	Take $x\in G$, $xz=zx\Longrightarrow x^{-1}xzx^{-1}=x^{-1}zxx^{-1}$ ^477648
Then, we prove normal subgroup
Now take $H\leq Z(G)$, then if $x\in G,\ z\in H$
$xz=zx\Longrightarrow xzx^{-1}=z\in H$, thus normal ^0bc35a

---

$G$ is commutative, then for arbitrary $x,y\in G$, $xy=yx$, which means $x$ is the center of $G$
If $G=Z(G)$, then obviously $G$ is commutative ^705713

---

"${} Z(GL_{n}(K))\supseteq\{\lambda I_{n}:\lambda\in K^{*}\} {}$": This part is obvious
"$Z(GL_{n}(K))\subseteq\{\lambda I_{n}\}:\lambda\in K^{*}$": The following is the proof. 
Without loss of generality, we prove the center for **all linear maps** belongs to $\{\lambda I_{n}, \lambda\in K\}$, after proving that, we restrict $\lambda$ to $K^{*}$. Suppose $XM=MX$, for $\forall X$, want to show that $M(x)=\lambda_{x}x$, which means that $x$ and $M(x)$ are linear dependent. If not, then we can obtain a basis $\{x, M(x), v_{1}, \dots, v_{n}\}$.
Define $S$ as $S(x)=v, S(M(x))=v, S(v_{1})=0, \dots, S(v_{n})=0$, this $S$ is a linear map.
$Sx=SMx=MSx=v$ , so ${} Mx$ and $x$ are linear dependent. (existence)
But we also need to prove that the $\lambda$ is independent of the $x$ we choose.
Choose a basis $\{v_{1}, \dots, v_{n}\}$,
$T(c_{1}v_{1}+\dots+c_{n}v_{n})=c_{1}b_{1}v_{1}+\dots +c_{n}b_{n}v_{n}$, but also
${} T(c_{1}v_{1}+\dots+c_{n}v_{n})=\lambda_{v}v=\lambda_{v}c_{1}v_{1}+\dots+\lambda_{v}c_{n}v_{n} {}$, then $b_{1}=\dots=b_{n}=\lambda_{v}$, since $b_{1}, \cdots, b_{n}$ are independent of $x$, so the proof is done. ^8a7dfb

---

