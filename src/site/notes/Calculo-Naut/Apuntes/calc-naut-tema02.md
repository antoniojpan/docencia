---
{"dg-publish":true,"permalink":"/calculo-naut/apuntes/calc-naut-tema02/","updated":"2025-11-25T07:18:21.152+01:00"}
---

[[Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 2: Cálculo diferencial en varias variables
- [[Calculo-Naut/Apuntes/calc-naut-tema02#0. Introducción\|0. Introducción]]
- [[Calculo-Naut/Apuntes/calc-naut-tema02#1. Dominio de Funciones\|1. Dominio de Funciones]]
- [[Calculo-Naut/Apuntes/calc-naut-tema02#2. Derivadas Parciales y Diferenciabilidad\|2. Derivadas Parciales y Diferenciabilidad]]
- [[Calculo-Naut/Apuntes/calc-naut-tema02#3. Derivadas Direccionales, Gradiente y Regla de la Cadena\|3. Derivadas Direccionales, Gradiente y Regla de la Cadena]]
- [[Calculo-Naut/Apuntes/calc-naut-tema02#4. Plano Tangente y Recta Normal\|4. Plano Tangente y Recta Normal]]
- [[Calculo-Naut/Apuntes/calc-naut-tema02#5. Optimización de Funciones\|5. Optimización de Funciones]]

## 0. Introducción
Varias variables en varias variables:
$$
f:\mathbb R^n \to \mathbb R^m
$$
$$
(x,y,z,\ldots) \mapsto (f_1,f_2,\ldots)
$$
Ejemplos:
- Para cada punto de un mapa $(x,y)$ podemos dar su temperatura $T$: $$(x,y) \mapsto T(x,y)$$
- Para cada punto de un mapa $(x,y)$ podemos dar la velocidad del viento $v_1,v_2$: $$(x,y) \mapsto (v_1(x,y),v_2(x,y))$$
- Para cada valor de tiempo $t$ podemos dar un punto de un mapa $(x,y)$: $$t\mapsto (x(t),y(t))$$
## 1. Dominio de Funciones

El **dominio** de una función $f$ de varias variables, $Dom(f)$, es el conjunto de puntos $(x, y, \dots)$ del espacio $\mathbb{R}^n$ para los cuales la función está definida.

Para hallar el dominio, debemos identificar las operaciones que tienen restricciones:

1. **Denominadores:** El denominador no puede ser cero.
    
    - Si $f(x,y) = \frac{g(x,y)}{h(x,y)}$, se debe cumplir $h(x,y) \neq 0$.
        
2. **Raíces Cuadradas (y de índice par):** El argumento de la raíz (radicando) no puede ser negativo.
    
    - Si $f(x,y) = \sqrt{g(x,y)}$, se debe cumplir $g(x,y) \geq 0$.
        
3. **Logaritmos:** El argumento del logaritmo debe ser estrictamente positivo.
    
    - Si $f(x,y) = \log(g(x,y))$, se debe cumplir $g(x,y) > 0$.
        
4. **Funciones Trigonométricas Inversas:** (Como $arcsin, arccos$) sus argumentos están restringidos a $[-1, 1]$.
    

**Nota:** Funciones como polinomios, $e^{g(x,y)}$, $\sin(g(x,y))$ y $\cos(g(x,y))$ están definidas siempre que su argumento $g(x,y)$ lo esté.

## 2. Derivadas Parciales y Diferenciabilidad
En varias variables existen la correspondientes nociones de límite y de continuidad. Dado su dificultad técnica no serán tratadas aquí, sino que nos ocuparemos directamente de la generalización del concepto de derivada.

### Derivadas Parciales
La **derivada parcial** de $f(x,y)$ con respecto a $x$ en un punto $(a,b)$ se calcula tratando $y$ como una constante y derivando con respecto a $x$. Se denota $\frac{\partial f}{\partial x}(a,b)$ o $f_x(a,b)$.

- **Cálculo práctico:** 
	- Para hallar $\frac{\partial f}{\partial x}$, deriva $f$ con respecto a $x$ tratando $y$ como una constante.
	- Para hallar $\frac{\partial f}{\partial y}$, deriva $f$ con respecto a $y$ tratando $x$ como una constante.

### Diferenciabilidad
Una función $f$ es **diferenciable** en un punto $P_0 = (a,b)$ si sus derivadas parciales existen en $P_0$ y hay una buena aproximación de orden 1 de la función cerca de $P_0$
$$
P_f: (x,y)\mapsto f(a,b)+\begin{pmatrix} \frac{\partial f}{\partial x} \frac{\partial f}{\partial y}\end{pmatrix}\cdot \begin{pmatrix}x-a \\ y-b\end{pmatrix}
$$
**Ejemplo:**
Sea la función $f(x, y) = x^2 + y^3 - 5$ en el punto $P_0 = (1, 3)$.

1.  **Calculamos el valor de la función en el punto:**
$f(1, 3) = (1)^2 + (3)^3 - 5 = 1 + 27 - 5 = 23$

2.  **Calculamos las derivadas parciales:**

* $\frac{\partial f}{\partial x} = 2x$ (tratando $y^3 - 5$ como una constante)
* $\frac{\partial f}{\partial y} = 3y^2$ (tratando $x^2 - 5$ como una constante)

3.  **Evaluamos las derivadas parciales en el punto $(1, 3)$:**

* $\frac{\partial f}{\partial x}(1, 3) = 2(1) = 2$
* $\frac{\partial f}{\partial y}(1, 3) = 3(3)^2 = 3 \cdot 9 = 27$

4.  **Construimos la aproximación lineal $P_f$ (plano tangente):**
Usando la fórmula $P_f(x,y) = f(a,b) + \frac{\partial f}{\partial x}(a,b)(x-a) + \frac{\partial f}{\partial y}(a,b)(y-b)$:
$$
P_f: (x,y) \mapsto 23 + \begin{pmatrix} 2 & 27 \end{pmatrix}\\ \cdot \begin{pmatrix}x-1 \\ y-3 \end{pmatrix}
$$
de donde
$$P_f(x, y) = 2x + 27y - 60$$


**Condición Suficiente de Diferenciabilidad (Criterio práctico)**:
Si las derivadas parciales $\frac{\partial f}{\partial x}$ y $\frac{\partial f}{\partial y}$ existen y son continuas en un entorno (una región abierta) alrededor de un punto $(a,b)$, entonces $f$ es diferenciable en $(a,b)$.

**Ejemplo**: En el ejemplo anterior, dado que las derivadas parciales $f_x = 2x$ y $f_y = 3y^2$ son continuas en todo $\mathbb{R}^2$, la función $f$ es diferenciable en todos sus puntos, incluido el $(1, 3)$.

**Relaciones importantes:**
- Diferenciable $\implies$ Continua.
- Diferenciable $\implies$ Existen todas las derivadas parciales.
- El contrario no es cierto: que existan las derivadas parciales no implica diferenciabilidad


## 3. Derivadas Direccionales, Gradiente y Regla de la Cadena

### Vector Gradiente
El **vector gradiente** de una función $f$ en un punto $P$, denotado $\nabla f(P)$, es el vector de sus derivadas parciales.
- Para $f(x,y)$: $\nabla f(x,y) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right)$  
- Para $f(x,y,z)$: $\nabla f(x,y,z) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \right)$  

### Derivada Direccional
La **derivada direccional** de $f$ en un punto $P$ en la dirección de un **vector unitario** $\vec{u}$ mide la tasa de cambio de $f$ en esa dirección.
Cálculo:
$$D_{\vec{u}}f(P) = \nabla f(P) \cdot \vec{u}$$
(Es el producto escalar del gradiente por el vector unitario).

¡Importante! El vector de dirección $\vec{u}$ debe ser unitario ($\|\vec{u}\| = 1$). Si te dan una dirección $\vec{v}$ que no es unitaria (como en el Problema 4.2), primero debes normalizarla:
$$\vec{u} = \frac{\vec{v}}{\|\vec{v}\|}$$
donde $\|\vec{v}\| = \sqrt{v_1^2 + v_2^2 + \dots}$

### Propiedades del Gradiente
El gradiente $\nabla f(P)$ nos da información clave sobre el cambio de $f$ en el punto $P$:
1. **Máximo Crecimiento:** La dirección de máximo crecimiento (o "máxima pendiente") de $f$ es la dirección del propio vector gradiente, $\nabla f(P)$.
    - La _tasa_ de ese crecimiento (la derivada direccional máxima) es la norma del gradiente, $\|\nabla f(P)\|$.
2. **Máximo Decrecimiento:** La dirección de máximo decrecimiento de $f$ es la opuesta al gradiente, $-\nabla f(P)$.
    - La _tasa_ de ese decrecimiento es $-\|\nabla f(P)\|$.
3. **Sin Cambio:** La derivada direccional es cero en cualquier dirección perpendicular a $\nabla f(P)$.

### Regla de la Cadena
Se usa cuando las variables de una función dependen de otras.
Caso 1 (Problema 4.8): $z = f(u, v)$ donde $u = u(x,y)$ y $v = v(x,y)$.
$$\frac{\partial z}{\partial x} = \frac{\partial f}{\partial u}\frac{\partial u}{\partial x} + \frac{\partial f}{\partial v}\frac{\partial v}{\partial x}$$$$\frac{\partial z}{\partial y} = \frac{\partial f}{\partial u}\frac{\partial u}{\partial y} + \frac{\partial f}{\partial v}\frac{\partial v}{\partial y}$$
Caso 2 (Problema 4.9): $h(t) = f(x(t), y(t), z(t))$.
$$h'(t) = \frac{df}{dt} = \frac{\partial f}{\partial x}\frac{dx}{dt} + \frac{\partial f}{\partial y}\frac{dy}{dt} + \frac{\partial f}{\partial z}\frac{dz}{dt}$$
## 4. Plano Tangente y Recta Normal
Se usan para aproximar superficies. Hay dos casos comunes:

**Caso 1: Gráfica de una función** $z = f(x,y)$ **en** $P_0 = (x_0, y_0, z_0)$  
- Plano Tangente:
    
    $z - z_0 = \frac{\partial f}{\partial x}(x_0, y_0)(x - x_0) + \frac{\partial f}{\partial y}(x_0, y_0)(y - y_0)$
    
Coincide con la gráfica de la aproximación a $f$, $P_f$, vista anteriormente.

**Caso 2: Superficie implícita $F(x,y,z) = k$ en $P_0 = (x_0, y_0, z_0)$**
(Nota: El Caso 1 es un caso particular de éste si tomamos $F(x,y,z) = f(x,y) - z$ y $k=0$).
1. Calcula el vector gradiente de $F$ en $P_0$:    
    $\nabla F(P_0) = \left( \frac{\partial F}{\partial x}(P_0), \frac{\partial F}{\partial y}(P_0), \frac{\partial F}{\partial z}(P_0) \right)$
    Este vector es normal (perpendicular) a la superficie en $P_0$.
    
2. Ecuación del Plano Tangente:
    $\nabla F(P_0) \cdot (x-x_0, y-y_0, z-z_0) = 0$
    Es decir:
    $\frac{\partial F}{\partial x}(P_0)(x-x_0) + \frac{\partial F}{\partial y}(P_0)(y-y_0) + \frac{\partial F}{\partial z}(P_0)(z-z_0) = 0$
    
3. Ecuación de la Recta Normal (paramétrica):
    $\vec{r}(t) = (x_0, y_0, z_0) + t \cdot \nabla F(P_0)$

## 5. Optimización de Funciones

### Extremos Locales (Sin restricciones)
Para hallar los máximos, mínimos o puntos de silla de $f(x,y)$ en una región abierta.

Paso 1: Encontrar Puntos Críticos
Los puntos críticos son los candidatos a ser extremos. Son los puntos $(a,b)$ donde:
$$\nabla f(a,b) = (0,0)$$ 
(es decir, $\frac{\partial f}{\partial x} = 0$ y $\frac{\partial f}{\partial y} = 0$), o   

Paso 2: Clasificar Puntos Críticos (Criterio de la Segunda Derivada)
Calculamos el Hessiano, $D(x,y)$, en cada punto crítico $(a,b)$.
1. Calcula las segundas derivadas: $f_{xx}$, $f_{yy}$, $f_{xy}$.
    
2. Calcula el determinante de la matriz Hessiana:
$$
H(x,y)=\begin{pmatrix}f_{xx} & f_{xy} \\ f_{yx} & f_{yy}\end{pmatrix},
$$
es decir,
$$D(x,y) = f_{xx}(x,y) \cdot f_{yy}(x,y) - (f_{xy}(x,y))^2$$
3. En el punto crítico $(a,b)$:
    
    - Si $D(a,b) > 0$ y $f_{xx}(a,b) > 0$ $\implies$ **Mínimo Local**.
        
    - Si $D(a,b) > 0$ y $f_{xx}(a,b) < 0$ $\implies$ **Máximo Local**.
        
    - Si $D(a,b) < 0$ $\implies$ **Punto de Silla**.
        
    - Si $D(a,b) = 0$ $\implies$ El criterio no decide.
        

### Extremos Condicionados (Multiplicadores de Lagrange)
Para optimizar $f(x,y)$ sujeto a una restricción (ligadura) $g(x,y) = c$. (También funciona para $f(x,y,z)$ con $g(x,y,z) = c$).

**Pasos a seguir:**
1.  **Definir la función Lagrangiana:**
$$L(x, y, \lambda) = f(x, y) - \lambda (g(x, y) - c)$$
2.  **Construir la Matriz Hessiana Orlada ($\bar{H}$):**
    Esta matriz incluye las segundas derivadas de $L$ y las primeras derivadas de la restricción $g$.
    **Para 2 variables ($f(x,y)$ con $g(x,y)=c$):**
    $$
    \bar{H} = \begin{pmatrix}
    0 & g_x & g_y \\
    g_x & L_{xx} & L_{xy} \\
    g_y & L_{yx} & L_{yy}
    \end{pmatrix}
    $$
    Donde $g_x = \frac{\partial g}{\partial x}$, $L_{xx} = \frac{\partial^2 L}{\partial x^2} = f_{xx} - \lambda g_{xx}$, $L_{xy} = f_{xy} - \lambda g_{xy}$, etc.

3.  **Evaluar el Determinante:** Se evalúa $\det(\bar{H})$ en cada punto candidato $(x_0, y_0, \lambda_0)$ que encontraste.
    * Si $\det(\bar{H}) > 0$: El punto es un **Máximo Local**.
    * Si $\det(\bar{H}) < 0$: El punto es un **Mínimo Local**.
    * Si $\det(\bar{H}) = 0$: El criterio no concluye.

### Extremos Absolutos en Conjuntos Compactos (Cerrados y Acotados)

Para hallar el máximo y mínimo absoluto de una función continua $f$ en una región cerrada y acotada $A$ (como un disco, Problema 5.7).

**Método (Teorema de Weierstrass):**

1. **Interior:** Encuentra todos los puntos críticos de $f$ que estén _dentro_ de la región $A$ (usando el método de extremos locales $\nabla f = 0$).
    
2. **Frontera:** Encuentra los puntos extremos de $f$ _sobre la frontera_ de $A$. (Esto se hace usando Multiplicadores de Lagrange, donde la frontera es la restricción $g(x,y)=c$).
    
3. **Comparar:** Evalúa $f$ en todos los puntos obtenidos en los pasos 1 y 2.
    
    - El valor más grande es el **Máximo Absoluto**.
        
    - El valor más pequeño es el **Mínimo Absoluto**.


[[Calculo-Naut/Apuntes/calc-naut-tema02-ej\|Ejercicios]]
