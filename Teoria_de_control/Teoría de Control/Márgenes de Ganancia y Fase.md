# Márgenes de Ganancia y Fase

Cuantifican **cuánto puede variar la ganancia o la fase** de lazo abierto antes de que el sistema se vuelva inestable (es decir, antes de que el trazado alcance el punto crítico $(-1, j0)$). Se leen de los [[Diagramas de Bode]] o del [[Criterio de Nyquist|trazado de Nyquist]].

## Definiciones (lazo abierto $G(j\omega)$)
- **Frecuencia de cruce de ganancia** $\omega_{gc}$: donde $|G(j\omega_{gc})|=1$ (0 dB)
- **Frecuencia de cruce de fase** $\omega_{pc}$: donde $\angle G(j\omega_{pc})=-180°$

### Margen de fase (MF)
Cuánta fase adicional (negativa) permite el sistema hasta perder estabilidad:
$$\phi_m=180°+\angle G(j\omega_{gc})$$

Interpretación: el desfase máximo admisible en $\omega_{gc}$ antes de que la fase llegue a $-180°$.

### Margen de ganancia (MG)
Cuánto se puede **aumentar** la ganancia antes de la inestabilidad:
$$GM=-\;20\log_{10}|G(j\omega_{pc})|\ \text{dB}$$

Equivalente: $GM=20\log_{10}\left(\dfrac{1}{|G(j\omega_{pc})|}\right)$. Si el cruce de fase no existe, $GM=\infty$.

## Criterios de diseño típicos
| Magnitud | Valor recomendado |
|----------|-------------------|
| Margen de fase | $30°$ – $60°$ |
| Margen de ganancia | $\ge 6$ dB |

## Reglas para la estabilidad relativa
- $MF>0$ y $GM>0$ → zona de estabilidad razonable
- El sistema es estable ⇒ $|G(j\omega_{pc})|<1$ (GM positivo) y fase en $\omega_{gc} > -180°$ (MF positivo)

## Relación MF–amortiguamiento
Para sistemas de segundo orden dominantes:
$$\phi_m\approx 100\,\zeta \quad\text{(MF en grados)}$$

Así, $MF=45°$ ≈ $\zeta=0.45$ (≈ 20 % de sobreimpulso en [[Respuesta Temporal]]).

## Uso en diseño
- Un **compensador de avance** aumenta $\phi_m$
- Un **compensador de retardo** reduce el error de estado estacionario manteniendo $MF$
- Se refinan con la sintonización del [[Control PID]]
- Margen suficiente ⇒ robustez frente a retardos y variaciones de parámetros

## Conceptos relacionados
- [[Diagramas de Bode]]
- [[Respuesta en Frecuencia]]
- [[Criterio de Nyquist]]
- [[Estabilidad]]
- [[Control PID]]