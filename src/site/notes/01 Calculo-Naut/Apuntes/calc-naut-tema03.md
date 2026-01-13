---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema03/","updated":"2026-01-12T11:54:16.342+01:00"}
---

[[01 Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 3: Cálculo Integral de Varias Variables
- [[01 Calculo-Naut/Apuntes/calc-naut-tema03#1. Integrales Dobles\|1. Integrales Dobles]]
- [[01 Calculo-Naut/Apuntes/calc-naut-tema03#2. Integrales Triples\|2. Integrales Triples]]
- [[01 Calculo-Naut/Apuntes/calc-naut-tema03#3. Cambio de Variables\|3. Cambio de Variables]]
- [[01 Calculo-Naut/Apuntes/calc-naut-tema03#Ejercicios\|Ejercicios]]


## 1. Integrales Dobles

**Idea:** De manera análoga a cómo en una variable sumamos una infinidad de rectángulos diminutos para calcular el área bajo una curva, en el cálculo de varias variables extendemos este concepto. Con las integrales dobles, sumamos una infinidad de prismas rectangulares infinitesimalmente delgados para determinar el volumen total que se encuentra bajo una superficie.
![Pasted image 20251124121347.png|600](/img/user/imagenes/Pasted%20image%2020251124121347.png)
### Teorema de Fubini
Permite calcular integrales dobles como integrales iteradas (o sucesivas).
- **Sobre Rectángulos**: Si $\Omega = [a,b] \times [c,d]$: 
$$\iint_{\Omega} f(x,y) \, dA = \int_a^b \left( \int_c^d f(x,y) \, dy \right) dx = \int_c^d \left( \int_a^b f(x,y) \, dx \right) dy$$
- **Sobre Regiones Generales:**
     - Tipo I (Vertical): $\Omega = \{(x,y) \in \mathbb{R}^2 : a \le x \le b, \, g_1(x) \le y \le g_2(x)\}$, 
$$\iint_{\Omega} f(x,y) \, dA = \int_a^b \int_{g_1(x)}^{g_2(x)} f(x,y) \, dy \, dx$$
    - Tipo II (Horizontal): $\Omega = \{(x,y) \in \mathbb{R}^2 : c \le y \le d, \, h_1(y) \le x \le h_2(y)\}$, 
$$\iint_{\Omega} f(x,y) \, dA = \int_c^d \int_{h_1(y)}^{h_2(y)} f(x,y) \, dx \, dy$$
### Cambio de Orden de Integración
Consiste en describir una región de Tipo I como una región de Tipo II (o viceversa) para facilitar la integración. Es fundamental dibujar la región de integración.

### Aplicaciones
- **Volumen bajo superficie:** $V = \iint_{\Omega} (z_{techo}(x,y) - z_{suelo}(x,y)) \, dA$
- **Área (2D):** $A(\Omega) = \iint_{\Omega} 1 \, dA$

Dada una lámina $\Omega$ con función de densidad superficial $\sigma(x,y)$:
- **Masa:** $M = \iint_{\Omega} \sigma(x,y) \, dA$
- **Centro de Gravedad $(\bar{x}, \bar{y})$:**
    - $\bar{x} = \frac{M_y}{M}$
    - $\bar{y} = \frac{M_x}{M}$
    siendo 
    - $M_x = \iint_{\Omega} y \cdot \sigma(x,y) \, dA$
    - $M_y = \iint_{\Omega} x \cdot \sigma(x,y) \, dA$
    Nota: Si la densidad es constante, el centro de gravedad se llama centroide.

---

## 2. Integrales Triples

Se calculan de forma análoga a las dobles, usando el Teorema de Fubini.

- Sobre Cajas Rectangulares: Si $\Omega = [a,b] \times [c,d] \times [e,f]$:
    
    $$\iiint_{\Omega} f(x,y,z) \, dV = \int_a^b \int_c^d \int_e^f f(x,y,z) \, dz \, dy \, dx \quad \text{(y los otros 5 órdenes)}$$
    
Ejemplo: 
Calcular la integral de la función $f(x,y,z) = x + yz$ sobre la caja $B = [0,1] \times [0,2] \times [0,1]$.
Al ser una caja rectangular, los límites son constantes. Podemos elegir cualquier orden. Usaremos el orden $dz\,dy\,dx$.

$$I = \int_0^1 \int_0^2 \int_0^1 (x + yz) \, dz \, dy \, dx$$

**Resolución paso a paso:**
    $$\int_0^1 (x + yz) \, dz = \left[ xz + y\frac{z^2}{2} \right]_{z=0}^{z=1} = \left(x(1) + \frac{y}{2}\right) - 0 = x + \frac{y}{2}$$
    $$\int_0^2 \left( x + \frac{y}{2} \right) \, dy = \left[ xy + \frac{y^2}{4} \right]_{y=0}^{y=2} = \left(2x + \frac{4}{4}\right) - 0 = 2x + 1$$
        $$\int_0^1 (2x + 1) \, dx = \left[ x^2 + x \right]_0^1 = (1+1) - 0 = \mathbf{2}$$
    

- Sobre Regiones Generales: Si $W \subset \mathbb{R}^3$ se proyecta sobre una región $\Omega$ en el plano $XY$, y está limitada superior e inferiormente por $z=u_2(x,y)$ y $z=u_1(x,y)$:
    
    $$\iiint_W f(x,y,z) \, dV = \iint_{\Omega} \left( \int_{u_1(x,y)}^{u_2(x,y)} f(x,y,z) \, dz \right) dA$$
    - Otra forma de hacerlo consiste en  proyectar sobre el eje $z$, dando lugar a un intervalo $[a,b]$, y luego integrar la sección horizontal (rebanadas) $\Omega_z$ resultante para cada $z$:
    $$\iiint_W f(x,y,z) \, dV = \int_a^b \left( \iint_{\Omega(z)} f(x,y,z) \, dA \right) dz$$
    Ejemplo: Imagina un tetraedro (una pirámide triangular) limitado por los planos coordenados ($x=0, y=0, z=0$) y el plano inclinado $x + y + z = 1$.

El objetivo: Calcular $\iiint_W 2z \, dV$ usando el método de rebanadas horizontales.

- **Límites de $z$:** El sólido va desde el suelo ($z=0$) hasta el pico más alto donde $x=0, y=0$, por lo que $z=1$. El intervalo es $[0,1]$.
    
- **La sección $\Omega(z)$:** Para un $z$ fijo, cortamos la pirámide horizontalmente. La forma resultante es un **triángulo** en el plano $XY$ limitado por $x=0$, $y=0$ y la recta $x+y = 1-z$ (despejando de la ecuación del plano).
    

Planteamiento:

La integral se ve así: $\int_0^1 \left[ \iint_{\Omega(z)} f(x,y,z) \, dA \right] dz$

1. Resolvemos primero la integral doble (la rebanada):
    
    Como la función a integrar es $2z$, y dentro de la integral doble $z$ es una constante, podemos sacarla fuera de la integral interior:
    
    $$\iint_{\Omega(z)} 2z \, dA = 2z \cdot \iint_{\Omega(z)} 1 \, dA = 2z \cdot \text{Área}(\Omega(z))$$
    
    Nota: $\iint 1 dA$ es simplemente el área de la región.
    
    La región $\Omega(z)$ es un triángulo rectángulo con catetos de longitud $(1-z)$.
    
    $$\text{Área} = \frac{\text{base} \cdot \text{altura}}{2} = \frac{(1-z)(1-z)}{2} = \frac{(1-z)^2}{2}$$
    
    Por tanto, el resultado de la integral interior es:
    
    $$2z \cdot \frac{(1-z)^2}{2} = z(1-z)^2$$
    
2. Resolvemos la integral exterior (respecto a $z$):
    
    Ahora integramos ese resultado desde $z=0$ hasta $z=1$:
    
    $$I = \int_0^1 z(1-z)^2 \, dz$$
    
    Expandimos el binomio: $(1-z)^2 = 1 - 2z + z^2$. Multiplicamos por $z$:
    
    $$I = \int_0^1 (z - 2z^2 + z^3) \, dz$$
    
    Calculamos la primitiva:
    
    $$\left[ \frac{z^2}{2} - \frac{2z^3}{3} + \frac{z^4}{4} \right]_0^1 = \frac{1}{2} - \frac{2}{3} + \frac{1}{4}$$
    
    Mínimo común múltiplo (12):
    
    $$\frac{6}{12} - \frac{8}{12} + \frac{3}{12} = \frac{1}{12}$$
    

**Resultado Final:** $\mathbf{\frac{1}{12}}$

### Aplicaciones en Sólidos (3D)

Dada una región sólida $W$ con función de densidad volumétrica $\rho(x,y,z)$:

- **Masa:** $M = \iiint_W \rho(x,y,z) \, dV$
    

## 3. Cambio de Variables
### Jacobiano
Si un cambio de variables viene dado por $x=x(u,v)$ e $y=y(u,v)$, el Jacobiano de la transformación es:
$$J(u,v) = \det \begin{pmatrix} \frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} \end{pmatrix}$$
La fórmula del cambio de variable es:
$$\iint_{\Omega} f(x,y) \, dx \, dy = \iint_{\Omega^*} f(x(u,v), y(u,v)) \, |J(u,v)| \, du \, dv$$
Para 3D, el Jacobiano es el determinante de la matriz 3x3 de derivadas parciales.

### Coordenadas Polares (en 2D)
Es un cambio de variable específico para simetría circular.
- **Transformación:** $x = r \cos \theta$, $y = r \sin \theta$ 
- **Jacobiano:** $J(r, \theta) = r$
- **Elemento de área:** $dA = r \, dr \, d\theta$
##### Ejemplo: volumen bajo un Paraboloide

Imagina que queremos calcular la integral doble de la función $f(x, y) = x^2 + y^2$ sobre una región $D$, donde $D$ es un círculo centrado en el origen con radio 2.

$$I = \iint_D (x^2 + y^2) \, dA$$
Si intentáramos resolver esto con $x$ e $y$, la integral se vería así:
$$\int_{-2}^{2} \int_{-\sqrt{4-x^2}}^{\sqrt{4-x^2}} (x^2 + y^2) \, dy \, dx$$

Resolver esas raíces cuadradas dentro de la integral es largo y complicado.
Transformaremos todo a términos de radio ($r$) y ángulo ($\theta$).
1.  **Cambio de Variables:** $x^2 + y^2$ se convierte en $r^2$.
2.  **El Diferencial de Área:** $dA$ no es solo $dr \, d\theta$. Debes multiplicar por el Jacobiano, que es **$r$**.
    $$dx \, dy \Rightarrow r \, dr \, d\theta$$
3.  **Nuevos Límites:**
    * **Radio ($r$):** Como es un círculo de radio 2, $r$ va de $0$ a $2$.
    * **Ángulo ($\theta$):** Como es el círculo completo, $\theta$ da la vuelta entera, de $0$ a $2\pi$.


Sustituimos todo en la integral original:
$$I = \int_{0}^{2\pi} \int_{0}^{2} \underbrace{(r^2)}_{\text{función}} \cdot \underbrace{r \, dr \, d\theta}_{\text{dA (con el Jacobiano)}}$$
$$I = \int_{0}^{2\pi} \int_{0}^{2} r^3 \, dr \, d\theta$$

**Paso A: Integral interna (respecto a $r$)**
Integramos $r^3$:
$$\left[ \frac{r^4}{4} \right]_{0}^{2} = \frac{2^4}{4} - \frac{0^4}{4} = \frac{16}{4} = 4$$

**Paso B: Integral externa (respecto a $\theta$)**
Ahora integramos la constante que nos quedó ($4$):
$$\int_{0}^{2\pi} 4 \, d\theta = \left[ 4\theta \right]_{0}^{2\pi}$$
$$= 4(2\pi) - 4(0)$$

**Resultado Final:**
$$8\pi$$


### Coordenadas Cilíndricas (en 3D)

Extensión de las polares a 3D. Útil para cilindros, conos, paraboloides.

- **Transformación:** $x = r \cos \theta$, $y = r \sin \theta$, $z = z$
    
- **Relación útil:** $x^2 + y^2 = r^2$
    
- **Elemento de volumen:** $dV = r \, dz \, dr \, d\theta$
    

### Coordenadas Esféricas (en 3D)

Útil para esferas y conos. (Convención ISO: $\rho$ = radio, $\phi$ = ángulo polar (desde Z+), $\theta$ = ángulo azimutal (desde X+)).

- **Transformación:**
    
    - $x = \rho \sin \phi \cos \theta$
        
    - $y = \rho \sin \phi \sin \theta$
        
    - $z = \rho \cos \phi$
        
- **Relaciones útiles:** $x^2 + y^2 + z^2 = \rho^2$, $x^2 + y^2 = \rho^2 \sin^2 \phi$
    
- **Elemento de volumen (Jacobiano = $\rho^2 \sin \phi$):** $dV = \rho^2 \sin \phi \, d\rho \, d\phi \, d\theta$
    

---

## Ejercicios
[[01 Calculo-Naut/Apuntes/calc-naut-tema03-ej\|Enlace]].