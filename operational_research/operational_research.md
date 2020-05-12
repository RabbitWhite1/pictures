# 运筹学

## Poisson Distribution

$P_n(t)=\frac{(\lambda t)^n}{n!}e^{-\lambda t}, t>0, n=0, 1, 2,\cdots$

## Negative Exponential Distribution

$$f_T(t)=\left\{\begin{array}{lr}\lambda e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$$F_T(t)=\left\{\begin{array}{lr}1-e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$数学期望 E[T]=\frac{1}{\lambda}; 方差 Var[T]=\frac{1}{\lambda^2}; 标准差\sigma[T]=\frac{1}{\lambda}$

## Erlang Distribution

$T=v_1+v_2+\cdots+v_k, where v_1, v_2, \cdots, v_k i.i.d. Exp(k\mu)$

$b_k(t)=\frac{\mu k(\mu kt)^{k-1}}{(k-1)!}e^{-\mu kt},\ t>0$