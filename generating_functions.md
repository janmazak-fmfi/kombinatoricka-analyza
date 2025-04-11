# Exercises for generating functions (GFs)

Exercises are supposed to have a solution.
Please report any errors or omissions to _jan.mazak@fmph.uniba.sk_.

## GFs without convolution (i.e. no product of GFs)

Find explicit formulas for the following sequences:
1. $a_{n+1} = 3a_n+2$ for $n\ge 0$, $a_0=0$

    <details>
    <summary>solution</summary>

    * $2x/(1-x)(1-3x)$
    * $3^n-1$
    </details>

2. $a_{n+1} = \alpha a_n + \beta$ for $n\ge 0$, $a_0=0$

    <details>
    <summary>solution</summary>

    * $\beta x/(1-x)(1-\alpha x)$
    * ${\alpha^n-1\over \alpha-1}\beta$
    </details>

3. $a_{n+1} = a_n/3 + 1$ for $n\ge 0$, $a_0=1$

    <details>
    <summary>solution</summary>

    * ${3/2\over 1-x}-{1/2\over 1-x/3}$
    * ${3^{n+1}-1\over 2\cdot 3^n}$
    </details>

4. $a_{n+2} = 2a_{n+1}-a_n$ for $n\ge 0$, $a_0=0$, $a_1=1$

    <details>
    <summary>solution</summary>

    * $x/(1-x)^2$;
    * $n$
    </details>

5. $a_{n+2} = 3a_{n+1}-2a_n+3$ for $n\ge 0$, $a_0=1$, $a_1=2$

    <details>
    <summary>solution</summary>

    * ${4\over 1-2x}-{3\over (1-x)^2}$
    * $2^{n+2}-3n-3$    </details>

6. $a_n = 2a_{n-1}-a_{n-2}+(-1)^n$ for $n>1$, $a_0=a_1=1$

    <details>
    <summary>solution</summary>

    * ${1/2\over (1-x)^2}+{1/4\over 1-x}+{1/4\over 1+x}$
    * ${2n+3+(-1)^n\over 4}$
    </details>

7. $a_n = 2a_{n-1}-n\cdot(-1)^n$ for $n\ge 1$, $a_0=0$

    <details>
    <summary>solution</summary>

    * ${x/9-2/9\over (1+x)^2}+{2/9\over 1-2x}$
    * ${2^{n+1}-(3n+2)(-1)^n\over 9}$
    </details>

8. $a_n = 3a_{n-1} + {n\choose 2}$ for $n\ge 1$, $a_0=2$

    <details>
    <summary>solution</summary>

    * $A(x) = \frac{-2x^3 + 7x^2 - 6x + 2}{(1-3x)(1-x)^3}$
    * ${1\over 8}(19\cdot 3^n-2n(n+2)-3)$
    </details>

9. $a_n = 2a_{n-1}-a_{n-2}-2$ for $n > 1$, $a_0=a_{10}=0$

    <details>
    <summary>solution</summary>

    * $A(x) = \frac{9x - 11 x^2}{(1-x)^3} = \frac{-11}{1-x} + \frac{13}{(1-x)^2} - \frac{2}{(1-x)^3}$
    * $n(a_1+1-n)$, so with $a_{10}$, $a_n=n(10-n)$
    </details>

10. $a_n = 4(a_{n-1}-a_{n-2})+(-1)^n$ for $n \ge 2$, $a_0=1$, $a_1=4$

    <details>
    <summary>solution</summary>

    * ${1+x+x^2\over (1+x)(1-2x)^2} = {1\over 9}{1\over 1+x} +\left({-5\over 18}\right) {1\over 1-2x} + \left({7\over 6}\right){1\over (1-2x)^2}$
    * ${1\over 9}(-1)^n-{5\over 18}\cdot 2^n+{7\over 6}(n+1)\cdot 2^n$
    </details>

11. $a_n = -3a_{n-1}+a_{n-2}+3a_{n-3}$ for $n\ge 3$, $a_0=20$, $a_1=-36$, $a_2=60$

    <details>
    <summary>solution</summary>

    * $A(x) = \frac{20 + 24x - 68x^2}{(1+3x)(1-x^2)}$
    * $5\cdot(-3)^n+18\cdot(-1)^n-3$
    </details>

12. $a_n = -3a_{n-1}+a_{n-2}+3a_{n-3}+128n$ for $n\ge 3$, $a_0=0$, $a_1=0$, $a_2=0$

    <details>
    <summary>solution</summary>

    * $A(x) = \frac{128 x^3 (3-2x)}{(1+3x)(1-x)^3(1+x)}$
    * $8n^2+28n-29-11(-3)^n+40(-1)^n$
    </details>


## GFs with convolution (i.e. products of GFs sometimes needed)

Before doing the computations, check the book
[generatingfunctionology](https://www2.math.upenn.edu/~wilf/gfologyLinked2.pdf).
Specifically, Rules 1 to 5 in Section 2.2.

1. Solve $g_n=g_{n-1}+g_{n-2}$ for $n\ge 2$, $g_0 = 0$, $g_{10} = 10.$

    <details>
    <summary>solution</summary>

    * $g_n = {g_{10}\over F_{10}}F_n$
    * try also the ``boundary method'' from the lecture, computer necessary
    </details>

2. Using Rule 5, prove that $F_0+F_1+\dots+F_n=F_{n+2}-1$ for $n\ge 0$.\
    [Wilf 38, example 6]

    <details>
    <summary>solution</summary>

    * Compare gfs of both sides, left is $f/(1-x)$, where $f = x/(1-x-x^2)$, i.e. Fibonacci.
    </details>

3. Solve $a_n = \sum_{k=0}^{n-1}a_k$ for $n > 0$, $a_0 = 1$.\
    [R16]

    <details>
    <summary>solution</summary>

    * $a_n = 2^{n-1}$ for $n \ge 1$
    </details>

4. Solve $f_n=2f_{n-1}+f_{n-2}+f_{n-3}+\dots+f_1+1$ for $n\ge 1$, $f_0 = 0$.\
    [Knuth 349/(7.41)]

    <details>
    <summary>solution</summary>

    * $F(x) = x/(1-3x+x^2)$
    * $f_n=F_{2n}$
    </details>

5. Solve $g_n = g_{n-1} + 2g_{n-2}+\dots +ng_0$ for $n > 0$, $g_0 = 1$.\
    [K7.7]

    <details>
    <summary>solution</summary>

    * $G(x)=1+{x\over 1-3x+x^2}$
    * $g_n=F_{2n} + [n=0]$
    </details>

6. Solve $g_n = \sum_{k=1}^{n-1} {g_k + g_{n-k} + k\over 2}$ for $n\ge 2$, $g_1 = 1$.

    <details>
    <summary>solution</summary>

    * $G(x)=\frac{2x-3x^2+2x^3}{2(1-x)^2(1-2x)}$
    * $g_n=3\cdot 2^{n-2}-\frac{n+1}{2}$ for $n\ge 2$
    </details>

7. Solve $g_n=g_{n-1}+2g_{n-2}+(-1)^n$ for $n\ge 2$, $g_0 = g_1 = 1$.

    <details>
    <summary>solution</summary>

    * $G(x) = {1+x+x^2\over (1-2x)(1+x)^2}$
    * $g_n = {7\over 9}2^n + {1\over 9}(3n+2)(-1)^n$
    </details>

8. Solve $a_{n+2}=3a_{n+1}-2a_n+n+1$ for $n\ge 0$, $a_0 = a_1 = 1$\
    [R24]

    <details>
    <summary>solution</summary>

    * $A(z) = {2\over 1-2z}-{1\over (1-z)^3}$
    * $a_n = 2^{n+1}-{n+2\choose 2}$
    </details>


9. Prove that $\ln {1\over 1-x} = \sum_{n\ge 1} {1\over n} x^n$.
    <details>
    <summary>solution</summary>

    * consider $\int {1\over 1-x}$
    </details>


## Skipping sequence elements via GFs

1. Assume that $A(x)$ is the ogf for $(a_n)$. Express the generating function for $\sum_{n\ge 0} a_{3n}x^n$ in terms of $A(x)$.
    <details>
    <summary>solution</summary>

    * ${1\over 3}(A(x^{1/3}) + A(\omega x^{1/3})) + A(\omega^2 x^{1/3})$, where $\omega=e^{2\pi i/3}$
    </details>

2. Compute $S_n=\sum_{n\ge 0} F_{3n}\cdot 10^{-n}$ (by plugging a suitable value into the generating function for $F_{3n}$).
    <details>
    <summary>solution</summary>

    * The gf is ${2x\over 1-4x-x^2}$ and $S_n=20/59$.
    </details>

3. Compute $\sum_k {n\choose 4k}$.
    <details>
    <summary>solution</summary>

    * $2^{{n\over 2} - 2} \left(2^{n\over 2} + \cos\left({1\over 4}n \pi\right) + (-1)^n \cos\left({3\over 4}n \pi\right)\right)$
    </details>

4. Compute $\sum_k {6m\choose 3k+1}$.
    <details>
    <summary>solution</summary>

    * Compute it for general $n$ and then plug in $n=6m$
    * $(2^{6m}-1)/3$
    </details>


## More exercises

5. Evaluate $S_n = \sum_{0\le k\le n} (-1)^k k^2$.
    <details>
    <summary>solution</summary>

    * $S(x) = {-x\over (1+x)^3}$
    * $S_n={1\over 2}(-1)^n n(n+1)$
    </details>

6. Find ogf for $H_n = 1 + 1/2 + 1/3 + \dots$.
    <details>
    <summary>solution</summary>

    * ${-\ln(1-x) \over 1-x}$
    </details>

7. Find the number of ways of cutting a convex $n$-gon with labelled vertices into triangles.
    <details>
    <summary>solution</summary>

    * $C_{n-2}$ (shifted Catalan numbers)
    </details>

