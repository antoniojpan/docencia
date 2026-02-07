---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema02-ej/","created":"2026-02-07T13:01:41.827+01:00","updated":"2026-02-07T13:02:01.632+01:00"}
---

# Hoja de Ejercicios: Resolución Numérica de Ecuaciones

## Ejercicio 1
**Enunciado:** Demostrar que la ecuación $x^{4}-4x-1=0$ tiene exactamente dos soluciones reales y dar un intervalo al que pertenezcan cada una de ellas.

**Solución:**
Consideramos la función $f(x)=x^{4}-4x-1$, que es continua y derivable. Buscamos sus puntos críticos:
$$f^{\prime}(x)=4x^{3}-4=0 \Rightarrow x=1$$
Evaluamos la función en el punto crítico: $f(1)=-4 < 0$. 
Analizamos los límites y puntos de prueba para determinar cambios de signo:
* $\lim_{x\rightarrow-\infty}f(x)=+\infty$. Punto de prueba: $f(-1)=4 > 0$.
* $\lim_{x\rightarrow+\infty}f(x)=+\infty$. Punto de prueba: $f(2)=7 > 0$.

**Conclusión:** Existen cambios de signo en los intervalos $[-1,1]$ y $[1,2]$, por lo que existen solo dos soluciones reales, una en cada intervalo.

---

## Ejercicio 2
**Enunciado:** Demostrar que la ecuación $x^{4}+x^{3}+x^{2}-2=0$ tiene exactamente dos soluciones reales y dar un intervalo al que pertenezcan cada una de ellas.

**Solución:**
Sea $f(x)=x^{4}+x^{3}+x^{2}-2$. Puntos críticos:
$$f^{\prime}(x)=4x^{3}+3x^{2}+2x=x(4x^{2}+3x+2)=0 \Rightarrow x=0$$
Evaluamos en el punto crítico: $f(0)=-2 < 0$. 
Límites y puntos de prueba:
* $\lim_{x\rightarrow-\infty}f(x)=+\infty$. Punto de prueba: $f(-2)=10 > 0$.
* $\lim_{x\rightarrow+\infty}f(x)=+\infty$. Punto de prueba: $f(1)=1 > 0$.

**Conclusión:** Hay dos intervalos con cambios de signo: $[-2,0]$ y $[0, 1]$. Existen solo dos soluciones reales.

---

## Ejercicio 3
**Enunciado:** Demostrar que la ecuación $x^{3}-5x^{2}+3x+2=0$ tiene exactamente tres soluciones reales y dar un intervalo al que pertenezcan cada una de ellas.

**Solución:**
Sea $f(x)=x^{3}-5x^{2}+3x+2$. Puntos críticos:
$$f^{\prime}(x)=3x^{2}-10x+3=0 \Rightarrow x_{1}=\frac{1}{3}, x_{2}=3$$
Evaluamos la función en los críticos: $f(\frac{1}{3})=\frac{67}{27} > 0$ y $f(3)=-7 < 0$. 
Límites y puntos de prueba:
* $\lim_{x\rightarrow-\infty}f(x)=-\infty$. Punto de prueba: $f(-1)=-7 < 0$.
* $\lim_{x\rightarrow+\infty}f(x)=+\infty$. Punto de prueba: $f(5)=17 > 0$.

**Conclusión:** Tres intervalos con cambio de signo: $[-1, 1/3]$, $[1/3, 3]$ y $[3, 5]$. Existen tres soluciones reales.

---

## Ejercicio 4
**Enunciado:** Demostrar que las curvas $y=e^{x-2}$ e $y=-x^{2}+4$ se cortan exactamente en dos puntos y dar un intervalo al que pertenezcan cada uno de ellos.

**Solución:**
Definimos $h(x)=e^{x-2} - (-x^{2}+4)$. 
Puntos críticos: $h^{\prime}(x)=e^{x-2}+2x=0 \Rightarrow x \approx -0.063$. 
Evaluamos: $h(-0.063)=-3.868 < 0$. 
Límites y puntos de prueba:
* $\lim_{x\rightarrow-\infty}h(x)=+\infty$. Punto de prueba: $h(-3)=5.006 > 0$.
* $\lim_{x\rightarrow+\infty}h(x)=+\infty$. Punto de prueba: $h(3)=7.718 > 0$.

**Conclusión:** Intervalos con cambio de signo: $[-3, -0.063]$ y $[-0.063, 3]$. Existen dos puntos de corte.

---

## Ejercicio 5
**Enunciado:** ¿En cuántos puntos se intersecan las curvas $y=\ln x$ e $y=\frac{1}{9}x^{2}$?

**Solución:**
Sea $h(x)=\ln x - \frac{1}{9}x^{2}$, definida para $x>0$. 
Puntos críticos: $h^{\prime}(x)=\frac{1}{x}-\frac{2}{9}x=0 \Rightarrow x=\frac{3}{\sqrt{2}} \approx 2.12$. 
Evaluamos: $h(\frac{3}{\sqrt{2}})=0.252 > 0$. 
Límites y puntos de prueba:
* $\lim_{x\rightarrow 0^+}h(x)=-\infty$. Punto de prueba: $h(1)=-0.111 < 0$.
* $\lim_{x\rightarrow+\infty}h(x)=-\infty$. Punto de prueba: $h(4)=-0.391 < 0$.

**Conclusión:** Existen dos intervalos con cambio de signo: $[1, 2.12]$ y $[2.12, 4]$. Existen dos puntos de corte.

---

## Ejercicio 6
**Enunciado:** ¿En cuántos puntos se intersecan las curvas $y=e^{x}$ e $y=3x^{2}$?

**Solución:**
Sea $h(x)=e^{x}-3x^{2}$. Puntos críticos: $x_{1}=0.204$, $x_{2}=2.833$. 
Evaluamos: $h(0.204)=1.101 > 0$ y $h(2.833)=-7.081 < 0$. 
Límites y puntos de prueba:
* $\lim_{x\rightarrow-\infty}h(x)=-\infty$. Punto de prueba: $h(-1)=-2.632 < 0$.
* $\lim_{x\rightarrow+\infty}h(x)=+\infty$. Punto de prueba: $h(4)=6.598 > 0$.

**Conclusión:** Tres intervalos con cambio de signo: $[-1, 0.204]$, $[0.204, 2.833]$ y $[2.833, 4]$. Existen tres puntos de corte.

---

## Ejercicio 7
**Enunciado:** Demostrar que $1-x=\tan x$ tiene una única solución en $[-\frac{\pi}{4},\frac{\pi}{4}]$. Aproximar con Bisección y Newton.

**Solución:**
* **Existencia y Unicidad:** $f(x)=1-x-\tan x$. $f(-\frac{\pi}{4}) \approx 2.785 > 0$, $f(\frac{\pi}{4}) \approx -0.785 < 0$. La derivada $f^{\prime}(x)=-2-\tan^{2}x$ es siempre negativa, por lo que la función es monótona decreciente y la raíz es única.
* **Bisección (3 aprox.):** $c_{0}=0$; $c_{1}=\frac{\pi}{8}$; $c_{2}=\frac{3\pi}{16}$. Solución aprox: $0.589$.
* **Newton ($x_0=0$):** $x_{1}=0.5$; $x_{2}=0.479$; $x_{3}=0.479$.

---

## Ejercicio 8
**Enunciado:** Dada la ecuación $\cos x-x=0$, probar unicidad en $[0, \frac{\pi}{2}]$ y aproximar con Bisección y Newton.

**Solución:**
* **Existencia y Unicidad:** $f(0)=1 > 0$, $f(\frac{\pi}{2}) \approx -1.57 < 0$. $f^{\prime}(x)=-\sin x-1$, no se anula en el intervalo. Solución única.
* **Bisección:** Solución aprox $c_3 \approx 0.687$. Para error $< 10^{-3}$, se requieren 10 iteraciones.
* **Newton ($x_0=\frac{\pi}{4}$):** $x_1 = 0.7395$; $x_2 = 0.7390$; $x_3 = 0.7390$.

---

## Ejercicio 9
**Enunciado:** Dada $2x-e^{-x}=0$, probar unicidad en $[0,1]$ y aproximar con Bisección y Newton.

**Solución:**
* **Existencia y Unicidad:** $f(0)=-1 < 0$, $f(1) \approx 1.632 > 0$. $f^{\prime}(x)=2+e^{-x} > 0$. Solución única.
* **Bisección:** Solución aprox $c_3 = 0.312$. Para error $< 10^{-2}$ se requieren 6 iteraciones.
* **Newton ($x_0=0.5$):** $x_1 = 0.349$; $x_2 = 0.351$.

---

## Ejercicio 10
**Enunciado:** ¿Es aplicable el método de Bisección a $f(x)=\frac{1}{x-2}-\frac{1}{2}$ en $[3,7]$ y en $[1,7]$?

**Solución:**
* **En $[3,7]$:** SÍ. $f$ es continua en el intervalo, $f(3)=1/2 > 0$ y $f(7)=-3/10 < 0$.
* **En $[1,7]$:** NO. La función presenta una discontinuidad en $x=2$.
* **Raíz en $[3,7]$:** $c_0=5, f(5)<0 \Rightarrow [3,5]$. $c_1=4, f(4)=0$. La raíz exacta es $x=4$.

---

## Ejercicio 11
**Enunciado:** Estudia la unicidad de $f(x)=2x-3e^{-x}$ en $[0,1]$ y realiza dos iteraciones de Newton.

**Solución:**
* **Unicidad:** $f(0)=-3$, $f(1) \approx 0.896$. $f^{\prime}(x)=2+3e^{-x} > 0$. Solución única.
* **Newton ($x_0=0.5$):** $x_1 = 0.714$; $x_2 = 0.725$.

---

## Ejercicio 12
**Enunciado:** Aproximar la solución de $x^{3}-x+1=0$ en $[-2,0]$ con Regula Falsi y Newton.

**Solución:**
* **Regula Falsi:** $c_0=-0.333$; $c_1=-0.676$; $c_2 = -0.960$.
* **Newton ($x_0 = -1$):** $x_1 = -1.5$; $x_2 = -1.347$.

---

## Ejercicio 13
**Enunciado:** Aplicar Regula Falsi en $[0,1]$ a $e^{-x}-x=0$ hasta que $|c_{n}-c_{n-1}|\le 0.005$.

**Solución:**
* $c_0=0.612$.
* $c_1=0.572$ ($|c_1 - c_0| = 0.04$).
* $c_2 = 0.568$ ($|c_2 - c_1| = 0.004 < 0.005$).
**Aproximación final:** $0.567$.

---

## Ejercicio 14
**Enunciado:** Realizar dos iteraciones de Regula Falsi para $(x-1)e^{-x}=0$ en $[0,3]$.

**Solución:**
* $c_0=2.728$.
* $c_1=2.451$.
* $c_2 = 2.205$.

---

## Ejercicio 15
**Enunciado:** Realizar dos iteraciones de Regula Falsi para $x\cos x-e^{x}+1=0$ en $[-1, -0.2]$.

**Solución:**
* $c_0=-0.310$.
* $c_1=-0.475$.
* $c_2 = -0.645$.

---

## Ejercicio 16
**Enunciado:** Sea $f(x)=x^{3}-3x+2$. Demostrar unicidad en $[-3,-1.5]$ y calcular aproximación con Regula Falsi.

**Solución:**
* **Unicidad:** $f(-3)=-16$, $f(-1.5)=3.125$. $f^{\prime}(x)=3x^{2}-3$ tiene raíces en $\pm 1$, fuera del intervalo. Solución única.
* **Regula Falsi:** $c_0 = -1.74$; $c_1 = -1.87$; $c_2 = -1.94$.
**Aproximación final:** $c_3 = -1.975$.

---

## Ejercicio 17
**Enunciado:** Demostrar que $\frac{1}{x}-e^{x}=0$ tiene solución única en $[0.1, 2.1]$ y aproximar con Bisección.

**Solución:**
* **Unicidad:** $f(0.1)=8.894$, $f(2.1)=-7.689$. $f^{\prime}(x)=-\frac{1}{x^{2}}-e^{x} < 0$. Solución única.
* **Bisección (3 iteraciones):** $c_0 = 1.1$; $c_1 = 0.6$; $c_2 = 0.35$.
**Aproximación final:** $c_3 = 0.475$.