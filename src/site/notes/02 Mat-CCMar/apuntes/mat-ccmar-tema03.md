---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema03/","created":"2026-09-15T09:30:39.590+02:00","updated":"2026-10-07T07:43:43.021+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 3: Diagonalización

## 1. Motivación e Interpretación en Sistemas Dinámicos

### 1.1. Modelización de Poblaciones y Matriz de Transición
**Definición.** Un sistema dinámico discreto lineal describe la evolución temporal de variables interrelacionadas a intervalos regulares mediante una ecuación de recurrencia de la forma $\mathbf{X}_{k+1} = A \cdot \mathbf{X}_k$, donde $A$ es la matriz de transición del sistema y $\mathbf{X}_k$ representa el vector de estado en el periodo $k$.

**Interpretación biológica.** En modelos poblacionales (como la dinámica de dos poblaciones de peces $x$ e $y$), los coeficientes de la matriz $A = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix}$ reflejan tanto el crecimiento propio como las interacciones ecológicas:
- **Tasa propia de crecimiento ($a_{11}, a_{22}$):** Mide el ritmo de autorreproducción anual de cada especie en ausencia de influencias externas.
- **Tasa de interacción ($a_{12}, a_{21}$):** Mide la influencia de una especie sobre la otra. Un valor positivo ($a_{ij} > 0$) representa una relación de mutualismo o beneficio mutuo, donde la presencia de la especie $j$ favorece la multiplicación de la especie $i$.

---

### 1.2. Evolución a Largo Plazo y el Problema de la Potencia Matricial
**Propiedad.** Si la condición inicial del sistema en el instante $t = 0$ es el vector $\mathbf{X}_0$, la población tras $n$ periodos o años viene determinada por la aplicación iterada de la matriz de transición:
$$\mathbf{X}_n = A^n \cdot \mathbf{X}_0$$

> [!example] Ejemplo 1.1: Modelización matricial de dos poblaciones de peces interrelacionadas
> Calcular la matriz de transición del sistema y plantear la ecuación matricial para determinar la población tras 20 años de dos especies de peces $x$ e $y$ cuyas poblaciones anuales futuras $\bar{x}$ e $\bar{y}$ vienen dadas por:
> $$\begin{cases} \bar{x} = 3x + y \\ \bar{y} = 2x + 2y \end{cases}$$
> partiendo de una población inicial $x_0 = 5$ e $y_0 = 2$.
> 
> **Desarrollo paso a paso:**
> 1. Escribimos el sistema de ecuaciones en forma matricial relacionando el vector de estado futuro $\mathbf{\bar{X}} = \begin{pmatrix} \bar{x} \\ \bar{y} \end{pmatrix}$ con el vector de estado actual $\mathbf{X} = \begin{pmatrix} x \\ y \end{pmatrix}$:
> $$\begin{pmatrix} \bar{x} \\ \bar{y} \end{pmatrix} = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}$$
> 
> 2. Identificamos la matriz de transición $A$:
> $$A = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix}$$
> 
> 3. Interpretamos los coeficientes: El valor $3$ indica que cada pez de la especie $x$ produce $3$ individuos para el siguiente año; el valor $1$ expresa que cada pez de la especie $y$ contribuye a aumentar en $1$ individuo la población de $x$ (mutualismo). Asimismo, $2x$ representa la aportación de $x$ al crecimiento de $y$, y $2y$ representa la tasa propia de crecimiento de $y$.
> 
> 4. Planteamos la ecuación para la población transcurridos $n = 20$ años con la condición inicial $\mathbf{X}_0 = \begin{pmatrix} 5 \\ 2 \end{pmatrix}$:
> $$\mathbf{X}_{20} = A^{20} \cdot \mathbf{X}_0 = A^{20} \begin{pmatrix} 5 \\ 2 \end{pmatrix}$$
> 
> **Solución:** La matriz de transición es $A = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix}$ y la relación matricial tras 20 años es $\mathbf{X}_{20} = A^{20} \begin{pmatrix} 5 \\ 2 \end{pmatrix}$.


---

> [!example] Ejemplo 1.2: Poblaciones desacopladas 
> Supongamos ahora dos especies de peces $u$ e $v$ que viven en tanques separados, sin interacción ecológica. Sus poblaciones evolucionan independientemente según:
> $$\begin{cases} \bar{u} = 3u \\ \bar{v} = 2v \end{cases}$$
> con condición inicial $u_0 = 5$, $v_0 = 2$.
> 
> **Desarrollo:**
> 1. La matriz de transición del sistema es **diagonal** (las variables están desacopladas):
> $$D = \begin{pmatrix} 3 & 0 \\ 0 & 2 \end{pmatrix}$$
> 
> 2. La población tras 20 años es $D^{20} \begin{pmatrix} 5 \\ 2 \end{pmatrix}$. Como $D$ es diagonal, **la potencia se calcula de forma trivial** elevando cada elemento diagonal a la potencia 20:
> $$D^{20} = \begin{pmatrix} 3^{20} & 0 \\ 0 & 2^{20} \end{pmatrix}$$
> 
> 3. La solución es inmediata:
> $$\mathbf{X}_{20} = \begin{pmatrix} 3^{20} & 0 \\ 0 & 2^{20} \end{pmatrix}\begin{pmatrix} 5 \\ 2 \end{pmatrix} = \begin{pmatrix} 5 \cdot 3^{20} \\ 2 \cdot 2^{20} \end{pmatrix}$$


---

**Observación.** Para valores elevados de $n$ (como $n = 20$), calcular $A^n$ del Ejemplo 1.1 mediante multiplicaciones matriciales sucesivas directas resulta impracticable: su matriz está llena de interacciones cruzadas y cada variable se interfiere con la otra. En cambio, la matriz $D$ del Ejemplo 1.2 era diagonal — cada especie evolucionaba sola — y $D^{20}$ se obtuvo de un vistazo, elevando cada elemento diagonal a la potencia 20. La diferencia es brutal, y se reduce a una única propiedad: que la matriz sea **diagonal**. Este es el gran premio que buscamos: cambiar a un sistema de coordenadas (definido por los autovectores) en el que $A$ se vea diagonal, es decir, en el que las variables se comporten de forma independiente, desacopladas como las del Ejemplo 1.2.


**La idea clave de la diagonalización.** En lugar de analizar directamente las especies reales $x$ e $y$, buscamos definir una "remezcla" de ellas: unos **seres imaginarios $A$ y $B$** (combinaciones lineales fijas de $x$ e $y$) que tengan la propiedad de ser totalmente independientes entre sí.
- Mientras que $x$ e $y$ están acoplados y se interfieren mutuamente, los seres imaginarios $A$ y $B$ **se comportan de forma desacoplada**.
- La evolución temporal de $A$ y $B$ es independiente y sigue una simple escala exponencial multiplicada por sus respectivos autovalores ($\lambda_1$ y $\lambda_2$).
- Una vez calculada la evolución trivial de $A$ y $B$ tras $n$ años, desechamos el cambio para volver a las poblaciones reales $x$ e $y$.

![Pasted image 20260915095403.png\|900](/img/user/imagenes/Pasted%20image%2020260915095403.png)

---

## 2. Autovalores y Autovectores

### 2.1. Concepto y Ecuación Característica
**Definición.** Dada una matriz cuadrada $A \in \mathbb{R}^{n \times n}$, un escalar $\lambda \in \mathbb{R}$ es un **autovalor** (o valor propio) de $A$ si existe un vector no nulo $\mathbf{v} \neq \mathbf{0}$ tal que:
$$A \cdot \mathbf{v} = \lambda \cdot \mathbf{v}$$
Al vector $\mathbf{v}$ se le denomina **autovector** (o vector propio) asociado a $\lambda$.

**Propiedad.** Reescribiendo la ecuación previa como un sistema homogéneo $(A - \lambda I)\mathbf{v} = \mathbf{0}$, este admite soluciones no triviales si y solo si el determinante de la matriz del sistema es nulo:
$$|A - \lambda I| = 0$$
Esta expresión constituye la **ecuación característica**, cuyo polinomio asociado $p(\lambda) = |A - \lambda I|$ es el **polinomio característico** de $A$. Sus raíces reales son los autovalores de la matriz.

---

### 2.2. Subespacios Propios y Cálculo de Autovectores
**Definición.** El conjunto formado por todos los autovectores asociados a un autovalor $\lambda$, junto con el vector nulo $\mathbf{0}$, constituye un subespacio vectorial denominado **espacio propio** o **subespacio asociado**, denotado por $E(\lambda) = \text{Ker}(A - \lambda I)$.

**Método de cálculo de autovectores.** Para cada autovalor $\lambda_i$:
1. Sustituir $\lambda_i$ en el sistema homogéneo $(A - \lambda_i I)\mathbf{v} = \mathbf{0}$.
2. Resolver el sistema por el método de Gauss para obtener la relación entre las componentes del vector.
3. Asignar un parámetro libre para hallar la base del autovector $\mathbf{v}_i$.

---

> [!example] Ejemplo 2.1: Cálculo de autovalores y autovectores
> Calcular los autovalores y autovectores de la matriz de transición del sistema poblacional:
> $$A = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix}$$
> 
> **Desarrollo paso a paso:**
> 1. Planteamos la ecuación característica $|A - \lambda I| = 0$:
> $$\begin{vmatrix} 3 - \lambda & 1 \\ 2 & 2 - \lambda \end{vmatrix} = 0$$
> 
> 2. Desarrollamos el determinante de orden $2 \times 2$:
> $$(3 - \lambda)(2 - \lambda) - (1 \cdot 2) = 0 \implies 6 - 3\lambda - 2\lambda + \lambda^2 - 2 = 0 \implies \lambda^2 - 5\lambda + 4 = 0$$
> 
> 3. Resolvemos la ecuación de segundo grado mediante la fórmula general:
> $$\lambda = \frac{-(-5) \pm \sqrt{(-5)^2 - 4(1)(4)}}{2(1)} = \frac{5 \pm \sqrt{25 - 16}}{2} = \frac{5 \pm \sqrt{9}}{2} = \frac{5 \pm 3}{2}$$
> Obtenemos dos autovalores reales y distintos:
> $$\lambda_1 = 4, \quad \lambda_2 = 1$$
> 
> 4. Determinamos el autovector $\mathbf{v}_1 = \begin{pmatrix} x \\ y \end{pmatrix}$ asociado a $\lambda_1 = 4$:
> Sustituimos $\lambda = 4$ en $(A - 4I)\mathbf{v} = \mathbf{0}$:
> $$\begin{pmatrix} 3 - 4 & 1 \\ 2 & 2 - 4 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix} \implies \begin{pmatrix} -1 & 1 \\ 2 & -2 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$$
> Obtenemos la ecuación $-x + y = 0 \implies x = y$. Tomando $x = 1$:
> $$\mathbf{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$$
> 
> 5. Determinamos el autovector $\mathbf{v}_2 = \begin{pmatrix} x \\ y \end{pmatrix}$ asociado a $\lambda_2 = 1$:
> Sustituimos $\lambda = 1$ en $(A - 1I)\mathbf{v} = \mathbf{0}$:
> $$\begin{pmatrix} 3 - 1 & 1 \\ 2 & 2 - 1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix} \implies \begin{pmatrix} 2 & 1 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$$
> Obtenemos la ecuación $2x + y = 0 \implies y = -2x$. Tomando $x = 1$:
> $$\mathbf{v}_2 = \begin{pmatrix} 1 \\ -2 \end{pmatrix}$$
> 
> **Solución:** Los autovalores de la matriz son $\lambda_1 = 4$ y $\lambda_2 = 1$, con autovectores asociados $\mathbf{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$ y $\mathbf{v}_2 = \begin{pmatrix} 1 \\ -2 \end{pmatrix}$.

---

## 3. Matriz de Paso y Diagonalización

### 3.1. Teorema de Diagonalización y Matriz de Paso
**Definición.** Una matriz cuadrada $A \in \mathbb{R}^{n \times n}$ es **diagonalizable** si existe una matriz invertible $P$ (matriz de paso) y una matriz diagonal $D$ tales que:
$$A = P \cdot D \cdot P^{-1} \quad \text{o, equivalentemente,} \quad D = P^{-1} \cdot A \cdot P$$

**Propiedad.** Una matriz $A$ de orden $n$ es diagonalizable si y solo si posee $n$ autovectores linealmente independientes. Si todos sus autovalores son reales y distintos, la matriz es directamente diagonalizable.

**Algoritmo de diagonalización :**
1. Formar la matriz diagonal $D$ situando los autovalores $\lambda_1, \dots, \lambda_n$ en la diagonal principal:
$$D = \begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$$
2. Construir la matriz de paso $P$ disponiendo los autovectores asociados por columnas en el mismo orden:
$$P = \begin{pmatrix} \mathbf{v}_1 & \mathbf{v}_2 \end{pmatrix}$$
3. Obtener la matriz inversa $P^{-1}$ mediante el método de reducción de Gauss-Jordan sobre la matriz ampliada $(P \mid I)$.

---

> [!example] Ejemplo 3.1: Obtención de las matrices $P$, $D$ e inversa $P^{-1}$
> Obtener la matriz diagonal $D$, la matriz de paso $P$ y su inversa $P^{-1}$ para la matriz $A = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix}$.
> 
> **Desarrollo paso a paso:**
> 1. Formamos la matriz diagonal $D$ con los autovalores $\lambda_1 = 4$ y $\lambda_2 = 1$:
> $$D = \begin{pmatrix} 4 & 0 \\ 0 & 1 \end{pmatrix}$$
> 
> 2. Formamos la matriz de paso $P$ alineando los autovectores $\mathbf{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$ y $\mathbf{v}_2 = \begin{pmatrix} 1 \\ -2 \end{pmatrix}$ como columnas:
> $$P = \begin{pmatrix} 1 & 1 \\ 1 & -2 \end{pmatrix}$$
> 
> 3. Calculamos la inversa $P^{-1}$ aplicando Gauss-Jordan a la matriz ampliada $(P \mid I)$:
> $$\begin{pmatrix} 1 & 1 & \big| & 1 & 0 \\ 1 & -2 & \big| & 0 & 1 \end{pmatrix}$$
> Restamos la fila 1 a la fila 2 ($F_2 \leftarrow F_2 - F_1$):
> $$\begin{pmatrix} 1 & 1 & \big| & 1 & 0 \\ 0 & -3 & \big| & -1 & 1 \end{pmatrix}$$
> Dividimos la fila 2 por $-3$ ($F_2 \leftarrow -\frac{1}{3} F_2$):
> $$\begin{pmatrix} 1 & 1 & \big| & 1 & 0 \\ 0 & 1 & \big| & \frac{1}{3} & -\frac{1}{3} \end{pmatrix}$$
> Restamos la fila 2 a la fila 1 ($F_1 \leftarrow F_1 - F_2$):
> $$\begin{pmatrix} 1 & 0 & \big| & \frac{2}{3} & \frac{1}{3} \\ 0 & 1 & \big| & \frac{1}{3} & -\frac{1}{3} \end{pmatrix}$$
> Extraemos la matriz inversa de la mitad derecha:
> $$P^{-1} = \begin{pmatrix} \frac{2}{3} & \frac{1}{3} \\[4pt] \frac{1}{3} & -\frac{1}{3} \end{pmatrix} = \frac{1}{3} \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$
> 
> **Solución:** La matriz diagonal es $D = \begin{pmatrix} 4 & 0 \\ 0 & 1 \end{pmatrix}$, la matriz de paso es $P = \begin{pmatrix} 1 & 1 \\ 1 & -2 \end{pmatrix}$ y la matriz de paso inversa es $P^{-1} = \frac{1}{3} \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$.

---

## 4. Aplicaciones del Cálculo Matricial y Resolución del Modelo

### 4.1. Potencias Matriciales por Diagonalización
**Propiedad.** Utilizando la relación de semejanza $A = P \cdot D \cdot P^{-1}$, la potencia $n$-ésima de la matriz $A$ se simplifica a:
$$A^n = (P \cdot D \cdot P^{-1})^n = P \cdot D^n \cdot P^{-1}$$
donde la potencia de la matriz diagonal se calcula de forma directa elevando sus elementos diagonales a $n$:
$$D^n = \begin{pmatrix} \lambda_1^n & 0 \\ 0 & \lambda_2^n \end{pmatrix}$$

**Método de cálculo de $A^n$.**
1. Elevar los autovalores en la matriz diagonal a la potencia $n$: $D^n$.
2. Multiplicar $P$ por $D^n$.
3. Multiplicar el resultado anterior por $P^{-1}$.

---

### 4.2. Solución Completa del Sistema Dinámico
**Método.** Para hallar el estado final de las poblaciones tras $n$ años, aplicamos la fórmula explícita $\mathbf{X}_n = \left( P \cdot D^n \cdot P^{-1} \right) \cdot \mathbf{X}_0$.

---

> [!example] Ejemplo 4.1: Cálculo de $A^{20}$ y resolución de la población tras 20 años
> Calcular la potencia $A^{20}$ para la matriz $A = \begin{pmatrix} 3 & 1 \\ 2 & 2 \end{pmatrix}$ y obtener el tamaño exacto de las poblaciones $x_{20}$ e $y_{20}$ transcurridos 20 años partiendo de $x_0 = 5$, $y_0 = 2$.
> 
> **Desarrollo paso a paso:**
> 1. Expresamos la potencia matricial $A^{20} = P \cdot D^{20} \cdot P^{-1}$:
> $$A^{20} = \begin{pmatrix} 1 & 1 \\ 1 & -2 \end{pmatrix} \begin{pmatrix} 4^{20} & 0 \\ 0 & 1^{20} \end{pmatrix} \cdot \frac{1}{3} \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$$
> 
> 2. Calculamos primero el producto $P \cdot D^{20}$ (con $1^{20} = 1$):
> $$P \cdot D^{20} = \begin{pmatrix} 1 & 1 \\ 1 & -2 \end{pmatrix} \begin{pmatrix} 4^{20} & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 4^{20} & 1 \\ 4^{20} & -2 \end{pmatrix}$$
> 
> 3. Multiplicamos por la matriz inversa $P^{-1}$:
> $$A^{20} = \frac{1}{3} \begin{pmatrix} 4^{20} & 1 \\ 4^{20} & -2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix} = \frac{1}{3} \begin{pmatrix} 2 \cdot 4^{20} + 1 & 4^{20} - 1 \\ 2 \cdot 4^{20} - 2 & 4^{20} + 2 \end{pmatrix} = \begin{pmatrix} \frac{2 \cdot 4^{20} + 1}{3} & \frac{4^{20} - 1}{3} \\[6pt] \frac{2 \cdot 4^{20} - 2}{3} & \frac{4^{20} + 2}{3} \end{pmatrix}$$
> 
> 4. Multiplicamos la matriz de potencia $A^{20}$ por el vector poblacional inicial $\mathbf{X}_0 = \begin{pmatrix} 5 \\ 2 \end{pmatrix}$:
> $$\mathbf{X}_{20} = A^{20} \begin{pmatrix} 5 \\ 2 \end{pmatrix} = \begin{pmatrix} \frac{2 \cdot 4^{20} + 1}{3} & \frac{4^{20} - 1}{3} \\[6pt] \frac{2 \cdot 4^{20} - 2}{3} & \frac{4^{20} + 2}{3} \end{pmatrix} \begin{pmatrix} 5 \\ 2 \end{pmatrix}$$
> 
> 5. Evaluamos cada componente de $\mathbf{X}_{20} = \begin{pmatrix} x_{20} \\ y_{20} \end{pmatrix}$:
> $$x_{20} = 5 \cdot \left( \frac{2 \cdot 4^{20} + 1}{3} \right) + 2 \cdot \left( \frac{4^{20} - 1}{3} \right) = \frac{10 \cdot 4^{20} + 5 + 2 \cdot 4^{20} - 2}{3} = \frac{12 \cdot 4^{20} + 3}{3} = 4 \cdot 4^{20} + 1 = 4^{21} + 1$$
> 
> $$y_{20} = 5 \cdot \left( \frac{2 \cdot 4^{20} - 2}{3} \right) + 2 \cdot \left( \frac{4^{20} + 2}{3} \right) = \frac{10 \cdot 4^{20} - 10 + 2 \cdot 4^{20} + 4}{3} = \frac{12 \cdot 4^{20} - 6}{3} = 4 \cdot 4^{20} - 2 = 4^{21} - 2$$
> 
> **Solución:** La matriz elevada a la potencia 20 es $A^{20} = \begin{pmatrix} \frac{2 \cdot 4^{20} + 1}{3} & \frac{4^{20} - 1}{3} \\[6pt] \frac{2 \cdot 4^{20} - 2}{3} & \frac{4^{20} + 2}{3} \end{pmatrix}$ y el tamaño final de las poblaciones tras 20 años es $\mathbf{x_{20} = 4^{21} + 1}$ e $\mathbf{y_{20} = 4^{21} - 2}$.

