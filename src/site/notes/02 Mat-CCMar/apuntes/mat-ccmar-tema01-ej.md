---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema01-ej/","created":"2026-09-14T12:12:47.774+02:00","updated":"2026-09-14T13:39:56.398+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 1: Sistemas de Ecuaciones Lineales y Matrices


> [!question] Ejercicio 1
> Resuelve los siguientes sistemas de ecuaciones lineales e indica de qué tipo son según el número de soluciones (Sistema Compatible Determinado, Sistema Compatible Indeterminado o Sistema Incompatible):
>
> **(a)** 
> $$\begin{cases} ax + y = 3 \\ ax - y = 7 \end{cases}$$
>
> **(b)** 
> $$\begin{cases} x + ay = 3 \\ x - ay = 3 \end{cases}$$
>
> **(c)** 
> $$\begin{cases} x + y + z = a \\ x + 2y + 2z = b \\ x + 3y + 4z = c \end{cases}$$
>
> **(d)** 
> $$\begin{cases} x + ay = 2 \\ ax + y = 2 \end{cases}$$
>
> **(e)** 
> $$\begin{cases} ax + y + z = 1 \\ ax + x + y + z = 2 \\ ax + y + az = 0 \end{cases}$$
>
> **(f)** 
> $$\begin{cases} (1 + a)x + y + z = 2 \\ 2x + ay + 2z = 4 \\ x + y + z = a \end{cases}$$



> [!question] Ejercicio 2
> En las siguientes matrices, indica para qué valores del parámetro $t$ son invertibles:
>
> **(a)** $A = \begin{pmatrix} 1 & t \\ 1 & 1 \end{pmatrix}$
>
> **(b)** $B = \begin{pmatrix} 2 & t \\ t & 8 \end{pmatrix}$
>
> **(c)** $C = \begin{pmatrix} t & 2 \\ t & 0 \end{pmatrix}$
>
> **(d)** $D = \begin{pmatrix} t & 1 & -1 \\ 1 & t & -1 \\ 1 & -1 & t \end{pmatrix}$
>
> **(e)** $E = \begin{pmatrix} 2 & 2 & 2 \\ 2 & t & 2 \\ 2 & 2 & t \end{pmatrix}$
>
> **(f)** $F = \begin{pmatrix} t & 2 & 3 \\ 3 & t & 2 \\ 2 & 3 & t \end{pmatrix}$


> [!question] Ejercicio 3
> Dando a $t$ el valor $1$, calcula las inversas de las matrices del **Ejercicio 2** (en los casos en que sean invertibles para ese valor de $t$).

> [!question] Ejercicio 4
> Comprueba los resultados del **Ejercicio 3** multiplicando cada matriz por su correspondiente inversa (\\(A \cdot A^{-1} = I\\)).

---

# Soluciones

> [!success] Solución del Ejercicio 1
> **(a)**
> - Si $a = 0$: **Sistema Incompatible (S.I.)**.
> - Si $a \neq 0$: **Sistema Compatible Determinado (S.C.D.)**. Solución: $(x, y) = \left(\frac{5}{a}, -2\right)$.
>
> **(b)**
> - Si $a = 0$: **Sistema Compatible Indeterminado (S.C.I.)** con 1 parámetro. Solución: $(x, y) = (3, 0) + t(0, 1)$ con $t \in \mathbb{R}$.
> - Si $a \neq 0$: **Sistema Compatible Determinado (S.C.D.)**. Solución: $(x, y) = (3, 0)$.
>
> **(c)**
> - **Sistema Compatible Determinado (S.C.D.)** para cualesquiera valores de $a, b, c$. Solución: $(x, y, z) = (2a - b, \; -2a + 3b - c, \; a - 2b + c)$.
>
> **(d)**
> - Si $a = -1$: **Sistema Incompatible (S.I.)**.
> - Si $a = 1$: **Sistema Compatible Indeterminado (S.C.I.)** con 1 parámetro. Solución: $(x, y) = (2, 0) + t(-1, 1)$ con $t \in \mathbb{R}$.
> - Si $a \neq -1$ y $a \neq 1$: **Sistema Compatible Determinado (S.C.D.)**. Solución: $(x, y) = \left(\frac{2}{a+1}, \; \frac{2}{a+1}\right)$.
>
> **(e)**
> - Si $a = 1$: **Sistema Incompatible (S.I.)**.
> - Si $a \neq 1$: **Sistema Compatible Determinado (S.C.D.)**. Solución: $(x, y, z) = \left(1, \; \frac{a^2 - 2a}{1 - a}, \; \frac{1}{1 - a}\right)$.
>
> **(f)**
> - Si $a = 0$: **Sistema Incompatible (S.I.)**.
> - Si $a = 2$: **Sistema Compatible Indeterminado (S.C.I.)** con 1 parámetro. Solución: $(x, y, z) = (0, 2, 0) + t(0, -1, 1)$ con $t \in \mathbb{R}$.
> - Si $a \neq 0$ y $a \neq 2$: **Sistema Compatible Determinado (S.C.D.)**. Solución: $(x, y, z) = \left(\frac{2 - a}{a}, \; -2, \; \frac{a^2 + 3a - 2}{a}\right)$.

---

> [!success] Solución del Ejercicio 2
> Los valores de $t$ para los cuales cada matriz es invertible son:
>
> - **(a)** Invertible para $t \neq 1$.
> - **(b)** Invertible para $t \neq -4$ y $t \neq 4$.
> - **(c)** Invertible para $t \neq 0$.
> - **(d)** Invertible para $t \neq -1$, $t \neq 0$ y $t \neq 1$.
> - **(e)** Invertible para $t \neq 2$.
> - **(f)** Invertible para $t \neq -5$.

---

> [!success] Solución del Ejercicio 3
> Evaluando en $t = 1$:
>
> - **(a)** Para $t = 1$, la matriz **no tiene inversa** (puesto que solo es invertible para $t \neq 1$).
> - **(b)** Para $t = 1$, la inversa es:
>   $$B^{-1} = \frac{1}{15} \begin{pmatrix} 8 & -1 \\ -1 & 2 \end{pmatrix}$$
> - **(c)** Para $t = 1$, la inversa es:
>   $$C^{-1} = \begin{pmatrix} 0 & 1 \\ 1/2 & -1/2 \end{pmatrix}$$
> - **(d)** Para $t = 1$, la matriz **no tiene inversa** (puesto que solo es invertible para $t \neq -1, 0, 1$).
> - **(e)** Para $t = 1$, la inversa es:
>   $$E^{-1} = \begin{pmatrix} -3 & 2 & 1 \\ 2 & -1 & 0 \\ 1 & 0 & -1 \end{pmatrix}$$
> - **(f)** Para $t = 1$, la inversa es:
>   $$F^{-1} = \frac{1}{18} \begin{pmatrix} -5 & 7 & 1 \\ 1 & -5 & 7 \\ 7 & 1 & -5 \end{pmatrix}$$
