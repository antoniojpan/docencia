---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/examenes/ano-24-25-sept-r-mat-ii-gqui/","updated":"2026-01-13T12:02:02.028+01:00"}
---

#### EXAMEN MATEMÁTICAS II. GRADO EN QUÍMICA. 15 de septiembre de 2025
(Duración: 2h )

**1. a) Se considera la función $f(x) = \ln(x+2)$.** Utilizar el método de interpolación de Newton para aproximar la función mediante un polinomio, usando los puntos $(-1, f(-1)), (0, f(0))$ y $(1, f(1))$.
   **b) Buscando raíces cúbicas.** Se quiere encontrar una solución para la ecuación $x^3 = 5$. Usa el método de Newton-Raphson para encontrar una aproximación de dicha solución. Comienza con el valor inicial $x_0=2$ y realiza tres iteraciones.
**(2.5 puntos)**

**2. Datación por Carbono-14.** El isótopo de Carbono-14 ($^{14}C$) decae exponencialmente con un periodo de semidesintegración (el tiempo que tarda en reducirse a la mitad) de 5730 años. Se encuentra un resto fósil de un organismo que en vida habría tenido 10 gramos de $^{14}C$, y se mide que la cantidad actual es de solo 3 gramos. Plantea y resuelve la ecuación diferencial del decaimiento radiactivo para determinar la edad aproximada del fósil.
**(2.5 puntos)**

**3**. Resolver, mediante el método de los coeficientes indeterminados, el problema de valor inicial (PVI):
$$
\begin{cases}
y'' + 9y = \cos(3x),\\
y(0)=1,\\
y'(0)=0.
\end{cases}
$$
**(2.5 puntos)**

**4**. Resolver el siguiente sistema de ecuaciones diferenciales con las condiciones iniciales dadas:
$$
\begin{cases}
\dfrac{dx}{dt} = y,\\[6pt]
\dfrac{dy}{dt} = -2x + 3y,
\end{cases}
\qquad
x(0)=0,\;\; y(0)=2.
$$
**(2.5 puntos)**

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

[[04 MatII-Qui/Exámenes/Soluciones 24-25 sept R Mat II-GQUI\|Soluciones 24-25 sept R Mat II-GQUI]] 