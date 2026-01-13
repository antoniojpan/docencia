---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/examenes/ano-24-25-jun-r-mat-ii-gqui/","updated":"2026-01-13T12:01:28.719+01:00"}
---

#### EXAMEN MATEMÁTICAS II. GRADO EN QUÍMICA. 27 de junio de 2025
(Duración: 1h y 20 min)

1. Aproxima el valor de la integral
$$
I = \int_{-30}^{30} \frac{e^{-x/2}}{1+x} \, dx,
$$
utilizando 3 subintervalos con la fórmula de Simpson.
**(2.5 puntos)**

---
2. Resuelve el siguiente PVI de primer orden:
$$
\begin{cases}
y' = 2y + xe^{3x} \\
y(0) = 2
\end{cases}
$$
**(2.5 puntos)**
---
3. La tasa de crecimiento de una población de bacterias es proporcional a la cantidad de bacterias presentes. Se empieza un cultivo con 14 millones de bacterias, y se ha comprobado que a los tres días hay 30 millones de bacterias. Halla el modelo para la evolución de esta población de bacterias con el tiempo.
**(2.5 puntos)**
---

4. Calcula la solución general del sistema $y' = Ay$, donde
$$
A = \begin{pmatrix}
1 & 3 \\
3 & 0
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
