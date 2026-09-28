---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema01/","created":"2026-09-28T10:34:31.283+02:00","updated":"2026-09-28T10:36:06.954+02:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|Volver al índice]]

# **TEMA 1: Números complejos**
Un número complejo es, esencialmente, un vector del plano. Esa es la razón de que sea el tema con el que se abre el curso: módulo y argumento son exactamente los dos datos que describen una dirección en el plano, y de ellos dependen tanto la trigonometría que usaremos en los temas siguientes como la interpretación de rumbos.

- [[01 Calculo-Naut/apuntes/calc-naut-tema01#1. El número complejo y sus operaciones\|1. El número complejo y sus operaciones]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema01#2. Forma polar de un complejo\|2. Forma polar de un complejo]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema01#3. Cómo calcular el argumento en 3 pasos\|3. Cómo calcular el argumento en 3 pasos]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema01#4. Ejemplos resueltos\|4. Ejemplos resueltos]]
- [[01 Calculo-Naut/apuntes/calc-naut-tema01#5. Operaciones en forma polar\|5. Operaciones en forma polar]]

## 1. El número complejo y sus operaciones
Un número complejo es de la forma
$$
z = a + bi, \quad a,b \in \mathbb{R}, \quad i^2 = -1.
$$

* Parte real: $\Re(z)=a$
* Parte imaginaria: $\Im(z)=b$

**Representación**: el plano complejo (plano de Argand), donde $a$ se ubica en el eje horizontal y $b$ en el vertical.

**Suma y resta**
$$
(a+bi) + (c+di) = (a+c) + (b+d)i.
$$
**Producto**
$$
(a+bi)(c+di) = (ac-bd) + (ad+bc)i.
$$

Se aplica distributiva y $i^2=-1$.

**Conjugado**
$$
\overline{z} = a - bi.
$$

**Propiedad importante:**
* $z \overline{z} = a^2+b^2 \in \mathbb{R}$

**División**. 
Se multiplica numerador y denominador por el conjugado del denominador:
$$
\frac{a+bi}{c+di} = \frac{(a+bi)(c-di)}{c^2+d^2}.
$$
Dicho de otra forma:
$\dfrac{1}{z} = \dfrac{\overline{z}}{|z|^2}$ (si $z\neq 0$)


**Potencias de números complejos.** 
Para exponentes pequeños se desarrolla con binomio o distributiva.
Ejemplo:
$$
(1+i)^2 = 2i, \qquad (1+i)^4 = -4.
$$
Pero, en general, no tiene sentido hacerlo así. Se usa la fórmula de De Moivre, una vez que entendamos la forma polar.

---

## 2. Forma polar de un complejo
Un número complejo $z=a+bi$ puede interpretarse como un vector, y por tanto podrá representarse como:
$$
z = r(\cos\theta + i \sin\theta),
$$
donde:
* $r=|z|=\sqrt{a^2+b^2}$ es el **módulo**, es decir, la **distancia** al origen.
* $\theta=\arg(z)$ es el **argumento**, es decir, el ángulo que forma el vector con el eje real, medido en sentido **antihorario**.

También se denotará por $z=re^{i\theta}$, o bien $r_{\theta}$.

> [!note] Requisito
> Se supone $z\neq 0$. Si $z=0$ no hay módulo que calcular más que $0$, y **el argumento no existe**: el origen no tiene dirección.

## 3. Cómo calcular el argumento en 3 pasos

El módulo sale directamente de $\sqrt{a^2+b^2}$. El argumento se calcula siempre con la **misma receta de 3 pasos**:

1. **Mira el signo de $a$** (la parte real). Si $a>0$, el vector está a la derecha del eje imaginario; si $a<0$, a la izquierda.
2. **Aplica el cociente** $\dfrac{b}{a}$ y la función $\arctan$:
$$
\theta=\begin{cases}
\arctan\left(\dfrac{b}{a}\right) & \text{si } a>0\\[8pt]
\arctan\left(\dfrac{b}{a}\right)+180^\circ & \text{si } a<0
\end{cases}
$$
3. **Si $a=0$**, no hay cociente que hacer, pero tampoco hay cálculo: $z$ está en el eje imaginario, así que
$$
\theta=\begin{cases}90^\circ & \text{si } b>0\\ 270^\circ & \text{si } b<0\end{cases}
$$

> [!tip] Ojo
> Algunas calculadoras científicas traen la función `atan2(b, a)`, que hace los tres pasos de golpe. Conviene saber usarla, pero saber *por qué* funciona es lo que evita los errores.

---

## 4. Ejemplos resueltos

**1º cuadrante.** $z=1+\sqrt3\,i$ → $a=1>0$, $b=\sqrt3>0$.
$$|z|=\sqrt{1+3}=2,\qquad \theta=\arctan\left(\tfrac{\sqrt3}{1}\right)=60^\circ=\tfrac{\pi}{3}$$
$$z=2e^{i\pi/3}=2\left(\tfrac12+\tfrac{\sqrt3}{2}i\right)=1+\sqrt3\,i \;\checkmark$$

**2º cuadrante.** $z=-\sqrt3+i$ → $a=-\sqrt3<0$, $b=1>0$.
$$|z|=\sqrt{3+1}=2,\qquad \theta=\arctan\left(\tfrac{1}{-\sqrt3}\right)+180^\circ=-30^\circ+180^\circ=150^\circ=\tfrac{5\pi}{6}$$
$$z=2e^{i5\pi/6}=2\left(-\tfrac{\sqrt3}{2}+\tfrac12 i\right)=-\sqrt3+i \;\checkmark$$

**3º cuadrante.** $z=-1-i$ → $a=-1<0$, $b=-1<0$.
$$|z|=\sqrt{1+1}=\sqrt2,\qquad \theta=\arctan\left(\tfrac{-1}{-1}\right)+180^\circ=45^\circ+180^\circ=225^\circ=\tfrac{5\pi}{4}$$
$$z=\sqrt2\,e^{i5\pi/4}=\sqrt2\left(-\tfrac{\sqrt2}{2}-\tfrac{\sqrt2}{2}i\right)=-1-i \;\checkmark$$

**4º cuadrante.** $z=\sqrt2-\sqrt2\,i$ → $a=\sqrt2>0$, $b=-\sqrt2<0$.
$$|z|=\sqrt{2+2}=2,\qquad \theta=\arctan\left(\tfrac{-\sqrt2}{\sqrt2}\right)=-45^\circ$$
Aquí aparece negativo:
$$\theta=-45^\circ+360^\circ=315^\circ=\tfrac{7\pi}{4},\qquad z=2e^{i7\pi/4}=\sqrt2-\sqrt2\,i \;\checkmark$$

**Eje imaginario.** $z=-7i$ → $a=0$, $b=-7<0$.
$$|z|=7,\qquad \theta=270^\circ=\tfrac{3\pi}{2}\;\checkmark$$


> [!warning] El argumento no es un rumbo
> Trabajaremos con $[0,360^\circ)$, que es lo natural en navegación. Pero ojo, los rumbos se miden **en sentido horario desde el Norte**. El argumento se mide **en sentido antihorario desde el Este**. Si un buque navega con rumbo $\beta$, el desplazamiento tiene argumento $\theta=90^\circ-\beta$.

## 5. Operaciones en forma polar

* Conjugado (con $-\theta$ entendido módulo $360^\circ$):
$$
\overline{z}=r(\cos(-\theta)+i\sin(-\theta))=re^{-i\theta}.
$$
* Producto:
$$
z_1 z_2 = r_1 r_2 \big(\cos(\theta_1+\theta_2)+i\sin(\theta_1+\theta_2)\big)=r_1r_2e^{i(\theta_1+\theta_2)}.
$$
* Cociente:
$$
\frac{z_1}{z_2} = \frac{r_1}{r_2} \big(\cos(\theta_1-\theta_2)+i\sin(\theta_1-\theta_2)\big).
$$
* Potencias (De Moivre):
$$
z^n = r^n (\cos(n\theta)+i\sin(n\theta)), \quad n\in\mathbb{Z}^+.
$$


[[01 Calculo-Naut/apuntes/calc-naut-tema01-ej\|Ejercicios]]
