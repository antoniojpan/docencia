---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema05/","created":"2026-10-05T14:12:07.995+02:00","updated":"2026-10-05T14:12:05.000+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 5: Derivación en Varias Variables

## 1. Funciones de Varias Variables

### 1.1. Concepto y Tipos de Funciones

Las funciones de varias variables son transformaciones matemáticas que dependen de más de una entrada de datos y/o pueden devolver varios valores numéricos. Se clasifican según sus espacios de origen (dominio) y llegada (codominio):

- **Campos escalares ($f: \mathbb{R}^2 \to \mathbb{R}$):** Asignan un único valor numérico a un par de entradas $(x, y)$.
  - *Ejemplo real:* El coste total $f(x, y) = x \cdot y$ al comprar $x \text{ kg}$ de tomates a un precio de $y \text{ €/kg}$.
- **Curvas en el espacio ($\mathbf{g}: \mathbb{R} \to \mathbb{R}^2$):** Dependen de una única variable independiente (habitualmente el tiempo $t$) y devuelven una posición vectorial.
  - *Ejemplo real:* La latitud y longitud de un ciclista en función del tiempo: $t \mapsto (x(t), y(t))$.
- **Campos vectoriales en el plano ($\mathbf{f}: \mathbb{R}^2 \to \mathbb{R}^2$):** Asignan un vector de velocidad o fuerza a cada punto del plano.
  - *Ejemplo real:* La velocidad del viento $(u, v)$ en cada posición geográfica $(x, y)$.
- **Campos vectoriales en el espacio ($\mathbf{f}: \mathbb{R}^3 \to \mathbb{R}^3$):** Describen la velocidad o fuerza en un punto tridimensional.
  - *Ejemplo real:* La velocidad de una corriente de agua o aire $(u, v, w)$ en un punto espacial $(x, y, z)$.

### 1.2. Representación Gráfica y Curvas de Nivel

Para visualizar un campo escalar $f: \mathbb{R}^2 \to \mathbb{R}$, resulta muy útil emplear **curvas de nivel**. Una curva de nivel es el conjunto de puntos $(x, y)$ del plano donde la función toma un valor constante $c$:

$$f(x, y) = c$$

- **Isotermas:** Curvas de nivel donde la temperatura permanece constante.
- **Isobaras:** Curvas de nivel donde la presión atmosférica es constante.

---

## 2. Límites y Continuidad

El cálculo de límites en funciones de varias variables presenta una elevada complejidad al existir infinitos caminos de aproximación a un punto del plano o del espacio.

**Criterio de continuidad:** Una función de varias variables es continua en un punto si y solo si todas sus **funciones componentes** son continuas en dicho punto.

> [!example] Ejemplo 2.1: Continuidad por Componentes
> Estudiar la continuidad de la función vectorial $f(x, y) = (x^2 + y, \; x - y)$.
>
> **Solución:**
> Dado que las funciones componentes $f_1(x, y) = x^2 + y$ y $f_2(x, y) = x - y$ son polinomios de dos variables, son continuas en todo $\mathbb{R}^2$. Por tanto, la función vectorial $f(x, y)$ es continua en todo su dominio.

---

## 3. Derivadas Parciales

### 3.1. Definición e Interpretación

Hallar la **derivada parcial** de una función respecto a una variable consiste en derivar de la manera tradicional respecto a dicha variable, tratando a todas las demás variables como si fueran constantes.

- **Interpretación:** La derivada parcial de $f$ respecto a $x$ ($\frac{\partial f}{\partial x}$ o $f_x$) mide la tasa de variación o la influencia de la variable $x$ en el comportamiento global de $f$.

> [!example] Ejemplo 3.1: Derivadas Parciales en 3 Variables
> Dada la función $f(x, y, z) = \sqrt{x} + yz$, calcular sus derivadas parciales.
>
> **Solución:**
>
> - Respecto a $x$ (tratando $y, z$ como constantes):
>   $$\frac{\partial f}{\partial x} = \frac{1}{2\sqrt{x}}$$
> - Respecto a $y$ (tratando $x, z$ como constantes):
>   $$\frac{\partial f}{\partial y} = z$$
> - Respecto a $z$ (tratando $x, y$ como constantes):
>   $$\frac{\partial f}{\partial z} = y$$

> [!example] Ejemplo 3.2: Derivadas Parciales de un Cociente
> Calcular las derivadas parciales de $g(x, y) = \frac{x - y}{xy}$.
>
> **Solución:**
>
> - Respecto a $x$:
>   $$g_x = \frac{1 \cdot (xy) - (x - y) \cdot y}{(xy)^2} = \frac{xy - xy + y^2}{x^2 y^2} = \frac{y^2}{x^2 y^2} = \mathbf{\frac{1}{x^2}}$$
> - Respecto a $y$:
>   $$g_y = \frac{-1 \cdot (xy) - (x - y) \cdot x}{(xy)^2} = \frac{-xy - x^2 + xy}{x^2 y^2} = \frac{-x^2}{x^2 y^2} = \mathbf{-\frac{1}{y^2}}$$
>
> *Nota sobre la influencia:* Si $f(x, y, z) = y z^3 + 3$, se observa que $f_x = 0$, lo que indica que la variable $x$ no influye en absoluto en el valor de la función.

---

## 4. Gradiente y Derivada Direccional

### 4.1. El Vector Gradiente

Dado un campo escalar $f(x, y)$, el **gradiente** es un vector formado por las derivadas parciales primeras de la función en cada punto:

$$\nabla f = \left( \frac{\partial f}{\partial x}, \; \frac{\partial f}{\partial y} \right)$$

- **Propiedad fundamental:** El vector gradiente $\nabla f(x_0, y_0)$ apunta siempre en la **dirección de máximo crecimiento** de la función en ese punto, y su módulo representa la tasa máxima de aumento.

### 4.2. Derivada Direccional

Para calcular la variación o incremento de la función $f(x, y)$ en una dirección arbitraria dada por un vector $v = (a, b)$, se utiliza la **derivada direccional**:

$$D_v f = a \frac{\partial f}{\partial x} + b \frac{\partial f}{\partial y} = \nabla f \cdot v$$

- Si $D_v f = 0$, significa que el movimiento en la dirección $v$ se realiza a lo largo de una **curva de nivel** (sin cambio en el valor de la función).

> [!example] Ejemplo 4.1: Gradiente y Derivada Direccional
> Dada la función $f(x, y) = x^2 y + \sqrt{x}$:
>
> 1. **Calcular el gradiente $\nabla f$:**
>    $$\frac{\partial f}{\partial x} = 2yx + \frac{1}{2\sqrt{x}}, \qquad \frac{\partial f}{\partial y} = x^2$$
>    $$\nabla f = \left( 2yx + \frac{1}{2\sqrt{x}}, \; x^2 \right)$$
>
> 2. **Calcular la derivada direccional en el punto $(2, 1)$ según la dirección $v = (3, 5)$:**
>    $$D_{(3,5)} f(2, 1) = 3 \left( 2(1)(2) + \frac{1}{2\sqrt{2}} \right) + 5 (2^2) = 3 \left( 4 + \frac{1}{2\sqrt{2}} \right) + 20 \approx \mathbf{34.12}$$
>    *Interpretación:* Si nos encontramos en la posición $(2, 1)$ y nos desplazamos en la dirección $(3, 5)$, la altitud o valor de la función aumenta a una razón de $34.12$ unidades.

> [!example] Ejemplo 4.2: Máximo Ascenso en una Montaña
> Dada la superficie de una montaña descrita por $A(x, y) = \frac{x^2 + y^2}{10} + 50$, determinar hacia dónde debemos movernos desde el punto $(2, -1)$ para llegar lo más rápido posible a la cima.
>
> **Solución:**
> Debemos movernos en la dirección del gradiente $\nabla A(2, -1)$:
> $$\nabla A = \left( \frac{2x}{10}, \; \frac{2y}{10} \right) = \left( \frac{x}{5}, \; \frac{y}{5} \right)$$
> Evaluando en el punto $(2, -1)$:
> $$\nabla A(2, -1) = \mathbf{\left( \frac{2}{5}, \; -\frac{1}{5} \right)}$$

---

## 5. Operadores Diferenciales en Campos Vectoriales

### 5.1. Rotacional

El **rotacional** mide la tendencia de un campo vectorial a girar o inducir rotación en el flujo alrededor de cada punto.

- **En $\mathbb{R}^2 \to \mathbb{R}^2$:** Para $\mathbf{f}(x, y) = (f_1, f_2)$:
  $$\operatorname{rot}(\mathbf{f}) = \frac{\partial f_2}{\partial x} - \frac{\partial f_1}{\partial y} = \begin{vmatrix} \frac{\partial}{\partial x} & \frac{\partial}{\partial y} \\ f_1 & f_2 \end{vmatrix}$$

- **En $\mathbb{R}^3 \to \mathbb{R}^3$:** Para $\mathbf{f}(x, y, z) = (f_1, f_2, f_3)$:
  $$\operatorname{rot}(\mathbf{f}) = \nabla \times \mathbf{f} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ f_1 & f_2 & f_3 \end{vmatrix} = \left( \frac{\partial f_3}{\partial y} - \frac{\partial f_2}{\partial z}, \; \frac{\partial f_1}{\partial z} - \frac{\partial f_3}{\partial x}, \; \frac{\partial f_2}{\partial x} - \frac{\partial f_1}{\partial y} \right)$$

> [!example] Ejemplo 5.1: Rotacional en el Plano y en el Espacio
> 1. **Para $\mathbf{f}(x, y) = (x^2 y, \; x + y)$:**
>    $$\operatorname{rot}(\mathbf{f}) = \frac{\partial (x+y)}{\partial x} - \frac{\partial (x^2 y)}{\partial y} = \mathbf{1 - x^2}$$
> 2. **Para $\mathbf{f}(x, y, z) = \left( xy, \; x^2 - y, \; \frac{1}{z} \right)$:**
>    $$\operatorname{rot}(\mathbf{f}) = \left( 0 - 0, \; 0 - 0, \; 2x - x \right) = \mathbf{(0, 0, x)}$$

### 5.2. Divergencia

La **divergencia** mide la cantidad de flujo que se origina (fuente/manantial) o se destruye (sumidero) por unidad de volumen alrededor de cada punto.

- **En $\mathbb{R}^2$:** $\operatorname{Div}(\mathbf{f}) = \frac{\partial f_1}{\partial x} + \frac{\partial f_2}{\partial y}$
- **En $\mathbb{R}^3$:** $\operatorname{Div}(\mathbf{f}) = \frac{\partial f_1}{\partial x} + \frac{\partial f_2}{\partial y} + \frac{\partial f_3}{\partial z}$

> [!example] Ejemplo 5.2: Cálculo de la Divergencia
> Para el campo $\mathbf{f}(x, y, z) = \left( \frac{x}{y}, \; z - y, \; \frac{x^2}{z} \right)$:
> $$\operatorname{Div}(\mathbf{f}) = \frac{\partial}{\partial x}\left(\frac{x}{y}\right) + \frac{\partial}{\partial y}(z - y) + \frac{\partial}{\partial z}\left(\frac{x^2}{z}\right) = \frac{1}{y} - 1 - \frac{x^2}{z^2} = \mathbf{\frac{z^2 - yz^2 - x^2 y}{y z^2}}$$

---

## 6. Optimización en Varias Variables

### 6.1. Puntos Críticos y Matriz Hessiana

Para hallar los extremos relativos (máximos y mínimos locales) de una función escalar $f(x, y)$:

1. **Hallar los puntos críticos:** Resolver el sistema de ecuaciones dado por el gradiente nulo:
   $$\nabla f = (0, 0) \iff \begin{cases} f_x(x, y) = 0 \\ f_y(x, y) = 0 \end{cases}$$

2. **Construir la Matriz Hessiana $H$:** Matriz de derivadas parciales segundas:
   $$H(x, y) = \begin{pmatrix} f_{xx} & f_{xy} \\ f_{yx} & f_{yy} \end{pmatrix}$$

3. **Criterio del Determinante de $H$:** Evaluar $\det(H)$ en cada punto crítico:
   - **Si $\det(H) > 0$ y $f_{xx} > 0$:** Existe un **Mínimo Local**.
   - **Si $\det(H) > 0$ y $f_{xx} < 0$:** Existe un **Máximo Local**.
   - **Si $\det(H) < 0$:** Existe un **Punto de Silla** (la función sube en una dirección y baja en otra).
   - **Si $\det(H) = 0$:** El criterio **no es concluyente** (caso dudoso).

### 6.2. Ejemplos Resueltos Paso a Paso

> [!example] Ejemplo 6.1: Análisis de Extremos Relativos
> Estudiar los puntos críticos de $f(x, y) = 5 - x^2 - y^2$.
>
> **Solución:**
>
> 1. **Gradiente:** $\nabla f = (-2x, -2y) = (0, 0) \implies \begin{cases} -2x = 0 \implies x = 0 \\ -2y = 0 \implies y = 0 \end{cases} \implies C_1 = (0, 0)$.
> 2. **Matriz Hessiana:**
>    $$f_{xx} = -2, \quad f_{xy} = 0, \quad f_{yy} = -2 \implies H = \begin{pmatrix} -2 & 0 \\ 0 & -2 \end{pmatrix}$$
> 3. **Clasificación en $(0,0)$:**
>    $$\det(H) = (-2)(-2) - 0 = 4 > 0 \quad \text{y} \quad f_{xx} = -2 < 0$$
>    Por tanto, en el punto $(0, 0)$ la función presenta un **Máximo Local** de valor $f(0,0) = 5$.

> [!example] Ejemplo 6.2: Clasificación de Puntos Críticos Compleja
> Estudiar los extremos de $f(x, y) = x^3 + y^3 - 3xy$.
>
> **Solución:**
>
> 1. **Puntos críticos:**
>    $$\nabla f = (3x^2 - 3y, \; 3y^2 - 3x) = (0, 0) \implies \begin{cases} 3x^2 - 3y = 0 \implies y = x^2 \\ 3y^2 - 3x = 0 \implies 3(x^2)^2 - 3x = 0 \implies 3x(x^3 - 1) = 0 \end{cases}$$
>    De aquí obtenemos dos soluciones: $x = 0 \implies y = 0$ y $x = 1 \implies y = 1$.
>    Puntos críticos: **$C_1(0, 0)$** y **$C_2(1, 1)$**.
> 2. **Matriz Hessiana general:**
>    $$H(x, y) = \begin{pmatrix} 6x & -3 \\ -3 & 6y \end{pmatrix}$$
> 3. **Clasificación de los puntos:**
>
>    - **Para $C_1(0, 0)$:**
>      $$H(0, 0) = \begin{pmatrix} 0 & -3 \\ -3 & 0 \end{pmatrix} \implies \det(H) = 0 - 9 = -9 < 0$$
>      Al ser $\det(H) < 0$, el punto $(0, 0)$ es un **Punto de Silla**.
>    - **Para $C_2(1, 1)$:**
>      $$H(1, 1) = \begin{pmatrix} 6 & -3 \\ -3 & 6 \end{pmatrix} \implies \det(H) = 36 - 9 = 27 > 0 \quad \text{y} \quad f_{xx} = 6 > 0$$
>      Al ser $\det(H) > 0$ y $f_{xx} > 0$, la función presenta un **Mínimo Local** en $(1, 1)$.