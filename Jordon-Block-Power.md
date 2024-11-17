# Jordon Block Powers

Let $\dim(\mathbf{V})=n$ and let's consider the Jordan Block

$$
\mathbf{J} = 
\left[\begin{matrix}
\lambda & 1 & 0 & ... & 0 & 0 & 0
\\
0 & \lambda & 1 & ... & 0 & 0 & 0
\\
0 & 0 & \lambda & ... & 0 & 0 & 0
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & ... & \lambda & 1 & 0
\\
0 & 0 & 0 & ... & 0 & \lambda & 1
\\
0 & 0 & 0 & ... & 0 & 0 & \lambda\end{matrix}
\right]
= 
\lambda \mathbf{I} + \mathbf{N}
$$

for 

$$
\mathbf{N} = 
\left[\begin{matrix}
0 & 1 & 0 & ... & 0 & 0 & 0
\\
0 & 0 & 1 & ... & 0 & 0 & 0
\\
0 & 0 & 0 & ... & 0 & 0 & 0
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & ... & 0 & 1 & 0
\\
0 & 0 & 0 & ... & 0 & 0 & 1
\\
0 & 0 & 0 & ... & 0 & 0 & 0\end{matrix}
\right]
$$.

Now it is clear that for basis $v_1...v_n$ of v that,

$$
\mathbf{N}v_k = 
\begin{cases}
    0 & \text{if } k=1
    \\
    v_{k-1} & \text{if } k= 2, \ ... \ n
\end{cases}
$$

it therefore follows that

$$
\mathbf{N}^rv_k = 
\begin{cases}
    0 & \text{if } k \leq r
    \\
    v_{k-r} & \text{if } k > r
\end{cases}
$$.

Hence the bionomial expansion gives us that

$$
\begin{align*}
\mathbf{J}^m  
= 
(\mathbf{\lambda I + N})^m
=
\sum_{r=0}^m \binom{m}{r}\lambda^{n-r} \mathbf{N}^r
\end{align*}
$$

and therefore

$$
\begin{align*}
\mathbf{J}^m v_k
= 
(\mathbf{\lambda I + N})^m
&=
\sum_{r=0}^m \binom{m}{r}\lambda^{n-r}
\mathbf{N}^r v_k
\\
&=
\sum_{r<k} \binom{m}{r}\lambda^{n-r}
v_{k-r}
\\
&=
\sum_{r=0}^{k-1} \binom{m}{r}\lambda^{n-r}
v_{k-r}
\\
&= 
\sum_{i=1}^k \binom{m}{k-i} \lambda^{n+i-k} v_i
\end{align*}
$$

Therefore J look like

$$
\left[\begin{matrix}
\lambda^{n} & \lambda^{n - 1} m & \lambda^{n - 2} {\binom{m}{2}} & \ldots & \lambda^{- k + n + 2} {\binom{m}{k - 2}} & \lambda^{- k + n + 1} {\binom{m}{k - 1}} & \lambda^{- k + n} {\binom{m}{k}} & \ldots & \lambda^{2} {\binom{m}{n - 2}} & \lambda {\binom{m}{n - 1}}
\\
0 & \lambda^{n} & \lambda^{n - 1} m & \ldots & \lambda^{- k + n + 3} {\binom{m}{k - 3}} & \lambda^{- k + n + 2} {\binom{m}{k - 2}} & \lambda^{- k + n + 1} {\binom{m}{k - 1}} & \ldots & \lambda^{3} {\binom{m}{n - 3}} & \lambda^{2} {\binom{m}{n - 2}}
\\
0 & 0 & \lambda^{n} & \ldots & \lambda^{- k + n + 4} {\binom{m}{k - 4}} & \lambda^{- k + n + 3} {\binom{m}{k - 3}} & \lambda^{- k + n + 2} {\binom{m}{k - 2}} & \ldots & \lambda^{4} {\binom{m}{n - 4}} & \lambda^{3} {\binom{m}{n - 3}}
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & 0 & \lambda^{i - k + n} {\binom{m}{- i + k}} & \lambda^{i - k + n - 1} {\binom{m}{- i + k + 1}} & \lambda^{i - k + n - 2} {\binom{m}{- i + k + 2}} & \ldots & \lambda^{i} {\binom{m}{- i + n}} & \lambda^{i - 1} {\binom{m}{- i + n + 1}}
\\
0 & 0 & 0 & 0 & 0 & \lambda^{i - k + n} {\binom{m}{- i + k}} & \lambda^{i - k + n - 1} {\binom{m}{- i + k + 1}} & \ldots & \lambda^{i + 1} {\binom{m}{- i + n - 1}} & \lambda^{i} {\binom{m}{- i + n}}
\\
0 & 0 & 0 & 0 & 0 & 0 & \lambda^{i - k + n} {\binom{m}{- i + k}} & \ldots & \lambda^{i + 2} {\binom{m}{- i + n - 2}} & \lambda^{i + 1} {\binom{m}{- i + n - 1}}
\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \lambda^{n} & \lambda^{n - 1} m
\\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \lambda^{n}\end{matrix}
\right]

$$