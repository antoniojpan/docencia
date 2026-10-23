---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema04/","created":"2026-10-23T09:22:29.966+02:00","updated":"2026-10-23T09:22:21.794+02:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 4: Cálculo diferencial en varias variables
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#1. Funciones de Varias Variables\|1. Funciones de Varias Variables]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#2. Dominio, Límites y Continuidad\|2. Dominio, Límites y Continuidad]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#3. Derivadas Parciales\|3. Derivadas Parciales]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#4. Gradiente y Derivada Direccional\|4. Gradiente y Derivada Direccional]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#5. Operadores Diferenciales\|5. Operadores Diferenciales]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema04#6. Optimización en Varias Variables\|6. Optimización en Varias Variables]]

## 1. Funciones de Varias Variables

### 1.1. Concepto y Tipos de Funciones

Las funciones de varias variables dependen de más de una entrada y/o devuelven varios valores. Se clasifican según sus espacios de origen y llegada:

- **Campos escalares ($f: \mathbb{R}^N \to \mathbb{R}$):** asignan un único valor numérico a cada punto.
  - *Ejemplo náutico:* la profundidad del fondo marino en cada posición $(x,y)$ de la carta náutica (las isóbatas son sus curvas de nivel).
- **Curvas en el plano o en el espacio ($\mathbf{g}: \mathbb{R} \to \mathbb{R}^N$):** dependen de una única variable (habitualmente el tiempo $t$) y devuelven una posición.
  - *Ejemplo náutico:* la derrota del buque, $t \mapsto (x(t), y(t))$.
- **Campos vectoriales en el plano ($\mathbf{f}: \mathbb{R}^2 \to \mathbb{R}^2$):** asignan un vector a cada punto del plano.
  - *Ejemplo náutico:* el viento $(u,v)$ en cada posición $(x,y)$.
- **Campos vectoriales en el espacio ($\mathbf{f}: \mathbb{R}^3 \to \mathbb{R}^3$):** dan un vector en cada punto del espacio.
  - *Ejemplo náutico:* la corriente marina o la velocidad del aire $(u,v,w)$ en un punto $(x,y,z)$.

En el tema 4 trabajamos sobre todo con el primer tipo (campos escalares), pero conviene conocer los otros dos porque aparecen constantemente en navegación.

### 1.2. Representación Gráfica

Cada tipo exige una representación distinta: los **campos escalares** se visualizan mediante curvas de nivel, las **curvas parametrizadas** mediante su trayectoria y los **campos vectoriales** mediante flechas o líneas de campo.

#### 1.2.1. Campos escalares: curvas de nivel

Para visualizar un campo escalar $f:\mathbb{R}^2\to\mathbb{R}$ se usan las **curvas de nivel**: el conjunto de puntos donde la función toma un valor constante $c$,
$$f(x,y)=c.$$

- **Isóbatas:** curvas de nivel de la profundidad (cartas náuticas).
- **Isotermas:** curvas de nivel de la temperatura.

![campo-escalar-curvas-nivel.png\|500](/img/user/imagenes/campo-escalar-curvas-nivel.png)

El color indica el valor de $f$ y las líneas blancas son curvas de nivel $f(x,y)=c$ para $c=1,2,4,6,8$. Obsérvese que las curvas se acumulan donde la función crece más deprisa: la separación entre curvas mide, cualitativamente, el módulo del gradiente.

La misma información en tres dimensiones: la **gráfica** de $f$ es una superficie (la "montaña") y las curvas de nivel son sus cortes horizontales proyectados sobre el plano $z=0$:

![campo-escalar-superficie-3d.png\|520](/img/user/imagenes/campo-escalar-superficie-3d.png)

#### 1.2.2. Curvas parametrizadas en el plano

Una curva en el plano es la imagen de una función $\mathbf{g}:\mathbb{R}\to\mathbb{R}^2$,
$$\mathbf{g}(t)=\big(x(t),\,y(t)\big),$$
donde $t$ recorre un intervalo (habitualmente el tiempo). La gráfica es la **trayectoria**; el parámetro añade dos informaciones que la trayectoria por sí sola no contiene:

- **Orientación:** el sentido en que se recorre al aumentar $t$.
- **Velocidad:** el vector tangente $\mathbf{g}'(t)=\big(x'(t),y'(t)\big)$, que indica dirección y rapidez en cada instante.

![curva-parametrizada-plano.png\|500](/img/user/imagenes/curva-parametrizada-plano.png)

#### 1.2.3. Campos vectoriales en el plano

Un campo vectorial asigna un vector a cada punto:
$$\mathbf{f}(x,y)=\big(u(x,y),\,v(x,y)\big).$$
Se representa dibujando en cada punto una flecha con la dirección y sentido del vector. Para que sea legible se suele:

- **Normalizar o escalar las flechas**, ya que su longitud real puede tapar el dibujo.
- **Colorear según la norma** $\|\mathbf{f}(x,y)\|$, lo que añade información cuantitativa.
- **Superponer líneas de campo** (*streamlines*), curvas tangentes al campo en cada punto: son las trayectorias de una partícula arrastrada por el viento o la corriente.

![campo-vectorial-plano.png\|500](/img/user/imagenes/campo-vectorial-plano.png)

En la figura, el campo de rotación $\mathbf{f}(x,y)=(-y,x)$: las flechas giran alrededor del origen, el color codifica $\|\mathbf{f}\|$ y las líneas negras son las trayectorias de una partícula.

## 2. Dominio, Límites y Continuidad

### 2.1. Dominio

El **dominio** de una función $f$ de varias variables, $Dom(f)$, es el conjunto de puntos donde está definida. Hay que identificar las operaciones con restricciones:

1. **Denominadores:** si $f=\frac{g}{h}$, debe ser $h(x,y)\neq 0$.
2. **Raíces de índice par:** si $f=\sqrt{g}$, debe ser $g(x,y)\ge 0$.
3. **Logaritmos:** si $f=\log g$, debe ser $g(x,y)>0$.
4. **Trigonométricas inversas:** si $f=\arcsin g$ o $\arccos g$, debe ser $g(x,y)\in[-1,1]$.

Los polinomios, $e^{g}$, $\operatorname{sen} g$ y $\cos g$ están definidos siempre que lo esté $g$.

### 2.2. Límites y Continuidad

El cálculo de límites en varias variables es técnicamente delicado, porque hay infinitos caminos de aproximación a un punto; en este curso no lo necesitaremos en detalle.

**Criterio de continuidad:** una función de varias variables es continua en un punto si y solo si todas sus **funciones componentes** son continuas en dicho punto.

En la práctica, todas las funciones del curso son continuas en su dominio (polinomios, exponenciales, senos, cocientes con denominador no nulo, etc.).

## 3. Derivadas Parciales

### 3.1. Definición e Interpretación

Hallar la **derivada parcial** respecto a una variable consiste en derivar de la manera tradicional respecto a esa variable, tratando las demás como constantes. Se denota $\frac{\partial f}{\partial x}$ o $f_x$.

- **Cálculo práctico:**
  - Para $\frac{\partial f}{\partial x}$, deriva respecto a $x$ tratando $y$ como constante.
  - Para $\frac{\partial f}{\partial y}$, deriva respecto a $y$ tratando $x$ como constante.
- **Interpretación:** $\frac{\partial f}{\partial x}$ mide la tasa de variación de $f$ cuando solo se mueve $x$; es decir, la influencia de $x$ en el valor de la función.

### 3.2. Diferenciabilidad

Una función $f$ es **diferenciable** en $P_0=(a,b)$ si, cerca de ese punto, se puede aproximar por un plano (una función lineal) con un error que se hace despreciable al acercarse a $P_0$. Es la generalización de que una curva tenga recta tangente.

Que existan las derivadas parciales **no garantiza** la diferenciabilidad: la función puede tener derivadas parciales y aun así presentar un "pico" al movernos en otras direcciones. Por eso se usa este criterio práctico:

**Condición suficiente (la que se aplica en la práctica):** si $f_x$ y $f_y$ existen y son continuas en un entorno de $(a,b)$, entonces $f$ es diferenciable en $(a,b)$.

- Diferenciable $\implies$ continua.
- Diferenciable $\implies$ existen todas las derivadas parciales (el recíproco es falso).

**Ejemplo:** Sea $f(x,y)=x^2+y^3-5$ en $P_0=(1,3)$.

1. Valor en el punto: $f(1,3)=1+27-5=23$.
2. Derivadas parciales: $f_x=2x$, $f_y=3y^2$; en $(1,3)$, $f_x(1,3)=2$ y $f_y(1,3)=27$.
3. Como $f_x$ y $f_y$ son continuas en todo $\mathbb{R}^2$, $f$ es diferenciable en $(1,3)$ y en cualquier otro punto.

### 3.3. Plano Tangente y Recta Normal

La aproximación lineal de $f$ cerca de $P_0=(x_0,y_0)$ es precisamente el **plano tangente** a su gráfica en ese punto. Para la gráfica de $z=f(x,y)$, con $z_0=f(x_0,y_0)$:

**Plano tangente:**
$$z-z_0=\frac{\partial f}{\partial x}(x_0,y_0)(x-x_0)+\frac{\partial f}{\partial y}(x_0,y_0)(y-y_0)$$

**Recta normal** (perpendicular al plano tangente):
$$(x,y,z)=(x_0,y_0,z_0)+t\,\bigl(f_x(x_0,y_0),\,f_y(x_0,y_0),\,-1\bigr)$$

**Ejemplo (continuación):** para $f(x,y)=x^2+y^3-5$ en $(1,3)$, con $z_0=23$:
$$z-23=2(x-1)+27(y-3)\quad\Longrightarrow\quad z=2x+27y-60$$
y la recta normal:
$$(x,y,z)=(1,3,23)+t\,(2,27,-1)$$

## 4. Gradiente y Derivada Direccional

### 4.1. El Vector Gradiente

Dado un campo escalar $f(x,y)$, el **gradiente** es el vector formado por las derivadas parciales primeras:
$$\nabla f=\left(\frac{\partial f}{\partial x},\;\frac{\partial f}{\partial y}\right).$$
Para $f(x,y,z)$: $\nabla f=\left(f_x,\,f_y,\,f_z\right)$.

**Propiedades del gradiente** en un punto $P$:

1. **Máximo crecimiento:** la dirección de máximo crecimiento (o "máxima pendiente") es la del propio gradiente $\nabla f(P)$; la tasa de ese crecimiento es $\|\nabla f(P)\|$.
2. **Máximo decrecimiento:** la dirección opuesta, $-\nabla f(P)$; la tasa es $-\|\nabla f(P)\|$.
3. **Sin cambio:** la derivada direccional es cero en cualquier dirección perpendicular a $\nabla f(P)$. En particular, **el gradiente es perpendicular a la curva de nivel** que pasa por $P$.

### 4.2. Derivada Direccional

La **derivada direccional** de $f$ en un punto $P$ en la dirección de un **vector unitario** $\vec u$ mide la tasa de cambio de $f$ en esa dirección:
$$D_{\vec u}f(P)=\nabla f(P)\cdot\vec u.$$

- Si $D_{\vec u}f=0$, el movimiento en la dirección $\vec u$ se realiza a lo largo de una **curva de nivel** (sin cambio en el valor de la función).
- Si la dirección viene dada por un vector $\vec v$ no unitario, primero se normaliza:
$$\vec u=\frac{\vec v}{\|\vec v\|},\qquad \|\vec v\|=\sqrt{v_1^2+v_2^2+\dots}$$
(Es lo que hay que hacer en el Problema 4.2.)

## 5. Operadores Diferenciales

A cada tipo de objeto geométrico le corresponde un operador diferencial natural: el **gradiente** actúa sobre campos escalares, la **derivada** sobre curvas y el **rotacional** y la **divergencia** sobre campos vectoriales.

### 5.1. Rotacional

El **rotacional** mide la tendencia de un campo vectorial a girar o inducir rotación en el flujo alrededor de cada punto (por ejemplo, el giro de una corriente o de una borrasca).

- **En $\mathbb{R}^2\to\mathbb{R}^2$:** para $\mathbf{f}(x,y)=(f_1,f_2)$,
$$\operatorname{rot}(\mathbf{f})=\frac{\partial f_2}{\partial x}-\frac{\partial f_1}{\partial y}.$$
- **En $\mathbb{R}^3\to\mathbb{R}^3$:** para $\mathbf{f}(x,y,z)=(f_1,f_2,f_3)$,
$$\operatorname{rot}(\mathbf{f})=\nabla\times\mathbf{f}=\left(\frac{\partial f_3}{\partial y}-\frac{\partial f_2}{\partial z},\;\frac{\partial f_1}{\partial z}-\frac{\partial f_3}{\partial x},\;\frac{\partial f_2}{\partial x}-\frac{\partial f_1}{\partial y}\right).$$

### 5.2. Divergencia

La **divergencia** mide el flujo que se origina (fuente/manantial) o se destruye (sumidero) por unidad de volumen alrededor de cada punto. Su signo distingue una surgencia de una zona de convergencia.

- **En $\mathbb{R}^2$:** $\operatorname{div}(\mathbf{f})=\frac{\partial f_1}{\partial x}+\frac{\partial f_2}{\partial y}$.
- **En $\mathbb{R}^3$:** $\operatorname{div}(\mathbf{f})=\frac{\partial f_1}{\partial x}+\frac{\partial f_2}{\partial y}+\frac{\partial f_3}{\partial z}$.

### 5.3. Vector Tangente en Curvas

El operador diferencial natural de una curva $\mathbf{g}(t)=(x(t),y(t))$ es su **vector derivada**:
$$\mathbf{g}'(t)=\big(x'(t),\,y'(t)\big).$$

- **Interpretación física:** si $t$ es el tiempo, $\mathbf{g}'(t)$ es el **vector velocidad**: apunta en la dirección de avance y su módulo $\|\mathbf{g}'(t)\|$ es la rapidez.
- **Interpretación geométrica:** $\mathbf{g}'(t)$ es tangente a la trayectoria en $\mathbf{g}(t)$. La recta tangente en $t_0$ es $\mathbf{g}(t_0)+\lambda\,\mathbf{g}'(t_0)$.
- **Curva regular:** si $\mathbf{g}'(t)\neq\mathbf{0}$ para todo $t$, admite el **vector tangente unitario**
$$\mathbf{T}(t)=\frac{\mathbf{g}'(t)}{\|\mathbf{g}'(t)\|},$$
que depende de la trayectoria y de su orientación, no de la rapidez. Si $\mathbf{g}'(t_0)=\mathbf{0}$ puede aparecer una **cúspide** o punto singular.

**Relación con el gradiente.** Si $\mathbf{g}(t)$ recorre una curva de nivel $f(x,y)=c$, entonces $f(\mathbf{g}(t))=c$ para todo $t$; derivando (regla de la cadena) se obtiene
$$\nabla f(\mathbf{g}(t))\cdot\mathbf{g}'(t)=0:$$
el gradiente es perpendicular a la curva de nivel, como ya sabíamos por la propiedad 3 del gradiente.

![gradiente-tangente-curva-nivel.png\|480](/img/user/imagenes/gradiente-tangente-curva-nivel.png)

> [!summary] Qué operador para cada objeto
> | Objeto | Representación | Operador diferencial natural |
> |---|---|---|
> | Campo escalar $f:\mathbb{R}^2\to\mathbb{R}$ | Curvas de nivel / superficie | Gradiente $\nabla f$ |
> | Curva $\mathbf{g}:\mathbb{R}\to\mathbb{R}^2$ | Trayectoria + orientación | Derivada $\mathbf{g}'(t)$ (tangente) |
> | Campo vectorial $\mathbf{f}:\mathbb{R}^2\to\mathbb{R}^2$ | Flechas / líneas de campo | Rotacional $\operatorname{rot}$, divergencia $\operatorname{div}$ |

## 6. Optimización en Varias Variables

### 6.1. Puntos Críticos y Matriz Hessiana

Para hallar los extremos relativos (máximos y mínimos locales) de $f(x,y)$:

**Paso 1: puntos críticos.** Resolver el sistema
$$\nabla f=(0,0)\iff\begin{cases}f_x(x,y)=0\\ f_y(x,y)=0\end{cases}$$

**Paso 2: clasificar con el Hessiano.** Calcular las segundas derivadas y
$$H(x,y)=\begin{pmatrix}f_{xx}&f_{xy}\\ f_{yx}&f_{yy}\end{pmatrix},\qquad D(x,y)=f_{xx}f_{yy}-(f_{xy})^2.$$

**Paso 3: criterio.** En cada punto crítico $(a,b)$:

- Si $D(a,b)>0$ y $f_{xx}(a,b)>0$ $\implies$ **mínimo local**.
- Si $D(a,b)>0$ y $f_{xx}(a,b)<0$ $\implies$ **máximo local**.
- Si $D(a,b)<0$ $\implies$ **punto de silla**.
- Si $D(a,b)=0$ $\implies$ el criterio no decide.

### 6.2. Ejemplos Resueltos Paso a Paso

**Ejemplo:** Estudiar los extremos de $f(x,y)=5-x^2-y^2$.

1. $\nabla f=(-2x,-2y)=(0,0)\implies (0,0)$ es el único punto crítico.
2. $f_{xx}=-2$, $f_{xy}=0$, $f_{yy}=-2$, luego $H=\begin{pmatrix}-2&0\\0&-2\end{pmatrix}$ y $D=4>0$.
3. $D>0$ y $f_{xx}<0$: en $(0,0)$ hay un **máximo local**, con $f(0,0)=5$.

**Ejemplo:** Estudiar los extremos de $f(x,y)=x^3+y^3-3xy$.

1. $f_x=3x^2-3y=0\implies y=x^2$; $f_y=3y^2-3x=0\implies x^4=x$, de donde $x=0$ o $x=1$. Puntos críticos: $(0,0)$ y $(1,1)$.
2. $H(x,y)=\begin{pmatrix}6x&-3\\-3&6y\end{pmatrix}$.
3. En $(0,0)$: $D=-9<0\implies$ **punto de silla**. En $(1,1)$: $D=27>0$ y $f_{xx}=6>0\implies$ **mínimo local** ($f(1,1)=-1$).

### 6.3. Extremos Condicionados: Multiplicadores de Lagrange

Para optimizar $f(x,y)$ sujeta a una restricción (ligadura) $g(x,y)=c$. También vale para $f(x,y,z)$ con $g(x,y,z)=c$.

**Pasos:**

1. **Función Lagrangiana:**
$$L(\lambda,x,y)=f(x,y)-\lambda\bigl(g(x,y)-c\bigr)$$
2. **Puntos candidatos:** resolver $\nabla L=0$, es decir,
$$\begin{cases}f_x=\lambda g_x\\ f_y=\lambda g_y\\ g(x,y)=c\end{cases}$$
3. **Clasificar con el Hessiano orlado:**
$$\bar H=\begin{pmatrix}0&g_x&g_y\\ g_x&L_{xx}&L_{xy}\\ g_y&L_{yx}&L_{yy}\end{pmatrix},$$
donde $L_{xx}=f_{xx}-\lambda g_{xx}$, $L_{xy}=f_{xy}-\lambda g_{xy}$, etc. Evaluado en cada candidato $(x_0,y_0,\lambda_0)$:
   - $\det(\bar H)>0$ $\implies$ **máximo local**.
   - $\det(\bar H)<0$ $\implies$ **mínimo local**.
   - $\det(\bar H)=0$ $\implies$ el criterio no concluye.

[[01 Calculo-Naut/apuntes/calc-naut-tema04-ej\|Ejercicios]]
