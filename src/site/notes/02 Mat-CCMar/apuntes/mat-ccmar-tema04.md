---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema04/","created":"2026-10-05T16:38:29.650+02:00","updated":"2026-10-05T16:30:21.000+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 4: Cálculo Diferencial en una Variable

## 1. Límite y Continuidad de Funciones

**Concepto de límite y tipos de funciones.** Las funciones de una variable real asignan a cada valor del dominio un único valor de salida. Según sus expresiones algebraicas y analíticas, las funciones elementales se clasifican en:

- **Polinómicas**: $f(x) = x^5 - 3x + 1$
- **Racionales**: $f(x) = \frac{x^2+1}{x-2}$
- **Trigonométricas**: $f(x) = \operatorname{sen}(x)$
- **Irracionales**: $f(x) = \sqrt[3]{x^2-1}$
- **Exponenciales**: $f(x) = e^x$, $f(x) = 3^x$
- **Logarítmicas**: $f(x) = \ln(x)$, $g(x) = \log(x)$

### 1.1. Composición de Funciones y Definición de Límite

**Composición de funciones.** Las funciones elementales pueden combinarse mediante operaciones algebraicas y composición (encadenar funciones donde la salida de una es la entrada de la otra, por ejemplo, $x \mapsto x^2 \mapsto \operatorname{sen}(x^2)$).

**Definición de Límite.** Llamamos **límite de una función** $f$ en $x_0$ al valor $L$ al que se acerca $f(x)$ cuando $x$ se acerca a $x_0$:

$$\lim_{x \to x_0} f(x) = L$$

### 1.2. Teorema de Bolzano

**Teorema de Bolzano (Existencia de raíces).** Sea $f: [a,b] \to \mathbb{R}$ una función continua en el intervalo cerrado $[a, b]$. Si $f(a)$ y $f(b)$ tienen signos contrarios (es decir, $f(a) \cdot f(b) < 0$), entonces la ecuación $f(x) = 0$ tiene al menos una solución dentro del intervalo abierto $(a, b)$:

$$\exists \, c \in (a, b) \quad \text{tal que} \quad f(c) = 0$$

---

## 2. La Derivada

**Concepto de derivada.** La derivada de una función en un punto mide la tasa de cambio instantánea o la pendiente de la recta tangente a la curva en dicho punto.

**Definición formal.** Dada una función $f(x)$ definida en un entorno de $x_0$, su derivada en $x_0$, denotada $f'(x_0)$, se define mediante el límite del cociente incremental:

$$f'(x_0) = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}$$

**Interpretación geométrica.** Geométricamente, la derivada representa la **inclinación** de la recta tangente a la gráfica de $f$ en el punto $(x_0, f(x_0))$.

---

### 2.1. Estudio de Funciones y Extremos Relativos

**Análisis de extremos locales.** Para encontrar los máximos y mínimos locales de una función $f(x)$:

1. Obtener la primera derivada $f'(x)$ e igualar a cero para hallar los **puntos críticos**.
2. Analizar el signo de $f'(x)$ en los intervalos delimitados por los puntos críticos:
   - Si $f'(x) > 0$, la función es creciente ($\nearrow$).
   - Si $f'(x) < 0$, la función es decreciente ($\searrow$).
   - Un cambio de $+ \to -$ indica un **máximo local**; un cambio de $- \to +$ indica un **mínimo local**.

> [!example] Ejemplo 4.1: Estudio Completo de Extremos Relativos
> **Enunciado:** Hallar los extremos de la función $f(x) = x^3 - 5x^2 + 3x + 1$ y estudiar la existencia de extremos absolutos.
>
> **Paso 1: Cálculo de la derivada y puntos críticos**
> $$f'(x) = 3x^2 - 10x + 3$$
> Igualando a cero mediante la fórmula de la ecuación de segundo grado:
> $$x = \frac{10 \pm \sqrt{(-10)^2 - 4(3)(3)}}{2(3)} = \frac{10 \pm \sqrt{100 - 36}}{6} = \frac{10 \pm 8}{6} \implies \begin{cases} x_1 = 3 \\ x_2 = \frac{1}{3} \end{cases}$$
>
> **Paso 2: Tabla de signos de la derivada e intervalos**
>
> | Intervalo | $x < \frac{1}{3}$ | $x = \frac{1}{3}$ | $\frac{1}{3} < x < 3$ | $x = 3$ | $x > 3$ |
> | :--- | :---: | :---: | :---: | :---: | :---: |
> | **Signo de $f'(x)$** | $+$ | $0$ | $-$ | $0$ | $+$ |
> | **Comportamiento $f(x)$** | Creciente ($\nearrow$) | **Máximo local** | Decreciente ($\searrow$) | **Mínimo local** | Creciente ($\nearrow$) |
>
> **Paso 3: Evaluación de los puntos y estudio global**
>
> - **Máximo local:** En $x = \frac{1}{3}$, $f\left(\frac{1}{3}\right) = \left(\frac{1}{3}\right)^3 - 5\left(\frac{1}{3}\right)^2 + 3\left(\frac{1}{3}\right) + 1 = \frac{146}{27}$. Punto: $\left(\frac{1}{3}, \frac{146}{27}\right)$.
> - **Mínimo local:** En $x = 3$, $f(3) = 3^3 - 5(3)^2 + 3(3) + 1 = -8$. Punto: $(3, -8)$.
> - **Límites en el infinito:**
>   $$\lim_{x \to -\infty} f(x) = -\infty, \qquad \lim_{x \to \infty} f(x) = \infty$$
>
> **Conclusión:** La función posee un máximo local en $\left(\frac{1}{3}, \frac{146}{27}\right)$ y un mínimo local en $(3, -8)$. Puesto que los límites en el infinito divergen a $-\infty$ y $+\infty$, la función **no posee extremos absolutos**.

### 2.2. Optimización

**Problemas de optimización.** Consisten en determinar los valores de las variables que maximizan o minimizan una función objetivo sujeta a ciertas restricciones geométricas o físicas.

> [!example] Ejemplo 4.2: Minimización del Superficie de una Lata Cilíndrica
> **Enunciado:** Se desea fabricar latas de refresco de volumen fijo $V = 0.33 \text{ L} = 0.33 \text{ dm}^3$. Minimizar el gasto de aluminio hallando el radio $r$ y la altura $h$ que minimizan la superficie total.
>
> **Desarrollo algebraico:**
>
> 1. **Relación del volumen:**
>    $$V = \pi r^2 h = 0.33 \implies h = \frac{0.33}{\pi r^2}$$
> 2. **Función objetivo (área total):**
>    $$f(r, h) = 2\pi r^2 + 2\pi r h$$
>    Sustituyendo $h$:
>    $$f(r) = 2\pi r^2 + 2\pi r \left(\frac{0.33}{\pi r^2}\right) = 2\pi r^2 + \frac{0.66}{r}$$
> 3. **Punto crítico:**
>    $$f'(r) = 4\pi r - \frac{0.66}{r^2} = 0 \implies 4\pi r^3 = 0.66 \implies r^3 = \frac{0.66}{4\pi} \approx 0.0525 \implies r \approx 0.37 \text{ dm}$$
> 4. **Cálculo de la altura $h$:**
>    $$h = \frac{0.33}{\pi (0.37)^2} \approx 0.76 \text{ dm}$$
>
> **Conclusión:** Las dimensiones óptimas para minimizar la cantidad de aluminio son un radio $r \approx 0.37 \text{ dm}$ y una altura $h \approx 0.76 \text{ dm}$.

---

## 3. Polinomio de Taylor

### 3.1. Recta Tangente y Aproximación Polinómica

**Recta tangente.** La recta tangente a la gráfica de $f(x)$ en el punto $x = a$ es la mejor aproximación lineal (grado 1) a la función cerca de $a$:

$$y = f(a) + f'(a)(x-a)$$

**Polinomio de Taylor.** El polinomio de Taylor generaliza la idea de la recta tangente. Dada una función $f$ derivable en $a$, su polinomio de Taylor de grado $n$ en $a$ es el polinomio de grado $n$ que mejor aproxima a $f$ "cerca de $a$":

$$P_{n,a}(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \dots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$

Expresado de forma compacta mediante sumatorio:

$$P_{n,a}(x) = \sum_{k=0}^{n} \frac{f^{(k)}(a)}{k!} (x-a)^k$$

donde $n! = n \cdot (n-1) \cdot (n-2) \cdots 1$ representa el factorial de $n$.

**Polinomio de Maclaurin.** Cuando el centro de desarrollo es $a = 0$, el polinomio de Taylor recibe el nombre de **polinomio de Maclaurin**:

$$P_{n,0}(x) = \sum_{k=0}^{n} \frac{f^{(k)}(0)}{k!} x^k$$