
Since $v_{p}(x)>0$, $x=p^{n}k$, $n\in\mathbb{N}^{+}$, $\text{gcd}(k,x)=1$.
Since $v_{p}(u)=0$, $\text{gcd}(u, p)=1$. Write $u=pt+r$, where $t\in\mathbb{N}$ and $0<r<p$, then $x+u=p^{n}k+pt+r$, which implies that $p$ doesn't divide $x+u$. Hence $v_{p}(u+x)=0$. ^0f4e05

---

Consider the map $m_{g}: U\to gU$ as $u\mapsto gu$, the map is surjective for sure. If $gu_{1}=gu_{2}$, then $g^{-1}gu_{1}=g^{-1}gu_{2}\implies u_{1}=u_{2}$, which means that $m_{g}$ is injective. Hence $m_{g}$ is bijective. Since $U$ is a finite subgroup with cardinality $p^{m}$, $gU$ has cardinality $p^{m}$, which implies $gU\in\mathfrak{U}$. ^974644

---

Firstly, for all $U\in\mathfrak{U}$, $eU=\{eu, u\in U\}=U$.
Secondly, for all $g,h\in G$, $g(hU)=g\{hu: u\in U\}=\{g(hu): u\in U\}=\{ghu:u\in U\}$, also, $(gh)U=\{(gh)u:u\in U\}=\{ghu: u\in U\}$. Then $g(hU)=(gh)U$.
Hence it is a group action. ^715c78

---

$\text{Stab}_{G}(U)=\{g\in G: gU=U, U\in\mathfrak{U}\}$, then for all $g\in\text{Stab}_{G}(U)$, $gu\in U$. 
Consider $\text{Stab}_{G}(U)u=\{su, s\in\text{Stab}_{G}(U)\}\subseteq U$, then since the map ${} g\to gu$ is bijective,  $|\text{Stab}_{G}(U)|= |\{su: s\in\text{Stab}_{G}(U)\}|\leq |U|=p^{m}$. ^88c75f

---

If $|\text{Stab}_{G}(U)|=p^{m}$, then $v_{p}(|\text{Stab}_{G}(U)|)=v_{p}(p^{m})=m$.
Conversely, suppose that $v_{p}(|\text{Stab}_{G}(U)|)=m$, then $|\text{Stab}_{G}(U)|=p^{m}u$, where $u\in\mathbb{Z}$ and $\text{gcd}(u,p)=1$. Since $|\text{Stab}_{G}(U)|\leq p^{m}$, $|\text{Stab}_{G}(U)|=0$ or $p^{m}$. But $\text{Stab}_{G}(U)$ isn't empty, thus $|\text{Stab}_{G}(U)|=p^{m}$. ^f73276

---

If $v_{p}(|\text{Stab}_{G}(U)|)=m$. According to Orbit-Stabilizer Theorem, $|G|=|\text{Stab}_{G}(U)|\times |G.U|$. $v_{p}(|G.U|)=v_{p}\left (\frac{|G|}{|\text{Stab}_{G}(U)|}\right)=v_{p}\left(\frac{p^{m}a}{p^{m}u}\right)=v_{p}(a)-v_{p}(u)=v_{p}(a)$, since $\text{gcd}(u,p)=1$.
Conversely, suppose that $v_{p}(|G.U|)=v_{p}(a)$. Use Orbit-Stabilizer Theorem again, $|\text{Stab}_{G}(U)|=\frac{|G.U|}{|G|}$, then $v_{p}(|\text{Stab}_{G}(U)|)=v_{p}\left(\frac{|G.U|}{|G|}\right)$, then $v_{p}(|\text{Stab}_{G}(U)|)=v_{p}\left(\frac{p^{m}a}{a}\right)=m$. ^329ba3

---

$|\mathfrak{U}|=C^{p^{m}}_{p^{m}a}$, then by the definition of $\mathfrak{U}$. $v_{p}(|\mathfrak{U}|)=v_{p}(a)$. ^c2f6ac

---

$a\prod\limits_{j=1}^{p^{m}-1}\frac{\frac{p^{m}a-j}{p^{v_{p}(j)}}}{\frac{p^{m}-j}{p^{v_{p}(j)}}}=a\prod\limits_{j=1}^{p^{m}-1}\frac{p^{m}a-j}{p^{m}-j}=\prod\limits_{j=0}^{p^{m}-1}\frac{p^{m}a-j}{p^{m}-j}=C^{p^{m}}_{p^{m}a}$, then 
$v_{p}(C^{p^{m}}_{p^{m}a})=v_{p}(a)+\sum\limits_{j=1}^{p^{m}-1}v_{p}(p^{m}a-j)-\sum\limits_{j=0}^{p^{m}-1}v_{p}(p^{m}-j)$.
Consider $v_{p}(p^{m}-j)$, $j\in\{0, \cdots, p^{m}-1\}$. If $j=p^{k}$, $k\in\{0, \cdots, m-1\}$, then $v_{p}(p^{m}-j)=v_{p}(p^{k}(p^{m-k}-1))=v_{p}(p^{k})=k$.
If $j=0$, $v_{p}(p^{m}-j)=m$. Otherwise, $j\in (0,p^{1})\cup\cdots\cup(p^{m-1},p^{m}-1], j\in\mathbb{N}$, in this case, $\text{gcd}(p,p^{m}-j)=0$ implies $v_{p}(p^{m}-j)=0$.
Similarly with $v_{p}(p^{m}a-j)$. Hence, $v_{p}(C^{p^{m}}_{p^{m}a})=v_{p}(a)+(1+2+\cdots+m)-(1+2+\cdots+m)=v_{p}(a)$ ^108ef1

---

$|G|=p^{m}a=p^{m+r}u$, where $\text{gcd}(p,u)=1$. According to the Orbit-Stabilizer Theorem, $|G.\omega|\cdot|\text{Stab}_{G}(\omega)|=|G|$ for all $\omega\in\mathfrak{U}$, then $v_{p}(|G.\omega|)+v_{p}(|\text{Stab}_{G}(\omega)|)=v_{p}(|G|)=m+r$. Suppose there is no $\omega\in\mathfrak{U}$ such that ${} \text{Stab}_{G}(\omega)=p^{m} {}$, then for each orbit $v_{p}(|G.\omega|)>r\implies |G.\omega|=p^{r+k}l$, so if we add these orbits up and take their $p$ - adic, we find that $v_{p}(|\mathfrak{U}|)>r$. But by previous lemma, we've already known that $v_{p}(|\mathfrak{U}|)=v_{p}(a)=r$, which leads to a contradiction. The statement is proved. ^0ce704

---

$egS_{0} = gS_{0}$
$h(gS_{0}) = (hg)S_{0}$, thus it's obviously a group action. ^910022

---

$\Leftarrow$: Take ${} h\in gS_{0}g^{-1} {}$, then write $h = gsg^{-1}$ for some ${} s\in S_{0} {}$, thus $hgS_{0} = gsg^{-1}gS_{0} = gS_{0}$.
$\Rightarrow$: Take ${} gS_{0}\in (G / S_{0})^{H} {}$, then for arbitrary $h\in H$, $hgS_{0} = gS_{0}$, then $hg\in gS_{0}$, then $hg = gs$ for some $s\in S_{0}$, thus $h = gsg^{-1}$, which implies that $H\leq gS_{0}g^{-1}$.  ^cce8e7

---

This is equivalent to prove that there exists $g\in G$ such that ${} gS_{0}\in (G / S_{0})^{H} {}$, which means that ${} (G / S_{0})^{H} {}$ is nonempty. By the fact that $|X^{K}| \equiv |X|\mod p$, where $K$ is a $p$ -group, ${} |(G / S_{0})^{H}|\equiv |G / S_{0}|\mod p {}$, but $|G / S_{0}| = a$, where $\gcd(a, p) = 1$, then $|(G / S_{0})^{H}|$ is nonempty. ^051d22

---

Notice that the action is transitive due to previous theorem, then by Orbit-Stabilizer Theorem, $G / \text{Stab}_{G}(S_{0})\sim \textbf{S}$, thus $n_{p}\big| |G|$. ^d8e193

---

It's obvious that $S_{0}\leq \text{Stab}_{G}(S) = G'$, also, $S\leq \text{Stab}_{G}(S)$ by simp, so $S\leq G'\leq G$, thus $|S_{0}| = |S| \big | |G'| \big | |G|$. Write $|G'| = p^{m}\times b$ where $\gcd(b, p) = 1$, so $S_{0}$ and $S$ are both Sylow $p$ - subgroup of $G'$. However, $G' = \{g\in G, gSg^{-1} = S\}$, then $S\lhd G'$, which by previous corollary, implies $S_{0} = S$. ^066a65

---

$|\textbf{S}^{S_{0}}|\equiv |\textbf{S}|\mod p$, then $n_{p}\equiv 1\mod p$. Combining with the fact that $n_{p}\big | |G| = p^{m}\cdot a$, $n_{p}$ divides $a$. ^850a4a

---
