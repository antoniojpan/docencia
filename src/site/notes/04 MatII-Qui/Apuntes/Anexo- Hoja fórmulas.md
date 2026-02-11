---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/anexo-hoja-formulas/","created":"2026-01-08T10:24:16.932+01:00","updated":"2026-02-11T13:06:19.434+01:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Hoja Fórmulas

| **Método**                          | **Fórmula**                                                                                                                          | **Error**                                                           |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| **Bisección** (Criterio de paro)    | $x_n=\dfrac{a_n+b_n}{2}$; $\frac{b - a}{2^{n+1}} < \varepsilon$                                                                      | —                                                                   |
| **Regula Falsi** (Iteración)        | $x_n = b_n - \dfrac{b_n - a_n}{f(b_n) - f(a_n)} f(b_n)$                                                                              | —                                                                   |
| **Newton-Raphson** (Iteración)      | $x_{1} = x_0 - \dfrac{f(x_0)}{f'(x_0)}$                                                                                              | —                                                                   |
| **Regla Punto Medio**               | $2h \sum_{i=1}^{n} f(x_{2i-1}),\quad h=\dfrac{b-a}{2n}$                                                                              | $E_{Pm}(f)\leq \frac{(b - a)^3}{24n^2} \max_{x \in [a, b]}f''(x)$   |
| **Regla Compuesta Trapecio**        | $\frac{h}{2} \left( f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{i}) + f(x_{n}) \right),\quad h=\frac{b-a}{n}$                                   | $E_{Tr}(f)\leq \frac{(b - a)^3}{12n^2} \max_{x \in [a, b]}f''(x)$   |
| **Regla Compuesta Simpson**         | $\frac{h}{3} \left[ f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{2i}) + 4 \sum_{i=1}^{n} f(x_{2i-1}) + f(x_{2n}) \right],\quad h=\frac{b-a}{2n}$ | $E_S(f)\leq \frac{(b - a)^5}{2880n^4} \max_{x \in [a, b]}f^{iv}(x)$ |
| **EDO1 lineales**                   | $y(x) = e^{-\int P(x)dx} \left( \int Q(x)e^{\int P(x)dx}dx + C \right)$                                                              | —                                                                   |
| **Sol particular sistema no homog** | $X_p(t) = \Phi(t) \int \Phi^{-1}(t) F(t) \, dt$                                                                                      | —                                                                   |



