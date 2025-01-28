
Let $n$ be an integer and $g(t)=t-np$, then $g$ is strictly increasing on $[a+np,a+(n+1)p]$. 
We have $(f\circ g)g'\in\mathscr{R}[a+np,a+(n+1)p]$, however, $(f\circ g)g'(t)=f(t-np)=f(t)$, hence $f$ is Riemann integrable on $[a+np,a+(n+1)p]$ for arbitrary $n$, then $f$ is Riemann integrable on $\mathbb{R}$.
We notice that $\int_{p}^{c+p}f(t)dt=\int_{0}^{c}f(t+p)dt=\int_{0}^{c}f(t)dt$
Then $\int_{c}^{c+p}f(t)dt=\int_{c}^{p}f(t)dt+\int_{p}^{c+p}f(t)dt=\int_{c}^{p}f(t)dt+\int_{0}^{c}f(t)dt=\int_{0}^{p}f(t)dt$  ^dea7ac

---

We first extend $\mathbb{N}$ to $\mathbb{Q}$.
If $p=\frac{n}{m}$, where $m,n$ are two positive integers, then $[E(p)]^{m}=E(mp)=E(n)=e^{n}$, then $E(p)=e^{p}$ ($p>0$, $p$ rational)
Then by property $E(z)E(-z)=1$, we have $E(-p)=e^{-p}$, thus the extension is done.
Then we extend $\mathbb{Q}$ to $\mathbb{R}$.
Define $e^{x}=\sup e^{p}$ ($p<x$, $p$ rational), since $E$ is monotone and increasing, $E(x)=e^{x}$. ^6b455a

---

By definition, $e^{x}>\frac{x^{n+1}}{(n+1)!}$ for $x>0$, so that $x^{n}e^{-x}<\frac{(n+1)!}{x}$
We obtain the property. ^adda82

---

Since $C^{2}(x)+S^{2}(x)=1$, then $C^{2}(x)=1-S^{2}(x)\leq1$
Then $C(x)\in[-1,1]$, the conclusion is clear. ^edf180

---

Suppose $0<t<\pi/2$ , and $E(it)=x+iy$ with $x,y$ real, we know that $0<x<1, 0<y<1$.
Note that $E(4it)=(x+iy)^{4}=x^{4}-6x^{2}y^{2}+y^{4}+4ixy(x^{2}-y^{2})$

---

Recall the identity: $\sin(u+v)-\sin(u-v)=2\sin(v)\cos(u)$
We have $\sin[(k+\frac{1}{2})t]-\sin[(k-1+\frac{1}{2})t]=2\sin(\frac{t}{2})\cos(kt)$
Since:  $\sin[(n+\frac{1}{2})t]-\sin(\frac{1}{2})=\sum\limits_{k=1}^{n}\{\sin[(k+\frac{1}{2})t]-\sin[(k-1+\frac{1}{2})]\}$
$= \sum\limits_{k=1}^{n}2\sin(\frac{t}{2})\cos(kt)$
That lead to what we want. ^9d7a2d

---

Define $g_{1}(t)=g(t)$ on $\delta\leq|t|\leq\pi$ and 0 otherwise; define $g_{2}(t)=g(t)\cot(t/2)$ in a similar manner.
By [[002 Fourier Series#^13ac64|Riemann-Lebesgue Lemma]], 
$\lim_{n\rightarrow\infty}\int_{-\pi}g_{1}(t)\cos(nt)dt=0=\lim_{n\rightarrow\infty}\int_{-\pi}^{\pi}g_{2}(t)\sin(nt)dt$
Since when $\delta\leq|t|\leq\pi$, $D_{n}(t)=\frac{\sin[(n+1/2)t]}{2\sin(t/2)}$
$\text{LHS}=(\int_{-\pi}^{-\delta}+\int_{\delta}^{\pi})g(t)D_{n}(t)dt=(\int_{-\pi}^{-\delta}+\int_{\delta}^{\pi})g(t)\frac{\sin(nt)\cos(t/2)+\sin(t/2)\cos(nt)}{2\sin(t/2)}dt$
$=\frac{1}{2}(\int_{-\pi}^{-\delta}+\int_{\delta}^{\pi})g(t)(\cot(t/2)\sin(nt)+\cos(nt))dt$
$=\frac{1}{2}[\int_{-\pi}^{\pi}g_{2}(t)\sin(nt)+\int_{-\pi}^{\pi}g_{1}(t)\cos(nt)dt]\rightarrow0$. ^6e1316

---

Suppose $f'(x)=\lim_{y\rightarrow x}\frac{f(y)-f(x)}{y-x}$
Taking $\epsilon=1$, then there exists  $\delta>0$ s.t. if $0<|y-x|\leq\delta$, then $\bigr|\frac{f(y)-f(x)}{y-x}-f'(x)\bigr|<1$
Thus $|f(y)-f(x)|\leq(1+|f'(x)|)|y-x|$  ^55d110

---

It is sufficient to prove that $\lim_{n\rightarrow\infty}\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)D_{n}(t)dt=f(x)$
By [[003 Pointwise Convergence of Fourier Series#^5faef0|Theorem]], we have $f(x)=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)D_{n}(t)dt$
Then we have to show that $\lim_{n\rightarrow\infty}\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x-y)-f(x)]D_{n}(t)dt=0$
Let $\epsilon>0$, since
$\lim_{t\rightarrow0}\frac{1\sin(t/2)}{t}=1$, there exist constant $k$ and $\delta_{1}$, $0<\delta_{1}<\pi$ s.t.
$|\frac{t}{2\sin(t/2)}|<k$ for all $0<|t|\leq\delta_{1}$
Thus for any positive integer $n$, if $0<|t|\leq\delta_{1}$, we have 
$|tD_{n}(t)|=|\frac{t}{2\sin(t/2)}\sin[(n+\frac{1}{2})t]|<k$ 
If $t=0$, $tD_{n}(t)=0$, so that 
$|tD_{n}(t)|<k$ for all $|t|\leq\delta_{1}$ and $n$ a positive number
Because of Lipschitz condition, there exists $\delta_{2}>0$ and $M>0$ s.t.
$|f(x)-f(y)|\leq M|x-y|$ for $|x-y|\leq\delta_{2}$ 
Let $\delta=\min\{\delta_{1},\delta_{2}, \epsilon/(4Mk)\}$
$|\int_{-\delta}^{\delta}[f(x-t)-f(t)]D_{n}(t)dt|\leq\int_{-\delta}^{\delta}|f(x-t)-f(x)||D_{n}(t)|dt\leq\int_{-\delta}^{\delta}M|t||D_{n}(t)|dt$ 
$\leq\int_{-\delta}^{\delta}Mkdt=2Mk\delta\leq\frac{\epsilon}{2}$
Combine with the fact that $\lim_{n\rightarrow\infty}\bigr [\int_{-\pi}^{-\delta}g(t)D_{n}(t)dt+\int_{\delta}^{\pi}g(t)D_{n}(t)dt\bigr]=0$, the conclusion is obtained. ^a8ebd5

---

$K_{n}(t)=\frac{1}{n+1}\sum\limits_{k=0}^{n}D_{k}(t)=\frac{1}{n+1}\sum\limits_{k=0}^{n}\frac{\sin[(k+1/2)t]}{2\sin(t/2)}$
$=\frac{1}{2(n+1)\sin^{2}(t/2)}\sum\limits_{k=0}^{n}\sin[(k+\frac{1}{2})t]\sin(\frac{t}{2})$ for all $t$ with $\sin(t/2)\neq0$
Use the identity $\cos(u-v)-\cos(u+v)=2\sin(u)\sin(v)$
Taking $u=(k+\frac{1}{2})t$ and $v=t/2$, we have
$\frac{\cos(kt)-\cos[(k+1)t]}{2}=\sin[(k+\frac{1}{2})t]\sin(\frac{t}{2})$
Then by telescoping sum
$\frac{1-\cos[(n+1)t]}{2}=\sum\limits_{k=0}^{n}\frac{\cos(kt)-\cos[(k+1)t]}{2}=\sum\limits_{k=0}^{n}\sin[(k+1/2)t]\sin(t/2)$
Also, $\frac{1-\cos[(n+1)t]}{2}=\sin^{2}[(n+1)t/2]$
The conclusion follows. ^099c21

---

$|\sigma-f(x)|=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)K_{n}(t)dt-f(x)=\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x-t)-f(x)]K_{n}(t)dt\leq\frac{1}{\pi}\int_{-\pi}^{\pi}|f(x-t)-f(x)|K_{n}(t)dt$
when $|t|\leq\delta<\pi$, $|(x-t)-x|\leq\delta$, then $|f(x-t)-f(x)|\leq\frac{\epsilon}{4}$ (uniform convergence of $f$)
$\frac{1}{\pi}\int_{-\delta}^{\delta}|f(x-t)-f(x)|K_{n}(t)dt\leq\frac{\epsilon}{4\pi}\int_{-\delta}^{\delta}K_{n}(t)dt\leq\frac{\epsilon}{4\pi}\int_{-\pi}^{\pi}K_{n}(t)dt=\frac{\epsilon}{4}$ for all $n$
There exists $N$ s.t. if $n\geq N$ and $\delta\leq\pi$, $K_{n}(t)\leq\frac{\epsilon}{16M}$, where $|f|$ is bounded by $M$
Then $\frac{1}{\pi}(\int_{-\pi}^{-\delta}+\int_{\delta}^{\pi})|f(x-t)-f(x)|K_{n}(t)dt\leq\frac{1}{\pi}\int_{-\pi}^{\pi}2M\frac{\epsilon}{16M}=\frac{\epsilon}{4}$
In conclusion, $|\sigma(x)-f(x)|\leq\frac{1}{\pi}\int_{-\pi}^{\pi}|f(x-t)-f(x)|K_{n}(t)dt=\frac{1}{\pi}(\int_{-\pi}^{-\delta}+\int_{\delta}^{\pi})|f(x-t)-f(x)|K_{n}(t)dt+\frac{1}{\pi}\int_{-\delta}^{\delta}|f(x-t)-f(x)|K_{n}(t)dt$ $\leq\frac{\epsilon}{2}<\epsilon$ for all $x$. ^978497

---

Let $f\in CP[a,a+2\pi]$, let $\{s_{n}\}$ be a sequence of partial sums of Fourier Series, $\{\sigma_{n}\}$ be the sequence of Cesaro Sums.
$\forall\epsilon>0$, exists $N$ s.t. if $n\geq N$, then $|f(x)-\sigma_{n}(x)|<\frac{\sqrt{\epsilon}}{2\sqrt{\pi}}$ 
Thus if $n\geq N$, $\|f-\sigma_{n}\|^{2}=\int_{a}^{a+2\pi}(f-\sigma_{n})^{2}\leq\int_{a}^{a+2\pi}\frac{\epsilon}{4\pi}=\frac{\epsilon}{2}$
Then $\|f(x)-s_{n}(x)\|\leq\|f(x)-\sigma_{n}(x)\|\leq\frac{\epsilon}{2}<\epsilon$. ^c7bc50

---

If $z=0$, then $f$ is constant and thus is continuous
Otherwise, let $\epsilon>0$, $\delta=\epsilon/\|z\|$. If $\|x-y\|<\delta$, then 
$|f(x)-f(y)|=|(x-y,z)|\leq\|x-y\|\|z\|\leq\|x-y\|\|z\|<\delta\|z\|=\epsilon$ ^9a699a

---

$\|x-z_{n}\|^{2}=\|x\|^{2}-\sum\limits_{k=1}^{n}(x,x_{k})$
$\|x-y_{n}\|=\|x\|^{2}-\sum\limits_{k=1}^{n}(x,x_{k})^{2}+\sum\limits_{k=1}^{n}[(x,x_{k})-c_{k}]^{2}$
Then it's obvious to see the conclusion. ^a76f60

---

Taking $c_{k}=(x,x_{k})$, we have
$\|x\|^{2}-\sum\limits_{k=1}^{n}(x,x_{k})^{2}=\|x-y\|^{2}\geq0$
Then for every $n$, 
$\sum\limits_{k=1}^{n}(x,x_{k})^{2}\leq\|x\|^{2}$ ^cf9740

---

Let $x,y\in V$. Then $x=\sum\limits_{n=1}^{\infty}(x,x_{n})x_{n}$, $y=\sum\limits_{m=1}^{\infty}(y,x_{m})x_{m}$
By [[001 Preliminary Knowledge#^25e832|Corollary]], we have
$(x,y)=(\sum\limits_{n=1}^{\infty}(x,x_{n})x_{n}, \sum\limits_{m=1}^{\infty}(y,x_{m})x_{m})=\sum\limits_{n=1}^{\infty}(x,x_{n})(x_{n}, \sum\limits_{m=1}^{\infty}(y,x_{m})x_{m})=\sum\limits_{n=1}^{\infty}(x,x_{n})\sum\limits_{m=1}^{\infty}(y,x_{m})(x_{n}, x_{m})$
$=\sum\limits_{n=1}^{\infty}(x,x_{n})(y,x_{n})$. ^0ddf22

---

If $(x,x_{n})=0$ for all $n$. Then by 2, $\|x\|^{2}=\sum\limits_{n=1}^{\infty}(x,x_{n})^{2}=0$ ^b83575

---

Suppose $x\notin X$ and $X\cup\{x\}$ is an orthonormal set. Then $(x,x_{n})=0$ for all $n$. Then by 3, $x=0$, which is impossible. ^740066

---







