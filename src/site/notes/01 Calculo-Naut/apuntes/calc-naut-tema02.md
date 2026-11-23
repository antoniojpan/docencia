---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema02/","created":"2026-11-23T07:46:42.133+01:00","updated":"2026-11-23T07:46:30.041+01:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|Volver al índice]]

# **TEMA 2: Cálculo diferencial e integral en una variable**

- [[01 Calculo-Naut/apuntes/calc-naut-tema02#1. Funciones, Límites y Continuidad\|1. Funciones, Límites y Continuidad]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema02#2. Concepto de Derivada\|2. Concepto de Derivada]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema02#2.3. Aproximación de funciones: polinomios de Taylor\|2.3. Aproximación de funciones: polinomios de Taylor]]
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


### **2.3. Aproximación de funciones: polinomios de Taylor**

La recta tangente aproxima una función cerca de un punto $a$ usando su valor y su pendiente:
$$y(x)=f(a)+f'(a)(x-a).$$
Esta aproximación es exacta en $a$ y suele ser útil para valores próximos a él. Podemos mejorarla incorporando información sobre cómo cambia la pendiente, es decir, sobre la curvatura de la función.

Si $f$ tiene derivadas hasta orden $n$ en un entorno de $a$, su **polinomio de Taylor de orden $n$** alrededor de $a$ es
$$P_n(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2!}(x-a)^2+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^n.$$
Los primeros órdenes muestran la idea:
$$P_0(x)=f(a),\qquad P_1(x)=y(x),\qquad P_2(x)=y(x)+\frac{f''(a)}{2}(x-a)^2.$$
Así, el término cuadrático corrige la aproximación lineal teniendo en cuenta la curvatura; los términos siguientes incorporan información adicional sobre la variación de la función. Cerca de $a$, se usa $P_n(x)$ como aproximación de $f(x)$:
$$f(x)\approx P_n(x).$$

El error es el resto $R_n(x)=f(x)-P_n(x)$. Si $f$ tiene derivada de orden $n+1$ continua entre $a$ y $x$, el teorema de Taylor garantiza que, para algún $\xi$ entre ambos puntos,
$$R_n(x)=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-a)^{n+1}.$$
En particular, si $|f^{(n+1)}(t)|\le M$ en ese intervalo, entonces
$$|R_n(x)|\le \frac{M}{(n+1)!}|x-a|^{n+1}.$$
La fórmula permite controlar el error cuando se conoce una cota para la derivada correspondiente.

**Ejemplo.** Aproximar $\sqrt{4.1}$ mediante la recta tangente y mediante el polinomio de Taylor de orden 2 de $f(x)=\sqrt{x}$ alrededor de $a=4$.

Como $f(4)=2$ y $f'(4)=\frac14$, la aproximación por la recta tangente es
$$y(x)=2+\frac14(x-4),\qquad y(4.1)=2.025.$$
Además, $f''(x)=-\frac{1}{4x^{3/2}}$, por lo que $f''(4)=-\frac1{32}$. El término cuadrático da
$$P_2(x)=2+\frac14(x-4)-\frac1{64}(x-4)^2,$$
$$P_2(4.1)=2.02484375.$$
El valor es aproximadamente $\sqrt{4.1}\approx2.02485$: en este caso, añadir la corrección cuadrática mejora la aproximación de la tangente.

Cuando el punto de desarrollo es $a=0$, el polinomio se llama **polinomio de Maclaurin**. Por ejemplo, para $e^x$:
$$P_3(x)=1+x+\frac{x^2}{2}+\frac{x^3}{6},$$
que proporciona una aproximación de $e^x$ para valores de $x$ próximos a $0$.



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

### 1. Introducción
Queremos calcular la **masa total de un alambre sin pesarlo**, conociendo únicamente su densidad. La densidad lineal se mide en kilogramos por metro ($\mathrm{kg/m}$): si vale $2\,\mathrm{kg/m}$, cada metro de alambre tiene una masa de $2\,\mathrm{kg}$.

**Etapa 1. Un alambre con densidad constante**

Un alambre mide $5\,\mathrm{m}$ y tiene una densidad de $2\,\mathrm{kg/m}$ en todos sus puntos. Cada metro aporta $2\,\mathrm{kg}$, de modo que
$$M=5\,\mathrm{m}\cdot 2\,\mathrm{kg/m}=10\,\mathrm{kg}.$$
Aquí basta una multiplicación: $\text{masa total}=\text{longitud}\times\text{densidad}$.

**Etapa 2. Un alambre con tres densidades**

Ahora el alambre mide $6\,\mathrm{m}$ y está formado por tres tramos de $2\,\mathrm{m}$ cada uno. Ya no podemos multiplicar por una única densidad, así que calculamos la masa de cada tramo por separado:

- Primer tramo: $2\,\mathrm{m}\cdot 2\,\mathrm{kg/m}=4\,\mathrm{kg}$.
- Segundo tramo: $2\,\mathrm{m}\cdot 5\,\mathrm{kg/m}=10\,\mathrm{kg}$.
- Tercer tramo: $2\,\mathrm{m}\cdot 1\,\mathrm{kg/m}=2\,\mathrm{kg}$.

Después sumamos las tres masas:
$$M=4+10+2=16\,\mathrm{kg}.$$
La estrategia ha pasado de hacer **una multiplicación** a hacer **una suma de multiplicaciones**.

**Etapa 3. Una densidad que cambia en cada punto**

Consideremos ahora un alambre de $4\,\mathrm{m}$. A una distancia $x$ del extremo izquierdo, su densidad es $\rho(x)=x^3-6x^2+9x+2$, medida en $\mathrm{kg/m}$. Al principio vale $2\,\mathrm{kg/m}$; al cabo de $1\,\mathrm{m}$ ha subido a $6\,\mathrm{kg/m}$, a los $2\,\mathrm{m}$ ha bajado a $4\,\mathrm{kg/m}$, a los $3\,\mathrm{m}$ vale $2\,\mathrm{kg/m}$ y al final vuelve a subir a $6\,\mathrm{kg/m}$.

No hay una única densidad que podamos multiplicar por $4\,\mathrm{m}$. Repetimos la estrategia anterior: dividimos el alambre en trozos tan pequeños que, dentro de cada uno, la densidad apenas cambia. En el dibujo, cada trozo da lugar a un rectángulo estrecho cuya área aproxima su masa. Con más rectángulos y más estrechos, la suma de sus áreas se aproxima mejor a la masa total; al pasar al límite obtenemos una **integral definida**.

Un trocito de longitud $dx$ situado en la posición $x$ tiene una masa aproximada de $\rho(x)\,dx$. La integral suma las aportaciones de todos esos trocitos desde $x=0$ hasta $x=4$:
$$M=\int_0^4\left(x^3-6x^2+9x+2\right)\,dx.$$
Dejamos el cálculo indicado: ahora lo importante es entender **qué está sumando** la integral.

![integral-definida-alambre-densidad.png\|1100](/img/user/imagenes/integral-definida-alambre-densidad.png)

**¿Por qué aparece un área?** En el dibujo, la longitud se representa en horizontal y la densidad en vertical. Por tanto,
$$\text{longitud}\times\text{densidad}=\text{base}\times\text{altura}=\text{área}.$$
En la primera etapa hay un solo rectángulo; en la segunda, sumamos tres rectángulos; en la tercera, sumamos muchos rectángulos estrechos y después hacemos tender su anchura a cero. Aunque lo representamos como un área, sus unidades son $\mathrm{m}\cdot(\mathrm{kg/m})=\mathrm{kg}$ y, por eso, sigue representando una masa.

**La idea general.** Para un alambre situado entre $x=a$ y $x=b$, con densidad $\rho(x)$, procedemos igual: lo dividimos en trozos de longitudes $\Delta x_i$, elegimos un punto $x_i^*$ en cada trozo y aproximamos su masa por $\rho(x_i^*)\Delta x_i$. Al refinar la división obtenemos
$$M=\lim_{\max \Delta x_i\to 0}\sum_{i=1}^{n}\rho(x_i^*)\Delta x_i=\int_a^b\rho(x)\,dx.$$
La integral definida es, por tanto, una manera de **sumar las aportaciones de una cantidad que cambia de punto a punto**.

**Otros ejemplos en náutica**

- **Distancia recorrida.** Si la corredera indica una velocidad variable $v(t)$, la distancia es $d=\int_{t_1}^{t_2}v(t)\,dt$: sumamos las distancias recorridas en pequeños intervalos de tiempo.
- **Combustible consumido.** Si $c(t)$ es el consumo instantáneo en $\mathrm{L/h}$, el total gastado es $C=\int_{t_1}^{t_2}c(t)\,dt$. Esto permite estimar el combustible necesario y la autonomía de la embarcación.
- **Volumen de desplazamiento.** Si $A_s(x)$ es el área sumergida de cada sección del casco, $V=\int_0^L A_s(x)\,dx$ suma los volúmenes de finas rodajas a lo largo de la eslora. Multiplicando $V$ por $\rho_{\text{agua}}$ obtenemos la masa de agua desplazada.

**Integral de Riemann**

La **integral definida** de una función $f(x)$ en un intervalo $[a, b]$, denotada como $\int_{a}^{b} f(x) dx$, representa el **área neta** entre la gráfica de la función y el eje x. Se define como el límite de una suma de áreas de rectángulos (Suma de Riemann).


**Teorema Fundamental del Cálculo**

Este teorema es el pilar que conecta el cálculo diferencial y el integral. Establece que la derivación y la integración son operaciones inversas.

**Regla de Barrow**

Es la consecuencia práctica del Teorema Fundamental del Cálculo y nos permite calcular integrales definidas de forma sencilla. Si $F(x)$ es cualquier primitiva de $f(x)$, entonces:
$$\int_{a}^{b} f(x) dx = [F(x)]_{a}^{b} = F(b) - F(a)$$

**Ejemplo:** Calcular el área bajo la curva $y=x^2$ desde $x=0$ hasta $x=2$.
El área viene dada por la integral definida:
$$A = \int_{0}^{2} x^2 dx$$
1.  Encontramos una primitiva de $x^2$: $F(x) = \frac{x^3}{3}$.
2.  Aplicamos la Regla de Barrow:
$$A = \left[ \frac{x^3}{3} \right]_{0}^{2} = \frac{2^3}{3} - \frac{0^3}{3} = \frac{8}{3} - 0 = \frac{8}{3}$$
El área es $\frac{8}{3}$ unidades cuadradas.

### Área entre dos curvas

Cuando queremos el área **encerrada entre dos funciones** $f$ y $g$, primero hay que **hallar los cortes** de ambas curvas (resolver $f(x) = g(x)$): esos cortes son los límites de integración. Entre ellos, la función mayor es la que resta a la menor:
$$A = \int_{a}^{b} \bigl[f(x) - g(x)\bigr]\, dx$$
Si las curvas se cruzan dentro del intervalo, hay que **partir la integral en cada trozo** y comprobar en cada uno cuál va por encima.

---

### Ejemplo 4: Área entre una parábola y una recta

Calcular el área encerrada por $y = x^2$ e $y = 2x + 3$.

**1. Cortes de las dos funciones:**
$$x^2 = 2x + 3 \;\Longrightarrow\; x^2 - 2x - 3 = 0 \;\Longrightarrow\; (x-3)(x+1) = 0$$
$$x = -1, \quad x = 3$$
Los cortes son $(-1, 1)$ y $(3, 9)$.

**2. ¿Quién va arriba?** Probamos un punto intermedio, $x = 0$: $2\cdot 0 + 3 = 3 > 0 = 0^2$. La recta está por encima de la parábola en todo el intervalo $[-1, 3]$.

**3. Integral:**
$$A = \int_{-1}^{3} \bigl[(2x+3) - x^2\bigr]\, dx = \left[ x^2 + 3x - \frac{x^3}{3} \right]_{-1}^{3}$$
$$A = \left(9 + 9 - 9\right) - \left(1 - 3 + \frac{1}{3}\right) = 9 - \left(-\frac{5}{3}\right) = \frac{32}{3}$$

---

### Ejemplo 5: Área entre dos curvas que se cruzan (partir la integral)

Calcular el área encerrada por $y = \sin x$ e $y = \cos x$ en $[0, \pi]$.

**1. Cortes de las dos funciones:**
$$\sin x = \cos x \;\Longrightarrow\; \tan x = 1 \;\Longrightarrow\; x = \frac{\pi}{4} \quad \text{en } [0,\pi]$$

**2. ¿Quién va arriba?**
* En $\left[0, \frac{\pi}{4}\right]$: $\cos x \ge \sin x$ (p. ej. en $x=0$: $1 > 0$).
* En $\left[\frac{\pi}{4}, \pi\right]$: $\sin x \ge \cos x$ (p. ej. en $x=\pi$: $0 > -1$).

Como el orden cambia en el corte, **partimos la integral en dos**:
$$A = \int_{0}^{\pi/4} (\cos x - \sin x)\, dx \;+\; \int_{\pi/4}^{\pi} (\sin x - \cos x)\, dx$$

**3. Cálculo:**
$$\int_{0}^{\pi/4} (\cos x - \sin x)\, dx = \Bigl[\sin x + \cos x\Bigr]_{0}^{\pi/4} = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} - (0 + 1) = \sqrt{2} - 1$$
$$\int_{\pi/4}^{\pi} (\sin x - \cos x)\, dx = \Bigl[-\cos x - \sin x\Bigr]_{\pi/4}^{\pi} = (1 - 0) - \left(-\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2}\right) = 1 + \sqrt{2}$$
$$A = (\sqrt{2} - 1) + (1 + \sqrt{2}) = 2\sqrt{2}$$

---

[[01 Calculo-Naut/apuntes/calc-naut-tema02-ej\|Ejercicios]]

