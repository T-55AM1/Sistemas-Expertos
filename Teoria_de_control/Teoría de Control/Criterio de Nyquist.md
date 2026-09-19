# Criterio de Nyquist

Criterio de [[Estabilidad]] basado en la [[Respuesta en Frecuencia]] del sistema de lazo abierto. Utiliza el **diagrama polar** de $G(s)H(s)$ (trazado de Nyquist) y el principio del argumento.

## Principio del argumento
Si una curva cerrada $C$ encierra $Z$ ceros y $P$ polos de $F(s)=1+G(s)H(s)$, el número de **envolvimientos** de $C$ alrededor del origen es:
$$N=Z-P$$

## El contorno de Nyquist
Curva cerrada en el plano $s$ que rodea el semiplano derecho completo ($j\omega$ de $-\infty$ a $\infty$ más el arco de radio infinito). Así $Z$ cuenta los ceros de $F$ → polos del lazo cerrado inestables.

## Enunciado del criterio
El sistema de lazo cerrado es estable si y solo si el número de **envolvimientos** $N$ del trazado de $G(j\omega)H(j\omega)$ alrededor del punto $(-1, j0)$ cumple:

$$Z=N+P=0$$

- $N>0$: rodeos en sentido horario (negativos)
- $P$: polos de lazo abierto en el SPD (conocidos)
- Se requiere $Z=0$

## Polos de lazo abierto sobre el eje $j\omega$
Se evitan con **desvíos** de radio pequeño alrededor de $s=j\omega$. Cada polo sobre el eje añade un arco de 180° al trazado.

## Lectura del diagrama polar
- **Magnitud** $|G(j\omega)|$: distancia al origen
- **Fase**: ángulo respecto al eje real
- El punto crítico $(-1, j0)$ equivale a $KG(s)H(s)=-1$, la condición de oscilación marginal

## Relación con otros métodos
- De $|G(j\omega_{gc})|$ y $\angle G(j\omega_{pc})$ se obtienen los [[Márgenes de Ganancia y Fase]]
- El cruce por $(-1, j0)$ coincide con el límite de estabilidad del [[Criterio de Routh-Hurwitz]] y del [[Lugar Geométrico de las Raíces]]
- Con los [[Diagramas de Bode]] se traza lo mismo en forma semilogarítmica

## Conceptos relacionados
- [[Estabilidad]]
- [[Respuesta en Frecuencia]]
- [[Márgenes de Ganancia y Fase]]
- [[Diagramas de Bode]]
- [[Función de Transferencia]]