---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema04-ej/","created":"2026-10-05T13:34:11.530+02:00","updated":"2026-10-05T13:34:09.000+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 4: Cálculo Diferencial en una Variable

> [!question] Ejercicio 1
> Calcula las derivadas de las siguientes funciones, simplificando cuando sea posible:
>
> **(a)** $f(x) = 0$
>
> **(b)** $f(x) = 5 \cdot 4242 - \pi e + 7x$
>
> **(c)** $f(x) = x^4 - 4x + 3\sqrt{x}$
>
> **(d)** $f(x) = x^3 - 2x + \cos x$
>
> **(e)** $f(x) = \frac{x^2 - x + 1}{x}$
>
> **(f)** $f(x) = \operatorname{sen} 3x$
>
> **(g)** $f(x) = \operatorname{sen} x^3$
>
> **(h)** $f(x) = \operatorname{sen}^3 x$
>
> **(i)** $f(x) = 2\operatorname{sen} x \cos x$
>
> **(j)** $f(x) = \cos^2 3x + \operatorname{sen}^2 3x$
>
> **(k)** $f(x) = \frac{\operatorname{sen} x^2}{\cos x^2}$
>
> **(l)** $f(x) = \frac{\operatorname{sen}^2 x}{\cos^2 x}$
>
> **(m)** $f(x) = \frac{\operatorname{sen} x}{1 + \cos x}$
>
> **(n)** $x(t) = \frac{t^3 - 3t}{t^4}$
>
> **(ñ)** $f(x) = -10 \tan(\ln(2 - x))$
>
> **(o)** $x(t) = \ln \sqrt{\frac{t^2}{4 + t + t^3}}$
>
> **(p)** $f(x) = 2x \arctan(x) - \ln(1 + x^2)$
>
> **(q)** $f(x) = 7^{x^2 - 3x}$
>
> **(r)** $f(x) = e^{\ln(x^5 - 7x)}$$
>
> **(s)** $f(x) = \ln(e^{x^3 - 3x + x^2 - 1})$
>
> **(t)** $f(x) = e^{\cos x}$
>
> **(u)** $f(x) = e^{7 - \ln(\operatorname{sen} x^3)}$
>
> **(v)** $f(x) = (\tan x)^{\ln x}$
>
> **(w)** $f(x) = \tan(x \ln x)$
>
> **(x)** $f(x) = x^{\tan x}$
>
> **(y)** $f(x) = x^{x^{2 - 2x}}$
>
> **($\alpha$)** $f(x) = \log_{10} x$
>
> **($\beta$)** $f(x) = \log_4 (x \operatorname{sen} x)$
>
> **($\gamma$)** $f(x) = \log_{10} (x^3 - x)$

> [!question] Ejercicio 2
> Para las funciones que siguen calcula el máximo, el mínimo y una acotación, todo ello en el intervalo indicado:
>
> **(a)** $f(x) = \cos x$ en $[-1, 2]$
>
> **(b)** $f(x) = x^2 - 9$ en $[-2, 1]$
>
> **(c)** $f(x) = -e^{-x}$ en $[0, 3]$
>
> **(d)** $f(x) = \ln(1 + x^2)$ en $[-1, 1]$
>
> **(e)** $f(x) = \ln(1 + x^2)$ en $[2, 3]$
>
> **(f)** $f(x) = \sqrt[3]{x^2 - 4}$ en $[-3, 3]$

> [!question] Ejercicio 3
> Resuelve los problemas de optimización siguientes:
>
> **(a)** La suma de tres números positivos es 18 y el primer número es el doble del segundo. ¿Cuánto es lo máximo que puede valer su producto?
>
> **(b)** Queremos construir un tanque de agua hermético, con forma cilíndrica y con capacidad para $1024\pi$ litros. ¿Cuáles son las dimensiones apropiadas para que el gasto de material sea mínimo?
>
> **(c)** Queremos construir una piscina de base rectangular cuya profundidad no puede superar los 3 metros. Además, ha de tener dos paredes opuestas cuadradas y una capacidad de $281.25$ metros cúbicos. ¿Cuáles son las dimensiones óptimas para el menor gasto de material? (incluyendo las cuatro paredes y el suelo).

> [!question] Ejercicio 4
> Calcula el polinomio de Taylor de las siguientes funciones:
>
> **(a)** $e^{-2x}$ en $a = 0$ (grado 4)
>
> **(b)** $\cos 3x$ en $a = 0$ (grado 5)
>
> **(c)** $x^2 - 4x + 5$ en $a = 2$ (grado 3) y en $a = -1$ (grado 3). ¿Observas algo especial? ¿A qué crees que se debe?

---

# Soluciones

> [!success] Solución del Ejercicio 1
> Derivadas:
>
> **(a)** $0$
>
> **(b)** $7$
>
> **(c)** $4x^3 - 4 + \frac{3}{2\sqrt{x}}$
>
> **(d)** $3x^2 - 2 - \operatorname{sen} x$
>
> **(e)** $1 - \frac{1}{x^2}$
>
> **(f)** $3 \cos 3x$
>
> **(g)** $3x^2 \cos x^3$
>
> **(h)** $3 \operatorname{sen}^2 x \cos x$
>
> **(i)** $2 \cos^2 x - 2 \operatorname{sen}^2 x = 2 \cos 2x$
>
> **(j)** $0$
>
> **(k)** $2x + 2x \tan^2 x^2$
>
> **(l)** $\frac{2 \operatorname{sen} x}{\cos^3 x}$
>
> **(m)** $\frac{1}{1 + \cos x}$
>
> **(n)** $-\frac{1}{t^2} + \frac{9}{t^4}$
>
> **(ñ)** $\frac{10}{(2-x)\cos^2(\ln(2-x))}$
>
> **(o)** $\frac{1}{t} - \frac{3t^2 + 1}{2(4 + t + t^3)}$
>
> **(p)** $2 \arctan x$
>
> **(q)** $7^{x^2 - 3x}(2x - 3) \ln 7$
>
> **(r)** $5x^4 - 7$
>
> **(s)** $3x^2 + 2x - 3$
>
> **(t)** $-(\operatorname{sen} x) e^{\cos x}$
>
> **(u)** $-\frac{3e^7 x^2}{\operatorname{sen} x^3 \tan x^3}$
>
> **(v)** $(\tan x)^{\ln x} \left( \frac{\ln \tan x}{x} + \frac{2 \ln x}{\operatorname{sen} 2x} \right)$
>
> **(w)** $(1 + \tan^2(x \ln x))(1 + \ln x)$
>
> **(x)** $x^{\tan x} \left( \frac{\ln x}{\cos^2 x} + \frac{\tan x}{x} \right)$
>
> **(y)** $x^{x^{2-2x}} \left( (2x - 2^x \ln 2)\ln x + \frac{x - 2^x}{x} \right)$
>
> **($\alpha$)** $\frac{1}{x \ln 10}$
>
> **($\beta$)** $\frac{\operatorname{sen} x + x \cos x}{x(\ln 4) \operatorname{sen} x}$
>
> **($\gamma$)** $\frac{3x^2 - 1}{(x^3 - x)\ln 10}$

> [!success] Solución del Ejercicio 2
> Monotonía y acotaciones:
>
> **(a)** $\text{Máx } f = 1$, $\text{Mín } f = \cos 2 \approx -0.41614$, $|f(x)| \le 1$ si $x \in [-1, 2]$
>
> **(b)** $\text{Máx } f = -5$, $\text{Mín } f = -9$, $|f(x)| \le 9$ si $x \in [-2, 1]$
>
> **(c)** $\text{Máx } f = -e^{-3} \approx -0.04978$, $\text{Mín } f = -1$, $|f(x)| \le 1$ si $x \in [0, 3]$
>
> **(d)** En $[-1, 1]$: $\text{Máx } f = \ln 2 \approx 0.6931$, $\text{Mín } f = 0$, $|f(x)| \le \ln 2$ si $x \in [-1, 1]$
>
> **(e)** En $[2, 3]$: $\text{Máx } f = \ln 10 \approx 2.3025$, $\text{Mín } f = \ln 5 \approx 1.6094$, $|f(x)| \le \ln 10$ si $x \in [2, 3]$
>
> **(f)** $\text{Máx } f = \sqrt[3]{5} \approx 1.70997$, $\text{Mín } f = \sqrt[3]{-4} \approx -1.58740$, $|f(x)| \le \sqrt[3]{5}$ si $x \in [-3, 3]$

> [!success] Solución del Ejercicio 3
> Problemas de optimización:
>
> **(a)** El valor máximo del producto es $192$.
>
> **(b)** Radio de la base $r = 8$ y altura $h = 16$.
>
> **(c)** Profundidad y ancho: $3\text{ m}$. Largo: $31.25\text{ m}$.

> [!success] Solución del Ejercicio 4
> Polinomio de Taylor:
>
> **(a)** $1 - 2x + 2x^2 - \frac{4x^3}{3} + \frac{2x^4}{3}$
>
> **(b)** $1 - \frac{9x^2}{2} + \frac{27x^4}{8}$
>
> **(c)** En $a = 2$: $x^2 - 4x + 5$. En $a = -1$: $x^2 - 4x + 5$. Se obtiene el mismo resultado porque la función de partida es un polinomio, con lo cual su polinomio de Taylor de grado mayor o igual que su grado coincide exactamente con la propia función.