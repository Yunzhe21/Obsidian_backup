
If $Hx=Hx'$, then $i(x)H=i(Hx)=i(Hx')=i(x')H$, which means $\alpha$ is well-defined. Similarly, $\beta$ is well-defined
Also, $\alpha\cdot \beta=Id$, $\beta\cdot \alpha=Id$  ^8ef97a

---

The map $l_{x^{-1}}:\ xH\rightarrow H$ as $y\longmapsto x^{-1}y$ is the inverse of $l_{x}$
Similar with $r_{x}$ ^bfbe4a

---

Take $R\subseteq G$ be representatives for $\frac{G}{\sim_{H}}$, $|R|=\bigr|\frac{G}{\sim_{H}}\bigr|$ 
Moreover, $G=\bigcup_{x\in R}xH$ 
$\Longrightarrow\ |G|=\sum\limits_{x\in R}|xH|=\sum\limits_{x\in R}|H|=|R|\times |H|=\bigr|\frac{R}{\sim_{H}}|\times |H|$  ^68f1ad

---

"$\Longleftarrow$" If $\forall x\in G$, then $xHx^{-1}=H$, then $xHx^{-1}\subseteq H\ \Longrightarrow H\lhd G$
"$\Longrightarrow$" If $H\lhd G$, then $\forall x\in G$, $xHx^{-1}\subseteq H$
	But also, for fixed $x\in G$: $x^{-1}H(x^{-1})^{-1}\subseteq H$
	This means $H\subseteq xHx^{-1}$ for all $x\in G$
	Thus $H=xHx^{-1}$ ^18e936

---

Check: when $\overline{x}=\overline{x'},\ \overline{y}=\overline{y'}$, then $\overline{xy}=\overline{x'y'}$
Take $g\in xyH$, then there exists $h\in H$ s.t. $g=xyh$
Since $\overline{x}=\overline{x'}$, $\exists h_{1}\in H$ s.t. $x'=xh$, similarly, $\exists h_{2}\in H$ s.t. $y'=yh$
So $x'y'=xh_{1}yh_{2}=xyy^{-1}h_{1}yh_{2}=xyh_{3}h_{2}$
$\iff\ xy=x'y'h_{5}\ \Longrightarrow g=x'y'h_{6}\Longrightarrow g\in \overline{x'y'}$
The inverse is identical ^854c43

---

First prove the uniqueness of $\overline{f}$
	If $f=\overline{f}p\ \Longrightarrow \forall \overline{g}\in\frac{G}{ker(f)}$, $\overline{f}(p(g))=f(g)\iff \overline{f}(\overline{g})=f(g)$, hence unique
Then we prove the existence of $\overline{f}$ (well-defined? Homomorphism?)
We need to check that $\overline{f}:\ \frac{G}{ker(f)}\rightarrow G'$ as $\overline{g}\longmapsto f(g)$ is well-defined
	CHECK: If $\overline{g}=\overline{g'}$, then $\overline{f}(\overline{g})=\overline{f}(\overline{g'})\iff f(g)=f(g')$ 
	If $\overline{g}=\overline{g'}$, then $\exists\ k\in ker(f)$ s.t. $g'=gk\ \Longrightarrow f(g')=f(gk)=f(g)f(k)=f(g)$
Check if $\overline{f}$ is a group homomorphism
	$\overline{f}(\overline{x}\overline{y})=\overline{f}(\overline{xy})=f(xy)=f(x)f(y)=\overline{f}(\overline{x})\overline{f}(\overline{y})$ 
Lastly, we check injectivity
	If $\overline{x}\in ker(\overline{f})$, then $\overline{f}(\overline{x})=e'\iff f (x)=e'\iff x\in ker(f)\iff \overline{x}=\overline{e}\in \frac{G}{ker(f)}$  ^caf9fa

---

1). We know that $f(H)\leq f(G)$, take $y\in f(H),\ y'\in f(G)$, $y=f(h),\ y'=f(g)$
Then $f(g)f(h)f(g)^{-1}=f(ghg^{-1})\in f(H)\Longrightarrow f(H)\lhd f(G)$
2). We know that $f^{-1}(H)\leq G$, if $g\in G,\ h\in f^{-1}(K)$, then $f(ghg^{-1})=f(g)f(h)f(g)^{-1}\in K$, then $ghg^{-1}\in f^{-1}(K)$, thus normal in $G$ ^2ce42d

---

Well-defined:
For $I$:
	1. $ker(f)\leq H\leq G$, then $f(H)\leq Im(f)$
	2. For $H'=H$, satisfying the condition, $f(H)=f(H')$ because $f$ is well-defined in $G$
For $J$:
	1. For $K\leq Im(f)=f(G)$, $e_{G'}\in K$, then $ker(f)=f^{-1}(e_{G'})\subseteq f^{-1}(K)$
Now take $K\in B$, $K\leq f(G)$, then $IJ(K)=f(f^{-1}(K))=K$, because $K\leq f(G)$ 
Conversely, take $H\in A$, $ker(f)\leq H\leq G$, then $H\subseteq J(I(H))=f^{-1}(f(H))$
Now let $x\in f^{-1}(f(H))$, so $f(x)\in f(H)\Longrightarrow f(x)=f(h)$ for $h\in H$ 
$\iff f(xh^{-1})=e_{G'}\iff xh^{-1}\in ker(G)\subseteq H\Longrightarrow x=(xh^{-1})h\in H\Longrightarrow J(I(H))=H$ ^aadc17

---

Take $\bar{x}\in \frac{\mathbb{Z}}{m\mathbb{Z}}$, exists $(q,r)\in \mathbb{Z}\times \{0, 1, \dots, m-1\}$ s.t. $x=qm+r$, then ${} \bar{x}=\overline{qm+r}=\overline{qm}+\overline{r}=\overline{0}+\overline{r} {}$ 
Then we need to show that $\{\bar{0}, \dots, \overline{m-1}\}$ are distinct.
Suppose that there exists $0\leq x<y\leq m-1$ s.t. $\overline{x}=\overline{y}$, then $\overline{y}-\overline{x}=\overline{y-x}=0\Longrightarrow m|(y-x)$. However, this cannot happen. ^eaaeda

---

