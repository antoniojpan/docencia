---
{"dg-publish":true,"permalink":"/mat-ii-qui/apuntes/tema-7-sistemas-de-ecuaciones-diferenciales-ordinarias/","updated":"2025-09-15T17:21:14.234+02:00"}
---


[[MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 7: Sistemas de EDOs
- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Introducción\|Introducción]]
- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Sistemas homogéneos: forma general\|Sistemas homogéneos: forma general]]
	- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Sistemas homogéneos: forma general\|Caso 1: matriz diagonalizable (autovalores reales y distintos)]]
	- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Sistemas homogéneos: forma general\|Caso 2: autovalores complejos]]
	- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Sistemas homogéneos: forma general\|Caso 3: autovalores reales repetidos (deficiente)]]
	- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Sistemas homogéneos: forma general\|Resumen]]
- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Caso no homogéneo: variación de constantes\|Caso no homogéneo: variación de constantes]]
- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Ejercicios de la hoja.\|Ejercicios de la hoja.]]
- [[MatII-Qui/Apuntes/Tema 7. Sistemas de ecuaciones diferenciales ordinarias#Ejercicios nuevos.\|Ejercicios nuevos.]]


## Introducción
Los sistemas de ecuaciones diferenciales ordinarias (EDOs) son una herramienta fundamental para modelar fenómenos donde múltiples variables interactúan entre sí. Estos sistemas describen cómo evolucionan en el tiempo varias funciones incógnitas cuyos comportamientos están interconectados.  
Ejemplos:
- **Ecología**: Dinámica de poblaciones de especies que compiten o cooperan.  
- **Química**: Reacciones químicas con múltiples reactivos y productos acoplados.  
- **Física**: Sistemas mecánicos con grados de libertad interdependientes.  

**Ejemplo**
Lotka-Volterra.
Considera un sistema depredador-presa con dos poblaciones: presas $x(t)$ y depredadores $y(t)$. La dinámica se rige por las constantes $a, b, c, d > 0$, donde:
* $a$: tasa de crecimiento de las presas,
* $b$: tasa de depredación,
* $c$: tasa de muerte de los depredadores,
* $d$: tasa de crecimiento de los depredadores por consumo de presas.

El sistema resultante es:

$$
\begin{cases}
x'(t) = a x(t) - b x(t) y(t), \\
y'(t) = -c y(t) + d x(t) y(t).
\end{cases}
$$


**Ejemplo**
Considera la interconversión reversible entre dos especies químicas $X$ e $Y$, con concentraciones $x(t)$ e $y(t)$, respectivamente. La dinámica se rige por las constantes de velocidad $k_1$ y $k_2$ para las reacciones $X \rightarrow Y$ y $Y \rightarrow X$:
$$
X \underset{k_2}{\overset{k_1}{\rightleftharpoons}} Y
$$
El sistema resultante es:
$$
\begin{cases}
x'(t) = -k_1 x(t) + k_2 y(t), \\
y'(t) = \phantom{-}k_1 x(t) - k_2 y(t).
\end{cases}
$$


En este tema, nos centraremos en sistemas lineales homogéneos de orden dos con coeficientes constantes, es decir, sistemas de la forma:  
$$
\begin{cases}
x'(t) = a x(t) + b y(t), \\
y'(t) = c x(t) + d y(t),
\end{cases}
$$  
donde $a, b, c, d$ son constantes.  
## Sistemas homogéneos: forma general
Un sistema de EDOs lineales homogéneo de orden 2 con coeficientes constantes se puede escribir en la forma:
$$
X' = A X
$$
donde:
- $X = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix}$ es el vector de funciones incógnita.
- $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ es una matriz constante.

La solución depende de los autovalores ($\lambda$) y autovectores ($v$) de $A$.

### Caso 1: matriz diagonalizable (autovalores reales y distintos)
- **Autovalores**: $\lambda_1 \neq \lambda_2$ (reales).
- **Autovectores**: $v_1$ y $v_2$ asociados a $\lambda_1$ y $\lambda_2$.
- **Solución General**:
  $$
  X(t) = C_1 e^{\lambda_1 t} v_1 + C_2 e^{\lambda_2 t} v_2
  $$
  **Ejemplo**:
  Si $A = \begin{pmatrix} 0 & 4 \\ 1 & 0 \end{pmatrix}$, con $\lambda_1 = 2$, $\lambda_2 = -2$, y autovectores $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$, $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$, entonces:
  $$
  X(t) = C_1 e^{2t} \begin{pmatrix} 2 \\ 1 \end{pmatrix} + C_2 e^{-2t} \begin{pmatrix} -2 \\ 1 \end{pmatrix}.
  $$

---
### Caso 2: autovalores complejos
- **Autovalores**: $\lambda = \alpha \pm i\beta$.
- **Autovector**: $v = u \pm i w$, donde $u$ y $w$ son vectores reales.
- **Solución General**:
  $$
  X(t) = e^{\alpha t} \left( C_1 (u \cos(\beta t) - w \sin(\beta t)) + C_2 (w \cos(\beta t) + u \sin(\beta t)) \right)
  $$
  **Ejemplo**:
  Si $A = \begin{pmatrix} 4 & 4 \\ -1 & 4 \end{pmatrix}$, con $\lambda = 4 \pm 2i$ y autovector $\begin{pmatrix} 1 \\ \frac{i}{2} \end{pmatrix}$, entonces $u = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$, $w = \begin{pmatrix} 0 \\ \frac{1}{2} \end{pmatrix}$. La solución es:
  $$
  X(t) = e^{4t} \left( C_1 \begin{pmatrix} \cos(2t) \\ -\frac{1}{2} \sin(2t) \end{pmatrix} + C_2 \begin{pmatrix} \sin(2t) \\ \frac{1}{2} \cos(2t) \end{pmatrix} \right).
  $$

---

### Caso 3: autovalores reales repetidos (deficiente)
- **Autovalor**: $\lambda$ (doble) con un solo autovector linealmente independiente $v$.
- **Autovector Generalizado**: Resolver $(A - \lambda I)w = v$ para encontrar $w$.
- **Solución General**:
  $$
  X(t) = C_1 e^{\lambda t} v + C_2 e^{\lambda t} (t v + w)
  $$
  **Ejemplo**:
  Si $A = \begin{pmatrix} 3 & 4 \\ -1 & 7 \end{pmatrix}$, con $\lambda = 5$ (doble) y autovector $v = \begin{pmatrix} 1 \\ \frac{1}{2} \end{pmatrix}$, se busca $w$ tal que $(A - 5I)w = v$. La solución es:
  $$
  X(t) = C_1 e^{5t} \begin{pmatrix} 1 \\ \frac{1}{2} \end{pmatrix} + C_2 e^{5t} \left( t \begin{pmatrix} 1 \\ \frac{1}{2} \end{pmatrix} + \begin{pmatrix} \frac{3}{2} \\ 1 \end{pmatrix} \right).
  $$

---



### Resumen

| **Caso**              | **Condición**                    | **Método de Solución**                   |
| --------------------- | -------------------------------- | ---------------------------------------- |
| Diagonalizable        | $\lambda_1 \neq \lambda_2$       | Autovalores y autovectores.              |
| Autovalor deficiente  | $\lambda$ repetido, 1 autovector | Autovector generalizado.                 |
| Autovalores complejos | $\lambda = \alpha \pm i\beta$    | Partes real e imaginaria del autovector. |


## Caso no homogéneo: variación de constantes
Si tenemos un sistema lineal **no homogéneo** con coeficientes constantes:
$$
X'(t) = A X(t) + F(t),
$$
donde $F(t)$ es un vector función conocido, la solución general se escribe como:
$$
X(t) = X_h(t) + X_p(t),
$$
donde:
* $X_h(t)$ es la solución general del sistema homogéneo $X' = AX$,
* $X_p(t)$ es **una solución particular** del sistema completo.

Usaremos el método de variación de constantes:
**Teorema.** Sea $\Phi(x)$ una matriz fundamental del sistema lineal homogéneo
$$
X' = AX,
$$
entonces una solución particular del sistema no homogéneo
$$
X' = AX + F(t),
$$
está dada por
$$
\boxed{
X_p(t) = \Phi(t) \int \Phi^{-1}(t) F(t) \, dt.
}
$$
$\blacksquare$


**Ejemplo**
Sea el sistema:
$$
X'(t) = \begin{pmatrix} 2 & 1 \\ 0 & 3 \end{pmatrix} X(t) + \begin{pmatrix} t \\ 1 \end{pmatrix}.
$$

**1. Sistema homogéneo:**
$$
X'(t) = \begin{pmatrix} 2 & 1 \\ 0 & 3 \end{pmatrix} X(t)
$$
**Matriz $A$:**
$$
A = \begin{pmatrix} 2 & 1 \\ 0 & 3 \end{pmatrix}
$$
**Autovalores:**
La matriz es triangular superior, así que los autovalores son directamente los elementos de la diagonal:
$$
\lambda_1 = 2, \quad \lambda_2 = 3
$$
**Vectores propios:**

* Para $\lambda_1 = 2$:

$$
(A - 2I) = \begin{pmatrix} 0 & 1 \\ 0 & 1 \end{pmatrix} \Rightarrow y = 0 \Rightarrow v_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}
$$

* Para $\lambda_2 = 3$:

$$
(A - 3I) = \begin{pmatrix} -1 & 1 \\ 0 & 0 \end{pmatrix} \Rightarrow x = y \Rightarrow v_2 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

**Solución general del sistema homogéneo:**
$$
X_h(t) = c_1 \begin{pmatrix} 1 \\ 0 \end{pmatrix} e^{2t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{3t}
$$

---

**2. Solución particular (Variación de constantes)**
La **matriz fundamental** construida con las soluciones del sistema homogéneo es:
$$
\Phi(t) = \begin{pmatrix} e^{2t} & e^{3t} \\ 0 & e^{3t} \end{pmatrix}
$$
**Inversa de $\Phi(t)$:**
$$
\Phi^{-1}(t) = \begin{pmatrix} e^{-2t} & -e^{-2t} \\ 0 & e^{-3t} \end{pmatrix}
$$

Multiplicamos $\Phi^{-1}(t)$ por el término no homogéneo:
$$
\Phi^{-1}(t) \begin{pmatrix} t \\ 1 \end{pmatrix} = 
\begin{pmatrix} e^{-2t} & -e^{-2t} \\ 0 & e^{-3t} \end{pmatrix} 
\begin{pmatrix} t \\ 1 \end{pmatrix} = 
\begin{pmatrix} e^{-2t}(t - 1) \\ e^{-3t} \end{pmatrix}
$$

Integramos componente a componente:

* Para la primera componente:
$$
\int e^{-2t}(t - 1)\,dt = \left( -\frac{1}{2}t + \frac{1}{4} \right)e^{-2t} + C
$$

* Para la segunda:

$$
\int e^{-3t} dt = -\frac{1}{3}e^{-3t} + C
$$

Multiplicamos por $\Phi(t)$ para obtener la solución particular:
$$
X_p(t) = \Phi(t) \int \Phi^{-1}(t) \begin{pmatrix} t \\ 1 \end{pmatrix} dt = 
\begin{pmatrix} e^{2t} & e^{3t} \\ 0 & e^{3t} \end{pmatrix}
\begin{pmatrix}
\left( -\frac{1}{2}t + \frac{1}{4} \right)e^{-2t} \\
-\frac{1}{3} e^{-3t}
\end{pmatrix}
$$

**Solución particular:**
$$
X_p(t) = \begin{pmatrix} -\frac{1}{2}t - \frac{1}{12} \\ -\frac{1}{3} \end{pmatrix}
$$

**Solución general del sistema:**
$$
X(t) = c_1 \begin{pmatrix} 1 \\ 0 \end{pmatrix} e^{2t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{3t} + \begin{pmatrix} -\frac{1}{2}t - \frac{1}{12} \\ -\frac{1}{3} \end{pmatrix}, \quad c_1, c_2 \in \mathbb{R}
$$



## Ejercicios de la hoja.
**Ejercicio 4a**
Determinar la solución general del sistema diferencial:

$$
\begin{cases}
\dfrac{dx}{dt} = 2x + 2y \\
\dfrac{dy}{dt} = x + 3y
\end{cases}
$$

La solución general es:

$$
Y(t) = c_1 \begin{pmatrix} -2 \\ 1 \end{pmatrix} e^t + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{4t}
$$

---

**Ejercicio 4b**
Determinar la solución general del sistema:

$$
\begin{cases}
\dfrac{dx}{dt} = -2x + 2y \\
\dfrac{dy}{dt} = 8x - 2y
\end{cases}
$$

La solución general es:

$$
Y(t) = c_1 \begin{pmatrix} 1 \\ 2 \end{pmatrix} e^{2t} + c_2 \begin{pmatrix} -1 \\ 2 \end{pmatrix} e^{-6t}
$$

---

**Ejercicio 5c**
Determinar la solución general del sistema:

$$
Y' = \begin{pmatrix} 12 & -9 \\ 4 & 0 \end{pmatrix} Y
$$

La solución general es:

$$
Y(t) = c_1 \begin{pmatrix} 3 \\ 2 \end{pmatrix} e^{6t} + c_2 \begin{pmatrix} 2 + 3t \\ 1 + 2t \end{pmatrix} e^{6t}
$$

---

**Ejercicio 6a**
Determinar la solución general del sistema:
$$
\begin{cases}
\dfrac{dx}{dt} = x + y \\
\dfrac{dy}{dt} = -2x + y
\end{cases}
$$

La solución general es:

$$
Y(t) = c_1 \begin{pmatrix} \cos(\sqrt{2}t) \\ -\sqrt{2} \sin(\sqrt{2}t) \end{pmatrix} e^t + c_2 \begin{pmatrix} \sin(\sqrt{2}t) \\ \sqrt{2} \cos(\sqrt{2}t) \end{pmatrix} e^t
$$

---

**Ejercicio 6b**
Determinar la solución general del sistema:

$$
\begin{cases}
\dfrac{dx}{dt} = 4x + 5y \\
\dfrac{dy}{dt} = -2x + 6y
\end{cases}
$$

La solución general es:

$$
Y(t) = c_1 \begin{pmatrix} 5\cos(3t) \\ \cos(3t) - 3\sin(3t) \end{pmatrix} e^{5t} + c_2 \begin{pmatrix} 5\sin(3t) \\ 3\cos(3t) + \sin(3t) \end{pmatrix} e^{5t}
$$

---

**Ejercicio 7**
Resolver el problema con condición inicial:

$$
Y' = \begin{pmatrix} \frac{1}{2} & 0 \\ 1 & -\frac{1}{2} \end{pmatrix} Y, \quad Y(0) = \begin{pmatrix} 3 \\ 5 \end{pmatrix}
$$

La solución es:

$$
Y(t) = \begin{pmatrix} 3 \\ 3 \end{pmatrix} e^{t/2} + \begin{pmatrix} 0 \\ 2 \end{pmatrix} e^{-t/2}
$$
**Ejercicio 9**
Calcular la solución general del siguiente sistema:
$$
Y' = \begin{pmatrix} -3 & 1 \\ 2 & -4 \end{pmatrix} Y + \begin{pmatrix} 3 \\ e^{-t} \end{pmatrix}
$$

**Solución:**
Se resuelve en dos partes:
**1. Sistema homogéneo asociado:**

$$
Y' = \begin{pmatrix} -3 & 1 \\ 2 & -4 \end{pmatrix} Y
$$

Los autovalores son $\lambda_1 = -5$, $\lambda_2 = -2$, con vectores propios:

$$
V_1 = \begin{pmatrix} 1 \\ -2 \end{pmatrix}, \quad V_2 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

Solución homogénea:

$$
Y_h(t) = c_1 \begin{pmatrix} 1 \\ -2 \end{pmatrix} e^{-5t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{-2t}
$$

**2. Solución particular (variación de constantes):**

$$
\Phi(t) = \begin{pmatrix} e^{-5t} & e^{-2t} \\ -2e^{-5t} & e^{-2t} \end{pmatrix}, \quad \Phi^{-1}(t) = \begin{pmatrix} \frac{1}{3}e^{5t} & -\frac{1}{3}e^{5t} \\ \frac{2}{3}e^{2t} & \frac{1}{3}e^{2t} \end{pmatrix}
$$

Multiplicación e integración dan:

$$
Y_p(t) = \begin{pmatrix} \frac{6}{5} + \frac{1}{4} e^{-t} \\ \frac{3}{5} + \frac{1}{2} e^{-t} \end{pmatrix}
$$

**Solución general:**

$$
Y(t) = c_1 \begin{pmatrix} 1 \\ -2 \end{pmatrix} e^{-5t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{-2t} + \begin{pmatrix} \frac{6}{5} + \frac{1}{4} e^{-t} \\ \frac{3}{5} + \frac{1}{2} e^{-t} \end{pmatrix}
$$

---

**Ejercicio 10**
Calcular la solución general del sistema:
$$
\begin{cases}
\frac{dx}{dt} = 2x - y \\
\frac{dy}{dt} = 3x - 2y + 4t
\end{cases}
$$

**Solución:**
**1. Sistema homogéneo asociado:**

$$
Y' = \begin{pmatrix} 2 & -1 \\ 3 & -2 \end{pmatrix} Y
$$

Autovalores: $\lambda_1 = -1$, $\lambda_2 = 1$
Vectores propios:

$$
V_1 = \begin{pmatrix} 1 \\ 3 \end{pmatrix}, \quad V_2 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

Solución homogénea:

$$
Y_h(t) = c_1 \begin{pmatrix} 1 \\ 3 \end{pmatrix} e^{-t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^{t}
$$

**2. Solución particular (variación de constantes):**
$$
\Phi(t) = \begin{pmatrix} e^{-t} & e^{t} \\ 3e^{-t} & e^{t} \end{pmatrix}, \quad \Phi^{-1}(t) = \begin{pmatrix} -\frac{1}{2}e^t & \frac{1}{2}e^t \\ \frac{3}{2}e^{-t} & -\frac{1}{2}e^{-t} \end{pmatrix}
$$
Multiplicando por el vector $F$ y luego integrando:
$$
\Phi^{-1}(t)
\begin{pmatrix}
0\\
4t
\end{pmatrix}
=
\begin{pmatrix}
2t\,e^t\\
-2t\,e^{-t}
\end{pmatrix}
\Rightarrow
\int \Phi^{-1}(t)
\begin{pmatrix}
0\\
4t
\end{pmatrix} dt
=
\begin{pmatrix}
2t\,e^t - 2e^t\\
2t\,e^{-t} + 2e^{-t}
\end{pmatrix}
$$

$$
\Rightarrow
Y_p(t) = \Phi(t)
\begin{pmatrix}
2t\,e^t - 2e^t\\
2t\,e^{-t} + 2e^{-t}
\end{pmatrix}
=
\begin{pmatrix}
4t\\
8t - 4
\end{pmatrix}
$$

**Solución general:**
$$
Y(t) = c_1 \begin{pmatrix} 1 \\ 3 \end{pmatrix} e^{-t} + c_2 \begin{pmatrix} 1 \\ 1 \end{pmatrix} e^t + \begin{pmatrix} 4t \\ 8t - 4 \end{pmatrix}
$$




## Ejercicios nuevos.
**Ejercicio 1**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 3x + 4y \\
\dfrac{dy}{dt} = -x + 2y
\end{cases}, \quad Y(0) = \begin{pmatrix} 1 \\ 0 \end{pmatrix}
$$
Solución:
$$
\begin{cases}
x(t) = e^{\frac{5}{2}t} \left( \cos\left(\frac{\sqrt{15}}{2}t\right) + \frac{1}{\sqrt{15}} \sin\left(\frac{\sqrt{15}}{2}t\right) \right) \\
y(t) = e^{\frac{5}{2}t} \left( -\frac{2}{\sqrt{15}} \sin\left(\frac{\sqrt{15}}{2}t\right) \right)
\end{cases}
$$


---

**Ejercicio 2**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = -2x + y \\
\dfrac{dy}{dt} = -x - 2y
\end{cases}, \quad Y(0) = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
$$
Solución:
$$
\begin{cases}
x(t) = e^{-2t} \sin(t) \\
y(t) = e^{-2t} \cos(t)
\end{cases}
$$


---

**Ejercicio 3**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 5x - 3y \\
\dfrac{dy}{dt} = 2x + y
\end{cases}, \quad Y(0) = \begin{pmatrix} 2 \\ -1 \end{pmatrix}
$$

Solución:
$$
\begin{cases}
x(t) = e^{3t} \left( 2\cos(\sqrt{2}t) + \frac{7\sqrt{2}}{2} \sin(\sqrt{2}t) \right) \\
y(t) = e^{3t} \left( -\cos(\sqrt{2}t) + 3\sqrt{2} \sin(\sqrt{2}t) \right)
\end{cases}
$$

---

**Ejercicio 4**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 4x + y \\
\dfrac{dy}{dt} = -2x + y
\end{cases}, \quad Y(0) = \begin{pmatrix} 2 \\ -1 \end{pmatrix}
$$
**Solución:**

$$
\begin{aligned}
x(t) &= e^{2t} \left(-1 + 3e^{t}\right) \\
y(t) &= -e^{2t} \left(-2 + 3e^{t}\right)
\end{aligned}
$$



---

**Ejercicio 5**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 5x - 2y \\
\dfrac{dy}{dt} = 4x + y
\end{cases}, \quad Y(0) = \begin{pmatrix} 0 \\ 3 \end{pmatrix}
$$
**Solución:**

$$
\begin{aligned}
x(t) &= -3e^{3t} \sin(2t) \\
y(t) &= 3e^{3t} \left(\cos(2t) - \sin(2t)\right)
\end{aligned}
$$


---

**Ejercicio 6**
Resolver el siguiente sistema con condición inicial:
$$
\begin{cases}
\dfrac{dx}{dt} = 2x + 5y \\
\dfrac{dy}{dt} = -3x + y
\end{cases}, \quad Y(0) = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

**Solución:**

$$
\begin{aligned}
x(t) &= \frac{1}{59} e^{\frac{3t}{2}} \left(59 \cos\left(\frac{\sqrt{59}t}{2}\right) + 11\sqrt{59} \sin\left(\frac{\sqrt{59}t}{2}\right)\right) \\
y(t) &= -\frac{1}{59} e^{\frac{3t}{2}} \left(-59 \cos\left(\frac{\sqrt{59}t}{2}\right) + 7\sqrt{59} \sin\left(\frac{\sqrt{59}t}{2}\right)\right)
\end{aligned}
$$

---

**Ejercicio 7**
Resuelve el PVI:
$$
\begin{cases}
\dfrac{dx}{dt} = 7x + y \\
\dfrac{dy}{dt} = -4x + 3y
\end{cases}, \quad \vec{x}(0) = \begin{pmatrix} 2 \\ -5 \end{pmatrix}
$$

**Solución.**
Autovalor doble $\lambda=5$. Autovector $(1,-2)^t$. Autovector generalizado: $(0,1)^t$.
$$
\vec{x}(t) = c_1 e^{5t} \begin{pmatrix} 1 \\ -2 \end{pmatrix} + c_2 \left( e^{5t} t \begin{pmatrix} 1 \\ -2 \end{pmatrix} + e^{5t} \begin{pmatrix} 0 \\ 1 \end{pmatrix} \right)
$$
$c_1=2, c_2=-1$.


---

**Ejercicio 8**
Resuelve el sistema:
$$
\begin{cases}
x'(t) = 2\,x(t) + 1\,y(t) + 3,\\[6pt]
y'(t) = 1\,x(t) + 2\,y(t) + 1.
\end{cases}
$$
sabiendo que $x(0)=1,y(0)=3$. Calcula $x(2),y(2)$
**Solución ejercicio 8**
En forma de matriz:
$$
\mathbf X' = A\,\mathbf X + \mathbf b,\quad
A = \begin{pmatrix}2&1\\1&2\end{pmatrix},\quad
\mathbf b=\begin{pmatrix}3\\1\end{pmatrix}.
$$
Solución del homogéneo
$$
\det(A-\lambda I)=
\begin{vmatrix}2-\lambda&1\\1&2-\lambda\end{vmatrix}
=(2-\lambda)^2-1
\;\Rightarrow\;\lambda_1=3,\;\lambda_2=1.
$$
* For $\lambda_1=3$: $(A-3I)\mathbf v=0$ gives $\mathbf v_1=(1,1)^T$.
* For $\lambda_2=1$: gives $\mathbf v_2=(1,-1)^T$.
Solución de la homogénea:
$$
\mathbf X_h(t)
= C_1\,e^{3t}\begin{pmatrix}1\\1\end{pmatrix}
+ C_2\,e^{\,t}\begin{pmatrix}1\\-1\end{pmatrix}.
$$
Buscamos ahora solución particular del no homogéneo:
$$
\mathbf X' = A\,\mathbf X + \mathbf b,
\quad
A = \begin{pmatrix}2 & 1\\[4pt]1 & 2\end{pmatrix},
\quad
\mathbf b=\begin{pmatrix}3\\1\end{pmatrix}.
$$
usando
$$
X_p(t)=\Phi(t)\,\int \Phi(t)^{-1}F\,dt,
$$


1. **Calcular $\Phi^{-1}(t)$.**

$$
\Phi(t)
=\begin{pmatrix}e^{3t}&e^t\\e^{3t}&-e^t\end{pmatrix},\qquad
\det\Phi=-2e^{4t},
$$

por lo que
$$
\Phi^{-1}(t)
=\frac1{-2e^{4t}}
\begin{pmatrix}-e^t&-e^t\\-e^{3t}&e^{3t}\end{pmatrix}
=
\begin{pmatrix}
\dfrac1{2e^{3t}}&\dfrac1{2e^{3t}}\\[6pt]
\dfrac1{2e^t}&-\dfrac1{2e^t}
\end{pmatrix}.
$$

2. **Multiplicar $\Phi^{-1}F$.**
$$
\Phi^{-1}F
=\begin{pmatrix}
\dfrac1{2e^{3t}}&\dfrac1{2e^{3t}}\\[4pt]
\dfrac1{2e^t}&-\dfrac1{2e^t}
\end{pmatrix}
\begin{pmatrix}3\\1\end{pmatrix}
=
\begin{pmatrix}
\dfrac{3+1}{2e^{3t}}\\[6pt]
\dfrac{3-1}{2e^t}
\end{pmatrix}
=
\begin{pmatrix}
2e^{-3t}\\[4pt]
e^{-t}
\end{pmatrix}.
$$

3. **Integrar componente a componente.**
$$
\int\Phi^{-1}F\,dt
=\int
\begin{pmatrix}
2e^{-3t}\\
e^{-t}
\end{pmatrix}
dt
=
\begin{pmatrix}
-\,\tfrac{2}{3}e^{-3t}\\[6pt]
-\,e^{-t}
\end{pmatrix}.
$$

4. **Multiplicar por** $\Phi$.
$$
X_p(t)
=\Phi(t)\,
\begin{pmatrix}
-\tfrac{2}{3}e^{-3t}\\[6pt]
-\,e^{-t}
\end{pmatrix}
=
\begin{pmatrix}
e^{3t}&e^t\\[4pt]
e^{3t}&-e^t
\end{pmatrix}
\begin{pmatrix}
-\tfrac{2}{3}e^{-3t}\\[6pt]
-\,e^{-t}
\end{pmatrix}
=
\begin{pmatrix}
-\,\tfrac{5}{3}\\[6pt]
\;\tfrac{1}{3}
\end{pmatrix}.
$$

Por tanto, **una solución particular** del sistema es

$$
{X_p(t)=\begin{pmatrix}-\tfrac{5}{3}\\[4pt]\tfrac{1}{3}\end{pmatrix}.}
$$

Solución general:
$$
\boxed{\mathbf X(t)
= \mathbf X_h(t) + \mathbf X_p
= \underbrace{C_1e^{3t}\begin{pmatrix}1\\1\end{pmatrix}
+ C_2e^{t}\begin{pmatrix}1\\-1\end{pmatrix}}_{\text{homogeno}}
\;+\;\underbrace{\begin{pmatrix}\tfrac{5}{3}\\-\tfrac{1}{3}\end{pmatrix}}_{\text{particular}}.}
$$
En componentes:
$$
\boxed{
\begin{aligned}
x(t)&=-\frac{5}{3} \;+\;C_1\,e^{3t}\;+\;C_2\,e^{t},\\[6pt]
y(t)&=+\frac{1}{3} \;+\;C_1\,e^{3t}\;-\;C_2\,e^{t},
\end{aligned}
}
$$

Ahora queda aplicar los valores iniciales
$$
\begin{aligned}
x(0) &= -\frac{5}{3} + C_1 + C_2 = 1 \\
y(0) &= \frac{1}{3} + C_1 - C_2 = 3
\end{aligned}
$$

$$
\begin{aligned}
C_1 + C_2 &= \frac{8}{3} \quad \text{(1)} \\
C_1 - C_2 &= \frac{8}{3} \quad \text{(2)}
\end{aligned}
$$
Tenemos $C_1=8/3$ y $C_2=0$. Sustituimos:
$$
\begin{aligned}
x(t) &= -\frac{5}{3} + \frac{8}{3} e^{3t} \\
y(t) &= \frac{1}{3} + \frac{8}{3} e^{3t}
\end{aligned}
$$
Y ahora por fin 
$$
\begin{aligned}
x(2) &\approx \frac{8}{3} \cdot 403.429 - \frac{5}{3} \approx 1075.811, \\
y(2) &\approx \frac{8}{3} \cdot 403.429 + \frac{1}{3} \approx 1081.478
\end{aligned}
$$
[[MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].