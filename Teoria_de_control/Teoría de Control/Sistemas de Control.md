# Sistemas de Control

Un **sistema de control** manipula las variables de un proceso para que su salida siga una referencia deseada, reduciendo el efecto de perturbaciones e incertidumbre.

## Configuración en lazo abierto (open-loop)
La entrada no depende de la salida. No hay medición ni corrección.
```
Referencia → Controlador → Planta → Salida
```
- Simple y barato, pero no compensa perturbaciones.

## Configuración en lazo cerrado (closed-loop / feedback)
La salida se mide, se compara con la referencia y el error se usa para corregir.
```
Referencia (−) → Error → Controlador → Planta → Salida
                     ↑                             |
                     └────── Sensor y realimentación ┘
```

## Función de transferencia de lazo cerrado
Para realimentación unitaria:
$$T(s)=\frac{C(s)\,G(s)}{1+C(s)\,G(s)}$$

- **Planta** $G(s)$: sistema a controlar.
- **Controlador** $C(s)$: por lo general un [[Control PID]].
- **Sensor**: mide la salida (puede añadir su propia dinámica $H(s)$).

## Ventajas del lazo cerrado
- Menor sensibilidad a perturbaciones
- Reducción de la sensibilidad a variaciones de parámetros
- Mejora del comportamiento dinámico (ver [[Respuesta Temporal]]
- Permite estabilizar sistemas inestables (ver [[Estabilidad]]

## Conceptos relacionados
- [[Función de Transferencia]]
- [[Diagramas de Bloques]]
- [[Control PID]]
- [[Respuesta en Frecuencia]]