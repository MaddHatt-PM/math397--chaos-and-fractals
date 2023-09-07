# September 6, 2023 - Parameterized Family of Functions (Cont)
On Tuesday, we will be working on practice problems.

Short pseudo quiz for defining *fixed points* and *attractive fixed points*.  
Def: Fixed Point: Let $x_0 \in \R$. If $f(x_0) = x_0$, then $x_0$ is a fixed point.  
Def: Attractive Fixed Point: 

---

Last time: Parameterized families of functions  
Quadratic family: $f_c(x) = x^2 + c$  
Logistic family: $g_\lambda(x) = \lambda x(1-x)$  

### Finding Fixed Points with the Quadratic Family
Given $x^2 + c = x$, we can:
$$
\begin{aligned}
x^2 + c &= x\\
0 &= x^2 - x + c\\
x &= \frac{1 \pm \sqrt{1-4c}}{2}.
\end{aligned}
$$
So we have 2 fixed points if $1-4c > 0$ and 1 fixed point if $1-4c = 0$ or $c = \frac{1}{4}$  
Note: We denote $x_f=\frac{1 \pm \sqrt{1-4c}}{2}$.  
We express the derivative of $f$ at $x_f$ as $f'(x_f) = 1\pm \sqrt{1-4c}$.  
Recall: Bifurcation means a change in state.  
The next bifurcation as $c$ moves down occurs when $1-\sqrt{1-4c} \le -1$.  
So we solve for $c$ with:
$$
\begin{aligned}
1-\sqrt{1-4c} &\le -1\\
-\sqrt{1-4c} &\le -2\\
\sqrt{1-4c} &\ge 2\\
1-4c &\ge 4\\
-4c &\ge 3\\
c &\ge -\frac{3}{4}\\
&\space\blacksquare
\end{aligned}
$$

### Conjugacy
___Def: Conjugacy:___  
Let $S$ and $T$ be sets.  
Suppose $f:S \to S$ and $g:T \to T$.  
We say that $f$ is semi-conjugate to $g$ if there is a subjective function $\varphi $ such that $ f \circ\varphi = \varphi \circ g$.  
In the case that $\phi$ is a bijection, we say that $f$ and $g$ are conjugate.

Note: that $f^2 \circ \varphi = f \circ f \circ \varphi = f \circ \varphi \circ g = \varphi \circ g \circ g = \varphi \circ g^2$,  
$\therefore$  By induction (skipped proof), $f^n \circ \varphi = \varphi \circ g^n$. 

Recall: Surjective means that a function is one-to-one.  
Recall: Bijective means that a function is one-to-one and onto.

Claim: $f(x) = x^2 - 2$ is conjugate to $g(x) = 2x^2 +2x + 1$ under $\varphi(x) = 2x+1$.  
Note: $f \circ \varphi = \varphi \circ \varphi$ so $\varphi^{-1} \circ f = g \circ \varphi^{-1}$.  
Show $f \circ \varphi = \varphi \circ g$.  
So
$$
\begin{aligned}
f(\varphi(x)) &= (2x+1)^2 -2\\
    &= 4x^2 + 4x + 1 - 2 \\
    &= 4x^2 + 4x -1.\\
\\
g(\varphi(x)) &= 2(2x^2 + 4x - 1) + 1\\
&= 4x^2 + 4x -2 +1\\
&= 4x^2 + 4x -1.\\
\\

&\therefore f \text{ and } g \text{ are conjugate}.\\
&\space\blacksquare
\end{aligned}
$$

Note: This may be on a test or a quiz but instead of proving, we'll be checking the proof.  
Conjugacy transfer the dynamics of one function to another function.  

The conjugacy function $\varphi$ can be used to describe $f$ as $f = \varphi \circ g \circ \varphi$.  
With this property, we can express that:
$$
\begin{aligned}
f^2 &= (\varphi \circ g \circ \varphi{^-1}) (\varphi \circ g \circ \varphi{^-1})\\
&= \varphi \circ g \circ \varphi{^-1} \circ \varphi \circ g \circ \varphi{^-1}\\
&= \varphi \circ g \circ g \circ \varphi{^-1}\\
&= \varphi \circ g^2 \circ \varphi{^-1}.\\
\end{aligned}
$$
By induction (skipped proof), we can say that $f^n = \varphi \circ g^n \circ \varphi^{-1}$.

---

Finding the conjugate between two functions can be difficult to obtain.  
Let $f(x) = x^2 - 2$ and $g(x) = 4x(1-x)$.  
Find $\varphi(x)$.  

$$
\begin{aligned}
f(\varphi(x)) &= (ax+b)^2-2\\
&= a^2x^2 + 2abx +b^2 -2\\
\\
\varphi(g(x)) &= a4x(1-x)+b\\
&= 4ax-4ax^2+b\\
\end{aligned}
$$


So with the coefficients,
$$
\begin{aligned}
a^2 &=-4a \to a^2+4a = 0 \to a(a-4) = 0 \to a=0 \text{ or } \boxed{a=-4}.\\
2ab &= 4a \to 2(-4)b = 4(-4) \to-8b = -16 \to \boxed{b = 2}.\\
b^2 - 2 &= b \to (2)^2 - 2 = (2) \to 4-2 = 2 \to 2 = 2. \text{ which proves that } b=2.
\end{aligned}
$$


---

### Homework  
First we must find the fixed points of $x$ by setting it equal to $x$ and then solving for $x$, so:
$$
\begin{aligned}
x &= -2 + 4x - x^2\\
0 &= -2 + 3x - x^2\\\\
x &= \frac{3 \pm \sqrt{3^2-4(-1)(-2)}}{-2}\\
&= \frac{3 \pm \sqrt{9-8}}{-2}\\
&= \frac{3 \pm \sqrt{1}}{-2}\\
\text{so } &x=\frac{3+1}{2}=2 \text{ or } x = \frac{3-1}{2} = 1.
\end{aligned}
$$

With $f$, we find that $f'(x) = 4-2x$.  
With $x=2$, then $4-2(2) = 0$, so this fixed point is super-attractive.  
With $x=1$, then $4-2(1) = 2$. Since $2 > 0$, this fixed point is repulsive.  