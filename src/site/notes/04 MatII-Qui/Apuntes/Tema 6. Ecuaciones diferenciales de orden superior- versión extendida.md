---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/tema-6-ecuaciones-diferenciales-de-orden-superior-version-extendida/","updated":"2025-11-08T15:53:54.410+01:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 6: Ecuaciones Diferenciales de Orden Superior
- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Conceptos Básicos\|Conceptos Básicos]]
- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Wronskiano y el EDOs lineales homogéneas\|Wronskiano y el EDOs lineales homogéneas]]
- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Ecuaciones Lineales Homogéneas con Coeficientes Constantes\|Ecuaciones Lineales Homogéneas con Coeficientes Constantes]]
- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Ecuaciones Lineales No Homogéneas con Coeficientes Constantes\|Ecuaciones Lineales No Homogéneas con Coeficientes Constantes]]
	- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Ecuaciones Lineales No Homogéneas con Coeficientes Constantes\|Método de Variación de Constantes]]
	- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Ecuaciones Lineales No Homogéneas con Coeficientes Constantes\|Método de los Coeficientes Indeterminados]]
- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Aplicaciones: Modelos de Movimientos Vibratorios\|Aplicaciones: Modelos de Movimientos Vibratorios]]
	- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Aplicaciones: Modelos de Movimientos Vibratorios\|Movimiento Armónico Simple]]
	- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Aplicaciones: Modelos de Movimientos Vibratorios\|Movimiento Amortiguado]]
	- [[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales de orden superior- versión extendida#Aplicaciones: Modelos de Movimientos Vibratorios\|Movimiento Forzado]]

([[04 MatII-Qui/Apuntes/Tema 6. Ecuaciones diferenciales ordinarias de orden superior\|versión reducida]])

---
## Conceptos Básicos
Una **ecuación diferencial de orden superior** es una ecuación que involucra derivadas de una función desconocida de orden mayor o igual a dos:
$$ F(x, y, y', y'', ..., y^{(n)}) = 0 $$
**El PVI y el Teorema de Existencia y Unicidad**
Un problema de valores iniciales (PVI) de orden superior para EDOs lineales es una ecuación diferencial lineal junto con los valores de la incógnita y sus $n-1$ primeras derivadas en un punto, según el siguiente esquema:
$$
\begin{cases}
y^{(n)} = F(x, y, y', \dots, y^{(n-1)}) \\
y(x_0) = y_0 \\
y'(x_0) = y_1 \\
\vdots \\
y^{(n-1)}(x_0) = y_{n-1}
\end{cases}
$$

El **teorema de existencia y unicidad** establece que si exigimos ciertas condiciones de continuidad para $F$ entonces existe una única solución que satisface estas condiciones iniciales.

Se dice que una ecuación es **lineal**, si tiene la forma:
$$ 
a_n(x)y^{(n)} + a_{n-1}(x)y^{(n-1)} + \dots + a_1(x)y' + a_0(x)y = g(x),
$$
donde los coeficientes $a_i(x)$ pueden ser funciones de $x$, y $g(x)$ es el término no homogéneo.

Si $g(x) = 0$, la ecuación es **homogénea**. Si las funciones $a_n(x), a_{n-1}(x), ..., a_0(x)$ son todas constantes, se dice que la EDO es de **coeficientes constantes**. En caso contrario, se dice que la EDO es de **coeficientes variables**.

**Ejemplos:**
1.  $4y'' + 7xy' - \sqrt{x}y = x^4$
2.  $4y''' + 3y'' - y' + 7y = 0$
3.  $7x^3y''' + 8x^2y'' - e^xxy' + \frac{y}{x} = 0$
4.  $9y'' + y + \ln(x) = 0$


En lo que sigue, vamos a centrarnos en ecuaciones lineales con coeficientes constantes
$$ 
a_ny^{(n)} + a_{n-1}y^{(n-1)} + \dots + a_1y' + a_0y = g(x),
$$
## Wronskiano y el EDOs lineales homogéneas
**Definición:** Se dice que un conjunto de funciones ${f_1(x), f_2(x), ..., f_n(x)}$ es **linealmente dependiente** en un intervalo I si existen unas constantes $c_1, c_2, ..., c_n$ no todas nulas tales que
$$
c_1f_1(x) + c_2f_2(x) + ... + c_nf_n(x) = 0.
$$

En caso contrario decimos que el conjunto ${f_1(x), f_2(x), ..., f_n(x)}$ es **linealmente independiente**. Caso particular de [[functional dependence\|functional dependence]].

**Ejemplo**. Decidir si el conjunto formado por las funciones $f_1(x) = x + 2$ y $f_2(x) = x - 2$, es linealmente independiente. $\blacksquare$

**Ejemplo**. Comprobar si el conjunto formado por las funciones $f_1(x) = x(1 - x)$, $f_2(x) = x^2(1 - x)$ y $f_3(x) = x(1 - x)^2$, es linealmente independiente.$\blacksquare$

El [[Wronskian\|Wroskiano]] de un conjunto de funciones $y_1, y_2, ..., y_n$ se define como el determinante:
$$ 
W(y_1, y_2, ..., y_n) = \begin{vmatrix} y_1 & y_2 & \cdots & y_n \\ y_1' & y_2' & \cdots & y_n' \\ \vdots & \vdots & \ddots & \vdots \\ y_1^{(n-1)} & y_2^{(n-1)} & \cdots & y_n^{(n-1)} \end{vmatrix} 
$$

**Teorema**. Si $W \neq 0$, las funciones son linealmente independientes.$\blacksquare$

**Definición**. Se denomina **sistema fundamental de soluciones** (SFS) de una ecuación diferencial lineal homogénea de orden $n$ a cualquier conjunto de $n$ soluciones linealmente independientes.

**Ejemplo.** Demostrar que $y_1(x) = e^x$ y $y_2(x) = e^{9x}$ es un conjunto fundamental de soluciones de la ecuación $y'' - 10y' + 9y = 0$.


**Teorema (Principio de superposición lineal).** Sea $\{y_1, y_2, ..., y_n\}$ un conjunto fundamental de soluciones de una ecuación diferencial lineal homogénea. Entonces la solución general es
$$ 
y(x) = C_1 y_1(x) + C_2 y_2(x) + \cdots + C_n y_n(x), 
$$
donde $C_1, C_2, ..., C_n$ son constantes arbitrarias.

**Ejemplo**. La solución general de $y'' - 10y' + 9y = 0$ es $y=C_1 e^x+C_2e^{9x}$.

**Teorema**. Sea $y_p$ una solución particular de una ecuación diferencial lineal no homogénea, y $\{y_1, y_2, ..., y_n\}$ un conjunto fundamental de soluciones de la ecuación homogénea asociada. Entonces la solución general de la ecuación no homogénea es
$$
y(x) = C_1 y_1(x) + C_2 y_2(x) + \cdots + C_n y_n(x) + y_p(x),
$$
donde $C_1, C_2, ..., C_n$ son constantes arbitrarias e $y_p(x)$ es una solución particular de la ecuación no homogénea.

**Ejemplo**. Buscar una solución del problema de valores iniciales
$$
\begin{cases}
y'' - 10y' + 9y  = 9 \\
y(0) = 1 \\
y'(0) = 1
\end{cases}
$$

sabiendo que $y_p(x) = 1$ es una solución particular de la EDO.


---

## Ecuaciones Lineales Homogéneas con Coeficientes Constantes
Vamos a empezar por el caso más sencillo, $y'' + by' + cy = 0$. Suponemos que la solución tiene la forma $y = e^{\lambda x}$, donde $\lambda$ es un número complejo a determinar. Sustituyendo en la ecuación, obtenemos:
$$
\lambda^2 e^{\lambda x} + b \lambda e^{\lambda x} + c e^{\lambda x} = 0
$$
Dividiendo por $e^{\lambda x}$ (que no es cero), obtenemos la llamada ecuación característica:
$$
\lambda^2 + b \lambda + c = 0
$$
Denotamos sus raíces como $\lambda_1$ y $\lambda_2$, y se tienen los siguientes casos:

**Caso 1**: $\lambda_1$ y $\lambda_2$ son reales y diferentes. En este caso el SFS es
$$
y_1(x) = e^{\lambda_1 x}, \quad y_2(x) = e^{\lambda_2 x}
$$
y la solución general de la ecuación $y(x) = C_1 e^{\lambda_1 x} + C_2 e^{\lambda_2 x}, \quad C_1, C_2 \in \mathbb{R}$.

**Caso 2**: $\lambda_1 = \lambda_2$ es real. En este caso el SFS es
$$
y_1 = e^{\lambda_1 x}, \quad y_2(x) = xe^{\lambda_1 x},
$$
y la solución general de la ecuación $y(x) = C_1 e^{\lambda_1 x} + C_2 xe^{\lambda_1 x}, \quad C_1, C_2 \in \mathbb{R}$.

**Caso 3**: $\lambda_1$ y $\lambda_2$ son complejas conjugadas. Podemos escribirlas como
$$
\lambda_1 = \alpha + i\beta, \quad \lambda_2 = \alpha - i\beta.
$$
En este caso el SFS es
$$
y_1(x) = e^{\alpha x} \cos(\beta x), \quad y_2(x) = e^{\alpha x} \operatorname{sen}(\beta x).
$$

Y la solución general de la ecuación viene dada como

$$y(x) = C_1 e^{\alpha x} \cos(\beta x) + C_2 e^{\alpha x} \operatorname{sen}(\beta x), \quad C_1, C_2 \in \mathbb{R}.$$

**Ejemplo**: Resolver la ecuación diferencial $y'' + 2y' - 3y = 0$.

**Ejemplo**: Resolver la ecuación diferencial $y'' - 4y' + 4y = 0$.

**Ejemplo**: Resolver la ecuación diferencial $y'' - 2y' + 2y = 0$.

La técnica arriba explicada para ecuaciones de segundo orden, puede extenderse fácilmente a orden superior. Vamos a ver unos ejemplos:

**Ejemplo**: Buscar la solución general de la ecuación de tercer orden
$y''' + y'' + y' - 3y = 0$.

**Ejemplo**: Buscar la solución general de la ecuación de tercer orden
$y''' - 3y'' + 3y' - y = 0$.

**Ejemplo**: Buscar la solución general de la ecuación de cuarto orden
$y^{(iv)} - 2y'' + y = 0$.


---

## Ecuaciones Lineales No Homogéneas con Coeficientes Constantes
Consideramos la ecuación
$$
y'' + by' + cy = f(x).
$$
De acuerdo con lo que vimos en la sección anterior tenemos que si conocemos un conjunto fundamental de soluciones de la ecuación homogénea asociada, basta con determinar una solución particular de la no homogénea para conocer su solución general.

Introducimos, a continuación, dos métodos para determinar soluciones particulares de la ecuación anterior.

### Método de Variación de Constantes

Este método es más general y se puede aplicar a cualquier ecuación lineal no homogénea, siempre que se conozca un conjunto fundamental de soluciones de la ecuación homogénea asociada.
**Pasos:**
1.  Propón una solución particular de la forma $y_p(x) = u_1(x)y_1(x) + u_2(x)y_2(x)$, donde $u_1(x)$ y $u_2(x)$ son funciones desconocidas.
2.  Impón la condición auxiliar
$$
u_1'(x)y_1(x) + u_2'(x)y_2(x) = 0
$$
para simplificar el cálculo de las derivadas.
3.  Sustituye $y_p(x)$, $y_p'(x)$ y $y_p''(x)$ en la ecuación original. Se obtiene un sistema sencillo que permite resolver para $u_1'(x)$ y $u_2'(x)$.
4.  Integra $u_1'(x)$ y $u_2'(x)$ para encontrar $u_1(x)$ y $u_2(x)$. Finalmente, sustitúyelos en
$$
y_p(x) = u_1(x)y_1(x) + u_2(x)y_2(x)
$$
para obtener la solución particular.


**Ejemplo:** Resolver la ecuación diferencial:
$$
y'' - 5y' + 4y = e^x + 1.
$$

**Ejemplo:** Resolver el problema de valores iniciales:
$$
\begin{cases} y'' - 4y' + 4y = x \\ y(0) = 1 \\ y'(0) = -1 \end{cases}
$$

### Método de los Coeficientes Indeterminados
Este método es más sencillo, pero solo se puede aplicar a ecuaciones no homogéneas donde $f(x)$ tiene una forma específica (polinomios, exponenciales, senos, cosenos o combinaciones de estos).
**Pasos:**

1.  Basándote en la forma de $f(x)$, propón una solución particular $y_p(x)$ con coeficientes indeterminados.
    
| $f(x)$                          | Forma de $y_p(x)$ propuesta    |
| ------------------------------- | ------------------------------ |
| $a$                             | $A$                            |
| $ax + b$                        | $Ax + B$                       |
| $ax^2 + bx + c$                 | $Ax^2 + Bx + C$                |
| $e^{ax}$                        | $Ae^{ax}$                      |
| $e^{ax} (b x + c)$              | $e^{ax} (Ax + B)$              |
| $\sin(bx)$ o $\cos(bx)$         | $A\cos(bx) + B\sin(bx)$        |
| $x^m e^{ax}$                    | $e^{ax} (A_m x^m + ... + A_0)$ |
| $x^n \sin(bx)$ o $x^n \cos(bx)$ | $x^n (A\cos(bx) + B\sin(bx))$  |

2.  Calcula $y_p'(x)$ e $y_p''(x)$. Sustituye $y_p(x)$, $y_p'(x)$ e $y_p''(x)$ en la ecuación original.
3.  Iguala los coeficientes de términos similares en ambos lados de la ecuación. Resuelve el sistema de ecuaciones resultante para encontrar los coeficientes indeterminados.
4.  Sustituye los coeficientes encontrados en $y_p(x)$.


Generalización: [[Laplace transform\|Laplace transform]].

---

## Aplicaciones: Modelos de Movimientos Vibratorios

### Movimiento Armónico Simple
Un sistema masa-resorte sin fricción satisface la ecuación:
$$ 
m y'' + k y = 0 
$$
cuya solución es:
$$ 
y(t) = A \cos(\omega t) + B \sin(\omega t) 
$$
donde $\omega = \sqrt{k/m}$.

### Movimiento Amortiguado
Incluye un término de fricción:

$$ m y'' + b y' + k y = 0 $$

Las soluciones dependen del discriminante $\Delta = b^2 - 4mk$.

### Movimiento Forzado

Si hay una fuerza externa $F(t)$:

$$ m y'' + b y' + k y = F(t) $$

Las soluciones incluyen la respuesta transitoria y la respuesta estacionaria.


## Ejercicios
De la hoja del tema 6: 4, 7, 8, 10, 11, 12