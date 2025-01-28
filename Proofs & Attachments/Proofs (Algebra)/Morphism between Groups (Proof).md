$f(e\cdot e)=f(e)\cdot f(e)=f(e)$, then $f(e)=e'$  ^f976d1

---

$f(x\cdot x^{-1})=f(x)\cdot f(x^{-1})=f(e)=e'$, then $f(x^{-1})=f(x)^{-1}$  ^7f32eb

---

Take $f\in Hom(\mathbb{Z},\mathbb{Z})$, put $a\coloneqq f(1)$, WTP: $f=m_{a}$ with $m_{a}:\ x\longmapsto ax$ 
Let $x\in \mathbb{Z}$, if $x=0$, $f(0)=0=m_{a}(0)$
If $x\geq 0$, $f(x)=f(1+1+1+\dots +1)=\sum\limits f(1)=xa=m_{a}(x)$
If $x<0$, $f(x)=f(-|x|)=-f(|x|)=-a|x|=ax=m_{a}(x)$   ^1e47dc

---

$f_{2}\circ f_{1}(g\cdot h)=f_{2}(f_{1}(g+h))=f_{2}(f_{1}(g)\cdot f_{1}(h))=f_{2}(f_{1}(g))\cdot f_{2}(f_{1}(h))=f_{2}\circ f_{1}(g)\cdot f_{2}\circ f_{1}(h)$, thus homomorphism    ^ba977e

---

Image:
1). $e'=f(e)\in f(H)$
2). If $x',y'\in f(H)$, $\exists x,y\in H$ s.t. $f(x)=x',\ f(y)=y'$ and $x'y'=f(x)f(y)=f(xy)\in f(H)$
3). $y'^{-1}=f(y)^{-1}=f(y^{-1})\in f(H)$ 
Kernal:
1). $f(e)=e'\Longrightarrow e= f^{-1}(e')\in f^{-1}(H')$ 
2). If $x,y\in f^{-1}(H')$, $f(xy)=f(x)f(y)\in H'\Longrightarrow xy\in f^{-1}(H')$ 
3). $f(y^{-1})=f(y)^{-1}\in H'\Longrightarrow y^{-1}\in f^{-1}(H')$ ^f2c310

---

"$\Longrightarrow$" If $x\in ker(f),\ f(x)=e'$, hence $f(x)=f(e) \Longrightarrow x=e\Longrightarrow ker(f)\subseteq \{e\}, ker(f)=\{e\}$ 
"$\Longleftarrow$" Assume $ker(f)=\{e\}$, then if $f(x)=f(y)$, $f(x)f(y)^{-1}=e'\iff f(xy^{-1}=4'\Longrightarrow xy^{-1}=e\Longrightarrow x=y\Longrightarrow$ injective  ^ab512f

---

We just need to prove that $f^{-1}$ is a homomorphism since we've already known that the inverse of a bijective map is bijective.
Take $x',y'\in G'$, $\exists!\ x,y\in G$ s.t. $f(x)=x',\ f(y)=y'$
$x=f^{-1}(x'), y=f^{-1}(y')$
$f^{-1}(x'y')=f^{-1}(f(xy))=xy=f^{-1}(x)f^{-1}(y')$  ^604f47

---

1). $Id_{G}\in Aut(G)$ is also the neutral element of $\mathfrak{S}_{G}$  
2). If $f\in Aut(G)$, then $f^{-1}\in Iso(G,G)=Aut(G)$
3). If $f,f'\in Aut(G)$, then $f\circ f'\in Hom(G,G)$, $f\circ f'$ is also bijective $\Longrightarrow\ f\circ f'\in Aut(G)$  ^e0d463

---

We know that $Aut(\mathbb{Z})\subseteq End(\mathbb{Z})=\{m_{a},a\in \mathbb{Z}\}$ 
If $m_{a}$ is bijective, then it must be surjective, particularly there exists unique $x\in \mathbb{Z}$ s.t. m_{a}(x)=1
$\Longrightarrow$ ($a=1$ and $x=1$) or ($a=-1$ and $x=-1$)
Hence $Aut(\mathbb{Z})\subseteq \{m_{1},m_{-1}\}$
The converse is obvious ^cbc4c2

---

First prove $\iota_{x}$ is group homomorphism
$\iota_{x}(gh)=xghx^{-1}=xgx^{-1}xhx^{-1}=\iota_{x}(g)\cdot \iota_{x}(h)$ 
Then prove $\iota_{x}$ is isomorphism
	Surjectivity: for arbitrary $y$ in the image,
	$\iota{x^{-1}yx}=xx^{-1}yxx^{-1}=y$ 
	Injectivity: $\iota_{x}(g)=\iota_{x}(h)\iff xgx^{-1}=xhx^{-1}\iff g=h$  ^8fda91

---

1). $Id=\iota_{e}$ is the neutral element
2). $\iota, \varphi\in Inn(G)$, obviously $\iota\varphi\in Inn(G)$ 
3). For $\iota_{x}$, $\iota_{x^{-1}}=\iota_{x}^{-1}\in Inn(G)$  ^72bd4e

---

If $x \in G$, then $x=exe^{-1}$, which indicates that $x\sim x.$ <font color="#ff0000">(reflectivity)</font>
If $y\sim x$, then $\exists \  g\in G$ s.t. $y=gxg^{-1}$, then $x=(g^{-1})y(g^{-1})^{-1}$, which indicates that $x\sim y$ <font color="#ff0000">(symmetry)    </font>
If $y\sim x$ and $z\sim y$, then $\exists \ a,b\in G$ s.t. $y=\iota_{a}(x)$ and $z=\iota_{b}(y)$, then $z=\iota_{b}(\iota_{a}(x))=\iota_{ba}(x)$, then $z\sim x$. <font color="#ff0000">(transitivity)</font> ^86b54f

---

**"Right inclusion"**: $Cl_{\mathfrak{S}_{n}}(c)\subseteq\{All\ r-cycles\}$ 
Take $\varphi\in \mathfrak{S}_{n}$, let's compute $\varphi (1, \dots , r)\varphi^{-1}$. Take $x\in [1,n]$, where $[...]$ denotes integers inside this interval, either:
	1).  $x\in \{\varphi(1),\dots, \varphi(r)\}$ 
	2). $x\in [1,n]-\{\varphi(1),\dots, \varphi(r)\}$
For case 1, where $x=\varphi(i)$ for $i\in \{1, \dots, r\}$, then ${} \varphi (1, \dots , r)\varphi^{-1}(\varphi(i)) {}$ equals to
	$\varphi(i+1)$ if $i\leq r-1$
	$\varphi(1)$ if $i=r$
For case 2, $\varphi (1, \dots , r)\varphi^{-1}\cdot x=x$ 
In conclusion: $\varphi (1, \dots , r)\varphi^{-1}\cdot x$ equals to 
	$x$ if $x\in [1,n]-\{\varphi(1),\dots, \varphi(r)\}$
	$\varphi(i+1)$ if $x\in \{\varphi(1),\dots, \varphi(r)\}$ and $i\leq r-1$
	$\varphi(1)$ if $x\in \{\varphi(1),\dots, \varphi(r)\}$ and  $i=r$
It is a r-cycle.
**"Left inclusion"**: $Cl_{\mathfrak{S}_{n}}(c)\supseteq\{All\ r-cycles\}$ 
Take function $\varphi$: 
	$1\longrightarrow a_{1}$
	$2\longrightarrow a_{2}$
	$\dots$
	$r\longrightarrow a_{r}$
Note that $[1,n]-\{1, \dots, r\}$ and $[1,n]-\{a_{1}, \dots, a_{r}\}$ have same cardinality, so $f$ is bijective.
$\varphi (1, 2, \dots, r)\varphi^{-1}=(\varphi(1), \dots, \varphi(r))=(a_{1}, \dots, a_{r})$  ^269474

---



