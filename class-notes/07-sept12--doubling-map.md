#
___Def: The doubling map___: $d: H \to H$ such that $H=[0,1) = \{x\in \R\ : 0 \le x < 1>\}$.  
Define
$
d(x) = 2x \text{ mod } 1 = 
\begin{cases}
2x &\text{if}\quad 0 \le x < \frac{1}{2}\\
2(x-1) &\text{if}\quad \frac{1}{2} \le x < 1
\end{cases}
$

Affect of the doubling map on binary expressions:  
If $x \in H$, then we can write,  
$$
x = \sum_{n=1}^{\infin} \frac{d_n}{2^n}.
$$

Recall, the geometric formula is
$$
\sum_{n=1}^{\infin} r^n= \frac{r^n}{1-r}.
$$
By the geometric series we can express $\frac{1}{2}$ as $d(\frac{1}{2}) = 0.1=0.11=0.111\dots$.  


Note: $n$ corresponds to the digit index of the input when $H$ is the domain

With our domain $H$ we can generally say,
$$
d(x)
=d\Biggl(\space \sum_{n=1}^{\infin} \frac{x_n}{2^n} \space\Biggl)
= \begin{cases}
\sum_{n=1}^{\infin} \frac{x_n}{2^n} \quad \text{if} \quad x < \frac{1}{2}\\[0.5em]
\sum_{n=1}^{\infin} \frac{x_n}{2^n} \quad \text{if} \quad x \le \frac{1}{2}
\end{cases}
$$

With the doubling map, we can express any integer as a periodic number

---

A set $S\subseteq H$ is called ___dense___ if for every open subinterval $I \subseteq H$,  
there is some element of $x \in S$ that's also in $I$.  

Cantor Set

---

It is important to examine how far apart two numbers are away from each other.  
Notation: $0_{\dot 2}b_1\dots$ indicates a binary expansion.  
Suppose that,
$$
x_1 = 0_{\dot 2} b_1 b_2 \dots b_n b_{b+1} b_{n+2}
\quad \text{and} \quad 
x_1 = 0_{\dot 2} b_1 b_2 \dots b_n b'_{b+1} b'_{n+2}
$$

## Criteria for Mathematical Chaos
There are three conditions for a function is chaos,  
$\quad$ 1. Sensitive dependence on initial conditions  
$\qquad$ Let $\forall x \in H$ and $\epsilon > 0$, then $\exists y \in H$ and   
$\quad$ 2. Denseness of periodic orbit  
$\qquad$  
$\quad$ 3. A dense orbit  
$\qquad$  

Note: There is no universally accepted definition of chaos, but