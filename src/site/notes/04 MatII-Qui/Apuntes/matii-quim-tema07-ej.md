---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema07-ej/","created":"2026-05-04T13:03:26.650+02:00","updated":"2026-05-11T12:03:52.986+02:00"}
---

[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Ejercicios tema 7

**Ejercicio 1.** Escribir el sistema en forma matricial:

(a) $\begin{cases} x' = x - y + t - 1 \\ y' = 2x + y - 3t^2 \end{cases}$

(b) $\begin{cases} x' = -3x + 4y + e^{-t} \text{sen}(2t) \\ y' = 5x + 9y + 4e^{-t} \cos(2t) \end{cases}$

---

**Ejercicio 2**. Expresar en forma de sistema de ecuaciones el sistema matricial dado:

(a) $\begin{pmatrix} x' \\ y' \end{pmatrix} = \begin{pmatrix} 3 & -7 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} + \begin{pmatrix} 4 \\ 8 \end{pmatrix} \text{sen } t + \begin{pmatrix} t - 4 \\ 2t + 1 \end{pmatrix} e^{4t}$

(b) $X' = \begin{pmatrix} 7 & 5 & -9 \\ 4 & 1 & 1 \\ 0 & -2 & 3 \end{pmatrix} X + \begin{pmatrix} 0 \\ 2 \\ 1 \end{pmatrix} e^{5t} - \begin{pmatrix} 8 \\ 0 \\ 3 \end{pmatrix} e^{-2t}$

---

**Ejercicio 3**. Comprobar que

$$X = \begin{pmatrix} 5 \cos t \\ 3 \cos t - \text{sen } t \end{pmatrix} e^t$$

es solución del sistema

$$\begin{cases} x' = -2x + 5y \\ y' = -2x + 4y \end{cases}$$

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

**Ejercicio 8**. El núcleo radiactivo se descompone de acuerdo con la ley

$$\frac{dN}{dt} = -\lambda N,$$

donde $N$ es la concentración del núcleo dado y $\lambda$ la constante particular de desintegración. En una serie radiactiva de dos núcleos diferentes se tiene el sistema

$$\begin{cases} \dfrac{dN_1}{dt} = -\lambda_1 N_1 \\ \\ \dfrac{dN_2}{dt} = \lambda_1 N_1 - \lambda_2 N_2 \end{cases}$$

Calcular la solución $N_2(t)$ con las condiciones $N_1(0) = N_0$ y $N_2(0) = 0$, siendo $\lambda_1 = 1$ y $\lambda_2 = 2$.

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

[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].