
Firstly, $e_{\mathfrak{S}_{X}}=Id_{X}$, so $e_{\mathfrak{S}_{X}}x=Id_{X}(x)=x$
Secondly, $\varphi, \tau\in\mathfrak{S}_{X}$, $x\in X$: $(\varphi\circ\tau)x=\varphi\circ\tau(x)=\varphi(\tau(x))=\varphi(\tau x)$ ^a8b8d9

---

$x\sim x$ since $x=ex$ <font color="#ff0000">(reflectivity)</font>
$y=gx\Longrightarrow g^{-1}y=g^{-1}gx=x\Longrightarrow y\sim x$ <font color="#ff0000">(symmetry)</font>
If $x\sim y$ and $y\sim z$, then exists $g, g'\in G$ s.t. $y=gx, z=g'y\longrightarrow z=g'(gx)=(g'g)x\Longrightarrow x\sim z$ <font color="#ff0000">(transitivity)</font> ^505a5a

---

First, it's easy to see that $\varphi(g): X\to X$ is bijective with inverse map $\varphi(g^{-1})$, proof is by simple calculation and the definition of group action. Thus $\varphi(g)\in\mathfrak{S}_{X}$.
Moreover, $(\varphi(g)\cdot\varphi(h))(x)=\varphi(g)(\varphi(h)(x))=g\cdot(hx)=(gh)(x)=\varphi(gh)(x)$, then $\varphi\in Hom(G,\mathfrak{S}_{X})$. ^159ba7

---

If $v=0_{v}$, then $O_{0_{v}}=\{0_{v}\}$.
If $v\neq 0_{v}$, then claim: $O_{v}=V-\{0_{v}\}$.
Take arbitrary $w_{1}\neq 0\in V$, want to find a $g\in GL(V)$ such that $w_{1}=g(v)$. First complete $v$ into ${} (v, v_{2} \cdots, v_{n}) {}$ basis of $V$, $w_{1}$ into $\{w_{1}, \cdots, w_{n}\}$ basis fo $V$. Then from Linear Algebra, there exists a $g\in\mathscr{L}(V)$ such that $g(v)=w_{1}$. ^4878be

---

Take $i\in\{1,\cdots, n\}$, find $\sigma\in\mathfrak{S}_{n}$ such that $i=\sigma(1)$. If $i=1$, take $\sigma=I$, otherwise, take $\sigma=(1,i)$. ^098b1f

---

For $\sigma\in\mathfrak{S}_{n-1}$, define $\tilde{\sigma}$ by $\tilde{\sigma}(i)=\sigma(i)$ if ${} i\in\{1, \cdots, n-1\} {}$, and $\tilde{\sigma}(n)=n$. By our construction, $\tilde{\sigma}\in\text{Stab}_{\mathfrak{S}_{n}}(n)$. Now, we are left to check $\iota:\mathfrak{S}_{n-1}\to\text{Stab}_{\mathfrak{S}_{n}}(n)$ as $\sigma\mapsto\tilde{\sigma}$ is an isomorphism.
For $\sigma_{1},\sigma_{2}\in\mathfrak{S}_{n-1}$, consider $\iota(\sigma_{1}\sigma_{2})=\tilde{\sigma_{1}\sigma_{2}}$, when $i\in\{1, \cdots, n-1\}$, $\iota(\sigma_{1}\sigma_{2})(i)=\sigma_{1}\sigma_{2}(i)=\iota(\sigma_{1})\iota(\sigma_{2})(i)$; when $i=n$, then $\iota(\sigma_{1}\sigma_{2})(n)=\iota(\sigma_{1})\iota(\sigma_{2})(n)$, thus $\iota$ is indeed a homomorphism.
To prove surjectivity, pick any $\tilde{\sigma}\in\text{Stab}_{\mathfrak{S}_{n}}(n)$, then $\tilde{\sigma}\in\mathfrak{S}_{n}$ and $\tilde{\sigma(n)}=n$, then it is easy to reconstruct a $\sigma$.
For injectivity, from our construction of $\tilde{\sigma}$, the proof should be self-evident. ^1d853d

---

To prove well-define, we suppose that if $g\text{Stab}_{G}(x)=g'\text{Stab}_{G}(x)$, then there exists a $h\in\text{Stab}_{G}(x)$ such that $g'=gh$, hence $g'x=(gh)x=g(hx)=gx$. 
The map is clearly surjective by our construction of $\varphi_{x}$. Finally, $\varphi(g)=\varphi(g')\iff g'x=gx\iff$ 
$g^{-1}g'x=x\iff g^{-1}g'\in\text{Stab}_{G}(x)\iff g'\in g\text{Stab}_{G}(x)\iff g'\text{Stab}_{G}(x)=g\text{Stab}_{G}(x)$. ^e39246

---

If $X=X^{G}$, the proof is obvious.
Otherwise, note that $x\in X^{G}\iff G.x=\{x\}\iff |\text{Stab}_{G}(x)|=|G|\iff \text{Stab}_{G}(x)=G$. Write $X=\bigcup_{i=1}^{r}G.x_{i}$, and by reordering we suppose the first $r$ orbits has cardinality one, i.e. ${} X^{G}=\{x_{1}, \cdots, x_{s}\} {}$. Since by our assumption $X^{G}\subsetneq X$, we have $s<r$. By class formula, we write $|X|=\sum\limits_{i=1}^{r}|G.x_{i}|=s+\sum\limits_{i=s+1}^{r}|G.x_{i}|$, then we are left to prove that $\sum\limits_{i=s+1}^{r}|G.x_{i}|$ is a multiple of $p$. Since $|G.x_{i}|=\frac{|G|}{\text{Stab}_{G}(x_{i})}$, and by the fact that $\text{Stab}_{G}(x_{i})\leq |G|$ and thus a $p$ -group, then $|G.x_{i}|$ is a multiple of $p$. ^8b8753

---

Apply the previous theorem by setting $X=G$, and the group action as conjugation, we have $|G|\equiv |Z(G)|\text{ mod }p$. Hence $|Z(G)|\equiv 0\text{ mod }p$, so $|Z(G)|\neq 1$. ^5487f8

---

By previous corollary, center $Z(G)$ is not trivial, then Lagrange Theorem gives that $|Z(G)|=p$ or $p^2$. In the latter case, the proof is obvious. Suppose $|Z(G)|=p$, and take an element of $G$ that is not in $Z(G)$. Notice the centralizer $Z_{G}(x)$ contains $Z(G)$ as well as $x$, then $Z_{G}(x)$ properly contains $Z(G)$, then $|Z_{G}(x)|$ must equal to $p^2$, and therefore $Z(x)=G$. This means that $x$ commutes with all elements in $G$, which leads to a contradiction.  ^b48fac

---

