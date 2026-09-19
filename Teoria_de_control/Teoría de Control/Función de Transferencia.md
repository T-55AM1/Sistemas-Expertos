# Función de Transferencia

Modelo algebraico que relaciona la salida $Y(s)$ con la entrada $U(s)$ de un sistema lineal e invariante en el tiempo (LTI), en el dominio de **Laplace**, con condiciones iniciales nulas.

$$G(s)=\frac{Y(s)}{U(s)}$$

## Transformada de Laplace
$$F(s)=\mathcal{L}\{f(t)\}=\int_0^\infty f(t)\,e^{-st}\,dt$$

Propiedad clave (derivada):
$$\mathcal{L}\{f'(t)\}=sF(s)-f(0)$$

## Forma factorizada
$$G(s)=K\,\frac{\prod(s-z_i)}{\prod(s-p_j)}$$

- **Polos** $p_j$: raíces del denominador. Determinan la dinámica y la [[Estabilidad]].
- **Ceros** $z_i$: raíces del numerador. Afectan la forma de la respuesta.
- **Ganancia estática** $K$: $G(0)$ en el caso de sistemas con ganancia finita.

## Ganancia y constante de tiempo
La ganancia estática es:
$$K_s=G(0)=\lim_{t\to\infty} y(t)\quad\text{para entrada escalón}$$

## Tipos de sistemas según la FT
| Tipo | Denominador | Ejemplo |
|------|-------------|---------|
| de ganancia | constante | $K$ |
| de primer orden | $1$ polo | $\dfrac{K}{\tau s+1}$ |
| de segundo orden | $2$ polos | $\dfrac{K\omega_n^2}{s^2+2\zeta\omega_n s+\omega_n^2}$ |
| con integrador | polo en $s=0$ | $\dfrac{K}{s}$ |
| con retardo | $e^{-Ls}$ | $G(s)e^{-Ls}$ |

## Obtención
- A partir de ecuaciones diferenciales (Laplace + despejar $Y/U$)
- A partir de la respuesta al impulso o al escalón
- A partir de datos experimentales (identificación)

## Conceptos relacionados
- [[Sistemas de Control]]
- [[Diagramas de Bloques]]
- [[Sistema de Primer Orden]]
- [[Sistema de Segundo Orden]]