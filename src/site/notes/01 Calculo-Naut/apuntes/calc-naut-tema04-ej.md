---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema04-ej/","created":"2026-10-23T11:22:50.687+02:00","updated":"2026-10-23T11:22:37.686+02:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Hoja de Ejercicios Tema 4: Derivación en Varias Variables

## 1. Funciones de varias variables

> [!question] Problema 1.1
> Describe el tipo de función (campo escalar, curva parametrizada o campo vectorial) y qué representa:
>
> **(a)** La temperatura del agua en cada punto de un mapa.
>
> **(b)** La posición de un buque en función del tiempo, $(x(t),y(t))$.
>
> **(c)** El viento $(u,v)$ en cada punto de una zona de navegación.
>
> **(d)** La profundidad del fondo marino en cada posición $(x,y)$.

> [!question] Problema 1.2
> Para $f(x,y)=x^2+y^2$, dibuja las curvas de nivel $f=1$, $f=4$ y $f=9$ e indica qué forma tienen.

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

> [!question] Problema 3.3
> Halla la ecuación del plano tangente y de la recta normal a la gráfica de las siguientes funciones en los puntos indicados:
>
> **(a)** $f(x,y)=x^{2}+4y^{2}$ en $(x_0,y_0)=(2,-1)$
>
> **(b)** $f(x,y)=\log x+y+x\cos y$ en $(x_0,y_0)=(1,0)$
>
> **(c)** $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(x_0,y_0)=(1,1/2)$

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

> [!question] Problema 6.2
> Calcula y clasifica los puntos críticos de las siguientes funciones sujetas a las restricciones que se especifican mediante multiplicadores de Lagrange:
>
> **(a)** $f(x,y)=x^{2}+y^{2}$ sujeta a $xy=1$
>
> **(b)** $f(x,y)=xy$ sujeta a $x^{2}+4y^{2}=4$
>
> **(c)** $f(x,y)=x^{2}+y^{2}+6x-8y+25$ sujeta a $x^{2}+4y^{2}=16$
>
> **(d)** $f(x,y)=xy$ sujeta a $2x+3y=5$
>
> **(e)** $f(x,y)=\dfrac{\log x}{x}+\dfrac{\log y}{y}$ sujeta a $x+y=1$ con $x,y>0$

> [!question] Problema 6.3
> Una empresa precisa vallar un terreno rectangular de $20\,\mathrm{m}^{2}$. Para el lado más largo desea vallas de hierro gris a $25\ \text{€/m}$; para el lado más corto, vallas de aluminio blanco a $20\ \text{€/m}$. ¿Qué dimensiones minimizan el coste manteniendo el área de $20\,\mathrm{m}^{2}$?

> [!question] Problema 6.4
> Una caja rectangular sin tapa se fabrica con $12\,\mathrm{m}^{2}$ de cartón. Calcula el volumen máximo.

> [!question] Problema 6.5
> Calcula la distancia máxima y mínima desde el origen a un punto de la elipse $x^{2}+4y^{2}=16$.

> [!question] Problema 6.6
> Una empresa desea diseñar un tanque cilíndrico con extremos semiesféricos para almacenar $8000\,\mathrm{m}^{3}$. ¿Qué radio y qué altura debe tener la parte cilíndrica para usar la menor cantidad posible de material?

---

# Soluciones

> [!success] Solución del Problema 1.1
> **(a)** Campo escalar $f:\mathbb{R}^2\to\mathbb{R}$.
>
> **(b)** Curva parametrizada $\mathbf{g}:\mathbb{R}\to\mathbb{R}^2$ (la derrota).
>
> **(c)** Campo vectorial $\mathbf{f}:\mathbb{R}^2\to\mathbb{R}^2$.
>
> **(d)** Campo escalar $f:\mathbb{R}^2\to\mathbb{R}$; sus curvas de nivel son las isóbatas de la carta náutica.

> [!success] Solución del Problema 1.2
> Las curvas de nivel son circunferencias centradas en el origen de radios $1$, $2$ y $3$ respectivamente. La separación entre ellas disminuye al alejarse del origen, lo que indica que $|\nabla f|$ crece con la distancia.

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

> [!success] Solución del Problema 3.3
> **(a)** $z_0=8$, $f_x=2x$, $f_y=8y$, luego $f_x(2,-1)=4$ y $f_y(2,-1)=-8$. Plano: $z=4x-8y-8$. Recta normal: $(x,y,z)=(2,-1,8)+t\,(4,-8,-1)$.
>
> **(b)** $z_0=1$, $f_x=\frac1x+\cos y$, $f_y=1-x\operatorname{sen} y$, luego $f_x(1,0)=2$ y $f_y(1,0)=1$. Plano: $z=2x+y-1$. Recta normal: $(x,y,z)=(1,0,1)+t\,(2,1,-1)$.
>
> **(c)** $z_0=\sqrt5/2$, $f_x=\frac{x}{\sqrt{x^2+y^2}}$, $f_y=\frac{y}{\sqrt{x^2+y^2}}$, luego $f_x=\frac{2}{\sqrt5}$ y $f_y=\frac{1}{\sqrt5}$. Plano: $z=\frac{\sqrt5}{2}+\frac{2}{\sqrt5}(x-1)+\frac{1}{\sqrt5}\left(y-\frac12\right)$. Recta normal: $(x,y,z)=\left(1,\frac12,\frac{\sqrt5}{2}\right)+t\left(\frac{2}{\sqrt5},\frac{1}{\sqrt5},-1\right)$.

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

> [!success] Solución del Problema 6.2
> **(a)** De $2x=\lambda y$, $2y=\lambda x$ y $xy=1$ se deduce $x^{2}=y^{2}$, luego $y=x$ (la opción $y=-x$ daría $xy=-x^{2}=1$, imposible). Puntos: $(1,1)$ y $(-1,-1)$, ambos con $f=2$: son **mínimos** (la función no está acotada superiormente sobre la hipérbola).
>
> **(b)** Parametrizando $x=2\cos t$, $y=\operatorname{sen} t$ resulta $f=\operatorname{sen} 2t$. **Máximos** en $(\sqrt2,\sqrt2/2)$ y $(-\sqrt2,-\sqrt2/2)$, con $f=1$; **mínimos** en $(-\sqrt2,\sqrt2/2)$ y $(\sqrt2,-\sqrt2/2)$, con $f=-1$.
>
> **(c)** $f=(x+3)^{2}+(y-4)^{2}$, el cuadrado de la distancia al punto $(-3,4)$. Con $x=4\cos t$, $y=2\operatorname{sen} t$ se obtiene un único **mínimo** en $(-2.22,\,1.66)$ con $f\approx 6.07$ y un único **máximo** en $(3.78,\,-0.65)$ con $f\approx 67.6$.
>
> **(d)** De $y=2\lambda$, $x=3\lambda$ y $2x+3y=5$: $x=\frac54$, $y=\frac56$, con $f=\frac{25}{24}$, que es un **máximo** (sobre la recta $f\to-\infty$).
>
> **(e)** Por simetría y $x+y=1$: $x=y=\frac12$, con $f=-4\log 2\approx-2.77$, que es un **máximo** (en los extremos del intervalo $f\to-\infty$).

> [!success] Solución del Problema 6.3
> Con lados $L$ (largo, a $25$ €/m) y $W$ (corto, a $20$ €/m), el coste es $C=2(25L+20W)=50L+40W$ con $LW=20$. Al no existir restricción de precio la solución de $\nabla C=\lambda\nabla g$ da $L=4$, $W=5$ y $C=400$ €: el óptimo usa los lados de $5$ m con la valla **barata**, lo que contradice el enunciado. Exigiendo $L\ge W$ (el lado caro es el largo), el mínimo se alcanza en el límite $L=W=\sqrt{20}\approx4.47$ m, con $C=90\sqrt{20}\approx402.5$ €.
>
> **Respuesta habitual:** lados de $5$ m y $4$ m con coste $400$ € (colocando la valla de $25$ €/m en los lados de $4$ m) o, si el enunciado se toma al pie de la letra, el cuadrado de $\sqrt{20}$ m con $\approx402.5$ €.

> [!success] Solución del Problema 6.4
> Con base $x\times y$ y altura $z$: $xy+2xz+2yz=12$ y $V=xyz$. El máximo se alcanza para $x=y=2z$. Sustituyendo, $x^{2}+4xz=12$ con $z=x/2$, es decir, $x^{2}+2x^{2}=12$, de donde $x=y=2$ m y $z=1$ m. El volumen máximo es $V=4\ \mathrm{m}^{3}$.

> [!success] Solución del Problema 6.5
> Con $x=4\cos t$, $y=2\operatorname{sen} t$: $r^{2}=x^{2}+y^{2}=16\cos^{2}t+4\operatorname{sen}^{2}t=4+12\cos^{2}t$. Por tanto $r^{2}$ varía entre $4$ y $16$: **distancia mínima** $2$ en $(0,\pm2)$ y **máxima** $4$ en $(\pm4,0)$.

> [!success] Solución del Problema 6.6
> Con radio $r$ y altura $h$: volumen $\pi r^{2}h+\frac43\pi r^{3}=8000$ y superficie $2\pi rh+4\pi r^{2}$. Despejando $h$ y sustituyendo, $S=\frac{16000}{r}+\frac{4}{3}\pi r^{2}$, cuyo mínimo cumple $r^{3}=\frac{6000}{\pi}$, es decir, $r\approx12.4$ m. Entonces $h=0$: el tanque óptimo es **esférico** (la esfera minimiza la superficie para un volumen dado).
