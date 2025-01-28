
It is sufficient to consider $P^{*}=P\cup\{x_{i}^{*}\}$, $x_{i}^{*}\in (x_{i-1},x_{i})$
$U(f,P)=\sum\limits_{j=1}^{n}M_{j}\Delta x_{j}$ 
$U(f,P^{*})=\sum\limits_{j=1,j\neq i}^{n}M_{j}\Delta x_{j}+M_{i}^{'}(x^{*}-x_{i-1})+M_{i}^{''}(x_{i}-x^{*})\leq U(f,P)$, where $M_{i}^{'}=\sup\{f(x):x\in[x_{i-1},x^{*}\}$ and $M^{''}\sup\{f(x): x\in[x^{*},x_{i}]\}$ 
The same with the lower sum. ^0d846e

---

"$\Longleftarrow$" $\mathscr{L}(f,P)\leq \underline{\int_{a}^{b}}fdx\leq\overline{\int_{a}^{b}}fdx\leq U(f,P)$, then if $\forall\epsilon>0:\exists P$ s.t. $U(f,P)-\mathscr{L}(f,P)<\epsilon\Longrightarrow \underline{\int_{a}^{b}}fdx=\overline{\int_{a}^{b}}fdx$, then $f$ is Riemann Integrable.
"$\Longrightarrow$" $\forall\epsilon>0:$ since $f\in\mathscr{R}[a,b]\Longrightarrow\overline{\int_{a}^{b}}fdx=\inf\{U(f,\hat{P})\}$, exists $P_{1}$ s.t. $\overline{\int_{a}^{b}}fdx\leq U(f,P_{1})<\overline{\int_{a}^{b}}fdx+2\epsilon$
Similarly, there exists $P_{2}$ s.t. ${} \mathscr{L}(f,P_{2})+\epsilon/2\leq\underline{\int_{a}^{b}}fdx<\mathscr{L}(f,P_{2}) {}$ 
Let $P=P_{1}\cup P_{2}$, then
$-\epsilon/2+\underline{\int_{a}^{b}}fdx\leq\mathscr{L}(f,P_{2})\leq\mathscr{L}(f,P)\leq U(f,P)\leq U(f,P_{1})\leq\overline{\int_{a}^{b}}fdx+\epsilon/2$ 
Thus $U(f,P)-\mathscr{L}(f,P)<\epsilon$. ^f60ab3

---

Since $f$ is continuous on $[a,b]$, $f$ is uniformly continuous.
$\forall\epsilon>0$, $\exists \delta>0$ s.t. whenever $|x-y|<\delta$, $|f(x)-f(y)|<\frac{\epsilon}{b-a}$
Now divide $[a,b]$ equally into n-smaller intervals s.t. $\frac{b-a}{n}<\delta$, for this equal partition $P_{\delta}$ 
$U(f,P_{\delta})-\mathscr{L}(f,P_{\delta})=\sum\limits_{i=1}^{n}(M_{i}-m_{i})\Delta x_{i}<\frac{\epsilon}{b-a}\sum\limits_{i=1}^{n}\Delta x_{i}=\epsilon$ ^a61b7e

---

Let $P: a=x_{0}<x_{1}<\cdots<x_{n}=b$, $\Delta x_{i}=\frac{b-a}{n}$
$U(f,P)-\mathscr{L}(f,P)-\sum\limits_{i=1}^{n}(M_{i}-m_{i})\Delta x_{i}=\frac{b-a}{n}\sum\limits_{i=1}^{n}(f(x_{i})-f(x_{i-1}))=\frac{b-a}{n}(f(b)-f(a))<\epsilon$
for n large. ^debd58

---

Since $g\in C[m,M]$, then $g$ is uniformly continuous, which means that $\forall\epsilon>0, \exists\delta<\frac{\epsilon}{4K+1}$ s.t. if $|y_{1}-y_{2}|<\delta$, then $|g(y_{1})-g(y_{2})|<\epsilon/2(b-a)$, where $K=\max|g(x)|$.
Since $f\in\mathscr{R}[a,b]$, for all $\delta^{2}>0$ there exists partition $P$ s.t. $U(f,P)-\mathscr{L}(f,P)<\delta^{2}$
Let $h(x)=g\circ f(x)$, partition $P: x_{0}=a<x_{1}<\cdots<x_{n}=b$ and $M^{*},m^{*}$ just as convention for $h$ and $M,m$ for $f$.
Let $A=\{i: M_{i}-m_{i}<\delta\}$ and $\{i: M_{i}-m_{i}\geq\delta\}$ 
For $f$, $\delta^{2}>U(f,P)-\mathscr{L}(f,P)=\sum\limits_{i=1}^{n}(M_{i}-m_{i})\Delta x_{i}\geq \sum\limits_{i\in B}(M_{i}-m_{i})\Delta x_{i}>\delta\sum\limits_{i\in B}\Delta x_{i}$ 
Thus $\sum\limits_{i\in B}\Delta x_{i}<\delta$ 
$U(h,P)-\mathscr{L}(h,P)=\sum\limits_{i\in A}(M_{i}^{*}-m_{i}^{*})\Delta x_{i}+\sum\limits_{i\in B}(M_{i}^{*}-m_{i})\Delta x_{i}$
Since $\sum\limits_{i\in A}(M_{i}^{*}-m_{i}^{*})\Delta x_{i}<\sum\limits_{i\in A}\frac{\epsilon}{2(b-a)}\Delta x_{i}$, and 
$\sum\limits_{i\in B}(M_{i}^{*}-m_{i}^{*})\Delta x_{i}\leq 2K\sum\limits_{i\in B}\Delta x_{i}\leq 2K\delta<\frac{2K\epsilon}{4K+1}$
Then $U(h,P)-\mathscr{L}(h,P)<\frac{\frac{\epsilon}{2}+\epsilon}{2}=\epsilon$. ^d712a7

---

"$\Longleftarrow$" is obvious from definition
"$\Longrightarrow$" $\forall\epsilon>0:\exists$ partition ${} P: a=x_{0}<x_{1}<\cdots<x_{n}=b {}$ s.t. $U(f,P)=\mathscr{L}(f,P)<\epsilon$ 
Let $P_{n}$ be the equal partition of $[a,b]$ into n-smaller intervals $a=y_{0}<y_{1}<\cdots<y_{n}=b$, $y_{i}-y_{i}=\frac{b-a}{n}$ 
$U(f,P\cup P_{n})-\mathscr{L}(f,P\cup P_{n})<\epsilon$ 
We can always make $P\cup P_{n}$ an equal partition ${} P' {}$, then
$U(f,P')-\mathscr{L}(f,P')<\epsilon$. ^da33d4

---

First want to show that $f\circ g\in\mathscr{R}[c,d]$
Since $f$ is integrable, then $\forall\epsilon>0:\exists$ a partition $P$ of $[c,d]: a=u_{0}<u_{1}<\cdots<u_{n}=b$ s.t. $U(f,P)-\mathscr{L}(f,P)<\epsilon$. Since $g:[c,d]\longrightarrow [a,b]$ is one-one, then $\exists \hat{P}: c=x_{0}<x_{1}<\cdots<x_{n}=d$ s.t. $g(x_{i})=u_{i}$, thus $U(f\circ g,\hat{P})-\mathscr{L}(f\circ g,\hat{P})<\epsilon$, hence $f\circ g\in\mathscr{R}[c,d]$, plus the fact that ${} g'\in\mathscr{R}[c,d] {}$ 
$\Longrightarrow$ $f\circ g(x)g'(x)\in\mathscr{R}[c,d]$
Let $u=g(x)$, $du=g'(x)dx$, $u_{i}-u{i-1}=g(x_{i})-g(x_{i-1})=g'(\hat{x_{i}})\Delta x_{i}$, where $\hat{x_{i}}\in[x_{i-1},x_{i}]$ 
$I=\int_{a}^{b}f(u)du\approx\sum\limits_{i=1}^{n}f(\xi_{i})\Delta u_{i}$, $\xi\in[u_{i-1},u_{i}]$, then $\xi_{i}=g(\hat{x_{i}})$ for $\hat{x_{i}}\in [x_{i-1},x_{i}]$ 
$\approx\sum\limits_{i=1}^{n}f(\xi_{i})g'(\hat{x_{i}})\Delta x_{i}\approx\sum\limits_{i=1}^{n}f\circ g(\hat{x_{i}})g'(\hat{x_{i}})\leadsto\int_{c}^{d}f\circ g(x)g'(x)dx$  ^b77223

---

We know that $f(a)\leq f(x)\leq f(b)$
Then for arbitrary $x_{0}$, denote $E=\{f(x): x>x_{0}\}$ and $F=\{f(x):x<x_{0}\}$ 
Denote $\inf E=f(x_{0}^{+})$, $\sup E=f(x_{0}^{-})$ 
If $f(x^{+})=f(x^{-})$, then $f$ is continuous
Otherwise, for discontinuity points, $E_{n}=\{x\in(a,b): f(x^{+})-f(x^{-})\geq1/n\}$ is not empty for $n=1, 2,\cdots$ 
Also, for each $E_{n}$, then number of elements in it is finite, since the total "jump" cannot be bigger than $f(b)-f(a)$, then $\bigcup_{i=1}^{\infty}E_{n}$ is countable. ^3e2b34

---

**Step 1:** we consider $\mathbb{Q}\cap[a,b]=\{r_{1}, r_{2}, \cdots\}$, look at
$\{f_{n}(r_{1})\}_{n=1}^{\infty}$, then there exists subsequence s.t. $\{f_{1k}\}_{k=1}^{\infty}(r_{1})\longrightarrow f(r_{1})$ 
Then there exists an subsequence of the subsequence $\{1,k\}$ s.t. $\{f_{2k}\}_{k=1}^{\infty}\longrightarrow f(r_{2})$ 
$\vdots$ 
We just choose $f_{ii}$ from the i-th subsequence generated above, then $\{f_{ii}\}_{i=1}^{\infty}(r)\longrightarrow f(r)$ for every rational number in $[a,b]$, and clearly that $f$ is monotone increasing.
**Step 2:** the function $f$ so far is only defined on rational numbers, so for $x\in[a,b]$ but $\neq r_{n}$ for all $n$, there exists an increasing rational sequence $\{r_{jk}\}$ of $\{r_{j}\}$ s.t. it converges to $x$, define $f(x)=\lim_{k\to\infty}f(r_{jk})$ 
For continuity points of $f$, let's say $x_{0}$. Then $x_{0}$ is in between ${} r_{i}<r_{j} {}$, we choose this two rationals carefully s.t. $f(r_{i})-f(r_{j})<\epsilon$, then by the fact that $f_{jj}(x)-f(r_{i})\leq f_{jj}(x)-f(x)\leq f_{jj}(x)-f(x_{j})$, guarenteed by monotonicity, we obtain $\frac{-\epsilon}{2}\leq\liminf_{k\to\infty}(f_{jj}(x)-f(x))\leq \limsup_{k\to\infty}(f_{jj}(x)-f(x))\leq\epsilon$, then $\{f_{jj}\}$ converges pointwise on continuous points
But for non-continuous points, we observe that $f$ can only have at most countable many discontinuity points, we shall list them as $\{x_{1}, x_{2}, \cdots\}$, then we try **Step 1** again, but this time works on $\{f_{jj}\}$ instead. ^2e0cda

---

"$\Longrightarrow$" if $f$ is continuous at $x_{0}$, then $\forall\epsilon>0$: $\exists\delta>0$ s.t. if $|x-x_{0}|<\delta$, we have $|f(x)-f(x_{0})|<\epsilon/2$ $\iff\omega_{f}(x,\delta)<\epsilon\iff \omega_{f}(x)=0$.
"$\Longleftarrow$" the proof is the same since they are all equivalent. ^1320dc

---

Let $A=\{x: \omega_{f}(x)<\epsilon\}$, then for all $x\in A$, there exists open ball $J$ s.t. ${} x\in J$, $\omega_{f}(J)<\epsilon$ 
Since $J\cap[a,b]$ is still open in $[a,b]$, there exists $\delta$ s.t. $(x-\delta,x+\delta)\cap [a,b]\subseteq J\cap[a,b]$.
Thus for $y\in(x-\delta,x+\delta)\cap[a,b]$, $\omega_{f}(y)<\epsilon$, then $A$ is open. ^8038bb

---




