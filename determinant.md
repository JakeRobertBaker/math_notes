# Theorem

**Lemma**
$ \det(B) = (-1)^{D-1}(b_D \lambda^{D-1} + ... + b_d \lambda^{d-1} + ... +b_1) $
for
$$
B=
\left[
    \begin{matrix}
b_{D} & b_{D-1} & b_{D-2} & ... & b_{3} & b_{2} & b_{1}
\\
1 & - \lambda & 0 & ... & 0 & 0 & 0
\\
0 & 1 & - \lambda & ... & 0 & 0 & 0
\\
0 & 0 & 1 & ... & 0 & 0 & 0
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & ... & - \lambda & 0 & 0
\\
0 & 0 & 0 & ... & 1 & - \lambda & 0
\\
0 & 0 & 0 & ... & 0 & 1 & - \lambda
\end{matrix}
\right]
$$

**Proof**

Expading about column 1 we see that

$$
\det(B) = b_D
$$