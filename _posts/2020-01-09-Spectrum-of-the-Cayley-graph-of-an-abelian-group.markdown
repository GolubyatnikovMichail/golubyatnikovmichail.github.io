---
layout: post
mathjax: true
title:  "Спектр графа Кэли абелевой группы."
date: 2020-01-09
categories: group-theory graph-theory
---

Пусть $G$ — конечная абелева группа порядка $n$. И $S \subset G$: 

1. $1 \notin S$
2. $S = S^{-1}$ 
3. $\langle S \rangle = G$

И пусть $\Gamma$ — граф Кэли $(G, S)$. Пусть $\chi_i$ ($i=1,\dots, n$)  — различные характеры группы $G$. Тогда ${\rm Spec}(\Gamma) = \\{\chi_i(S) : i=1,\dots,n\\}$, где $\chi(S) = \sum_{s\in S}\chi(s).$ 

---

Пусть $G$ — конечная абелева группа типа $(m_1, \dots, m_d)$, где $m_i \| m_{i+1}$
и $n = \prod\limits_{i=1}^{d}m_i$

Тогда, $G = \langle a_i \rangle \times \cdots \times \langle a_d \rangle$, где $\|\langle a_i \rangle\| = m_i.$

Имеется каноническая биекция между множеством характеров $\{ \chi_i \}$ и $G$.

Пусть $a\in G$ и $a = a_1^{x_1} \cdots a_d^{x_d}$,  $\zeta_i$ — примитивный корень степени $m_i$ из единицы, тогда

$$\chi_{a}(a_1^{y_1} \cdots a_d^{y_d})= \chi_{x_1, x_2, \dots, x_d}(a_1^{x_1} \cdots a_d^{x_d}) =\zeta_1^{x_1 y_1} \cdots \zeta_d^{x_d y_d}$$

И значит

$${\rm Spec}(\Gamma) = \{ x_1,x_2,\dots,x_d \;|\; \chi_{x_1,x_2,\dots,x_d}(S) \}$$

Пусть $k = \|S\|$ и $S = \\{s_1, \dots, s_k\\}$, тогда любой элемент из $s \in S$ имеет вид:

$$s_1 =  a_1^{k_{11}} \cdot a_2^{k_{12}} \dots a_d^{k_{1d}}$$

$$s_2 =  a_1^{k_{21}} \cdot a_2^{k_{22}} \dots a_d^{k_{2d}}$$ 

$$ \dots $$

$$s_k  =  a_1^{k_{k1}} \cdot a_2^{k_{k2}} \dots a_d^{k_{kd}}$$

Тогда

$$\chi_{x_1,x_2,\dots,x_d}(S) = \sum_{s\in S}\chi_{x_1,x_2,\dots,x_d}(s) =
\sum_{l = 1}^k\chi_{x_1,x_2,\dots,x_d}(a_1^{k_{l1}} \cdot a_2^{k_{l2}} \dots a_d^{k_{ld}}) = \sum_{l = 1}^k \zeta_1^{x_1 k_{l1}} \cdots \zeta_d^{x_d k_{ld}}$$

Отсюда

$${\rm Spec}(\Gamma) = \{x_1,x_2,\dots,x_d \;|\; \left(\sum_{l = 1}^k \zeta_1^{x_1 k_{l1}} \cdots \zeta_d^{x_d k_{ld}}\right) \}$$

где $x_i$ пробегают множество $\\{1, 2, \dots, m_i\\}$, отсюда

Заметим

$$\zeta_1^{x_1 k_{l1}} \cdots \zeta_d^{x_d k_{ld}} = e^{\frac{2i\pi}{m_1}x_1k_{1l}} \cdots e^{\frac{2i\pi}{m_d}x_dk_{dl}} = e^{ {\frac{2i\pi}{m_1}x_1k_{1l}} + \cdots +{\frac{2i\pi}{m_d}x_dk_{dl}} }$$

$${\frac{2i\pi}{m_1}x_1k_{1l}} + \cdots +{\frac{2i\pi}{m_d}x_dk_{dl}} = 2i\pi\sum\limits_{i=1}^d \frac{x_i k_{li}}{m_i}$$

Пусть $K$ — $d \times k$ матрица: $(K_{li}) = \frac{k_{li}}{m_i}$, обозначим $1_k$ — вектор размера $k$ — состоящий из одних единиц. Введем вектор функцию $F(x_1,x_2,\dots,x_d) = K\cdot {\rm x}$, где ${\rm x} = (x_1,x_2,\dots,x_d)^{T}$

Тогда:

$${\rm Spec}(\Gamma) = \{ x_1,x_2,\dots,x_d \;|\; \left( e^{2\pi i F(x_1,x_2,\dots,x_d)},  1_k \right) \}$$

где $e^{2\pi i F(x_1,x_2,\dots,x_d)}$ — вектор функция, а $(\cdot, \cdot)$ — стандартное скалярное произведение.