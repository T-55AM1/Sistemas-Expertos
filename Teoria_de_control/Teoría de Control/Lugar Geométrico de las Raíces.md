# Lugar Geométrico de las Raíces

Técnica gráfica que muestra cómo se desplazan los **polos del lazo cerrado** en el plano complejo cuando varía la ganancia $K$ (de $0$ a $\infty$). Permite diseñar ganancias del [[Control PID|controlador]] y evaluar la [[Estabilidad]].

## Ecuación característica
$$1+K\,G(s)H(s)=0 \;\Rightarrow\; KG(s)H(s)=-1$$

Condiciones de módulo y ángulo:
$$|KG(s)H(s)|=1$$
$$\angle\,[G(s)H(s)]=180^\circ+360^\circ k=(2k+1)180^\circ$$

## Lugar directo (−180°) y lugar inverso (0°)
- Lugar directo ($0\le K<\infty$): condición de ángulo $-180^\circ$
- Lugar inverso ($-\infty<K\le0$): condición $0^\circ$

## Reglas de construcción (lugar directo)
1. **Número de ramas** = número de polos de lazo abierto $n$
2. **Puntos de inicio** ($K=0$): polos de lazo abierto
3. **Puntos finales** ($K\to\infty$): ceros de lazo abierto; el resto tiende a **asíntotas**
4. **Trazos sobre el eje real**: a la izquierda de un número **impar** de polos+ceros reales
5. **Asíntotas**: centroide y ángulos
   $$\sigma_a=\frac{\sum p_i-\sum z_i}{n-m},\qquad \phi_a=\frac{(2k+1)180^\circ}{n-m}$$
6. **Puntos de ruptura** (separación/entrada al eje real): soluciones de
   $$\frac{d}{ds}\big[G(s)H(s)\big]=0$$
7. **Ángulos de salida/entrada** desde polos/hacia ceros complejos: conservación de ángulos
8. **Cruces con el eje $j\omega$**: resolver $1+KG(s)H(s)=0$ con $s=j\omega$ (o usar [[Criterio de Routh-Hurwitz]]), obteniendo el valor crítico de $K$

## Interpretación de diseño
- Polos en el SPD → inestable
- Polos dominantes (más cercanos al origen) rigen la [[Respuesta Temporal]]
- Para el [[Sistema de Segundo Orden]]: $\zeta\omega_n=\sigma$ (parte real), $\omega_d$ (parte imaginaria)
- Especificaciones: colocar polos en la región que cumpla $\%M_p$ y $t_s$

## Conceptos relacionados
- [[Estabilidad]]
- [[Sistema de Segundo Orden]]
- [[Respuesta Temporal]]
- [[Criterio de Routh-Hurwitz]]
- [[Control PID]]