# Sistema de Segundo Orden

Sistema cuya [[Función de Transferencia]] tiene dos polos. Es la dinámica más importante del diseño de control porque muchos sistemas reales se aproximan con ella.

$$G(s)=\frac{\omega_n^2}{s^2+2\zeta\omega_n s+\omega_n^2}$$

- $\omega_n$: **frecuencia natural** (rad/s)
- $\zeta$: **coeficiente de amortiguamiento**

## Polos
$$s_{1,2}=-\zeta\omega_n\pm\omega_n\sqrt{\zeta^2-1}$$

## Clasificación según $\zeta$
| $\zeta$ | Tipo | Polos |
|---------|------|-------|
| $\zeta=0$ | no amortiguado | imaginarios puros $\pm j\omega_n$ |
| $0<\zeta<1$ | subamortiguado | complejos conjugados |
| $\zeta=1$ | críticamente amortiguado | doble real |
| $\zeta>1$ | sobreamortiguado | reales distintos |

## Respuesta al escalón (subamortiguado)
$$y(t)=1-\frac{e^{-\zeta\omega_n t}}{\sqrt{1-\zeta^2}}\,\sin\!\left(\omega_d t+\phi\right),\qquad \omega_d=\omega_n\sqrt{1-\zeta^2},\quad \phi=\arctan\!\frac{\sqrt{1-\zeta^2}}{\zeta}$$

## Parámetros de diseño
- **Sobreimpulso máximo** (%):
$$\%M_p=e^{-\frac{\pi\zeta}{\sqrt{1-\zeta^2}}}\times100$$
- **Frecuencia amortiguada**: $\omega_d=\omega_n\sqrt{1-\zeta^2}$
- **Tiempo de pico**:
$$t_p=\frac{\pi}{\omega_d}$$
- **Tiempo de subida** (0→100 %): $t_r\approx\dfrac{\pi-\phi}{\omega_d}$
- **Tiempo de asentamiento** (2 %):
$$t_s\approx\frac{4}{\zeta\omega_n}$$

## Relación con el controlador
El [[Control PID]] modifica polos y ceros para mover $\zeta$ y $\omega_n$ hacia valores de diseño (ver [[Lugar Geométrico de las Raíces]]).

## Conceptos relacionados
- [[Función de Transferencia]]
- [[Respuesta Temporal]]
- [[Sistema de Primer Orden]]
- [[Estabilidad]]