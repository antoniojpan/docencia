---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema05-ej/","created":"2026-10-05T13:29:07.159+02:00","updated":"2026-10-05T13:29:05.000+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 5: Derivación en Varias Variables

> [!question] Ejercicio 1
> Calcula las derivadas parciales que se indican:
>
> **(a)** $f(x, y) = x^{y+1}$; $f_x$, $f_y$, $f_{xy}$
>
> **(b)** $f(x, y) = \ln(y + x^2)$; $f_x$, $f_y$, $f_{xy}$
>
> **(c)** $f(x, y) = \cos x + \tan \frac{y}{x} - \operatorname{sen} y$; $f_x$, $f_y$
>
> **(d)** $f(x, y) = x^2 y^3 - 5y^4 + 5$; $f_x$, $f_{xx}$, $f_{xy}$, $f_{yy}$, $f_{xxyyy}$, $\frac{\partial^5 f}{\partial x^2 \partial y^3}$
>
> **(e)** $f(x, y, z) = xy + z - \ln 2$; $f_x$, $f_y$, $f_{yz}$, $f_z$, $f_{xy}$
>
> **(f)** $f(x, y, z) = 2^{xz}$; $f_x$, $f_y$, $f_z$, $f_{xx}$, $f_{xy}$
>
> **(g)** $f(x, y) = e^{xy} \cos y^2$; $f_x$, $f_y$
>
> **(h)** $z = \frac{\sqrt{x+y}}{x}$; $z_x$, $z_y$

> [!question] Ejercicio 2
> Calcula el gradiente de las funciones del Ejercicio 1.

> [!question] Ejercicio 3
> Calcula la divergencia de las siguientes funciones:
>
> **(a)** $f(x, y, z) = (x + 2y, \; x + 3z, \; 2y + 3z)$
>
> **(b)** $f(x, y) = (y - x, \; x + y)$
>
> **(c)** $f(x, y, z) = (x^2 + y - 3z, \; \ln(x - z), \; \cos y)$
>
> **(d)** $f(x, y) = (x^2 + y^2, \; xy)$
>
> **(e)** $f(x, y, z) = \left( \frac{1}{x+y}, \; z + y - 3, \; \cos(xyz) \right)$
>
> **(f)** $f(x, y) = (x^y, \; y^x)$

> [!question] Ejercicio 4
> Calcula el rotacional de las funciones **(a)**, **(c)** y **(e)** del **Ejercicio 3**.

> [!question] Ejercicio 5
> Clasifica los puntos críticos de las siguientes funciones mediante el Hessiano:
>
> **(a)** $f(x, y) = x^3 + y^3 - 3xy$
>
> **(b)** $f(x, y) = 4x + 6y - x^2 - y^2$
>
> **(c)** $f(x, y) = x^2 y + xy^2$
>
> **(d)** $f(x, y) = 12x + 3y - x^3 - y^3$
>
> **(e)** $f(x, y) = 64x + 32y - 16x^4 - y^4$
>
> **(f)** $f(x, y) = 2x^3 + 2y^3 - x^2 y^2$

---

# Soluciones

> [!success] Solución del Ejercicio 1
> Derivadas parciales:
>
> **(a)** $f_x = (y + 1)x^y, \quad f_y = x^{y+1} \ln x, \quad f_{xy} = x^y(1 + (y + 1) \ln x)$
>
> **(b)** $f_x = \frac{2x}{y+x^2}, \quad f_y = \frac{1}{y+x^2}, \quad f_{xy} = -\frac{2x}{(y+x^2)^2}$
>
> **(c)** $f_x = -\operatorname{sen} x - \frac{y}{x^2}\left(1 + \tan^2 \frac{y}{x}\right), \quad f_y = \frac{1}{x}\left(1 + \tan^2 \frac{y}{x}\right) - \cos y$
>
> **(d)** $f_x = 2xy^3, \quad f_{xx} = 2y^3, \quad f_{xy} = 6xy^2, \quad f_{yy} = 6x^2y - 60y^2, \quad f_{xxyyy} = 12, \quad \frac{\partial^5 f}{\partial x^2 \partial y^3} = 12$
>
> **(e)** $f_x = y, \quad f_y = x, \quad f_{yz} = 0, \quad f_z = 1, \quad f_{xy} = 1$
>
> **(f)** $f_x = z \cdot 2^{xz} \ln 2, \quad f_y = 0, \quad f_z = x \cdot 2^{xz} \ln 2, \quad f_{xx} = z^2 \cdot 2^{xz}(\ln 2)^2, \quad f_{xy} = 0$
>
> **(g)** $f_x = y e^{xy} \cos y^2, \quad f_y = e^{xy}(x \cos y^2 - 2y \operatorname{sen} y^2)$
>
> **(h)** $z_x = -\frac{\sqrt{x+y}}{x^2} + \frac{1}{2x\sqrt{x+y}}, \quad z_y = \frac{1}{2x\sqrt{x+y}}$

> [!success] Solución del Ejercicio 2
> Gradiente de las funciones del Ejercicio 1 (utilizando $f_y = 3x^2y^2 - 20y^3$ para el apartado **(d)**):
>
> **(a)** $\nabla f = \left((y + 1)x^y, \; x^{y+1} \ln x\right)$
>
> **(b)** $\nabla f = \left(\frac{2x}{y+x^2}, \; \frac{1}{y+x^2}\right)$
>
> **(c)** $\nabla f = \left(-\operatorname{sen} x - \frac{y}{x^2}\left(1 + \tan^2 \frac{y}{x}\right), \; \frac{1}{x}\left(1 + \tan^2 \frac{y}{x}\right) - \cos y\right)$
>
> **(d)** $\nabla f = \left(2xy^3, \; 3x^2y^2 - 20y^3\right)$
>
> **(e)** $\nabla f = (y, \; x, \; 1)$
>
> **(f)** $\nabla f = \left(z \cdot 2^{xz} \ln 2, \; 0, \; x \cdot 2^{xz} \ln 2\right)$
>
> **(g)** $\nabla f = \left(y e^{xy} \cos y^2, \; e^{xy}(x \cos y^2 - 2y \operatorname{sen} y^2)\right)$
>
> **(h)** $\nabla f = \left(-\frac{\sqrt{x+y}}{x^2} + \frac{1}{2x\sqrt{x+y}}, \; \frac{1}{2x\sqrt{x+y}}\right)$

> [!success] Solución del Ejercicio 3
> Divergencias:
>
> **(a)** $\operatorname{Div}(f) = 4$
>
> **(b)** $\operatorname{Div}(f) = 0$
>
> **(c)** $\operatorname{Div}(f) = 2x$
>
> **(d)** $\operatorname{Div}(f) = 3x$
>
> **(e)** $\operatorname{Div}(f) = -\frac{1}{(x+y)^2} + 1 - xy \operatorname{sen}(xyz)$
>
> **(f)** $\operatorname{Div}(f) = y x^{y-1} + x y^{x-1}$

> [!success] Solución del Ejercicio 4
> Rotacionales:
>
> **(a)** $\operatorname{rot}(f) = (-1, \; 0, \; -1)$
>
> **(c)** $\operatorname{rot}(f) = \left(-\operatorname{sen} y + \frac{1}{x-z}, \; -3, \; \frac{1}{x-z} - 1\right)$
>
> **(e)** $\operatorname{rot}(f) = \left(-xz \operatorname{sen}(xyz) - 1, \; yz \operatorname{sen}(xyz), \; \frac{1}{(x+y)^2}\right)$

> [!success] Solución del Ejercicio 5
> Clasificación mediante el Hessiano:
>
> **(a)** Puntos críticos: $(0, 0)$ (punto de silla) y $(1, 1)$ (mínimo relativo).
>
> **(b)** Punto crítico: $(2, 3)$ (máximo relativo).
>
> **(c)** Punto crítico: $(0, 0)$ (el criterio no decide).
>
> **(d)** Puntos críticos: $(2, 1)$ (máximo relativo), $(2, -1)$ (punto de silla), $(-2, 1)$ (punto de silla) y $(-2, -1)$ (mínimo relativo).
>
> **(e)** Punto crítico: $(1, 2)$ (máximo relativo).
>
> **(f)** Puntos críticos: $(3, 3)$ (punto de silla) y $(0, 0)$ (el criterio no decide).