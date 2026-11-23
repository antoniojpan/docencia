---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema06/","created":"2026-11-23T07:57:12.178+01:00","updated":"2026-11-23T09:40:39.811+01:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 6: Cálculo Integral

## 1. La Antiderivada e Integrales Inmediatas

### 1.1. Concepto de Primitiva e Integral Indefinida

La **integración** es la operación inversa de la derivación. Dada una función $f(x)$, buscamos una función $F(x)$ (llamada **primitiva** o **antiderivada**) tal que su derivada sea la función original:

$$F'(x) = f(x)$$

Puesto que la derivada de cualquier constante $K \in \mathbb{R}$ es cero, la **integral indefinida** representa a toda la familia de primitivas de $f(x)$ y se denota mediante:

$$\int f(x) \, dx = F(x) + K$$

### 1.2. Tabla de Integrales Inmediatas y Funciones Compuestas

A partir de las reglas de derivación elementales se obtiene la tabla de integrales inmediatas:

- **Potencias:** $\int x^n \, dx = \frac{x^{n+1}}{n+1} + K \quad (n \neq -1)$
- **Tipo logarítmico:** $\int \frac{1}{x} \, dx = \ln|x| + K \quad \text{o en general } \int \frac{f'(x)}{f(x)} \, dx = \ln|f(x)| + K$
- **Exponenciales:** $\int e^x \, dx = e^x + K$
- **Trigonométricas:** $\int \operatorname{sen} x \, dx = -\cos x + K, \qquad \int \cos x \, dx = \operatorname{sen} x + K$

> [!example] Ejemplo 1.1: Integrales Inmediatas
> Calcula las siguientes primitivas inmediatas:
>
> 1. $\int 3x^2 \, dx = x^3 + K$
> 2. $\int \sqrt{x} \, dx = \int x^{1/2} \, dx = \frac{2}{3}x^{3/2} + K = \frac{2}{3}\sqrt{x^3} + K$
> 3. $\int \frac{1}{x^2} \, dx = \int x^{-2} \, dx = -x^{-1} + K = -\frac{1}{x} + K$
> 4. $\int \frac{1}{(x-2)^3} \, dx = \int (x-2)^{-3} \, dx = \frac{(x-2)^{-2}}{-2} + K = -\frac{1}{2(x-2)^2} + K$
> 5. $\int \frac{5}{(1-x)^3} \, dx = 5 \int (1-x)^{-3} \, dx = \frac{5}{4(1-x)^4} + K$

---

## 2. Métodos de Integración

### 2.1. Cambio de Variable (Sustitución)

El método de **cambio de variable** consiste en realizar una sustitución $t = g(x)$ para transformar la integral en otra más sencilla respecto a la variable $t$, utilizando el diferencial $dt = g'(x) \, dx$:

$$\int f(g(x)) g'(x) \, dx = \int f(t) \, dt$$

> [!example] Ejemplo 2.1: Integración por Cambio de Variable
> Calcula $\int x \operatorname{sen}(x^2) \, dx$.
>
> **Solución:**
> Hacemos la sustitución $t = x^2 \implies dt = 2x \, dx \implies x \, dx = \frac{1}{2} dt$:
>
> $$\int x \operatorname{sen}(x^2) \, dx = \int \operatorname{sen}(t) \cdot \frac{1}{2} dt = \frac{1}{2} (-\cos t) + K = -\frac{1}{2}\cos(x^2) + K$$

> [!example] Ejemplo 2.2: Cambio de Variable con Raíces y Logaritmos
> 1. $\int \frac{\cos x}{\operatorname{sen} x + 2} \, dx$: Con $t = \operatorname{sen} x + 2 \implies dt = \cos x \, dx$, se tiene:
>    $$\int \frac{dt}{t} = \ln|t| + K = \ln(\operatorname{sen} x + 2) + K$$
> 2. $\int \frac{1}{\sqrt{x}} \operatorname{sen}(\sqrt{x}) \, dx$: Con $t = \sqrt{x} \implies dt = \frac{1}{2\sqrt{x}} \, dx \implies \frac{dx}{\sqrt{x}} = 2dt$:
>    $$2 \int \operatorname{sen} t \, dt = -2 \cos t + K = -2 \cos(\sqrt{x}) + K$$

### 2.2. Integración por Partes (Regla "ALPES")

El método de **integración por partes** se deriva de la regla del producto de derivadas y sigue la fórmula:

$$\int u \, dv = u \cdot v - \int v \, du$$

Para elegir la función $u$, se emplea la regla nemotécnica **ALPES** (prioridad de arriba a abajo):

1. **A:** Arcotangente / Arcoseno (funciones trigonométricas inversas)
2. **L:** Logaritmos
3. **P:** Polinomios / Potencias de $x$
4. **E:** Exponenciales
5. **S:** Seno / Coseno

> [!example] Ejemplo 2.3: Integración por Partes
> Calcula $\int x \operatorname{sen} x \, dx$.
>
> **Solución:**
> Siguiendo **ALPES**, elegimos el polinomio para $u$:
>
> - $u = x \implies du = dx$
> - $dv = \operatorname{sen} x \, dx \implies v = -\cos x$
>
> Aplicando la fórmula:
>
> $$\int x \operatorname{sen} x \, dx = x (-\cos x) - \int (-\cos x) \, dx = -x \cos x + \operatorname{sen} x + K$$

### 2.3. Integrales Racionales (Fracciones Simples)

Para integrar cocientes de polinomios $\int \frac{P(x)}{Q(x)} \, dx$:

1. **Si $\operatorname{grado}(P) \ge \operatorname{grado}(Q)$:** Se realiza primero la división polinómica para obtener $\frac{P(x)}{Q(x)} = C(x) + \frac{R(x)}{Q(x)}$, donde $C(x)$ es el cociente y $R(x)$ el resto con $\operatorname{grado}(R) < \operatorname{grado}(Q)$.
2. **Si $\operatorname{grado}(P) < \operatorname{grado}(Q)$:** Se factoriza el denominador $Q(x)$ y se descompone la fracción en **fracciones simples**:
   - Raíces reales simples: $\frac{A}{x - x_1} + \frac{B}{x - x_2}$
   - Raíces reales múltiples de orden $k$: $\frac{A}{x - x_1} + \frac{B}{(x - x_1)^2} + \dots + \frac{K}{(x - x_1)^k}$

> [!example] Ejemplo 2.4: Integración Racional
> Calcula $\int \frac{x^3 + 2}{x^2 - 1} \, dx$.
>
> **Solución:**
> Como el grado del numerador (3) es mayor que el del denominador (2), dividimos $x^3 + 2$ entre $x^2 - 1$:
> $$x^3 + 2 = x(x^2 - 1) + (x + 2) \implies \frac{x^3 + 2}{x^2 - 1} = x + \frac{x + 2}{x^2 - 1}$$
>
> Descomponemos $\frac{x+2}{(x-1)(x+1)}$ en fracciones simples:
> $$\frac{x+2}{(x-1)(x+1)} = \frac{A}{x+1} + \frac{B}{x-1} \implies x + 2 = A(x-1) + B(x+1)$$
>
> - Para $x = 1 \implies 3 = 2B \implies B = \frac{3}{2}$
> - Para $x = -1 \implies 1 = -2A \implies A = -\frac{1}{2}$
>
> Integrando cada término:
>
> $$\int \frac{x^3 + 2}{x^2 - 1} \, dx = \int x \, dx - \frac{1}{2} \int \frac{1}{x+1} \, dx + \frac{3}{2} \int \frac{1}{x-1} \, dx = \frac{x^2}{2} - \frac{1}{2}\ln|x+1| + \frac{3}{2}\ln|x-1| + K$$

---

## 3. Integral Definida y Aplicaciones

### 3.1. Introducción

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

**Otros ejemplos en ciencias del mar**

- **Agua intercambiada por una marea.** Si $Q(t)$ es el caudal que entra en una bahía durante la creciente, $V=\int_{t_1}^{t_2}Q(t)\,dt$ es el volumen total incorporado. Este cálculo ayuda a estudiar la renovación del agua.
- **Distancia recorrida por un pez marcado.** En un seguimiento por telemetría, si se estima la velocidad $v(t)$ de un pez equipado con un transmisor, la distancia total recorrida es $d=\int_{t_1}^{t_2}v(t)\,dt$: sumamos los pequeños desplazamientos para estudiar sus movimientos y migraciones.
- **Producción de fitoplancton en la columna de agua.** Si $P(z)$ es la producción por unidad de volumen a profundidad $z$, $P_{\text{columna}}=\int_0^H P(z)\,dz$ suma la producción de todas las capas. Como la luz cambia con la profundidad, no basta medir una sola capa.

**DEFINICIÓN: Integral definida (de Riemann)**

Como límite de las sumas de Riemann, la **integral definida** de una función $f(x)$ entre $x = a$ y $x = b$ representa el área neta comprendida entre la gráfica de $f(x)$, el eje $X$ y las rectas verticales $x = a$ y $x = b$:

$$\int_a^b f(x) \, dx$$

### 3.2. Regla de Barrow y Cálculo de Áreas

**Regla de Barrow:** Si $F(x)$ es una primitiva continua de $f(x)$ en $[a, b]$, entonces:

$$\int_a^b f(x) \, dx = [F(x)]_a^b = F(b) - F(a)$$

> [!example] Ejemplo 3.1: Área Bajo la Exponencial
> Calcula el área encerrada por $f(x) = e^x$ entre $x = 0$ y $x = 5$.
>
> **Solución:**
> $$A = \int_0^5 e^x \, dx = [e^x]_0^5 = e^5 - e^0 = e^5 - 1 \approx 147.41 \text{ u}^2$$

### 3.3. Cálculo de Áreas con Cambio de Signo

Cuando la función corta al eje $X$ dentro del intervalo $[a, b]$, el área física total se calcula sumando en valor absoluto las integrales de cada subintervalo:

> [!example] Ejemplo 3.2: Área con Cortes con el Eje X
> Calcular el área encerrada por $f(x) = x^3 - 8x^2 + 19x - 12$ y las rectas $x = -1$ y $x = 4$.
>
> **Solución:**
> Hallamos los puntos de corte con el eje $X$: $x^3 - 8x^2 + 19x - 12 = 0 \implies x = 1, \; x = 3, \; x = 4$.
> Estudiando el signo de $f(x)$ en los subintervalos:
>
> - En $[-1, 1]$, $f(x) \le 0 \implies A_1 = -\int_{-1}^1 f(x) \, dx = \frac{88}{3}$
> - En $[1, 3]$, $f(x) \ge 0 \implies A_2 = \int_1^3 f(x) \, dx = \frac{8}{3}$
> - En $[3, 4]$, $f(x) \le 0 \implies A_3 = -\int_3^4 f(x) \, dx = \frac{5}{12}$
>
> El área total es $A_T = A_1 + A_2 + A_3 = \frac{88}{3} + \frac{8}{3} + \frac{5}{12} = \frac{389}{12} \approx 32.42 \text{ u}^2$.

---

## 4. Integrales Múltiples (Integrales Dobles)

### 4.1. Teorema de Fubini en Rectángulos

Una **integral doble** extiende el concepto de integración a funciones de dos variables $f(x, y)$ sobre una región bidimensional $R \subset \mathbb{R}^2$:

$$\iint_R f(x, y) \, dA$$

Geométricamente, si $f(x, y) \ge 0$, la integral doble representa el **volumen** del sólido delimitado por la superficie $z = f(x, y)$ y la región del plano $R$.

**Teorema de Fubini:** Si $R = [a, b] \times [c, d]$ es un rectángulo en el plano, la integral doble se puede calcular mediante integrales reiteradas en cualquier orden:

$$\iint_R f(x, y) \, dA = \int_c^d \left[ \int_a^b f(x, y) \, dx \right] dy = \int_a^b \left[ \int_c^d f(x, y) \, dy \right] dx$$

> [!example] Ejemplo 4.1: Integral Doble en un Rectángulo
> Calcula $\iint_R xy \, dA$ sobre el rectángulo $R = [0, 3] \times [1, 5]$.
>
> **Solución:**
> $$\iint_R xy \, dA = \int_1^5 \left[ \int_0^3 xy \, dx \right] dy = \int_1^5 \left[ \frac{x^2 y}{2} \right]_0^3 dy = \int_1^5 \frac{9y}{2} \, dy = \frac{9}{2} \left[ \frac{y^2}{2} \right]_1^5 = \frac{9}{2} \left( \frac{25}{2} - \frac{1}{2} \right) = 54 \text{ u}^3$$

### 4.2. Integración sobre Regiones Generales

Si la región $R$ no es un rectángulo sino que está acotada por funciones de $x$: $R = \{ (x, y) \in \mathbb{R}^2 : a \le x \le b, \; g_1(x) \le y \le g_2(x) \}$, la integral doble adopta la forma:

$$\iint_R f(x, y) \, dA = \int_a^b \left[ \int_{g_1(x)}^{g_2(x)} f(x, y) \, dy \right] dx$$

> [!example] Ejemplo 4.2: Región General
> Calcula $\iint_R xy \, dy \, dx$ sobre la región $R = \{ 1 \le x \le 2, \; 0 \le y \le x \}$.
>
> **Solución:**
> $$\int_1^2 \left[ \int_0^x xy \, dy \right] dx = \int_1^2 \left[ \frac{x y^2}{2} \right]_0^x dx = \int_1^2 \frac{x^3}{2} \, dx = \left[ \frac{x^4}{8} \right]_1^2 = \frac{16}{8} - \frac{1}{8} = \frac{15}{8}$$

### 4.3. Aplicaciones de la Integral Doble

1. **Cálculo de Áreas Planas:** Si se toma $f(x, y) \equiv 1$, el volumen coincide numéricamente con el área del recinto:
   $$A = \iint_R 1 \, dA$$
2. **Cálculo de Volúmenes:** El volumen acotado entre una superficie superior $z_{\text{tapadera}} = f(x,y)$ y una inferior $z_{\text{suelo}} = g(x,y)$ viene dado por:
   $$V = \iint_R (f(x, y) - g(x, y)) \, dA$$
3. **Masa Total con Densidad Variable $d(x, y)$:** La masa de una lámina plana con densidad de masa por unidad de área $d(x, y)$ es:
   $$M = \iint_R d(x, y) \, dA$$