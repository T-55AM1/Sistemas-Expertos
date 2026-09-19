# Respuesta Temporal

Evolución de la salida de un sistema en el tiempo ante una entrada (escalón, rampa, impulso). Se divide en **respuesta transitoria** y **respuesta en estado estacionario**.

$$y(t)=y_{TR}(t)+y_{SS}(t)$$

## Entradas de prueba
- **Escalón unitario**: $\mathcal{L}\{1\}=\dfrac{1}{s}$
- **Rampa**: $\mathcal{L}\{t\}=\dfrac{1}{s^2}$
- **Impulso**: $\mathcal{L}\{\delta(t)\}=1$

## Parámetros transitorios (escalón)
| Parámetro | Definición |
|-----------|------------|
| Sobreimpulso máximo $M_p$ | pico máximo por encima del valor final, en % |
| Tiempo de pico $t_p$ | tiempo hasta el primer pico |
| Tiempo de subida $t_r$ | tiempo de 10 % a 90 % (o 0 a 100 %) |
| Tiempo de asentamiento $t_s$ | tiempo para quedarse dentro de una banda (±2 % o ±5 %) |

Para un [[Sistema de Segundo Orden]] subamortiguado:
$$\%M_p=e^{-\frac{\pi\zeta}{\sqrt{1-\zeta^2}}}\times100,\qquad t_p=\frac{\pi}{\omega_d},\qquad t_s\approx\frac{4}{\zeta\omega_n}$$

## Error en estado estacionario
$$e_{ss}=\lim_{t\to\infty} e(t),\qquad E(s)=R(s)-C(s)$$

Mediante el teorema del valor final:
$$e_{ss}=\lim_{s\to0}s\,E(s)$$

Con realimentación unitaria $E(s)=\dfrac{R(s)}{1+G(s)}$:

| Tipo de sistema | Escalón $1/s$ | Rampa $1/s^2$ | Parábola $1/s^3$ |
|-----------------|------------|-------------|---------------|
| tipo 0 | $\dfrac{1}{1+K_p}$ | $\infty$ | $\infty$ |
| tipo 1 | $0$ | $\dfrac{1}{K_v}$ | $\infty$ |
| tipo 2 | $0$ | $0$ | $\dfrac{1}{K_a}$ |

Con las constantes de error estático:
$$K_p=\lim_{s\to0}G(s),\qquad K_v=\lim_{s\to0}s\,G(s),\qquad K_a=\lim_{s\to0}s^2G(s)$$

## Relación tiempo–frecuencia
- Mayor $\zeta\omega_n$ → respuesta más rápida
- Los polos dominantes gobiernan la respuesta transitoria
- En [[Diagramas de Bode]] se traza la misma información en el dominio frecuencial

## Conceptos relacionados
- [[Sistema de Primer Orden]]
- [[Sistema de Segundo Orden]]
- [[Estabilidad]]
- [[Control PID]]
- [[Función de Transferencia]]