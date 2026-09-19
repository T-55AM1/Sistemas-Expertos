# Sistema de Primer Orden

Sistema cuya [[Función de Transferencia]] tiene un único polo real.

$$G(s)=\frac{K}{\tau s+1}$$

- $K$: ganancia estática
- $\tau$: **constante de tiempo** (s)

## Polo
$$s=-\frac{1}{\tau}$$

## Respuesta al escalón
$$y(t)=K\left(1-e^{-t/\tau}\right),\quad t\ge0$$

## Parámetros característicos (escalón unitario)
| Magnitud | Valor |
|----------|-------|
| Valor final | $K$ |
| $63.2\,\%$ | $t=\tau$ |
| Tiempo de subida (0→90 %) | $t_r\approx 2.2\,\tau$ |
| Tiempo de asentamiento (2 %) | $t_s=4\tau$ |
| Pendiente inicial | $\dfrac{K}{\tau}$ |

- **No presenta sobreimpulso**: es monótona creciente.
- Forma canónica alternativa: $G(s)=\dfrac{1}{Ts+1}$ con polo en $-1/T$.

## Integrador
Caso límite con polo en el origen:
$$G(s)=\frac{K}{s}\;\Rightarrow\; y(t)=K\,t$$

## Ejemplo físico
Circuito RC: $G(s)=\dfrac{1}{RC\,s+1}$, torque en motor, temperatura de un horno, etc.

## Conceptos relacionados
- [[Función de Transferencia]]
- [[Respuesta Temporal]]
- [[Sistema de Segundo Orden]]
- [[Estabilidad]]