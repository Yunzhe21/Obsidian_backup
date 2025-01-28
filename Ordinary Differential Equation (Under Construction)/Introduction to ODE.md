---
tags:
  - DirectionField
  - KeplerLaw
---

In this section we study **Ordinary Differential Equations**, where equations contain derivatives.

---

## Differential Equation

Here we give an elementary example of a ODE.

<font color="#ff0000">Example 1:</font> (free fall with dragging) Suppose that an object is falling in the atomsphere. Describe velocity $v(t)$ with respect to time $t$. Newton's second law says that $F=ma$, where $m$ is the mass of the object, $a$ is the acceleration such that $v'(t)=a$. Now we suppose that the gravity acceleration $g$ remain unchanged, and that the air drag is proportional to the velocity by the drag constant $\gamma$. Since the drag acts in the opposite direction to the gravity when the object is falling, the net force of the object is 
$$
F=mg-\gamma\cdot v
$$
where the downward direction is the positive direction. Now we establish the model equation
$$
mv'=mg-\gamma\cdot v
$$

## Direction Field
#DirectionField

We can draw a direction field for the equation derived above. 

Fix a $t, v$ pair, then draw a small <font color="#ff0000">slope</font>, which is just $v'$

![[9f0ca99a25b93649bd7c8c63002d3bd.jpg]]

---

Let's solve the ODE we established before:

First rewrite the previous general form as 
$$
v'(t)=av-b
$$
by letting $a=-\gamma/m$, $b=-g$

**Step 1:** First consider the stable case $v=b/a$, then $v'(t)=0$, which satisfies the ODE.

**Step 2:** Now let $y(t)=v(t)-b/a$, then we simplify the ODE as 
$$
y'=ay
$$

When $y\neq 0$, we see $(\log |y|)'=y'/y=a$, then $\log |y|=at+C$, thus
$$
y=\pm e^{at+C}=\pm e^{C}\cdot e^{at}=Ke^{at}
$$
for all $K\in\mathbb{R}$ 

**Step 3:** Rigorously, we need to check that we don't miss any other solutions. Assume that $\omega(t)=y(t)e^{-at}$, and compute that $\omega'(t)=y'(t)e^{-at}-ay(t)e^{-at}=e^{-at}(y'-ay)=0$, then $\omega(t)$ must be a constant, thus we didn't miss any other solutions. We call such solutions **<font color="#ff0000">General solution</font>.****

## Initial value problem

As we can see from the example before, general solution is not unique but depends on $K$. This constant can be determined from the initial data $v(0)$.

In some good cases, initial value yields unique solution. Consider the initial value $v(0)=0=\frac{b}{a}+K\implies K=\frac{-b}{a}$, then $v(t)=\frac{b}{a}(1-e^{at})$ 

---

## Examples

### Kepler laws
#KeplerLaw
Preliminary definitions:

<font color="#ff0000">Definition:</font> (Central force) The force that is **radially** pointing and the magnitude is dependent on the **distance** from the source.

And the **Central field** is a space where each position is assigned with a central force. (Personal understanding)

<font color="#ff0000">Definiton:</font> The **motion** of a matrial point with unit mass in a central field is defined by the equation
$$
\ddot{\textbf{r}}=\Phi(|\textbf{r}|)\frac{\textbf{r}}{|\textbf{r}|} 
$$
where $\textbf{r}$ is the radius vector beginning at the center of the field 0.

<font color="#ff0000">Definition:</font> The **angular momentum** of a material point of a unit mass relative the the point 0 is the vector product $\textbf{M}=[\textbf{r}, \dot{\textbf{r}}]$, this symbol is just cross product.

<font color="#ff0000">Theorem:</font> (Conservation of angular momentum) Under motions in a central field, the angular momentum $\textbf{M}$ relative to the center of the field 0 does not change with time. Moreover every orbit is planar.
	Remark: This theorem explains why planets in the solar system orbit in a plane.
	[[Introduction (Proof)#^b75692|Proof]]

---

The above theorem is discovered by Kepler by observing the motion of Mars. However, Kepler develops it in a different way.

We first construct a polar coordinate $r, \varphi$ at the center of the field. Picture below is the summary of the notations we will use later. Note that ${} \textbf{e}_{\varphi} {}$ and $\textbf{e}_{r}$ are unit vectors.
![[Pasted image 20240515154129.png]]

<font color="#ff0000">Lemma:</font> We have relation
$$
\begin{align}
\dot{\textbf{r}}&=\dot{r}\textbf{e}_{r}+r\dot{\varphi}\textbf{e}_{\varphi} \\
\textbf{M}&= r^{2}\dot{\varphi}[\textbf{e}_{r}, \textbf{e}_{\varphi}]
\end{align}
$$
Moreover, quantity $M=r^{2}\dot{\varphi}$ is preserved.
	Proof: 



