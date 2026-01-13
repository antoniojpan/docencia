---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema02-ej/","created":"2026-01-08T10:24:16.928+01:00","updated":"2025-12-08T11:02:18.947+01:00"}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 2: Cálculo diferencial en varias variables. Ejercicios

**Problema 1.1** Halla el domino de las siguientes funciones:

1. $f(x,y)=x^{2}-y^{2}$  
    
2. $f(x,y)=\sqrt{x^{2}-4y^{2}}$  
    
3. $f(x,y)=\frac{x^{3}-y^{2}}{x-y}$  
    
4. $f(x,y)=e^{x/y}$  
    
5. $f(x,y)=log(xy)$  
    
6. $f(x,y)=cos(\frac{1}{x-y})$  
    
7. $f(x,y)=\frac{\sqrt{9-y^{2}}}{1+\sqrt{4-(x^{2}+y^{2})}}$  
	
8. $f(x,y)=\frac{x}{x^2-y}$
    

### Derivadas parciales. Diferenciabilidad

**Problema 3.1** Demuestra que las siguientes funciones son diferenciables en los conjuntos que se indican:

1. $f(x,y,z)=x^{2}+y^{2}+z^{2}$ en $\mathbb{R}^{3}$  
    
2. $f(x,y,z)=sen(x+y+z)$ en $\mathbb{R}^{3}$  
    
3. $f(x,y)=e^{x}sen~y$ en $\mathbb{R}^{2}$  
    
4. $f(x,y)=(x^{2}+y^{2})e^{-xy}$ en $\mathbb{R}^{2}$  
    
5. $f(x,y)=\frac{x}{x^{2}+y^{2}}$ en $\mathbb{R}^{2}$  
    

**Problema 3.2** Sea la función $f(x,y)=\sqrt{x^{2}+y^{2}}.$  

1. Demuestra que $\frac{\partial f}{\partial x}$ no está definida en (0,0).
    
2. ¿Es f diferenciable en (0,0)?
    
    

### Derivadas direccionales, vector gradiente y regla de la cadena

**Problema 4.1** Calcular el gradiente de las siguientes funciones:

1. $f(x,y)=3x^{2}-xy+y$  
    
2. $f(x,y)=x^{3}e^{-y}$  
    
3. $f(x,y)=\sqrt{1-(x^{2}+y^{2})}$  
    
4. $f(x,y,z)=xe^{y^{2}}+ye^{z}$  
    
5. $f(x,y,z)=x~sen~y+y~sen~z+z~sen~x$  
    
6. $f(x,y,z)=sen(x+xy^{2}+z^{2})$  
    

**Problema 4.2** Halla la derivada direccional en el punto dado en la dirección indicada:

1. $f(x,y)=xe^{y}-ye^{x}$ en (1,0) en la dirección de $(1,-\sqrt{3})$  
    
2. $f(x,y)=\frac{3x}{x-y}$ en (1.0) en la dirección de (1,-1)
    
3. $f(x,y,z)=x^{2}y+y^{2}z+z^{2}x$ en (1,-1,1) en la dirección de (1, -1,2)
    
4. $f(x,y,z)=log(\sqrt{x^{2}+y^{2}+z^{2}})$ en (2,0, 1) en la dirección de (1,2, 0)
    
5. $f(x,y,z)=e^{x}cos(yz)$ en (0,0,0) en la dirección de (2, 1, -2)
    

**Problema 4.3** Sea $f(x,y)=e^{x+2y}$ halla el conjunto de puntos $(x,y)\in\mathbb{R}^{2}$ tales que la derivada direccional de f en el punto (x, y) en la dirección del vector (4,3) sea igual a 2e.

**Problema 4.4** Sea $f(x,y)=1+sen(3x+y)$, ¿existe algún vector $\vec{v}\in\mathbb{R}^{2}$ tal que la derivada direccional de f en el punto (0,0) en la dirección del vector $\vec{v}$ sea igual a 1?

**Problema 4.5** La temperatura de cada punto de una hoja de metal viene dada por la función $T(x,y)=e^{x}cos~y+e^{y}cosx$.

1. ¿En qué dirección crece la temperatura más rápidamente a partir del punto (0,0)?
    
2. ¿Y en qué dirección decrece más rápidamente?
    

**Problema 4.6** La densidad de una bola de metal centrada en el origen viene dada por la función $\rho(x,y,z)=ke^{-(x^{2}+y^{2}+z^{2})},$ k constante positiva

1. ¿En qué dirección crece la densidad más rápidamente a partir del punto (x, y, z)?
    
2. ¿Y en qué dirección decrece más rápidamente?
    
3. ¿cuáles son los coeficientes de variación (derivadas direccionales) de la densidad en (x, y, z) en las direcciones $\vec{i},$ $\vec{j}$ y $\vec{k}$?
    

**Problema 4.7**

1. Sea $h(x,y)=2e^{-x^{2}}+e^{-3y^{2}}$ la altura de una montaña en la posición $(x,y)\in\mathbb{R}^{2}$ ¿En qué dirección desde (1.0) se debería comenzar a caminar para escalar lo más rápido posible?
    
2. Supongamos que la temperatura en cada punto $(x,y,z)\in\mathbb{R}^{3}$ viene dada por la función $T(x,y,z)=e^{-x}+e^{-2y}+e^{-3z}$ ¿En qué dirección debe moverse una persona situada en el punto (1, 1, 1) con el fin de enfriarse lo más rápido posible?
    

**Problema 4.8** Calcula las derivadas parciales $\frac{\partial z}{\partial x}$ y $\frac{\partial z}{\partial y}$  

1. donde $z(x,y)=f(x+y)+f(x-y)$ siendo f una función real de variable real continua con derivada continua en R.
    
2. donde $z(u,v)=e^{uv}$ siendo las funciones $u(x,y)=log(x+y)$ y $v(x,y)=arctan(x/y)$.
    

**Problema 4.9** Calcula $h^{\prime}(0)$ si $h(t)=f(u(t),v(t),w(t))$ donde:

$f(x,y,z)=\frac{log(1+x^{2}+2z^{2})}{1+y^{2}},$

$(u(t),v(t),w(t))=(t+1,1-t^{2}, sent)$


**Problema 4.10** Halla la ecuación del plano tangente y de la recta normal a la gráfica de las funciones $f(x,y)$ o a las superficies dadas en los puntos indicados:

1. $f(x,y)=x^{2}+4y^{2}$ en $(x_{0},y_{0})=(2,-1)$  
    
2. $f(x,y)=log~x+y+x~cos~y$ en $(x_{0},y_{0})=(1,0)$  
    
3. $f(x,y)=\sqrt{x^{2}+y^{2}}$ en $(x_{0},y_{0})=(1,1/2)$  
    
4. $x^{3}-2y^{3}+z^{3}=0$ en $(x_{0},y_{0},z_{0})=(1,1,1)$  
    
5. $e^{z}cos~x~cos~y=0$ en $(x_{0},y_{0},z_{0})=(\pi/2,1,0)$  
    
6. $e^{xyz}=1$ en $(x_{0},y_{0},z_{0})=(1,2,0)$  
### Optimización de funciones de varias variables

**Problema 5.1** Halla los puntos críticos y determina los valores extremos locales de las siguientes funciones de dos variables:

1. $f(x,y)=x^{2}+2y^{2}-4y$  
    
2. $f(x,y)=x^{2}-xy+y^{2}+2x+2y-6$  
    
3. $f(x,y)=8x^{3}-24xy+y^{3}$  
    
4. $f(x,y)=\frac{x-y}{1+x^{2}+y^{2}}$  
    
5. $f(x,y)=arctan(e^{2x}-2x)+\frac{y^{3}}{3}+\frac{y^{2}}{2}-2y+1$  
    

**Problema 5.2** Calcula los extremos de la función $f(x,y)=e^{-x^{2}+cy^{2}}$ para $c=0,1,-1.$  

**Problema 5.3** Calcula y clasifica los puntos críticos de las siguientes funciones sujetas a las restricciones que se especifican:

1. $f(x,y)=x^{2}+y^{2}$ en el conjunto $A=\{(x,y)\in\mathbb{R}^{2}:xy=1\}$  
    
2. $f(x,y)=xy$ en el conjunto $A=\{(x,y)\in\mathbb{R}^{2}:x^{2}+4y^{2}=4\}$  
    
3. $f(x,y)=x^{2}+y^{2}+6x-8y+25$ en el conjunto $A=\{(x,y)\in\mathbb{R}^{2}:x^{2}+4y^{2}=16\}$  
    
4. $f(x,y)=xy$ sujeta a $2x+3y-5=0$  
    
5. $f(x,y)=\frac{log~x}{x}+\frac{log~y}{y}$ sujeta a $x+y=1$ con $x, y>0$  
    

**Problema 5.4** Una empresa precisa vallar un terreno rectangular de $20m^{2}$. Para el lado más largo, la empresa desea vallas de hierro gris cuyo precio es $25 \in/m.$ Para el lado más corto, las vallas tienen que ser de alumninio blanco, a $20 \in/m$ ¿Cuáles son las dimensiones de los lados que permiten minimizar el coste cumpliendo que el área rectangular sea de $20m^{2}$?

**Problema 5.5** Una caja rectangular sin tapa se fabrica con $12m^{2}$ de cartón. Calcula el volumen máximo de la caja.

**Problema 5.6** Calcula la distancia máxima y la distancia mínima desde el origen a un punto de la elipse $x^{2}+4y^{2}=16$.

**Problema 5.7** Supongamos que la temperatura en grados centígrados en cada punto (x, y) del disco limitado por la circunferencia $x^{2}+y^{2}=1$ viene dada por la función $T(x,y)=2x^{2}+y^{2}-y.$ Determina los puntos más calientes y los más fríos del disco indicando la temperatura alcanzada en dichos puntos.

**Problema 5.8** Una empresa desea diseñar un tanque cilíndrico con extremos semiesféricos para almacenar $8000m^{3}$ de gas líquido. ¿Qué radio y qué altura se recomienda para la parte cilíndrica del tanque, a fin de que la empresa utilice la menor cantidad posible de material para construir el tanque?