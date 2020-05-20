# 运筹学

## Poisson Distribution

$P_n(t)=\frac{(\lambda t)^n}{n!}e^{-\lambda t}, t>0, n=0, 1, 2,\cdots$

## Negative Exponential Distribution

$$f_T(t)=\left\{\begin{array}{lr}\lambda e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$$F_T(t)=\left\{\begin{array}{lr}1-e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$数学期望 E[T]=\frac{1}{\lambda}; 方差 Var[T]=\frac{1}{\lambda^2}; 标准差\sigma[T]=\frac{1}{\lambda}$

## Erlang Distribution

$T=v_1+v_2+\cdots+v_k, where\ v_1, v_2, \cdots, v_k i.i.d. Exp(k\mu)$

$b_k(t)=\frac{\mu k(\mu kt)^{k-1}}{(k-1)!}e^{-\mu kt},\ t>0$

$E[T]=\sum\limits_{i=1}^kE(v_i)=\sum\limits_{i=1}^k\frac{1}{k\mu}=\frac{1}{\mu}; Var[T]=\frac{1}{k\mu^2}$#

## M/M/1模型

$$\begin{array}{l}P_0=1-\rho\\P_n=(1-\rho)\rho^n,\ n\ge1\end{array}\ \rho<1$$

$$\begin{array}{ll}(1)\ L_s=\frac{\lambda}{\mu-\lambda} & (2)\ L_q=\frac{\rho\lambda}{\mu-\lambda}\\(3)\ W_s=\frac{1}{\mu-\lambda} & (4)\ W_q=\frac{\rho}{\mu-\lambda}\end{array}$$

$$\begin{array}{ll}(1)\ L_s=\lambda W_s & (2)\ L_q=\lambda W_q\\(3)\ W_s=W_q+\frac{1}{\mu} & (4)\ L_s=L_q+\frac{\lambda}{\mu}\end{array}$$

## M/M/1/N/$\infty$模型

$$\left\{\begin{array}{lc}P_0=\frac{1-\rho}{1-\rho^{N+1}} & \rho\not= 1 \\ P_n=\frac{1-\rho}{1-\rho^{N+1}} & n\le N \end{array}\right.$$

$$\left\{\begin{array}{l}
L_s=\frac{\rho}{1-\rho}-\frac{(N+1)\rho^{N+1}}{1-\rho^{N+1}}\\
L_q=L_s-(1-P_0)\\
W_s=\frac{L_s}{\mu(1-P_0)}\\
W_q=W_s-\frac{1}{\mu}
\end{array}\right.$$

https://raw.githubusercontent.com/RabbitWhite1/pictures/master/operational_research/M_M_1_P_n.png