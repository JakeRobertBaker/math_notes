# Theorem

**Lemma**:
$ \det(B_D) = 
(-1)^{D-1}
\left(
    b_D \lambda^{D-1} + ... + b_d \lambda^{d-1} 
    + ... +
    b_1
\right)
$
for
$$
B_D=
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
\begin{align*}
\det(B_D) &= b_D (-\lambda)^{D-1} - 

\left|
\begin{matrix}
b_{D-1} & b_{D-2} & ... & b_{3} & b_{2} & b_{1}
\\
1 & - \lambda & ... & 0 & 0 & 0
\\
0 & 1 & ... & 0 & 0 & 0
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & ... & - \lambda & 0 & 0
\\
0 & 0 & ... & 1 & - \lambda & 0
\\
0 & 0 & ... & 0 & 1 & - \lambda
\end{matrix}
\right|
\\
\\
&= (-1)^{D-1} b_D \lambda^{D-1} - \det(B_{D-1})
\end{align*}
$$
This breakdown works for all $d \in \{1,2,...,D\}$.
Letting $\mathcal{E}(d)=\det(B_d)$ we get,

$$
\mathcal{E}(d) = (-1)^{d-1} b_d \lambda^{d-1} - \mathcal{E}(d-1)
$$

Therefore if we start with $\mathcal{E}(D)$ and apply
$i$
expansions we get that the coefficent for $\mathcal{E}(D-i)$ is 
$\textcolor{green}{(-1)^i}$ and $\mathcal{E}(D-i)$ looks like,

$$
\mathcal{E}(D-i) = (-1)^{D-i-1} b_{D-i} \lambda^{D-i-1}
- \mathcal{E}(D-i-1)
$$

therefore the coefficent for 
$\lambda^{D-i-1}$ is
$\textcolor{green}{(-1)^i}  (-1)^{D-i-1} b_{D-i} = (-1)^{D-1} b_{D-i}$.

Hence it holds that
$$
\mathcal{E}(D) = 
(-1)^{D-1}
\left(
    b_D \lambda^{D-1} + ... + b_d \lambda^{d-1} 
    + ... +
    b_1
\right)
$$

$\square$

**Application**

We can then find the characteristic polynomial of the matrix describing a linear reccurence relation.

$x_n = \sum_{i=1}^D a_i x_{n-i} = a_1x_{n-1} +...+ a_D x_{n-D}$

Which can be written as 
$\textbf{x}_{n} = A \textbf{x}_{n-1}$
for, 

$$
\underbrace{\left[
    \begin{matrix}
        x_n 
        \\ x_{n-1}
        \\ x_{n-2} 
        \\ x_{n-3}
        \\ \vdots 
        \\ x_{n-D+2}
        \\ x_{n-D+1}
        \\ x_{n-D}
    \end{matrix}
\right]}_{\coloneqq \textbf{x}_{n}}

=

\underbrace{\left[
    \begin{matrix}
a_{1} & a_{2} & a_{3} & ... & a_{D-2} & a_{D-1} & a_{D}
\\
1 & 0 & 0 & ... & 0 & 0 & 0
\\
0 & 1 & 0 & ... & 0 & 0 & 0
\\
0 & 0 & 1 & ... & 0 & 0 & 0
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & ... & 0 & 0 & 0
\\
0 & 0 & 0 & ... & 1 & 0 & 0
\\
0 & 0 & 0 & ... & 0 & 1 & 0
\end{matrix}
\right]}_{\coloneqq A}

\underbrace{\left[
    \begin{matrix} 
        x_{n-1}
        \\ x_{n-2} 
        \\ x_{n-3}
        \\ x_{n-4}
        \\ \vdots 
        \\ x_{n-D+1}
        \\ x_{n-D}
        \\ x_{n-D-1}
    \end{matrix}
\right]}_{\coloneqq \textbf{x}_{n-1}}
$$

Where the determinant of $A$ can be calculated with the lemma,

$$
\left|
    \begin{matrix}
a_{1} - \lambda & a_{2} & a_{3} & ... & a_{D-2} & a_{D-1} & a_{D}
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
\right| = 
(-1)^{D-1}
\left(
    - \lambda^D + a_1 \lambda^{D-1} + ... + a_{D-d+1} \lambda^{d-1} 
    + ... +
    a_D
\right)
$$