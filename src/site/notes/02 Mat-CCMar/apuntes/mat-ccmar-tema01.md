---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema01/","created":"2026-09-14T12:28:49.025+02:00","updated":"2026-09-14T12:28:06.000+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 1: Sistemas de Ecuaciones Lineales y Matrices


## 1. Sistemas de Ecuaciones Lineales

**Definición.** Un **sistema de ecuaciones lineales** es una colección de ecuaciones lineales que deben ser resueltas de manera simultánea.

### 1.1. Clasificación de Sistemas de Ecuaciones

**Criterio de clasificación.** La **discusión y clasificación de sistemas** es uno de los apartados fundamentales del álgebra lineal. Según el número de soluciones que poseen, los sistemas se clasifican en:

- **Incompatible (S.I.)**: No existe ningún valor de las incógnitas que cumpla todas las ecuaciones simultáneamente (sin solución).
- **Compatible Determinado (S.C.D.)**: Existe un **único valor** para cada incógnita que satisface el sistema (solución única).
- **Compatible Indeterminado (S.C.I.)**: Existen **infinitos valores** de las incógnitas que satisfacen el sistema (infinitas soluciones).

---

### 1.2. Ejemplos Resueltos de Resolución de Sistemas

> [!example] Ejemplo 1.1: Sistema Compatible Determinado ($2 \times 2$)
> **Resolver el siguiente sistema:**
> $$\begin{cases} x + y = 10 \\ x - y = 4 \end{cases}$$
> 
> **Solución:**
> Sumando ambas ecuaciones directamente:
> $$2x = 14 \implies \mathbf{x = 7}$$
> 
> Sustituyendo el valor de $x$ en la primera ecuación:
> $$7 + y = 10 \implies \mathbf{y = 3}$$
> 
> **Conclusión:** El sistema es **Compatible Determinado (S.C.D.)** con solución única $(x, y) = (7, 3)$.

---

> [!example] Ejemplo 1.2: Sistema Compatible Indeterminado con Parámetro Libre
> **Resolver el siguiente sistema:**
> $$\begin{cases} 2x + 4y + z = 6 \\ 2x + 2y = 1 \end{cases}$$
> 
> **Solución:**
> Como tenemos 3 incógnitas y 2 ecuaciones, asignamos un parámetro libre a una de las variables. Sea $z = t$ con $t \in \mathbb{R}$:
> $$\begin{cases} 2x + 4y = 6 - t \\ 2x + 2y = 1 \end{cases}$$
> 
> Restando la segunda ecuación a la primera:
> $$2y = 5 - t \implies \mathbf{y = \frac{5-t}{2}}$$
> 
> Sustituyendo $y$ en la segunda ecuación:
> $$2x = 1 - 2\left(\frac{5-t}{2}\right) = 1 - 5 + t = -4 + t \implies \mathbf{x = -2 + \frac{t}{2}}$$
> 
> **Conclusión:** El sistema es **Compatible Indeterminado (S.C.I.)** con soluciones parametrizadas por $t \in \mathbb{R}$:
> $$(x, y, z) = \left(-2 + \frac{t}{2}, \; \frac{5-t}{2}, \; t\right), \quad t \in \mathbb{R}$$

---

### 1.3. Discusión de Sistemas con Parámetros

**Método de análisis.** Para discutir un sistema con parámetros, se analiza la existencia y unicidad de las soluciones en función de los valores que tome el parámetro genérico (habitualmente $a,\lambda, k,\ldots$).

> [!example] Ejemplo 1.3: Discusión Completa según el Parámetro $a$
> **Discutir y resolver el sistema:**
> $$\begin{cases} x - ay = -2 \\ ax - y = 2 \end{cases}$$
> 
> **Desarrollo algebraico:**
> Despejando $x$ de la primera ecuación ($x = ay - 2$) y sustituyendo en la segunda:
> $$a(ay - 2) - y = 2 \implies a^2 y - y - 2a = 2 \implies (1 - a^2)x = -2 - 2a$$
> 
> Despejando las variables cuando $1 - a^2 \neq 0$ (es decir, $a \neq 1$ y $a \neq -1$):
> $$x = \frac{-2 - 2a}{1 - a^2} = \frac{-2(1+a)}{(1-a)(1+a)} = \frac{-2}{1-a} = \frac{2}{a-1}$$
> $$y = \frac{-2a - 2}{1 - a^2} = \frac{-2(a+1)}{(1-a)(1+a)} = \frac{-2}{1-a} = \frac{2}{a-1}$$
> 
> **Discusión según los casos del parámetro $a$:**
> 1. **Si $a \neq 1$ y $a \neq -1$:** El sistema es **Compatible Determinado (S.C.D.)**. Solución única: $\left(\frac{2}{a-1}, \frac{2}{a-1}\right)$.
> 2. **Si $a = 1$:** Sustituyendo $a = 1$ en el sistema original:
>    $$\begin{cases} x - y = -2 \\ x - y = 2 \end{cases} \implies -2 = 2 \quad \text{(Imposible)}$$
>    El sistema es **Incompatible (S.I.)**.
> 3. **Si $a = -1$:** Sustituyendo $a = -1$ en el sistema original:
>    $$\begin{cases} x + y = -2 \\ -x - y = 2 \end{cases} \implies x + y = -2 \quad \text{(Ecuaciones equivalentes)}$$
>    El sistema es **Compatible Indeterminado (S.C.I.)**. Soluciones: $y = t$, $x = -2 - t$ con $t \in \mathbb{R}$.

---

> [!example] Ejemplo 1.4: Discusión de un Sistema Lineal Paramétrico
> **Discutir el sistema:**
> $$\begin{cases} x + y = 20 \\ (1+a)x + y = 22 \end{cases}$$
> 
> **Solución:**
> Restando la primera ecuación a la segunda:
> $$((1+a)x + y) - (x + y) = 22 - 20 \implies ax = 2$$
> 
> **Discusión:**
> 1. **Si $a \neq 0$:** El sistema es **Compatible Determinado (S.C.D.)**.
>    $$x = \frac{2}{a}, \quad y = 20 - \frac{2}{a}$$
> 2. **Si $a = 0$:** Sustituyendo $a = 0$:
>    $$\begin{cases} x + y = 20 \\ x + y = 22 \end{cases} \implies \text{No es posible } (20 \neq 22)$$
>    El sistema es **Incompatible (S.I.)**.

---

## 2. Matrices

**Concepto de matriz.** Las **matrices** son estructuraciones en forma de "cajas de números" que poseen gran utilidad en matemáticas. Poseen la propiedad particular de comportarse algebraicamente de manera análoga a los números simples.

```
       ┌               ┐
       │  a11 a12 a13  │
   A = │  a21 a22 a23  │
       │  a31 a32 a33  │
       └               ┘
```

---

### 2.1. Aplicaciones

Las matrices permiten expresar de forma compacta grandes cantidades de información. Dos aplicaciones fundamentales son la **representación de sistemas de ecuaciones lineales** y el **modelado de sistemas dinámicos**.

> [!example] Ejemplo 2.1: Representación Matricial de un Sistema Lineal
> Un sistema de ecuaciones lineales se escribe de forma compacta como $A \cdot X = B$. Por ejemplo, el sistema del Ejemplo 1.1:
> $$\begin{cases} x + y = 10 \\ x - y = 4 \end{cases} \iff \underbrace{\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}}_{A} \cdot \underbrace{\begin{pmatrix} x \\ y \end{pmatrix}}_{X} = \underbrace{\begin{pmatrix} 10 \\ 4 \end{pmatrix}}_{B}$$
> donde $A$ es la **matriz de coeficientes**, $X$ el **vector de incógnitas** y $B$ el **vector de términos independientes**.

> [!example] Ejemplo 2.2: Sistema Dinámico: Evolución de una Población de Peces
> Consideremos dos especies de peces, $x$ e $y$, que conviven en un mismo ecosistema. Si las cantidades al inicio de un año son $x_A$ e $y_A$ (cantidades actuales), al año siguiente pasan a ser:
> $$\begin{cases} x_N = 3x_A + 2y_A \\ y_N = -4x_A + 4y_A \end{cases}$$
> 
> **Interpretación de los coeficientes:**
> - **3**: la especie $x$ se reproduce, triplicando su propio número en un año.
> - **2**: la especie $x$ crece alimentándose de la especie $y$.
> - **$-4$**: la especie $y$ disminuye por ser depredada por la especie $x$.
> - **4**: la especie $y$ se reproduce, cuadruplicando su propio número en un año.
> Las dos ecuaciones anteriores se escriben de forma compacta como $$X_N = A \cdot X_A,$$ donde $X_A$ es el vector de cantidades actuales, $X_N$ el vector de cantidades nuevas y la **matriz de evolución** $A$ concentra la dinámica del ecosistema:
> $$X_N = \begin{pmatrix} x_N \\ y_N \end{pmatrix}, \quad X_A = \begin{pmatrix} x_A \\ y_A \end{pmatrix}, \quad A = \begin{pmatrix} 3 & 2 \\ -4 & 4 \end{pmatrix}$$
> 
> Iterando la expresión $X_{t+1} = A \cdot X_t$ se pueden **simular las poblaciones año tras año**, lo que permite predecir su evolución a largo plazo.

---

### 2.2. Operaciones con Matrices

Las matrices se pueden **sumar**, **restar** y **multiplicar**, dando lugar a un álgebra análoga a la de los números. Entre estas operaciones destaca también la **matriz inversa**.

- **Suma y Resta**: operaciones que se realizan elemento a elemento (requieren matrices de la misma dimensión).
- **Producto de Matrices**: se calcula multiplicando **cada fila por cada columna**.

> [!example] Ejemplo 2.3: Producto de Matrices $2 \times 2$
> $$\begin{pmatrix} 2 & 3 \\ 1 & 5 \end{pmatrix} \cdot \begin{pmatrix} -1 & 2 \\ 1 & 4 \end{pmatrix} = \begin{pmatrix} 2(-1)+3(1) & 2(2)+3(4) \\ 1(-1)+5(1) & 1(2)+5(4) \end{pmatrix} = \begin{pmatrix} 1 & 16 \\ 4 & 22 \end{pmatrix}$$

**La matriz inversa.** Dada una matriz cuadrada $A$, su **matriz inversa** $A^{-1}$ verifica la relación:
$$A^{-1} \cdot A = I \quad \text{o bien} \quad A \cdot A^{-1} = I$$
donde $I$ representa la **matriz identidad**. La forma práctica de calcularla se estudia en el apartado 2.4 mediante el método de **Gauss-Jordan**.

---

### 2.3. Tipos de Matrices

**Matriz fila y matriz columna.** La **matriz fila** tiene una sola fila y la **matriz columna** una sola columna:
$$F = \begin{pmatrix} a & b & c \end{pmatrix}, \qquad C = \begin{pmatrix} a \\ b \\ c \end{pmatrix}$$

**Matriz cuadrada y matriz triangular.** Una **matriz cuadrada** tiene el mismo número de filas que de columnas. Entre ellas destacan las **triangulares**, con todos los ceros por debajo (**superior** $S$) o por encima (**inferior** $T$) de la diagonal principal:
$$S = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ 0 & a_{22} & a_{23} \\ 0 & 0 & a_{33} \end{pmatrix}, \qquad T = \begin{pmatrix} a_{11} & 0 & 0 \\ a_{21} & a_{22} & 0 \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$

**Matriz diagonal.** Una **matriz diagonal** es una matriz cuadrada cuyos elementos fuera de la diagonal principal son todos nulos:
$$D = \begin{pmatrix} x_1 & 0 & 0 & \dots \\ 0 & x_2 & 0 & \dots \\ 0 & 0 & x_3 & \dots \\ \vdots & \vdots & \vdots & \ddots \end{pmatrix}$$

**Matriz identidad.** La **matriz identidad** $I$ es la matriz diagonal con unos en la diagonal principal. Actúa como **elemento neutro del producto** de matrices y juega un papel clave en el cálculo de inversas.

---

### 2.4. Método de Gauss

Una de las principales funciones prácticas de las matrices es el **estudio y resolución de sistemas de ecuaciones lineales** empleando la **matriz ampliada** y transformaciones elementales por filas. La misma técnica, en su variante de **Gauss-Jordan**, permite **calcular la matriz inversa**.

**Operaciones elementales por filas.** El método de Gauss se apoya en tres tipos de **operaciones elementales por filas** sobre la matriz ampliada, todas ellas **reversibles** y que **no alteran las soluciones** del sistema:

- **Permutar dos filas**: $F_i \leftrightarrow F_j$ (equivale a reordenar las ecuaciones).
- **Multiplicar una fila por un número no nulo**: $F_i \leftarrow k \cdot F_i$.
- **Combinar filas**: sumar a una fila un múltiplo de otra: $F_i \leftarrow F_i + k \cdot F_j$ (equivale a sumar ecuaciones entre sí).

**Tres versiones del método de Gauss.** Según la forma final que se le dé a la matriz, distinguimos tres versiones:

1. **Gauss clásico (matriz triangular):** se anulan los elementos por debajo de la diagonal, de modo que esta queda con elementos **no nulos pero arbitrarios**. El sistema se resuelve entonces por **sustitución regresiva**.
2. **Gauss con diagonal de unos:** tras triangular, se **normaliza** cada fila dividiéndola entre su pivote, con lo que todos los elementos de la diagonal son $1$. La sustitución regresiva se simplifica, pues cada variable se despeja directamente de su propia fila.
3. **Gauss-Jordan:** además de los ceros por debajo, se anulan también los elementos **por encima** de la diagonal, hasta convertir la parte de los coeficientes en la **matriz identidad**. La solución queda directamente en la última columna, sin sustitución regresiva. Esta es la variante usada para el **cálculo de inversas**.

**Cambio de columnas (caso particular).** En ocasiones el elemento de la diagonal es cero y **también lo son todos los que tiene por debajo** en esa columna; entonces permutar filas no sirve y hay que **intercambiar la columna** con la de alguna de las variables siguientes. Como cada columna de coeficientes corresponde a una variable, al permutar columnas las variables **cambian de lugar**, por lo que hay que **seguir la pista al cambio de nombre** de las variables para no equivocarse al leer la solución final.

**Algoritmo de eliminación gaussiana:**

1. Escribir la matriz ampliada del sistema $(A|B)$.
2. Obtener ceros por debajo de la diagonal principal mediante operaciones elementales por filas.
3. Reconstruir el sistema equivalente triangular y resolver por sustitución regresiva.

> [!example] Ejemplo 2.4: Resolución Completa de un Sistema $3 \times 3$ por Gauss
> **Resolver el sistema mediante su matriz ampliada:**
> $$\begin{cases} 2x + 3y - z = 5 \\ x - y + 2z = 0 \\ 5x + 2y - z = 7 \end{cases}$$
> 
> **Paso 1: Matriz ampliada inicial**
> $$\left( \begin{array}{ccc|c} 2 & 3 & -1 & 5 \\ 1 & -1 & 2 & 0 \\ 5 & 2 & -1 & 7 \end{array} \right)$$
> 
> **Paso 2: Intercambio de filas ($F_1 \leftrightarrow F_2$) para facilitar el pivote igual a 1**
> $$\sim \left( \begin{array}{ccc|c} 1 & -1 & 2 & 0 \\ 2 & 3 & -1 & 5 \\ 5 & 2 & -1 & 7 \end{array} \right)$$
> 
> **Paso 3: Ceros en la primera columna ($F_2 \leftarrow F_2 - 2F_1$, $F_3 \leftarrow F_3 - 5F_1$)**
> $$\sim \left( \begin{array}{ccc|c} 1 & -1 & 2 & 0 \\ 0 & 5 & -5 & 5 \\ 0 & 7 & -11 & 7 \end{array} \right)$$
> 
> **Paso 4: Normalizar la fila 2 ($F_2 \leftarrow \frac{1}{5}F_2$)**
> $$\sim \left( \begin{array}{ccc|c} 1 & -1 & 2 & 0 \\ 0 & 1 & -1 & 1 \\ 0 & 7 & -11 & 7 \end{array} \right)$$
> 
> **Paso 5: Cero en la segunda columna ($F_3 \leftarrow F_3 - 7F_2$)**
> $$\sim \left( \begin{array}{ccc|c} 1 & -1 & 2 & 0 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & -4 & 0 \end{array} \right)$$
> 
> **Paso 6: Normalizar la fila 3 ($F_3 \leftarrow -\frac{1}{4}F_3$)**
> $$\sim \left( \begin{array}{ccc|c} 1 & -1 & 2 & 0 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & 1 & 0 \end{array} \right)$$
> 
> **Paso 7: Reconstrucción del sistema y solución**
> $$\begin{cases} x - y + 2z = 0 \\ y - z = 1 \\ z = 0 \end{cases}$$
> 
> Resolviendo desde la última ecuación hacia arriba:
> 4. $z = 0$
> 5. $y - 0 = 1 \implies \mathbf{y = 1}$
> 6. $x - 1 + 2(0) = 0 \implies \mathbf{x = 1}$
> 
> **Solución:** $(x, y, z) = (1, 1, 0)$.

**Método de Gauss-Jordan para el cálculo de la inversa.** Se construye la matriz en bloques $(A \mid I)$ y se aplican operaciones elementales por filas hasta transformarla en $(I \mid A^{-1})$.

> [!example] Ejemplo 2.5: Cálculo de la Inversa por Gauss-Jordan
> **Dada la matriz $A$:**
> $$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & -2 \\ 2 & 1 & 1 \end{pmatrix}$$
> 
> **Disposición en bloques $(A \mid I)$:**
> $$\left( \begin{array}{ccc|ccc} 1 & 2 & 0 & 1 & 0 & 0 \\ 0 & 1 & -2 & 0 & 1 & 0 \\ 2 & 1 & 1 & 0 & 0 & 1 \end{array} \right)$$
> 
> **Reducción de Gauss-Jordan:**
> 1. Hacer cero en la tercera fila ($F_3 \leftarrow F_3 - 2F_1$):
>    $$\left( \begin{array}{ccc|ccc} 1 & 2 & 0 & 1 & 0 & 0 \\ 0 & 1 & -2 & 0 & 1 & 0 \\ 0 & -3 & 1 & -2 & 0 & 1 \end{array} \right)$$
> 2. Triangular la matriz ($F_3 \leftarrow F_3 + 3F_2$):
>    $$\left( \begin{array}{ccc|ccc} 1 & 2 & 0 & 1 & 0 & 0 \\ 0 & 1 & -2 & 0 & 1 & 0 \\ 0 & 0 & 1 & 1 & -1 & -1 \end{array} \right)$$
> 3. Hacer ceros por encima de la diagonal ($F_2 \leftarrow F_2 + 2F_3$):
>    $$\left( \begin{array}{ccc|ccc} 1 & 2 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 2 & -1 & -2 \\ 0 & 0 & 1 & 1 & -1 & -1 \end{array} \right)$$
> 4. Eliminar el último elemento ($F_1 \leftarrow F_1 - 2F_2$):
>    $$\left( \begin{array}{ccc|ccc} 1 & 0 & 0 & -3 & 2 & 4 \\ 0 & 1 & 0 & 2 & -1 & -2 \\ 0 & 0 & 1 & 1 & -1 & -1 \end{array} \right)$$
> 
> **Matriz Inversa Resultante:**
> $$A^{-1} = \begin{pmatrix} -3 & 2 & 4 \\ 2 & -1 & -2 \\ 1 & -1 & -1 \end{pmatrix}$$

