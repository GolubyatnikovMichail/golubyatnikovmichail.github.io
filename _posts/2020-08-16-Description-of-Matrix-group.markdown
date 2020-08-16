---
layout: post
mathjax: true
title:  "Описание одной матричной группы."
date: 2020-08-16
categories: group-theory
---

Пусть 

$$
M_n = \left\{ \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} : a,b \in \mathbb{Z_n}, \gcd(a^2-b^2, n)=1  \right\}
$$

Матрицы из $$M_n$$ образуют абелевую группу. 

---

#### Структура группы $M_n$

**Теорема:**

$$M_n \simeq \begin{cases}
\mathbb{Z}_n^* \times \mathbb{Z}_n^* & \text{n is odd} \\
\mathbb{Z}_2 \times \mathbb{Z}_n^* \times \mathbb{Z}_n^* & \text{n is even} \\
\end{cases}$$

где $\varphi(n)$ — функция Эйлера.

*Доказательство*:

Заметим, что 

$$\begin{pmatrix}
a & b \\
b & a
\end{pmatrix} 
\begin{pmatrix}
1  \\
1 
\end{pmatrix} 
= (a+b)
\begin{pmatrix}
1  \\
1 
\end{pmatrix}$$

и

$$\begin{pmatrix}
a & b \\
b & a
\end{pmatrix} 
\begin{pmatrix}
1  \\
-1 
\end{pmatrix} 
= (a-b)
\begin{pmatrix}
1  \\
-1 
\end{pmatrix}$$

Пусть $n$ — нечетно, обозначим 

$$T =\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}$$


тогда $\det(T)=-2$ и как $\gcd(-2,n)=1$, то матрица $T$ обратима в $\mathbb{Z_n}$.

Рассмотрим отображение $\varphi: M_n \rightarrow \mathbb{Z}_n \times \mathbb{Z}_n$, заданное формулой:

$$\varphi\left( \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} \right) = \begin{pmatrix}
a+b  \\
a-b
\end{pmatrix}$$

Заметим, что 

$$\varphi\left( \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} 
\begin{pmatrix}
a' & b' \\
b' & a'
\end{pmatrix}\right) = \begin{pmatrix}
(aa'+bb') + (ab'+ba')  \\
(aa'+bb') - (ab'+ba') 
\end{pmatrix} = 
\begin{pmatrix}
a+b  \\
a-b
\end{pmatrix}\begin{pmatrix}
a'+b'  \\
a'-b'
\end{pmatrix}$$

Отсюда $\varphi$ — сохраняет групповую операцию, и следовательно $\varphi$ — гомоморфизм $\varphi: M_n \rightarrow \mathbb{Z}_n^* \times \mathbb{Z}_n^*$

Пусть $\alpha, \beta \in \mathbb{Z}_n^*$ и рассмотрим систему

$$\begin{cases}
a+b = \alpha \\
a-b = \beta
\end{cases}$$

Так как главная матрица этой системы $T$ обратима, то система имеет единственное. Отсюда $\varphi$ — биекция, и следовательно $M_n \simeq \mathbb{Z}_n^* \times \mathbb{Z}_n^*$

Пусть теперь $n$ четно. Так-же, рассмотрим отображение $\varphi: M_n \rightarrow \mathbb{Z}_n \times \mathbb{Z}_n$

$$\varphi\left( \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} \right) = \begin{pmatrix}
a+b  \\
a-b
\end{pmatrix}$$

Которое по прежнему будет гомоморфизмом  $\varphi: M_n \rightarrow \mathbb{Z}_n^* \times \mathbb{Z}_n^*$. Однако в этом случае матрица $T$ уже не будет обратимой. Рассмотрим уравнение

$$\begin{cases}
a+b = 0 \\
a-b = 0
\end{cases}$$

При четном $n$ уравнение имеет еще одно решение в $\mathbb{Z}_n$: $a = b = \frac{n}{2}$.

Отсюда $\ker(\varphi) = \{1, \varepsilon\}$, где  

$$\varepsilon = 
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} + \begin{pmatrix}
\frac{n}{2} & \frac{n}{2} \\
\frac{n}{2} & \frac{n}{2}
\end{pmatrix} = 
\begin{pmatrix}
1+\frac{n}{2} & \frac{n}{2} \\
\frac{n}{2} & 1+\frac{n}{2}
\end{pmatrix}$$

Заметим, что $\varepsilon^2 = 1$. Отсюда 
$$M_n/\ker(\varphi) \simeq  \mathbb{Z}_n^* \times \mathbb{Z}_n^*$$

и $M_n \simeq \mathbb{Z}_2 \times \mathbb{Z}_n^* \times \mathbb{Z}_n^*$

---

#### Число порождающих группы $M_n$

Минимальное число порождающих группы $\mathbb{Z}_n^*$, определяется формулой:

$$r(n) = \begin{cases}
\omega(n) - 1 &  \text{if } n>2, 2|n \text{ and } 4 \nmid  n\\
\omega(n) + 1 &  \text{if } 8|n \\
\omega(n) &  \text{other cases}
\end{cases}$$

где функция $\omega(n)$ — число различных простых делителей числа $n$

Отсюда минимальное число порождающих $g(n)$ определится формулой

$$g(n) = \begin{cases}
2r(n) & \text{n is odd} \\
2r(n)+ 1 & \text{n is even} \\
\end{cases}$$
