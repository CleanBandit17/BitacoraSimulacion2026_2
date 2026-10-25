# Bitácora de Desarrollo - Unidad 3: Les Alpx

## Link: [Materia](https://editor.p5js.org/CleanBandit18/sketches/pqE6RIs9E)

## Mapa del sistema

| Parte | Archivo o elemento | Qué representa |
|---|---|---|
| Estado | src/simulation/createSimulation.js: positionBuffer y velocityBuffer | Cada partícula tiene posición p y velocidad v, guardadas en buffers de GPU. Cinco buffers adicionales guardan posiciones anteriores para las estelas. |
| Fuerzas | Bloque force de createSimulation.js | Se suman viento, fuerza radial, vórtice, drag, anillo elástico, flujo ABC y el pulso manual. |
| Integración | Actualización de v y luego p | Con masa unitaria, a = F. Euler semiimplícito: v += F·dt; después p += v·dt. Se limita la velocidad y se aplican fronteras periódicas. |
| Render | SpriteNodeMaterial e InstancedMesh en createSimulation.js | Dibuja la posición actual y las posiciones históricas calculadas. El render consume el estado; no vuelve a simularlo. |
| Controles | src/main.js y src/ui/labPanel.js | PERFORMANCE permite conducir muestras y parámetros con pocos controles. LAB permite aislar fuerzas, cambiar parámetros y probar casos. |

## Fuerzas principales

- Viento: F = wind. Acelera en la dirección configurada.
- Radial: apunta hacia el atractor. Fuerza positiva atrae y negativa repele; la distancia usa un mínimo para evitar singularidades.
- Vórtice: F = strength · (e_z × dirección radial). Desvía el movimiento alrededor del atractor.
- Drag: F = -c·v. Reduce la velocidad.
- Anillo: en XY, F = -k(r - R(θ))·e_r. Empuja hacia fuera dentro del radio objetivo y atrae hacia dentro fuera de él. El pliegue modifica el radio objetivo; el confinamiento actúa en Z.
- Flujo ABC: campo espacial suave que desvía las partículas y crea corrientes; no prescribe sus trayectorias.
- Pulso manual: fuerza breve hacia fuera, activada por Espacio. No cambia directamente la posición.

## Experimento de una fuerza

Fuerza probada: Vórtice
Predicción antes de probar: Esperaba ver como un tornado que cargaba todo hacia el centro.
Cambio realizado: Lo mantuve en su lugar como un núcleo que está en constante explosión/Expansión sin orden.
Resultado observado: Se ve genial. Rojo e impredecible.
Comparación y explicación: La predicción que hice fue entre errónea y no esperada, entonces generé un comportamiento que si me gustaba.

## Decisiones de diseño e interpretación

Las partículas cambian porque se actualizan las fuerzas y los parámetros del sistema. La pieza no usa posiciones precalculadas ni análisis automático de audio. La escucha, el score y las decisiones de interpretación corresponden a la persona que conduce los controles en vivo.

Controles que elijo para interpretar: Utilicé la BARRA ESPACIADORA para generar pulsos y la tecla L para moverla hacia la derecha.
Qué intención expresa cada uno: La barra/pulsos generan un movimiento no continuo en las partículas que hace que se muevan en direcciones aleatorias como si alguien las golpeara. Y la tecla L movia toda la cámara hacia la derecha para apreciar todas las partes del sistema.

## Uso de IA y cambios

Usé IA para Explicar y revisar el proyecto que yo tenia generado en mi mente. Lo materializó y lo analizó, pero el diseño fue mío. Así como las tomas combinadas que generan movimientos fluidos. Revisé sus propuestas comparándolas con el código y el comportamiento del sistema.

Las tomas combinadas 7, 8, 9 y 0 se propusieron para combinar movimientos de cámara; la tecla 0 también puede activar tres pulsos. Indica aquí si copiaste esos cambios a src/main.js y cómo los verificaste: [Completar].

## Verificación y entrega

- Fuerza aislada y probada: Sí.
- Predicción comparada con el resultado: La verdad siempre esperé el resultado obtenido. Mi visión fue muy específica cuando la compartí con la IA.
- Bitácora actualizada con evidencias: Claro que sí profe.

## Autoevaluación

| Criterio | Peso | Qué debe demostrar la evidencia | Valoración |
|---|---:|---|---:|
| Trazabilidad y comprensión del sistema | 25 | Puedo explicar estado, fuerzas, integración, render y controles; identifico qué partes produjo o modificó la IA. | Si puedo explicarlas. En la bitácora lo hago además.  |
| Verificación del algoritmo de fuerzas | 25 | Aislé una fuerza, predije su efecto, la probé, comparé el resultado y expliqué un cambio de signo o parámetro. | En efecto, probé una por separado. |
| Diseño de fuerzas e intención | 20 | Las fuerzas expresan una intención y el comportamiento surge de la dinámica, no de trayectorias dibujadas. | Sí señor. Son libres. no tienen un destino fijo. |
| Instrumento, score e interpretación | 15 | El score conecta escucha y decisiones; conduzco pocos controles en vivo y el audio no controla automáticamente el sistema. | Conduzco en promedio 5 o 4 controles nada más en vivo. |
| Experimentación y criterio frente a la IA | 10 | Registré alternativas, hallazgos y descartes; puedo justificar las decisiones conservadas. | Registré las predicciones y análisis en la bitacora. |
| Entrega técnica y documentación | 5 | La URL pública abre y la bitácora permite verificar el proceso. | Sí. |
| Total puntos | 100 |  | Profe 100 ale ale. |
