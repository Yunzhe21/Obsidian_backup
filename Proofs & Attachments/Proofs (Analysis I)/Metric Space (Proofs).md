
First we need to prove that $\sum\limits_{n=1}^{\infty}|a_{n}-b_{n}|$ converges absolutely
	This is obvious since $|a_{n}=b_{n}|\leq |a_{n}|+|b_{n}|$ 
3). Let $\{a_{n}\}, \{b_{n}\}, \{c_{n}\}$ be elements in $l^{1}$, then $|a_{n}-c_{n}|\leq |a_{n}-b_{n}|+|b_{n}-c_{n}|$ for every $n$, so $\sum\limits_{n=1}^{k}|a_{n}-c_{n}|\leq \sum\limits_{n=1}^{k}|a_{n}-b_{n}|+\sum\limits_{n=1}^{k}|a_{n}-c_{n}|$.
Take limit of both sides, we get what we want. ^0c8517

---

1), 2) are trivial and we ommit it 
3). For $(x_{1}, \dots, x_{n}), (y_{1}, \dots, y_{n}), (z_{1}, \dots, z_{n})$, want to prove:
$\sqrt{\sum\limits_{k=1}^{n}(x_{k}-z_{k})}\leq \sqrt{\sum\limits_{k=1}^{n}(x_{k}-y_{k})^{2}} + \sqrt{\sum\limits_{k=1}^{n}(y_{k}-z_{k})^{2}} \iff \sqrt{\sum\limits_{k=1}^{n}(a_{k}+b_{k})^{2}}\leq \sqrt{\sum\limits_{k=1}^{n}a_{k}^{2}}+\sqrt{\sum\limits_{k=1}^{n}b_{k}^{2}}$$\iff \sum\limits_{k=1}^{n}a_{k}b_{k}\leq \sqrt{\sum\limits_{k=1}^{n}a_{k}^{2}}\cdot \sqrt{\sum\limits_{k=1}^{n}b_{k}^{2}}$ 
<font color="#ff0000">Theorem</font> (Cauchy-Schwaz inequality for $\mathbb{R}^{n}$)
If $b_{k}=0$ for $1\leq k\leq n$, this ineqaulity holds.
If $b_{k}\neq 0$ for some k, $\sum\limits_{k=1}^{n}b_{k}^{2}>0$ 
	$0\leq \sum\limits_{k=1}^{n}(a_{k}-Xb_{k})^{2}$ for all real number $X$
	$0\leq \sum\limits_{k=1}^{n}a_{k}^{2}-2X\sum\limits_{k=1}^{n}a_{k}b_{k}+X^{2}\sum\limits_{k=1}^{n}b_{k}^{2}$, denote $\sum\limits_{k=1}^{n}a_{k}^{2}=A, \sum\limits_{k=1}^{n}a_{k}b_{k}=B,\sum\limits_{k=1}^{n}b_{k}^{2}=C$
	Let $X=\frac{B}{C}\Longrightarrow 0\leq AC-B^{2}$ 
We obtain the conclusion. ^4987c9

---

We've already known that $\sum\limits_{k=1}^{n}(x_{k}-y_{k})^{2}=\sum\limits_{k=1}^{n}x_{k}^{2}+\sum\limits_{k=1}^{n}y_{k}^{2}-2\sum\limits_{k=1}^{n}x_{k}y_{k}$ , we only need to show that $\sum\limits_{k=1}^{n}x_{k}y_{k}$ exists when $n\rightarrow\infty$ 
<font color="#ff0000">Theorem</font> (Cauchy-Schwaz inequality for $l^{2}$) 
	Proof is obvious by taking limits of both sides in Cauchy-Schwaz inequality for $\mathbb{R}^{n}$
Hence $\sum\limits_{k=1}^{\infty}(x_{k}-y_{k})^{2}$ exists, $d$ is well-defined. ^4289cc

---

1), 2) are simple
3). Let $\{a_{n}\}, \{b_{n}\}, \{c_{n}\}\in l^{2}$, $\sqrt{\sum\limits_{k=1}^{n}(a_{k}-c_{k})}\leq \sqrt{\sum\limits_{k=1}^{n}(a_{k}-b_{k})^{2}} + \sqrt{\sum\limits_{k=1}^{n}(b_{k}-c_{k})^{2}}$  for every $n$. Take limits from both sides, $d(\{a_{n}\}, \{c_{n}\})\leq d(\{a_{n}\}, \{b_{k}\})+d(\{b_{n}\}, \{c_{n}\})$ 
Hence we obtain the conclusion. ^370861

---

$\Longrightarrow$: If $\{x^{k}\}\rightarrow x$, $\forall \epsilon >0:\ \exists N$ s.t. if $k>N, \ d(x^{k}, x)<\epsilon$. 
Let $1\leq j\leq n$, $|x_{j}^{k}-x|\leq \sqrt{\sum\limits_{j=1}^{n}(x_{j}^{k}-x)^{2}}=d(x^{k}, x)<\epsilon$ $\Longrightarrow \lim_{k\to\infty}x_{j}^{k}=x_{j}$ 
$\Longleftarrow$: Suppose for each $j\in \{1, \dots, n\}$, $\{x_{j}^{k}\}\rightarrow x_{j}$ as $k\rightarrow \infty$. Then $\forall \epsilon>0$, for each $j$, $\exists N_{j}$  s.t. if $n>N_{j}$, $|x_{j}^{k}-x_{j}|<\frac{\epsilon}{\sqrt{n}}$ , then $d(x^{k}, x)<\sqrt{\sum\limits_{j=1}^{n}(x_{j}^{k}-x)^{2}}<\sqrt{n\times \frac{\epsilon^{2}}{n}}=\epsilon$ 
Hence, $\{x^{k}\}\rightarrow x$. ^28bf6e

---

Let $x$ be a cluster point of $X$, i.e. $\exists \{x_{k}\}\in X-\{x\}$ s.t. $\{x_{k}\}\rightarrow x$, so there must exists infinitely many $x_{k}$ that belongs to one of the $X_{i}$, hence $x\in$ one of $X_{i}$ ^0873e4

---

Let $x$ be a cluster point of $X$, then $\exists \{x_{n}\}\subset X-\{x\}$ s.t. $\{x_{n}\}\rightarrow x$
Since $\{x_{n}\subset X$, then $\{X_{n}\}\subset X_{j}$ for all $j$
Since all $X_{j}$ are closed, then $x=\lim_{n\to\infty}x_{n}\in X_{j}$
Hence $x\in X_{j}$ for all $j$
$x\in \bigcap_{j=1}^{\infty}X_{j}$ ^353f1a

---

$\Longrightarrow$: If $X$ is open, then $\forall x\in X$, $\exists B_{r}(x)\subset X$, which means that no points of $X^{c}$ is inside $B_{r}(x)$, hence $x$ is not an accumulation point of $X^{x}$.
So all accumulation points of $X^{c}$ have to be in $X^{c}$, so $X^{c}$ is closed.
$\Longleftarrow$: Suppose $X$ is not open, then let $\epsilon_{n}=\frac{1}{n}$, $\exists \{x_{n}\}$ s.t. $x_{n}\notin X$ while $d(x_{0}, x_{n})<\frac{1}{n}$, i.e. $x_{n}\in X^{c}$ s.t. $x_{n}\rightarrow x_{0}\in X$ rather than $X^{c}$, hence $X^{c}$ is not closed. ^f4b14d

---

$\mathbb{M}-(\bigcap_{i=1}^{N}O_{i})=\bigcup_{i=1}^{N}(\mathbb{M}-O_{i})$ is closed, then by [[002 Topology for metric spaces (M, d)#^ComplementOfCloseOpen|Theorem]], we have $\bigcap_{i=1}^{N}O_{i}$ is open ^980e86

---

$\mathbb{M}-(\bigcup_{i=1}^{\infty}O_{i})=\bigcap_{i=1}^{\infty}(M-O_{i})$ is closed, then $\bigcup_{i=1}^{\infty}O_{i}$ is open. ^c95eff

---

"Compactness $\Longrightarrow$ Sequentially Compactness": Choose $\{x_{n}\}\subset \mathbb{M}$, define subset  $E$ of $\mathbb{M}$ as $\{x_{n}|n=1, 2, \dots\}$.
If  $E$ is finite subset. Then write $E$ as $\{x_{1}, \dots x_{m}\}$, at least one of the $x_{i}$ must repeat infinitely, then pick the subsequence that eventually stable at $x_{i}$, we obtain sequentially conpactness.
If  $E$ is an infinite subset. $E=\{x_{1}, x_{2}\dots\}$. Suppose that no subsequence of $E$ converges, then $\forall x\in \mathbb{M}, \exists \epsilon_{x}>0$ s.t. $B_{\epsilon_{x}}(x)\cap E=\{x\}$. Let $\{B_{\epsilon_{x}}(x)\}$ be the open cover of $\mathbb{M}$, then it cannot be reduced a finite subcover, which leads to contradiction. ^5d3219

---

Given $\epsilon>=0$, let $x_{1}\in \mathbb{M}$ and consider $\mathbb{M}-B_{\epsilon}(x_{1})$. 
	If $\mathbb{M}\subset B_{\epsilon}(x_{1})$, then the proof is done already
	Otherwise, choose $x_{2}\in M-B_{\epsilon}(x_{1})$ 
		If $\mathbb{M}\subset B_{\epsilon}(x_{1})\cup B_{\epsilon}(x_{2})$, then the proof is done
		Otherwise, choose $x_{3}\in\mathbb{M}-B_{\epsilon}(x_{2})-B_{\epsilon}(x_{1})$ 
Repeat this process , we will eventually end somewhere or we don't
For the latter case, we naturally find a sequence $\{x_{1}, x_{2}, \dots\}$ s.t. $x_{j}-x_{i}>\epsilon$ for $j>i$. This means that a sequence is divergent, contradicting the fact that $\mathbb{M}$ is sequentially compact. ^433766

---

Let $\{x_{n}\}\subset K\subset \mathbb{M}$, since $\mathbb{M}$ is sequentially compact, $\exists \{x_{n_{k}}\}\subset K\rightarrow x\in \mathbb{M}$.
Given $K$ is closed and $x$ is a limit point, $x\in K$, which means $K$ is sequentially compact. ^5e2d84

---

Let $\{O_{\alpha}\}_{\alpha\in\Lambda}$ be a collection of open sets in $K$ which covers $K$, $O_{\alpha}=K\cap U_{\alpha}$, where $\{U_{\alpha}\}$ are open in $\mathbb{M}$. Naturally, $K\subset \bigcup_{\alpha\in\Lambda}U_{\alpha}$, so $\{U_{\alpha}\}_{\alpha\in\Lambda}\cup\{\mathbb{M}-K\}$ covers $\mathbb{M}$. 
Since $\mathbb{M}$ is compact, exists $\{U_{\alpha_{i}}\}_{i=1}^{m}\cup\{\mathbb{M}-K\}$ covers $\mathbb{M}$, then $K\subset \{U_{\alpha_{i}}\}_{i=1}^{m}$, hence $K$ is compact. ^e2dba9

---

Let $\{O_{\alpha}\}_{\alpha\in\Lambda}$ be an open cover of $\mathbb{M}$.
Suppose there is no finite subcollection of $\{O_{\alpha}\}_{\alpha\in\Lambda}$ which covers $\mathbb{M}$.
According to [[002 Topology for metric spaces (M, d)#^74be69|lemma]], for $\epsilon=1$, exists $x_{1}, \dots, x_{m_{1}}\in \mathbb{M}$ s.t. $\mathbb{M}=\bigcup_{i=1}^{m_{1}}B_{i}(x_{i})=\bigcup_{i=1}^{m_{1}}\{x\in\mathbb{M}|d(x,x_{i})\leq 1\}$ 
Check: $\{x\in\mathbb{M}|d(x,x_{i})\leq 1\}$ are closed
Since $\mathbb{M}$ is sequentially compact, then $\{x\in\mathbb{M}|d(x,x_{i})\leq 1\}$ are sequentially compact according to [[002 Topology for metric spaces (M, d)#^886425|lemma]].
At least one of such balls cannot be covered by any finite subcollection of $\{O_{\alpha}\}_{\alpha\in\Lambda}$ 
Denote this ball by $\overline{B_{1}(x_{n_{1}})}$, simply repeat this process on the ball with $\epsilon_{2}=\frac{1}{2}$
$\overline{B_{1}(x_{n_{1}})}\subset \bigcup_{i=1}^{m_{2}}\overline{B_{\frac{1}{2}}(x_{i+m_{1}})}$ , exists one ball $\overline{B_{\frac{1}{2}}(x_{n_{2}})}$ can't be covered by any finite subcollection of $\{O_{\alpha}\}_{\alpha\in\Lambda}$ 
$\dots$ 
$\mathbb{M} \supseteq \overline{B_{1}(x_{n_1})} \supseteq \overline{B_{\frac{1}{2}}(x_{n_2})} \supseteq \dots \supseteq \overline{B_{\frac{1}{2^{k}}}(x_{n_k})}\dots$ s.t. each ball cannot be covered by finite subcollection 
$x_{n_{k}}\rightarrow x_{\star}\in \mathbb{M}$ 
Exists $\alpha_{\star}\in \Lambda$ s.t. $x_{\star}\in O_{\alpha_{\star}}$ ($\mathbb{M}$ is covered by O's)
Exists $\delta_{\star}>0$ s.t. $B_{\delta_{\star}}(x_{\star})\subset O_{\alpha_{\star}}$ (openness)
Since $\{x_{n_{k}}\}\rightarrow x_{\star}\Longrightarrow d(x_{n_{k}}, x_{\star})<\frac{\delta_{\star}}{4}$ when $k\geq K$, then $\frac{1}{2^{k}}<\frac{\delta_{\star}}{4}$ if $k\geq K$ 
Hence $\overline{B_{\frac{1}{2^{k}}}(x_{n_k})}\subset B_{\delta_{\star}}(x_{\star})\subset O_{\alpha_{\star}}$, contradicting the fact that $\overline{B_{\frac{1}{2^{k}}}(x_{n_k})}$ cannot be covered by any finite collection of open sets. Hence we obtain the final conclusion. ^cd19a4

---

Suppose $K$ is compact relative to $X$.
Let $\{V_{\alpha}\}_{\alpha\in\Lambda}$ be a collection of open sets relative to $Y$, and $K\subset \bigcup_{\alpha\in\Lambda}V_{\alpha}$.
According to [[002 Topology for metric spaces (M, d)#^CloseOpenRelative|Theorem]], $V_{\alpha}=Y\cap G_{\alpha}$ for $G_{\alpha}$ open relative to $X$.
Since $K$ is compact relative to $X$, then exists $\{G_{\alpha_{n}}\}_{n=1}^{m}$ s.t. $K\subset \bigcup_{n=1}^{m} G_{\alpha_{n}}$
Then, since $K\subset Y$, then $K\subset \bigcup_{n=1}^{m}V_{\alpha_{n}}\Longrightarrow$ $K$ compact relative to $Y$
If $K$ is compact relative to $Y$.
Let $\{G_{\alpha}\}_{\alpha\in\Lambda}$ be a collection of open sets relative to $X$. Put $V_{\alpha}=Y\cap G_{\alpha}$, then $K\subset \bigcup_{\alpha\in\Lambda}V_{\alpha}$ holds for a selection of $\{V_{\alpha}\}$, so $K\subset \bigcup_{n=1}^{m} G_{\alpha_{n}}$ holds $\Longrightarrow$ $K$ is compact relative to $X$. ^667fc8

---

(Closeness) Let $K$ be a compact subset of $X$, we aim to prove that the complement of $K$ is open.
Let $p\in K^{c}$, if  $q\in K$, define $V_{q}, W_{q}$ as neighbors of $p$ and $q$, with radius all less than $\frac{1}{2}d(p, q)$. 
Since K is compact, then there exists $\{W_{q_{1}}, \dots, W_{q_{n}}\}$ s.t. it covers K, $V=\bigcap_{i=1}^{n}V_{q_{i}}$ is a neighbor of $p$ which doesn't intersect with K, so $p$ is an interior point of $K^{c}$. Since the choice of $p$ is arbitrary in $K^{c}$, all points in $K^{c}$ are interial points $\Longrightarrow$ closed.
(Bounded) Suppose that $K$ is not bounded, then for $n\in \mathbb{N}$, exists $x_{n}\in X$ s.t. $d(x, x_{n})>n$, so $\{x_{n}\}$ is divergent, which contradicts the fact that $K$ is not sequentially compact. ^d87cfd

---

Let $\{a^{(k)}\}_{k=1}^{\infty}$, since $K$ is bounded, then $\{a_{1}^{(k)}\}_{k=1}^{\infty}$ is bounded, so it contains a sebsequence $\{a_{1}^{(k_{j})}\}_{j=1}^{\infty}$ that is convergent.
Now, let's consider $\{a_{2}^{(k_{j})}\}_{j=1}^{\infty}$, which is also bounded, so it contains a subsequence $\{a_{2}^{(k_{j_{l}})}\}_{l=1}^{\infty}$ that is convergent. Note that $\{a_{1}^{(k_{j_{l}})}\}_{l=1}^{\infty}$ is still convergent.
Continue this process, we obtain a subsequence of $\{a^{(k)}\}_{k=1}^{\infty}$ s.t. it is convergent $\Longrightarrow$ Sequentially compact $\Longrightarrow$ Compact
The opposite side is already proven in a general sense. ^58787a

---

Suppose $M$ is not connected 1), then there exists a proper subset $U$ of $M$ s.t. U is both open and closed in $M$, then we find $U\cup U^{c}=M$ and $U\cap U^{c}=\varnothing$, which proves both 2) and 3).
Suppose 2). Then let $U,V$ be two open and nonempty proper subset of $M$ s.t. $U\cup V=M$ and $U\cap V=\varnothing$, $M=M-(U\cap V)=U^{c}\cup V^{c}$ and $\varnothing=M-(U\cup V)=U^{c}\cap V^{c}$, where $U^{c}, V^{c}$ are closed and nonempty. Hence 3).
If $M=C\cup D$, where $C,D$ are closed and $C\cap D=\varnothing$ 3). Then $D=C^{c}$ and $C=D^{c}$, then $D$ is open and closed at the same time while $D$ is nonempty and proper. Hence 1). ^84b417

---

$\Longrightarrow$: suppose that $X$ is connected and exists $a, b\in X$, $a<b$, and $\exists c\in [a, b]$ s.t. $c\notin X$.
Then define $U=\{x:x<c\}\cap [a, b]$ and $V=\{x:x>c\}\cap [a,b]$
According to [[002 Topology for metric spaces (M, d)#^CloseOpenRelative|Theorem]], then $U$ is open in $X$ and $V$ is open relative to $X$, then $X$ is not connected, which lead to a contradiction.
$\Longleftarrow$: suppose that whenever $a,b\in X$ with $a<b$, we have $[a,b]\subset X$ 
If $X$ is not connected, then exists $C,D$ closed and nonempty s.t. $X=C\cup D$ and $\varnothing=C\cap D$.
Let $a\in C$ and $b\in D$ and assume that $a<b$.
Define $c=lub\{x\in C: x<b\}$
By approximation property, for every $n\in \mathbb{N}^{+}$, $\exists x_{n}$ s.t. $c-\frac{1}{n}<x_{n}<c$, so $x_{n}\rightarrow c$ by the definition of limit of sequence, and since $C$ is closed, then $c\in C$.
By definition of $c$, $c<b$, then by our hypothesis, $[c, b]\in X$ 
Next, we want to show that $(c,d)\subset D$. If there exists $y\in (c,d)$ s.t. $y\notin D$, then $y\in C$, so $y<c=lub\{x\in C:x<b\}$, which contradicts the fact that $y\in (c, d)$, hence, $(c,d)\subset D$, then $c$ is a limit point of $D$, then $c\in D$ for $D$ is a closed set.
Finally, we have $c\in C\cap D=\varnothing$, which is absurd. ^cfbc21

---

$\Longrightarrow$: Let $f$ be continuous at $a$, then $\forall \epsilon>0$: $\exists \delta>0$ s.t. if $d_{1}(x, a)<\delta$, $x\in M_{1}$, then $d_{2}(f(x), f(a))<\epsilon$. Now if $\{x_{n}\}\subset M_{1}$ s.t. $x_{n}\rightarrow a$, then for $\delta>0$, there is $N\in\mathbb{N}$ s.t. if $n\geq N$, $d(x_{n}, a)<\delta\Longrightarrow d_{2}(f(x_{n}), f(a))<\epsilon$.
$\Longleftarrow$: Suppose $f$ is not continuous at $a$, then $\exists \epsilon_{0}>0$ s.t. no matter how small $\delta$ is, $\exists x\in M$ s.t. $d_{1}(x, a)<\delta$, but $d_{2}(f(x), f(a))\geq\epsilon$.
Take $\delta=\delta_{n}=\frac{1}{n}\Longrightarrow\exists x_{n}\in M$, but $d_{2}(f(x_{n}), f(a))\geq \epsilon_{0}>0$
This contradicts that for all $\{x_{n}\}\rightarrow a\Longrightarrow \{f(x)\}\rightarrow f(a)$ ^c82423

---

$1)\Longrightarrow2)$: Suppose that $f$ is continuous on $M_{1}$. Let $V$ open relative to $M_{2}$, $U=f^{-1}(V)$
Let $a\in U$, $f(a)\in V\Longrightarrow \exists \epsilon>0$ s.t. $B_{\epsilon}(b)\subset V\subset M_{2}$ 
Since $f$ is continuous, then for $\epsilon>0:$ $\exists \delta>0$ s.t. whenever $d_{1}(x, a)<\delta$, then $d_{2}(f(x), b)<\epsilon$, $B_{\delta}(a)\subset f^{-1}(B_{\epsilon}(b))\subset U\Longrightarrow$ open.
$2)\Longrightarrow3)$: Let $F$ be closed in $M_{2}$ ($\Longrightarrow F^{c}=V$ is open)
By 2), $U=f^{-1}(V)$ is open. Note: $f^{-1}(V)=f^{-1}(M_{2}-F)=f^{-1}(M_{2})-f^{-1}(F)=M_{1}-f^{-1}(F)=E^{c}$. Therefore $E^{c}$ is open, $E$ is closed.
$3)\Longrightarrow1)$: Suppose that $f$ is not continuous. There is an $a\in M_{1}$ s.t. $f$ is not continuous at $a\Longrightarrow$ $\exists \{x_{n}\}\subset M_{1}$ s.t. $\{x_{n}\}\rightarrow s$ but $d(f(x_{n}), f(a))>\epsilon>0$ 
Let $F=\{y\in M_{2}:d(y, f(a))\geq \epsilon_{0}\}$, $F$ is closed in $M_{2}$
By 3), we know that $f^{-1}(F)=E$ is also closed in $M_{1}$
Consider $\{x_{n}\}\subset E$, with $x_{n}\rightarrow a$, since $E$ is closed, $a\in E\iff d(f(a), f(a))\geq 0$ (by definition of set $F$), which is absurd. ^0c0e0b

---

(First part) For arbitrary $x_{0}\in M$, $f(x_{0})\in \mathbb{R}$. Since $f$ is continuous, then when $\epsilon=1$, $\exists \delta_{x_{0}}>0$ s.t. whenever $|x-x_{0}|<\delta_{x_{0}}$, $|f(x)-f(x_{0})|<\epsilon=1$ $\Longrightarrow f(x_{0})-1\leq f(x)\leq f(x_{0})+1\Longrightarrow f$ is bounded in a ball.
Since $M$ is compact, then for $M\subset \bigcup_{x\in M} B_{\delta_{x}}(x)$, where $\delta_{x}$ is chosen as shown above, there exists $\{x_{1}, \dots, x_{n}\}\subset M$ s.t. $M\subset \bigcup_{i=1}^{n}B_{\delta_{x_{i}}}(x_{i})$. In each ball, $f$ is bounded, hence $f$ is bounded in $M$.
(Second part) Here we only prove the maximal case.
Let $B^{\star}=sup\{f(x): x\in M\}$, we claim that there exists $x_{\star}$ s.t. $f(x_{\star})=B^{\star}$
Suppose that $f(x)<B^{\star}$ for all $x\in M$, then consider $g(x)=\frac{1}{B^{\star}-f(x)}$, which is continuous.
By the first part, we know that $g(x)\leq T^{\star}$, then $\frac{1}{B^{\star}-f(x)}\leq T^{\star}\Longrightarrow f(x)\geq B^{\star}-\frac{1}{T^{\star}}$, which is absurd if we take supreme from both sides $B^{\star}\geq B^{\star}-\frac{1}{T^{\star}}$. ^022d32

---

Since $f$ is continuous, then for arbitrary $\epsilon>0$, for all $p\in M_{1}$, we associate a $\delta_{p}$ s.t. whenever $d_{1}(x-p)<\delta_{p}$, we have $d_{2}(f(x)-f(p))<\frac{1}{2}\epsilon$. 
Let $J(p)$ be the set of $q$ s.t. $d_{1}(q, p)<\frac{1}{2}\delta_{p}$, so $J(p)$ covers the whole $M_{1}$. 
Since $M_{1}$ is compact, exists $\{p_{1}, \dots, p_{n}\}$ s.t. $J(p_{1}), \dots, J(p_{n})$ covers $M_{1}$
Put $\delta=\frac{1}{2}min\{J(p_{1}), \dots, J(p_{n})\}>0$
Let $p, q$ be two points s.t. $d_{1}(p,q)<\delta$, we know that $p\in J(p_{m})$ for $1\leq m\leq n$, so $d_{1}(p, p_{m})<\frac{1}{2}\delta_{p_{m}}$.
Then $d_{1}(q, p_{m})\leq d_{1}(p, p_{m})+d_{1}(p, q)<\frac{1}{2}\delta_{p_{m}}+\delta<\delta_{p_{m}}$, hence 
$d_{2}(f(p), f(q))\leq d_{2}(f(p), f(p_{m}))+d_{2}(f(p_{m}), f(q))\leq \epsilon$. ^9db0f1

---

Denote $g=f^{-1}$, and let $C$ be a closed subset of $M_{1}$, $g^{-1}(C)=f(C)$.
Since $C$ is closed subset of a compact set, then $C$ is also compact, then $f(C)$ is closed by virtue of continuity.
Hence $g$ is continuous. ^790b31

---

To show that $\bigcap_{n=1}^{\infty}O_{n}$ is dense in $M$, it's sufficient to show that when we fix $x\in M$ and $\epsilon>0$ , we always have $y\in \bigcap_{n=1}^{\infty}O_{n}$ s.t. $d(x,y)<\epsilon$. 
Since $U_{1}$ is dense in $M$, there exists $y_{1}\in U_{1}\cap B_{\epsilon}(x)$ (By definition of **density**). Since $U_{1}\cap B_{\epsilon}$ is open (two parts are both open), then there exists a ball $B_{\epsilon_{1}}(y_{1})$ s.t. $B_{\epsilon_{1}}(y_{1})\subset U_{1}\cap B_{\epsilon}(x)$. **Let** $\delta_{1}=min\{\frac{\epsilon_{1}}{2}, 1\}$. From now on $B_{\delta_{1}}(y_{1})$ takes the role of $B_{\epsilon}(x)$.
Since $U_{2}$ is dense in $M$, there exists $y_{2}\in U_{2}\cap B_{\delta_{1}}(y_{1})$. Since $U_{2}\cap B_{\delta_{1}}(y_{1})$ is open, there exists an open ball $B_{\epsilon_{2}}(y_{2})\subset U_{2}\cap B_{\delta_{1}}(y_{1})$ is open. **Let** $\delta_{2}=min\{\frac{\epsilon_{2}}{2}, \frac{1}{2}\}$ 
We continue this process inductively. Next, we choose $y_{3}\in U_{3}\cap B_{\delta_{2}}(y_{2})$ (by definition of density) and an open ball $B_{\epsilon_{3}}(y_{3})\subset U_{3}\cap B_{\delta_{2}}(y_{2})$, we **let** $\delta_{3}=min\{\frac{\epsilon_{3}}{2}, \frac{1}{2}\}$ 
We now obtain a sequence $\{y_{n}\}$ and open balls $\{B_{\epsilon_{n}}(y_{n})\}$ and $\{B_{\delta_{n}}(y_{n})\}$ satisfying 
1).  $B_{\epsilon_{n+1}}\subset U_{n+1}\cap B_{\delta_{n}}(y_{n})$ 
2).  $\delta_{n}=min\{\frac{\epsilon_{n}}{2}, \frac{1}{n}\}$, for $n=1, 2, \dots$ 
Now $B_{\delta_{n+1}}(y_{n+1})\subset B_{\epsilon_{n+1}}(y_{n+1})\subset B_{\delta_{n}}(y_{n})$, thus
$y_{m}\in B_{\delta_{n}}(y_{n})$ for $m>n$
Since $\delta_{n}\leq \frac{1}{n}$, we have $d(y_{m}, y_{n})<\frac{1}{n}$ if $m>n$ (review the choice of $y_{n}$), and therefore $\{y_{n}\}$ is a **Cauchy sequence**. Since $M$ is a **complete metric space**, $y_{n}\rightarrow y$ for $y$ in $M$. $y\in\overline{B_{\delta_{n}}(y_{n})}$ 
Since $\delta_{n}\leq\frac{\epsilon_{n}}{2}$, we have $y\in \overline{B_{\delta_{n}}(y_{n})}\subset \overline{B_{\frac{\epsilon_{n}}{2}}(y_{n})}\subset B_{\epsilon_{n}}(y_{n})\subset U_{n}$ for $n=1,2, \dots$ 
Therefore $y\in \bigcap_{n=1}^{\infty}U_{n}$
Finally, since $B_{\epsilon_{1}}(x_{1})\subset B_{\epsilon}(x)$, then $d(y,x)< \epsilon$. ^d1dfc3

---

Suppose that $M$ is complete but of the 1-st category, then $M=\bigcup_{n=1}^{\infty} A_{n}$, where $\{A_{n}\}$ are nowhere dense.
$M=\bigcap_{n=1}^{\infty}\overline{A_{n}}$, then $\varnothing=M^{c}=\bigcup_{n=1}^{\infty}\overline{A_{n}}^{c}$, here we notice that $\overline{A_{n}}^{c}$ is open and dense.
$\varnothing=\bigcup_{n=1}^{\infty}\overline{\overline{A_{n}}^{c}}$ , then by the previous [[004 Two Fundamental Theorems for Complete Metric Spaces#^a19c2e|theorem]], $\varnothing$ is dense, but this is absurd. Hence we obtain the theorem. ^491b25

---

Suppose $M$ is countable. Then $M=\bigcup_{i=1}^{\infty}\{a_{n}\}$, and each set is nowhere dense (single point is nowhere dense). Thus $M$ is of first category, and this contradicts [[004 Two Fundamental Theorems for Complete Metric Spaces#^BaireCategoryThm|Theorem]]  ^ea9594

---

Choose any $x_{0}\in M$, define the sequence $\{x_{n}\}$ where
$x_{n+1}=f(x_{n})$, $n=0, 1,\dots$
Want to show that **1).** $\{x_{n}\}$ is a Cauchy Sequence **2).** The limit $x$ is a fixed point of $f$ **3).** The fixed point is unique.
$d(x_{m+1}, x_{m})=d(f(x_{m}), f(x_{m-1}))\leq Kd(x_{m}, x_{m-1})=Kd(f(x_{m-1}), f(x_{m-2}))$
$\leq K^{2}d(x_{m-1}, x_{m-2})\dots \leq K^{m}d(x_{1}, x_{0})$ 
By triangular inequality ($n>m$), $d(x_{m}, x_{n})\leq d(x_{m}, x_{m+1})+\dots+d(x_{n-1}, x_{n})\leq$
$(K^{m}+K^{m+1}+\dots+K^{n})\cdot d(x_{1}, x_{0})=K^{m}\frac{1-K^{n-m}}{1-K}d(x_{0}, x_{1})$ 
Since $0<K<1$, we have $1-K^{n-m}<1$, $d(x_{m}, x_{n})$ is Cauchy
Because $M$ is complete, there exists an $x\in X$ s.t. $x_{n}\rightarrow x$ 
Next, we prove $x$ is a fixed point of $f$, consider $d(x,f(x))$
$d(x, f(x))\leq d(x, x_{m})+d(x_{m}, f(x))=d(x, x_{m})+d(f(x_{m-1}), f(x))\leq$
$d (x, x_{m})+Kd (x_{m-1}, x)$ 
Take $m\rightarrow \infty$, $d(x,f(x))=0\Longrightarrow f(x)=x$
Finally, we prove uniqueness. Suppose there are two fixed points $x$ and $\overline{x}$ of $f$, then $d(x, \overline{x})=d(f(x), f(\overline{x}))\leq Kd(x, \overline{x})$, which implies $d(x,\overline{x})=0\Longrightarrow x=\overline{x}$. ^c210bc

---













