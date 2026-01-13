---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/examenes/ano-24-25-sept-mat-ii-gqui/","created":"2026-01-08T10:24:16.933+01:00","updated":"2026-01-13T12:01:50.862+01:00"}
---

#### EXAMEN MATEMÁTICAS II. GRADO EN QUÍMICA. 11 de septiembre de 2025
(Duración: 2h )

1. a) Se considera la función $f(x) = 5^x$. Utilizar el método de interpolación de Newton para aproximar la función mediante un polinomio, usando los puntos $(−1, f (−1)), (0, f (0))$ y $(1, f (1))$.
   b) Matando moscas a cañonazos. Todo el mundo sabe que la ecuación $x^2=2$ tiene dos soluciones, una de ellas $x=\sqrt{2}$. Usa el método de Newton-Raphson para encontrar, de manera aproximada esa solución. Empieza con la aproximación $x_0=5$, y usa tres iteraciones.
**(2.5 puntos)**

2. Antes del mediodía, el cuerpo de una víctima de homicidio se encuentra en un cuarto que se conserva a temperatura constante de 21º. Al mediodía, la temperatura del cuerpo es de 26º y una hora más tarde es de 24º. Si se considera que la temperatura de un cuerpo en condiciones normales es de 37º. ¿Cuál fue la hora de la muerte?
**(2.5 puntos)**

3. Resolver, mediante el método de los coeficientes indeterminados, el PVI
$$
\begin{cases}
y'' + y' - 2y = 5e^x,\\
y(0)=0,\\
y'(0)=0.
\end{cases}
$$
**(2.5 puntos)**

4. Resolver el siguiente sistema de ecuaciones diferenciales con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 5x + 2y,\\[6pt]
\dfrac{dy}{dt} = -2x + y,
\end{cases}
\qquad
x(0)=1,\;\; y(0)=1.
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
[[04 MatII-Qui/Exámenes/Soluciones 24-25 sept Mat II-GQUI\|Soluciones 24-25 sept Mat II-GQUI]]  