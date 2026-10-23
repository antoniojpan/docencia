---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema05-ej/","created":"2026-10-23T09:33:10.033+02:00","updated":"2026-10-23T09:33:03.100+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 5: Derivación en Varias Variables

## 3. Derivadas parciales y diferenciabilidad

> [!question] Problema 3.1
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

> [!question] Problema 3.2
> Estudia la diferenciabilidad de las siguientes funciones en los conjuntos que se indican:
>
> **(a)** $f(x,y,z)=x^{2}+y^{2}+z^{2}$ en $\mathbb{R}^{3}$
>
> **(b)** $f(x,y)=e^{x}\operatorname{sen} y$ en $\mathbb{R}^{2}$
>
> **(c)** $f(x,y)=(x^{2}+y^{2})e^{-xy}$ en $\mathbb{R}^{2}$
>
> **(d)** $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(0,0)$

## 4. Gradiente y derivada direccional

> [!question] Problema 4.1
> Calcula el gradiente de las funciones del Problema 3.1.

> [!question] Problema 4.2
> Halla la derivada direccional en el punto y en la dirección indicados:
>
> **(a)** $f(x,y)=xe^{y}-ye^{x}$ en $(1,0)$ en la dirección de $(1,-\sqrt{3})$
>
> **(b)** $f(x,y)=\dfrac{3x}{x-y}$ en $(1,0)$ en la dirección de $(1,-1)$
>
> **(c)** $f(x,y,z)=x^{2}y+y^{2}z+z^{2}x$ en $(1,-1,1)$ en la dirección de $(1,-1,2)$
>
> **(d)** $f(x,y,z)=\log\sqrt{x^{2}+y^{2}+z^{2}}$ en $(2,0,1)$ en la dirección de $(1,2,0)$
>
> **(e)** $f(x,y,z)=e^{x}\cos(yz)$ en $(0,0,0)$ en la dirección de $(2,1,-2)$

> [!question] Problema 4.3
> Sea $f(x,y)=e^{x+2y}$. Halla el conjunto de puntos $(x,y)\in\mathbb{R}^{2}$ tales que la derivada direccional en $(x,y)$ en la dirección $(4,3)$ sea $2e$.

> [!question] Problema 4.4
> Sea $f(x,y)=1+\operatorname{sen}(3x+y)$. ¿Existe algún vector $\vec v\in\mathbb{R}^{2}$ tal que la derivada direccional de $f$ en $(0,0)$ en la dirección de $\vec v$ sea igual a $1$?

> [!question] Problema 4.5
> La temperatura de cada punto de una hoja de metal viene dada por $T(x,y)=e^{x}\cos y+e^{y}\cos x$.
>
> **(a)** ¿En qué dirección crece la temperatura más rápidamente a partir de $(0,0)$?
>
> **(b)** ¿Y en qué dirección decrece más rápidamente?

> [!question] Problema 4.6
> La densidad de una bola de metal centrada en el origen es $\rho(x,y,z)=ke^{-(x^{2}+y^{2}+z^{2})}$, con $k$ constante positiva.
>
> **(a)** ¿En qué dirección crece la densidad más rápidamente a partir de $(x,y,z)$?
>
> **(b)** ¿Y en qué dirección decrece más rápidamente?
>
> **(c)** ¿Cuáles son las derivadas direccionales de la densidad en las direcciones $\vec i$, $\vec j$ y $\vec k$?

> [!question] Problema 4.7
> **(a)** Sea $h(x,y)=2e^{-x^{2}}+e^{-3y^{2}}$ la altura de una montaña en la posición $(x,y)$. ¿En qué dirección desde $(1,0)$ se debe caminar para escalar lo más rápido posible?
>
> **(b)** La temperatura en cada punto $(x,y,z)$ es $T(x,y,z)=e^{-x}+e^{-2y}+e^{-3z}$. ¿En qué dirección debe moverse una persona situada en $(1,1,1)$ para enfriarse lo más rápido posible?

## 5. Operadores diferenciales y curvas

> [!question] Problema 5.1
> Calcula la divergencia de las siguientes funciones:
>
> **(a)** $\mathbf{f}(x, y, z) = (x + 2y, \; x + 3z, \; 2y + 3z)$
>
> **(b)** $\mathbf{f}(x, y) = (y - x, \; x + y)$
>
> **(c)** $\mathbf{f}(x, y, z) = (x^2 + y - 3z, \; \ln(x - z), \; \cos y)$
>
> **(d)** $\mathbf{f}(x, y) = (x^2 + y^2, \; xy)$
>
> **(e)** $\mathbf{f}(x, y, z) = \left( \frac{1}{x+y}, \; z + y - 3, \; \cos(xyz) \right)$
>
> **(f)** $\mathbf{f}(x, y) = (x^y, \; y^x)$

> [!question] Problema 5.2
> Calcula el rotacional de las funciones **(a)**, **(c)** y **(e)** del Problema 5.1.

> [!question] Problema 5.3
> Para las siguientes curvas, calcula el vector tangente $\mathbf{g}'(t)$, el vector tangente unitario $\mathbf{T}(t)$ y la recta tangente en el punto indicado. Indica también si la curva es regular.
>
> **(a)** $\mathbf{g}(t) = (t^2, \; t^3)$ en $t = 1$. ¿Qué ocurre en $t = 0$?
>
> **(b)** $\mathbf{g}(t) = (e^t \cos t, \; e^t \operatorname{sen} t)$ en $t = 0$. Calcula además $\|\mathbf{g}'(t)\|$.
>
> **(c)** $\mathbf{g}(t) = (\cos^3 t, \; \operatorname{sen}^3 t)$ en $t = \frac{\pi}{4}$.
>
> **(d)** Comprueba que $\mathbf{g}(t) = (2\cos t, \; 3\operatorname{sen} t)$ es una curva de nivel de $f(x,y) = \frac{x^2}{4} + \frac{y^2}{9}$ y verifica que $\nabla f \cdot \mathbf{g}' = 0$ en $t = \frac{\pi}{3}$.

## 6. Optimización

> [!question] Problema 6.1
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

> [!success] Solución del Problema 3.1
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

> [!success] Solución del Problema 3.2
> Diferenciabilidad:
>
> **(a)** Sus derivadas parciales ($2x, 2y, 2z$) son continuas en $\mathbb{R}^3$; por tanto es diferenciable en todo $\mathbb{R}^3$.
>
> **(b)** $f_x=e^{x}\operatorname{sen} y$, $f_y=e^{x}\cos y$, continuas en $\mathbb{R}^2$; es diferenciable en todo $\mathbb{R}^2$.
>
> **(c)** $f_x=2xe^{-xy}-y(x^{2}+y^{2})e^{-xy}$, $f_y=2ye^{-xy}-x(x^{2}+y^{2})e^{-xy}$, continuas en $\mathbb{R}^2$; es diferenciable en todo $\mathbb{R}^2$.
>
> **(d)** En $(0,0)$ la derivada parcial $f_x(0,0)=\lim_{h\to 0}\frac{|h|}{h}$ no existe, luego $f$ **no es diferenciable** en el origen (es continua, pero presenta un "pico").

> [!success] Solución del Problema 4.1
> Gradiente de las funciones del Problema 3.1 (utilizando $f_y = 3x^2y^2 - 20y^3$ para el apartado **(d)**):
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

> [!success] Solución del Problema 4.2
> Derivadas direccionales (con $\vec u$ unitario):
>
> **(a)** $\nabla f=(e^{y}-ye^{x},\; xe^{y}-e^{x})$, $\nabla f(1,0)=(1,\,1-e)$, $\vec u=\left(\tfrac12,\,-\tfrac{\sqrt3}{2}\right)$:
> $$D_{\vec u}f(1,0)=\frac12+\frac{\sqrt3}{2}(e-1)\approx 1.99$$
>
> **(b)** $f_x=-\dfrac{3y}{(x-y)^{2}}$, $f_y=\dfrac{3x}{(x-y)^{2}}$; en $(1,0)$: $\nabla f=(0,3)$, $\vec u=\left(\tfrac{1}{\sqrt2},-\tfrac{1}{\sqrt2}\right)$:
> $$D_{\vec u}f(1,0)=-\frac{3}{\sqrt2}=-\frac{3\sqrt2}{2}$$
>
> **(c)** $\nabla f=(2xy+z^{2},\; x^{2}+2yz,\; y^{2}+2zx)$; en $(1,-1,1)$: $(-1,-1,3)$, $\vec u=\frac{1}{\sqrt6}(1,-1,2)$:
> $$D_{\vec u}f=\frac{-1+1+6}{\sqrt6}=\sqrt6$$
>
> **(d)** $\nabla f=\dfrac{(x,y,z)}{x^{2}+y^{2}+z^{2}}$; en $(2,0,1)$: $\left(\tfrac25,0,\tfrac15\right)$, $\vec u=\frac{1}{\sqrt5}(1,2,0)$:
> $$D_{\vec u}f=\frac{2}{5\sqrt5}=\frac{2\sqrt5}{25}$$
>
> **(e)** $\nabla f=\left(e^{x}\cos(yz),\; -ze^{x}\operatorname{sen}(yz),\; -ye^{x}\operatorname{sen}(yz)\right)$; en $(0,0,0)$: $(1,0,0)$, $\vec u=\frac13(2,1,-2)$:
> $$D_{\vec u}f=\frac23$$

> [!success] Solución del Problema 4.3
> $\nabla f=e^{x+2y}(1,2)$ y $\vec u=\frac{1}{5}(4,3)$, luego
> $$D_{\vec u}f=e^{x+2y}\cdot\frac{4+6}{5}=2e^{x+2y}.$$
> Igualando a $2e$: $e^{x+2y}=e$, es decir, la recta $x+2y=1$.

> [!success] Solución del Problema 4.4
> $\nabla f(0,0)=(3,1)$, con $\|\nabla f(0,0)\|=\sqrt{10}>1$. Como $D_{\vec u}f(0,0)=\nabla f(0,0)\cdot\vec u$ recorre de forma continua el intervalo $[-\sqrt{10},\sqrt{10}]$ al girar $\vec u$, **sí existe** (de hecho, dos direcciones): basta tomar $\vec u=(\cos\theta,\operatorname{sen}\theta)$ con $3\cos\theta+\operatorname{sen}\theta=1$.

> [!success] Solución del Problema 4.5
> $\nabla T=(e^{x}\cos y-e^{y}\operatorname{sen} x,\; -e^{x}\operatorname{sen} y+e^{y}\cos x)$ y $\nabla T(0,0)=(1,1)$.
>
> **(a)** La temperatura crece más rápidamente en la dirección $(1,1)$, es decir, $\frac{1}{\sqrt2}(1,1)$.
>
> **(b)** Decrece más rápidamente en la dirección opuesta, $\frac{1}{\sqrt2}(-1,-1)$.

> [!success] Solución del Problema 4.6
> $\nabla\rho=-2k\,e^{-(x^{2}+y^{2}+z^{2})}(x,y,z)$.
>
> **(a)** Crece más rápidamente en la dirección $-\frac{1}{\sqrt{x^{2}+y^{2}+z^{2}}}(x,y,z)$ (hacia el origen).
>
> **(b)** Decrece más rápidamente en la dirección $\frac{1}{\sqrt{x^{2}+y^{2}+z^{2}}}(x,y,z)$ (alejándose del origen).
>
> **(c)** $\rho_x=-2kx\,e^{-(x^{2}+y^{2}+z^{2})}$, $\rho_y=-2ky\,e^{-(x^{2}+y^{2}+z^{2})}$, $\rho_z=-2kz\,e^{-(x^{2}+y^{2}+z^{2})}$.

> [!success] Solución del Problema 4.7
> **(a)** $\nabla h=(-4xe^{-x^{2}},\, -6ye^{-3y^{2}})$, luego $\nabla h(1,0)=(-4/e,\,0)$: se debe caminar en la dirección $(-1,0)$ (hacia $x$ decreciente).
>
> **(b)** $\nabla T=(-e^{-x},\,-2e^{-2y},\,-3e^{-3z})$ y $\nabla T(1,1,1)=\left(-e^{-1},\,-2e^{-2},\,-3e^{-3}\right)$. Para enfriarse hay que moverse en la dirección de máximo decrecimiento, $-\nabla T(1,1,1)=\left(e^{-1},\,2e^{-2},\,3e^{-3}\right)$.

> [!success] Solución del Problema 5.1
> Divergencias:
>
> **(a)** $\operatorname{div}(\mathbf{f}) = 4$
>
> **(b)** $\operatorname{div}(\mathbf{f}) = 0$
>
> **(c)** $\operatorname{div}(\mathbf{f}) = 2x$
>
> **(d)** $\operatorname{div}(\mathbf{f}) = 3x$
>
> **(e)** $\operatorname{div}(\mathbf{f}) = -\frac{1}{(x+y)^2} + 1 - xy \operatorname{sen}(xyz)$
>
> **(f)** $\operatorname{div}(\mathbf{f}) = y x^{y-1} + x y^{x-1}$

> [!success] Solución del Problema 5.2
> Rotacionales:
>
> **(a)** $\operatorname{rot}(\mathbf{f}) = (-1, \; 0, \; -1)$
>
> **(c)** $\operatorname{rot}(\mathbf{f}) = \left(-\operatorname{sen} y + \frac{1}{x-z}, \; -3, \; \frac{1}{x-z} - 1\right)$
>
> **(e)** $\operatorname{rot}(\mathbf{f}) = \left(-xz \operatorname{sen}(xyz) - 1, \; yz \operatorname{sen}(xyz), \; \frac{1}{(x+y)^2}\right)$

> [!success] Solución del Problema 5.3
> Vectores tangentes:
>
> **(a)** $\mathbf{g}'(t) = (2t, \; 3t^2)$. En $t = 1$: $\mathbf{g}'(1) = (2, 3)$, $\|\mathbf{g}'(1)\| = \sqrt{13}$ y $\mathbf{T}(1) = \left(\frac{2}{\sqrt{13}}, \frac{3}{\sqrt{13}}\right)$. Recta tangente en $(1,1)$: $(1,1) + \lambda(2,3)$, es decir, $y = \frac{3}{2}x - \frac{1}{2}$.
> En $t = 0$ se tiene $\mathbf{g}'(0) = (0,0)$: la curva **no es regular** en ese punto y presenta una **cúspide** (parábola semicúbica).
>
> **(b)** $\mathbf{g}'(t) = e^t(\cos t - \operatorname{sen} t, \; \operatorname{sen} t + \cos t)$, de donde $\|\mathbf{g}'(t)\| = \sqrt{2}\,e^t$ y $\mathbf{T}(t) = \frac{1}{\sqrt{2}}(\cos t - \operatorname{sen} t, \; \operatorname{sen} t + \cos t)$. En $t = 0$: $\mathbf{g}'(0) = (1, 1)$, $\|\mathbf{g}'(0)\| = \sqrt{2}$ y $\mathbf{T}(0) = \left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}\right)$. Recta tangente en $(1,0)$: $y = x - 1$. La curva (espiral logarítmica) es regular en todo $\mathbb{R}$.
>
> **(c)** $\mathbf{g}'(t) = (-3\cos^2 t \operatorname{sen} t, \; 3\operatorname{sen}^2 t \cos t)$. En $t = \frac{\pi}{4}$: $\mathbf{g}'\left(\frac{\pi}{4}\right) = \left(-\frac{3\sqrt{2}}{4}, \frac{3\sqrt{2}}{4}\right)$, $\left\|\mathbf{g}'\left(\frac{\pi}{4}\right)\right\| = \frac{3}{2}$ y $\mathbf{T}\left(\frac{\pi}{4}\right) = \left(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$. El punto es $\left(\frac{\sqrt{2}}{4}, \frac{\sqrt{2}}{4}\right)$ y la recta tangente es $y = -x + \frac{\sqrt{2}}{2}$. La curva (astroide) es regular salvo en $t = 0, \frac{\pi}{2}, \pi, \frac{3\pi}{2}$, donde $\mathbf{g}' = \mathbf{0}$ y aparecen las cuatro cúspides.
>
> **(d)** $f(\mathbf{g}(t)) = \frac{4\cos^2 t}{4} + \frac{9\operatorname{sen}^2 t}{9} = \cos^2 t + \operatorname{sen}^2 t = 1$: es la curva de nivel $f = 1$ (una elipse). $\nabla f = \left(\frac{x}{2}, \frac{2y}{9}\right)$ y $\mathbf{g}'(t) = (-2\operatorname{sen} t, \; 3\cos t)$. En $t = \frac{\pi}{3}$: $\mathbf{g}\left(\frac{\pi}{3}\right) = \left(1, \frac{3\sqrt{3}}{2}\right)$, $\nabla f = \left(\frac{1}{2}, \frac{\sqrt{3}}{3}\right)$ y $\mathbf{g}' = \left(-\sqrt{3}, \frac{3}{2}\right)$. Por tanto
> $$\nabla f \cdot \mathbf{g}' = \frac{1}{2}(-\sqrt{3}) + \frac{\sqrt{3}}{3}\cdot\frac{3}{2} = -\frac{\sqrt{3}}{2} + \frac{\sqrt{3}}{2} = 0.$$

> [!success] Solución del Problema 6.1
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
