---
{"dg-publish":true,"permalink":"/01-calculo-naut/apuntes/calc-naut-tema04-ej/","created":"2026-11-23T11:36:33.500+01:00","updated":"2026-11-23T11:36:23.637+01:00","dg-note-properties":{}}
---

[[01 Calculo-Naut/calc-naut-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 4: Cálculo Integral de Varias Variables


> [!question] Ejercicio 1
> Dibuja la región de integración y calcula $\iint_{\Omega}f$ en los siguientes casos:
>
> **(a)** $f(x,y)=x\sin y-y e^{x}$ en $\Omega=[-1,1]\times[0,\pi/2]$.
>
> **(b)** $f(x,y)=x^{2}-y$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[-1,1],\ -x^{2}\leq y\leq x^{2}\}$.
>
> **(c)** $f(x,y)=xy-x^{3}$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[0,1],\ -1\leq y\leq x\}$.
>
> **(d)** $f(x,y)=2x\sin(x^{2}y)$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:x\in[0,2],\ |y|\leq x\}$.
>
> **(e)** $f(x,y)=y\sin x$ en $\Omega=\{(x,y)\in\mathbb{R}^{2}:|x|+|y|\leq1\}$.

> [!question] Ejercicio 2
> Sobre el recinto $\Omega=\{(x,y)\in\mathbb{R}^{2}:x^{2}+(y-1)^{2}\leq1,\ x\geq0\}$ se consideran las funciones
> $$f(x,y)=\frac{1}{\sqrt{1-x^{2}}}\qquad\text{y}\qquad g(x,y)=\sin(y-1).$$
> Aplica el teorema de Fubini a $\iint_{\Omega}f$ y $\iint_{\Omega}g$ en las dos ordenaciones posibles. Calcula las integrales en el orden más adecuado.

> [!question] Ejercicio 3
> Determina el recinto de integración y cambia el orden de integración en las siguientes integrales:
>
> **(a)** $\displaystyle\int_{0}^{3}\int_{4x/3}^{\sqrt{25-x^{2}}}f(x,y)\,dy\,dx$
>
> **(b)** $\displaystyle\int_{0}^{1}\int_{0}^{y}f(x,y)\,dx\,dy$
>
> **(c)** $\displaystyle\int_{0}^{\pi/2}\int_{-\sin(x/2)}^{\sin(x/2)}f(x,y)\,dy\,dx$
>
> **(d)** $\displaystyle\int_{0}^{e}\int_{0}^{\log x}f(x,y)\,dy\,dx$

> [!question] Ejercicio 4
> Halla el valor de la siguiente integral (requiere cambiar el orden de integración):
> $$\int_{0}^{\pi}\int_{x}^{\pi}\frac{\sin y}{y}\,dy\,dx.$$

> [!question] Ejercicio 5
> Calcula el área limitada por las curvas $y=x$ e $y=2-x^{2}$.

> [!question] Ejercicio 6
> Sea $S$ una región del plano limitada por las curvas que se indican. Calcula la masa y el centro de gravedad de $S$ suponiendo que la densidad es constante e igual a $\rho$.
>
> **(a)** $y=x^{2}$, $x+y=2$.
>
> **(b)** $y+3=x^{2}$, $x^{2}=5-y$.
>
> **(c)** $y=\sin^{2}x$, $y=0$, $x\in[0,\pi]$.
>
> **(d)** $y=\sin x$, $y=\cos x$, $x\in[0,\pi/4]$.

> [!question] Ejercicio 7
> Determina las coordenadas del centro de gravedad de la placa
> $$B=\{(x,y)\in\mathbb{R}^{2}:1\leq x\leq2,\ 1\leq y\leq3\}$$
> cuya densidad viene dada por la función $\sigma(x,y)=xy$.

> [!question] Ejercicio 8
> Una placa metálica viene representada por el conjunto del plano
> $$P=\{(x,y)\in\mathbb{R}^{2}:|y|\leq1\}$$
> y su densidad es $\sigma(x,y)=y^{2}$. Calcula el centro de gravedad y los momentos de inercia con respecto a los ejes.

## 2. Integrales triples

> [!question] Ejercicio 9
> Calcula las siguientes integrales en los recintos que se indican:
>
> **(a)** $\displaystyle\iiint_{\Omega}(x^{2}+y^{2}+z^{2})\,dx\,dy\,dz$, donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
>
> **(b)** $\displaystyle\iiint_{\Omega}x^{3}\,dx\,dy\,dz$, donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
>
> **(c)** $\displaystyle\iiint_{\Omega}y e^{-xy}\,dx\,dy\,dz$, donde $\Omega=[0,1]\times[0,1]\times[0,1]$.
>
> **(d)** $\displaystyle\iiint_{\Omega}(2x+3y+z)\,dx\,dy\,dz$, donde $\Omega=[1,2]\times[-1,1]\times[0,1]$.
>
> **(e)** $\displaystyle\iiint_{\Omega}z e^{x+y}\,dx\,dy\,dz$, donde $\Omega=[0,1]\times[0,1]\times[0,1]$.

> [!question] Ejercicio 10
> Calcula la integral $\iiint_{\Omega}x^{2}\cos x\,dx\,dy\,dz$, donde $\Omega$ es la región limitada por los planos
> $$z=0,\qquad z=\pi,\qquad y=0,\qquad x=0,\qquad x+y=1.$$
> Dibuja la región de integración.

> [!question] Ejercicio 11
> Calcula los siguientes volúmenes:
>
> **(a)** Volumen de la región limitada por $x^{2}+y^{2}\leq4$ y $x^{2}+y^{2}+z^{2}\leq16$.
>
> **(b)** Volumen del sólido limitado por los conos $z=1-\sqrt{x^{2}+y^{2}}$ y $z=-1+\sqrt{x^{2}+y^{2}}$.
>
> **(c)** Volumen de la región limitada por el paraboloide $z=x^{2}+y^{2}$ y por $x^{2}+y^{2}=4$ en $z\geq0$.
>
> **(d)** Volumen de la región limitada por $x^{2}+y^{2}+z^{2}<2$, $x^{2}+y^{2}\leq z$ y $z<6/5$.

## 3. Cambios de variable

> [!question] Ejercicio 12
> Calcula, usando coordenadas polares, la integral de la función $f(x,y)=\sqrt{x^{2}+y^{2}}$ sobre la región
> $$\Omega=\{(x,y)\in\mathbb{R}^{2}:x^{2}+y^{2}\leq1\}.$$

> [!question] Ejercicio 13
> Evalúa, usando coordenadas polares, la integral doble
> $$\iint_{\Omega}(x^{2}+y^{2})\,dx\,dy,$$
> donde $\Omega$ es la mitad superior del disco de radio $2$, definida por $x^{2}+y^{2}\leq4$ e $y\geq0$.

> [!question] Ejercicio 14
> Calcula, usando coordenadas polares, la integral de la función exponencial sobre la región anular comprendida entre los círculos de radios $1$ y $3$:
> $$\iint_{\Omega}e^{-(x^{2}+y^{2})}\,dx\,dy,\qquad \Omega=\{(x,y)\in\mathbb{R}^{2}:1\leq x^{2}+y^{2}\leq9\}.$$

> [!question] Ejercicio 15
> Calcula las siguientes integrales usando coordenadas cilíndricas $(r,\theta,z)$, definidas por $x=r\cos\theta$, $y=r\sin\theta$:
>
> **(a)** $\displaystyle\iiint_{\Omega}(x^{2}+y^{2})\,dV$, donde $\Omega=\{(x,y,z)\in\mathbb{R}^{3}:x^{2}+y^{2}\leq4,\ 0\leq z\leq3\}$.
>
> **(b)** $\displaystyle\iiint_{\Omega}z\sqrt{x^{2}+y^{2}}\,dV$, donde $\Omega$ es el sólido interior al cilindro $x^{2}+y^{2}\leq1$ y comprendido entre $z=0$ y $z=1-x^{2}-y^{2}$.
>
> **(c)** $\displaystyle\iiint_{\Omega}e^{x^{2}+y^{2}}\,dV$, donde $\Omega$ es el sólido limitado por el cono $z=\sqrt{x^{2}+y^{2}}$ y el plano $z=2$.

> [!question] Ejercicio 16
> Determina, mediante coordenadas cilíndricas, los volúmenes de los siguientes sólidos:
>
> **(a)** El sólido limitado por el paraboloide $z=x^{2}+y^{2}$ y el plano $z=4$.
>
> **(b)** El sólido limitado por el cono $z=\sqrt{x^{2}+y^{2}}$ y el paraboloide $z=2-x^{2}-y^{2}$.
>
> **(c)** El sólido interior al cilindro $x^{2}+y^{2}\leq2x$ y comprendido entre $z=0$ y $z=\sqrt{x^{2}+y^{2}}$.

> [!question] Ejercicio 17
> Calcula las siguientes integrales usando coordenadas esféricas $(\rho,\theta,\phi)$, definidas por $x=\rho\sin\phi\cos\theta$, $y=\rho\sin\phi\sin\theta$, $z=\rho\cos\phi$:
>
> **(a)** $\displaystyle\iiint_{\Omega}(x^{2}+y^{2}+z^{2})\,dV$, donde $\Omega=\{(x,y,z)\in\mathbb{R}^{3}:x^{2}+y^{2}+z^{2}\leq4\}$.
>
> **(b)** $\displaystyle\iiint_{\Omega}z\,dV$, donde $\Omega$ es la mitad superior de la bola unidad, es decir, $x^{2}+y^{2}+z^{2}\leq1$ y $z\geq0$.
>
> **(c)** $\displaystyle\iiint_{\Omega}\frac{1}{\sqrt{x^{2}+y^{2}+z^{2}}}\,dV$, donde $\Omega=\{(x,y,z)\in\mathbb{R}^{3}:1\leq x^{2}+y^{2}+z^{2}\leq4\}$.

> [!question] Ejercicio 18
> Resuelve los siguientes problemas mediante coordenadas esféricas:
>
> **(a)** Calcula el volumen de la región interior a la esfera $x^{2}+y^{2}+z^{2}\leq16$ y situada sobre el cono $z=\sqrt{x^{2}+y^{2}}$.
>
> **(b)** Calcula el volumen de la región interior a la esfera $x^{2}+y^{2}+z^{2}=2z$ y situada por encima del plano $z=1$.
>
> **(c)** Calcula la masa de una bola de radio $R$ cuya densidad es $\delta(x,y,z)=k(1+x^{2}+y^{2}+z^{2})$, con $k>0$.

---

# Soluciones

> [!success] Solución del Ejercicio 1
> **(a)** $\displaystyle-\frac{\pi^{2}}{8}\left(e-e^{-1}\right)$
>
> **(b)** $\displaystyle\frac{4}{5}$
>
> **(c)** $\displaystyle-\frac{23}{40}$
>
> **(d)** $0$
>
> **(e)** $0$

> [!success] Solución del Ejercicio 2
> En las dos ordenaciones posibles:
> $$\iint_{\Omega}f=\int_{0}^{1}\int_{1-\sqrt{1-x^{2}}}^{1+\sqrt{1-x^{2}}}\frac{dy\,dx}{\sqrt{1-x^{2}}}=\int_{0}^{2}\int_{0}^{\sqrt{2y-y^{2}}}\frac{dx\,dy}{\sqrt{1-x^{2}}}=2,$$
> $$\iint_{\Omega}g=\int_{0}^{1}\int_{1-\sqrt{1-x^{2}}}^{1+\sqrt{1-x^{2}}}\sin(y-1)\,dy\,dx=\int_{0}^{2}\int_{0}^{\sqrt{2y-y^{2}}}\sin(y-1)\,dx\,dy=0.$$

> [!success] Solución del Ejercicio 3
> **(a)** $\Omega=\{0\leq y\leq4,\ 0\leq x\leq3y/4\}\cup\{4\leq y\leq5,\ 0\leq x\leq\sqrt{25-y^{2}}\}$;
> $$\int_{0}^{4}\int_{0}^{3y/4}f(x,y)\,dx\,dy+\int_{4}^{5}\int_{0}^{\sqrt{25-y^{2}}}f(x,y)\,dx\,dy.$$
>
> **(b)** $\Omega=\{0\leq x\leq1,\ x\leq y\leq1\}$;
> $$\int_{0}^{1}\int_{x}^{1}f(x,y)\,dy\,dx.$$
>
> **(c)** $\Omega=\{0\leq x\leq\pi/2,\ |y|\leq\sin(x/2)\}$;
> $$\int_{-\sqrt{2}/2}^{0}\int_{-2\arcsin y}^{\pi/2}f(x,y)\,dx\,dy+\int_{0}^{\sqrt{2}/2}\int_{2\arcsin y}^{\pi/2}f(x,y)\,dx\,dy.$$
>
> **(d)** El recinto con $0<x<1$ tiene orientación negativa; la integral con el orden cambiado es
> $$-\int_{-\infty}^{0}\int_{0}^{e^{y}}f(x,y)\,dx\,dy+\int_{0}^{1}\int_{e^{y}}^{e}f(x,y)\,dx\,dy.$$

> [!success] Solución del Ejercicio 4
> $2$

> [!success] Solución del Ejercicio 5
> $\displaystyle A=\frac{9}{2}$

> [!success] Solución del Ejercicio 6
> **(a)** $m=\displaystyle\frac{9\rho}{2}$, $(\bar x,\bar y)=\displaystyle\left(-\frac{1}{2},\frac{8}{5}\right)$.
>
> **(b)** $m=\displaystyle\frac{64\rho}{3}$, $(\bar x,\bar y)=(0,1)$.
>
> **(c)** $m=\displaystyle\frac{\pi\rho}{2}$, $(\bar x,\bar y)=\displaystyle\left(\frac{\pi}{2},\frac{3}{8}\right)$.
>
> **(d)** $m=\rho(\sqrt{2}-1)$, $(\bar x,\bar y)=\displaystyle\left(\frac{\frac{\pi\sqrt{2}}{4}-1}{\sqrt{2}-1},\frac{\sqrt{2}+1}{4}\right)$.

> [!success] Solución del Ejercicio 7
> $(\bar x,\bar y)=\displaystyle\left(\frac{14}{9},\frac{13}{6}\right)$.

> [!success] Solución del Ejercicio 8
> Con el recinto tal como está definido, la masa es infinita; el centro de gravedad no está definido y los momentos de inercia respecto de ambos ejes son infinitos.

> [!success] Solución del Ejercicio 9
> **(a)** $1$
>
> **(b)** $\displaystyle\frac14$
>
> **(c)** $\displaystyle e^{-1}$
>
> **(d)** $7$
>
> **(e)** $\displaystyle\frac{(e-1)^{2}}{2}$

> [!success] Solución del Ejercicio 10
> $\pi\left(4\sin1+5\cos1-6\right)$

> [!success] Solución del Ejercicio 11
> **(a)** $\displaystyle V=\frac{32\pi}{3}(8-3\sqrt{3})$
>
> **(b)** $\displaystyle V=\frac{2\pi}{3}$
>
> **(c)** $V=8\pi$
>
> **(d)** $\displaystyle V=\frac{493\pi}{750}$

> [!success] Solución del Ejercicio 12
> $\displaystyle\frac{2\pi}{3}$

> [!success] Solución del Ejercicio 13
> $4\pi$

> [!success] Solución del Ejercicio 14
> $\pi\left(e^{-1}-e^{-9}\right)$

> [!success] Solución del Ejercicio 15
> **(a)** $24\pi$
>
> **(b)** $\displaystyle\frac{8\pi}{105}$
>
> **(c)** $\displaystyle\pi\left(\frac{\sqrt{\pi}}{2}\operatorname{erfi}(2)-2\right)$

> [!success] Solución del Ejercicio 16
> **(a)** $V=8\pi$
>
> **(b)** $\displaystyle V=\frac{5\pi}{6}$
>
> **(c)** $\displaystyle V=\frac{32}{9}$

> [!success] Solución del Ejercicio 17
> **(a)** $\displaystyle\frac{128\pi}{5}$
>
> **(b)** $\displaystyle\frac{\pi}{4}$
>
> **(c)** $6\pi$

> [!success] Solución del Ejercicio 18
> **(a)** $\displaystyle V=\frac{64\pi}{3}(2-\sqrt{2})$
>
> **(b)** $\displaystyle V=\frac{2\pi}{3}$
>
> **(c)** $\displaystyle m=\frac{4\pi kR^{3}}{15}(5+3R^{2})$
