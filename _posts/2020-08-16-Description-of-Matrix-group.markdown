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

Матрицы из $M_n$ образуют абелевую группу. 

---

#### Порядок группы $M_n$

**Теорема:**

$$M_n = \begin{cases}
\varphi(n)^2 & \text{n is odd} \\
2\varphi(n)^2 & \text{n is even} \\
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

Рассмотрим отображение $f: M_n \rightarrow \mathbb{Z}_n \times \mathbb{Z}_n$, заданное формулой:

$$f\left( \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} \right) = \begin{pmatrix}
a+b  \\
a-b
\end{pmatrix}$$

Заметим, что 

$$f\left( \begin{pmatrix}
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

Отсюда $f$ — сохраняет групповую операцию, и следовательно $f$ — гомоморфизм $f: M_n \rightarrow \mathbb{Z}_n^* \times \mathbb{Z}_n^*$

Пусть $\alpha, \beta \in \mathbb{Z}_n^*$ и рассмотрим систему

$$\begin{cases}
a+b = \alpha \\
a-b = \beta
\end{cases}$$

Так как главная матрица этой системы $T$ обратима, то система имеет единственное. Отсюда $f$ — биекция, и следовательно $M_n \simeq \mathbb{Z}_n^* \times \mathbb{Z}_n^*$

Пусть теперь $n$ четно. Так-же, рассмотрим отображение $f: M_n \rightarrow \mathbb{Z}_n \times \mathbb{Z}_n$

$$f\left( \begin{pmatrix}
a & b \\
b & a
\end{pmatrix} \right) = \begin{pmatrix}
a+b  \\
a-b
\end{pmatrix}$$

Которое по прежнему будет гомоморфизмом  $f: M_n \rightarrow \mathbb{Z}_n^* \times \mathbb{Z}_n^*$. Однако в этом случае матрица $T$ уже не будет обратимой. Рассмотрим уравнение

$$\begin{cases}
a+b = 0 \\
a-b = 0
\end{cases}$$

При четном $n$ уравнение имеет еще одно решение в $\mathbb{Z}_n$: $a = b = \frac{n}{2}$.

Отсюда $\ker(f) = \\{ 1, \varepsilon \\}$, где  

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
$$M_n/\ker(f) \simeq  \mathbb{Z}_n^* \times \mathbb{Z}_n^*$$

---
