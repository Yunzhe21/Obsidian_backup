
Suppose $\{f_{n}\}$ converges uniformly to $f$, then $\forall\epsilon>0$, $\exists N>0$ s.t. whenever $n,m>N$, we have
$|f_{n}-f|<\frac{\epsilon}{2}$ and $|f_{m}-f|<\frac{\epsilon}{2}$ 
Then $|f_{m}-f_{n}|\leq |f_{m}-f|+|f_{n}-f|<\epsilon$, satisfying the Cauchy criteria
Conversly, if the Cauchy Criteria holds, then $\{f_{n}(x)\}$ converges pointwise.
Let $\epsilon>0$, choose that $N>0$ s.t. whenever $n,m>N$, $|f_{m}(x)-f_{n}(x)|<\epsilon$
Let $n$ approaches $+\infty$, $f_{n}(x)\rightarrow f(x)$, then $|f_{m}(x)-f(x)|<\epsilon$ for all $x$.
Hence uniformly convergent. ^505a69

---

Let $\{f_{n}\}$ be a Cauchy Sequence of bounded functions on $[a,b]$, then
$\forall\epsilon>0$, $\exists N>0$ s.t whenever $m,n>N$, we have $d(f_{m}, f_{n})<\epsilon\iff \|f_{m}-f_{n}\|_{\infty}<\epsilon$, which is exactly the equivalence of the Cauchy Criteria.
Thus $\{f_{n}\}$ converges uniformly to $f$
Want to show that this $f$ is also bounded. This is obvious since $-\epsilon+f_{n}(x)<f(x)<f_{n}(x)+\epsilon$ for $n$ sufficiently large. Since $f_{n}(x)$ is bounded, then $f(x)$ is also bounded. 
Hence complete. ^fd405e

---

$f_{n}\rightarrow f$ uniformly, then for $\epsilon>0$, $\exists N>0$ s.t. whenever $n\geq N$, $|f_{n}(x)-f(x)|<\frac{\epsilon}{3}$ for all $x\in M$.
Let $n=N$, $|f_{N}(x)-f(x)|<\frac{\epsilon}{3}$ for all $x\in M$
Since $f_{N}$ is continuous at $x_{0}$, $\exists\delta_{0}>0$ s.t. whenever $d(x,x_{0})<\delta_{0}$, $|f_{N}(x_{0})-f_{N}(x)|<\frac{\epsilon}{3}$ 
Then if $d(x,x_{0})<\delta_{0}$, $|f(x)-f(x_{0})|\leq |f(x)-f_{N}(x)|+|f_{N}(x_{0})-f_{N}(x)|+|f_{N}(x_{0})-f(x_{0})|<\epsilon$.
Hence $f$ is continuous. ^abcf77

---

Consider $g_{n}(x)=f_{n}(x)-f(x)$, we easily know that $g_{n}$ is continuous and $\{g_{n}\}$ is decreasing. Also, $g_{n}$ converges pointwise to 0.
Let $\epsilon$ be given, consider $K_{n}=\{x\in [a,b]: g_{n}(x)\geq\epsilon\}$ 
We can see that $K_{n}\supseteq K_{n+1}$, since $g_{n}\rightarrow 0$ pointwise, then $x\notin K_{n}$ for $n$ is sufficiently large.
$\bigcap K_{n}$ is empty $\Longrightarrow$ $K_{n}$ is empty for some $N$ (this can be proved by contradiction.)
$\Longrightarrow$ $K_{n}$ is empty for $n\geq N$ (recall the definition of $K_{n}$ and $K_{n}\supseteq K_{n+1}$)  
Hence for $n\geq N$, $0\leq g_{n}(x)\leq\epsilon$ for all $x\in [a, b]$ 
Hence we obtain Dini's Theorem. ^fe3c96

---

Write $f(x)=f_{n}(x)+(f(x)-f_{n}(x))$
Since $f_{n}(x)$ converges uniformly to $f$, then $\forall\epsilon>0$, $\exists N$ s.t. whenever $n\geq N$, we have $|f(x)-f_{n}(x)|<\epsilon$.
Since $f_{N}\in \mathscr{R}[a,b]$, then $\forall\epsilon>0$, $\exists$ partition $P$ s.t. $\mathscr{U}(f_{N}, P)-\mathscr{L}(f_{N}, P)<\epsilon$ 
$\mathscr{U}(f, P)-\mathscr{L}(f, P)< \mathscr{U}(f_{N}, P)-\mathscr{L}(f_{N}, P)+2\epsilon\cdot(b-a)$, then $f\in\mathscr{R}[a, b]$
Notice that  $|\int_{a}^{b}(f_{n}(x)-f(x))dx|\leq\int_{a}^{b}|f_{n}(x)-f(x)|dx\leq\epsilon\cdot(b-a)$, then 
$\int_{a}^{b}f_{n}(x)dx\rightarrow\int_{a}^{b}f(x)dx$ as $n\rightarrow\infty$.  ^cacde9

---

Let $\epsilon>0$, choose $N$ s.t. whenever $m,n>N$, $|f_{m}(x_{0})-f_{n}(x_{0})|<\frac{\epsilon}{2}$ (pointwise convergence of $f_{n}$), and $|f'_{m}(x)-f'_{n}(x)|<\frac{\epsilon}{2(b-a)}$ (uniform convergence of $f'_{n}$)
$|f_{m}(x_{0})-f_{n}(x_{0})-f_{m}(x)+f_{n}(x)|<\frac{|x-t|\epsilon}{2(b-a)}\leq \frac{\epsilon}{2}$ (Mean value Theorem)
For $|f_{m}(x)-f_{n}(x)|\leq |f_{m}(x)-f_{n}(x)-f_{m}(x_{0})+f_{n}(x_{0})|+|f_{m}(x_{0})-f_{n}(x_{0})|<\epsilon$.
Hence $\{f_{n}\}$ converges uniformly.
Define $\phi_{n}(t)=\frac{f_{n}(t)-f_{n}(x)}{t-x}$, $\phi(t)=\frac{f(t)-f(x)}{t-x}$, then $\lim_{t\to x}\phi_{n}(t)=f'_{n}(x)$ 
$\phi_{n}(t)-\phi_{m}(t)<\frac{\epsilon}{2(b-a)}$ for $m,n>N$, then $\phi(t)$ converges uniformly for $t\neq x$.
Since $f_{n}$ converges uniformly to $f$, then $\lim_{n\to\infty}\phi_{n}(t)=\phi(t)$ for $t\neq x$
Then $\lim_{t\to x}\phi(t)=\lim_{n\to\infty}f'_{n}(t)$  
**The last step can be better explained through Rudin's analysis.**
![[Pasted image 20231221104313.png]]
^113c33

---

Just need to prove that the sequence of partial sums $\{S_{n}(x)\}$ is Cauchy in $\mathscr{L}^{\infty}(X)$ 
$\forall\epsilon>0$, $\exists N$ s.t. whenever $m,n>0$, we have $|S_{m}(x)-S_{n}(x)|=\bigr|\sum\limits_{i=n+1}^{m}u_{i}(x)\bigr|$  
$\leq\sum\limits_{i=n+1}^{m}M_{i}<\epsilon$ when choose $N$ sufficiently large (because $\sum\limits_{i=1}^{\infty}M_{i}<\infty$)  ^1ae6f5

---

$a_{n}(x-t)^{n}<|a_{n}|S^{n}$, and since $0<S<R$, $\sum\limits_{n=0}^{\infty}|a_{n}|S^{n}$ converges
By [[003 Series of Functions#^WeierstrassMTest|Weierstrass M-Test]], $\sum\limits_{n=0}^{\infty}a_{n}(x-t)^{n}$ converges uniformly. ^697eaa

---

Using mathematical Induction:
First, we know that $a_{0}$ must be 0, when we take $x=x_{0}$
Assume that $a_{j}=0$ for $j\leq k$, want to show that $a_{k+1}=0$
$\sum\limits_{n=0}^{\infty}a_{n}(x-x_{0})^{n}=a_{k+1}(x-x_{0})^{k+1}+a_{k+2}(x-x_{0})^{k+2}+\dots=(x-x_{0})^{k+1}[a_{k+1}+(x-x_{0})a_{k+2}+\dots]$
Given that the series is convergent, the latter part, denote it as $f$, must vanish for $0<|x-x_{0}|<R$
Since $\lim_{x\to x_{0}}f(x)=f(x_{0})=0$ (continuity of $f$), then $a_{k+1}=0$. ^9a3384

---

$|\sum\limits_{m+1}^{n}u_{k}v_{k}|\leq |\sum\limits_{m+1}^{n-1}S_{k}(v_{k}-v_{k+1})|+|S_{n}v_{n}|$, where $S_{k}=\sum\limits_{j=m+1}^{k}u_{j}(x)$ by Summation by parts
$\forall\epsilon>0$, $\sum\limits_{n=1}^{\infty}u_{n}(x)$ converges uniformly on $X\Longrightarrow$ $\exists N\in \mathbb{N}$ s.t. $\forall m,n\geq N$, $|\sum\limits_{m+1}^{n}u_{k}(x)|<\frac{\epsilon}{3M}$. For $m,n\geq N$ and $|v_{k}(x)|\leq M$ for $k=1,2,\dots$ $\forall x\in X$
Then $|S_{n}v_{n}|\leq\frac{\epsilon}{3M}M=\frac{\epsilon}{3}$
$|\sum\limits_{m+1}^{n-1}S_{k}(v_{k}-v_{k+1})|\leq\sum\limits_{m+1}^{n-1}|S_{k}|(v_{k-1}-v_{k})\leq\frac{\epsilon}{3M}\sum\limits_{m+1}^{n-1}(v_{k-1}-v_{k})=(v_{m}-v_{n})\frac{\epsilon}{3M}\leq\frac{2M}{3M}\epsilon$ In conclusion, $|\sum\limits_{m+1}^{n}u_{k}v_{k}|\leq \epsilon$ ^7cc85e

---

Let $u_{n}(x)=a_{n}$, $\sum\limits_{n=0}^{\infty}a_{n}$ converges, then $\sum\limits_{n=0}^{\infty}u_{n}(x)$ converges uniformly
Let $v_{n}(x)=x^{n}$ with  $x\in[0,1]$, $v_{n}\geq v_{n+1}$ and bounded by $1$
The Abel Test tells us that $\sum\limits_{n=0}^{\infty}a_{n}x^{n}$ converges uniformly on $[0,1]$ ^a2fb48

---

If $f(x)=\sum\limits_{n=0}^{\infty}a_{n}x^{n}$ converges for $|x|<1$ and $\lim_{x\to1^{-}}f(x)=s$
Since $n|a_{n}|\rightarrow0$, then for $\sigma_{n}=\frac{|a_{1}|+2|a_{2}|+\dots+n|a_{n}|}{n}\rightarrow0$ as $n\rightarrow\infty$
<font color="#ff0000">Goal:</font> let $S_{n}=\sum\limits_{j=0}^{n}a_{j}$, then $S_{n}\rightarrow s$ as $n\rightarrow\infty$
$\forall\epsilon>0$, $\exists n\geq N$ s.t. $|f(1-\frac{1}{n})-s|<\frac{\epsilon}{3}$, $\sigma_{n}<\frac{\epsilon}{3}$, and $n|a_{n}|<\frac{\epsilon}{3}$ 
$S_{n}-s=f(x)-s+S_{n}-f(x)=f(x)-s+(S_{n}-\sum\limits_{j=0}^{n}a_{j}x^{j})-\sum\limits_{j=n+1}^{\infty}a_{j}x^{j}$  
($x=1-\frac{1}{n}$)
$|S_{n}-\sum\limits_{j=0}^{n}a_{j}x^{j}|=|\sum\limits_{j=0}^{\infty}a_{j}(1-x^{j})|\leq\sum\limits_{j=0}^{\infty}|a_{n}|(1-x^{j})\leq(1-x)n\sum\limits_{n=0}^{\infty}\frac{|a_{j}|j}{n}=\sigma_{n}$ 
$\sum\limits_{j=n+1}^{\infty}a_{j}x^{j}=\sum\limits_{j=n+1}^{\infty}a_{j}j\frac{x^{j}}{j}\leq \frac{\epsilon}{3}\frac{\sum\limits_{j=n+1}^{\infty}a_{j}}{n+1}=\frac{\epsilon}{3}\frac{x^{n+1}}{(1-x)(n+1)}<\frac{\epsilon}{3}$ 
Then by using the triangular inequality, we obtain the conclusion. ^5a8071

---

Given $\sum\limits_{n=0}^{\infty}a_{n}$, define $s_{n}=\sum\limits_{j=0}^{n}a_{j}$, $S_{n}=\sum\limits_{j=0}^{n}s_{j}$
Observe that $(1-x)\sum\limits_{n=0}^{\infty}s_{n}x^{n}=\sum\limits_{n=0}^{\infty}s_{n}(x^{n}-x^{n+1})=\sum\limits_{n=0}^{\infty}(s_{n}-s_{n-1})x^{n}=\sum\limits_{n=0}^{\infty}a_{n}x^{n}$ 
The second equality is given by virtue of [[005 Abel Limit Theorem#^SummationByParts|Summation By Parts]], because
$\sum\limits_{n=0}^{m}(s_{k}-s_{k-1})x^{k}=\sum\limits_{n=0}^{m-1}s_{n}(x^{k}-x^{k+1})+s_{m}x^{m}$, then take limit from both sides (Notice that $|x|<1$).
Further, we notice that $(1-x)\sum\limits_{n=0}^{\infty}S_{n}x^{n}=\sum\limits_{n=0}^{\infty}(S_{n}-S_{n-1})x^{n}=\sum\limits_{n=0}^{\infty}s_{n}x^{n}$
Hence $(1-x)^{2}\sum\limits_{n=0}^{\infty}S_{n}x^{n}=\sum\limits_{n=0}^{\infty}a_{n}x^{n}$ 
$\sum\limits_{n=0}^{\infty}a_{n}x^{n}=(1-x)^{2}\sum\limits_{n=0}^{\infty}S_{n}x^{n}=\sum\limits_{n=0}^{\infty}(n+1)x^{n}(1-x)^{2}\frac{S_{n}}{n+1}$
Important fact: $\sum\limits_{n=0}^{\infty}(n+1)x^{n}=(1-x)^{-2}$
$|\sum\limits_{n=0}^{\infty}a_{n}x^{n}-s|=|\sum\limits_{n=0}^{\infty}(n+1)x^{n}(1-x)^{2}(\frac{S_{n}}{n+1}-s)|\leq \sum\limits_{n=0}^{N}(n+1)x^{n}(1-x)^{2}|\frac{S_{n}}{n+1}-s|+\sum\limits_{n=N+1}^{\infty}(n+1)x^{n}(1-x)^{2}|\frac{S_{n}}{n+1}-s|$
$\forall\epsilon>0:$ $\exists N$ s.t. $|\frac{S_{n+1}}{n+1}-s|<\frac{\epsilon}{2}$, then the second term $\leq\frac{\epsilon}{2}\sum\limits_{N+1}^{\infty}(n+1)x^{n}(1-x)^{2}\leq\frac{\epsilon}{2}$
For fixed $N$, the absolute value of the first term $\leq\frac{\epsilon}{2}\sum\limits_{n=0}^{N} M(1-x)^{2}\leq\frac{\epsilon}{2}$ if $|x-1|<\delta_{n}$. 
Then the statement is proved. ^b4b41d

---











