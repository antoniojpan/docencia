---
{"dg-publish":true,"permalink":"/calculo-naut/apuntes/calc-naut-tema03/","updated":"2026-01-07T10:12:12.907+01:00"}
---

[[Calculo-Naut/calc-naut-indice\|volver al índice]]
# Tema 3: Cálculo Integral de Varias Variables
- [[Calculo-Naut/Apuntes/calc-naut-tema03#1. Integrales Dobles\|1. Integrales Dobles]]
- [[Calculo-Naut/Apuntes/calc-naut-tema03#2. Integrales Triples\|2. Integrales Triples]]
- [[Calculo-Naut/Apuntes/calc-naut-tema03#3. Cambio de Variables\|3. Cambio de Variables]]
- [[Calculo-Naut/Apuntes/calc-naut-tema03#Ejercicios\|Ejercicios]]


## 1. Integrales Dobles

**Idea:** De manera análoga a cómo en una variable sumamos una infinidad de rectángulos diminutos para calcular el área bajo una curva, en el cálculo de varias variables extendemos este concepto. Con las integrales dobles, sumamos una infinidad de prismas rectangulares infinitesimalmente delgados para determinar el volumen total que se encuentra bajo una superficie.
![[Pasted image 20251124121347.png\|600]]
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
    
- Sobre Regiones Generales: Si $W \subset \mathbb{R}^3$ se proyecta sobre una región $\Omega$ en el plano $XY$, y está limitada superior e inferiormente por $z=u_2(x,y)$ y $z=u_1(x,y)$:
    
    $$\iiint_W f(x,y,z) \, dV = \iint_{\Omega} \left( \int_{u_1(x,y)}^{u_2(x,y)} f(x,y,z) \, dz \right) dA$$
    - Otra forma de hacerlo consiste en  proyectar sobre el eje $z$, dando lugar a un intervalo $[a,b]$, y luego integrar la sección horizontal (rebanadas) $\Omega_z$ resultante para cada $z$:
    $$\iiint_W f(x,y,z) \, dV = \int_a^b \left( \iint_{\Omega(z)} f(x,y,z) \, dA \right) dz$$
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
[[Calculo-Naut/Apuntes/calc-naut-tema03-ej\|Enlace]].