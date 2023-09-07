## August 31, 2013 - More on Orbits
### Recall:  
$f(x) = ax$  
$f^2(x) = f(f(x)) = a* (ax) = a^2$  
$f^n(x) = a^nx$  
When $a$ is less than 1, the fixed point is repulsive.  
When $a$ is greater than 1, the fixed point is attractive.

---

$
\begin{aligned}
    \text{Let } g(x) = ax + b  
    ax + b &= x\\
    ax - x + b &= 0\\
    (a-1)x + b &= 0\\
    x &= \frac{-b}{a-1}\\
    x &= \frac{b}{1-a}.
\end{aligned}
$  

Note: $\frac{b}{1-a}$ is a fixed point of the original function.

$
\therefore g(x)=ax \to g(x) = a(x-\frac{b}{1-a}) + \frac{b}{1-a}
$

$
\begin{aligned}
\text{So } g^2(x) &= a\left[g^1(x)\right] - \frac{b}{1-a}\\
&= a\left[{g(x) = a(x-\frac{b}{1-a}) + \frac{b}{1-a}}\right] - \frac{b}{1-a}.
\end{aligned}
$

This process of nested subfunction will continue as $n$ grows.  
This explains how difficult it may be to find a closed form expression of a recursive function.

Notation: Another way to write this relationship is with $\phi$ (phi), where $\phi(x) = x-\frac{b}{1-a}$.  
$g^1= \phi^{-1} \circ f \circ \phi$  
$g^2= \phi^{-1} \circ f \circ \phi \circ \phi^{-1} \circ f \circ \phi$  
$g^2 = \phi^{-1} \circ f{^2} \circ \phi$

---

Proof:  
Suppose $x_0$ is a fixed point of a continuous function $f$. (ie: $f(x_0) = x_0$)  
Suppose also that $|f'(x_0)| < r < 1$ where $r$ is some point in between.  
_Recall_: When we need the distance between values, we use the absolute value of the difference.  
_Recall_: __Mean Value Theorem__: If $f:[a,b] \to \R$ and $f$ is differentiable on $[a,b]$, then $\exists \in (a,b)$ such that $f'(c) = \frac{f(b)-f(a)}{b-a}$.
$\quad$ Simple terms: ...  
$
\begin{aligned}
|f(x) - x_0| &= |f(x) - f(x_0)|\\
&=|f'(c)| |x-x_0| \quad \text{ by the  Mean Value Theorem}.
\end{aligned}
$

$
|f^n(x) - x_0| < r^n|x-x_0|.
$

---

### 2.5 Classification of Periodic Orbits
___Def 2.5.1:___ Let $f:\R \to \R$ be continuously differentiable and suppose $x_0\in\R$ is a periodic point of $f$ with period $n$.  
We classify $x_0$ and its orbit as:
1. __Attractive__ if $|F'(x_0)| < 1$.
2. __Super-attractive__ if $f'(x_0) = 0$
3. __Repulsive or repelling__ if $|F'(x_0) > 1$
4. __Neutral__ if $|F'(x_0)| = 1$ 

___Lemma 2.5.2___: Suppose that $x_0 \to x_1  \to \dots \to x_{n-1} \to x_0$ is an orbit of period $n$ for $f: \R\to\R$,  
then the multiplier of the orbit is $f'(x_0)f'(x_1)\dots f'(x_{n-1})$.

Note: When graphing a function with a cobweb plot, the points of intersection with $f$ and $y=x$ are not always the fixed points.

Corollary 2.5.3: A periodic orbit is super-attracting iff it contains a critical point.

### 2.6 Critical Orbits
___Def: Critical Point___ of $f$ is a point where the derivative of $f$ at that point is $0$.  
___Def: Critical Orbit___ is an orbit around a critical point.

Some mathematical properties are easier in Complex Analysis than in Real Analysis.  
Example: All polynomials of power $n$ in the complex domain have _exactly_ $n$ roots while polynomials of power $n$ in the real domain have __at most__ $n$ roots.

___Theorem 2.6.1___:  If $f: \Complex \to \Complex$ has an attractive or super-attractive orbit, then that orbit must attract at least one critical point.

### Homework Talk
Recall that a logistic function is a function of the form $g_\lambda(x) = \lambda x(1-x)$.  
Use the Safe cell in [the example of 2.6](https://www.marksmath.org/classes/Fall2023ChaosAndFractals/chaos_and_fractals_2023/sec-critical_orbits.html).
