# 运筹学

## 排队论

### Poisson Distribution

$P_n(t)=\frac{(\lambda t)^n}{n!}e^{-\lambda t}, t>0, n=0, 1, 2,\cdots$

### Negative Exponential Distribution

$$f_T(t)=\left\{\begin{array}{lr}\lambda e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$$F_T(t)=\left\{\begin{array}{lr}1-e^{-\lambda t}, &t\ge0\\0,&t<0\end{array}\right.$$
$数学期望 E[T]=\frac{1}{\lambda}; 方差 Var[T]=\frac{1}{\lambda^2}; 标准差\sigma[T]=\frac{1}{\lambda}$

### Erlang Distribution

$T=v_1+v_2+\cdots+v_k, where\ v_1, v_2, \cdots, v_k i.i.d. Exp(k\mu)$

$b_k(t)=\frac{\mu k(\mu kt)^{k-1}}{(k-1)!}e^{-\mu kt},\ t>0$

$E[T]=\sum\limits_{i=1}^kE(v_i)=\sum\limits_{i=1}^k\frac{1}{k\mu}=\frac{1}{\mu}; Var[T]=\frac{1}{k\mu^2}$#

### M/M/1模型

$$\begin{array}{l}P_0=1-\rho\\P_n=(1-\rho)\rho^n,\ n\ge1\end{array}\ \rho<1$$

$$\begin{array}{ll}(1)\ L_s=\frac{\lambda}{\mu-\lambda} & (2)\ L_q=\frac{\rho\lambda}{\mu-\lambda}\\(3)\ W_s=\frac{1}{\mu-\lambda} & (4)\ W_q=\frac{\rho}{\mu-\lambda}\end{array}$$

$$\begin{array}{ll}(1)\ L_s=\lambda W_s & (2)\ L_q=\lambda W_q\\(3)\ W_s=W_q+\frac{1}{\mu} & (4)\ L_s=L_q+\frac{\lambda}{\mu}\end{array}$$

### M/M/1/N/$\infty$模型

$$\left\{\begin{array}{lc}P_0=\frac{1-\rho}{1-\rho^{N+1}} & \rho\not= 1 \\ P_n=\frac{1-\rho}{1-\rho^{N+1}} & n\le N \end{array}\right.$$

$$\left\{\begin{array}{l}
L_s=\frac{\rho}{1-\rho}-\frac{(N+1)\rho^{N+1}}{1-\rho^{N+1}}\\
L_q=L_s-(1-P_0)\\
W_s=\frac{L_s}{\mu(1-P_0)}\\
W_q=W_s-\frac{1}{\mu}
\end{array}\right.$$

$$\lambda_e=\lambda(1-P_N)$$

### Little公式

- $\mu$: 平均服务率
- $1/\mu$: 平均服务时间
- $\lambda$: 平均到达率
- $\lambda_e$: 有效到达率($\lambda,\ \lambda(1-P_N),\ \lambda(m-1))$
- $\lambda_e/\mu$: 被服务的平均顾客数. 记为$L_{se}$

$\begin{array}{l}
L_s=L_q+L_{se}\\
L_s=\lambda_eW_s\\
W_s=W_q+W_{se}\\
L_q=\lambda_eW_q
\end{array}$

## 存储论

### 模型一: 不允许缺货, 备货时间很短

$$需求速度R;\ 生产速度P; 经济订购批量Q_0;\ 初始存储量S;\ 最大缺货量B_0\\
单位时间单位物品存储费C_1;\ 缺货费C_2;\ 订购费C_3;\ 货物单价K; $$

$C(t)=\frac{C_3}{t}+KR+\frac{1}{2}C_1Rt\\
Q_0=\sqrt{\frac{2C_3R}{C_1}}; C_0=\sqrt{2C_1C_3R}$

### 模型二: 不允许缺货, 生产需要一定时间

$C(t)=\frac{1}{t}\left[\frac{1}{2}C_1(P-R)\frac{Rt^2}{P}+C_3\right]\\
t_0=\sqrt{\frac{2C_3}{C_1R}\cdot\frac{P}{P-R}}\\
Q_0=\sqrt{\frac{2C_3R}{C_1}\cdot\frac{P}{P-R}}\\
C(t_0)=\sqrt{2C_1C_3R\cdot\frac{P-R}{P}}\\
$

### 模型三: 允许缺货, 备货时间很短

$
C(t,S)=\frac{1}{t}\left[C_1\frac{S^2}{2R}+C_2\frac{(Rt-S)^2}{2R}+C_3\right]\\
t_0=\sqrt{\frac{2C_3}{C_1R}\cdot\frac{C_1+C_2}{C_2}}\\
S_0=\sqrt{\frac{2C_3R}{C_1}\cdot\frac{C_2}{C_1+C_2}}\\
C_0(t_0,S_0)=\sqrt{2C_1C_3R\cdot\frac{C_2}{C_1+C_2}}\\
$

### 模型四: 允许缺货, 生产需一定时间

$
C(t,t_2)=\frac{1}{t}\left[\frac{1}{2}C_1\frac{(P-R)R}{P}(t-t_2)^2+\frac{1}{2}C_2\frac{(P-R)R}{P}t_2^2+C_3\right]\\
t_2=\frac{C_1}{C_1+C_2}t_0\\
t_0=\sqrt{\frac{2C_3}{C_1R}\cdot\frac{C_1+C_2}{C_2}\cdot\frac{P}{P-R}}\\
Q_0=Rt_0\\
S_0=R(t_0-t_3)\\
B_0=Rt_1\\
C_0(t_0,S_0)=\sqrt{2C_1C_3R\cdot\frac{C_2}{C_1+C_2}\cdot\frac{P}{P-R}}\\
$





https://raw.githubusercontent.com/RabbitWhite1/pictures/master/operational_research/M_M_1_P_n.png