---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema02-ej/","created":"2026-09-15T08:49:27.279+02:00","updated":"2026-09-15T08:49:24.000+02:00","dg-note-properties":{}}
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

> [!question] Ejercicio 4
> Determina si el vector $v=(2,5,1)$ es combinación lineal de
> $$u_1=(1,2,0),\qquad u_2=(0,1,1),\qquad u_3=(1,0,1).$$
> En caso afirmativo, calcula los coeficientes y decide si la expresión es única.

> [!question] Ejercicio 5
> Considera los vectores de $\mathbb{R}^4$:
> $$v_1=(1,0,1,2),\quad v_2=(0,1,1,1),\quad v_3=(1,1,2,3),\quad v_4=(2,-1,1,3).$$
> Calcula el rango del conjunto y extrae una base del subespacio que generan.

> [!question] Ejercicio 6
> En $\mathbb{R}^4$, determina una base, unas ecuaciones paramétricas y la dimensión del subespacio definido por
> $$
> \begin{cases}
> x+y+z+w=0\\
> x-y+z-w=0.
> \end{cases}
> $$


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

> [!success] Solución del Ejercicio 4
> Planteamos $v=au_1+bu_2+cu_3$. El sistema resultante es
> $$a+c=2,\qquad 2a+b=5,\qquad b+c=1.$$
> Se obtiene $a=2$, $b=1$ y $c=0$. Por tanto,
> $$v=2u_1+u_2.$$
> Los tres vectores son linealmente independientes, por lo que los coeficientes obtenidos son únicos.

> [!success] Solución del Ejercicio 5
> Se verifica que $v_3=v_1+v_2$ y $v_4=2v_1-v_2$. Por tanto, el conjunto tiene rango $2$ y una base del subespacio generado es
> $$\{v_1,v_2\}=\{(1,0,1,2),(0,1,1,1)\}.$$

> [!success] Solución del Ejercicio 6
> Tomando $z=s$ y $w=t$, las ecuaciones dan $x=-s$ e $y=-t$. Así,
> $$
> (x,y,z,w)=s(-1,0,1,0)+t(0,-1,0,1).
> $$
> Una base es
> $$\{(-1,0,1,0),(0,-1,0,1)\},$$
> unas ecuaciones paramétricas son
> $$\begin{cases}x=-s\\y=-t\\z=s\\w=t\end{cases},$$
> y la dimensión es $2$.


