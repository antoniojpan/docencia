---
{"dg-publish":true,"permalink":"/02-mat-cc-mar/apuntes/mat-ccmar-tema03-ej/","created":"2026-10-01T07:49:33.138+02:00","updated":"2026-10-01T10:44:42.134+02:00","dg-note-properties":{}}
---

[[02 Mat-CCMar/mat-ccmar-indice\|Volver al índice]]

# Hoja de Ejercicios Tema 3: Diagonalización

> [!question] Ejercicio 1
> Diagonaliza las siguientes matrices si es posible:
>
> **(A)** $A = \begin{pmatrix} 3 & 4 \\ 5 & 2 \end{pmatrix}$
>
> **(B)** $B = \begin{pmatrix} -2 & 2 & 0 \\ -6 & 5 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>
> **(C)** $C = \begin{pmatrix} 1 & 0 & 0 \\ 1 & -1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$
>
> **(K)** $K = \begin{pmatrix} 3 & -3 & 4 \\ -3 & 3 & 4 \\ -2 & -2 & 0 \end{pmatrix}$
>
> **(E)** $E = \begin{pmatrix} 1 & 1 & 0 & 0 \\ 1 & 1 & 0 & 0 \\ 0 & 0 & -1 & -1 \\ 0 & 0 & -1 & -1 \end{pmatrix}$
>
> **(F)** $F = \begin{pmatrix} 0 & 2 \\ 0 & 0 \end{pmatrix}$
>
> **(G)** $G = \begin{pmatrix} 2 & -1 & -1 \\ 4 & 3 & -4 \\ -3 & -1 & 4 \end{pmatrix}$
>
> **(H)** $H = \begin{pmatrix} -2 & -2 & -1 \\ -2 & 1 & 2 \\ 1 & -2 & -4 \end{pmatrix}$
>
> **(I)** $I = \begin{pmatrix} -1 & 0 & -1 \\ 0 & 0 & 0 \\ 1 & 0 & 1 \end{pmatrix}$
>
> **(J)** $J = \begin{pmatrix} 5 & 0 & 0 & 0 \\ 0 & 3 & 0 & 0 \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 0 & 5 \end{pmatrix}$

> [!question] Ejercicio 2
> Para las matrices del ejercicio anterior, calcula las siguientes potencias:
>
> $A^5, \quad B^9, \quad C^{21}, \quad K^2, \quad E^{15}, \quad F^{88}, \quad G^5, \quad H^4, \quad I^{47}, \quad J^6$

---

# Soluciones

> [!success] Solución del Ejercicio 1
> **(A)** $D = \begin{pmatrix} 7 & 0 \\ 0 & -2 \end{pmatrix}, \quad P = \begin{pmatrix} 1 & -4 \\ 1 & 5 \end{pmatrix}$
>
> **(B)** $D = \begin{pmatrix} 2 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \quad P = \begin{pmatrix} 1 & 2 & 0 \\ 2 & 3 & 0 \\ 0 & 0 & 1 \end{pmatrix}$
>
> **(C)** $D = \begin{pmatrix} -1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad P = \begin{pmatrix} 0 & -1 & 2 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix}$
>
> **(K)** **No es diagonalizable** (faltan autovalores).
>
> **(E)** $D = \begin{pmatrix} -2 & 0 & 0 & 0 \\ 0 & 2 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \quad P = \begin{pmatrix} 0 & 1 & 0 & -1 \\ 0 & 1 & 0 & 1 \\ 1 & 0 & -1 & 0 \\ 1 & 0 & 1 & 0 \end{pmatrix}$
>
> **(F)** **No es diagonalizable** (faltan autovectores).
>
> **(G)** $D = \begin{pmatrix} 5 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad P = \begin{pmatrix} 1 & 1 & 1 \\ -8 & -2 & 0 \\ 5 & 1 & 1 \end{pmatrix}$
>
> **(H)** $D = \begin{pmatrix} -3 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \quad P = \begin{pmatrix} 1 & 2 & 1 \\ 0 & 1 & -2 \\ 1 & 0 & 1 \end{pmatrix}$
>
> **(I)** **No es diagonalizable** (faltan autovectores).
>
> **(J)** $D = \begin{pmatrix} 5 & 0 & 0 & 0 \\ 0 & 3 & 0 & 0 \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 0 & 5 \end{pmatrix}, \quad P = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$

> [!success] Solución del Ejercicio 2
> - $A^5 = \begin{pmatrix} 9323 & 7484 \\ 9355 & 7452 \end{pmatrix}$
>
> - $B^9 = \begin{pmatrix} -1532 & 1022 & 0 \\ -3066 & 2045 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>
> - $C^{21} = \begin{pmatrix} 1 & 0 & 0 \\ 1 & -1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$
>
> - $K^2 = \begin{pmatrix} 10 & -26 & 0 \\ -26 & 10 & 0 \\ 0 & 0 & -16 \end{pmatrix}$
>
> - $E^{15} = \begin{pmatrix} 16384 & 16384 & 0 & 0 \\ 16384 & 16384 & 0 & 0 \\ 0 & 0 & -16384 & -16384 \\ 0 & 0 & -16384 & -16384 \end{pmatrix}$
>
> - $F^{88} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$
>
> - $G^5 = \begin{pmatrix} -538 & -121 & 539 \\ 5764 & 243 & -5764 \\ -3663 & -121 & 3664 \end{pmatrix}$
>
> - $H^4 = \begin{pmatrix} 61 & 40 & 40 \\ 20 & 1 & -40 \\ -20 & 40 & 101 \end{pmatrix}$
>
> - $I^{47} = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
>
> - $J^6 = \begin{pmatrix} 15625 & 0 & 0 & 0 \\ 0 & 729 & 0 & 0 \\ 0 & 0 & 64 & 0 \\ 0 & 0 & 0 & 15625 \end{pmatrix}$