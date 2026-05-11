---
{"dg-publish":true,"permalink":"/04-mat-ii-qui/apuntes/matii-quim-tema04-ej/","created":"2026-03-05T08:33:36.717+01:00","updated":"2026-05-11T11:56:19.714+02:00"}
---

[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].
# Tema 4: Métodos de integración numérica — Ejercicios aplicables

## Ejercicio 1
Sea $f(x) = 5^x$, calcular $\int_0^1 f(x)\,dx$ utilizando la **regla del trapecio** y comparar con el resultado exacto.

## Ejercicio 2
Aproximar $\int_1^2 \ln x\,dx = 0.3862943\ldots$ utilizando:
- (a) Las reglas del **punto medio**, del **trapecio** y de **Simpson**.
- (b) La **regla compuesta del punto medio** con $n = 4$.
- (c) La **regla compuesta del trapecio** con $n = 4$.
- (d) La **regla compuesta de Simpson** con $n = 4$.
- (e) Comparar en cada apartado la aproximación con la solución exacta.

## Ejercicio 3
Sea $f(x) = \dfrac{1}{1+x}$.
- (a) Aproximar $\int_0^4 f(x)\,dx$ usando la **regla compuesta del trapecio** con $n = 4$ (nodos uniformemente espaciados). Comparar con la solución exacta.
- (b) Aproximar $\int_0^4 f(x)\,dx$ usando la **regla compuesta del punto medio** con $n = 4$ (nodos uniformemente espaciados). Comparar con la solución exacta.
- (c) Calcular el número de nodos necesarios en ambos casos para que el error sea menor que $0.001$.

## Ejercicio 4
Aproximar $I = \int_1^2 \dfrac{1}{\sin x}\,dx$.
- (a) Primera aproximación mediante la **regla de Simpson**.
- (b) Aproximación mediante la **fórmula compuesta de Simpson** con $n = 5$.

## Ejercicio 5
Aproximar $I = \int_1^2 x\ln x\,dx$ mediante la **regla del trapecio compuesta** con $h = \tfrac{1}{8}$. Calcular la cota del error.

## Ejercicio 6
Dada $\int_0^1 e^{-x}\,dx$:
- (a) Aproximar mediante las reglas del **punto medio**, del **trapecio** y de **Simpson**.
- (b) Utilizar la **regla compuesta de Simpson** con $h = \tfrac{1}{4}$.
- (c) Comparar con el resultado exacto.

## Ejercicio 7
Aproximar $I = \int_1^3 (e^x + 1)\,dx$.
- (a) Aproximación mediante la **regla de Simpson**. Comparar con el valor exacto.
- (b) Aproximación mediante el **método del punto medio**.
- (c) Calcular la cota del error en ambos métodos.

## Ejercicio 8
Aproximar $I = \int_1^2 \ln x\,dx$ con $n = 4$, usando los métodos del **trapecio compuesto** y de **Simpson compuesto**. Comparar con la solución exacta.

## Ejercicio 9
Aproximar $\int_1^2 \dfrac{x^2}{1+\sqrt{x}}\,dx$ usando el **método del trapecio** y el del **punto medio**.

## Ejercicio 10
Aproximar $\int_{-1}^{1} \dfrac{1}{\sqrt{2\pi}}\,e^{-x^2/2}\,dx$ utilizando siete nodos con el **método del punto medio**, del **trapecio** y de **Simpson compuesto**.

## Ejercicio 11

Evaluar con el método del punto medio compuesto la integral de los siguientes datos:

| **x** | **0** | **0.1** | **0.2** | **0.3** | **0.4** | **0.5** | **0.6** |
| ----- | ----- | ------- | ------- | ------- | ------- | ------- | ------- |
| f(x)  | 1     | 7       | 4       | 3       | 5       | 2       | 1       |
|       |       |         |         |         |         |         |         |

### **Ejercicio 12**

Evaluar la siguiente integral utilizando el método del punto medio compuesto con h=0.3:
$$
\int_{0}^{3}\frac{e^{x}sen~x}{1+x^{2}}dx.
$$
## Ejercicio 13
Evaluar $\int_{-3}^{3} \ln(4x^2+4)\,dx$ utilizando el **método del punto medio compuesto** con siete nodos. Calcular la cota del error.

## Ejercicio 14
Aproximar mediante los métodos del **punto medio**, del **trapecio** y de **Simpson** la integral $\int_{-1}^{1} e^{-x^2}\,dx$.

## Ejercicio 15
Aproximar la integral del ejercicio anterior con las **reglas compuestas** con cinco nodos. Calcular el número de pasos necesarios para que el error sea menor que $0.01$ en la **regla de Simpson compuesta**.


[[04 MatII-Qui/Matemáticas II- Química- Índice\|Volver al temario]].