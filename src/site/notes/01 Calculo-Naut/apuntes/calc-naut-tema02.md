---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema02/","created":"2026-09-28T10:35:37.480+02:00","updated":"2026-09-29T07:32:05.315+02:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|Volver al índice]]

# **TEMA 2: Cálculo diferencial e integral en una variable**

- [[01 Calculo-Naut/apuntes/calc-naut-tema02#1. Funciones, Límites y Continuidad\|1. Funciones, Límites y Continuidad]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema02#2. Concepto de Derivada\|2. Concepto de Derivada]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema02#3. La Integral Indefinida\|3. La Integral Indefinida]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema02#4. La Integral Definida y sus Aplicaciones\|4. La Integral Definida y sus Aplicaciones]]


## 1. Funciones, Límites y Continuidad

Una **función** $f$ es una regla que asigna a cada elemento $x$ de un conjunto A (el **dominio**) un único elemento $y$ de un conjunto B (el **codominio**). Lo escribimos como $f: A \to B$ y $y = f(x)$.

* **Dominio ($Dom(f)$):** El conjunto de todos los valores de entrada $x$ para los cuales la función está definida.
* **Imagen o Recorrido ($Im(f)$):** El conjunto de todos los valores de salida $y$ que la función puede producir.


El **límite** de una función $f(x)$ cuando $x$ se acerca a un punto $c$ es el valor $L$ al que la función se aproxima. Es una idea de "aproximación" y no necesariamente el valor que toma la función en el punto, pues podría incluso no estar definida en $c$.
Se denota como: 
$$\lim_{x \to c} f(x) = L$$

Una función $f(x)$ es **continua** en un punto $x=c$ si cumple tres condiciones:
1.  Existe $f(c)$ (la función está definida en el punto).
2.  Existe $\lim_{x \to c} f(x)$ (el límite existe).
3.  $\lim_{x \to c} f(x) = f(c)$ (el límite y el valor de la función coinciden).

Intuitivamente, una función es continua si puedes dibujar su gráfica sin levantar el lápiz del papel.

**Cálculo de Límites e Indeterminaciones:**
La mayoría de los límites se pueden resolver por sustitución directa. Sin embargo, a menudo nos encontramos con **indeterminaciones**, formas que no tienen un valor definido y requieren más análisis:
$$\frac{0}{0}, \quad \frac{\infty}{\infty}, \quad \infty - \infty, \quad 0 \cdot \infty, \quad 1^\infty, \quad 0^0, \quad \infty^0$$



## 2. Concepto de Derivada

La **derivada** de una función $f(x)$ en un punto $x$, denotada como $f'(x)$ o $\frac{dy}{dx}$,  se define formalmente como el límite:
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

* **Interpretación geométrica:** La derivada $f'(c)$ es la **pendiente de la recta tangente** a la gráfica de la función $y=f(x)$ en el punto $(c, f(c))$. Una derivada positiva indica que la función crece, una negativa que decrece, y una nula puede indicar un máximo o un mínimo.

* **Interpretación física:** Si $s(t)$ es la posición de un objeto en el tiempo $t$, la derivada $s'(t)$ es la **velocidad instantánea** del objeto. La segunda derivada, $s''(t)$, es la **aceleración instantánea**.

* **Interpretación general**: Mide la **tasa de cambio instantánea** de la función en ese punto.

### **2.1. Reglas de Derivación y Tabla de Derivadas**

Es fundamental conocer las reglas para derivar combinaciones de funciones y las derivadas de las funciones elementales.

- **Linealidad**: $(\alpha f+\beta g)'=\alpha f'+\beta g'$.
* **Regla del Producto:** $(f \cdot g)' = f'g + fg'$.
* **Regla del Cociente:** $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$.
* **Regla de la Cadena:** Si $y=f(u)$ y $u=g(x)$, entonces $\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$. Esencial para derivar funciones compuestas.

| Función $f(x)$ | Derivada $f'(x)$       |
| :------------- | :--------------------- |
| $k$ (constante) | $0$                       |
| $x^n$           | $n \cdot x^{n-1}$         |
| $e^x$           | $e^x$                     |
| $a^x$           | $a^x \ln a$               |
| $\ln(x)$        | $\frac{1}{x}$             |
| $\log_a(x)$     | $\frac{1}{x \ln a}$       |
| $\sin(x)$       | $\cos(x)$                 |
| $\cos(x)$       | $-\sin(x)$                |
| $\tan(x)$       | $\sec^2(x)$               |
| $\arcsin(x)$    | $\frac{1}{\sqrt{1-x^2}}$  |
| $\arctan(x)$    | $\frac{1}{1+x^2}$         |


#### Ejemplos.
Calcula la derivada de las siguientes funciones:

| 1. $f(x) = 3x$                | 11. $f(x) = \dfrac{x^3 - 1}{x}$ |
| ----------------------------- | ------------------------------- |
| 2. $f(x) = x^3$               | 12. $f(x) = \dfrac{\ln(x)}{x}$  |
| 3. $f(x) = 5x^2 - 4x + 7$     | 13. $f(x) = e^{2x}$             |
| 4. $f(x) = \dfrac{1}{x}$      | 14. $f(x) = \sin(x^2)$          |
| 5. $f(x) = \sqrt{x}$          | 15. $f(x) = \ln(\sqrt{x})$      |
| 6. $f(x) = e^x + 2x$          | 16. $f(x) = (3x+1)\cos(x)$      |
| 7. $f(x) = \ln(x)$            | 17. $f(x) = \dfrac{e^x}{x^2}$   |
| 8. $f(x) = \sin(x) + \cos(x)$ | 18. $f(x) = \sqrt{x^2 + 1}$     |
| 9. $f(x) = x \cdot e^x$       | 19. $f(x) = e^{\sin(x)}$        |
| 10. $f(x) = x^2 \sin(x)$      | 20. $f(x) = \ln(x^2 + 3x)$      |




### **2.2. Regla de L'Hôpital**

Es una herramienta muy útil para resolver indeterminaciones del tipo $\frac{0}{0}$ y $\frac{\infty}{\infty}$.

Si $\lim_{x \to c} f(x) = \lim_{x \to c} g(x) = 0$ (o ambos son $\pm\infty$), entonces:
$$\lim_{x \to c} \frac{f(x)}{g(x)} = \lim_{x \to c} \frac{f'(x)}{g'(x)}$$
**¡Importante!** Solo se puede aplicar a cocientes y después de haber verificado la indeterminación.

**Ejemplo:** Calcular $\lim_{x \to 0} \frac{\sin(x)}{x}$.
Es una indeterminación $\frac{0}{0}$. Aplicando L'Hôpital:
$$\lim_{x \to 0} \frac{\sin(x)}{x} = \lim_{x \to 0} \frac{\cos(x)}{1} = \frac{\cos(0)}{1} = 1$$
Más ejemplos
$$
\begin{aligned}
1.\;& \lim_{x \to 0} \frac{\sin x}{x} 
& \qquad 6.\;& \lim_{x \to \infty} \frac{e^x}{x^2} \\[6pt]
2.\;& \lim_{x \to 0} \frac{1-\cos x}{x^2} 
& \qquad 7.\;& \lim_{x \to 0^+} x \ln x \\[6pt]
3.\;& \lim_{x \to \infty} \frac{\ln x}{x} 
& \qquad 8.\;& \lim_{x \to 1} \frac{x^3-1}{x-1} \\[6pt]
4.\;& \lim_{x \to 0} \frac{e^x - 1}{x} 
& \qquad 9.\;& \lim_{x \to 0} \frac{\tan x - x}{x^3} \\[6pt]
5.\;& \lim_{x \to \infty} \frac{x}{e^x} 
& \qquad 10.\;& \lim_{x \to 0} \frac{\ln(1+x)}{x}
\end{aligned}
$$


---
## 3. La Integral Indefinida

### **1. Función Primitiva (Antiderivada)**

Una función $F(x)$ es una **primitiva** o **antiderivada** de $f(x)$ si se cumple que $F'(x) = f(x)$. Por ejemplo, $F(x) = x^3$ es una primitiva de $f(x) = 3x^2$.

La **integral indefinida** de una función $f(x)$, denotada como $\int f(x) dx$, es el conjunto de **todas** sus primitivas. Como la derivada de una constante es cero, si $F(x)$ es una primitiva, también lo es $F(x)+C$ para cualquier constante $C$.
$$\int f(x) dx = F(x) + C$$
Donde $C$ es la **constante de integración**.

### **2. Métodos Básicos de Integración**

* **Integrales Inmediatas:** Se resuelven directamente a partir de la tabla de derivadas (leída "al revés").
    * $\int x^n dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$
    * $\int \frac{1}{x} dx = \ln|x| + C$
    * $\int e^x dx = e^x + C$
    * $\int \cos(x) dx = \sin(x) + C$
- Inmediatas avanzadas: con regla cadena
* **Integración por Sustitución (Cambio de Variable):** Se utiliza para simplificar el integrando. Se basa en la regla de la cadena.
    $$\int f(g(x))g'(x) dx = \int f(u) du, \quad \text{con } u=g(x)$$
* **Integración por Partes:** Se usa para integrar productos de funciones. Se basa en la regla del producto.
    $$\int u \, dv = u \cdot v - \int v \, du$$
    Un truco para elegir $u$: **LIATE** (Logarítmicas, Inversas, Algebraicas, Trigonométricas, Exponenciales).

### 3. Integración de Funciones Racionales (casos sencillos)

Una función racional es un cociente de polinomios:
$$
R(x) = \frac{P(x)}{Q(x)}
$$

Para integrarla, primero se intenta descomponerla en **fracciones parciales** siempre que:

* El grado del numerador sea menor que el del denominador (si no, primero se divide).
* El denominador se pueda factorizar.

Según el tipo de factores del denominador, distinguimos:

* **Raíces reales simples**
  $$
  \frac{P(x)}{(x-a)(x-b)} \Rightarrow \frac{A}{x-a} + \frac{B}{x-b}
  $$

* **Raíces reales múltiples**
  $$
  \frac{P(x)}{(x-a)^n} \Rightarrow \frac{A_1}{x-a} + \frac{A_2}{(x-a)^2} + \cdots + \frac{A_n}{(x-a)^n}
  $$

* **Raíces cuadráticas irreducibles (complejas)** — [[01 Calculo-Naut/apuntes/calc-naut-tema01\|Tema 1]]
  $$
  \frac{Ax+B}{x^2+a^2} \Rightarrow 
  A\frac{x}{x^2+a^2} + B\frac{1}{x^2+a^2}
  $$
  El primer término se integra mediante logaritmo y el segundo mediante arctangente.

---

### Ejemplo 1: Raíces simples
$$
\int \frac{3x+1}{x^2-x} \,dx
$$

Factorizamos:
$$
x^2-x = x(x-1)
$$

Descomposición:
$$
\frac{3x+1}{x(x-1)} = \frac{1}{x} + \frac{2}{x-1}
$$

Integración:
$$
\int \left(\frac{1}{x} + \frac{2}{x-1}\right)dx
= \ln|x| + 2\ln|x-1| + C
$$

---

### Ejemplo 2: Raíz doble
$$
\int \frac{2x+1}{x^2}dx
$$

Descomposición:
$$
\frac{2x+1}{x^2} = \frac{2}{x} + \frac{1}{x^2}
$$

Integración:
$$
2\ln|x| - \frac{1}{x} + C
$$

---

### Ejemplo 3: Denominador cuadrático irreducible (arctangente)
$$
\int \frac{1}{x^2+4} dx
$$

Usamos:
$$
\int \frac{1}{x^2+a^2}dx = \frac{1}{a}\arctan\left(\frac{x}{a}\right) + C
$$

Entonces:
$$
\frac{1}{2}\arctan\left(\frac{x}{2}\right) + C
$$

---

## 4. La Integral Definida y sus Aplicaciones

### **1. Integral de Riemann (Definida)**

La **integral definida** de una función $f(x)$ en un intervalo $[a, b]$, denotada como $\int_{a}^{b} f(x) dx$, representa el **área neta** entre la gráfica de la función y el eje x. Se define como el límite de una suma de áreas de rectángulos (Suma de Riemann).



### **2. Teorema Fundamental del Cálculo**

Este teorema es el pilar que conecta el cálculo diferencial y el integral. Establece que la derivación y la integración son operaciones inversas.

### **3. Regla de Barrow**

Es la consecuencia práctica del Teorema Fundamental del Cálculo y nos permite calcular integrales definidas de forma sencilla. Si $F(x)$ es cualquier primitiva de $f(x)$, entonces:
$$\int_{a}^{b} f(x) dx = [F(x)]_{a}^{b} = F(b) - F(a)$$

**Ejemplo:** Calcular el área bajo la curva $y=x^2$ desde $x=0$ hasta $x=2$.
El área viene dada por la integral definida:
$$A = \int_{0}^{2} x^2 dx$$
1.  Encontramos una primitiva de $x^2$: $F(x) = \frac{x^3}{3}$.
2.  Aplicamos la Regla de Barrow:
$$A = \left[ \frac{x^3}{3} \right]_{0}^{2} = \frac{2^3}{3} - \frac{0^3}{3} = \frac{8}{3} - 0 = \frac{8}{3}$$
El área es $\frac{8}{3}$ unidades cuadradas.


[[01 Calculo-Naut/apuntes/calc-naut-tema02-ej\|Ejercicios]]

