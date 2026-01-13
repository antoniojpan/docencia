---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/examenes/ano-24-25-jun-mat-ii-gqui/","created":"2026-01-08T10:24:16.933+01:00","updated":"2025-09-13T17:06:11.747+02:00"}
---

#### EXAMEN MATEMÁTICAS II. GRADO EN QUÍMICA. 23 de junio de 2025
(Duración: 2h y 40 min)

1. Aproxima el valor de la integral
$$
I = \int_{0}^{60} \frac{e^{-x/20}}{10+x} \, dx,
$$
utilizando 3 subintervalos y usando las fórmulas compuestas del punto medio y de Simpson.
**(2.5 puntos)**

---
2. Resuelve el problema de valor inicial consistente en la ecuación diferencial
$$
(3x^2y + 2y^2)dx + (x^3 + 4xy + 6y)dy = 0
$$
con $y(0)=1$. **(2.5 puntos)**

---
3. Una bola de masa 1 kg se encuentra colgada de un muelle con constante $k = 2 \, \text{N/m}$. Todo el sistema se encuentra metido en miel, lo que propicia un coeficiente de rozamiento $\beta=4$. Inicialmente se estira la bola 10 m por debajo de su posición de equilibrio y se suelta de tal forma que la bola comienza a oscilar. Encontrar la ecuación de movimiento. **(2.5 puntos)**
---

4. Calcula la solución general del sistema $y' = Ay + b(t)$, donde
$$
A = \begin{pmatrix}
0 & 3 \\
3 & 0
\end{pmatrix}, \quad
b(t) = \begin{pmatrix}
1 \\
t
\end{pmatrix}.
$$
**(2.5 puntos)**

---

| **Método**              | **Fórmula**                                                                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Bisección**           | $\frac{b - a}{2^{n+1}} < \varepsilon$                                                                                                |
| **Regula Falsi**        | $c = b - \frac{b - a}{f(b) - f(a)} f(b)$                                                                                             |
| **Newton-Raphson**      | $x_{1} = x_0 - \frac{f(x_0)}{f'(x_0)}$                                                                                               |
| **Regla Punto Medio**   | $2h \sum_{i=1}^{n} f(x_{2i-1}),\quad h=\frac{b-a}{2n}$                                                                               |
| **Regla Trapecio**      | $\frac{h}{2} \left( f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{i}) + f(x_{n}) \right),\quad h=\frac{b-a}{n}$                                   |
| **Regla Simpson**       | $\frac{h}{3} \left[ f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{2i}) + 4 \sum_{i=1}^{n} f(x_{2i-1}) + f(x_{2n}) \right],\quad h=\frac{b-a}{2n}$ |
| **EDO1 lineales**       | $y(x) = e^{-\int P(x)dx} \left( \int Q(x)e^{\int P(x)dx}dx + C \right)$                                                              |
| **Sol part sistema NH** | $X_p(t) = \Phi(t) \int \Phi^{-1}(t) F(t) \, dt$                                                                                      |

---
[[04 MatII-Qui/Exámenes/Soluciones 24-25 jun Mat II-GQUI\|Soluciones 24-25 jun Mat II-GQUI]] 