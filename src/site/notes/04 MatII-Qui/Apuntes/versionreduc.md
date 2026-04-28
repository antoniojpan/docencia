---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/versionreduc/","created":"2026-01-08T10:24:16.932+01:00","updated":"2026-04-28T16:54:25.467+02:00"}
---


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 6: Ecuaciones Diferenciales de Orden Superior
- [[04 MatII-Qui/Apuntes/versionreduc#Conceptos Básicos\|Conceptos Básicos]]
- [[04 MatII-Qui/Apuntes/versionreduc#EDO homogéneas con coeficientes constantes\|EDO homogéneas con coeficientes constantes]]
- [[04 MatII-Qui/Apuntes/versionreduc#EDOs no homogéneas (coeficientes indeterminados)\|EDOs no homogéneas (coeficientes indeterminados)]]
- [[04 MatII-Qui/Apuntes/versionreduc#Aplicaciones físicas\|Aplicaciones físicas]]
- [[04 MatII-Qui/Apuntes/versionreduc#Ejercicios de la hoja:\|Ejercicios de la hoja:]]

Si quieres más, ve a la [[04 MatII-Qui/Apuntes/matii-quim-tema06\|versión extendida]]. 
## Conceptos Básicos
Una **ecuación diferencial de orden superior** es una ecuación que involucra derivadas de una función desconocida de orden mayor o igual a dos:
$$ F(x, y, y', y'', ..., y^{(n)}) = 0 $$
Un problema de valores iniciales (PVI) de orden superior para EDOs lineales es una ecuación diferencial lineal junto con los valores de la incógnita y sus $n-1$ primeras derivadas en un punto, según el siguiente esquema:
$$
\begin{cases}
y^{(n)} = h(x, y, y', \dots, y^{(n-1)}) \\
y(x_0) = y_0 \\
y'(x_0) = y_1 \\
\vdots \\
y^{(n-1)}(x_0) = y_{n-1}
\end{cases}
$$
**Ejemplo**. Problema estándar de física: segunda ley de Newton para construir una ecuación diferencial, y condiciones iniciales.
$$
\begin{cases}
mx''=-mg+kx+\cdots+F(x)\\
x(0) = 3 \\
x'(0) = 1 \\
\end{cases}
$$
a) Gravedad constante
b) Ley de Gravitación universal

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
y, en particular, en aquellas de orden 2.
## EDO homogéneas con coeficientes constantes  
Una EDO lineal homogénea de segundo orden con coeficientes constantes tiene la forma  
$$
a\,y''(x)+b\,y'(x)+c\,y(x)=0,
$$
donde $a$, $b$ y $c$ son constantes. Para resolverla se construye la **ecuación característica**
$$
a r^{2}+b r+c=0,
$$
cuyas raíces $r$ determinan la solución general:

| Raíces del polinomio                          | Solución general                                                     |
| --------------------------------------------- | -------------------------------------------------------------------- |
| Dos raíces reales distintas $r_{1}\neq r_{2}$ | $y(x)=C_{1}e^{r_{1}x}+C_{2}e^{r_{2}x}$                               |
| Una raíz real doble $r_{1}=r_{2}=r$           | $y(x)=C_{1}e^{rx}+C_{2}\,t\,e^{rx}$                                  |
| Raíces complejas $r=\alpha\pm i\beta$         | $y(x)=e^{\alpha x}\bigl[C_{1}\cos(\beta x)+C_{2}\sin(\beta x)\bigr]$ |

---

EJEMPLOS: resuelve las siguientes EDOs lineales homogéneas
a)
$$
x''+5x'+6x=0
$$
b) 
$$
x''+4x'+4x=0
$$

c)
$$
x''+2x'+5x=0
$$

---

## EDOs no homogéneas (coeficientes indeterminados)  
$$
a\,y''(x)+b\,y'(x)+c\,y(x)=f(x),
$$

Solamente necesitamos **una** solución particular $y_p$, pues la solución general será
$$
y=y_h+y_p,
$$
donde $y_h$ es la solución general de la homogénea. Piénsalo.

Basándonos en la forma de $f(x)$, lo que hacemos es proponer una solución particular $y_p(x)$ con coeficientes pendientes de determinar, siguiendo esta tabla:

| $f(x)$                          | Forma de $y_p(x)$ propuesta    |
| ------------------------------- | ------------------------------ |
| $ax + b$                        | $Ax + B$                       |
| $ax^2 + bx + c$                 | $Ax^2 + Bx + C$                |
| $e^{ax}$                        | $Ae^{ax}$                      |
| $e^{ax} (b x + c)$              | $e^{ax} (Ax + B)$              |
| $\sin(bx)$ o $\cos(bx)$         | $A\cos(bx) + B\sin(bx)$        |
| $x^m e^{ax}$                    | $e^{ax} (A_m x^m + ... + A_0)$ |
| $x^n \sin(bx)$ o $x^n \cos(bx)$ | $x^n (A\cos(bx) + B\sin(bx))$  |

**OJO:** Si la forma propuesta para $y_p(x)$ resulta ser una solución de la ecuación homogénea, entonces debemos multiplicarla por $x$ (o por una potencia mayor de $x$) hasta obtener una función que no sea solución de la homogénea.

Generalización: [[Laplace transform\|Laplace transform]].

---

EJEMPLO: resuelve las siguientes EDOs
$$
x''+3x'+2x=e^{t}
$$
Tenemos que encontrar:
1. Solución de la homogénea
2. Solución Particular: el término de la derecha es $e^{t}$; proponemos $x_{p}=A e^{t}$.  

---

## Aplicaciones físicas  
**a) Movimiento armónico simple.**
Movimiento oscilatorio: cualquier situación en la que haya una fuerza opuesta a la distancia al punto de equilibrio. Por ejemplo, un muelle. El sistema resultante recibe el nombre de oscilador armónico simple libre, y la ecuación de movimiento, obtenida a partir de $F=ma$, es
$$
mx''+kx=0
$$
con $k$ una constante positiva característica del sistema y $m$ la masa del objeto. La función $x=x(t)$ representa la distancia al punto de equilibro.
Caso especial: peso colgando de un muelle. En tal caso tendríamos dos fuerzas, la del muelle y la de la gravedad:
$$
mx''=-kx+mg.
$$
Pero en realidad se trata del mismo caso, lo único que cambia es que tenemos un nuevo punto de equilibrio, separado una distancia $l$ del anterior. En ese punto se cumple que 
$$
\text{Peso}=\text{Fuerza restauradora}
$$
es decir, $mg=kl$. Luego podemos cambiar la variable $x$, distancia al antiguo punto de equilibro, por la nueva variable $y$, distancia al nuevo punto de equilibro. Se cumple que $y(t)=x(t)-l$. Así pues
$$
mx''=-kx+mg.
$$
$$
my''=-k(y+l)+mg=-ky.
$$
EJEMPLO: Un cuerpo de 3kg se suspende, sin velocidad inicial, de un muelle con constante $k=2$, a $25cm$ por debajo del punto de equilibro. Calcula la ecuación de movimiento, resuélvela y dibújala. ¿A qué distancia del punto de equilibro se encontrará a los 4 segundos?

---

**b) Oscilador amortiguado**  
Supongamos ahora que introducimos el rozamiento con el aire. Tendremos una ecuación de la forma:
$$
mx''+\beta x'+kx=0
$$
donde $\beta$ es una constante positiva.

EJEMPLO: Un cuerpo de 3kg se suspende, sin velocidad inicial, de un muelle con constante $k=2$, a $25cm$ por debajo del punto de equilibro. El coeficiente de rozamiento es $\beta=1$. Calcula la ecuación de movimiento, resuélvela y dibújala. ¿A qué distancia del punto de equilibro se encontrará a los 4 segundos?

Prueba diferentes valores del coeficiente de rozamiento para ver cómo afecta a la trayectoria del objeto colgante (por ejemplo, el medio puede ser aire o agua).

EJEMPLO: Imagina un niño en un columpio, con una masa de $25kg$, y cuya proyección sobre el eje $x$ sigue un movimiento armónico de constante $k=150$. El punto de equilibrio está en $x=0$. Considera que el rozamiento con el aire y de las bisagras del columpio dan lugar a un coeficiente $\beta=10$. Representa el movimiento del niño durante 15 segundos, si parte del reposo con un desplazamiento inicial de $0.8m$. ¿En qué posición se encontrará a los 8 segundos?

---

**c) Oscilador forzado y amortiguado**  
En caso de que introduzcamos una fuerza externa $F(t)$ tendremos
$$
mx''+\beta x'+kx=F(t).
$$
Puedes imaginar un columpio (objeto oscilante) al que le empujamos con una fuerza variable $F(t)$.

EJEMPLO: Imagina un niño en un columpio, con una masa de $25kg$, y cuya proyección sobre el eje $x$ sigue un movimiento armónico de constante $k=150$. El punto de equilibrio está en $x=0$. Considera que el rozamiento con el aire y de las bisagras del columpio dan lugar a un coeficiente $\beta=10$. Ahora imagina que introducimos una fuerza $\cos(\sqrt(149)t/5 )$. Representa el movimiento del niño durante 50 segundos, si parte del reposo con un desplazamiento inicial de $0.8m$. 



[[04 MatII-Qui/Apuntes/matii-quim-tema06-ej\|matii-quim-tema06-ej]] 
[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].