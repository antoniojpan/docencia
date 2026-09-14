---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema02-ej/","created":"2026-09-14T13:39:31.722+02:00","updated":"2026-09-14T13:44:44.569+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 2: Espacios Vectoriales

> [!question] Ejercicio 1
> Determina si los siguientes conjuntos de vectores son linealmente dependientes o independientes. Si son dependientes, obtén además una base del subespacio que generan:
>
> **(a)** $\{(1, 2), (0, -5), (2, 3)\}$
>
> **(b)** $\{(1, 1, 3, 0), (0, 0, 4, 3), (1, 0, 0, -1)\}$
>
> **(c)** $\{(0, 2, 3, -4, 1), (0, 0, 2, 3, 4), (2, 2, -5, 2, 4), (2, 0, -6, 9, 7)\}$
>
> **(d)** $\{(1, 1, -4), (2, 1, 0), (-1, 0, 4)\}$
>
> **(e)** $\{(1, 0, 1), (0, 0, 0), (1, 2, 3)\}$
>
> **(f)** $\{(1, 0, 1), (2, 3, -1), (1, 0, 1)\}$
>
> **(g)** $\{(1, 0, 1), (2, 3, -1)\}$
>
> **(h)** $\{(1, 0, 1), (1, 2, -1), (1, 1, -1)\}$
>
> **(i)** $\{(1, 0, 1), (4, 4, -1), (-1, 0, -1)\}$

> [!question] Ejercicio 2
> En los siguientes apartados nos proporcionan uno de los tres datos siguientes de un subespacio: ecuaciones implícitas, ecuaciones paramétricas o una base. Calcula los dos datos restantes:
>
> **(a)** (en $\mathbb{R}^2$) Ecuaciones paramétricas: $\begin{cases} x = t - s \\ y = t + s \end{cases}$
>
> **(b)** (en $\mathbb{R}^3$) Ecuaciones implícitas: $\begin{cases} x = 0 \\ x + y - 2z = 0 \end{cases}$
>
> **(c)** (en $\mathbb{R}^3$) Ecuaciones paramétricas: $\begin{cases} x = t \\ y = -t \\ z = t + s \end{cases}$
>
> **(d)** (en $\mathbb{R}^3$) Base: $\{(1, 1, 1), (1, 2, 1), (0, 0, 3)\}$
>
> **(e)** (en $\mathbb{R}^3$) Ecuaciones implícitas: $\begin{cases} x + 2z = 0 \\ z - x = 0 \end{cases}$
>
> **(f)** (en $\mathbb{R}^3$) Ecuaciones implícitas: 
> $$\begin{pmatrix} 1 & 2 & 3 \\ 1 & 1 & 2 \\ 1 & 0 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$$
>
> **(g)** (en $\mathbb{R}^3$) Ecuaciones paramétricas: $\begin{cases} x = t \\ y = 3t \\ z = -t \end{cases}$
>
> **(h)** (en $\mathbb{R}^3$) Base: $\{(1, 0, 0), (0, 1, 1)\}$
>
> **(i)** (en $\mathbb{R}^4$) Base: $\{(1, 2, 1, 0), (0, 2, 1, 2)\}$

> [!question] Ejercicio 3
> En todos los apartados del Ejercicio 2, indica la dimensión del subespacio.

---

# Soluciones

> [!success] Solución del Ejercicio 1
> **(a)** **Linealmente dependientes**. Una base del subespacio generado es $\{(1, 2), (0, -5)\}$.
>
> **(b)** **Linealmente independientes**.
>
> **(c)** **Linealmente dependientes**. Una base del subespacio generado es $\{(0, 2, 3, -4, 1), (0, 0, 2, 3, 4), (2, 2, -5, 2, 4)\}$.
>
> **(d)** **Linealmente independientes**.
>
> **(e)** **Linealmente dependientes**. Una base del subespacio generado es $\{(1, 0, 1), (0, 2, 2)\}$.
>
> **(f)** **Linealmente dependientes**. Una base del subespacio generado es $\{(1, 0, 1), (0, 3, -3)\}$.
>
> **(g)** **Linealmente independientes**.
>
> **(h)** **Linealmente independientes**.
>
> **(i)** **Linealmente dependientes**. Una base del subespacio generado es $\{(1, 0, 1), (0, 4, -5)\}$.


> [!success] Solución del Ejercicio 2
> **(a)** Base: $\{(1, 1), (-1, 1)\}$. No tiene ecuaciones implícitas.  
> **(b)** Ecuaciones paramétricas: $(x, y, z) = t(0, 2, 1)$. Base: $\{(0, 2, 1)\}$.  
> **(c)** Base: $\{(1, -1, 1), (0, 0, 1)\}$. Ecuaciones implícitas: $x + y = 0$.  
> **(d)** No tiene ecuaciones implícitas. Ecuaciones paramétricas: $(x, y, z) = t(1, 1, 1) + s(1, 2, 1) + r(0, 0, 3)$.  
> **(e)** Ecuaciones paramétricas: $(x, y, z) = t(0, 1, 0)$. Base: $\{(0, 1, 0)\}$.  
> **(f)** Ecuaciones paramétricas: $(x, y, z) = t(-1, -1, 1)$. Base: $\{(-1, -1, 1)\}$.  
> **(g)** Base: $\{(1, 3, -1)\}$. Ecuaciones implícitas: $\begin{cases} 3x - y = 0 \\ x + z = 0 \end{cases}$.  
> **(h)** Ecuaciones implícitas: $y - z = 0$. Ecuaciones paramétricas: $\begin{cases} x = t \\ y = s \\ z = s \end{cases}$.  
> **(i)** Ecuaciones implícitas: $\begin{cases} x_4 - 2x_3 + 2x_1 = 0 \\ 2x_3 - x_2 = 0 \end{cases}$.

> [!success] Solución del Ejercicio 3
> - **(a)** Dimensión: $2$.  
> - **(b)** Dimensión: $1$.  
> - **(c)** Dimensión: $2$.  
> - **(d)** Dimensión: $3$.  
> - **(e)** Dimensión: $1$.  
> - **(f)** Dimensión: $1$
> - (g) Dimensión: $1$
> - (h) Dimensión: $2$
> - (i) Dimensión: $2$

