---
{"dg-publish":true,"permalink":"/calculo-naut/apuntes/calc-naut-tema01/","updated":"2025-11-04T10:59:12.088+01:00"}
---

[[Calculo-Naut/calc-naut-indice\|Volver al índice]]
# Tema 1: Sucesiones y Series
- [[Calculo-Naut/Apuntes/calc-naut-tema01#Sucesiones reales y límites\|Sucesiones reales y límites]]
- [[Calculo-Naut/Apuntes/calc-naut-tema01#Series reales y sumas exactas\|Series reales y sumas exactas]]
- [[Calculo-Naut/Apuntes/calc-naut-tema01#Criterios de convergencia para series de términos positivos\|Criterios de convergencia para series de términos positivos]]
- [[Calculo-Naut/Apuntes/calc-naut-tema01#Series de potencias y desarrollos de Taylor\|Series de potencias y desarrollos de Taylor]]

## Sucesiones reales y límites

**Definiciones**
* Sucesión real: aplicación $a:\mathbb{N}\to\mathbb{R}$, se escribe $(a_n)$.
* Convergencia: $(a_n)\to L$ si $\lim_{n\to\infty} a_n=L$.
* Divergencia: el límite no existe (oscilante) o es infinito.

**Cálculo de límites**
* Cociente de polinomios: divide numerador y denominador por la mayor potencia de $n$.
  Ejemplo:
  $\frac{5n^3+2}{2n^3-7n}\to \tfrac{5}{2}$.
* Comparaciones: si $0\leq a_n\leq b_n$ y $\lim b_n=0$, entonces $\lim a_n=0$.
  Ejemplo: $0\leq \frac{\sin n}{n}\leq \frac{1}{n}\to 0 \implies \lim \frac{\sin n}{n}=0$.
* Racionalización: útil con raíces.
  Ejemplo: $\lim_{n\to\infty}\bigl(\sqrt{n^2+3n}-n\bigr) = \lim \frac{3n}{\sqrt{n^2+3n}+n} = \tfrac{3}{2}$.


**Límites notables**
$$
\lim_{n\to\infty}\Bigl(1+\tfrac{1}{n}\Bigr)^n=e, 
\quad 
\lim_{n\to\infty} r^n=
\begin{cases}
0 & |r|<1\\
\infty & r>1.
\end{cases}
$$

**Ejemplos**
$\tfrac{n^2+1}{3n^2-2}\to \tfrac{1}{3}$.
$\sqrt{n^2+1}-n\to 0$.

---

## Series reales y sumas exactas

**Definición**
* Serie: $\sum_{n=1}^\infty a_n$.
* Converge si la sucesión de sumas parciales converge.

**Condición necesaria**
* Si $\sum a_n$ converge, entonces $\lim a_n=0$.
  Ejemplo: $a_n=\frac{1}{2n+1}\to 0$ (posible convergencia);
  en cambio, $a_n=\tfrac{1}{n+2}$ sí tiende a 0, pero la serie $\sum \tfrac{1}{n+2}$ diverge como la armónica.

**Series fundamentales**
* Geométrica: $\sum ar^n$. Converge si $|r|<1$, suma $=\frac{a}{1-r}$.
  Ejemplo: $\sum_{n=0}^\infty \left(\tfrac{1}{3}\right)^n = \tfrac{1}{1-\tfrac{1}{3}}=\tfrac{3}{2}$.
* Armónica: $\sum \tfrac{1}{n}$ diverge, $\sum \tfrac{1}{n^p}$ converge si $p>1$.

**Sumas exactas de series**: **Geométricas o combinaciones lineales de geométricas.**
   Ejemplo: $\sum (3\cdot 0.3^n+2\cdot 0.8^n)$.


---

## Criterios de convergencia para series de términos positivos

**Criterio de comparación**

* Si $0\leq a_n\leq b_n$ y $\sum b_n$ converge, también $\sum a_n$.
  Ejemplo: $a_n=\tfrac{1}{n^2+5}$, $b_n=\tfrac{1}{n^2}$. Como $\sum b_n$ converge, también $\sum a_n$.

**Criterio de comparación límite**

* Si $\lim \tfrac{a_n}{b_n}=c\in(0,\infty)$, ambas series tienen el mismo carácter.
  Ejemplo: $a_n=\tfrac{1}{n^2+1}$, $b_n=\tfrac{1}{n^2}$, límite $=1$, ambas convergen.

**Criterio del cociente (d’Alembert)**
$$
L=\lim_{n\to\infty}\Bigl|\tfrac{a_{n+1}}{a_n}\Bigr|
$$

* $L<1$: converge.
* $L>1$: diverge.
* $L=1$: no concluye.

Ejemplo: $a_n=\tfrac{n!}{n^n}$.
$\frac{a_{n+1}}{a_n}=\frac{(n+1)!}{(n+1)^{n+1}}\cdot \frac{n^n}{n!}=\left(\frac{n}{n+1}\right)^n\to e^{-1}<1$, converge.

**Criterio de la raíz (Cauchy)**
$$
L=\lim_{n\to\infty}\sqrt[n]{|a_n|}
$$

* $L<1$: converge.
* $L>1$: diverge.
* $L=1$: no concluye.
Ejemplo: $a_n=\left(\tfrac{3}{5}\right)^n$, raíz $\to \tfrac{3}{5}<1$, converge.
Ejemplo: $a_n=\tfrac{n^2}{2^n}$, raíz $\to \tfrac{1}{2}<1$, converge.


## Series de potencias y desarrollos de Taylor

**Series de potencias**

* Forma: $\sum a_n (x-x_0)^n$.
* Converge en un intervalo $(x_0-R, x_0+R)$.
* Radio $R$:
$$
R=\frac{1}{\limsup \sqrt[n]{|a_n|}}.
$$
- Permiten definir nuevas funciones y re-expresar otras.

**Ejemplo**
Serie geométrica: $\sum x^n=\tfrac{1}{1-x}, \ |x|<1$.


**Teorema de Taylor**

* Para $f$ derivable:

$$
f(x)=\sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!}(x-x_0)^k + R_n(x).
$$

**Series de McLaurin (desarrollo en $x_0=0$)**

* $e^x=\sum \tfrac{x^n}{n!}$.
* $\sin x=\sum (-1)^n \tfrac{x^{2n+1}}{(2n+1)!}$.
* $\cos x=\sum (-1)^n \tfrac{x^{2n}}{(2n)!}$.
* $\ln(1+x)=\sum (-1)^{n+1} \tfrac{x^n}{n}, \ |x|<1$.

**Ejemplo aplicado**

* Aproximar $\ln(1.1)$ usando los tres primeros términos:
  $\ln(1+x)\approx x-\tfrac{x^2}{2}+\tfrac{x^3}{3}$ con $x=0.1$:
  $\ln(1.1)\approx 0.1-0.005+0.000333=0.09533$ (valor real $0.09531$).

[[Calculo-Naut/Apuntes/calc-naut-tema01-ej\|Ejercicios]]

