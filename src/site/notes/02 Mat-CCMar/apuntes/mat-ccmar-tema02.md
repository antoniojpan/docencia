---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema02/","created":"2026-09-14T13:32:16.291+02:00","updated":"2026-09-14T13:40:02.887+02:00","dg-note-properties":{}}
---

[Volver al índice](mat-ccmar-indice)
# Tema 2: Espacios vectoriales

## 2. Espacios vectoriales, combinación lineal y rango

### 2.1. Definición de espacio vectorial y combinación lineal

**Definición.** Un **espacio vectorial** es un conjunto de elementos (denominados vectores) dotado de dos operaciones internas y externas (suma de vectores $+$, y producto por un escalar real $\cdot$) que cumplen una serie de propiedades algebraicas que podemos considerar "naturales" si pensamos en los vectores **como si fuesen flechas**. Los ejemplos fundamentales son los espacios euclídeos $\mathbb{R}^2$ y $\mathbb{R}^3$, formados por tuplas numéricas de la forma $(x,y)$ o $(x,y,z)$ con $x,y,z \in \mathbb{R}$.
![Pasted image 20260914130513.png](/img/user/imagenes/Pasted%20image%2020260914130513.png)
**Definición.** Dado un conjunto de vectores $\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3, \dots\}$ de un espacio vectorial $V$, se dice que un vector $\mathbf{v} \in V$ es **combinación lineal** de dicha colección si existen escalares reales $a_1, a_2, a_3, \dots \in \mathbb{R}$ tales que:
$$\mathbf{v} = a_1 \mathbf{u}_1 + a_2 \mathbf{u}_2 + a_3 \mathbf{u}_3 + \dots$$

> [!example] Ejemplo 2.1: Comprobación de combinación lineal de vectores
> **Enunciado:** Calcular los escalares $a_1$ y $a_2$ que expresan al vector $\mathbf{v} = (11,4)$ como combinación lineal de los vectores $\mathbf{u}_1 = (3,1)$ y $\mathbf{u}_2 = (5,2)$ en $\mathbb{R}^2$.
> 
> **Desarrollo paso a paso:**
> Planteamos la ecuación vectorial $\mathbf{v} = a_1 \mathbf{u}_1 + a_2 \mathbf{u}_2$:
> $$(11,4) = a_1 (3,1) + a_2 (5,2)$$
> Igualando componente a componente, obtenemos el siguiente sistema de ecuaciones lineales:
> $$\begin{cases} 3a_1 + 5a_2 = 11 \\ a_1 + 2a_2 = 4 \end{cases}$$
> De la segunda ecuación despejamos $a_1$:
> $$a_1 = 4 - 2a_2$$
> Sustituimos en la primera ecuación:
> $$3(4 - 2a_2) + 5a_2 = 11 \implies 12 - 6a_2 + 5a_2 = 11 \implies 12 - a_2 = 11 \implies a_2 = 1$$
> Sustituyendo el valor de $a_2 = 1$ en la expresión despejada de $a_1$:
> $$a_1 = 4 - 2(1) = 2$$
> Por tanto, los escalares resultantes son $a_1 = 2$ y $a_2 = 1$.
> 
> **Solución:** El vector $\mathbf{v}$ se expresa como combinación lineal de $\mathbf{u}_1$ y $\mathbf{u}_2$ mediante la relación $\mathbf{v} = 2\mathbf{u}_1 + \mathbf{u}_2$, comprobándose $2(3,1) + (5,2) = (6,2) + (5,2) = (11,4) \implies \mathbf{v} = 2\mathbf{u}_1 + \mathbf{u}_2$.
> 
> ![Pasted image 20260914130622.png](/img/user/imagenes/Pasted%20image%2020260914130622.png)

---

### 2.2. Independencia lineal y cálculo del rango por Gauss

**Definición.** Una colección de vectores $\{\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_k\}$ se dice que es **linealmente dependiente** si al menos uno de ellos se puede expresar como combinación lineal de los demás, lo que intuitivamente significa que "sobra" información en el conjunto. En caso contrario, si ningún vector depende linealmente de los demás, la colección es **linealmente independiente**.

**Definición.** El **rango de una matriz** es el número máximo de filas o de columnas linealmente independientes que posee dicha matriz.

**Método de cálculo del rango.** Existen dos métodos principales para determinar el rango de una matriz:
1. Mediante el cálculo de **menores** (submatrices cuadradas con determinante no nulo).
2. Mediante el **método de Gauss** (aplicación de transformaciones elementales por filas hasta escalonar la matriz).

Para estudiar el número de vectores independientes que hay en un conjunto dado, estudiamos el rango de la matriz consistente en poner esos vectores como filas de la matriz.

> [!example] Ejemplo 2.2: Cálculo del rango por el método de Gauss
> **Enunciado:** Estudiar cuántos vectores linealmente independientes hay en cada uno de los siguientes conjuntos de vectores:
> a) $\{\mathbf{u}_1, \mathbf{u}_2\} = \{(1, 2, 3),\; (-1, 2, 5)\}$ en $\mathbb{R}^3$.
> b) $\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\} = \{(2, 5, 1),\; (3, 1, 4),\; (5, 6, 5)\}$ en $\mathbb{R}^3$.
> 
> Para resolverlo, disponemos los vectores del conjunto como **filas** de una matriz y aplicamos eliminación gaussiana por filas. Las filas no nulas resultantes son linealmente independientes, de modo que su número coincide con el rango de la matriz, es decir, con la cantidad de vectores independientes del conjunto original.
> 
> **Desarrollo paso a paso:**
> **Caso a):**
> Disponemos los vectores como filas de la matriz $A$:
> $$A = \begin{pmatrix} 1 & 2 & 3 \\ -1 & 2 & 5 \end{pmatrix}$$
> Realizamos la transformación en la segunda fila $F_2 \to F_2 + F_1$:
> $$\begin{pmatrix} 1 & 2 & 3 \\ -1+1 & 2+2 & 5+3 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 4 & 8 \end{pmatrix}$$
> Simplificamos la fila 2 dividiendo entre 4 ($F_2 \to \frac{1}{4}F_2$):
> $$\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \end{pmatrix}$$
> Al obtener 2 filas no nulas escalonadas, se concluye la reducción.
> 
> **Caso b):**
> Partimos de la matriz $B$:
> $$B = \begin{pmatrix} 2 & 5 & 1 \\ 3 & 1 & 4 \\ 5 & 6 & 5 \end{pmatrix}$$
> Restamos la primera fila a la segunda ($F_2 \to F_2 - F_1$):
> $$\begin{pmatrix} 2 & 5 & 1 \\ 1 & -4 & 3 \\ 5 & 6 & 5 \end{pmatrix}$$
> Intercambiamos la primera y segunda fila ($F_1 \leftrightarrow F_2$):
> $$\begin{pmatrix} 1 & -4 & 3 \\ 2 & 5 & 1 \\ 5 & 6 & 5 \end{pmatrix}$$
> Hacemos ceros en la primera columna mediante $F_2 \to F_2 - 2F_1$ y $F_3 \to F_3 - 5F_1$:
> $$F_2 - 2F_1 = (2-2, 5 - 2(-4), 1 - 2(3)) = (0, 13, -5)$$
> $$F_3 - 5F_1 = (5-5, 6 - 5(-4), 5 - 5(3)) = (0, 26, -10)$$
> Obtenemos la matriz equivalente:
> $$\begin{pmatrix} 1 & -4 & 3 \\ 0 & 13 & -5 \\ 0 & 26 & -10 \end{pmatrix}$$
> Hacemos cero en la tercera fila aplicando la transformación $F_3 \to F_3 - 2F_2$:
> $$F_3 - 2F_2 = (0, 26 - 2(13), -10 - 2(-5)) = (0, 0, 0)$$
> La matriz escalonada resulta:
> $$\begin{pmatrix} 1 & -4 & 3 \\ 0 & 13 & -5 \\ 0 & 0 & 0 \end{pmatrix}$$
> Quedan 2 filas no nulas independientes.
> 
> **Solución:** En ambos conjuntos hay exactamente **2 vectores linealmente independientes**: en el caso a), $\mathrm{rango}(A) = 2 \implies \mathbf{\mathrm{rango}(A) = 2}$; y en el caso b), al anularse la tercera fila, $\mathrm{rango}(B) = 2 \implies \mathbf{\mathrm{rango}(B) = 2}$. En el conjunto b) el vector $\mathbf{u}_3 = (5,6,5)$ es combinación lineal de los otros dos, de modo que "sobra" y no aporta ninguna dirección nueva.

---

## 3. Espacios generados, bases y subespacios vectoriales

### 3.1. Espacio generado y sistema generador

**Definición.** Dada una colección de vectores $\{\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_k\}$ de un espacio vectorial $V$, se llama **espacio generado** por dicha colección al conjunto formado por todas las combinaciones lineales posibles que se pueden construir con ellos (todas las posibles "remezclas" de vectores).

**Definición.** Recíprocamente, a la colección de vectores $\{\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_k\}$ se le denomina **sistema generador** de dicho espacio vectorial.

![Pasted image 20260914132401.png](/img/user/imagenes/Pasted%20image%2020260914132401.png)

> [!example] Ejemplo 3.1: Determinación de un espacio generado y sistema generador
> **Enunciado:** Determinar el espacio generado por el conjunto $\{\mathbf{u}_1, \mathbf{u}_2\}$ con $\mathbf{u}_1 = (1,0,1)$ y $\mathbf{u}_2 = (0,1,1)$ en $\mathbb{R}^3$.
> 
> **Desarrollo paso a paso:**
> Construimos la combinación lineal genérica de los vectores $\mathbf{u}_1$ y $\mathbf{u}_2$ con escalares arbitrarios $\alpha, \beta \in \mathbb{R}$:
> $$\mathbf{v} = \alpha \mathbf{u}_1 + \beta \mathbf{u}_2 = \alpha(1,0,1) + \beta(0,1,1) = (\alpha,\; \beta,\; \alpha + \beta)$$
> Algunos vectores pertenecientes al espacio generado son:
> - Para $\alpha = 1, \beta = 1 \implies (1,1,2)$
> - Para $\alpha = 2, \beta = -1 \implies (2,-1,1)$
> - Para $\alpha = 1, \beta = 0 \implies \mathbf{u}_1 = (1,0,1)$


---

### 3.2. Base y dimensión de un espacio vectorial

**Definición.** Una **base** de un espacio o subespacio vectorial $S$ es un sistema generador de $S$ cuyos vectores son linealmente independientes.

**Definición.** La **dimensión** de un espacio o subespacio vectorial $S$, denotada como $\mathrm{dim}(S)$, es el número total de elementos (vectores) que componen cualquier base de $S$.

En la práctica, obtendremos una base a partir de un sistema generador, eliminando aquellos vectores "que sobren", por ser linealmente dependientes de los otros.

---

### 3.3. Subespacios vectoriales y sus formas de representación

**Definición.** Dado un espacio vectorial $V$, un **subespacio vectorial** $W$ es un subconjunto $W \subseteq V$ que posee estructura de espacio vectorial por sí mismo respecto a las operaciones de $V$. Por ejemplo, en $V = \mathbb{R}^3 = \{(x,y,z) : x,y,z \in \mathbb{R}\}$, el conjunto $W = \{(x,y,0) : x,y \in \mathbb{R}\}$ representa un subespacio vectorial contenido en $\mathbb{R}^3$ ($W \subseteq \mathbb{R}^3$).

> [!example] Ejemplo 3.2: Subespacio
> Considera el subespacio $W \subset \mathbb{R}^3$ definido por los vectores del sistema generador $B_W = \{ (1,1,2), (-2,1,0) \}$.
> 
> Un vector genérico $(x,y,z) \in W$ se expresa como combinación lineal de los elementos de $B_W$ introduciendo los parámetros $\lambda, \mu \in \mathbb{R}$:
> $$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \lambda \begin{pmatrix} 1 \\ 1 \\ 2 \end{pmatrix} + \mu \begin{pmatrix} -2 \\ 1 \\ 0 \end{pmatrix}$$
> Operando por componentes:
> $$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} \lambda \\ \lambda \\ 2\lambda \end{pmatrix} + \begin{pmatrix} -2\mu \\ \mu \\ 0 \end{pmatrix} = \begin{pmatrix} \lambda - 2\mu \\ \lambda + \mu \\ 2\lambda \end{pmatrix}$$
> Desglosando en ecuaciones individuales obtenemos las llamadas ecuaciones paramétricas:
> $$W:\begin{cases} x = \lambda - 2\mu \\ y = \lambda + \mu \\ z = 2\lambda \end{cases}$$



**Métodos de expresión de un subespacio.** Existen tres formas equivalentes de expresar analíticamente un subespacio vectorial $W$:
1. **Dando una base:** Especificando un conjunto de vectores linealmente independientes que generan $W$.
2. **Dando las ecuaciones paramétricas:** Expresando las coordenadas genéricas $(x,y,z,\dots)$ en función de los parámetros libres ($\lambda, \mu, \dots$) ponderados por los vectores de la base.
3. **Dando las ecuaciones implícitas (o cartesianas):** Mediante un sistema de ecuaciones lineales homogéneas que deben cumplir los elementos para pertenecer a $W$.

**Fórmula de relación entre dimensiones.** Para todo subespacio $W$ definido dentro de un espacio ambiente $V$, se verifica la relación fundamental:
$$\mathrm{dim}(V) = \mathrm{dim}(W) + n^\circ \text{ de ecuaciones implícitas independientes}$$
Es decir, cuanto mayor es la dimensión del subespacio, menos ecuaciones implícitas son necesarias para describirlo.


---

### 3.4. Conversiones entre formas de representación de subespacios

#### 3.4.1. Paso de base a ecuaciones paramétricas e implícitas

**Algoritmo de conversión de Base a Implícitas:**
1. Se construye la matriz cuya parte izquierda contiene los vectores de la base dispuestos por columnas y cuya última columna está formada por las variables $(x,y,z,\dots)$.
2. Se efectúa la reducción gaussiana por filas sobre las columnas de la base hasta obtener ceros en la zona inferior.
3. Se igualan a cero las expresiones algebraicas obtenidas en la columna de variables correspondientes a las filas nulas de la base. Dichas expresiones constituyen las **ecuaciones implícitas** de $W$.

> [!example] Ejemplo 3.3: Conversión de base a ecuaciones implícitas en $\mathbb{R}^3$
> **Enunciado:** Calcular la ecuación implícita del subespacio $W \subset \mathbb{R}^3$ que tiene como base $B_W = \{ (1,1,2), (-1,1,0) \}$.
> 
> **Desarrollo paso a paso:**
> Planteamos la matriz ampliada con los vectores de la base en columnas y las variables genéricas $(x,y,z)^T$ en el bloque derecho:
> $$\begin{pmatrix} 1 & -1 & x \\ 1 & 1 & y \\ 2 & 0 & z \end{pmatrix}$$
> Escalonamos la matriz mediante transformaciones elementales por filas:
> Hacemos ceros en la primera columna con $F_2 \to F_2 - F_1$ y $F_3 \to F_3 - 2F_1$:
> - Fila 2: $(1-1, 1-(-1), y-x) = (0, 2, y-x)$
> - Fila 3: $(2-2(1), 0-2(-1), z-2x) = (0, 2, z-2x)$
> Obtenemos la matriz intermedia:
> $$\begin{pmatrix} 1 & -1 & x \\ 0 & 2 & y-x \\ 0 & 2 & z-2x \end{pmatrix}$$
> Hacemos cero en la segunda columna de la fila 3 mediante $F_3 \to F_3 - F_2$:
> - Fila 3: $(0-0, 2-2, (z-2x) - (y-x)) = (0, 0, -x - y + z)$
> La matriz triangulada resulta:
> $$\begin{pmatrix} 1 & -1 & x \\ 0 & 2 & y-x \\ 0 & 0 & -x - y + z \end{pmatrix}$$
> Para garantizar la compatibilidad del sistema (que el vector pertenezca a $W$), el término de la fila de ceros debe anularse:
> $$-x - y + z = 0 \iff x + y - z = 0$$
> Comprobación de la fórmula de dimensiones: $\mathrm{dim}(\mathbb{R}^3) = 3$, $\mathrm{dim}(W) = 2$, por lo que requiere $3 - 2 = 1$ ecuación implícita.
> 
> **Solución:** La ecuación implícita que caracteriza al subespacio $W$ es $-x - y + z = 0 \implies \mathbf{-x - y + z = 0}$.

---

#### 3.4.2. Paso de ecuaciones implícitas a base

**Algoritmo de conversión de Implícitas a Base:**
1. Se plantea el sistema homogéneo dado por las ecuaciones implícitas.
2. Se resuelve el sistema mediante eliminación gaussiana para separar las variables libres de las dependientes.
3. Se expresa la solución general en función de parámetros ($\lambda, \mu, \dots$).
4. Se extraen los vectores asociados a cada parámetro. Si aparecen fracciones, se multiplican por el mínimo común denominador para obtener vectores de enteros.

> [!example] Ejemplo 3.4: Obtención de una base a partir de ecuaciones implícitas
> **Enunciado:** Resolver y determinar una base del subespacio $W \subset \mathbb{R}^3$ definido por el sistema de ecuaciones implícitas:
> $$\begin{cases} x - 3y + z = 0 \\ 2x - y = 0 \end{cases}$$
> 
> **Desarrollo paso a paso:**
> Escribimos la matriz ampliada del sistema homogéneo:
> $$\begin{pmatrix} 1 & -3 & 1 & 0 \\ 2 & -1 & 0 & 0 \end{pmatrix}$$
> Aplicamos $F_2 \to F_2 - 2F_1$:
> - Fila 2: $(2 - 2(1), -1 - 2(-3), 0 - 2(1), 0) = (0, 5, -2, 0)$
> La matriz escalonada es:
> $$\begin{pmatrix} 1 & -3 & 1 & 0 \\ 0 & 5 & -2 & 0 \end{pmatrix}$$
> Dividimos la segunda fila entre 5 ($F_2 \to \frac{1}{5}F_2$):
> $$\begin{pmatrix} 1 & -3 & 1 & 0 \\ 0 & 1 & -\frac{2}{5} & 0 \end{pmatrix}$$
> Obtenemos el sistema equivalente:
> $$\begin{cases} x - 3y + z = 0 \\ y - \frac{2}{5}z = 0 \end{cases}$$
> Asignamos a la variable libre el parámetro $z = \lambda$ ($\lambda \in \mathbb{R}$):
> De la segunda ecuación: $y = \frac{2}{5}\lambda$.
> Sustituimos $y$ y $z$ en la primera ecuación para despejar $x$:
> $$x = 3y - z = 3\left(\frac{2}{5}\lambda\right) - \lambda = \frac{6}{5}\lambda - \lambda = \frac{1}{5}\lambda$$
> La solución vectorial general es:
> $$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} \frac{1}{5}\lambda \\ \frac{2}{5}\lambda \\ \lambda \end{pmatrix} = \lambda \begin{pmatrix} \frac{1}{5} \\ \frac{2}{5} \\ 1 \end{pmatrix}$$
> Para simplificar denominadores, elegimos $\lambda = 5$, obteniendo el vector director $(1,2,5)$.
> 
> **Solución:** Una base del subespacio $W$ es $B_W = \{ (1, 2, 5) \}$, siendo su dimensión $\mathrm{dim}(W) = 1 \implies \mathbf{B_W = \{ (1, 2, 5) \}}$.

---

#### 3.4.3. Conversión completa en espacio ambiente $\mathbb{R}^4$

**Observación.** Cuando el espacio ambiente tiene dimensión $\mathrm{dim}(\mathbb{R}^4) = 4$, todo subespacio de dimensión $2$ requiere exactamente $4 - 2 = 2$ ecuaciones implícitas independientes para su completa caracterización.

> [!example] Ejemplo 3.5: Conversión de paramétricas a base e implícitas en $\mathbb{R}^4$
> **Enunciado:** Calcular una base y el sistema de ecuaciones implícitas del subespacio $W \subset \mathbb{R}^4$ presentado en ecuaciones paramétricas por:
> $$\begin{cases} x = \lambda - \mu \\ y = -\lambda \\ z = -\lambda + \mu \\ w = \mu \end{cases} \quad (\lambda, \mu \in \mathbb{R})$$
> 
> **Desarrollo paso a paso:**
> **Fase 1: Obtención de la base de $W$.**
> Separamos los parámetros $\lambda$ y $\mu$ en la expresión del vector $(x,y,z,w)^T$:
> $$\begin{pmatrix} x \\ y \\ z \\ w \end{pmatrix} = \begin{pmatrix} \lambda - \mu \\ -\lambda \\ -\lambda + \mu \\ \mu \end{pmatrix} = \lambda \begin{pmatrix} 1 \\ -1 \\ -1 \\ 0 \end{pmatrix} + \mu \begin{pmatrix} -1 \\ 0 \\ 1 \\ 1 \end{pmatrix}$$
> Los vectores coeficientes son $\mathbf{u}_1 = (1, -1, -1, 0)$ y $\mathbf{u}_2 = (-1, 0, 1, 1)$. Como no son proporcionales, son linealmente independientes y forman una base de $W$:
> $$B_W = \{ (1, -1, -1, 0), (-1, 0, 1, 1) \}$$
> 
> **Fase 2: Obtención de las ecuaciones implícitas.**
> Disponemos los vectores base en columnas y las variables genéricas $(x,y,z,w)^T$ en la última columna:
> $$\begin{pmatrix} 1 & -1 & x \\ -1 & 0 & y \\ -1 & 1 & z \\ 0 & 1 & w \end{pmatrix}$$
> Aplicamos transformaciones por filas para triangular el bloque base:
> - $F_2 \to F_2 + F_1$: $(-1+1, 0-1, y+x) = (0, -1, x+y)$
> - $F_3 \to F_3 + F_1$: $(-1+1, 1-1, z+x) = (0, 0, x+z)$
> Matriz intermedia:
> $$\begin{pmatrix} 1 & -1 & x \\ 0 & -1 & x+y \\ 0 & 0 & x+z \\ 0 & 1 & w \end{pmatrix}$$
> Multiplicamos la segunda fila por $-1$ ($F_2 \to -F_2$):
> $$\begin{pmatrix} 1 & -1 & x \\ 0 & 1 & -x-y \\ 0 & 0 & x+z \\ 0 & 1 & w \end{pmatrix}$$
> Hacemos cero en la cuarta fila mediante $F_4 \to F_4 - F_2$:
> - Fila 4: $(0-0, 1-1, w - (-x-y)) = (0, 0, x+y+w)$
> Reordenando las filas para colocar las nulas al final:
> $$\begin{pmatrix} 1 & -1 & x \\ 0 & 1 & -x-y \\ 0 & 0 & x+z \\ 0 & 0 & x+y+w \end{pmatrix}$$
> Igualando a cero las expresiones de las filas nulas obtenemos las ecuaciones implícitas:
> $$\begin{cases} x + z = 0 \\ x + y + w = 0 \end{cases}$$
> 
> **Comprobación de dimensiones:**
> Dimensión ambiente: $\mathrm{dim}(\mathbb{R}^4) = 4$. Dimensión del subespacio: $\mathrm{dim}(W) = 2$ (2 vectores en la base). Número de implícitas: 2. Cumple $4 = 2 + 2$.
> 
> **Solución:** La base de $W$ es $B_W = \{ (1, -1, -1, 0), (-1, 0, 1, 1) \}$ y sus ecuaciones implícitas son $\begin{cases} x + z = 0 \\ x + y + w = 0 \end{cases} \implies \mathbf{\begin{cases} x + z = 0 \\ x + y + w = 0 \end{cases}}$.