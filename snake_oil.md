# Exercises: snake oil

1. Prove that $\sum_k k{n\choose k} = n\cdot 2^{n-1}$ via the snake oil method.

    <details>
    <summary>solution</summary>

    * $L(x) = P(x) = {x\over (1-2x)^2}$
    </details>

2. Evaluate $\displaystyle s_n = \sum_k k^2{n\choose k}3^k$.
    <details>
    <summary>solution</summary>

    * $S(x) = {3x(1+2x)\over (1-4x)^3}={3/8\over 1-4x}-{3/2\over (1-4x)^2}+{9/8\over (1-4x)^3}$
    * $s_n = 3\cdot 4^{n-2}\cdot n(1+3n)$
    </details>

3. Find a GF for $\displaystyle \sum_{k\ge 0} {k\choose n-k}t^k$
(no need to actually do the partial fraction expansion for any $t$).
    <details>
    <summary>solution</summary>

    * $S(x) = 1/(1-tx-tx^2)$
    </details>

4. Evaluate $\displaystyle s_n = \sum_k {n+k\choose 2k}2^{n-k}$, $n\ge 0$.
    <details>
    <summary>solution</summary>

    * $S(x) = {1-2x\over (1-x)(1-4x)}={2\over 3(1-4x)}+{1\over 3(1-x)}$
    * $s_n = (2^{2n+1}+1)/3$
    </details>

5. Find GF for $\displaystyle s_n = \sum_{k\le n/2} (-1)^k{n-k\choose k}y^{n-2k}$.
    <details>
    <summary>solution</summary>

    * $S(x) = 1/(1-xy+x^2)$
    </details>

6. Evaluate $\displaystyle s_n = \sum_{k} {2n+1\choose 2p+2k+1}{p+k\choose k}$.
    <details>
    <summary>solution</summary>

    * replace $2n+1$ by $m$ and solve for $a_m = {m-p-1\choose p}2^{m-2p-1}$;  $s_n = a_{2n+1} = {2n-p\choose p}4^{n-p}$
    * $\displaystyle A(x) = \sum_{m\ge 0} a_m x^m = {x\over (1-x)^2}\sum_{k\ge 0} {p+k\choose p} \left({x\over 1-x}\right)^{2(p+k)}={x^{p+1}\over 2^p}\cdot {(2x)^p\over (1-2x)^{p+1}}$
    </details>
 
7. Try to prove that $\sum_k {n\choose k}{2n\choose n+k}={3n\choose n}$ via the snake oil method in three different ways: consider the sum
            $\displaystyle \sum_k {n\choose k}{m\choose r-k}$ and the free variable being one of $n$, $m$, $r$.
    <details>
    <summary>solution</summary>

    * TODO
    </details>

