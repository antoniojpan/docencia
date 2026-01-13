---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/examenes/ano-23-24-mat-ii-gqui/","updated":"2025-06-05T09:26:52.329+02:00"}
---

#### EXAMEN MATEMÁTICAS II. GRADO EN QUÍMICA . 3 DE FEBRERO DE 2024

1. Aproxima el valor de la integral
$$
I = \int_{1}^{2} \frac{\sin(x)}{x^4} \, dx,
$$
utilizando cinco nodos y usando las fórmulas compuestas del trapecio y del punto medio.
**(2.5 puntos)**

---
2. Un magnate posee una fortuna que crece a un ritmo que es proporcional al cuadrado de su valor en cada momento. Si tenía 10 millones de dólares hace un año y hoy tiene 20 millones, calcula cuánto será la fortuna dentro de 6 meses. **(2.5 puntos)**

---
3. Una bola de masa 1 kg se encuentra apoyada en una mesa y a su vez sujeta a una pared mediante un muelle de constante $k = 2 \, \text{N/m}$. Inicialmente se estira la bola 1 cm de su posición de equilibrio y se suelta de tal forma que la bola comienza a oscilar, siendo la fuerza de rozamiento con la mesa 2 veces la velocidad instantánea. Encontrar y resolver la ecuación de movimiento. **(2.5 puntos)**
---

4. Calcula la solución general del sistema $y' = Ay + b(t)$, donde
$$
A = \begin{pmatrix}
1 & 2 \\
3 & 2
\end{pmatrix}, \quad
b(t) = \begin{pmatrix}
t - 1 \\
-5t - 2
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

