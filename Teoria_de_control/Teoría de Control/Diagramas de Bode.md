# Diagramas de Bode

Representación de la [[Respuesta en Frecuencia]] de una [[Función de Transferencia]] como dos gráficas en función de $\omega$ (escala logarítmica):

1. **Magnitud**: $20\log_{10}|G(j\omega)|$ en **dB**
2. **Fase**: $\angle G(j\omega)$ en **grados**

La escala logarítmica convierte multiplicaciones en sumas, por lo que el diagrama de un producto es la suma de los diagramas de cada factor.

## Factores básicos
| Factor | Magnitud (asíntota) | Pendiente | Fase |
|--------|----------------------|-----------|------|
| $K$ | $20\log K$ | 0 | 0° |
| $\dfrac{1}{s}$ | $-20\log\omega$ | $-20$ dB/déc | $-90°$ |
| $s$ | $+20\log\omega$ | $+20$ dB/déc | $+90°$ |
| $\dfrac{1}{\tau s+1}$ | 0 → $-20$ dB/déc tras $\omega=1/\tau$ | $-20$ dB/déc | $0\to-90°$ |
| $\tau s+1$ | 0 → $+20$ dB/déc | $+20$ dB/déc | $0\to+90°$ |
| $\omega_n^2/(s^2+2\zeta\omega_n s+\omega_n^2)$ | 0 → $-40$ dB/déc tras $\omega_n$ | $-40$ dB/déc | $0\to-180°$ |

## Frecuencias de quiebre (corners)
- Polo real: $\omega=1/\tau$
- Par de polos complejos: $\omega=\omega_n$

## Ajuste por amortiguamiento
En $\omega=\omega_n$, la magnitud real del factor de segundo orden vale:
$$20\log_{10}\left(\frac{1}{2\zeta}\right)\ \text{dB}$$

- $\zeta$ pequeño → pico pronunciado (resonancia)
- Para $\zeta=0.5$: $+6$ dB; $\zeta=0.25$: $+12$ dB

## Caracterización del sistema
- **Cruce de ganancia** $\omega_{gc}$: $|G(j\omega)|=1$ (0 dB)
- **Cruce de fase** $\omega_{pc}$: $\angle G(j\omega)=-180°$
- De ellos se derivan los [[Márgenes de Ganancia y Fase]]
- Las asíntotas a baja frecuencia indican el **tipo de sistema** y el error en estado estacionario ([[Respuesta Temporal]])

## Diseño de compensadores
- **Avanse de fase** (lead): añade fase alrededor de $\omega_{gc}$, aumenta el margen de fase
- **Retraso de fase** (lag): reduce la ganancia a alta frecuencia, reduce el error de estado estacionario
- Se combinan con el método de ajuste del [[Control PID]]

## Conceptos relacionados
- [[Respuesta en Frecuencia]]
- [[Márgenes de Ganancia y Fase]]
- [[Criterio de Nyquist]]
- [[Estabilidad]]
- [[Función de Transferencia]]