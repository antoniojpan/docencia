---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema02/","created":"2026-01-08T10:24:16.931+01:00","updated":"2026-02-11T13:40:40.475+01:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 2. Métodos numéricos en ecuaciones de una variable

- [[04 MatII-Qui/Apuntes/matii-quim-tema02#1. Introducción\|1. Introducción]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema02#2. Separación de los ceros de una función\|2. Separación de los ceros de una función]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema02#3. Método de la bisección\|3. Método de la bisección]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema02#4. Método de la “regula falsi”\|4. Método de la “regula falsi”]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema02#5. Método de Newton-Raphson\|5. Método de Newton-Raphson]]
- [[04 MatII-Qui/Apuntes/matii-quim-tema02#6. Ejercicios\|6. Ejercicios]]

---
## 1. Introducción
Resolver ecuaciones es una tarea esencial en numerosas disciplinas (como la química, la ingeniería, la enología), donde los modelos matemáticos permiten predecir el resultado de procesos físicos, reacciones químicas o incluso la evolución de sistemas complejos. Sin embargo, en la mayoría de los casos, encontrar soluciones exactas no es una tarea sencilla.
Para ecuaciones de grado uno y dos, existen fórmulas que nos proporcionan las soluciones de manera directa, como la conocida ecuación cuadrática. Para polinomios de grado tres y cuatro también existen métodos exactos, aunque son mucho más complejos y poco prácticos. Pero a partir del grado cinco, el teorema de Abel-Ruffini establece que no siempre es posible encontrar una fórmula general que exprese las soluciones en términos de radicales.

Incluso cuando podemos aplicar el método de Ruffini para ciertos polinomios con raíces racionales, este proceso no siempre es viable, ya que no todas las ecuaciones tienen soluciones exactas expresables de manera sencilla. Además, muchas ecuaciones en la ciencia y la ingeniería no son polinómicas, sino trascendentes (como las que involucran exponenciales, logaritmos o funciones trigonométricas), lo que hace aún más difícil encontrar soluciones analíticas.

Por todas estas razones, en la práctica se recurre a métodos numéricos, que permiten encontrar aproximaciones a las soluciones con la precisión deseada. Tenemos métodos que consisten en construir una sucesión $x_0, x_1, x_2, \ldots, x_n, \ldots$ que converge al valor buscado, es decir,
$$
\lim_{n \to \infty} x_n = X.
$$
Un procedimiento de este tipo recibe el nombre de **algoritmo iterativo**. Con $n$ suficientemente grande, $x_n$ será una buena aproximación de la solución exacta $X$, y por tanto tomaremos:
$$
X \approx x_n.
$$
---

## 2. Separación de los ceros de una función
Antes de comenzar, tenemos que tener la certeza de que exista al menos una solución y que además sea única en el intervalo donde vayamos a trabajar, ya que de otro modo la sucesión podría no converger.

>**Teorema de Bolzano.**
>Sea $f(x)$ una función continua en $[a, b]$ tal que el signo de $f(a)$ es distinto del signo de $f(b)$ (es decir, $f(a) \cdot f(b) < 0$). Entonces existe al menos un punto $c \in (a, b)$ tal que $f(c) = 0$.

>**Teorema de Rolle.**
>Sea $f(x)$ una función continua en $[a, b]$ y derivable en $(a, b)$ tal que $f(a) = f(b)$. Entonces existe al menos un punto $c \in (a, b)$ tal que $f'(c) = 0$.

Considerando conjuntamente ambos teoremas, podemos demostrar la existencia y unicidad de solución de la ecuación $f(x) = 0$. Si $f$ es continua en $[a, b]$ y derivable en $(a, b)$, tal que $f(a) \cdot f(b) < 0$ y su derivada no cambia de signo en $(a, b)$, entonces la ecuación tiene una solución única.
El proceso de encontrar intervalos en los que estemos seguros de que existe una única solución de la ecuación recibe el nombre de **separación de soluciones**.
### Proceso para encontrar los intervalos deseados:
1. Comprobamos el signo en los extremos $a,b$ del intervalo dado (pueden ser $-\infty$ y $+\infty$)
2. Calculamos $f'(x)$ y los puntos críticos $x_1,\ldots,x_n$ (es decir, resolvemos $f'(x) = 0$).
3. Nos quedamos con aquellos puntos críticos que pertenezcan al intervalo $[a, b]$ y los ordenamos: $a < x_1 < \cdots < x_n < b$.
4. Evaluamos la función en dichos puntos, y nos quedamos con los intervalos donde hay cambio de signo. El número de intervalos que obtengamos será el número de ceros que tiene la función.

### Ejemplos
**Ejemplo 1:** Demostrar que la ecuación $x^3 - 6x + 2 = 0$ sólo tiene una solución en el intervalo $[-1, 1]$.
Para demostrar que la ecuación $x^3 - 6x + 2 = 0$ tiene una única solución en el intervalo $[-1, 1]$, seguimos el procedimiento:
1. **Evaluamos los extremos del intervalo:**
   - $f(-1) = (-1)^3 - 6(-1) + 2 = -1 + 6 + 2 = 7$ (positivo).
   - $f(1) = (1)^3 - 6(1) + 2 = 1 - 6 + 2 = -3$ (negativo).

   Hay un cambio de signo en $[-1, 1]$, lo que indica al menos una solución.
2. **Calculamos la derivada:**
   $$
   f'(x) = 3x^2 - 6.
   $$
   Resolviendo $f'(x) = 0$:
   $$
   3x^2 - 6 = 0 \implies x^2 = 2 \implies x = \pm \sqrt{2}.
   $$
   Los puntos críticos son $x = \sqrt{2}$ y $x = -\sqrt{2}$. Solo $x = -\sqrt{2} \approx -1.414$ está fuera del intervalo $[-1, 1]$, y $x = \sqrt{2} \approx 1.414$ también está fuera. Por lo tanto, no hay puntos críticos en $[-1, 1]$.
3. **Conclusión:**
   Como no hay puntos críticos en $[-1, 1]$ y hay un cambio de signo en los extremos, la función $f(x)$ es estrictamente decreciente en este intervalo. Por lo tanto, solo hay **una solución** en $[-1, 1]$. 

**Ejemplo 2:** Calcular cuántas soluciones tiene la ecuación $x^3 + 8x^2 - 3 = 0$ en el intervalo $[-10, 2]$.
Para determinar cuántas soluciones tiene la ecuación $x^3 + 8x^2 - 3 = 0$ en el intervalo $[-10, 2]$:
1. **Evaluamos los extremos del intervalo:**
   - $f(-10) = (-10)^3 + 8(-10)^2 - 3 = -1000 + 800 - 3 = -203$ (negativo).
   - $f(2) = (2)^3 + 8(2)^2 - 3 = 8 + 32 - 3 = 37$ (positivo).
   Hay un cambio de signo en $[-10, 2]$, lo que indica al menos una solución.
2. **Calculamos la derivada:**
   $$
   f'(x) = 3x^2 + 16x.
   $$
   Resolviendo $f'(x) = 0$:
   $$
   3x^2 + 16x = 0 \implies x(3x + 16) = 0 \implies x = 0 \text{ o } x = -\frac{16}{3}.
   $$
   Los puntos críticos son $x = 0$ y $x = -\frac{16}{3} \approx -5.333$. Ambos están dentro del intervalo $[-10, 2]$.
6. **Evaluamos la función en los puntos críticos:**
   - $f\left(-\frac{16}{3}\right) = \left(-\frac{16}{3}\right)^3 + 8\left(-\frac{16}{3}\right)^2 - 3 \approx -152.59 + 227.56 - 3 \approx 71.97$ (positivo).
   - $f(0) = 0 + 0 - 3 = -3$ (negativo).

   - En el intervalo $[-10, -\frac{16}{3}]$, $f(-10) = -203$ (negativo) y $f\left(-\frac{16}{3}\right) \approx 71.97$ (positivo). Hay un cambio de signo, por lo que hay **una solución** en este intervalo.
   - En el intervalo $[-\frac{16}{3}, 0]$, $f\left(-\frac{16}{3}\right) \approx 71.97$ (positivo) y $f(0) = -3$ (negativo). Hay otro cambio de signo, por lo que hay **una segunda solución** en este intervalo.
   - En el intervalo $[0, 2]$, $f(0) = -3$ (negativo) y $f(2) = 37$ (positivo). Hay un tercer cambio de signo, por lo que hay **una tercera solución** en este intervalo.
7. **Conclusión:**
   La ecuación tiene **tres soluciones** en el intervalo $[-10, 2]$.

En el resto del tema vamos a ver técnicas para aproximar las soluciones, una vez que las hemos separado.

---

## 3. Método de la bisección
Supongamos que partimos de una función $f(x)$ y un intervalo $[a, b]$ en el que sabemos que $f(a) \cdot f(b) < 0$. El método de la bisección consiste en construir una sucesión de intervalos encajados:
$$
[a, b] = [a_1, b_1] \supseteq [a_2, b_2] \supseteq \cdots \supseteq [a_n, b_n] \supseteq \cdots
$$
tales que $x \in [a_n, b_n]$ para $n = 1, 2, \ldots$ y $(b_{n+1} - a_{n+1}) = \frac{(b_n - a_n)}{2}$.
### Pasos del método:
1. Tomamos el punto medio del intervalo $[a_n, b_n]$:
$$
 x_n = \frac{a_n + b_n}{2}
 $$
2. Si $f(x_n) = 0$, entonces $x = c_n$ y hemos terminado.
3. Si $f(x_n) \neq 0$, entonces:
    a. Si $f(a_n) \cdot f(x_n) < 0$, escogemos como nuevo intervalo $[a_{n+1}, b_{n+1}] = [a_n, x_n]$.
    b. Si $f(x_n) \cdot f(b_n) < 0$, escogemos como nuevo intervalo $[a_{n+1}, b_{n+1}] = [x_n, b_n]$.
    c. Volvemos al paso 1 con el intervalo escogido.

Después de realizar $n$ pasos o iteraciones, la solución debe estar en el intervalo $[a_n, b_n]$ de longitud $\frac{(b - a)}{2^n}$. Si tomamos $x_n = \frac{(a_n + b_n)}{2}$ como aproximación de $X$, el error absoluto verifica:
$$
|x_n - X| \leq \frac{b - a}{2^{n+1}}.
$$
Para asegurarnos una aproximación con un error inferior a una tolerancia dada $\varepsilon$, debemos tomar $n$ tal que:
$$
\frac{b - a}{2^{n+1}} < \varepsilon,
$$
o equivalentemente:
$$
n > \log_2 \left( \frac{b - a}{\varepsilon} \right) - 1 \Rightarrow n > \frac{\log \left( \frac{b - a}{\varepsilon} \right)}{\log 2} - 1.
$$

### Ventajas y desventajas:
- **Ventajas:**
  - Es muy sencillo de calcular.
  - Permite decidir con anterioridad cuántas iteraciones hacen falta para controlar el error.
- **Desventajas:**
  - La convergencia es lenta, necesita muchas iteraciones para una buena aproximación.
### Ejemplo
Calcular cuatro aproximaciones con el método de la bisección del cero de la función $f(x) = x^4 + 2x^3 - 8x - 2$ en el intervalo $[1, 3]$. Calcular el número de iteraciones necesarias para que el error sea menor que $10^{-2}$.
Evaluamos la función en los extremos del intervalo:
$$
f(1) = -7
$$
$$
f(3) = 109
$$
Dado que $f(1) \cdot f(3) = (-7)(109) < 0$, por el **Teorema de Bolzano**, existe al menos un **cero en el intervalo $[1,3]$**.
**Iteración 1**
Punto medio:
$$
x_1 = \frac{1+3}{2} = 2
$$
Evaluamos $f(2)$:
$$
f(2) =  14
$$
Como $f(1) \cdot f(2) = (-7)(14) < 0$, tomamos el nuevo intervalo:
$$
[a_1, b_1] = [1,2]
$$
**Resto de iteraciones:**

| Iteración ($n$) | $a_n$ | $b_n$ | $x_n$ | $f(x_n)$ | Nuevo intervalo |
| --------------- | ----- | ----- | ----- | -------- | --------------- |
| 1               | 1     | 3     | 2     | 14       | $[1,2]$         |
| 2               | 1     | 2     | 1.5   | -2.1875  | $[1.5,2]$       |
| 3               | 1.5   | 2     | 1.75  | 4.0977   | $[1.5,1.75]$    |
| 4               | 1.5   | 1.75  | 1.625 | 0.584    | $[1.5,1.625]$   |

**Determinar el número de iteraciones necesarias para $\varepsilon = 10^{-2}$**
Queremos que el error cumpla:
$$
\frac{b-a}{2^{n+1}} < 10^{-2}
$$
Dado que $a = 1$ y $b = 3$, tenemos:
$$
\frac{2}{2^{n+1}} < 10^{-2}
$$
$$
2^{n+1} > \frac{2}{10^{-2}} = 200
$$
$$
n+1 > \log_2(200) \approx \frac{\log 200}{\log 2} = \frac{2.301}{0.301} \approx 7.64
$$
$$
n > 6.64
$$
Como $n$ debe ser entero, tomamos $n = 7$.

---

## 4. Método de la “regula falsi”
El método de la falsa posición o “regula falsi” consiste en dividir el intervalo $[a, b]$ en dos intervalos más pequeños de modo que uno de ellos contenga la solución $\bar{x}$, haciendo aproximaciones a través de la recta que une los puntos $(a, f(a))$ y $(b, f(b))$.
### Pasos del método:
1. Consideramos la recta que pasa por los puntos $(a_n, f(a_n))$ y $(b_n, f(b_n))$:  
$$
   y(x) = \frac{f(b_n) - f(a_n)}{b_n - a_n} (x - b_n) + f(b_n).
   $$
y definimos $x_n$ tal que $y(x_n) = 0$, es decir:
$$
   x_n = b_n - \frac{b_n - a_n}{f(b_n) - f(a_n)} f(b_n).
   $$
2. Tomamos el nuevo intervalo $[a_{n+1}, b_{n+1}]$ de acuerdo con:
 - Si $f(a_n) \cdot f(x_n) < 0$, escogemos como nuevo intervalo $[a_{n+1}, b_{n+1}] = [a_n, x_n]$.
- Si $f(x_n) \cdot f(b_n) < 0$, escogemos como nuevo intervalo $[a_{n+1}, b_{n+1}] = [x_n, b_n]$.
- Volvemos al paso 2 con el intervalo escogido.

### Criterio de paro:
En este método, los intervalos no tienen la misma longitud, por lo que no podemos encontrar un criterio para determinar el número de iteraciones necesarias para parar el método dada una tolerancia $\varepsilon$. El criterio de paro será:
$$
|x_n - x_{n+1}| < \varepsilon.
$$

### Ventajas y desventajas:
- **Ventajas:**
  - Converge más rápido que el método de la bisección.
- **Desventajas:**
  - No se puede predecir el número mínimo de iteraciones necesarias para acotar el error.


### Ejemplo 1
Calcular cuatro aproximaciones con el método de la falsa posición (regula falsi) del cero de la función $f(x) = x^4 + 2x^3 - 8x - 2$ en el intervalo $[1, 3]$.
Evaluamos la función en los extremos del intervalo inicial:
$$f(1) = -7$$
$$f(3) = 109$$
Como $f(1) \cdot f(3) < 0$, existe una raíz en el intervalo $[1, 3]$.
**Iteración 1**
Aplicamos la fórmula de la secante para encontrar $x_1$:
$$x_1 = b_1 - \frac{b_1 - a_1}{f(b_1) - f(a_1)} f(b_1)$$
Sustituyendo $a_1 = 1$ y $b_1 = 3$:
$$x_1 = 3 - \frac{3 - 1}{109 - (-7)} \cdot 109 = 3 - \frac{2}{116} \cdot 109 \approx 3 - 1.8793 = 1.1207$$
Evaluamos $f(x_1)$:
$$f(1.1207) \approx (1.1207)^4 + 2(1.1207)^3 - 8(1.1207) - 2 \approx -6.575$$
Nuevo intervalo:
$$[a_2, b_2] = [1.1207, 3]$$
**Resto de iteraciones:**

| **Iteración (n)** | **an​** | **bn​** | **xn​** | **f(xn​)** | **Nuevo intervalo** |
| ----------------- | ------- | ------- | ------- | ---------- | ------------------- |
| 1                 | 1       | 3       | 1.1207  | -6.575     | $[1.1207, 3]$       |
| 2                 | 1.1207  | 3       | 1.2276  | -5.850     | $[1.2276, 3]$       |
| 3                 | 1.2276  | 3       | 1.3178  | -5.046     | $[1.3178, 3]$       |
| 4                 | 1.3178  | 3       | 1.3922  | -4.234     | $[1.3922, 3]$       |

Valor de la raíz: $x\approx 1.602299$. En este caso gana el método de la bisección por la forma de la función.

### Ejemplo 2
Aproximar la solución de la ecuación $3x + 1 + \sin(x) = 0$ en el intervalo $[-1,1]$ mediante 2 iteraciones del método de la "regula falsi".

| Iteración | $a_n$               | $b_n$ | $x_n$               | Error                |
| --------- | ------------------- | ----- | ------------------- | -------------------- |
| 1         | -1.0                | 1.0   | -0.2603169473242832 | 0.2603169473242832   |
| 2         | -0.2603169473242832 | 1.0   | -0.2504154069722839 | 0.009901540351999305 |

**Raíz aproximada:** -0.2504154069722839

---

## 5. Método de Newton-Raphson
El método de Newton es un método que converge más rápido que los dos anteriores, pero las condiciones para la convergencia son más estrictas, ya que hay que comprobar que la función sea dos veces derivable, cerca de $x$, es decir, la derivada no se puede anular, y necesitamos una aproximación inicial $x_0$.

### Pasos del método:

1. Consideramos una aproximación inicial, $x_0$. Podemos usar el método de la bisección o de la “regula falsi” para obtenerlo.
2. Consideramos la recta tangente a la gráfica de $f(x)$ en el punto $(x_0, f(x_0))$, es decir, la recta de ecuación:
   $$
   y(x) = f'(x_0)(x - x_0) + f(x_0).
   $$
3. Definimos $x_1$ como aquella aproximación tal que $y(x_1) = 0$, es decir:
   $$
   f'(x_0)(x_1 - x_0) + f(x_0) = 0 \Rightarrow x_1 = x_0 - \frac{f(x_0)}{f'(x_0)}.
   $$

Este proceso puede ser iterado partiendo ahora de $x_1$ para calcular $x_2$, y repitiendo esto de forma sucesiva obtenemos la fórmula:
$$
x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}, \quad n = 0, 1, \ldots.
$$

### Criterio de paro:
Para este método, el criterio de paro para dar por buena una aproximación puede seguir siendo del tipo $|x_n - x_{n-1}| < \varepsilon$.

### Ventajas y desventajas:
- **Ventajas:**
  - Converge más rápido que los métodos anteriores.
- **Desventajas:**
  - Necesita calcular la derivada.
  - Necesita una primera aproximación.
  - No se puede prever el número de iteraciones para acotar el error.
  - No converge si la derivada se anula en el intervalo.
  
### Ejemplo
Aproximar la solución de la ecuación $x = \tan(x)$ mediante 4 iteraciones del método de Newton en el intervalo $[4, 4.8]$, tomando como aproximación inicial $x_0 = 4.4$.

| Iteración | x0                | x1                | Error                |
| --------- | ----------------- | ----------------- | -------------------- |
| 1         | 4.4               | 4.535980616856694 | 0.1359806168566937   |
| 2         | 4.535980616856694 | 4.501859629633508 | 0.03412098722318646  |
| 3         | 4.501859629633508 | 4.49374537634139  | 0.008114253292117902 |
| 4         | 4.49374537634139  | 4.49340999001035  | 3.353863310397997e-4 |


----
## 6. Ejercicios

Lista completa: [[04 MatII-Qui/Apuntes/matii-quim-tema02-ej\|Ejercicios Tema 2]].


1. Dada la ecuación $2x - e^{-x} = 0$:
- a) ¿Por qué podemos asegurar que hay al menos una solución en el intervalo $[0,1]$?
- b) Aplica el método de Newton para generar tres sucesivas aproximaciones a la raíz, empezando en $x_0=0.5$.

| Iteración | x0                 | x1                 | Error                   |
| --------- | ------------------ | ------------------ | ----------------------- |
| 1         | 0.5                | 0.3490448064283479 | 0.1509551935716521      |
| 2         | 0.3490448064283479 | 0.3517327695370981 | 0.002687963108750246    |
| 3         | 0.3517327695370981 | 0.3517337112490805 | 9.417119823385001*10^-7 |



Alternativa:
1. Dada la ecuación $x^3 - e^{x} = 0$, aplica el método de la "regula falsi" para aproximar una raíz en el intervalo $[0,2]$. Usa una tolerancia de 0.01.





"Iteración: "" "1" ""a:"" "0" ""b:"" "2" "" c: "" "1.241508160943651" "" Error: "" "1.241508160943651" "
"Iteración: "" "2" ""a:"" "1.241508160943651" ""b:"" "2" "" c: "" "1.785284272828892" "" Error: "" "0.5437761118852411" "
"Iteración: "" "3" ""a:"" "1.785284272828892" ""b:"" "2" "" c: "" "1.851285666364146" "" Error: "" "0.06600139353525325" "
"Iteración: "" "4" ""a:"" "1.851285666364146" ""b:"" "2" "" c: "" "1.856718804637825" "" Error: "" "0.005433138273678972 "
"Raíz aproximada: "" "1.856718804637825


 