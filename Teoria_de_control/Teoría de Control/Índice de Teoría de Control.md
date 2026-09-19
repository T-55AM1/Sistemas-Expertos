# Índice de Teoría de Control

## Introducción

La **Teoría de Control** es la disciplina de la ingeniería que estudia cómo hacer que un sistema (un motor, un horno, una planta industrial, un dron…) se comporte de la forma deseada mediante el diseño de **controladores**. En lugar de depender del azar o de ajustar el sistema "a ojo", se modela matemáticamente el proceso y se cierra un lazo de **realimentación**: se mide la salida, se compara con lo que se quiere obtener (la *referencia*) y se corrige el error.

Estas notas abarcan el recorrido completo de un curso de Teoría de Control, desde los cimientos hasta las técnicas de diseño más usadas:

- **Cómo modelar** un sistema con funciones de transferencia.
- **Cómo responde** ante diferentes entradas (respuesta temporal y frecuencial).
- **Cuándo es estable** y cómo comprobarlo.
- **Cómo diseñar** controladores, en particular el clásico **PID**.

Los conceptos están **interconectados entre sí** mediante enlaces: haz clic en cualquier `[[enlace]]` para saltar a la nota relacionada y seguir el hilo lógico. Todo lo que ves enmarcado con `$$...$$` son fórmulas matemáticas.

Mapa de conceptos de la asignatura **Teoría de Control**. Cada nota está interconectada mediante enlaces bidireccionales.

## Fundamentos
- [[Sistemas de Control]]
- [[Función de Transferencia]]
- [[Diagramas de Bloques]]

## Modelado y Respuesta
- [[Sistema de Primer Orden]]
- [[Sistema de Segundo Orden]]
- [[Respuesta Temporal]]

## Control y Estabilidad
- [[Control PID]]
- [[Estabilidad]]
- [[Criterio de Routh-Hurwitz]]
- [[Lugar Geométrico de las Raíces]]

## Análisis en Frecuencia
- [[Respuesta en Frecuencia]]
- [[Diagramas de Bode]]
- [[Criterio de Nyquist]]
- [[Márgenes de Ganancia y Fase]]

## Flujo de estudio sugerido

1. [[Sistemas de Control]] → entender el lazo de control
2. [[Función de Transferencia]] y [[Diagramas de Bloques]] → modelado
3. [[Sistema de Primer Orden]] y [[Sistema de Segundo Orden]] → dinámica básica
4. [[Respuesta Temporal]] → qué tan bien responde el sistema
5. [[Estabilidad]] → condición necesaria para controlar
6. [[Control PID]] → el controlador por excelencia
7. [[Lugar Geométrico de las Raíces]] y [[Diagramas de Bode]] → diseño