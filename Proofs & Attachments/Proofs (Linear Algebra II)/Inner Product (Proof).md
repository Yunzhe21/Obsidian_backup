
For all $t\in\mathbb{R}$, $\langle x+ty,x+ty\rangle\geq 0$
$\langle x+ty, x+ty\rangle=\langle x,x+ty\rangle +t\langle y,x+ty\rangle=\langle x,x\rangle+2t\langle x.y\rangle +t^{2}\langle y,y\rangle$ 
Then $\Delta=(2\langle x,y\rangle)^{2}-4\langle y,y\rangle\langle x,x\rangle\leq0$, then the lemma is proved. ^105258

---

Fix a basis $\{e_{1}, \cdots, e_{n}\}$ for $V$
Then $x=x_{1}e_{1}+\cdots+x_{n}e_{n}$ and $y=y_{1}e_{1}+\cdots+y_{n}e_{n}$ for arbitrary $x,y$
$\langle x,y\rangle=\langle \sum\limits x_{i}e_{i},\sum\limits y_{j}e_{j}\rangle=\sum\limits_{1\leq i,j\leq n}\overline{x_{i}}y_{j}\langle e_{i}, e_{j}\rangle=(\overline{x_{1}}, \cdots, \overline{x_{n}})\begin{pmatrix} \langle e_{1},e_{1}\rangle && \cdots && \langle e_{1},e_{n} \rangle \\ \vdots && \ddots && \vdots \\ \langle e_{n},e_{1} && \cdots && \langle e_{n},e_{n} \rangle \end{pmatrix}\begin{pmatrix} y_{1} \\ \vdots \\ y_{n}\end{pmatrix}$ ^15fad5

---

Fix a basis $\{e_{1}, \cdots, e_{n}\}$, then $f(x)=Ax$
By Jordan decomposition, $A=P\Lambda P^{-1}$
By QR-decomposition, $P=QR$
$A=Q(R\Lambda R^{-1})Q^{-1}=QUQ^{-1}$ ^bd1b41

---

(Uniqueness) If $\langle y,x\rangle=\langle y',x\rangle$, for all $x\in V$, then $\langle y-y',x\rangle=0$ for all $x\in V$
We just let $x=y-y'$, then $\|y-y'\|=0$, which implies that $y=y'$.
(Existence) As we know that $V=\text{Ker}f\oplus(\text{Ker}f)^{\perp}$ 
By the Rank Theorem, $\dim\text{Ker}f+\dim\text{Im}f=\dim V$, where $\dim\text{Im}f\leq 1$.
If $\dim\text{Im}f=0$, then $f=0$, we just choose $y=0$ and the proof is done.
If $\dim\text{Im}f=1$, then there exists $v\in(\text{Ker}f)^{\perp}$, where $v$ is also a unit vector.
Check: $f(x)=\langle \overline{f(v)}v,x\rangle$ for all $x\in V$
$\forall x\in V$, $x=x_{1}+k_{1}v$ for some $x_{1}\in\text{Ker}f$
$f(x)=f(x_{1})+k_{1}f(v)=k_{1}f(v)=\langle \overline{f(v)}v,x_{1}+k_{1}v\rangle$ ^d03113

---

$\forall y_{1}, y_{2}\in W$, $a_{1}, a_{2}\in\mathbb{F}$
$\langle a_{1}y_{1}+a_{2}y_{2}, f(x)\rangle_{W}=\langle f^{*}(a_{1}y_{1}+a_{2}y_{2}),x\rangle_{V}$ 
$\text{LHS}=\overline{a_{1}}\langle y_{1},f(x)\rangle_{W}+\overline{a_{2}}\langle y_{2},f(x)\rangle_{W}=\overline{a_{1}}\langle f^{*}(y_{1}), x\rangle_{V}+\overline{a_{2}}\langle f^{*}(y_{2}),x\rangle_{V}=\langle a_{1}f^{*}(y_{1})+a_{2}f^{*}(y_{2}),x\rangle_{V}$
Thus $f^{*}(a_{1}y_{1}+a_{2}y_{2})=a_{1}f^{*}(y_{1})+a_{2}f^{*}(y_{2})$ ^9afbfb

---

$\langle y,(f^{*})^{*}(x)\rangle=\overline{\langle (f^{*})^{*}(x),y\rangle}=\overline{\langle x,f^{*}(y)\rangle}=\langle f^{*}(y),x\rangle=\langle y,f(x)\rangle$ ^625582

---

$\forall z\in (\text{Im}f^{*})^{\perp}$, $z\perp f^{*}(y)$ for all $y\in W$
${} iff {}$ $\langle f^{*}(y),z\rangle=\langle y,f(z)\rangle=0$ for all $y$, then $f(z)=0$, which means that $z\in\text{Ker}f$
Conversly, $\forall z\in\text{Ker}f$, $f(z)=0$, $\langle f^{*}(y),z\rangle=\langle y,f(z)\rangle=0$ for all $y$, then $z\in(\text{Im}f^{*})^{\perp}$  ^8aba30

---

"$\Longleftarrow$" is obvious
"$\Longrightarrow$" $\text{Re}\langle x,y\rangle=\frac{1}{2}(\|x+y\|^{2}-\|x\|^{2}-\|y\|^{2})=\frac{1}{2}(\|f(x+y)\|^{2}-\|f(x)\|^{2}-\|f(y)\|^{2})=\text{Re}\langle f(x),f(y)\rangle$ $\text{Im}\langle x,y\rangle=-\frac{1}{2}(\|x+iy\|^{2}-\|x\|^{2}-\|y\|^{2})=\text{Im}\langle f(x),f(y)\rangle$ #PolarizationIdentity
Then $\langle f(x),f(y)\rangle=\text{Re}\langle f(x),f(y)\rangle+\text{Im}\langle f(x),f(y)\rangle=\text{Re}\langle x,y\rangle+\text{Im}\langle x,y\rangle=\langle x,y\rangle$  ^3166b2

---

$\langle x,y\rangle=\langle f(x),f(y)\rangle=f(x)^{*}Af(y)=x^{*}M^{*}AMy$ for all $x,y$ ^f4397e

---

$\det(M^{*})\det(A)\det(M)=\det(M^{*}AM)=\det(A)\neq0$ ^5e1839

---

"$\Longrightarrow$" is obvious
"$\Longleftarrow$" **For real vector space**, we define $\langle x,y\rangle=\frac{1}{4}(\|x+y\|^{2}-\|x-y\|^{2})$ (Polarization Identity for $\mathbb{R}$). The reason for that is $\langle x,x\rangle=\|x\|^{2}$
Now we check condition for an inner product.
It is obvious that $\langle x,y\rangle=\langle y,x\rangle$; $\langle x,x\rangle\geq0$ and the equality holds iff $x=0$.
$\langle x+y,z\rangle=\frac{1}{4}(\|x+y+z\|^{2}-\|x+y-z\|^{2})=\frac{1}{4}(\|x+z\|^{2}-\|x-z\|^{2})+\frac{1}{4}(\|y+z\|^{2}-\|y-z\|^{2})$ $=\langle x,z\rangle+\langle y,z\rangle$.
Inductively, we have $\langle nx,z\rangle=n\langle x,z\rangle$ for all integer $n$. Similarly, we have $\langle x,z\rangle=\langle n\frac{1}{n}x,z\rangle=n\langle\frac{1}{n}x,z\rangle$, thus $\langle\frac{1}{n}x,z\rangle=\frac{1}{n}\langle x,z\rangle$
Note that $t\rightarrow \frac{1}{t}\langle tx,z\rangle$ is continuous on $\mathbb{R}-\{0\}$, and the fact that each real number is the limit of a sequence of rational numbers. $\langle rx,z\rangle=r\langle x,z\rangle$ for real $r$.
**For complex vector space**, define $\langle x,y\rangle=\frac{1}{4}(\|x+y\|^{2}+i\|ix+y\|^{2}-\|-x+y\|^{2}-i\|-ix+y\|^{2})=\frac{1}{4}\sum\limits_{k=0}^{3}i^{k}\|i^{k}x+y\|^{2}$
We can do similar argument as before. ^f50011

---



 