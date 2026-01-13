---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema03-ej/","updated":"2026-01-12T12:55:51.087+01:00"}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 3: Cálculo Integral de Varias Variables. Ejercicios.

## 1. Integrales Dobles

### Definición y Cálculo General
**Ejercicio 1**
Dibuja la región de integración y calcula $\iint_{\Omega}f$ en los siguientes casos:
1.  $f(x,y)=x \sin y - y e^{x}$ en $\Omega=[-1,1]\times[0,\pi/2]$.
2.  $f(x,y)=x^{2}-y$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[-1,1], -x^{2}\le y\le x^{2}\}$.
3.  $f(x,y)=xy-x^{3}$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[0,1], -1\le y\le x\}$.
4.  $f(x,y)=2x\sin(x^{2}y)$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[0,2], |y|\leq x\}$.
5.  $f(x,y)=y \sin x$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:|x|+|y|\le1\}$.

### Teorema de Fubini
**Ejercicio 2**
Sobre el recinto $\Omega=\{(x,y)\in\mathbb{R}^{2}:x^{2}+(y-1)^{2}\le1, x\ge0\}$ se consideran las funciones:
$$f(x,y)=\frac{1}{\sqrt{1-x^{2}}} \quad \text{y} \quad g(x,y)=\sin(y-1)$$
Aplica el teorema de Fubini a $\iint_{\Omega}f$ y $\iint_{\Omega}g$ en las dos ordenaciones posibles. Calcula las integrales en el orden más adecuado.

### Cambio de Orden de Integración
**Ejercicio 3**
Determina el recinto de integración y cambia el orden de integración en las siguientes integrales:
1.  $\displaystyle \int_{0}^{3}\int_{4x/3}^{\sqrt{25-x^{2}}}f(x,y)\,dy\,dx$
2.  $\displaystyle \int_{0}^{1}\int_{0}^{y}f(x,y)\,dx\,dy$
3.  $\displaystyle \int_{0}^{\pi/2}\int_{-\sin(x/2)}^{\sin(x/2)}f(x,y)\,dy\,dx$
4.  $\displaystyle \int_{0}^{e}\int_{0}^{\log x}f(x,y)\,dy\,dx$

**Ejercicio 4**
Halla el valor de la integral (requiere cambiar el orden):
$$\int_{0}^{\pi}\int_{x}^{\pi}\frac{\sin y}{y}\,dy\,dx$$

### Aplicaciones
**Ejercicio 5**
Calcula las siguientes áreas:
1.  Área limitada por las curvas $y=x$ y $y=2-x^{2}$.
2.  Área encerrada por las curvas $xy=4$, $xy=8$, $xy^{3}=5$ y $xy^{3}=15$.

**Ejercicio 6**
Sea $S$ una región del plano limitada por las curvas que se indican. Calcula la masa y el centro de gravedad de $S$ suponiendo que la densidad es constante e igual a $\rho$.
1.  $y=x^{2}$, $x+y=2$.
2.  $y+3=x^{2}$, $x^{2}=5-y$.
3.  $y=\sin^{2}x$, $y=0$, $x\in[0,\pi]$.
4.  $y=\sin x$, $y=\cos x$, $x\in[0,\pi/4]$.

**Ejercicio 7**
Determina las coordenadas del centro de gravedad de la placa:
$$B=\{(x,y)\in\mathbb{R}^{2}: 1\le x\le2, 1\le y\le3\}$$
cuya densidad viene dada por la función $\sigma(x,y)=xy$.

**Ejercicio 8**
Una placa metálica viene representada por el conjunto del plano:
$$P=\{(x,y)\in\mathbb{R}^{2}: |y|\le1\}$$
y su densidad es $\sigma(x,y)=y^{2}$. Calcula el centro de gravedad y los momentos de inercia con respecto a los ejes.

---

## 2. Integrales Triples

### Cálculo General
**Ejercicio 9**
Calcula las siguientes integrales en los recintos que se indican:
1.  $\displaystyle \iiint_{\Omega}(x^{2}+y^{2}+z^{2})\,dx\,dy\,dz$ donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
2.  $\displaystyle \iiint_{\Omega}x^{3}\,dx\,dy\,dz$ donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
3.  $\displaystyle \iiint_{\Omega}y e^{-xy}\,dx\,dy\,dz$ donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
4.  $\displaystyle \iiint_{\Omega}(2x+3y+z)\,dx\,dy\,dz$ donde $\Omega=[1,2]\times[-1,1]\times[0,1]$.
5.  $\displaystyle \iiint_{\Omega}z e^{x+y}\,dx\,dy\,dz$ donde $\Omega=[0,1]\times[0,1]\times[0,1]$.

**Ejercicio 10**
Calcula la integral $\iiint_{\Omega}x^{2}\cos x \,dx\,dy\,dz$, donde $\Omega$ es la región limitada por los planos:
$$z=0, \quad z=\pi, \quad y=0, \quad x=0, \quad x+y=1$$
Dibuja la región de integración.

### Aplicaciones en Sólidos (3D)
**Ejercicio 11**
Calcula los siguientes volúmenes:
1.  Volumen de la región limitada por $x^{2}+y^{2}\le4$ y $x^{2}+y^{2}+z^{2}\le16$.
2.  Volumen del sólido limitado por los conos $z=1-\sqrt{x^{2}+y^{2}}$ y $z=-1+\sqrt{x^{2}+y^{2}}$.
3.  Volumen de la región limitada por el paraboloide $z=x^{2}+y^{2}$ y por $x^{2}+y^{2}=4$ en $z\ge0$.
4.  Volumen de la región limitada por $x^{2}+y^{2}+z^{2} < 2$, $x^{2}+y^{2}\le z$ y $z<6/5$.

---

## 3. Cambio de Variables

**Ejercicio 12**
Calcula, usando coordenadas polares, la integral de la función $f(x,y) = \sqrt{x^2 + y^2}$ sobre la región $\Omega$ definida por el círculo unitario:
$$\Omega = \{ (x,y) \in \mathbb{R}^2 \mid x^2 + y^2 \le 1 \}$$

**Ejercicio 13**
Evalúa, usando coordenadas polares, la siguiente integral doble:
$$\iint_{\Omega} (x^2 + y^2) \, dx \, dy$$
Donde $\Omega$ es la mitad superior del disco de radio 2 (definida por $x^2 + y^2 \le 4$ y $y \ge 0$).

**Ejercicio 14**
Calcula, usando coordenadas polares, la integral de la función exponencial sobre la región anular comprendida entre los círculos de radio 1 y radio 3 ($1 \le x^2 + y^2 \le 9$):
$$\iint_{\Omega} e^{-(x^2+y^2)} \, dx \, dy$$