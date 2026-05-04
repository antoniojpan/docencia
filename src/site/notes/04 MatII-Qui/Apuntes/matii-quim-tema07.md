---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema07/","created":"2026-01-08T10:24:16.931+01:00","updated":"2026-05-04T13:07:06.180+02:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 7: Sistemas de EDOs
- [[04 MatII-Qui/Apuntes/matii-quim-tema07#Introducción\|Introducción]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema07#Sistemas homogéneos: forma general\|Sistemas homogéneos: forma general]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema07#Caso no homogéneo: variación de constantes\|Caso no homogéneo: variación de constantes]]

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



[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].