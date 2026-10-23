---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema04-ej/","created":"2026-10-23T09:18:39.859+02:00","updated":"2026-10-23T09:18:25.915+02:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 4: Cálculo diferencial en varias variables. Ejercicios

## 1. Funciones de varias variables

**Problema 1.1** Describe el tipo de función (campo escalar, curva parametrizada o campo vectorial) y qué representa:

1. La temperatura del agua en cada punto de un mapa.
2. La posición de un buque en función del tiempo, $(x(t),y(t))$.
3. El viento $(u,v)$ en cada punto de una zona de navegación.
4. La profundidad del fondo marino en cada posición $(x,y)$.

**Problema 1.2** Para $f(x,y)=x^2+y^2$, dibuja las curvas de nivel $f=1$, $f=4$ y $f=9$ e indica qué forma tienen.

## 2. Dominio, límites y continuidad

**Problema 2.1** Halla el dominio de las siguientes funciones:

1. $f(x,y)=x^{2}-y^{2}$
2. $f(x,y)=\sqrt{x^{2}-4y^{2}}$
3. $f(x,y)=\frac{x^{3}-y^{2}}{x-y}$
4. $f(x,y)=e^{x/y}$
5. $f(x,y)=\log(xy)$
6. $f(x,y)=\cos\left(\frac{1}{x-y}\right)$
7. $f(x,y)=\frac{\sqrt{9-y^{2}}}{1+\sqrt{4-(x^{2}+y^{2})}}$
8. $f(x,y)=\frac{x}{x^{2}-y}$

**Problema 2.2** Estudia la continuidad de las siguientes funciones indicando dónde es continua:

1. $\mathbf{f}(x,y)=(x^{2}+y,\; x-y)$
2. $\mathbf{f}(x,y,z)=\left(\cos(xy),\; e^{x+z},\; \frac{1}{x^{2}+y^{2}+1}\right)$
3. $\mathbf{f}(x,y)=\left(\frac{x}{y},\; \operatorname{sen} x\right)$

## 3. Derivadas parciales y diferenciabilidad

**Problema 3.1** Calcula las derivadas parciales que se indican:

1. $f(x,y)=x^{y+1}$; $f_x$, $f_y$, $f_{xy}$
2. $f(x,y)=\ln(y+x^{2})$; $f_x$, $f_y$, $f_{xy}$
3. $f(x,y)=\cos x+\tan\frac{y}{x}-\operatorname{sen} y$; $f_x$, $f_y$
4. $f(x,y)=x^{2}y^{3}-5y^{4}+5$; $f_x$, $f_{xx}$, $f_{xy}$, $f_{yy}$, $f_{xxyyy}$, $\frac{\partial^{5}f}{\partial x^{2}\partial y^{3}}$
5. $f(x,y,z)=xy+z-\ln 2$; $f_x$, $f_y$, $f_{yz}$, $f_z$, $f_{xy}$
6. $f(x,y,z)=2^{xz}$; $f_x$, $f_y$, $f_z$, $f_{xx}$, $f_{xy}$
7. $f(x,y)=e^{xy}\cos y^{2}$; $f_x$, $f_y$
8. $z=\frac{\sqrt{x+y}}{x}$; $z_x$, $z_y$

**Problema 3.2** Estudia la diferenciabilidad de las siguientes funciones en los conjuntos que se indican:

1. $f(x,y,z)=x^{2}+y^{2}+z^{2}$ en $\mathbb{R}^{3}$
2. $f(x,y)=e^{x}\operatorname{sen} y$ en $\mathbb{R}^{2}$
3. $f(x,y)=(x^{2}+y^{2})e^{-xy}$ en $\mathbb{R}^{2}$
4. $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(0,0)$

**Problema 3.3** Halla la ecuación del plano tangente y de la recta normal a la gráfica de las siguientes funciones en los puntos indicados:

1. $f(x,y)=x^{2}+4y^{2}$ en $(x_0,y_0)=(2,-1)$
2. $f(x,y)=\log x+y+x\cos y$ en $(x_0,y_0)=(1,0)$
3. $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(x_0,y_0)=(1,1/2)$

## 4. Gradiente y derivada direccional

**Problema 4.1** Calcula el gradiente de las funciones del Problema 3.1.

**Problema 4.2** Halla la derivada direccional en el punto y en la dirección indicados (normaliza el vector si es necesario):

1. $f(x,y)=xe^{y}-ye^{x}$ en $(1,0)$ en la dirección de $(1,-\sqrt{3})$
2. $f(x,y)=\frac{3x}{x-y}$ en $(1,0)$ en la dirección de $(1,-1)$
3. $f(x,y,z)=x^{2}y+y^{2}z+z^{2}x$ en $(1,-1,1)$ en la dirección de $(1,-1,2)$
4. $f(x,y,z)=\log\sqrt{x^{2}+y^{2}+z^{2}}$ en $(2,0,1)$ en la dirección de $(1,2,0)$
5. $f(x,y,z)=e^{x}\cos(yz)$ en $(0,0,0)$ en la dirección de $(2,1,-2)$

**Problema 4.3** Sea $f(x,y)=e^{x+2y}$. Halla el conjunto de puntos $(x,y)\in\mathbb{R}^{2}$ tales que la derivada direccional en $(x,y)$ en la dirección $(4,3)$ sea $2e$.

**Problema 4.4** Sea $f(x,y)=1+\operatorname{sen}(3x+y)$. ¿Existe algún vector $\vec v\in\mathbb{R}^{2}$ tal que la derivada direccional de $f$ en $(0,0)$ en la dirección de $\vec v$ sea igual a 1?

**Problema 4.5** La temperatura de cada punto de una hoja de metal viene dada por $T(x,y)=e^{x}\cos y+e^{y}\cos x$.

1. ¿En qué dirección crece la temperatura más rápidamente a partir de $(0,0)$?
2. ¿Y en qué dirección decrece más rápidamente?

**Problema 4.6** La densidad de una bola de metal centrada en el origen es $\rho(x,y,z)=ke^{-(x^{2}+y^{2}+z^{2})}$, con $k$ constante positiva.

1. ¿En qué dirección crece la densidad más rápidamente a partir de $(x,y,z)$?
2. ¿Y en qué dirección decrece más rápidamente?
3. ¿Cuáles son las derivadas direccionales de la densidad en las direcciones $\vec i$, $\vec j$ y $\vec k$?

**Problema 4.7**

1. Sea $h(x,y)=2e^{-x^{2}}+e^{-3y^{2}}$ la altura de una montaña en la posición $(x,y)$. ¿En qué dirección desde $(1,0)$ se debe caminar para escalar lo más rápido posible?
2. La temperatura en cada punto $(x,y,z)$ es $T(x,y,z)=e^{-x}+e^{-2y}+e^{-3z}$. ¿En qué dirección debe moverse una persona situada en $(1,1,1)$ para enfriarse lo más rápido posible?

## 5. Operadores diferenciales y curvas

**Problema 5.1** Calcula la divergencia de las siguientes funciones:

1. $\mathbf{f}(x,y,z)=(x+2y,\; x+3z,\; 2y+3z)$
2. $\mathbf{f}(x,y)=(y-x,\; x+y)$
3. $\mathbf{f}(x,y,z)=(x^{2}+y-3z,\; \ln(x-z),\; \cos y)$
4. $\mathbf{f}(x,y)=(x^{2}+y^{2},\; xy)$
5. $\mathbf{f}(x,y,z)=\left(\frac{1}{x+y},\; z+y-3,\; \cos(xyz)\right)$
6. $\mathbf{f}(x,y)=(x^{y},\; y^{x})$

**Problema 5.2** Calcula el rotacional de las funciones 1, 3 y 5 del Problema 5.1.

**Problema 5.3** Para las siguientes curvas, calcula el vector tangente $\mathbf{g}'(t)$, el vector tangente unitario $\mathbf{T}(t)$ y la recta tangente en el punto indicado. Indica también si la curva es regular.

1. $\mathbf{g}(t)=(t^{2},t^{3})$ en $t=1$. ¿Qué ocurre en $t=0$?
2. $\mathbf{g}(t)=(e^{t}\cos t,\; e^{t}\operatorname{sen} t)$ en $t=0$. Calcula además $\|\mathbf{g}'(t)\|$.
3. $\mathbf{g}(t)=(\cos^{3}t,\; \operatorname{sen}^{3}t)$ en $t=\frac{\pi}{4}$.
4. Comprueba que $\mathbf{g}(t)=(2\cos t,\; 3\operatorname{sen} t)$ es una curva de nivel de $f(x,y)=\frac{x^2}{4}+\frac{y^2}{9}$ y verifica que $\nabla f\cdot\mathbf{g}'=0$ en $t=\frac{\pi}{3}$.

## 6. Optimización

**Problema 6.1** Clasifica los puntos críticos de las siguientes funciones mediante el Hessiano:

1. $f(x,y)=x^{3}+y^{3}-3xy$
2. $f(x,y)=4x+6y-x^{2}-y^{2}$
3. $f(x,y)=x^{2}y+xy^{2}$
4. $f(x,y)=12x+3y-x^{3}-y^{3}$
5. $f(x,y)=64x+32y-16x^{4}-y^{4}$
6. $f(x,y)=2x^{3}+2y^{3}-x^{2}y^{2}$

**Problema 6.2** Calcula y clasifica los puntos críticos de las siguientes funciones sujetas a las restricciones que se especifican:

1. $f(x,y)=x^{2}+y^{2}$ en $A=\{(x,y):xy=1\}$
2. $f(x,y)=xy$ en $A=\{(x,y):x^{2}+4y^{2}=4\}$
3. $f(x,y)=x^{2}+y^{2}+6x-8y+25$ en $A=\{(x,y):x^{2}+4y^{2}=16\}$
4. $f(x,y)=xy$ sujeta a $2x+3y-5=0$
5. $f(x,y)=\frac{\log x}{x}+\frac{\log y}{y}$ sujeta a $x+y=1$ con $x,y>0$

**Problema 6.3** Una empresa precisa vallar un terreno rectangular de $20\,\mathrm{m}^{2}$. Para el lado más largo desea vallas de hierro gris a $25\ \text{€/m}$; para el lado más corto, vallas de aluminio blanco a $20\ \text{€/m}$. ¿Qué dimensiones minimizan el coste manteniendo el área de $20\,\mathrm{m}^{2}$?

**Problema 6.4** Una caja rectangular sin tapa se fabrica con $12\,\mathrm{m}^{2}$ de cartón. Calcula el volumen máximo.

**Problema 6.5** Calcula la distancia máxima y mínima desde el origen a un punto de la elipse $x^{2}+4y^{2}=16$.

**Problema 6.6** Una empresa desea diseñar un tanque cilíndrico con extremos semiesféricos para almacenar $8000\,\mathrm{m}^{3}$ de gas líquido. ¿Qué radio y qué altura debe tener la parte cilíndrica para usar la menor cantidad posible de material?
