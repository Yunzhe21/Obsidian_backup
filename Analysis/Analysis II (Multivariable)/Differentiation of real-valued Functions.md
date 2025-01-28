---
tags:
  - "#Derivative"
  - "#PartialDerivative"
  - MeanValueTheorem
  - Gradient
  - Clairaut
  - FunctionClasses
  - TaylorExpansion
  - WhitneyExtension
  - AnalyticFunction
---
## Derivative

#Derivative 
>[! def |*] Derivative
> $f$ is a function with domain $D\subseteq E^{n}$ and $\textbf{x}_{0}$ is an interior point in $D$. The derivative of function $f$ at $\textbf{x}_{0}$ in the direction $\textbf{v}$ is $$
\lim_{t\to 0}\frac{f(\textbf{x}_{0}+t\textbf{v})-f(\textbf{x}_{0})}{t} $$ if the limit exists.



#PartialDerivative Partial derivatives of $f$ is defined as the derivative in the directions $e_{1}, \cdots, e_{n}$, if these directional derivatives exist. And the notation is $f_{i}(\textbf{x})$ or $\frac{\partial f}{\partial \textbf{x}_{i}}(\textbf{x})$ 

---

## Linear functions

Let $L$ be a real-valued function whose domain is $E^{n}$.

>[! def |*]
>The function $L$ is linear if:
>1.  $L(\textbf{x}+\textbf{y})=L(\textbf{x})+L(\textbf{y})$ for every $\textbf{x}$, $\textbf{y}\in E^{n}$.
>2.  $L(c\textbf{x})=cL(\textbf{x})$ for every $\textbf{x}\in E^n$ and scalar $c$.


>[! prp |*] 
>A real valued function $L$ is linear if and only if there exist real numbers $a_{1}, \cdots, a_{n}$ such that $L(\textbf{x})=\textbf{a}\cdot\textbf{x}$ for every $\textbf{x}\in E^{n}$.
-  [[Differentiation of real-valued Functions (Proof)#^76fe42|Proof]]
- The object $\textbf{a}$ is called *covector* and is not an element of $E^{n}$, but belong to the dual space $(E^{n})^{*}$ 

### Dual Space

Let $V$ be a n-dimensional vector space with basis $B=\{u_{1}, \cdots, u_{n}\}$, $\mathscr{L}(V, W)$ be the space of linear functions from $V$ to $W$. Here we let $W$ be $E^1$. The dual space is exactly $V^{*}=\mathscr{L}(V,W)$. 

Let $L_{1}, \cdots, L_{n}$ be linear functions in $\mathscr{L}(V, W)$ such that $L_{i}(c_{1}u_{1}+\cdots+c_{n}u_{n})=c_{i}$, which essentially means $L_{i}(u_{j})=\delta_{ij}$. We didn't choose these kind of functions arbitrarily, and in fact $\{L_{1}, \cdots, L_{n}\}$ is a basis for $V^{*}$ (easy to verify). If we use vector notation to denote them, we call $\{\textbf{e}^{1}, \cdots, \textbf{e}^{n}\}$ the **standard basis** for $(E^{n})^{*}$.

The reason for denoting them as $\{\textbf{e}^{1}, \cdots, \textbf{e}^{n}\}$ is because in this way every formula about vectors there is a corresponding formula about covecotrs obtained by simply interchanging the subscripts and superscripts. For example, $x^{i}=L_{i}(\textbf{x})=\textbf{e}^{i}\cdot\textbf{x}$ m, the doe product is valid because we've just proved that linear functions can be written in dot product form.

---

## Differentiable functions

We should first notice that having all partial derivatives does not imply having derivatives in other directions. Thus we should have a different definition for differentiable function. 

>[! def |*] Differentiable function
>The function $f$ is differentiable at $\textbf{x}_{0}$ if there is a linear function $L$ depending on $\textbf{x}_{0}$ such that $$
\lim_{\textbf{h}\to\textbf{0}}\frac{f(\textbf{x}_{0}+\textbf{h})-f(\textbf{x}_{0})-L(\textbf{h})}{|\textbf{h}|}=0 $$


Now, we can justify this new definition by showing that if $f$ is differentiable, then $f$ has a derivative at $\textbf{x}_{0}$ in every direction $\textbf{v}$ 
	Taking $\textbf{h}=t\textbf{v}$, the definition of differentiability gives us ${} \lim_{t\to0}\frac{f(\textbf{x}_{0}+\textbf{h})-f(\textbf{x}_{0})-L(t\textbf{v})}{t}=0 {}$. By the property of linear functions, we get $\lim_{t\to0}\frac{f(\textbf{x}_{0}+\textbf{h})-f(\textbf{x}_{0})}{t}=L(\textbf{v})$    

Previously, we identified each linear function with a covector. We let $df(\textbf{x}_{0})$ denote the covector corresponding to the linear function $L$. 

#Differential 
>[! def |*] Differential 
> $df(\textbf{x}_{0})$ is the differential of $f$ at $\textbf{x}_{0}$

By our discussion of linear functions, $L(\textbf{h})=df(\textbf{x}_{0})\cdot \textbf{h}$. Particularly, if $f$ is differentiable at $\textbf{x}_{0}$, then for direction $\textbf{e}_{i}$, the i-th partial derivative equals to $L(\textbf{e}_{i})$ <font color="#ff0000">(check by using the definition of derivative)</font>. Hence by the definition of covector, $df(\textbf{x}_{0})=\sum\limits_{i=1}^{n}f_{i}(\textbf{x}_{0})\textbf{e}^{i}$. Also, $df(\textbf{x}_{0})\cdot\textbf{h}=\sum\limits_{i=1}^{n}f_{i}(\textbf{x}_{0})h^{i}$ 

If $f$ is differentiable at $\textbf{x}_{0}$, then the differential at $\textbf{x}_{0}$ furnisjes a **linear approximation** $df(\textbf{x}_{0})\cdot(\textbf{x}-\textbf{x}_{0})$ to $f(\textbf{x})-f(\textbf{x}_{0})$ when $\textbf{x}_{0}$ is near $\textbf{x}$. 

>A **hyperplane** $P\subseteq E^{n+1}$ is called tangent to $M$ at $(\textbf{x}_{0},z_{0})$ if for each $(\textbf{x}, z)$ there exists $(\textbf{x},z')\in P$ such that $\lim_{\textbf{x}\to\textbf{x}_{0}}\frac{|z'-z|}{|\textbf{x}-\textbf{x}_{0}|}=0$  

**Geometrically**, think of $f$ as defining an n-dimensional surface in $E^{n+1}$, namely $M=\{(\textbf{x}, z): z=f(\textbf{x})\}$.  Let us take $P=\{(\textbf{x}, z'): z'=z_{0}+df(\textbf{x}_{0})\cdot(\textbf{x}-\textbf{x}_{0})\}$, $z_{0}=f(\textbf{x}_{0})$, it's easy to verify that $P$ is a tangent hyperplane to $M$ at $(\textbf{x}_{0},z_{0})$  

<font color="#ff0000">Example:</font> Let $f(x,y)=(xy)^{1/3}$, find the tangent plane at $(1,1,1)$.
	By calculus $f_{1}(x,y)=\frac{1}{3}x^{-2/3}y^{1/3}$, $f_{2}(x,y)=\frac{1}{3}x^{1/3}y^{-2/3}$ except at $(0,0)$. The equation for the tangent plane at $(x_{0},y_{0}, f(x_{0}, y_{0}))$ is $z=f(x_{0}, y_{0})+f_{1}(x_{0},y_{0})(x-x_{0})+f_{2}(x_{0},y_{0})(y-y_{0})$ 

---

## Differentiability and Continuity


>[! thm |*]
>If $f$ is differentiable at $\textbf{x}_{0}$, then $f$ is continuous at $\textbf{x}_{0}$.
- Proof

Notice that for a multi-variable function ($n\geq 2$), having all partial derivatives does not imply differentiability or even continuity, here we give a typical example

<font color="#ff0000">Example:</font> Let $f(x,y)=\frac{2xy^{2}}{x^{2}+y^{4}}$ when $(x,y)\neq(0,0)$, and $f(0,0)=0$
	If $\cos\theta\neq 0$, then the derivative at $(0,0)$ in the direction $(\cos\theta, \sin\theta)$ is 
	$$
\lim_{t\to 0}\frac{f(t\cos\theta, t\sin\theta)-f(0,0)}{t}=\lim_{t\to0}\frac{2\cos\theta\sin^{2}\theta}{\cos^{2}\theta+t^{2}\sin^{4}\theta}=\frac{2\sin^{2}\theta}{\cos\theta} 
    $$
	If $\cos\theta=0$, then $f(t\cos\theta, t\sin\theta)=0$, thus the directional derivative of $f$ is 0. However, $f(y^2,y)=1$ for every $y\neq 0$, combining with the fact that $f(0,0)=0$, then $f$ is not continuous at $(0,0)$, thus $f$ is not differentiable.

However, we can strengthen the statement of having all partial derivatives, the relating theorem is stated below.

>[! thm |*]
>If $f$ has all its first order partial derivatives in $U$ and they are continuous at $\textbf{x}_{0}$, then $f$ is differentiable at $\textbf{x}_{0}$
-  [[Differentiation of real-valued Functions (Proof)#^44ffaf|Proof]]

---

## Mean Value Theorem

In order to illustrate the Mean Value Theorem, we first prove a lemma.

>[! lem |*]
>Let $\phi(t)=f(\textbf{x}_{0}+t\textbf{h})$, then for every $t$ such that $f$ is differentiable at $\textbf{x}_{0}+t\textbf{h}$, $\phi'(t)=df(\textbf{x}_{0}+t\textbf{h})\cdot h$
- Proof

#MeanValueTheorem 
>[! thm |*] Mean Value Theorem
>Let $f$ be continuous at every point $\textbf{x}$ of the line segment $l$ joining $\textbf{x}_{0}$ and $\textbf{x}_{0}+\textbf{h}$, with $f$ differentiable at each point of $l$ except perhaps the endpoints. Then there exists a number $s$ such that $f(\textbf{x}_{0}+\textbf{h})-f(\textbf{x}_{0})=df(\textbf{x}_{0}+s\textbf{h})\cdot\textbf{h}$
-  [[Differentiation of real-valued Functions (Proof)#^579828|Proof]]

---

## Other Important Conclusions

>[! Cor |*]
> Let $f$ be differentiable on a convex set $K$ and $C\geq 0$ is a number such that $|df(\textbf{x})|\leq C$ for every $\textbf{x}\in K$. Then for every $\textbf{x},\textbf{y}\in K$, $|f(\textbf{x})-f(\textbf{y})|\leq C|\textbf{x}-\textbf{y}|$.
-  [[Differentiation of real-valued Functions (Proof)#^ea43f7|Proof]]
- <font color="#ff0000">Remark:</font> Convexity is important in the sense that every line segment drawn between two points in $K$ also belongs to $K$

>[! cor |*]
> Let $f$ be a differentiable function whose domain $D$ is an open connected set such that $df(\textbf{x})=\textbf{0}$ for every $\textbf{x}\in D$. Then $f$ is a constant function.
-  [[Differentiation of real-valued Functions (Proof)#^8b63da|Proof]] 
- <font color="#ff0000">Remark:</font> Actually, we can relax the condition of connectness to **path connectness**

---

## Gradient 

#Gradient 
>[! def |*] Gradient 
> $\text{grad} f(\textbf{x})=\sum\limits_{i=1}^{n}f_{i}(\textbf{x})\textbf{e}_{i}$, we also have the common notation $\nabla f(\textbf{x})$.

There is hardly any difference between differential and gradient as we are working on Euclidean Space. However, for information about the differences, check [https://math.stackexchange.com/questions/289923](https://math.stackexchange.com/questions/289923/what-are-the-differences-between-differential-and-gradient#:~:text=The%20differential%20of%20a%20function,)

#Gradient Now , consider the gradient vector $\nabla f$ with the same components as differential. Suppose that $\textbf{x}$ is not a critical point, then $\nabla f(\textbf{x})\neq 0$. We will show **intuition** about gradient vector.

Let's find the direction (a unit vector) $\textbf{v}$ for which the directional derivative at $\textbf{x}$ is maximum. By Cauchy's inequality, $L(\textbf{v})=\nabla f(\textbf{x})\cdot\textbf{v}\leq |\nabla f(\textbf{x})||\textbf{v}|$, the equality holds if and only if $\textbf{v}=\frac{1}{|\nabla f(\textbf{x})|}\nabla f(\textbf{x})$. This direction is called the **direction of the gradient** at $\textbf{x}$, and is the one that maximizes the directional derivative. The maximal value of the directional derivative is $|\nabla f(\textbf{x})|$. 

---

## Derivative of higher order

#Clairaut 
>[! thm |*] Clairaut
>If the second order derivatives $\{f_{ij}\}_{1\leq i,j\leq n}$ exists and are continuous at $\textbf{x}$, then $f_{ij}(\textbf{x})=f_{ji}(\textbf{x})$ 
-  [[Differentiation of real-valued Functions (Proof)#^4aa798|Proof]] 

Now, we are going to show a stronger version of mean value theorem for functions of class $\mathscr{C}^{q}$ and $\textbf{x},\textbf{x}_{0}\in D$ such that the line segment joining $\textbf{x}$ and $\textbf{x}_{0}$ is contained in the domain.
#TaylorExpansion
Let $\textbf{h}=\textbf{x}-\textbf{x}_{0}$, and define $\phi(t)=f(\textbf{x}_{0}+t\textbf{h})$. The domain of $\phi$ is $\{t:\textbf{x}+t\textbf{h}\}$, which is a subset of $E^{1}$ containing $[0,1]$

$\phi'(t)=\sum\limits_{i=1}^{n}f_{i}(\textbf{x}_{0}+t\textbf{h})h^{i}$
$\phi''(t)=\sum\limits_{i=1}^{n}\bigl [ \sum\limits_{j=1}^{n}f_{ij}(\textbf{x}_{0}+t\textbf{h})h^{j}\bigr ]h^{i}$
$\cdots$ 
$\phi^{(q)}(t)=\sum\limits_{i_{1}, \dots, i_{q}=1}^{n}f_{i_{1}, \dots, i_{q}}(\textbf{x}_{0}+t\textbf{h})h^{i_{1}}, \dots, h^{i_{q}}$  
 
By Taylor's formula, there exists $s\in(0,1)$ such that 
$\phi(1)=\phi(0)+\phi'(0)+\frac{1}{2}\phi''(0)+\cdots+\frac{1}{(q-1)!}\phi^{(q-1)}(0)+\frac{1}{q!}\phi^{(q)}(s)$. Substituting our previous conclusions, we have remainder $R_{q}(\textbf{x})=\frac{1}{q!}\sum\limits_{i_{1}, \dots, i_{q}=1}^{n}f_{i_{1}, \dots, i_{q}}(\textbf{x}_{0}+t\textbf{h})h^{i_{1}}, \dots, h^{i_{q}}$ 

Now, we want to <font color="#ff0000">estimate</font> the remainder since the remainder itself is difficult to calculate directly. (But we need to have an **additional condition**)

Suppose that $K$ is a convex set such that $\textbf{x}_{0}\in K$ and ${} \textbf{x}=\textbf{x}_{0}+\textbf{h}\in K {}$. Then $\textbf{x}_{0}+s\textbf{h}\in K$ for $0\leq s\leq 1$. Moreover **suppose** that all q-th partial derivatives satisfy $|f_{i_{1}, \dots, t_{q}}(\textbf{x})|\leq C$ for all $\textbf{x}\in K$. We can have $|R_{q}(\textbf{x})|\leq\frac{C}{q!}\sum\limits_{i_{1}, \dots, i_{q}=1}|h^{i_{1}}|\cdots |h^{i_{q}}|=\frac{C}{q!}\bigl ( \sum\limits_{i=1}^{n}|h^{i}|\bigr)^{q}$, also by the fact that $\sum\limits_{i=1}^{n}|h^{i}|\leq n^{1/2}|\textbf{h}|$ (Not hard to verify). Therefore, the remainder in Taylor's formula satisfies the estimate $|R_{q}(\textbf{x})|\leq\frac{Cn^{q/2}}{q!}|\textbf{h}|^{q}$, where $\textbf{h}=\textbf{x}-\textbf{x}_{0}$.

---

## Class of functions

#FunctionClasses 
>[! def |*] Function Classes
>If $f$ is continuous on $D$, then $f$ is said to be a function of class $\mathscr{C}^{0}$. If the partial derivatives $f_{1}(\textbf{x}), \dots, f_{n}(\textbf{x})$ exist for every $\textbf{x}\in D$, and they are also continuous, then $f$ is a function of class $\mathscr{C}^{(1)}$.

>[! def |*] Function Classes
>If all of the q-th order derivatives of $f$ exist at every $\textbf{x}\in D$ and each $f_{i_{1}, \dots, i_{q}}$ is a continuous function on $D$, then $f$ is a function of class $\mathscr{C}^{(q)}$.

>[! def |*]
>Let $A$ be a nonempty subset of the domain of $f$. Then $f$ is of class $\mathscr{C}^{(q)}$ on $A$ if there exists an open set $D_{1}$ containing $A$ and a function $F$ of class $\mathscr{C}^{(q)}$ with domain $D_{1}$ such that $F(\textbf{x})=f(\textbf{x})$.

Next, we will state Whitney's extension theorem without proof. The aim of this Whitney's Extension Theorem is to extend the class of function to the whole space.

#WhitneyExtension
>[! thm |*] Whitney Extension Theorem
>Assume the following, then there exists a function $F$ of class $\mathscr{C}^{(q)}$ on $E^{n}$ such that $F(\textbf{x})=f(\textbf{x})$ for every $\textbf{x}\in A$. Hence $f$ is of class $C^{(q)}$ on $A$.
>1.  $A$ is the closure of an open set $B$
>2. $A$ is convex or the boundary $\partial A$ is an (n - 1) - manifold of class $\mathscr{C}^{(1)}$
>3. . $f$ is of class $\mathscr{C}^{(q)}$ on $B$, and continuous on $A$
>4. . For each $i_{1}, \dots, i_{q}$ there is a function $F_{i_{1}, \dots, i_{q}}$ continuous on $A$ such that $F_{i_{1}, \dots, i_{q}}(\textbf{x})$ equals the partial derivative $f_{i_{1}, \dots, i_{q}}(\textbf{x})$ for every $\textbf{x}\in B$.

For more Whitney's Extension Theorem, check this paper [Analytic extensions of differentiable functions defined in closed sets](https://www.ams.org/journals/tran/1934-036-01/S0002-9947-1934-1501735-3/)

#FunctionClasses 
>[! def |*] Function Classes
> $f$ is of class $\mathscr{C}^{(\infty)}$ if $f$ is of $\mathscr{C}^{(q)}$ for every $q$.

If $f$ is of class $\mathscr{C}^{(\infty)}$ and $\lim_{q\to\infty}R_{q}(\textbf{x})=0$, then in place of Taylor's formula with remainder we may put the corresponding infinite series, and it is called the Taylor series of for $f(\textbf{x})$ at $\textbf{x}_{0}$.

#AnalyticFunction 
>[! def |*] Analytic Function
>A function $f$ is called analytic if every $\textbf{x}_{0}\in D$ has a neighborhood $U_{\textbf{x}_{0}}$ such that the Taylor series at $\textbf{x}_{0}$ converges to $f(\textbf{x})$ for every $\textbf{x}\in U_{\textbf{x}_{0}}$.


>[! thm |*]
>Let $f$ be of class $\mathscr{C}^{\infty}$, and suppose that every $\textbf{x}_{0}\in D$ has a neighborhood $U_{\textbf{x}_{0}}$ in which every qth-order partial derivatives of $f$, $|f_{i_{1}, \dots, i_{q}}(\textbf{x})|\leq M^{q}$, where $M$ is a positive number depending on $\textbf{x}_{0}$ and the radius of $U_{\textbf{x}_{0}}$. Then $f$ is analytic.
- Proof is not hard as we use the estimation before, $|R_{q}(\textbf{x})|\leq\frac{M^{q}n^{n/2}|\textbf{h}^{q}|}{q!}\to 0$ as $q\to 0$ 




