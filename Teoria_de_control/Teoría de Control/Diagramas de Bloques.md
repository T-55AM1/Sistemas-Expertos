# Diagramas de Bloques

Representación gráfica de un [[Sistemas de Control|sistema de control]] mediante bloques (funciones de transferencia) y sumadores. Permite simplificar el sistema hasta obtener una única [[Función de Transferencia]].

## Elementos básicos
- **Bloque**: aplica una FT, $Y(s)=G(s)\,U(s)$
- **Sumador**: combina señales $\pm$
- **Punto de bifurcación**: replica una señal

## Álgebra de bloques

### Serie (cascada)
$$G_{eq}=G_1(s)\,G_2(s)$$

### Paralelo
$$G_{eq}=G_1(s)+G_2(s)$$

### Realimentación
$$G_{eq}(s)=\frac{G(s)}{1\pm G(s)H(s)}$$

- signo `−`: realimentación negativa
- con $H(s)=1$ (realimentación unitaria):
$$G_{eq}(s)=\frac{G(s)}{1+G(s)}$$

### Cero de cancelación
Los bloques en una trayectoria directa se multiplican; los de una trayectoria de realimentación afectan al denominador.

## Reglas de reducción útiles
- Mover un sumador o bifurcación a través de un bloque requiere compensarlo por $G(s)$ o $G^{-1}(s)$
- Conservar las señales etiquetadas: el resultado final debe conservar $R(s)$ (referencia) y $C(s)$ (salida)

## Regla de Mason
Para diagramas complejos se usa la ganancia de la traza:
$$T=\frac{1}{\Delta}\sum_k G_k\,\Delta_k$$

- $G_k$: ganancia de cada trayecto directo
- $\Delta = 1 - \sum$ (lazos) $+ \sum$ (productos de lazos disjuntos) $-\cdots$
- $\Delta_k$: $\Delta$ excluyendo lazos que tocan al trayecto $k$

## Conceptos relacionados
- [[Sistemas de Control]]
- [[Función de Transferencia]]
- [[Control PID]]