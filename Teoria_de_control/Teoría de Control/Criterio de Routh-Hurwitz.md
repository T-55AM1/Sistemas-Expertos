# Criterio de Routh-Hurwitz

Método algebraico que determina si un sistema es [[Estabilidad|estable]] **sin calcular las raíces** del polinomio característico. Se basa en la **tabla de Routh**.

## Polinomio característico
$$D(s)=a_n s^n+a_{n-1}s^{n-1}+\cdots+a_1 s+a_0$$

**Condición necesaria (pero no suficiente):** todos los coeficientes deben ser positivos y existir.

## Construcción de la tabla de Routh

| $s^n$ | $a_n$ | $a_{n-2}$ | $a_{n-4}$ | … |
|-------|-------|-----------|-----------|---|
| $s^{n-1}$ | $a_{n-1}$ | $a_{n-3}$ | $a_{n-5}$ | … |
| $s^{n-2}$ | $b_1$ | $b_2$ | $b_3$ | … |
| $s^{n-3}$ | $c_1$ | $c_2$ | … | … |
| ⋮ | | | | |
| $s^0$ | $a_0$ | | | |

Coeficientes $b_i$ y $c_i$:
$$b_1=\frac{a_{n-1}a_{n-2}-a_n a_{n-3}}{a_{n-1}},\qquad b_2=\frac{a_{n-1}a_{n-4}-a_n a_{n-5}}{a_{n-1}}$$
$$c_1=\frac{b_1 a_{n-3}-a_{n-1}b_2}{b_1},\qquad\cdots$$

## Criterio
- El sistema es **estable** si **todos los elementos de la primera columna** son positivos (sin cambio de signo).
- Cada **cambio de signo** en la primera columna indica **un polo en el semiplano derecho** (SPD).

## Casos especiales
1. **Cero en la primera columna** (con el resto de la fila no nulo):
   - Sustituir el cero por $\epsilon>0$ y continuar; el signo final se analiza cuando $\epsilon\to0$.
2. **Fila completa de ceros**:
   - Hay raíces simétricas (raíces imaginarias puras o recíprocas).
   - Usar los coeficientes de la fila anterior como **polinomio auxiliar** $A(s)$:
   $$A(s)=\mathrm{coeficientes\ de\ la\ fila\ s^{2k}}$$
   - Derivar $A'(s)$ y usar sus coeficientes en la fila de ceros.
   - Las raíces de $A(s)=0$ son los polos marginalmente estables.

## Uso con ganancia desconocida
Permite hallar el **rango de $K$** para la estabilidad de $1+G(s)H(s)=0$:
- Escribir el polinomio con $K$
- Aplicar Routh y exigir primera columna positiva
- El cruce por cero define el valor crítico de $K$ (junto al [[Lugar Geométrico de las Raíces]] en $j\omega$)

## Ejemplo
$$D(s)=s^3+4s^2+5s+K$$

| $s^3$ | $1$ | $5$ |
|-------|-----|-----|
| $s^2$ | $4$ | $K$ |
| $s^1$ | $\dfrac{20-K}{4}$ | $0$ |
| $s^0$ | $K$ | |

Estable si $K>0$ y $20-K>0$ → $0<K<20$. ¿Coincide con el cruce del [[Criterio de Nyquist]]? Sí: el límite es la oscilación marginal.

## Conceptos relacionados
- [[Estabilidad]]
- [[Función de Transferencia]]
- [[Lugar Geométrico de las Raíces]]
- [[Criterio de Nyquist]]