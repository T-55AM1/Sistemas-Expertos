# Estabilidad

Un sistema es **estable** si, ante una entrada acotada, su salida permanece acotada (estabilidad BIBO, *bounded input–bounded output*). En la práctica: ningún polo en el semiplano derecho (SPD).

## Criterio de polos
Para un sistema lineal con [[Función de Transferencia]] $G(s)=\dfrac{N(s)}{D(s)}$:

- **Estable**: todos los polos tienen parte real negativa ($\Re(s)<0$)
- **Marginalmente estable**: polos imaginarios puros simples
- **Inestable**: algún polo con $\Re(s)\ge0$ (o polos repetidos en el eje imaginario)

## Respuesta al impulso
$$y(t)=\mathcal{L}^{-1}\{G(s)\}=\sum \frac{A_i}{s-p_i}$$

Cada polo contribuye un término $A_i e^{p_i t}$:
| Polo | Comportamiento |
|------|----------------|
| $p_i<0$ (real) | decae: $e^{-\sigma t}\to0$ → estable |
| $p_i>0$ (real) | crece: $e^{+\sigma t}\to\infty$ → inestable |
| $p_i=\pm j\omega$ | oscila sin amortiguar → marginalmente estable |

Los polos del lazo cerrado son las raíces de la **ecuación característica**:
$$1+G(s)H(s)=0$$

## Métodos para evaluar la estabilidad
- **Algebraico**: [[Criterio de Routh-Hurwitz]] — sin factorizar
- **Gráfico en el plano complejo**: [[Lugar Geométrico de las Raíces]] — variación de la ganancia
- **En frecuencia**: [[Criterio de Nyquist]] y [[Diagramas de Bode]] (con [[Márgenes de Ganancia y Fase]])

## Estabilidad interna vs. externa
- **Externa (BIBO)**: solo importan polos observables y controlables (cancelaciones polo-cero se eliminan)
- **Interna**: si hay cancelaciones polo-cero en el SPD, el sistema interno es inestable aun con FT estable

## Conceptos relacionados
- [[Función de Transferencia]]
- [[Sistemas de Control]]
- [[Respuesta Temporal]]
- [[Criterio de Routh-Hurwitz]]
- [[Criterio de Nyquist]]