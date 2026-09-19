# Control PID

El **controlador PID** (Proporcional–Integral–Derivativo) genera la señal de control a partir del error $e(t)=r(t)-y(t)$, combinando tres acciones.

$$u(t)=K_p\,e(t)+K_i\int_0^t e(\tau)\,d\tau+K_d\,\frac{de(t)}{dt}$$

## Función de transferencia del controlador
$$C(s)=K_p+\frac{K_i}{s}+K_d\,s=K_p\left(1+\frac{1}{T_i s}+T_d s\right)$$

- $K_p$: ganancia proporcional
- $T_i=\dfrac{K_p}{K_i}$: tiempo integral
- $T_d=\dfrac{K_d}{K_p}$: tiempo derivativo

## Acciones individuales
| Acción | Expresión | Efecto |
|--------|-----------|--------|
| **P** | $K_p\,e(t)$ | Reduce el error, pero deja **error en estado estacionario** (aumenta $K_p$ lo reduce) |
| **I** | $K_i\int e\,dt$ | Elimina el error en estado estacionario; puede aumentar el sobreimpulso y desestabilizar |
| **D** | $K_d\,\dot{e}$ | Anticipa el error, amortigua el sobreimpulso, mejora la estabilidad; amplifica el ruido |

## Efectos sobre la respuesta (escalón)
| Aumentar | Tiempo de subida | Sobreimpulso | Asentamiento | Error estacionario |
|----------|------------------|--------------|--------------|--------------------|
| $K_p$ | ↓ | ↑ | poco cambio | ↓ |
| $K_i$ | ↓ | ↑ | ↑ | elimina |
| $K_d$ | poco | ↓ | ↓ | poco |

## Configuraciones habituales
- **P**: solo ganancia, $C(s)=K_p$
- **PI**: $K_p\left(1+\dfrac{1}{T_i s}\right)$ — elimina el error en lazo abierto de tipo 1
- **PD**: $K_p(1+T_d s)$ — añade fase, mejora margen
- **PID**: combina las tres

## Sintonización (tuning)
### Método de Ziegler–Nichols (lazo cerrado, ganancia última)
1. Solo acción P, aumentar $K_p$ hasta oscilación sostenida → $K_u$
2. Medir el período último $T_u$

| Controlador | $K_p$ | $T_i$ | $T_d$ |
|-------------|-------|-------|-------|
| P | $0.5\,K_u$ | — | — |
| PI | $0.45\,K_u$ | $T_u/1.2$ | — |
| PID | $0.6\,K_u$ | $T_u/2$ | $T_u/8$ |

### Regla práctica de ajuste manual
Alternar: primero $K_p$, luego $T_i$ (o $K_i$), después $T_d$, comprobando la [[Respuesta Temporal]] en cada paso.

## Implementación y limitaciones
- La acción derivativa debe filtrarse (el ruido se amplifica a alta frecuencia)
- Cambios de referencia bruscos causan "differential kick": se aplica D a la salida en lugar del error
- Para sistemas con [[Función de Transferencia]] y retardo, pid puede combinarse con compensadores por [[Diagramas de Bode]]

## Conceptos relacionados
- [[Sistemas de Control]]
- [[Respuesta Temporal]]
- [[Estabilidad]]
- [[Lugar Geométrico de las Raíces]]
- [[Márgenes de Ganancia y Fase]]