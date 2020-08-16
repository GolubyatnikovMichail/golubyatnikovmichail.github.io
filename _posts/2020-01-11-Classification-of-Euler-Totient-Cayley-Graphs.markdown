---
layout: post
mathjax: true
title:  "Classification of Euler Totient Cayley Graphs"
date:   2020-01-11
categories: group-theory graph-theory
---

# Classification of Euler Totient Cayley Graphs

####  Euler Totient Cayley Graph 

Пусть $G = \mathbb{Z}_n$, $S = \\{k, (k,n)=1, k\le n\\}$, $\|S\| = \varphi(n)$, $n = p_1^{a_1} \cdots p_d^{a_d}$ 


Рассмотрим функцию

$$F(n, k) = \sum \limits_{\substack{s = 1 \\(s,n)=1}}^\frac{n-1}{2} \cos\left(\frac{2\pi ks}{n}\right)$$

Заметим, что 

$$\mu(n) = F(n,1)$$

$$\varphi(n) = F(n,n)$$

Спектр графа $\Gamma$:

$${\rm Spec}(\Gamma) = \{F(n,k) \, | \, 1\le k\le n \}$$

$$F(n,k) = \mu\left(\frac{n}{(n,k)}\right) \frac{\varphi(n)}{\varphi\left(\frac{n}{(n,k)}\right)}$$

$$F(n,k) = \sum\limits_{d|(n,k)}d\mu\left(\frac{n}{d}\right)$$

Если $n$–простое, то $F(p,p) = \mu(p)+p\mu(1) = p-1$, $F(p,k) = \mu(p) = -1$ (при $k \ne p$) и ${\rm Spec}(\Gamma_n) = \\{(p-1)^1, (-1)^{p-1} \\}$ и значит $\Gamma$ — полный граф.

Если  $n=p^k$ ($p$ — простое).  Тогда если $(n,l)=1$, то $F(p^k,l) = \mu(p^k) = 0$, отсюда $0$ — собственное значение графа $\Gamma_n$, кратности не меньше $p^{k-1}(p-1)$

Если $(p^k,l)=p^i$ ($i \le k$), то

$$F(p^k,l) = \sum\limits_{d|p^i}d\mu\left(\frac{p^k}{d}\right) = 
\sum\limits_{t=0}^{i} p^t \mu(p^{k-t}) = \mu(p^{k-i}) p^{i}$$

Если $k-i\ge 2$, то $\mu(p^{k-i}) = 0$. Обозначим $L(i) = \\{l \, : \, (p^k,l)=p^i\\}$, тогда кратность $0$ равняется $\|L(0)\|+\|L(1)\|+\|L(2)\|+\cdots+\|L(k-2)\|$

Если $i=k-1$, то $F(p^k,l) = \mu(p) p^{k-1} = -p^{k-1}$. 

Если $l=p^k$, то $F(p^k,p^k) = \varphi(p^k) = p^{k-1}(p-1)$. Отсюда 

$${\rm Spec}(\Gamma_n) = \{(p^{k-1}(p-1))^1, 0^{|L(1)|+|L(2)|+\cdots+|L(k-2)|}, (-p^{k-1})^{|L(k-1)|}\}$$

Заметим, что 

$$L(k-1) = \{p^{k-1}, 2p^{k-1},\dots,(p-1)p^{k-1} \}$$

$$|L(k-1)| = p-1$$

и

$$|L(1)|+|L(2)|+\cdots+|L(k-2)| = n - |L(k-1)| - |L(k)| = p^k-p$$

Окончательно получаем спектр графа $\Gamma_n$

$${\rm Spec}(\Gamma_n) = \{(p^{k-1}(p-1))^1, 0^{p^k-p}, (-p^{k-1})^{p-1}\}$$

Отсюда $\Gamma_n$ — сильно регулярный граф с параметрами: $(p^k, p^{k-1}(p-1),p^{k-1}(p-2),p^{k-1}(p-1))$ и $\Gamma_n$ — полный многодольный граф с долями порядка $p^{k-1}$ (дополнительный граф к дополнение к $pK_{p^{k-1}}$). 

Пусть теперь $n,m$ — два взаимно простых натуральный числа и $\Gamma_n$, $\Gamma_m$, $\Gamma_{nm}$ — Euler Totient Cayley Graphs (ETCG) порядка $n, m, nm$ соответственно.  Построим изоморфизм $\phi : \Gamma_{nm} \rightarrow \Gamma_n \times \Gamma_m$. 

Пусть $x \in \\{1,2,\dots,nm\\}$, по китайской теореме об остатках существуют $x_1 \in \\{1,2,\dots,n\\}$, $x_2 \in \\{1,2,\dots,m\\}$, что $x = nk+x_1$ и $x = mh+x_2$. Определим $\phi(x) = (x_1, x_2)$.

Очевидно, $\phi$  биекция. Покажем что $\phi$ — изоморфизм графов. Пусть $x, y \in \\{1,2,\dots,nm\\}$, $x, y$ смежны в графе $\Gamma_{mn}$ тогда и только тогда, когда $\gcd(x-y,mn) = 1$. Так как $\gcd(m,n)=1$, то $\gcd(x-y,mn) = \gcd(x-y,m)\gcd(x-y,n)$ и значит $\gcd(x-y,m)=1$ и $\gcd(x-y,n) = 1$.  

$$\gcd(x-y,n) = \gcd((nk+x_1)-(nk'+y_1),n) = \gcd(n(k-k')+(x_1-y_1),n)=\gcd(x_1-y_1,n)$$

Аналогично 

$$\gcd(x-y,n) = \gcd((mh+x_2)-(mh'+y_2),m) = \gcd(m(h-h')+(x_2-y_2),m)=\gcd(x_2-y_2,m)$$

Следовательно $\gcd(x-y,m)=1$ и $\gcd(x-y,n) = 1$. тогда и только тогда, когда $\gcd(x_1-y_1,n)=1$ и $\gcd(x_2-y_2,m)=1$, то есть пара $(x_1, x_2)$ и $(y_1, y_2)$ смежны в графе $\Gamma_n \times \Gamma_m$.

Мы доказали следующую классификационную теорему:


Пусть $\Gamma_n = {\rm Caley}(\mathbb{Z}_n, \{k, (k,n)=1, k\le n\})$, тогда 

1. Если $n$ — простое число, то $\Gamma_n$ — полный граф на $n$ — вершинах

2. Если $n=p^k$ ($p$ — простое, $k>1$), то $\Gamma_n$ — дополнение к $pK_{p^{k-1}}$

3. Если $(n,m)=1$, то $\Gamma_{mn} = \Gamma_n \times \Gamma_m$ (тензорное произведение графов)

---

### Спектральные мометны графов

Пусть $M_n(s) = {\rm tr}(\Gamma_n^s)$

$$M_n(s) = \sum\limits_{k=1}^{n} F(n,k)^s = \sum\limits_{k=1}^{n} \left(\sum\limits_{d|(n,k)}d\mu\left(\frac{n}{d}\right)\right)^s$$

Если $(n,m)=1$, то $M_{nm}(s)=M_n(s)M_m(s)$

$$M_p(s) = (p-1)^s+(-1)^s(p-1)$$

$$M_{p^k}(s) = (p^{k-1}(p-1))^s + ({p^k-p})0^s + (p-1)(-p^{k-1})^s$$

Если $s > 0$:

$$M_{p^k}(s) = p^{s(k-1)}((p-1)^s + (-1)^s(p-1)) = p^{s(k-1)}M_p(s)$$

Если $n = p_1^{a_1} \cdot p_2^{a_2}\cdots p_d^{a_d}$, тогда 

$$M_{n}(s) = \begin{cases} 
\prod\limits_{i=1}^{d} p_i^{s(a_i-1)}((p_i-1)^s + (p_i-1)) & s \text{ - even} \\
\prod\limits_{i=1}^{d} p_i^{s(a_i-1)}((p_i-1)^s - (p_i-1)) & s \text{ - odd}
\end{cases}$$

---