
$\langle y,f(x)\rangle=y^{*}ABx$, $\langle f^{*}(y),x\rangle=(f^{*}(x))^{*}Ax=y^{*}(f^{*})^{*}Ax$ 
$\Longrightarrow AB=(f^{*})^{*}A\Longrightarrow ABA^{-1}=(f^{*})^{*}\Longrightarrow f^{*}=(ABA^{-1})^{*}=(A^{-1})^{*}B^{*}A^{*}=(A^{-1})B^{*}A=f$
Then $A^{-1}B^{*}A=B$, then $B^{*}A^{*}=AB$ ^954051

---

If $f(x)=\lambda x$, $x\neq0$
$\langle x,f(x)\rangle=\langle x,\lambda x\rangle=\lambda\langle x,x\rangle$, also, $\langle f^{*}(x),x\rangle=\langle f(x),x\rangle=\langle \lambda x,x\rangle=\overline{\lambda}\langle x,x\rangle$ 
Then $\lambda$ is real. ^767124

---

If $f(x)=\lambda_{1}x, f(y)=\lambda_{2}y$, where $\lambda_{1}\neq\lambda_{2}$
$\langle x,f(y)\rangle=\langle x,\lambda_{2}y\rangle=\lambda_{2}\langle x,y\rangle$
$\langle f(x),y\rangle=\langle \lambda_{1}x,y\rangle=\lambda_{1}\langle x,y\rangle$
Since all equations above are equal, we have $\langle x,y\rangle=0$ ^8263d2

---

Since $V$ is finite dimensional, linear map $f$ has an eigenvalue over $\mathbb{C}$.
Since $f=f^{*}$, $\lambda\in\mathbb{R}$, there exists a unit vector $v_{1}\in V$ s.t. $f(v_{1})=\lambda v_{1}$
Consider $(\mathbb{F})^{\perp}\subseteq V$, for $x\in (\mathbb{F}v_{1})^{\perp}$, $f(x)\in(\mathbb{F}v_{1})^{\perp}$
That is because $\langle f(x),v_{1}\rangle=\langle f^{*}(x),v_{1}\rangle=\langle x,f(v_{1})\rangle=\langle x,\lambda v_{1}\rangle=0$ 
Now consider $f\bigr |_{(\mathbb{F}v_{1})^{\perp}}: (\mathbb{F}v_{1})^{\perp}\longrightarrow (\mathbb{F}v_{1})^{\perp}$, which should also be self-adjoint.
Repeat this argument on $(\mathbb{F}v)^{\perp}$, where $v$ are other eigenvalues. ^4c6f15

---

"$\Longrightarrow$" is obvious
"$\Longleftarrow$" Suppose $Ae_{1}=\lambda e_{1}$ for some unit vector $e_{1}$, extend $e_{1}$ to be an orthonormal basis $\{e_{1}=v_{1}, \cdots, v_{n}\}\subseteq\mathbb{C}^{n}$
$A[v_{1}, \cdots, v_{n}]=[Av_{1}, \cdots, Av_{n}]=[v_{1}, \cdots, v_{n}]\begin{pmatrix} \lambda && a_{2} && \cdots && a_{n} \\ 0 && && && \\ \vdots && && \textbf{A}_{1} && \\ 0 && && && \end{pmatrix}$, denote the latter as $B$, then $B=[v_{1}, \cdots, v_{n}]^{-1}A[v_{1}, \cdots, v_{n}]$ is also normal.
Consider the $(1,1)th$ entry, $(\overline{\lambda}, 0, \cdots, 0)\begin{pmatrix} \lambda \\ 0 \\ \vdots \\ 0\end{pmatrix}=(\lambda, a_{2}, \cdots, a_{n})\begin{pmatrix} \overline{\lambda} \\ \overline{a_{2}} \\ \vdots \\ \overline{a_{n}}\end{pmatrix}$   
Then we can deduce that $a_{2}=\cdots=a_{n}=0$
Since $B$ is normal, $A_{1}$ must also be normal. Continue this process for finite times and we are done.

---

