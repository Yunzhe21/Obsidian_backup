
For all $z_{1}, z_{2}\in H^{\perp}$, and $a,b\in\mathbb{R}$, we want to check that $az_{1}+bz_{2}\in H^{\perp}$
In order to achieve that, choose an arbitrary $x\in H_{1}$, $x\cdot (az_{1}+bz_{2})=axz_{1}+bxz_{2}=0$ ^75c25a

---

For all $x\in \text{Col}(A)^{\perp}\iff x\cdot z=0$ for all $z\in\text{Col}(A)\iff x\cdot Ay=0$ for all $y\in\mathbb{R}^{m}$ 
$\iff x^{T}Ay=0$ for all $y\in\mathbb{R}^{m}\iff (A^{T}x)^{T}y=0$ for all $y\in\mathbb{R}^{m}\iff A^{T}x$ is zero matrix
$\iff x\in\text{Null}(A^{T})$ ^d6900e

---

For all $x\in H$, we want to show that $x\in (H^{\perp})^{\perp}$ 
For all $z\in H^{\perp}$, $x\cdot z=0$ by definition, which finishes the proof ^3b4a85

---

For all $x\in\mathbb{R}^{n}$, $x=a_{1}v_{1}+\cdots+a_{n}v_{n}$ for some $a_{i}\in\mathbb{R}$.
$v_{i}\cdot x=v_{i}(a_{1}v_{1}+\cdots+a_{n}v_{n})=a_{i}v_{i}\cdot v_{i}$. ^b7c63c

---

$\text{Proj}_{H}(x)=\sum\limits_{i=1}^{k}(x\cdot v_{i})v_{i}=\sum\limits_{i=1}^{k}(v_{i}^{T}x)v_{i}=[v_{1}, \cdots, v_{k}]\begin{pmatrix} v_{1}^{T}x\\ \vdots \\v_{k}^{T}x\end{pmatrix}=[v_{1}, \cdots, v_{k}][v_{1}, \cdots, v_{k}]^{T}x$ ^317927

---

$A=[A_{1}, \cdots, A_{n}]$, $A^{T}=\begin{pmatrix} A_{1}^{T} \\ \vdots \\ A_{n}^{T}\end{pmatrix}$ 
$A^{T}A=\begin{pmatrix} A_{1}^{T}A_{1} && \cdots && A_{1}^{T}A_{n} \\ \vdots && \ddots && \vdots \\ A_{n}^{T}A_{1} && \cdots && A_{n}^{T}A_{n}\end{pmatrix}=I_{n}$, thus orthonormal. ^0b5e1d

---

"$\Longleftarrow$" $\|Ax\|^{2}=Ax\cdot Ax=(Ax)^{T}Ax=x^{T}A^{T}Ax=x^{T}x=\|x\|^{2}$
"$\Longrightarrow$" for all $x,y\in\mathbb{R}^{n}$
Since $\|f(x+y)\|^{2}=\|Ax+Ay\|^{2}=(Ax+Ay)\cdot(Ax+Ay)$
${} \|f(x+y)\|^{2}=\|x+y\|^{2}=x\cdot x+2x\cdot y+y\cdot y {}$ by assumption
$(Ax+Ay)\cdot(Ax+Ay)=Ax\cdot Ax+2Ax\cdot Ay+Ay\cdot Ay$
Thus $x\cdot y=Ax\cdot Ay$ i.e. $x^{T}y=x^{T}A^{T}Ay$ 
Choose $x,y\in \{e_{1}, \cdots, e_{n}\}$, then $x^{T}y=e_{i}^{T}e_{j}=(e_{i}^{T}A^{T})(Ae_{j})=\left \{\begin{matrix} 1 & i=j \\ 0 & i\neq j \end{matrix}\right.$   
The first bracket gives us the transpose of the i-th column vector, while the second bracket gives us the j-th column vector, which gives the proof. ^04db56

---

Choose an orthogonal basis $\{v_{1}, \cdots, v_{k}\}$ of $H$ and extend it to be an orthogonal basis ${} \{u_{1}, \cdots, u_{k}, u_{k+1}, \cdots, u_{n}\} {}$ of $\mathbb{R}^{n}$.
For all $x\in \mathbb{R}^{n}$, $x=a_{1}u_{1}+\cdots+a_{n}u_{n}=\sum\limits_{i\leq k}a_{i}u_{i}+\sum\limits_{i>k}a_{i}u_{i}$
$\forall x\in H\cap H^{\perp}$, $x\perp x$, thus $x\cdot x=\|x\|^{2}=0$, $x=0$. ^243991

---

If there exists $x\in (H^{\perp})^{\perp}-H$ 
$x=x_{1}+x_{2}$, where $x_{1}\in H$ and $x_{2}\in H^{\perp}$, ensured by the Corollary above.
$x_{2}\neq 0$ by our assumption, and $x_{2}\cdots x=x_{1}\cdot x_{2}+x_{2}\cdot x_{2}=\|x_{2}\|^{2}\neq0$
So $x_{2}$ is not perpendicular to $x$, which leads to a contridiction. ^65bd68

---

$Ax_{0}$ is the projection of $b$ onto $\text{Col(A)}$. Then $b-Ax_{0}\in\text{Col}(A)^{\perp}=\text{Null}(A^{T})$. 
Therefore, $A^{T}(b-Ax_{0})=0$ and $A^{T}Ax_{0}=A^{T}b$.
Conversely, when $A^{T}Ax_{0}=A^{T}b$, then $A^{T}(b-Ax_{0})=0$ and $b-Ax_{0}\in\text{Null}(A^{T})=\text{Col}(A)^{\perp}$, which implies that $\|b-Ax_{0}\|\leq \|b-Ax\|$ for all $x$. ^ffb957

---

When $A^{T}A$ is invertible, $n=\text{rank}(A^{T}A)\leq\text{rank}(A)$, then the columns of $A$ are linearly independent.
Conversly, when the columns are linearly independent, $Ax=0$ has only trivial solution 0, and $A^{T}Ax=0$.
This implies that $x^{T}A^{T}Ax=0=(Ax)^{T}Ax=\|Ax\|^{2}$, which implies that $Ax=0$ and thus $x=0$, therefore $A^{T}A$ is invertible. ^937c83

---

