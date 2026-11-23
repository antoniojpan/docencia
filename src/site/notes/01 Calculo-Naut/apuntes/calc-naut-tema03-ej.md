---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema03-ej/","created":"2026-11-16T16:03:16.001+01:00","updated":"2026-11-23T11:42:43.430+01:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Hoja de Ejercicios Tema 3: Derivación en Varias Variables



> [!question] Problema 1
> Describe el tipo de función (campo escalar, curva parametrizada o campo vectorial) y qué representa:
>
> **(a)** La temperatura del agua en cada punto de un mapa.
>
> **(b)** La posición de un buque en función del tiempo, $(x(t),y(t))$.
>
> **(c)** El viento $(u,v)$ en cada punto de una zona de navegación.
>
> **(d)** La profundidad del fondo marino en cada posición $(x,y)$.

> [!question] Problema 2
> Para $f(x,y)=x^2+y^2$, dibuja las curvas de nivel $f=1$, $f=4$ y $f=9$ e indica qué forma tienen.



> [!question] Problema 3
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


> [!question] Problema 4
> Halla la ecuación del plano tangente y de la recta normal a la gráfica de las siguientes funciones en los puntos indicados:
>
> **(a)** $f(x,y)=x^{2}+4y^{2}$ en $(x_0,y_0)=(2,-1)$
>
> **(b)** $f(x,y)=\log x+y+x\cos y$ en $(x_0,y_0)=(1,0)$
>
> **(c)** $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(x_0,y_0)=(1,1/2)$



> [!question] Problema 5
> Calcula el gradiente de las funciones del Problema 3.

> [!question] Problema 6
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

> [!question] Problema 7
> Sea $f(x,y)=e^{x+2y}$. Halla el conjunto de puntos $(x,y)\in\mathbb{R}^{2}$ tales que la derivada direccional en $(x,y)$ en la dirección $(4,3)$ sea $2e$.

> [!question] Problema 8
> Sea $f(x,y)=1+\operatorname{sen}(3x+y)$. ¿Existe algún vector $\vec v\in\mathbb{R}^{2}$ tal que la derivada direccional de $f$ en $(0,0)$ en la dirección de $\vec v$ sea igual a $1$?

> [!question] Problema 9
> La temperatura de cada punto de una hoja de metal viene dada por $T(x,y)=e^{x}\cos y+e^{y}\cos x$.
>
> **(a)** ¿En qué dirección crece la temperatura más rápidamente a partir de $(0,0)$?
>
> **(b)** ¿Y en qué dirección decrece más rápidamente?

> [!question] Problema 10
> La densidad de una bola de metal centrada en el origen es $\rho(x,y,z)=ke^{-(x^{2}+y^{2}+z^{2})}$, con $k$ constante positiva.
>
> **(a)** ¿En qué dirección crece la densidad más rápidamente a partir de $(x,y,z)$?
>
> **(b)** ¿Y en qué dirección decrece más rápidamente?
>
> **(c)** ¿Cuáles son las derivadas direccionales de la densidad en las direcciones $\vec i$, $\vec j$ y $\vec k$?

> [!question] Problema 11
> **(a)** Sea $h(x,y)=2e^{-x^{2}}+e^{-3y^{2}}$ la altura de una montaña en la posición $(x,y)$. ¿En qué dirección desde $(1,0)$ se debe caminar para escalar lo más rápido posible?
>
> **(b)** La temperatura en cada punto $(x,y,z)$ es $T(x,y,z)=e^{-x}+e^{-2y}+e^{-3z}$. ¿En qué dirección debe moverse una persona situada en $(1,1,1)$ para enfriarse lo más rápido posible?

> [!question] Problema 12
> La altitud de una montaña en la posición $(x,y)$ viene dada por
> $$h(x,y)=10-x^{2}-2y^{2}.$$
> Estamos situados en el punto $(1,1)$. Se pide:
>
> **(a)** ¿Qué altitud tenemos?
>
> **(b)** Si nos movemos en la dirección $(3,1)$, ¿estamos subiendo o bajando?
>
> **(c)** ¿Hacia dónde tenemos que movernos para no cambiar de altitud?
>
> **(d)** ¿En qué dirección debemos movernos para bajar lo más rápido posible?

> [!question] Problema 13
> La sonda (profundidad del fondo marino), medida en metros, en una zona de navegación viene dada por
> $$s(x,y)=20-2x^{2}-xy-y^{2}.$$
> El buque se encuentra en el punto $(1,2)$. Se pide:
>
> **(a)** ¿Qué sonda hay en ese punto?
>
> **(b)** Si navegamos en la dirección $(1,1)$, ¿la profundidad aumenta o disminuye?
>
> **(c)** ¿Hacia dónde debemos navegar para mantener la sonda constante?
>
> **(d)** ¿En qué dirección disminuye la sonda lo más rápidamente posible (es decir, hacia dónde se va a aguas más someras)?

> [!question] Problema 14
> La altitud de una ladera viene dada por
> $$h(x,y)=x\,e^{y}.$$
> Estamos en el punto $(2,0)$. Se pide:
>
> **(a)** ¿Qué altitud tenemos?
>
> **(b)** Si nos movemos en la dirección $(1,1)$, ¿estamos subiendo o bajando?
>
> **(c)** ¿Hacia dónde tenemos que movernos para no cambiar de altitud?
>
> **(d)** ¿En qué dirección debemos movernos para bajar lo más rápido posible?



> [!question] Problema 15
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

> [!question] Problema 16
> Calcula el rotacional de las funciones **(a)**, **(c)** y **(e)** del Problema 15.

> [!question] Problema 17
> Para las siguientes curvas, calcula el vector tangente $\mathbf{g}'(t)$, el vector tangente unitario $\mathbf{T}(t)$ y la recta tangente en el punto indicado. Indica también si la curva es regular.
>
> **(a)** $\mathbf{g}(t) = (t^2, \; t^3)$ en $t = 1$. ¿Qué ocurre en $t = 0$?
>
> **(b)** $\mathbf{g}(t) = (e^t \cos t, \; e^t \operatorname{sen} t)$ en $t = 0$. Calcula además $\|\mathbf{g}'(t)\|$.
>
> **(c)** $\mathbf{g}(t) = (\cos^3 t, \; \operatorname{sen}^3 t)$ en $t = \frac{\pi}{4}$.
>
> **(d)** Comprueba que $\mathbf{g}(t) = (2\cos t, \; 3\operatorname{sen} t)$ es una curva de nivel de $f(x,y) = \frac{x^2}{4} + \frac{y^2}{9}$ y verifica que $\nabla f \cdot \mathbf{g}' = 0$ en $t = \frac{\pi}{3}$.

> [!question] Problema 18
> Una embarcación sigue la derrota
> $$\mathbf{r}(t)=(2t^{2},\,4t),\qquad 0\leq t\leq 3,$$
> donde las coordenadas se miden en millas náuticas y $t$ en horas. El eje $x$ apunta hacia el este y el eje $y$ hacia el norte.
>
> **(a)** ¿Cuál es la posición de la embarcación al cabo de $1$ hora?
>
> **(b)** Calcula su velocidad vectorial y su rapidez en ese instante, indicando las unidades. ¿Hacia dónde se dirige?
>
> **(c)** Representa aproximadamente la trayectoria y dibuja el vector velocidad en el punto obtenido. ¿Se desplaza con rapidez constante?

> [!question] Problema 19
> Un ciclista da vueltas a una pista circular siguiendo el recorrido
> $$\mathbf{s}(t)=\bigl(3\cos(2t),\,3\operatorname{sen}(2t)\bigr),\qquad t\geq 0,$$
> donde las coordenadas se miden en kilómetros y $t$ en horas.
>
> **(a)** ¿Cuál es su posición en el instante $t=\frac{\pi}{6}$?
>
> **(b)** Calcula su velocidad vectorial y su rapidez en ese instante.
>
> **(c)** ¿Es constante la rapidez aunque cambie el vector velocidad? 



> [!question] Problema 20
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

> [!question] Problema 21
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

> [!question] Problema 22
> Una empresa precisa vallar un terreno rectangular de $20\,\mathrm{m}^{2}$. Para el lado más largo desea vallas de hierro gris a $25\ \text{€/m}$; para el lado más corto, vallas de aluminio blanco a $20\ \text{€/m}$. ¿Qué dimensiones minimizan el coste manteniendo el área de $20\,\mathrm{m}^{2}$?

> [!question] Problema 23
> Una caja rectangular sin tapa se fabrica con $12\,\mathrm{m}^{2}$ de cartón. Calcula el volumen máximo.

> [!question] Problema 24
> Calcula la distancia máxima y mínima desde el origen a un punto de la elipse $x^{2}+4y^{2}=16$.

> [!question] Problema 25
> Una empresa desea diseñar un tanque cilíndrico con extremos semiesféricos para almacenar $8000\,\mathrm{m}^{3}$. ¿Qué radio y qué altura debe tener la parte cilíndrica para usar la menor cantidad posible de material?

---

# Soluciones

> [!success] Solución del Problema 1
> **(a)** Campo escalar $f:\mathbb{R}^2\to\mathbb{R}$.
>
> **(b)** Curva parametrizada $\mathbf{g}:\mathbb{R}\to\mathbb{R}^2$.
>
> **(c)** Campo vectorial $\mathbf{f}:\mathbb{R}^2\to\mathbb{R}^2$.
>
> **(d)** Campo escalar $f:\mathbb{R}^2\to\mathbb{R}$.

> [!success] Solución del Problema 2
> Circunferencias centradas en el origen y de radios $1$, $2$ y $3$, respectivamente.

> [!success] Solución del Problema 3
> **(a)** $f_x=(y+1)x^y$, $f_y=x^{y+1}\ln x$, $f_{xy}=x^y(1+(y+1)\ln x)$.
>
> **(b)** $f_x=\frac{2x}{y+x^2}$, $f_y=\frac{1}{y+x^2}$, $f_{xy}=-\frac{2x}{(y+x^2)^2}$.
>
> **(c)** $f_x=-\operatorname{sen}x-\frac{y}{x^2}\left(1+\tan^2\frac{y}{x}\right)$, $f_y=\frac{1}{x}\left(1+\tan^2\frac{y}{x}\right)-\cos y$.
>
> **(d)** $f_x=2xy^3$, $f_{xx}=2y^3$, $f_{xy}=6xy^2$, $f_{yy}=6x^2y-60y^2$, $f_{xxyyy}=12$, $\frac{\partial^5 f}{\partial x^2\partial y^3}=12$.
>
> **(e)** $f_x=y$, $f_y=x$, $f_{yz}=0$, $f_z=1$, $f_{xy}=1$.
>
> **(f)** $f_x=z\,2^{xz}\ln2$, $f_y=0$, $f_z=x\,2^{xz}\ln2$, $f_{xx}=z^2\,2^{xz}(\ln2)^2$, $f_{xy}=0$.
>
> **(g)** $f_x=ye^{xy}\cos y^2$, $f_y=e^{xy}(x\cos y^2-2y\operatorname{sen}y^2)$.
>
> **(h)** $z_x=-\frac{\sqrt{x+y}}{x^2}+\frac{1}{2x\sqrt{x+y}}$, $z_y=\frac{1}{2x\sqrt{x+y}}$.

> [!success] Solución del Problema 4
> **(a)** Plano tangente: $z=4x-8y-8$. Recta normal: $(x,y,z)=(2,-1,8)+t(4,-8,-1)$.
>
> **(b)** Plano tangente: $z=2x+y-1$. Recta normal: $(x,y,z)=(1,0,1)+t(2,1,-1)$.
>
> **(c)** Plano tangente: $z=\frac{\sqrt5}{2}+\frac{2}{\sqrt5}(x-1)+\frac{1}{\sqrt5}\left(y-\frac12\right)$. Recta normal: $(x,y,z)=\left(1,\frac12,\frac{\sqrt5}{2}\right)+t\left(\frac{2}{\sqrt5},\frac{1}{\sqrt5},-1\right)$.

> [!success] Solución del Problema 5
> **(a)** $\nabla f=\left((y+1)x^y,\;x^{y+1}\ln x\right)$.
>
> **(b)** $\nabla f=\left(\frac{2x}{y+x^2},\;\frac{1}{y+x^2}\right)$.
>
> **(c)** $\nabla f=\left(-\operatorname{sen}x-\frac{y}{x^2}\left(1+\tan^2\frac{y}{x}\right),\;\frac{1}{x}\left(1+\tan^2\frac{y}{x}\right)-\cos y\right)$.
>
> **(d)** $\nabla f=\left(2xy^3,\;3x^2y^2-20y^3\right)$.
>
> **(e)** $\nabla f=(y,x,1)$.
>
> **(f)** $\nabla f=\left(z\,2^{xz}\ln2,\;0,\;x\,2^{xz}\ln2\right)$.
>
> **(g)** $\nabla f=\left(ye^{xy}\cos y^2,\;e^{xy}(x\cos y^2-2y\operatorname{sen}y^2)\right)$.
>
> **(h)** $\nabla z=\left(-\frac{\sqrt{x+y}}{x^2}+\frac{1}{2x\sqrt{x+y}},\;\frac{1}{2x\sqrt{x+y}}\right)$.

> [!success] Solución del Problema 6
> **(a)** $D_{\vec u}f(1,0)=\frac12+\frac{\sqrt3}{2}(e-1)\approx1.99$.
>
> **(b)** $D_{\vec u}f(1,0)=-\frac{3\sqrt2}{2}$.
>
> **(c)** $D_{\vec u}f(1,-1,1)=\sqrt6$.
>
> **(d)** $D_{\vec u}f(2,0,1)=\frac{2\sqrt5}{25}$.
>
> **(e)** $D_{\vec u}f(0,0,0)=\frac23$.

> [!success] Solución del Problema 7
> La recta $x+2y=1$.

> [!success] Solución del Problema 8
> Sí; las direcciones unitarias son $(0,1)$ y $\left(\frac35,-\frac45\right)$.

> [!success] Solución del Problema 9
> **(a)** $\frac{1}{\sqrt2}(1,1)$.
>
> **(b)** $\frac{1}{\sqrt2}(-1,-1)$.

> [!success] Solución del Problema 10
> **(a)** $-\frac{1}{\sqrt{x^2+y^2+z^2}}(x,y,z)$, hacia el origen, si $(x,y,z)\neq(0,0,0)$.
>
> **(b)** $\frac{1}{\sqrt{x^2+y^2+z^2}}(x,y,z)$, alejándose del origen, si $(x,y,z)\neq(0,0,0)$.
>
> **(c)** $\rho_x=-2kxe^{-(x^2+y^2+z^2)}$, $\rho_y=-2kye^{-(x^2+y^2+z^2)}$, $\rho_z=-2kze^{-(x^2+y^2+z^2)}$.

> [!success] Solución del Problema 11
> **(a)** En la dirección $(-1,0)$.
>
> **(b)** En la dirección $\left(e^{-1},2e^{-2},3e^{-3}\right)$.

> [!success] Solución del Problema 12
> **(a)** $7$.
>
> **(b)** Bajando.
>
> **(c)** En cualquiera de las direcciones $\pm\frac{1}{\sqrt5}(-2,1)$.
>
> **(d)** En la dirección $\frac{1}{\sqrt5}(1,2)$.

> [!success] Solución del Problema 13
> **(a)** $12$ m.
>
> **(b)** Disminuye.
>
> **(c)** En cualquiera de las direcciones $\pm\frac{1}{\sqrt{61}}(5,-6)$.
>
> **(d)** En la dirección $\frac{1}{\sqrt{61}}(6,5)$.

> [!success] Solución del Problema 14
> **(a)** $2$.
>
> **(b)** Subiendo.
>
> **(c)** En cualquiera de las direcciones $\pm\frac{1}{\sqrt5}(-2,1)$.
>
> **(d)** En la dirección $\frac{1}{\sqrt5}(-1,-2)$.

> [!success] Solución del Problema 15
> **(a)** $\operatorname{div}(\mathbf{f})=4$.
>
> **(b)** $\operatorname{div}(\mathbf{f})=0$.
>
> **(c)** $\operatorname{div}(\mathbf{f})=2x$.
>
> **(d)** $\operatorname{div}(\mathbf{f})=3x$.
>
> **(e)** $\operatorname{div}(\mathbf{f})=-\frac{1}{(x+y)^2}+1-xy\operatorname{sen}(xyz)$.
>
> **(f)** $\operatorname{div}(\mathbf{f})=yx^{y-1}+xy^{x-1}$.

> [!success] Solución del Problema 16
> **(a)** $\operatorname{rot}(\mathbf{f})=(-1,0,-1)$.
>
> **(c)** $\operatorname{rot}(\mathbf{f})=\left(-\operatorname{sen}y+\frac{1}{x-z},\;-3,\;\frac{1}{x-z}-1\right)$.
>
> **(e)** $\operatorname{rot}(\mathbf{f})=\left(-xz\operatorname{sen}(xyz)-1,\;yz\operatorname{sen}(xyz),\;\frac{1}{(x+y)^2}\right)$.

> [!success] Solución del Problema 17
> **(a)** $\mathbf{g}'(t)=(2t,3t^2)$, $\mathbf{T}(1)=\frac{1}{\sqrt{13}}(2,3)$ y recta tangente $y=\frac32x-\frac12$. La curva no es regular en $t=0$, donde presenta una cúspide.
>
> **(b)** $\mathbf{g}'(t)=e^t(\cos t-\operatorname{sen}t,\operatorname{sen}t+\cos t)$, $\|\mathbf{g}'(t)\|=\sqrt2e^t$, $\mathbf{T}(t)=\frac{1}{\sqrt2}(\cos t-\operatorname{sen}t,\operatorname{sen}t+\cos t)$ y recta tangente en $t=0$: $y=x-1$. La curva es regular en todo $\mathbb{R}$.
>
> **(c)** $\mathbf{g}'(\pi/4)=\frac{3\sqrt2}{4}(-1,1)$, $\mathbf{T}(\pi/4)=\frac{1}{\sqrt2}(-1,1)$ y recta tangente $y=-x+\frac{\sqrt2}{2}$. La curva es regular salvo en $t=\frac{k\pi}{2}$, con $k\in\mathbb{Z}$.
>
> **(d)** Es la elipse de nivel $f=1$ y $\nabla f\cdot\mathbf{g}'=0$ en $t=\frac{\pi}{3}$.

> [!success] Solución del Problema 18
> **(a)** $\mathbf{r}(1)=(2,4)$ millas náuticas.
>
> **(b)** $\mathbf{r}'(1)=(4,4)\ \mathrm{nmi/h}$, con rapidez $4\sqrt2\ \mathrm{nmi/h}\approx5.66$ nudos. Se dirige hacia el noreste, formando $45^\circ$ con la dirección este.
>
> **(c)** La trayectoria es la parábola $x=\frac{y^2}{8}$, con $y\geq0$, y el vector velocidad en $(2,4)$ es $(4,4)$. La rapidez no es constante: $\|\mathbf{r}'(t)\|=4\sqrt{t^2+1}\ \mathrm{nmi/h}$.

> [!success] Solución del Problema 19
> **(a)** $\left(\frac32,\frac{3\sqrt3}{2}\right)\ \mathrm{km}$.
>
> **(b)** $\mathbf{s}'(\pi/6)=(-3\sqrt3,3)\ \mathrm{km/h}$ y rapidez $6\ \mathrm{km/h}$.
>
> **(c)** Sí; $\|\mathbf{s}'(t)\|=6\ \mathrm{km/h}$ para todo $t$.

> [!success] Solución del Problema 20
> **(a)** $(0,0)$: punto de silla; $(1,1)$: mínimo relativo.
>
> **(b)** $(2,3)$: máximo relativo.
>
> **(c)** $(0,0)$: el criterio del Hessiano no decide.
>
> **(d)** $(2,1)$: máximo relativo; $(2,-1)$ y $(-2,1)$: puntos de silla; $(-2,-1)$: mínimo relativo.
>
> **(e)** $(1,2)$: máximo relativo.
>
> **(f)** $(3,3)$: punto de silla; $(0,0)$: el criterio del Hessiano no decide.

> [!success] Solución del Problema 21
> **(a)** Mínimos en $(1,1)$ y $(-1,-1)$, con $f=2$. No existe máximo.
>
> **(b)** Máximos en $(\sqrt2,\sqrt2/2)$ y $(-\sqrt2,-\sqrt2/2)$, con $f=1$; mínimos en $(-\sqrt2,\sqrt2/2)$ y $(\sqrt2,-\sqrt2/2)$, con $f=-1$.
>
> **(c)** Mínimo aproximado en $(-2.22,1.66)$, con $f\approx6.07$; máximo aproximado en $(3.78,-0.65)$, con $f\approx67.6$.
>
> **(d)** Máximo en $\left(\frac54,\frac56\right)$, con $f=\frac{25}{24}$.
>
> **(e)** Máximo en $\left(\frac12,\frac12\right)$, con $f=-4\ln2$.

> [!success] Solución del Problema 22
> Si el lado más caro debe ser necesariamente el más largo: cuadrado de lado $\sqrt{20}\approx4.47$ m y coste $90\sqrt{20}\approx402.5$ €.
>
> Sin esa restricción: lados de $4$ m y $5$ m, con la valla de $25$ €/m en los lados de $4$ m, y coste mínimo $400$ €.

> [!success] Solución del Problema 23
> Base $2\times2$ m, altura $1$ m y volumen máximo $4\ \mathrm{m}^3$.

> [!success] Solución del Problema 24
> Distancia mínima $2$, en $(0,\pm2)$; distancia máxima $4$, en $(\pm4,0)$.

> [!success] Solución del Problema 25
> $r=\sqrt[3]{\frac{6000}{\pi}}\approx12.4$ m y $h=0$: el tanque óptimo es una esfera.
