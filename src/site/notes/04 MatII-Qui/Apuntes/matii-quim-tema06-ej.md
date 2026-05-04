---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema06-ej/","created":"2026-04-28T16:54:25.785+02:00","updated":"2026-05-04T13:11:12.849+02:00"}
---

# Ejercicios tema 6

1. Estudiar la existencia y unicidad de los siguientes PVI:

(a) $\begin{cases} y'' = x^3 y' - \frac{1}{x} y \\ y(1) = 0 \\ y'(1) = -1 \end{cases}$

(b) $\begin{cases} y'' = \ln(x) y' + \sqrt{x} y \\ y(1) = 0 \\ y'(1) = 2 \end{cases}$

(c) $\begin{cases} x y'' - \operatorname{sen}(x) y' = e^x y \\ y(0) = 1 \\ y'(0) = 0 \end{cases}$

(d) $\begin{cases} x^2 y'' + x y' + y = 0 \\ y(0) = 1 \\ y'(0) = -1 \end{cases}$


---

2. Determinar si los siguientes conjuntos pueden formar o no un sistema fundamental de soluciones:

(a) $\{1, x, 3x\}$

(b) $\{e^x, e^{-x}, 1\}$

(c) $\{\operatorname{sen} x, \cos x, 2 \cos x\}$

(d) $\{e^x, x e^x\}$

3. Obtener la solución general de la ecuación diferencial dada:  

**(a)** $3y'' - y' = 0$  
**(b)** $2y'' + 5y' = 0$  
**(c)** $\frac{d^2y}{dx^2} + 8\frac{dy}{dx} + 16y = 0$  
**(d)** $y'' + 3y' - 4y = 0$  
**(e)** $y'' + y' + y = 0$  
**(f)** $y'' + y = 0$  

---

4. Resolver los problemas de valores iniciales:  

**(a)**  
$$
\begin{cases} 
y'' + 16y = 0 \\ 
y(0) = 2, & y'(0) = -2 
\end{cases}
$$  

**(b)**  
$$
\begin{cases} 
y'' - 4y' - 5y = 0 \\ 
y(1) = 0, & y'(1) = 2 
\end{cases}
$$  

---

5. Resolver el problema de valores iniciales:

$$\begin{cases} y^{iv)} - 2y''' - y'' + 2y' = 0 \\ y(0) = 0, \quad y'(0) = 1, \quad y''(0) = -1, \quad y'''(0) = 7 \end{cases}$$

---

6. Determinar una ecuación diferencial lineal con coeficientes constantes homogénea que tenga las soluciones indicadas y escribir la solución general de la ecuación.

(a) $\{e^{6x}, e^{-3x}\}$

(b) $\{1, x\}$

(c) $\{\operatorname{sen} x, \cos x\}$

---

7. Indicar, según la forma del término no homogéneo de la ecuación diferencial, la forma de la solución particular de la ecuación para el método de los coeficientes indeterminados (sin resolver la ecuación):  

**(a)** Para $y'' - 4y' + 3y = f(x)$ donde $f(x)$ es:  
- **i.** $f(x) = e^{2x}$  
- **ii.** $f(x) = e^x$  

**(b)** Para $3y'' - y' = f(x)$ donde $f(x)$ es:  
- **i.** $f(x) = 1$  
- **ii.** $f(x) = 5e^{\frac{x}{3}}$  
- **iii.** $f(x) = x^2 + 1$  
- **iv.** $f(x) = \cos(2x)$  

**(c)** Para $y'' + 8y' + 16y = f(x)$ donde $f(x)$ es:  
- **i.** $f(x) = e^{-4x}$  
- **ii.** $f(x) = 3e^x$  
- **iii.** $f(x) = 3$  
- **iv.** $f(x) = x$  

**(d)** Para $y'' + y' + y = f(x)$ donde $f(x)$ es:  
- **i.** $f(x) = \cos\left(\frac{\sqrt{3}}{2}x\right)$  
- **ii.** $f(x) = \text{sen}\,x$  
- **iii.** $f(x) = x$  


EJEMPLO: 

La solución general de la ecuación
$$
y'' + y' + y = \cos\!\Bigl(\tfrac{\sqrt3}{2}x\Bigr)
$$
se obtiene como suma de la solución de la homogénea y de una solución particular.

La ecuación homogénea asociada es
$$
y'' + y' + y = 0,
$$
con ecuación característica
$$
r^2 + r + 1 = 0
\;\;\Longrightarrow\;\;
r = \frac{-1\pm i\sqrt3}{2}.
$$
Por tanto
$$
y_{\mathrm{c}}(x)
= e^{-x/2}\Bigl(C_1\cos\!\tfrac{\sqrt3}{2}x + C_2\sin\!\tfrac{\sqrt3}{2}x\Bigr).
$$

Buscamos
$$
y_{\mathrm{p}}(x)
= A\cos\!\Bigl(\tfrac{\sqrt3}{2}x\Bigr) + B\sin\!\Bigl(\tfrac{\sqrt3}{2}x\Bigr).
$$
Calculemos sus derivadas (llamamos $\omega=\frac{\sqrt{3}}{2}$):
$$
\begin{cases}
y_{\mathrm{p}}' = -A\,\omega\,\sin(\omega x) + B\,\omega\,\cos(\omega x),\\
y_{\mathrm{p}}''= -A\,\omega^2\,\cos(\omega x) - B\,\omega^2\,\sin(\omega x).
\end{cases}
$$
Sustituyendo en la ecuación:

$$
y_{\mathrm{p}}'' + y_{\mathrm{p}}' + y_{\mathrm{p}}
= \bigl(-A\omega^2 + B\omega + A\bigr)\cos(\omega x)
+ \bigl(-B\omega^2 - A\omega + B\bigr)\sin(\omega x)
\;\stackrel!=\;\cos(\omega x).
$$
Igualamos coeficientes:
$$
\begin{cases}
-A\omega^2 + B\omega + A = 1,\\
-B\omega^2 - A\omega + B = 0.
\end{cases}
$$
Con $\omega^2=3/4$, estas ecuaciones son
$$
\begin{cases}
\frac14\,A + \frac{\sqrt3}{2}\,B = 1,\\
-\frac{\sqrt3}{2}\,A + \frac14\,B = 0.
\end{cases}
$$

Resolviendo:
$$
A = \frac{4}{13}, 
\qquad
B = \frac{8\sqrt3}{13}.
$$
Por tanto
$$
y_{\mathrm{p}}(x)
= \frac{4}{13}\,\cos\!\Bigl(\tfrac{\sqrt3}{2}x\Bigr)
+ \frac{8\sqrt3}{13}\,\sin\!\Bigl(\tfrac{\sqrt3}{2}x\Bigr).
$$
Combinando homogénea y particular:
$$
\boxed{
y(x) 
= e^{-x/2}\Bigl(C_1\cos\!\tfrac{\sqrt3}{2}x + C_2\sin\!\tfrac{\sqrt3}{2}x\Bigr)
+ \frac{4}{13}\,\cos\!\tfrac{\sqrt3}{2}x
+ \frac{8\sqrt3}{13}\,\sin\!\tfrac{\sqrt3}{2}x,
}
$$
donde $C_1,C_2$ son constantes arbitrarias.


---

8. Resolver, mediante el método de los coeficientes indeterminados, la ecuación  
$$
y'' + y' - 2y = r(x),
$$  

donde $r(x)$ es:  

**(a)** $r(x) = x^2 + x$  
**(b)** $r(x) = 5e^{-2x}$  
**(c)** $r(x) = -3e^x$  
**(d)** $r(x) = 4\cos x$  

---
9. Resolver la ecuación diferencial dada, mediante variación de constantes:
(a) $y'' + y = \operatorname{sen}^2 x$

(b) $y'' - y = x e^x$

---

10. Una masa que pesa un kilo se suspende de un resorte cuya constante es de 4 kg/m. El amortiguamiento del sistema se supone despreciable. Se aplica una fuerza externa $F(t) = 1 - 2\cos^2 t$. Determinar la ecuación del movimiento si la masa se libera al inicio con una velocidad de 2 m/s hacia arriba y en un punto que está a 4 metros por debajo de la posición de equilibrio.  

---

11. Una masa que pesa 4 kg se suspende de un resorte cuya constante es de 3 kg/m. Todo el sistema se sumerge en un líquido que ofrece una fuerza de amortiguamiento numérico igual a la velocidad instantánea. Se aplica una fuerza externa $F(t) = e^{-t}$. Determinar la ecuación del movimiento si la masa se libera al inicio desde el reposo en un punto que está a 2 metros bajo la posición de equilibrio.  

---

12. Una masa que pesa 24 kg, unida al extremo de un resorte, alarga a ésta 4 m. Al inicio, la masa se libera desde el reposo en un punto a 3 m hacia arriba de la posición de equilibrio. Encontrar la ecuación del movimiento. Además, encontrar la ecuación del movimiento si la masa anterior se libera desde la posición de equilibrio con una velocidad descendente de 2 m/s.  

