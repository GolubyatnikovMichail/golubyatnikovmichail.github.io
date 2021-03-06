---
layout: post
mathjax: true
title:  "Теорема Нивена"
date: 2020-07-28
categories: number-theory
---

**Теорема:**

​Рассмотрим угол  $\theta$,  принадлежащее промежутку $0 \le \theta \le \pi$ и такой что $\frac{\theta}{\pi} \in \mathbb{Q}$.  Тогда  $\cos(\theta) \in \mathbb{Q}$, только при 
$\theta \in \\\{0, \frac{\pi}{3}, \frac{\pi}{2}, \frac{2\pi}{3}, \pi \\\}$

*Доказательство:*

Пусть $T_n(x)$ — многочлен Чебышёва первого рода.  Который может быть определен с помощью равенства:

$$T_n(\cos(x))=\cos(nx)$$

при этом выполняются следующие свойства:

$$deg(T_n) = n$$

$$\text{leading coefficient } T_n \text{ is } 2^{n-1}$$

$$T_n(0) \in \{-1, 0, 1\}$$

Рассмотрим многочлен 

$$F_n(x) = 2T_n\left(\frac{x}{2}\right)$$

Тогда заметим что $F_n(x)$ является многочленом степени $n$ со старшим коэффициентом $1$. И выполняется равенство 

$$F_n(2\cos(x))=2\cos(nx)$$

Обозначим $\theta = \frac{n}{m}\pi$. Тогда 

$$F_m\left(2\cos\left(\frac{n}{m}\pi \right)\right)=2\cos(n \pi) = 2(-1)^n$$

Следовательно $2\cos(\theta)$ является корнем уравнения $F_m(x) \pm 2$. По теореме о рациональном корне имеем $2\cos(\theta) \in \mathbb{Z}$. Так как $\|\cos(\theta)\| \le 1$, то $2\cos(\theta) \in \\{-2, -1, 0, 1, 2\\}$. Отсюда 

$$\theta \in \left\{0, \frac{\pi}{3}, \frac{\pi}{2}, \frac{2\pi}{3}, \pi \right\}$$

### Квадратичные иррациональности

**Теорема:**

Рассмотрим угол  $\theta$,  принадлежащее промежутку $0 \le \theta \le \pi$ и такой что $\frac{\theta}{\pi} \in \mathbb{Q}$.  Тогда  $\cos(\theta)$ принадлежит квадратичному расширению поля $\mathbb{Q}$, только при 

$$\theta \in \left\{ \frac{\pi}{6}, \frac{\pi}{5}, \frac{\pi}{4},
\frac{2\pi}{5}, \frac{3\pi}{5}, \frac{3\pi}{4}, \frac{4\pi}{5}, \frac{5\pi}{6} \right\}$$

*Доказательство:*

Ранее было показано что $c = 2\cos(\theta)$ алгебраическое целое число, более того для любого алгебраически сопряженного $\overline{c}$ выполнено $\|\overline{c}\| \le 2$.

Пусть $c$ принадлежит квадратичному полю $\mathbb{Q}(\sqrt{D})$. Рассмотрим 2 случая

1. $D \equiv 2,3 \pmod{4}$. 
   
Тогда $c = a + b \sqrt{D}$, для $a, b \in \mathbb{Z}$.  В этом случае $\|a + b\sqrt{D}\| \le 2$ и $\|a - b\sqrt{D}\| \le 2$. Без ограничения общности можно считать $a \ge 0$ и $b > 0$. Тогда

$$a + b\sqrt{D} \le 2$$

​Отсюда $a=0$, $b = 1$ и $D \in \\{2, 3\\}$.

2. $D \equiv 1 \pmod{4}$. 
   
Тогда $c = a + b \frac{1+\sqrt{D}}{2}$.  В этом случае $\|a + b \frac{1+\sqrt{D}}{2}\| \le 2$ и $\|a + b \frac{1-\sqrt{D}}{2}\| \le 2$. Аналогично без ограничения общности можно считать $a \ge 0$ и $b > 0$. Тогда

$$a + b \frac{1+\sqrt{D}}{2} \le 2$$

Отсюда $a=0$, $b=1$ и $D = 5$

Имеем 

$$2\cos(\theta) \in \left\{ \pm\sqrt{2},  \pm\sqrt{3},  
\pm\frac{1}{2} \pm \frac{\sqrt{5}}{2} \right\}$$

и 

$$\cos(\theta) \in \left\{ \pm\frac{\sqrt{2}}{2},  \pm\frac{\sqrt{3}}{2},  \pm\frac{1}{4} \pm \frac{\sqrt{5}}{4} \right\}$$

И соответственно

$$\theta \in \left\{\frac{\pi}{6}, \frac{\pi}{5}, \frac{\pi}{4},
\frac{2\pi}{5}, \frac{3\pi}{5}, \frac{3\pi}{4}, \frac{4\pi}{5}, \frac{5\pi}{6} \right\}$$

### Кубические иррациональности

**Теорема: **

Рассмотрим угол  $\theta$,  принадлежащее промежутку $0 \le \theta \le \pi$ и такой что $\frac{\theta}{\pi} \in \mathbb{Q}$.  Тогда  $\cos(\theta)$ принадлежит кубическому расширению поля $\mathbb{Q}$, только при 

$$\theta \in \left\{\frac{\pi}{7},\frac{2\pi}{7},\frac{3\pi}{7},\frac{4\pi}{7},\frac{5\pi}{7}, \frac{6\pi}{7} \right\}$$
​	
и

$$\theta \in \left\{\frac{\pi}{9},\frac{2\pi}{9},\frac{4\pi}{9},\frac{5\pi}{9},\frac{7\pi}{9}, \frac{8\pi}{9} \right\}$$


*Доказательство:*

Пусть $c_1$, $c_2$, $c_3$ — корни неприводимого кубического многочлена 
$$x^3 + ax^2+bx+c$$
степени с целыми коэффициентами такие, что $|c_i|\le 2$. Из соотношений 

$$a = -(c_1 + c_2 + c_3)$$

$$b = c_1c_2 + c_1c_3+c_2c_3$$

$$c = -c_1c_2c_3$$

Имеем 

$$|a| \le 6$$

$$|b| \le 12$$

$$|c| \le 8$$

Все такие многочлены можно перебрать используя систему компьютерной алгебры. Вычисления показывают что существует только 4 таких многочлена:

1. $x^3 - x^2 - 2x + 1$

Его корни:  $2\cos\left(\frac{\pi}{7}\right)$, $2\cos\left(\frac{3\pi}{7}\right)$, $2\cos\left(\frac{5\pi}{7}\right)$;

2. $x^3+x^2-2x-1$

Его корни: $2\cos\left(\frac{2\pi}{7}\right)$, $2\cos\left(\frac{4\pi}{7}\right)$, $2\cos\left(\frac{6\pi}{7}\right)$;

3. $x^3-3x+1$

Его корни: $2\cos\left(\frac{2\pi}{9}\right)$, $2\cos\left(\frac{4\pi}{9}\right)$, $2\cos\left(\frac{8\pi}{9}\right)$;

4. $x^3-3x-1$

Его корни: $2\cos\left(\frac{\pi}{9}\right)$, $2\cos\left(\frac{5\pi}{9}\right)$, $2\cos\left(\frac{7\pi}{9}\right)$;

### Общий случай

Справедлива следующая теорема:

**Теорема:**

Пусть $\theta = 2\pi\frac{m}{n}$, где $m,n$ — взаимно простые целые числа, тогда 

1.  $\cos(\theta)$ рациональное число тогда и только тогда, когда  $\varphi(n) \le 2$. Т. е. при $n \in \\{1,2,3, 4,6\\}$
2.  $\cos(\theta)$ алгебраическое целое число степени $d > 1$ тогда и только тогда, когда $\varphi(n)  = 2d$.

Где $\varphi(n)$ — Функция Эйлера.

*Доказательство:*

Из формулы Эйлера

$$\cos(\theta) = \frac{\zeta_n^m+\zeta_n^{-m}}{2},$$

где $\zeta_n$ —  примитивный корень степени $n$ из единиц. Получаем, что $\zeta_n^m$ является решением квадратного уравнения $X^2-2\cos(\theta)X+1=0$ над $\mathbb{Q}(\cos(\theta))$. Так как $n$ и $m$ взаимно просты, то $\mathbb{Q}(\zeta_n^m)$ = $\mathbb{Q}(\zeta_n)$, то $[\mathbb{Q}(\zeta_n): \mathbb{Q}(\cos(\theta))] = 1, 2.$

Поскольку $\mathbb{Q}(\cos(\theta)) \subset \mathbb{R}$, то случай $[\mathbb{Q}(\zeta_n): \mathbb{Q}(\cos(\theta))] = 1$ возможет только при $\zeta_n \in \mathbb{R}$ т.е при $n=1,2$.  В противном случае 

$$[\mathbb{Q}(\cos(\theta)): \mathbb{Q}] = \frac{\varphi([\mathbb{Q}(\zeta_n): \mathbb{Q}])}{2}=\frac{\varphi(n)}{2}$$

---
Источник

[**Jörg Jahnel**. When is the (co)sine of a rational angle equal to a rational number?](https://arxiv.org/abs/1006.2938)