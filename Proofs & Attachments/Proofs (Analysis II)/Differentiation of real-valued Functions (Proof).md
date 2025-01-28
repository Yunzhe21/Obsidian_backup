
If the function $L$ is linear, let $a_{i}=L(\textbf{e}_{i})$. Since for each $x$ we have $\textbf{x}=x_{1}\textbf{e}_{1}+\cdots+x_{n}\textbf{e}_{n}$, then $L(\textbf{x})=x_{1}L(\textbf{e}_{1})+\cdots+x_{n}L(\textbf{e}_{n})$. By letting $a_{i}=L(\textbf{e}_{i})$, we get the desired form. Conversly, the conclusion is just trivial. ^76fe42

---

Let $\phi(t)=f(\textbf{x}_{0}+t\textbf{h})$, as in the previous lemma. Then $\phi(t)$ is continuous on $[0,1]$ by our condition, and $\phi(0)=f(\textbf{x}_{0})$, $\phi(1)=f(\textbf{x}_{0}+\textbf{h})$, $\phi'(t)=df(\textbf{x}_{0}+t\textbf{h})\cdot\textbf{h}$ if $0<t<1$. By Mean Value Theorem of single variable, there exists $s\in(0,1)$ such that $\phi(1)-\phi(0)=\phi'(s)$. ^579828

---

By the mean value theorem, $f(\textbf{x})-f(\textbf{y})=df(\textbf{y}+s(\textbf{x}-\textbf{y}))\cdot (\textbf{x}-\text{y})$, where $s\in(0,1)$. Then $|f(\textbf{x})-f(\textbf{y})|\leq |df(\textbf{y}+s(\textbf{x}-\textbf{y}))|\cdot|\textbf{x}-\textbf{y}|\leq C|\textbf{c}-\textbf{y}|$  ^ea43f7

---

Let $\textbf{x}_{0}$ be some point of $D$, and let $D_{1}=\{\textbf{x}: f(\textbf{x})=f(\textbf{x}_{0})\}$. If $\textbf{x}\in D_{1}$, then there exists a neighborhood $U$ of $\textbf{x}$ is contained in $D$. By the above corollary, setting $C=0$, we have $f(\textbf{y})=f(\textbf{x})=f(\textbf{x}_{0})$ for every $y\in U$, which means that $D_{1}$ is an open set.
Since $f$ is differentiable, $f$ is continuous. Therefore $D-D_{1}=\{\textbf{x}: f(\textbf{x})\neq f(\textbf{x}_{0})\}$ is also open. If $D-D_{1}$ is not empty, that would contradict the definition of connectness, thus $D=D_{1}$ ^8b63da

---

Write the increment $f(x+h, y+k)-f(x,y)=f(x+h,y+k)-f(x,y+k)+f(x,y+k)-f(x,y)$, and by using the mean value theorem for single variable, it is equal to $hf_{x}(x+\theta_{1}h, y+k)+kf_{y}(x,y+\theta_{2}k)$, where $0<\theta_{1},\theta_{2}<1$. Also, since by our hypothesis that $f_{x}$ and $f_{y}$ are continuous at $(x,y)$, we can write $f_{x}(x+\theta_{1}h,y+k)=f_{x}(x,y)+\epsilon_{1}$ and $f_{y}(x,y+\theta_{2}k)=f_{y}(x,y)+\epsilon_{2}$. Thus, we obtain $f(x+h,y+k)-f(x,y)=hf_{x}(x,y)+kf_{y}(x,y)+\epsilon_{1}h+\epsilon_{2}k=hf_{x}(x,y)+kf_{y}(x,y)+o(\sqrt{h^2+k^2})$ ^44ffaf

---

We consider four points $(x,y), (x+h,y), (x, y+k), (x+h,y+k)$, where $h,k\neq 0$ and small enough such that all these points lie in the domain. Let $\phi(x,y)=f(x,y+k)-f(x,y)$, then we can write $A:=f(x+h,y+h)-f(x+h,y)-f(x,y+k)+f(x,y)=\phi(x+h)-\phi(x)$. Applying the mean value theorem, we have $A=h\phi'(x+\theta h)$, where $\theta\in (0,1)$. From definition of $\phi$ we have $\phi'(x)=f_{x}(x,y+k)-f_{x}(x,y)$, apply mean value theorem again, $A=hkf_{yx}(x+\theta h,y+\theta'k)$, where $0<\theta, \theta'<1$. In a similar manner, define $\psi(y)=f(x+h,y)-f(x,y)$, and express $A=\psi(y+k)-\psi(y)$. Following the samw procedure as before, we ca derive the equation $A=hkf_{xy}(x+\theta_{1}h,y+\theta_{1}'k)$, where $\theta_{1},\theta_{1}'\in(0,1)$.
Hence $f_{yx}(x+\theta h,y+\theta' k)=f_{xy}(x+\theta_{1}h,y+\theta_{1}'k)$, by recalling that second derivatives are continuous, we let $h,k\to 0$ and obtain the desired conclusion. ^4aa798

---

Given a direction $\textbf{v}$, let $\phi(t)=f(\textbf{x}_{0}+t\textbf{v})$ for every $t$ in some open subset of $E^{1}$ containing $0$. Then $\phi$ has a relative extremum at $0$, and consequently by single-variable calculus $\phi'(0)=0$. But $\phi'(0)=df(\textbf{x}_{0})\cdot\textbf{v}$ is the derivative at $\textbf{x}_{0}$ in the direction $\textbf{v}$. Hence $df(\textbf{x}_{0})\cdot\textbf{v}=0$ for every $\textbf{v}$, which implies $df(\textbf{x}_{0})=0$. ^81c654

---

Indeed we only need to prove 1) and 1.1)
Let $f$ have a relative minimum at $\textbf{x}_{0}$. Then there exists a neighborhood $U$ of $\textbf{x}_{0}$ such that $f(\textbf{x})\geq f(\textbf{x}_{0})$ for every $x\in U\cap A$. Since $A$ is open, we can let $U\subseteq A$. Since $df(\textbf{x}_{0})=\textbf{0}$, by Taylor expansion, $Q(\textbf{x}_{0}+s\textbf{h},\textbf{h})\geq 0$ for all $\textbf{x}\in U$, where $\textbf{h}=\textbf{x}-\textbf{x}_{0}$. Since $f$ is of class $\mathscr{C}^{(2)}$, then $f_{ij}$ are continuous, hence $Q(\cdot, \textbf{h}_{0})$ is continuous on $A$. Suppose that $Q(\textbf{x}_{0}, \textbf{h}_{0})<0$ for some $\textbf{h}_{0}\in E^{n}$. Then there exists a neighborhood $U_{1}\subseteq U$ of $\textbf{x}_{0}$ such that $Q(\textbf{y},\textbf{h}_{0})<0$ for all $y\in U_{1}$. Take $\textbf{x}=\textbf{x}_{0}+c\textbf{h}_{0}$ where $|c|$ is small enough that $\textbf{x}\in U_{1}$, and $\textbf{y}=\textbf{x}_{0}+s\textbf{h}$, then $\textbf{h}=c\textbf{h}_{0}$. Since $Q(\textbf{x}_{0}+s\textbf{h},\cdot)$ is quadratic, $Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h})=c^{2}Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h}_{0})<0$, contradicting the fact that $Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h})\geq 0$. ^666d5b

---

Suppose that $Q(\textbf{x}_{0}, \cdot)>0$. Using the fact that $f_{ij}$ are continuous at $\textbf{x}_{0}$, then there exists a neighborhood $U$ of $\textbf{x}_{0}$ such that $U\subseteq A$ and $Q(\textbf{y}, \cdot)>0$ for every $\textbf{y}\in U$. Taking $\textbf{y}=\textbf{x}_{0}+s\textbf{h}$, then we have $f(\textbf{x})>f(\textbf{x}_{0})$ for every $\textbf{x}\in U$ and $\textbf{x}\neq \textbf{x}_{0}$.  ^9c23a1

---

Let $L^{1}, \cdots, L^{n}$ denote the components of $\textbf{L}$, and let $\boldsymbol{\phi}(\textbf{k})=\frac{1}{|\textbf{k}|}[\textbf{g}(\textbf{t}_{0}+\textbf{k})-\textbf{g}(\textbf{t}_{0})-\textbf{L}(\textbf{k})]$. The components are $\phi^{i}(\textbf{k})=\frac{1}{|\textbf{k}|}[g^{i}(\textbf{t}_{0}+\textbf{k})-g^{i}(\textbf{t}_{0})-L^{i}(\textbf{k})]$, $i=1, \cdots, n$. Since ${} \boldsymbol{\phi}(\textbf{k})\to\textbf{0} {}$ as $\textbf{k}\to\textbf{0}$ if and only if $\phi^{i}(\textbf{k})\to 0$ as $\textbf{k}\to\textbf{0}$, $i=1, \cdots, n$.
Recall that $L^{i}(\textbf{k})=dg^{i}(\textbf{t}_{0})\cdot\textbf{k}$ for every $\textbf{k}\in E^{r}$. Therefore, the row covectors of the matrix of $\textbf{L}$ are $dg^{1}(\textbf{t}_{0}), \cdots, dg^{n}(\textbf{t}_{0})$  ^36fd77

---

Let $\textbf{L}=D\textbf{g}(\textbf{t}_{0})$, $\textbf{M}=D\textbf{f}(\textbf{x}_{0})$. Let's first prove the theorem for two special cases.
**Case I:** If $\textbf{M}=\textbf{0}$. Let us show that $\lim_{\textbf{k}\to\textbf{0}}\frac{1}{|\textbf{k}|}[\textbf{F}(\textbf{t}_{0}+\textbf{k})-\textbf{F}(\textbf{t}_{0})]=\textbf{0}$. By previous proposition, by letting $C=\|\textbf{L}\|+1$ and $\epsilon=1$, then there exists $\delta_{0}>0$ such that $|\textbf{g}(\textbf{x}_{0}+\textbf{k})-\textbf{g}(\textbf{t}_{0})|\leq C|\textbf{k}|$ whenever $|\textbf{k}|<\delta_{0}$. Since $\textbf{M}=\textbf{0}$, $\|M\|=\|D\textbf{f}(\textbf{x}_{0})\|=0$. By previous proposition, given $\epsilon$, there exists $\eta>0$ such that $|\textbf{f}(\textbf{x})-\textbf{f}(\textbf{x}_{0})|\leq\frac{\epsilon}{C}|\textbf{x}-\textbf{x}_{0}|$ whenever $|\textbf{x}-\textbf{x}_{0}|<\eta$. Let $\delta=\min\{C^{-1}\eta, \delta_{0}\}$. Then by taking $\textbf{x}=\textbf{g}(\textbf{t}_{0}+\textbf{k})$, $|\textbf{F}(\textbf{t}_{0}+\textbf{k})-\textbf{F}(\textbf{t}_{0})|\leq\frac{\epsilon}{C}C|\textbf{k}|=\epsilon|\textbf{k}|$ if $|\textbf{k}|<\delta$, and this proves **case I**.
**Case II:** When $\textbf{f}$ is a linear transformation, $\textbf{f}(\textbf{x})=\textbf{M}\textbf{x}$ for all $\textbf{x}$. In this case, $\lim_{\textbf{k}\to\textbf{0}}\frac{1}{|\textbf{k}|}\textbf{M}[\textbf{g}(\textbf{t}_{0}+\textbf{k})-\textbf{g}(\textbf{t}_{0})-\textbf{L}(\textbf{k})]=\textbf{0}$, which means that $\textbf{F}$ is differentiable at $\textbf{t}_{0}$ with $D\textbf{F}(\textbf{t}_{0})=\textbf{M}\circ\textbf{L}$.
In the general case, let $\tilde{\textbf{f}}=\textbf{f}-\textbf{M}$, then $D\tilde{\textbf{f}}(\textbf{x}_{0})=\textbf{0}$, Case I applies to $\tilde{\textbf{F}}=\tilde{\textbf{f}}\circ\textbf{g}$, and Case II applies to $\textbf{G}=\textbf{M}\circ\textbf{g}$. Since $\textbf{F}=\tilde{\textbf{F}}+\textbf{G}$, then the thoerem follows. ^aa9300

---

In this example, let $g^{1}(r,\theta)=r\cos(\theta)$, $g^{2}(r,\theta)=r\sin(\theta)$. Using the chain rule, we get 
$F_{1}=f_{1}g_{1}^{1}+f_{2}g_{1}^{2}=f_{1}\cos(\theta)+f_{2}\sin(\theta)$
$F_{2}=f_{1}g_{2}^{1}+f_{2}g_{2}^{2}=f_{1}\cdot(-r\sin(\theta))+f_{2}\cdot(r\cos(\theta))$ 
Further using the chain rule, we get
$F_{11}=\cos\theta (f_{11}\cos\theta+f_{12}\sin\theta)+\sin\theta(f_{21}\cos\theta+f_{22}\sin\theta)$ 
$F_{22}=-r\sin\theta[f_{11}(-r\sin\theta)+f_{12}(r\cos\theta)]+r\cos\theta[f_{21}(-r\sin\theta)+f_{22}(r\cos\theta)]-f_{1}r\cos\theta-f_{2}r\sin\theta$
Combinign terms and using the fact that $f_{21}=f_{12}$, we may get the desired equation. ^396865

---

Let $B\subset\Delta$ be open, and consider any $\textbf{t}_{1}\in B$. By applying the inverse function theorem, there exists an open set $\Delta_{1}$ containing $\textbf{t}_{1}$, with $\Delta_{1}\subset B$ such that $\textbf{g}(\Delta_{1})$ is open. Therefore the point $\textbf{g}(\textbf{t}_{1})$ has a neighborhood $U_{1}$ such that $U_{1}\subset\textbf{g}(\Delta_{1})$ is open. But also, $\textbf{g}(\Delta_{1})\subset\textbf{g}(B)$, hence $\textbf{x}_{1}$ is an interior point of $\textbf{g}(B)$, then $\textbf{g}(B)$ is open. ^3f4846

---

Consider the partial sum ${} \boldsymbol{\psi}_{r}=\sum\limits_{m=0}^{r}\boldsymbol{\phi}^{[m]}(\textbf{t}) {}$. Since $|\boldsymbol{\phi}(\textbf{t})|\leq c|\textbf{t}|$ for all $\textbf{t}\in\Omega_{1}$, then ${} |\boldsymbol{\phi}^{[m]}(\textbf{t})|\leq c^{m}|\textbf{t}| {}$ for $m=0,1,2\dots$ Therefore by the comparison with the geometric series $|\textbf{t}|(1+c+c^{2}+\dots)$, the series defining $\boldsymbol{\psi}(\textbf{t})$ converges. Moreover, $|\boldsymbol{\psi}_{r}(\textbf{r})|\leq\frac{|\textbf{t}|}{1-c}$ and $|\boldsymbol{\psi}(\textbf{t})|\leq\frac{|\textbf{t}|}{1-c}$, then both $\boldsymbol{\psi}_{r}(\textbf{t})$ and $\boldsymbol{\psi}(\textbf{t})\in\Omega_{1}$. Moreover, $\boldsymbol{\psi}_{r}-\boldsymbol{\phi}\circ\boldsymbol{\psi}_{r}=\sum\limits_{m=0}^{r}\boldsymbol{\phi}^{[m]}-\sum\limits_{m=1}^{r+1}\boldsymbol{\phi}^{[m]}=\textbf{I}-\boldsymbol{\phi}^{[r+1]}$. Since $\boldsymbol{\psi}_{r}(\textbf{t})\to\boldsymbol{\psi}(\textbf{t})$ as $r\to\infty$, and $\boldsymbol{\phi}^{[r+1]}(\textbf{t})\to\textbf{0}$ as $r\to\infty$. Since $\boldsymbol{\phi}$ is continuous, $\boldsymbol{\phi}[\boldsymbol{\psi}_{r}(\textbf{r})]\to \boldsymbol{\psi}[\boldsymbol{\phi}(\textbf{t})]$ as $r\to\infty$. ^d75147

---

Without loss of generality, we may assume that $\textbf{t}_{1}=\textbf{0}$ and $\textbf{x}_{1}=\textbf{0}$, otherwise, we can do a translation. Let $\textbf{L}=D\textbf{g}(\textbf{0})$, and $\boldsymbol{\phi}=\textbf{I}-\textbf{L}^{-1}\circ\textbf{g}$. Notice that the inverse exists because $\textbf{L}$ is a linear mapping that is not $\textbf{0}$. Moreover, $\boldsymbol{\phi}(\textbf{0})=\textbf{0}$ (easy to verify) and $D\boldsymbol{\phi}(\textbf{0})=\textbf{I}-\textbf{L}^{-1}\circ D\textbf{g}(\textbf{0})=I-\textbf{L}^{-1}\circ\textbf{L}=\textbf{0}$. Apply [[Differential Mappings#^aedaf7|Proposition]] and let $\epsilon=1/2$, we have $|\boldsymbol{\phi}(\textbf{t})|\leq\frac{1}{2}|\textbf{t}|$ in some neighborhood $\Omega_{0}$ of $\textbf{0}$ of radius $\delta_{0}$. Choose $\Omega$ be the $\delta$ -neighborhood of $\textbf{0}$, with $\delta\leq\frac{1}{2}\delta_{0}$ sufficiently small that [[Differential Mappings#^d18699|Proposition]] can be applied when $\epsilon=\frac{1}{2}$.
To prove (i), suppose that $\textbf{g}(\textbf{s})=\textbf{g}(\textbf{t})$ with $\textbf{s},\textbf{t}\in\Omega$. Then by subtracting, we have $\boldsymbol{\phi}(\textbf{s})-\boldsymbol{\phi}(\textbf{t})=\textbf{s}-\textbf{t}$. But $|\boldsymbol{\phi}(\textbf{s})-\boldsymbol{\phi}(\textbf{t})|\leq\frac{1}{2}|\textbf{s}-\textbf{t}|$, therefore, $\textbf{s}=\textbf{t}$, thus proving the injectivity. ^3226fc

---

Let $\eta=\delta(2\|\textbf{L}^{-1}\|)^{-1}$, and let $U$ be the $\eta$ -neighborhood of $\textbf{0}$. Define $\textbf{F}$ by $\textbf{F}(\textbf{x})=\boldsymbol{\psi}[\textbf{L}^{-1}(\textbf{x})]$ for all $\textbf{x}\in U$. Since $c=\frac{1}{2}$, $|\textbf{F}(\textbf{x})|\leq 2|\textbf{L}^{-1}(\textbf{x})|\leq 2\|\textbf{L}^{-1}(\textbf{x})\|\leq 2\|\textbf{L}^{-1}\|\cdot|x|<\delta$  if $\textbf{x}\in U$. Thus $\textbf{F}(U)\subset U$.
By the definition of $\boldsymbol{\phi}$ and [[Differential Mappings#^887023|Lemma 1]], $\textbf{I}-\boldsymbol{\phi}=\textbf{L}^{-1}\circ\textbf{g}$, $(\textbf{I}-\boldsymbol{\phi})\circ\boldsymbol{\psi}=\textbf{I}$, the transformations in these equations being restricted to $\Omega$. Then $L^{-1}\circ\textbf{g}\circ\boldsymbol{\psi}=\textbf{I}$, in other words, $\textbf{g}[\boldsymbol{\psi}(\tau)]=\textbf{L}(\tau)$ for all $\tau\in\Omega$. Set $\tau=\textbf{L}^{-1}(\textbf{x})$, $\textbf{x}\in U$, then $\tau\in\Omega$ and $\textbf{g}[\textbf{F}(\textbf{x})]=\textbf{g}[\boldsymbol{\psi}(\tau)]=\textbf{L}[\textbf{L}^{-1}(\textbf{x})]=\textbf{x}$. This shows that $U\subset\textbf{g}(\Omega)$ and that $\textbf{g}[\textbf{F}(\textbf{x})]=\textbf{x}$, completing the proof of ii) and iii). ^ae5800

---

To prove 4). We have by [[Differential Mappings#^887023|Lemma 1]] $\boldsymbol{\psi}(\tau)-\tau=\boldsymbol{\phi}[\boldsymbol{\psi}(\tau)]$ for all $\tau\in\Omega$. Let $0<c\leq\frac{1}{2}$. Since $\boldsymbol{\phi}(\textbf{0})=\textbf{0}$ and $D\boldsymbol{\phi}(\textbf{0})=\textbf{0}$, then $|\boldsymbol{\phi}(\textbf{t})|\leq c|\textbf{t}|$ in some neighborhood $\tilde{\Omega}_{0}$ of $\textbf{0}$ of radius $\delta_{0}$. Let $\tilde{\delta}\leq(1-c)\tilde{\delta}_{0}$, then $|\boldsymbol{\psi}(\tau)-\tau|\leq|\boldsymbol{\psi}(\tau)|\leq\frac{c}{1-c}|\tau|$, if $|\tau|<\tilde{\delta}$. Since $|\tau|\leq\|\textbf{L}^{-1}\|\cdot|\textbf{x}|$ and $\textbf{F}(\textbf{x})=\boldsymbol{\psi}(\tau)$, we have $|\textbf{F}(\textbf{x})-\textbf{L}^{-1}(\textbf{x})|\leq \frac{c\|\textbf{L}^{-1}\|\cdot|\textbf{x}|}{1-c}$ whenever $|\textbf{x}|<\tilde{\eta}$, where $\tilde{\eta}=\tilde{\delta}(\|\textbf{L}^{-1}\|)^{-1}$. Given any $\epsilon>0$ choose $c$ such that $0<c\leq\frac{1}{2}$ and $\frac{c\|\textbf{L}^{-1}\|}{1-c}\leq\epsilon$. For the corresponding $\tilde{\eta}$ we have $\frac{1}{|\textbf{x}|}|\textbf{F}(\textbf{x})-\textbf{L}^{-1}(\textbf{x})|\leq\epsilon$, if $0<|\textbf{x}|<\tilde{\eta}$. Since $\textbf{F}(\textbf{0})=\textbf{0}$, this shows that $\lim_{\textbf{x}\to\textbf{0}}\frac{1}{|\textbf{x}|}|\textbf{F}(\textbf{x})-\textbf{L}^{-1}(\textbf{x})-\textbf{L}^{-1}(\textbf{x})|=0$. Thus $\textbf{F}$ is differentiable at $\textbf{0}$, and $\textbf{L}^{-1}=D\textbf{F}(\textbf{0})$. ^5381ca

---

Given $\textbf{t}_{0}$, take $\Delta_{0}$ a neighborhood of $\textbf{t}_{0}$ such that $\textbf{g}|_{\Delta_{0}}$ is injective. Since $\textbf{g}$ is of class $\mathscr{C}^{(q)}$, $q\geq 1$, $J\textbf{g}$ is continuous. Hence we can choose $\Delta_{0}$ such that $J\textbf{g}(\textbf{t})\neq 0$ for all $\textbf{t}\in\Delta_{0}$. Let $\textbf{f}=(\textbf{g}|_{\Delta_{0}})^{-1}$. Consider any $\textbf{t}_{1}\in\Delta_{0}$, let $\textbf{x}_{1}=\textbf{g}(\textbf{t}_{1})$, $\Omega,U,\textbf{F}$ be as in Lemma 2, with $\Omega\subset\Delta_{0}$. Since $U\subset\textbf{g}(\Omega)\subset\textbf{g}(\Delta_{0})$ and $\textbf{g}|_{\Delta_{0}}$ is injective, $\textbf{F}(\textbf{x})=\textbf{f}(\textbf{x})$ for all $\textbf{x}\in U$. Since each $\textbf{x}_{1}\in\textbf{g}(\Delta_{0})$ has such a neighborhood, $\textbf{g}(\Delta_{0})$ is an open set. Moreover, by 4) of lemma 2, $\textbf{f}$ is differentiable at $\textbf{x}_{1}$ and $D\textbf{f}(\textbf{x}_{1})=[D\textbf{g}(\textbf{t}_{1})]^{-1}$.
In order to finich the proof, one only need to show that $\textbf{f}$ is of class $\mathscr{C}^{(q)}$. $\textbf{f}$ is continuous at any point of $\textbf{g}(\Delta_{0})$ since it's also differentiable. Since $D\textbf{f}(\textbf{x})=[D\textbf{g}(\textbf{t})]^{-1}$, this gives us the identity: $\delta_{j}^{i}=\sum\limits_{l=1}^{n}f_{l}^{i}(\textbf{x})g_{j}^{l}(\textbf{t})$, where $\textbf{t}=\textbf{f}(\textbf{x})$. Since each $g_{j}^{l}$ is continuous and $\textbf{f}$ is continuous, the composite $g_{j}^{l}\circ\textbf{f}$ is continuous. 
Let $(y_{j}^{i})$ be a nonsingular matrix, then Cramer's rule expresses the solution $(z_{1}, \cdots, z_{n})$ of the system $b_{j}=\sum\limits_{l=1}^{n}z_{l}y_{j}^{l}$ as a rational function. Take $b_{j}=\delta_{j}^{i}, z_{l}=f_{l}^{i}(\textbf{x}), y_{j}^{l}=g_{j}^{l}(\textbf{t})$. Since $J\textbf{g}(\textbf{t})\neq 0$, then $f_{l}^{i}$ is the composite of continuous functions, thus each partial derivative $f_{l}^{i}$ is continuous, then $\textbf{f}$ is of class $\mathscr{C}^{(1)}$, repeating this process we obtain the desired conclusion. ^efaec8

---

Since $\boldsymbol{\Phi}$ is at least of class $\mathscr{C}^{(1)}$, the Jacobian $J\boldsymbol{\Phi}$ is a continuous function. By assumption it is not zero at $\textbf{x}_{0}$, therefore, it is not zero for $\textbf{x}$ in some neighborhood $U_{0}$ of $\textbf{x}_{0}$.
Consider the transformation $\textbf{f}$, with domain $U_{0}$ and values in $E^{n}$, $f^{i}(\textbf{x})=x^{i}$ for $i=1, \cdots, r$ ; $f^{r+l}(\textbf{x})=\Phi^{l}(\textbf{x})$ for $l=1, \cdots, m$. The transformation $\textbf{f}$ is of class $\mathscr{C}^{(q)}$. Its matrix of partial derivatives is $$
\begin{pmatrix}
 1 & 0 & \cdots & 0 & | & 0 & \cdots & 0\\
 0 & 1 & \cdots & 0 & | & 0 & \cdots & \vdots\\
 \vdots &  &  &  & | &  &  & \vdots\\
 0 &  & \cdots & 1 & | & 0 & \cdots & 0\\
 \_ & \_ & \_ & \_ & \_ & \_ & \_ & \_\\
 \Phi_{1}^{1} &  & \cdots & \Phi_{r}^{1} & | & \Phi_{r+1}^{1} & \cdots & \Phi_{n}^{1}\\
 \vdots &  & \cdots &  &  &  & \cdots & \vdots\\
 \Phi_{1}^{m} &  & \cdots & \Phi_{r}^{m} & | & \Phi_{r+1}^{m} & \cdots & \Phi_{n}^{m}
\end{pmatrix}
$$ By properties of determinants, $J\textbf{f}(\textbf{x})=\tilde{J}\boldsymbol{\Phi}(\textbf{x})$, therefore, $J\textbf{f}(\textbf{x})\neq 0$. By [[Differential Mappings#^9b2b16|Inverse Mapping Theorem]], there is a neighborhood $U$ of $\textbf{x}_{0}$ such that $\textbf{f}(U)$ is an open set, and the restriction $\textbf{f}|_{U}$ has an inverse $\textbf{g}$ of $\mathscr{C}^{(q)}$.  
Let $R=\{\hat{\textbf{x}}: (\hat{\textbf{x}}, \textbf{0})\in\textbf{f}(U)\}$. Since $\textbf{f}(U)$ is an open set, $R$ is open. For every $\hat{\textbf{x}}\in R$, let $\phi^{l}(\hat{\textbf{x}})=g^{r+l}(\hat{\textbf{x}}, \textbf{0})$. Then $\textbf{x}\in U$ and $\boldsymbol{\Phi}(\textbf{x})=\textbf{0}$ iff $\hat{\textbf{x}}\in R$ and $\textbf{f}(\textbf{x})=(\hat{\textbf{x}}, \textbf{0})$. 
For $(\hat{\textbf{x}},\boldsymbol{\phi}(\hat{\textbf{x}}))\in\{(\hat{\textbf{x}}, \boldsymbol{\phi}(\hat{\textbf{x}})):\hat{\textbf{x}}\in R\}=: H$, we find $(\hat{\textbf{x}},\textbf{0})=\textbf{f}\circ\textbf{g}(\hat{\textbf{x}},\textbf{0})=(\hat{\textbf{g}}(\hat{\textbf{x}},\textbf{0}), \boldsymbol{\Phi}(\textbf{g}(\hat{\textbf{x}},\textbf{0})))$, where the latter component can be rewritten as $\boldsymbol{\Phi}(\hat{\textbf{x}},\boldsymbol{\phi}(\hat{\textbf{x}}))$ and is equal to $\textbf{0}$.
On the other hand, if $\boldsymbol{\Phi}(\textbf{x})=\textbf{0}$, then immediately $\textbf{f}(\textbf{x})=(\hat{\textbf{x}},\textbf{0})$. Also, since $\textbf{f}$ has an inverse $\textbf{g}$ on $U$, then $\textbf{x}=\textbf{g}(\hat{\textbf{x}},\textbf{0})=(\hat{\textbf{x}}, \boldsymbol{\phi}(\hat{\textbf{x}}))$. Thus the two sets are equal. ^5bb822

---

