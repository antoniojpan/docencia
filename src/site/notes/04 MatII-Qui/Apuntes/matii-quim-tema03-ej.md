---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema03-ej/","created":"2026-03-02T13:54:05.252+01:00","updated":"2026-03-02T14:01:56.527+01:00"}
---

# Tema 3: Interpolación y aproximación de funciones
**Matemáticas II - Grado en Química** **UCA Universidad - Curso 2021-2022**

---


1. En una estación de metro pasan convoys cada 10 minutos durante las primeras horas de la mañana. A las 8 de la mañana suben al convoy 30 personas, 26 a las 8 y media y 21 a las 9. Estima (usando el polinomio de interpolación de Newton) cuántas personas suben a las $8:20$.

2. Se considera la función $f(x)=5^{x}$.
    * (a) Utilizar el método de diferencias divididas de Newton para calcular el polinomio de interpolación de los puntos $(-1, f(-1))$, $(0, f(0))$ y $(1, f(1))$.
    

3. Se consideran los puntos $Q_{1}=(2,3)$, $Q_{2}=(4,-1)$, $Q_{3}=(6,4)$, $Q_{4}=(8,0)$ y $Q_{5}=(10,-1)$.
    * (a) Calcular el polinomio de interpolación de los puntos $Q_{1}$, $Q_{2}$, $Q_{3}$, $Q_{4}$ usando las diferencias divididas de Newton.
    * (b) Utilizar las diferencias divididas del apartado anterior para calcular el polinomio de interpolación de los puntos $Q_{1}$, $Q_{2}$, $Q_{3}$, $Q_{4}$, $Q_{5}$.

4. Consideremos la función $f(x)=e^{\operatorname{sen} x}$.

    * (b) Utilizar el método de las diferencias divididas de Newton para calcular su polinomio de interpolación en los mismos puntos.
    * (c) Calcular el error cometido al considerar el valor $p(1.5)$ como aproximación de $f(1.5)$ en ambos casos.

5. Se considera la función $f(x)=\ln(1+x)$.
    * (a) Calcular el polinomio de interpolación de Hermite en los puntos $x_{1}=0$, $x_{2}=1$, $x_{3}=2$.
    * (b) Dar una aproximación de $\ln(2.5)$.

6. Consideremos la función $f(x)=\frac{x}{1+x^{2}}$.
    * 
    * (b) Utilizar el método de las diferencias divididas de Newton para calcular su polinomio de interpolación en los mismos puntos.
    * (c) Aproximar $f(1.5)$ haciendo uso de ambos polinomios.

7. Sea $f(x)=\operatorname{sen} x$.
    * (a) Utilizar el método de las diferencias divididas de Newton para calcular su polinomio de interpolación en $x_{0}=0$, $x_{1}=\frac{\pi}{6}$, $x_{2}=\frac{\pi}{3}$ y $x_{3}=\frac{\pi}{2}$.
    * (b) Utilizar el polinomio de interpolación de Hermite en los puntos $x_{0}$ y $x_{2}$.


8. Sea $f(x)=\cos x$.
    * (a) Calcular el polinomio de interpolación con diferencias divididas en los puntos $0$, $\frac{\pi}{2}$ y $\pi$.
    * (b) Calcular el polinomio de interpolación de Hermite en los mismos puntos que antes.
    * (c) Obtener la aproximación del valor $\cos(\frac{\pi}{4})$ usando los polinomios anteriores.

9. Dada la función $f(x)=2^{1/x}$.
    * (a) Hallar el polinomio de interpolación de $f(x)$ sobre el conjunto de puntos $x_{0}=0.5$, $x_{1}=1$, $x_{2}=1.5$, $x_{3}=2$ y $x_{4}=2.5$, mediante el método de las diferencias divididas de Newton.
    * (b) Usar dicho polinomio para calcular un valor aproximado de $\sqrt{2}$. Hallar una estimación del error cometido.

10. Utilizar el método de Hermite para hallar un polinomio $P(x)$ que satisfaga $P(-1)=-1$, $P'(-1)=14$, $P(2)=4$ y $P'(2)=5$.

11. Calcular $f(\frac{1}{8})$ a partir de una aproximación de la función $f(x)=\operatorname{tg}(\pi x)$ con el polinomio de interpolación de Hermite en los puntos $0$ y $\frac{1}{4}$.

12. Calcular el polinomio de Hermite que interpola la siguiente tabla:

| $x$ | $y$ | $y'$ |
| :-- | :-- | :--- |
| 1   | 5   | 12   |
| 0   | 2   | -7   |
| 2   | 51  | 40   |