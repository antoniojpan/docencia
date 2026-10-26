---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema05/","created":"2026-10-23T09:16:31.114+02:00","updated":"2026-10-24T08:57:02.305+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Tema 5: Cálculo diferencial en Varias Variables

## 1. Funciones de Varias Variables

### 1.1. Concepto y Tipos de Funciones

Las funciones de varias variables son transformaciones matemáticas que dependen de más de una entrada de datos y/o pueden devolver varios valores numéricos. Se clasifican según sus espacios de origen (dominio) y llegada (codominio):

- **Campos escalares en el plano o en el espacio ($f: \mathbb{R}^N \to \mathbb{R}$):** Asignan un único valor numérico a un par de entradas $(x, y)$.
  - *Ejemplo real:* El coste total $f(x, y) = x \cdot y$ al comprar $x \text{ kg}$ de tomates a un precio de $y \text{ €/kg}$.
- **Curvas en el espacio ($\mathbf{g}: \mathbb{R} \to \mathbb{R}^N$):** Dependen de una única variable independiente (habitualmente el tiempo $t$) y devuelven una posición vectorial.
  - *Ejemplo real:* La latitud y longitud de un ciclista en función del tiempo: $t \mapsto (x(t), y(t))$.
- **Campos vectoriales en el plano ($\mathbf{f}: \mathbb{R}^2 \to \mathbb{R}^2$):** Asignan un vector de velocidad o fuerza a cada punto del plano.
  - *Ejemplo real:* La velocidad del viento $(u, v)$ en cada posición geográfica $(x, y)$.
- **Campos vectoriales en el espacio ($\mathbf{f}: \mathbb{R}^3 \to \mathbb{R}^3$):** Describen la velocidad o fuerza en un punto tridimensional.
  - *Ejemplo real:* La velocidad de una corriente de agua o aire $(u, v, w)$ en un punto espacial $(x, y, z)$.

### 1.2. Representación Gráfica

Cada tipo de función exige una representación gráfica distinta. En el plano distinguimos tres casos fundamentales: los **campos escalares** ($f: \mathbb{R}^2 \to \mathbb{R}$) se visualizan mediante curvas de nivel, las **curvas parametrizadas** ($\mathbf{g}: \mathbb{R} \to \mathbb{R}^2$) mediante su trayectoria, y los **campos vectoriales** ($\mathbf{f}: \mathbb{R}^2 \to \mathbb{R}^2$) mediante flechas o líneas de campo.

#### 1.2.1. Campos escalares: curvas de nivel

Para visualizar un campo escalar $f: \mathbb{R}^2 \to \mathbb{R}$, resulta muy útil emplear **curvas de nivel**. Una curva de nivel es el conjunto de puntos $(x, y)$ del plano donde la función toma un valor constante $c$:

$$f(x, y) = c$$

- **Isotermas:** Curvas de nivel donde la temperatura permanece constante.
- **Isobaras:** Curvas de nivel donde la presión atmosférica es constante.

![campo-escalar-curvas-nivel.png\|500](/img/user/imagenes/campo-escalar-curvas-nivel.png)

En la figura, el color indica el valor de $f$ (mapa de calor) y las líneas blancas son las curvas de nivel $f(x,y)=c$ para $c=1,2,4,6,8$. Obsérvese que las curvas se acumulan donde la función crece más deprisa: la separación entre curvas mide, de forma cualitativa, el módulo del gradiente.

La misma información puede verse en tres dimensiones: la **gráfica** de $f$ es una superficie (la "montaña"), y las curvas de nivel son los **cortes horizontales** de esa superficie a distintas alturas, proyectados sobre el plano $z=0$:

![campo-escalar-superficie-3d.png\|520](/img/user/imagenes/campo-escalar-superficie-3d.png)

En esta figura se ha representado la "montaña gaussiana" $f(x,y)=3e^{-(x^2+y^2)/2}$. Cada curva de nivel de la base es la proyección de los puntos de la superficie que están a la misma altura $c$. Las dos representaciones son complementarias: el mapa de curvas de nivel es fácil de leer y de superponer a un plano (un mapa topográfico), mientras que la superficie muestra de un vistazo la forma global del campo y la posición de sus máximos, mínimos y pendientes.

#### 1.2.2. Curvas parametrizadas en el plano

Una curva en el plano es la imagen de una función $\mathbf{g}: \mathbb{R} \to \mathbb{R}^2$,

$$\mathbf{g}(t) = \big(x(t),\, y(t)\big),$$

donde $t$ recorre un intervalo (habitualmente el tiempo). La gráfica es la **trayectoria** de la curva, es decir, el conjunto de puntos recorridos; el parámetro $t$ añade dos informaciones que la trayectoria por sí sola no contiene:

- **Orientación:** el sentido en que se recorre la curva al aumentar $t$.
- **Velocidad:** el vector tangente $\mathbf{g}'(t) = (x'(t), y'(t))$, que indica dirección y rapidez de recorrido en cada instante.

![curva-parametrizada-plano.png\|500](/img/user/imagenes/curva-parametrizada-plano.png)

En la figura se representa la curva cerrada $\mathbf{g}(t)=\big(r(t)\cos t,\; r(t)\sin t\big)$ con $r(t)=1+0{,}35\,\mathrm{sen}(4t)$ y $t \in [0, 2\pi]$. El punto rojo es $\mathbf{g}(t_0)$ y la flecha verde su vector velocidad $\mathbf{g}'(t_0)$.

#### 1.2.3. Campos vectoriales en el plano

Un campo vectorial en el plano asigna un vector a cada punto:

$$\mathbf{f}(x,y) = \big(u(x,y),\, v(x,y)\big).$$

Se representa dibujando en cada punto $(x,y)$ una flecha con origen en él y dirección y sentido del vector $\mathbf{f}(x,y)$. Para que la imagen sea legible se suele:

- **Normalizar o escalar las flechas**, ya que su longitud real puede variar en órdenes de magnitud y tapar el dibujo.
- **Colorear según la norma** $\|\mathbf{f}(x,y)\|$, lo que añade información cuantitativa.
- **Superponer líneas de campo** (*streamlines*), curvas tangentes en cada punto al campo, que describen las trayectorias de las partículas.

![campo-vectorial-plano.png\|500](/img/user/imagenes/campo-vectorial-plano.png)

En la figura se muestra el campo de rotación $\mathbf{f}(x,y)=(-y,\,x)$: las flechas giran alrededor del origen, el color codifica $\|\mathbf{f}\|=\sqrt{x^2+y^2}$ y las líneas negras son circunferencias, es decir, las trayectorias de una partícula arrastrada por el campo.


## 2. Dominio, Límites y Continuidad

### 2.1. Dominio

El **dominio** de una función $f$ de varias variables, $Dom(f)$, es el conjunto de puntos donde está definida. Hay que identificar las operaciones con restricciones:

1. **Denominadores:** si $f=\frac{g}{h}$, debe ser $h(x,y)\neq 0$.
2. **Raíces de índice par:** si $f=\sqrt{g}$, debe ser $g(x,y)\ge 0$.
3. **Logaritmos:** si $f=\log g$, debe ser $g(x,y)>0$.
4. **Trigonométricas inversas:** si $f=\arcsin g$ o $\arccos g$, debe ser $g(x,y)\in[-1,1]$.

Los polinomios, $e^{g}$, $\operatorname{sen} g$ y $\cos g$ están definidos siempre que lo esté $g$.

### 2.2. Límites y Continuidad

El cálculo de límites en funciones de varias variables presenta una elevada complejidad al existir infinitos caminos de aproximación a un punto del plano o del espacio.

**Criterio de continuidad:** Una función de varias variables es continua en un punto si y solo si todas sus **funciones componentes** son continuas en dicho punto.

> [!example] Ejemplo 2.1: Continuidad por Componentes
> Estudiar la continuidad de la función vectorial $f(x, y) = (x^2 + y, \; x - y)$.
>
> **Solución:**
> Dado que las funciones componentes $f_1(x, y) = x^2 + y$ y $f_2(x, y) = x - y$ son polinomios de dos variables, son continuas en todo $\mathbb{R}^2$. Por tanto, la función vectorial $f(x, y)$ es continua en todo su dominio.

---

## 3. Derivadas Parciales

### 3.1. Definición e Interpretación

Hallar la **derivada parcial** de una función respecto a una variable consiste en derivar de la manera tradicional respecto a dicha variable, tratando a todas las demás variables como si fueran constantes.

- **Interpretación:** La derivada parcial de $f$ respecto a $x$ ($\frac{\partial f}{\partial x}$ o $f_x$) mide la tasa de variación o la influencia de la variable $x$ en el comportamiento global de $f$.

> [!example] Ejemplo 3.1: Derivadas Parciales en 3 Variables
> Dada la función $f(x, y, z) = \sqrt{x} + yz$, calcular sus derivadas parciales.
>
> **Solución:**
>
> - Respecto a $x$ (tratando $y, z$ como constantes):
>   $$\frac{\partial f}{\partial x} = \frac{1}{2\sqrt{x}}$$
> - Respecto a $y$ (tratando $x, z$ como constantes):
>   $$\frac{\partial f}{\partial y} = z$$
> - Respecto a $z$ (tratando $x, y$ como constantes):
>   $$\frac{\partial f}{\partial z} = y$$

> [!example] Ejemplo 3.2: Derivadas Parciales de un Cociente
> Calcular las derivadas parciales de $g(x, y) = \frac{x - y}{xy}$.
>
> **Solución:**
>
> - Respecto a $x$:
>   $$g_x = \frac{1 \cdot (xy) - (x - y) \cdot y}{(xy)^2} = \frac{xy - xy + y^2}{x^2 y^2} = \frac{y^2}{x^2 y^2} = \mathbf{\frac{1}{x^2}}$$
> - Respecto a $y$:
>   $$g_y = \frac{-1 \cdot (xy) - (x - y) \cdot x}{(xy)^2} = \frac{-xy - x^2 + xy}{x^2 y^2} = \frac{-x^2}{x^2 y^2} = \mathbf{-\frac{1}{y^2}}$$
>
> *Nota sobre la influencia:* Si $f(x, y, z) = y z^3 + 3$, se observa que $f_x = 0$, lo que indica que la variable $x$ no influye en absoluto en el valor de la función.

---

### 3.2. Diferenciabilidad

Una función $f$ es **diferenciable** en $P_0=(a,b)$ si, cerca de ese punto, se puede aproximar por un plano (una función lineal) con un error que se hace despreciable al acercarse a $P_0$. Que existan las derivadas parciales **no garantiza** la diferenciabilidad: la función puede tener un "pico" al movernos en otras direcciones.

**Condición suficiente (la que se aplica en la práctica):** si $f_x$ y $f_y$ existen y son continuas en un entorno de $(a,b)$, entonces $f$ es diferenciable en $(a,b)$.

- Diferenciable $\implies$ continua.
- Diferenciable $\implies$ existen todas las derivadas parciales (el recíproco es falso).

---

## 4. Gradiente y Derivada Direccional

### 4.1. El Vector Gradiente

Dado un campo escalar $f(x, y)$, el **gradiente** es un vector formado por las derivadas parciales primeras de la función en cada punto:

$$\nabla f = \left( \frac{\partial f}{\partial x}, \; \frac{\partial f}{\partial y} \right)$$

- **Propiedad fundamental:** El vector gradiente $\nabla f(x_0, y_0)$ apunta siempre en la **dirección de máximo crecimiento** de la función en ese punto, y su módulo representa la tasa máxima de aumento.

### 4.2. Derivada Direccional

La **derivada direccional** de $f$ en un punto $P$ en la dirección de un **vector unitario** $\vec u$ mide la tasa de cambio de $f$ en esa dirección:

$$D_{\vec u}f(P) = \nabla f(P) \cdot \vec u$$

- Si $D_{\vec u}f = 0$, el movimiento en la dirección $\vec u$ se realiza a lo largo de una **curva de nivel** (sin cambio en el valor de la función).
- Si la dirección viene dada por un vector $\vec v$ no unitario, primero se normaliza: $\vec u = \dfrac{\vec v}{\|\vec v\|}$.

> [!example] Ejemplo 4.1: Gradiente y Derivada Direccional
> Dada la función $f(x, y) = x^2 y + \sqrt{x}$:
>
> 1. **Calcular el gradiente $\nabla f$:**
>    $$\frac{\partial f}{\partial x} = 2yx + \frac{1}{2\sqrt{x}}, \qquad \frac{\partial f}{\partial y} = x^2$$
>    $$\nabla f = \left( 2yx + \frac{1}{2\sqrt{x}}, \; x^2 \right)$$
>
> 2. **Calcular la derivada direccional en el punto $(2, 1)$ en la dirección de $\vec v = (3, 5)$.** Como $\|\vec v\|=\sqrt{34}$, hay que normalizar:
>    $$D_{\vec u} f(2, 1) = \frac{3\left( 4 + \frac{1}{2\sqrt{2}} \right) + 5\,(4)}{\sqrt{34}} \approx \mathbf{5.67}$$
>    *Interpretación:* Si nos encontramos en la posición $(2, 1)$ y nos desplazamos en la dirección $(3, 5)$, la altitud o valor de la función aumenta a una razón de $5.67$ unidades por unidad de longitud.

> [!example] Ejemplo 4.2: Máximo Ascenso en una Montaña
> Dada la superficie de una montaña descrita por $A(x, y) = \frac{x^2 + y^2}{10} + 50$, determinar hacia dónde debemos movernos desde el punto $(2, -1)$ para llegar lo más rápido posible a la cima.
>
> **Solución:**
> Debemos movernos en la dirección del gradiente $\nabla A(2, -1)$:
> $$\nabla A = \left( \frac{2x}{10}, \; \frac{2y}{10} \right) = \left( \frac{x}{5}, \; \frac{y}{5} \right)$$
> Evaluando en el punto $(2, -1)$:
> $$\nabla A(2, -1) = \mathbf{\left( \frac{2}{5}, \; -\frac{1}{5} \right)}$$

---

## 5. Operadores Diferenciales

A cada tipo de objeto geométrico le corresponde un operador diferencial natural: el **gradiente** actúa sobre campos escalares, la **derivada** sobre curvas y el **rotacional** y la **divergencia** sobre campos vectoriales.

### 5.1. Rotacional

El **rotacional** mide la tendencia de un campo vectorial a girar o inducir rotación en el flujo alrededor de cada punto.

- **En $\mathbb{R}^2 \to \mathbb{R}^2$:** Para $\mathbf{f}(x, y) = (f_1, f_2)$:
  $$\operatorname{rot}(\mathbf{f}) = \frac{\partial f_2}{\partial x} - \frac{\partial f_1}{\partial y} = \begin{vmatrix} \frac{\partial}{\partial x} & \frac{\partial}{\partial y} \\ f_1 & f_2 \end{vmatrix}$$

- **En $\mathbb{R}^3 \to \mathbb{R}^3$:** Para $\mathbf{f}(x, y, z) = (f_1, f_2, f_3)$:
  $$\operatorname{rot}(\mathbf{f}) = \nabla \times \mathbf{f} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ f_1 & f_2 & f_3 \end{vmatrix} = \left( \frac{\partial f_3}{\partial y} - \frac{\partial f_2}{\partial z}, \; \frac{\partial f_1}{\partial z} - \frac{\partial f_3}{\partial x}, \; \frac{\partial f_2}{\partial x} - \frac{\partial f_1}{\partial y} \right)$$

> [!example] Ejemplo 5.1: Rotacional en el Plano y en el Espacio
> 1. **Para $\mathbf{f}(x, y) = (x^2 y, \; x + y)$:**
>    $$\operatorname{rot}(\mathbf{f}) = \frac{\partial (x+y)}{\partial x} - \frac{\partial (x^2 y)}{\partial y} = \mathbf{1 - x^2}$$
> 2. **Para $\mathbf{f}(x, y, z) = \left( xy, \; x^2 - y, \; \frac{1}{z} \right)$:**
>    $$\operatorname{rot}(\mathbf{f}) = \left( 0 - 0, \; 0 - 0, \; 2x - x \right) = \mathbf{(0, 0, x)}$$

### 5.2. Divergencia

La **divergencia** mide la cantidad de flujo que se origina (fuente/manantial) o se destruye (sumidero) por unidad de volumen alrededor de cada punto.

- **En $\mathbb{R}^2$:** $\operatorname{Div}(\mathbf{f}) = \frac{\partial f_1}{\partial x} + \frac{\partial f_2}{\partial y}$
- **En $\mathbb{R}^3$:** $\operatorname{Div}(\mathbf{f}) = \frac{\partial f_1}{\partial x} + \frac{\partial f_2}{\partial y} + \frac{\partial f_3}{\partial z}$

> [!example] Ejemplo 5.2: Cálculo de la Divergencia
> Para el campo $\mathbf{f}(x, y, z) = \left( \frac{x}{y}, \; z - y, \; \frac{x^2}{z} \right)$:
> $$\operatorname{Div}(\mathbf{f}) = \frac{\partial}{\partial x}\left(\frac{x}{y}\right) + \frac{\partial}{\partial y}(z - y) + \frac{\partial}{\partial z}\left(\frac{x^2}{z}\right) = \frac{1}{y} - 1 - \frac{x^2}{z^2} = \mathbf{\frac{z^2 - yz^2 - x^2 y}{y z^2}}$$

### 5.3. Vector Tangente en Curvas

Así como el gradiente describe la variación de un campo escalar y el rotacional/divergencia la de un campo vectorial, el operador diferencial natural de una curva $\mathbf{g}(t) = (x(t), y(t))$ es su **vector derivada**:

$$\mathbf{g}'(t) = \big(x'(t),\, y'(t)\big)$$

- **Interpretación física:** Si $t$ es el tiempo, $\mathbf{g}'(t)$ es el **vector velocidad**: apunta en la dirección de avance y su módulo $\|\mathbf{g}'(t)\|$ es la rapidez.
- **Interpretación geométrica:** $\mathbf{g}'(t)$ es tangente a la trayectoria de la curva en el punto $\mathbf{g}(t)$. La recta tangente en $t_0$ es
  $$\mathbf{g}(t_0) + \lambda\, \mathbf{g}'(t_0), \qquad \lambda \in \mathbb{R}.$$
- **Curva regular:** Si $\mathbf{g}'(t) \neq \mathbf{0}$ para todo $t$, la curva es *regular* y admite el **vector tangente unitario**
  $$\mathbf{T}(t) = \frac{\mathbf{g}'(t)}{\|\mathbf{g}'(t)\|},$$
  que solo depende de la trayectoria y de su orientación, no de la rapidez con que se recorra. Si $\mathbf{g}'(t_0) = \mathbf{0}$ puede aparecer una **cúspide** o un punto singular.

**Relación con el gradiente.** Si la curva $\mathbf{g}(t)$ recorre una curva de nivel $f(x,y) = c$, entonces $f(\mathbf{g}(t)) = c$ para todo $t$; derivando por la regla de la cadena:

$$\nabla f(\mathbf{g}(t)) \cdot \mathbf{g}'(t) = 0.$$

Es decir, **el gradiente es perpendicular a las curvas de nivel**: $\nabla f$ apunta en la dirección de máximo crecimiento y el vector tangente en la dirección en que $f$ no cambia.

![gradiente-tangente-curva-nivel.png\|480](/img/user/imagenes/gradiente-tangente-curva-nivel.png)

> [!example] Ejemplo 5.3: Vector Tangente y Ortogonalidad con el Gradiente
> Dada la curva $\mathbf{g}(t) = (t, t^2)$ y el campo escalar $f(x, y) = x^2 + y^2$:
>
> 1. **Vector tangente en $t = 1$:**
>    $$\mathbf{g}'(t) = (1, 2t) \implies \mathbf{g}'(1) = \mathbf{(1, 2)}$$
>    La recta tangente en $\mathbf{g}(1) = (1, 1)$ es $(1, 1) + \lambda(1, 2)$, es decir, $y = 2x - 1$.
> 2. **Vector tangente unitario en $t = 1$:**
>    $$\|\mathbf{g}'(1)\| = \sqrt{1 + 4} = \sqrt{5} \implies \mathbf{T}(1) = \left( \frac{1}{\sqrt{5}}, \frac{2}{\sqrt{5}} \right)$$
> 3. **¿Es $\mathbf{g}$ una curva de nivel de $f$?** No: $f(\mathbf{g}(t)) = t^2 + t^4$ no es constante, luego $\nabla f \cdot \mathbf{g}' \neq 0$. En efecto, en $t=1$:
>    $$\nabla f(1,1) = (2, 2), \qquad \nabla f \cdot \mathbf{g}'(1) = 2 + 4 = 6 \neq 0$$
>    La curva **no** es una curva de nivel: al movernos por ella, $f$ aumenta. Para la circunferencia $\mathbf{g}(t) = (\cos t, \sin t)$, en cambio, $f(\mathbf{g}(t)) = 1$ es constante y se comprueba que $\nabla f \cdot \mathbf{g}' = (2\cos t, 2\sin t) \cdot (-\sin t, \cos t) = 0$.

> [!summary] Qué operador para cada objeto
> | Objeto | Representación | Operador diferencial natural |
> |---|---|---|
> | Campo escalar $f: \mathbb{R}^2 \to \mathbb{R}$ | Curvas de nivel / superficie | Gradiente $\nabla f$ |
> | Curva $\mathbf{g}: \mathbb{R} \to \mathbb{R}^2$ | trayectoria + orientación | Derivada $\mathbf{g}'(t)$ (tangente) |
> | Campo vectorial $\mathbf{f}: \mathbb{R}^2 \to \mathbb{R}^2$ | Flechas / líneas de campo | Rotacional, divergencia |

---

## 6. Optimización en Varias Variables

### 6.1. Puntos Críticos y Matriz Hessiana

Para hallar los extremos relativos (máximos y mínimos locales) de una función escalar $f(x, y)$:

1. **Hallar los puntos críticos:** Resolver el sistema de ecuaciones dado por el gradiente nulo:
   $$\nabla f = (0, 0) \iff \begin{cases} f_x(x, y) = 0 \\ f_y(x, y) = 0 \end{cases}$$

2. **Construir la Matriz Hessiana $H$:** Matriz de derivadas parciales segundas:
   $$H(x, y) = \begin{pmatrix} f_{xx} & f_{xy} \\ f_{yx} & f_{yy} \end{pmatrix}$$

3. **Criterio del Determinante de $H$:** Evaluar $\det(H)$ en cada punto crítico:
   - **Si $\det(H) > 0$ y $f_{xx} > 0$:** Existe un **Mínimo Local**.
   - **Si $\det(H) > 0$ y $f_{xx} < 0$:** Existe un **Máximo Local**.
   - **Si $\det(H) < 0$:** Existe un **Punto de Silla** (la función sube en una dirección y baja en otra).
   - **Si $\det(H) = 0$:** El criterio **no es concluyente** (caso dudoso).

### 6.2. Ejemplos Resueltos Paso a Paso

> [!example] Ejemplo 6.1: Análisis de Extremos Relativos
> Estudiar los puntos críticos de $f(x, y) = 5 - x^2 - y^2$.
>
> **Solución:**
>
> 1. **Gradiente:** $\nabla f = (-2x, -2y) = (0, 0) \implies \begin{cases} -2x = 0 \implies x = 0 \\ -2y = 0 \implies y = 0 \end{cases} \implies C_1 = (0, 0)$.
> 2. **Matriz Hessiana:**
>    $$f_{xx} = -2, \quad f_{xy} = 0, \quad f_{yy} = -2 \implies H = \begin{pmatrix} -2 & 0 \\ 0 & -2 \end{pmatrix}$$
> 3. **Clasificación en $(0,0)$:**
>    $$\det(H) = (-2)(-2) - 0 = 4 > 0 \quad \text{y} \quad f_{xx} = -2 < 0$$
>    Por tanto, en el punto $(0, 0)$ la función presenta un **Máximo Local** de valor $f(0,0) = 5$.

> [!example] Ejemplo 6.2: Clasificación de Puntos Críticos Compleja
> Estudiar los extremos de $f(x, y) = x^3 + y^3 - 3xy$.
>
> **Solución:**
>
> 1. **Puntos críticos:**
>    $$\nabla f = (3x^2 - 3y, \; 3y^2 - 3x) = (0, 0) \implies \begin{cases} 3x^2 - 3y = 0 \implies y = x^2 \\ 3y^2 - 3x = 0 \implies 3(x^2)^2 - 3x = 0 \implies 3x(x^3 - 1) = 0 \end{cases}$$
>    De aquí obtenemos dos soluciones: $x = 0 \implies y = 0$ y $x = 1 \implies y = 1$.
>    Puntos críticos: **$C_1(0, 0)$** y **$C_2(1, 1)$**.
> 2. **Matriz Hessiana general:**
>    $$H(x, y) = \begin{pmatrix} 6x & -3 \\ -3 & 6y \end{pmatrix}$$
> 3. **Clasificación de los puntos:**
>
>    - **Para $C_1(0, 0)$:**
>      $$H(0, 0) = \begin{pmatrix} 0 & -3 \\ -3 & 0 \end{pmatrix} \implies \det(H) = 0 - 9 = -9 < 0$$
>      Al ser $\det(H) < 0$, el punto $(0, 0)$ es un **Punto de Silla**.
>    - **Para $C_2(1, 1)$:**
>      $$H(1, 1) = \begin{pmatrix} 6 & -3 \\ -3 & 6 \end{pmatrix} \implies \det(H) = 36 - 9 = 27 > 0 \quad \text{y} \quad f_{xx} = 6 > 0$$
>      Al ser $\det(H) > 0$ y $f_{xx} > 0$, la función presenta un **Mínimo Local** en $(1, 1)$.