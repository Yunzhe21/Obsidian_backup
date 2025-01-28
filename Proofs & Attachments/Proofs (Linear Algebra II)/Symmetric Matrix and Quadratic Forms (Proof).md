
Choose $x_{1}$ and $x_{2}$ to be two eigenvectors from distinct eigenspaces.
$x_{1}\cdot Ax_{2}=x_{1}^{T}A^{T}x_{2}=(Ax_{1})^{T}x_{2}=\lambda_{1}x_{1}^{T}x_{2}=\lambda_{1}x_{1}\cdot x_{2}$
On the other hand, $x_{1}\cdot Ax_{2}=x_{1}^{T}Ax_{2}=x_{1}^{T}\lambda_{2}x_{2}=\lambda_{2}x_{1}\cdot x_{2}$.
This means that $\lambda_{1}=\lambda_{2}$, which is a contradiction. ^7b0d4f

---

If $A^{T}=A$, $A$ is real and $Ax=\lambda x$, $\lambda\in\mathbb{C}$, $x\in\mathbb{C}^{n}$
$x^{*}Ax=x^{*}Ax=x^{*}\lambda x=\lambda x^{*}x$
On the other hand, $x^{*}Ax=x^{*}A^{*}x=(Ax)^{*}x=(\lambda x)^{*}x=\overline{\lambda}x^{*}x$ 
This means that $\lambda$ is real. ^f8788f

---

"$\Longleftarrow$" is obvious
"$\Longrightarrow$" Let $Ax=\lambda x$, $\lambda\in\mathbb{R}$ for unit vector $x\in \mathbb{R}^{n}$
Vector $x$ can be extended to an orthonormal basis $\{x=x_{1}, x_{2}, \cdots, x_{n}\}$ of $\mathbb{R}^{n}$
Then $A[x_{1}, \cdots, x_{n}]=[x_{1}, \cdots, x_{n}]\begin{pmatrix} \lambda && 0 && \cdots && 0 \\ 0 && && && \\ \vdots && && \ddots && \\ 0 && && && \end{pmatrix}$, the lower part of the latter matrix $M$ is denoted by $B$. The first row of $M$ is $0$ except for the first entry is because $M=[x_{1}, \cdots, x_{n}]^{-1}A[x_{1}, \cdots, x_{n}]$ is symmetric.
Continue this process for $B=B^{T}$, we get an orthogonal matrix $P_{(n-1)\times(n-1)}$ and diagonal $D'$ s.t. $B=PD'P^{-1}$
$A=[x_{1}, \cdots, x_{n}]\begin{pmatrix} \lambda && 0 \\ 0 && \textbf{PD'P}^{-1}\end{pmatrix}[x_{1}, \cdots, x_{n}]^{-1}=X\begin{pmatrix} 1 && 0 \\ 0 && \textbf{P}\end{pmatrix}\begin{pmatrix} \lambda && 0\\ 0 && \textbf{D'}\end{pmatrix}\begin{pmatrix} 1 && 0 \\ 0 && \textbf{P}^{-1}\end{pmatrix}X^{-1}$ ^0eacac

---

"$\Longrightarrow$" since $A=A^{T}$, there exists orthogonal $P$ and $D=\begin{pmatrix} d_{1} && && \\ && \ddots && \\ && && d_{n}\end{pmatrix}$ s.t. $A=PDP^{-1}$
Then $x^{T}Ax=x^{T}PDP^{-1}x=d_{1}y_{1}^{2}+\cdots+d_{n}y_{n}^{2}$ for $y=P^{T}x$.
Since $x^{T}Ax\geq0$ for all $x\in\mathbb{R}^{n}$, we have $d_{i}\geq0$
Also, $x^{T}Ax=0\iff x=0 \iff y=0$, we have $d_{i}>0$. 
"$\Longleftarrow$" is obvious ^47ec87

---

"$\Longrightarrow$" $A=PDP^{-1}=P\begin{pmatrix} d_{1} && && \\ && \ddots && \\ && && d_{n}\end{pmatrix}P^{-1}$ with $d_{i}\geq0$ for all $i$.
Then $A=P\begin{pmatrix} \sqrt{d_{1}} && && \\ && \ddots && \\ && && \sqrt{d_{n}}\end{pmatrix}\begin{pmatrix} \sqrt{d_{1}} && && \\ && \ddots && \\ && && \sqrt{d_{n}}\end{pmatrix}P^{T}$ 
This side is proved by setting $S=P\begin{pmatrix} \sqrt{d_{1}} && && \\ && \ddots && \\ && && \sqrt{d_{n}}\end{pmatrix}$
"$\Longleftarrow$" If $A=SS^{T}$ for some $S$
$x^{T}Ax=x^{T}SS^{T}x=\|x^{T}S\|^{2}\geq0$ for all $x\in\mathbb{R}$ ^9e7db1

---

There exists orthogonal matrix $P=[P_{1}, \cdots, P_{m}]$ and diagonal matrix $D=\begin{pmatrix} \lambda_{1} && && \\ && \ddots && \\ && && \lambda_{m}\end{pmatrix}$, where $\lambda_{1}\geq\lambda_{2}\geq\cdots\geq0$ s.t. $A^{T}A=PDP^{-1}$
$\min_{s\in S^{n-1}}\|Ax\|=\sqrt{\lambda_{m}}=\sigma_{m}$
Consider $AP_{i}\cdot AP_{j}=(AP_{i}^{T})AP_{j}=P_{i}^{T}A^{T}AP_{j}=P_{i}^{T}\lambda_{j}P_{j}=0$ if ${} i\neq j$ (orthogonality).
If $i=j$, $AP_{j}\cdot AP_{j}=\lambda_{j}$, $\|AP_{j}\|=\sqrt{\lambda_{j}}=\sigma_{j}$
Thus $\{AP_{1}, \cdots, AP_{m}\}\subseteq\mathbb{R}^{n}$ is orthogonal.
Suppose $\lambda_{1}\geq\lambda_{2}\geq\cdots\geq\lambda_{k}>\lambda_{k+1}=\cdots=\lambda_{m}=0$, in this sense, we include the case of not being full rank. ($k=\text{rank}(A)$)
Since $\{AP_{1}, \cdots, AP_{m}\}$ is an orthogonal basis for $\text{Col}(A)$
Extend $\{\frac{AP_{1}}{\|AP_{1}\|}, \cdots, \frac{AP_{k}}{\|AP_{k}\|}\}$ to be an orthonormal basis of $\mathbb{R}^{n}$ $\{v_{1}, \cdots, v_{n}\}$
Then when we consider linear map $A$ from one basis to another, we may observe that 
$P_{1}\longmapsto AP_{1}=\|AP_{1}\|v_{1}=\sigma_{1}v_{1}$
$\vdots$
$P_{k}\longmapsto AP_{k}=\|AP_{k}\|v_{k}=\sigma_{k}v_{k}$
$P_{k+1}\longmapsto AP_{k+1}=0$
$\vdots$
$P_{m}\longmapsto AP_{m}=0$ ^426715

---

$B_{n\times m}=P\begin{pmatrix} \sigma_{1} && 0 && \cdots && 0 \\ && \ddots && && \\ && && \sigma_{k} && \\ 0 && \cdots && \cdots && \textbf{0}\end{pmatrix}Q$, then
${} B^{T}B=Q^{T}\begin{pmatrix} \sigma_{1}^{2} && 0 && \cdots && 0 \\ && \ddots && && \\ && && \sigma_{k}^{2} && \\ 0 && \cdots && \cdots && \textbf{0}\end{pmatrix}Q {}$
$BB^{T}=P\begin{pmatrix} \sigma_{1}^{2} && 0 && \cdots && 0 \\ && \ddots && && \\ && && \sigma_{k}^{2} && \\ 0 && \cdots && \cdots && \textbf{0}\end{pmatrix}P^{T}$

---



