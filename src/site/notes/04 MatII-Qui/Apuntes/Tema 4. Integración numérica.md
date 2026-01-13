---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/tema-4-integracion-numerica/","created":"2026-01-08T10:24:16.931+01:00","updated":"2025-09-15T10:05:23.211+02:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 4. Métodos de integración numérica
- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#1. Introducción\|1. Introducción]]
- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|2. Regla del punto medio]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|2.1 Fórmula de cuadratura]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|2.2 Cota del error]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|2.3 Fórmula compuesta]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|2.4 Cota del error y cálculo del número de nodos]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#2. Regla del punto medio\|Ejemplo]]
- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#3. Regla del trapecio\|3. Regla del trapecio]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#3. Regla del trapecio\|Fórmula de cuadratura]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#3. Regla del trapecio\|Fórmula compuesta]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#3. Regla del trapecio\|Ejemplo]]
- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#4. Regla de Simpson\|4. Regla de Simpson]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#4. Regla de Simpson\|4.1 Fórmula de cuadratura]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#4. Regla de Simpson\|4.2 Cota del error]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#4. Regla de Simpson\|4.3 Fórmula compuesta y cota del error]]
	- [[04 MatII-Qui/Apuntes/Tema 4. Integración numérica#4. Regla de Simpson\|Ejemplo]]


---

## 1. Introducción
Consideremos la función $f(x) = e^{-x^2}$, cuya gráfica en el intervalo $[-2, 2]$ es:
![Pasted image 20250210090748.png|600](/img/user/imagenes/Pasted%20image%2020250210090748.png)
**¿Cómo calcularías el área que encierra dicha función con el eje $OX$?**
Sabemos que dicha área corresponde con el valor de la integral:
$$
  \int_{-2}^{2} e^{-x^2} \, dx
$$
Pero, ¿y si no existe una primitiva elemental de dicha función? En este tema, introduciremos métodos numéricos basados en interpolación para aproximar el valor de integrales definidas.

---

## 2. Regla del punto medio

### 2.1 Fórmula de cuadratura
Aproximamos la función $f(x)$ por una constante, tomando el valor de la función en el punto medio del intervalo $[a, b]$:
$$
c = \frac{a + b}{2}
$$
Entonces, la aproximación de la integral es:
$$
\int_{a}^{b} f(x) \, dx \approx (b - a) f\left(\frac{a + b}{2}\right)
$$

**Interpretación geométrica:** Aproximamos el área bajo la curva por el área de un rectángulo con base $[a, b]$ y altura $f\left(\frac{a + b}{2}\right)$.
![[Pasted image 20250210091056.png\|400]]

### 2.2 Cota del error
El error cometido es:
$$
E_{Pm}(f) = \frac{(b - a)^3}{24} f''(\xi), \quad \text{para } \xi \in [a, b]
$$
Cota del error:
$$
|E_{Pm}(f)| \leq \frac{(b - a)^3}{24} \max_{x \in [a, b]} |f''(x)|
$$

### 2.3 Fórmula compuesta
Dividimos el intervalo $[a, b]$ en $n$ subintervalos de longitud $\frac{b - a}{n}$. Lo más cómodo es definir $h=\frac{b-a}{2n}$, y $x_i=a+i\cdot h, i=0,1,\ldots, 2n$. 
La aproximación de la integral es:
$$
\int_{a}^{b} f(x) \, dx \approx 2h \sum_{i=0}^{n-1} f(x_{2i+1})
$$

### 2.4 Cota del error y cálculo del número de nodos
Cota del error para el cálculo de nodos:
$$
|E_{Pm}(f)| \leq \frac{(b - a)^3}{24n^2} \max_{x \in [a, b]} |f''(x)|
$$
### Ejemplo
Vamos a aplicar la **regla del punto medio compuesta** para aproximar la integral:  
$$
I = \int_{-1}^{1} \sqrt{1 - x^2} \, dx
$$
dividiendo el intervalo en **cuatro subintervalos**.

El intervalo de integración es $[-1,1]$, y dividimos en $n = 4$ subintervalos. Tomamos
$$
h = \frac{b - a}{2n}= \frac{1}{4}
$$
y por tanto:
$$
x_0 = -1, \quad x_1 = -\frac{3}{4}, \quad x_2 = -\frac{1}{2}, \quad x_3 = -\frac{1}{4}, \quad x_4 = 0,
$$
$$
x_5 = \frac{1}{4}, \quad x_6 = \frac{1}{2}, \quad x_7 = \frac{3}{4}, \quad x_8 = 1.
$$
Evaluamos en los impares:
$$
f\left(-\frac{3}{4}\right) = \sqrt{1 - \left(-\frac{3}{4}\right)^2} = \sqrt{1 - \frac{9}{16}} = \sqrt{\frac{7}{16}} = \frac{\sqrt{7}}{4}
$$
$$
f\left(-\frac{1}{4}\right) = \sqrt{1 - \left(-\frac{1}{4}\right)^2} = \sqrt{1 - \frac{1}{16}} = \sqrt{\frac{15}{16}} = \frac{\sqrt{15}}{4}
$$
$$
f\left(\frac{1}{4}\right) = \frac{\sqrt{15}}{4}, \quad f\left(\frac{3}{4}\right) = \frac{\sqrt{7}}{4}
$$
Aplicando la fórmula
$$
I \approx \frac{1}{2} \left[ \frac{\sqrt{7}}{4} + \frac{\sqrt{15}}{4} + \frac{\sqrt{15}}{4} + \frac{\sqrt{7}}{4} \right]=1.6297
$$
La integral exacta es conocida, la mitad del área  del círculo de radio 1:
$$
I_{\text{exacta}} = \frac{\pi}{2}
$$
luego el error cometido con la regla del punto medio compuesta es aproximadamente:
$$
|E| = |1.5708 - 1.6297| \approx 0.0589
$$


---

## 3. Regla del trapecio

### Fórmula de cuadratura
Aproximamos $f(x)$ por una recta que une los puntos $(a, f(a))$ y $(b, f(b))$:
$$
\int_{a}^{b} f(x) \, dx \approx \frac{b - a}{2} (f(a) + f(b))
$$

**Interpretación geométrica:** Aproximamos el área bajo la curva por el área de un trapecio con bases $f(a)$ y $f(b)$.
![[Pasted image 20250210091225.png\|400]]


### Fórmula compuesta
Dividimos el intervalo $[a, b]$ en $n$ subintervalos de longitud $\frac{b - a}{n}$. Tenemos $x_i=a+i\cdot h, i=0,1,\ldots, n$
La aproximación es:
$$
\int_{a}^{b} f(x) \, dx \approx \frac{h}{2} \left( f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{i}) + f(x_{n}) \right)
$$
Cota del error:
$$
|E_{Tr}(f)| \leq \frac{(b - a)^3}{12n^2} \max_{x \in [a, b]} |f''(x)|
$$
### Ejemplo
Para calcular la integral $I = \int_{-1}^{1} \sqrt{1 - x^2} \, dx$ utilizando la regla compuesta del trapecio con cuatro subintervalos, seguimos los siguientes pasos:
Tomamos $h=\frac{b-a}{n}=\frac{1}{2}$. Los puntos $x_i$ se calculan como:
$$
x_0 = -1, \quad x_1 = -0.5, \quad x_2 = 0, \quad x_3 = 0.5, \quad x_4 = 1
$$


Evaluamos $f(x) = \sqrt{1 - x^2}$ en cada $x_i$:
$$
\begin{align*}
f(x_0) &= f(-1) = \sqrt{1 - (-1)^2} = 0 \\
f(x_1) &= f(-0.5) = \sqrt{1 - (-0.5)^2} = \sqrt{1 - 0.25} = \sqrt{0.75} \approx 0.8660 \\
f(x_2) &= f(0) = \sqrt{1 - 0^2} = 1 \\
f(x_3) &= f(0.5) = \sqrt{1 - 0.5^2} = \sqrt{1 - 0.25} = \sqrt{0.75} \approx 0.8660 \\
f(x_4) &= f(1) = \sqrt{1 - 1^2} = 0 \\
\end{align*}
$$
Sustituyendo los valores:
$$
\begin{align*}
\int_{-1}^{1} \sqrt{1 - x^2} \, dx &\approx 0.5 \left( \frac{f(x_0)}{2} + f(x_1) + f(x_2) + f(x_3) + \frac{f(x_4)}{2} \right) \\
&= 0.5 \left( \frac{0}{2} + 0.8660 + 1 + 0.8660 + \frac{0}{2} \right) \\
&= 0.5 \left( 0 + 0.8660 + 1 + 0.8660 + 0 \right) \\
&= 0.5 \left( 2.7320 \right) \\
&= 1.3660 \\
\end{align*}
$$

Error cometido:
$$
|E| = |1.5708 - 1.3660| \approx 0.2048
$$

---

## 4. Regla de Simpson

### 4.1 Fórmula de cuadratura
$$
\int_{a}^{b} f(x) \, dx \approx \frac{b - a}{6} \left( f(a) + 4f\left(\frac{a + b}{2}\right) + f(b) \right)
$$

### 4.2 Cota del error
$$
E_S(f) = -\frac{(b - a)^5}{2880} f^{iv}(\xi)
$$

### 4.3 Fórmula compuesta y cota del error

Dividimos el intervalo $[a, b]$ en $n$ subintervalos de longitud $\frac{b - a}{n}$. Al igual que en la fórmula del punto medio, lo más cómodo es definir $h=\frac{b-a}{2n}$, y $x_i=a+i\cdot h, i=0,1,\ldots, 2n$. 
La aproximación de la integral es:
$$
\int_{a}^{b} f(x) \, dx=\frac{h}{3} \left[ f(x_0) + 2 \sum_{i=1}^{n-1} f(x_{2i}) + 4 \sum_{i=1}^{n} f(x_{2i-1}) + f(x_{2n}) \right]
$$
$$
|E_S(f)| \leq \frac{(b - a)^5}{2880n^4} \max_{x \in [a, b]} |f^{iv}(x)|
$$

### Ejemplo
Para calcular la integral $I = \int_{-1}^{1} \sqrt{1 - x^2} \, dx$ utilizando la regla compuesta de Simpson con cuatro subintervalos, seguimos los siguientes pasos. Tenemos $h=\frac{b-a}{2n}=\frac{1}{4}$
$$
x_0 = -1, \quad x_1 = -0.75, \quad x_2 = -0.5, \quad x_3 = -0.25, \quad x_4 = 0, \quad x_5 = 0.25, \quad x_6 = 0.5, \quad x_7 = 0.75, \quad x_8 = 1
$$

Evaluamos $f(x) = \sqrt{1 - x^2}$ en cada $x_i$:
$$
\begin{align*}
f(x_0) &= f(-1) = \sqrt{1 - (-1)^2} = 0 \\
f(x_1) &= f(-0.75) = \sqrt{1 - (-0.75)^2} = \sqrt{1 - 0.5625} = \sqrt{0.4375} \approx 0.6614 \\
f(x_2) &= f(-0.5) = \sqrt{1 - (-0.5)^2} = \sqrt{1 - 0.25} = \sqrt{0.75} \approx 0.8660 \\
f(x_3) &= f(-0.25) = \sqrt{1 - (-0.25)^2} = \sqrt{1 - 0.0625} = \sqrt{0.9375} \approx 0.9682 \\
f(x_4) &= f(0) = \sqrt{1 - 0^2} = 1 \\
f(x_5) &= f(0.25) = \sqrt{1 - 0.25^2} = \sqrt{1 - 0.0625} = \sqrt{0.9375} \approx 0.9682 \\
f(x_6) &= f(0.5) = \sqrt{1 - 0.5^2} = \sqrt{1 - 0.25} = \sqrt{0.75} \approx 0.8660 \\
f(x_7) &= f(0.75) = \sqrt{1 - 0.75^2} = \sqrt{1 - 0.5625} = \sqrt{0.4375} \approx 0.6614 \\
f(x_8) &= f(1) = \sqrt{1 - 1^2} = 0 \\
\end{align*}
$$

Sustituyendo los valores:
$$
\begin{align*}
\int_{-1}^{1} \sqrt{1 - x^2} \, dx &\approx \frac{1/4}{3} \left[ f(x_0) + 2 \left( f(x_2) + f(x_4) + f(x_6) \right) + 4 \left( f(x_1) + f(x_3) + f(x_5) + f(x_7) \right) + f(x_8) \right] \\
&= \frac{1}{12} \left[ 0 + 2 \left( 0.8660 + 1 + 0.8660 \right) + 4 \left( 0.6614 + 0.9682 + 0.9682 + 0.6614 \right) + 0 \right] \\
&= \frac{1}{12} \left[ 0 + 2 \left( 2.7320 \right) + 4 \left( 3.2592 \right) + 0 \right] \\
&= \frac{1}{12} \left[ 0 + 5.4640 + 13.0368 + 0 \right] \\
&= \frac{1}{12} \left[ 18.5008 \right] \\
&\approx 1.5417 \\
\end{align*}
$$
Error cometido:
$$
|E| = |1.5708 - 1.5417| \approx 0.0361
$$