# Respuesta en Frecuencia

Análisis del sistema ante entradas sinusoidales. Para un sistema LTI y estable, la salida en régimen permanente es una sinusoide de **igual frecuencia**, con **amplitud modificada** por la magnitud y **desplazada** por la fase.

$$y(t)=|G(j\omega)|\,\sin(\omega t+\angle G(j\omega))$$

## Respuesta en frecuencia
$$G(j\omega)=G(s)\big|_{s=j\omega}=|G(j\omega)|\,e^{j\angle G(j\omega)}$$

- **Magnitud**: $M(\omega)=|G(j\omega)|$ — ganancia a cada frecuencia
- **Fase**: $\phi(\omega)=\angle G(j\omega)$ — desfase introducido

## Propiedades clave
- Basta evaluar $G(j\omega)$ sobre el **eje imaginario**
- Se representa con [[Diagramas de Bode]] (separando magnitud y fase en dB y grados) o con el [[Criterio de Nyquist]] (diagrama polar)
- Fundamental para sistemas con polos/ceros complejos y retardos

## Frecuencias características
- **Frecuencia de resonancia** $\omega_r$: donde $|G(j\omega)|$ alcanza su máximo
- **Ancho de banda** $\omega_{BW}$: frecuencia donde $|G(j\omega)|$ cae a $-3$ dB respecto a su valor a baja frecuencia
- **Frecuencia de cruce de ganancia** $\omega_{gc}$: donde $|G(j\omega_{gc})|=1$
- **Frecuencia de cruce de fase** $\omega_{pc}$: donde $\angle G(j\omega_{pc})=-180^\circ$

## Caso particular: sistema de segundo orden
$$G(j\omega)=\frac{\omega_n^2}{(j\omega)^2+2\zeta\omega_n(j\omega)+\omega_n^2}$$

Pico de resonancia:
$$M_r=\frac{1}{2\zeta\sqrt{1-\zeta^2}},\qquad \omega_r=\omega_n\sqrt{1-2\zeta^2}\quad(\zeta<0.707)$$

## Relación con el tiempo
- Mayor ancho de banda → respuesta más rápida en [[Respuesta Temporal]]
- Margen de fase ↔ amortiguamiento de lazo cerrado: $\phi_m\approx 100\zeta$

## Diseño en frecuencia
Se especifican [[Márgenes de Ganancia y Fase]] para garantizar [[Estabilidad]] y robustez, y se ajustan compensadores modificando [[Diagramas de Bode]].

## Conceptos relacionados
- [[Diagramas de Bode]]
- [[Criterio de Nyquist]]
- [[Márgenes de Ganancia y Fase]]
- [[Estabilidad]]
- [[Función de Transferencia]]