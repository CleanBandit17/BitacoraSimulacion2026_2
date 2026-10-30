# DOPAMINE — Why Bother?

### Unidad 8 · ¿Para qué tomarte el trabajo?

**Proyecto:** Simulación computacional interactiva  
**Herramienta:** p5.js  
**Concepto:** Recompensa inmediata vs. esfuerzo y aprendizaje.

---

## 1. Punto de partida

Para este proyecto partí de una pregunta: ¿qué sentido tiene esforzarnos en hacer algo cuando existen herramientas capaces de hacerlo por nosotros de una manera mucho más rápida y sencilla?

A partir de la charla de Robert Hodgin, *Why Bother? Making Art in the Age of AI*, reflexioné sobre la relación que tenemos actualmente con la inteligencia artificial y cómo esta puede transformar [...]

Una de las ideas que más me hizo pensar fue que el valor de crear algo no está únicamente en el resultado final, sino también en todo lo que sucede durante el proceso. Esto me llevó a cuestionar [...]

## 2. Concepto de la obra

**DOPAMINE** es una simulación computacional interactiva de un cerebro construido completamente a partir de partículas.

La propuesta representa, de manera metafórica, dos formas distintas de obtener satisfacción al realizar una actividad:

- **Dopamina fácil:** representa la recompensa inmediata y la obtención de resultados sin involucrarse demasiado en el proceso.
- **Dopamina con esfuerzo:** representa el tiempo dedicado a aprender, experimentar y desarrollar una actividad por cuenta propia.

El cerebro comienza en un estado neutral, compuesto por partículas blancas. A partir de ese momento, el espectador puede interactuar con la simulación mediante el teclado.

### Controles

| Tecla | Acción | Representación |
|---|---|---|
| `D` | Dopamina fácil | Las partículas rojas llegan al cerebro y generan una reacción intensa e inestable. |
| `E` | Dopamina con esfuerzo | Las partículas azules llegan al cerebro y generan un movimiento fluido y organizado. |
| `SPACE` | Desafío mental | Activa una transformación final dependiendo del estímulo recibido. |
| `R` | Reiniciar | Devuelve la simulación a su estado inicial. |

> **Nota conceptual:** La dopamina se utiliza como una metáfora visual y no como una representación científica del funcionamiento del cerebro.

## 3. Exploración y desarrollo técnico

Para desarrollar la propuesta utilicé **p5.js**, una herramienta que permite crear experiencias visuales mediante programación.

El primer paso fue construir una estructura tridimensional que representara un cerebro utilizando partículas individuales. La intención era que, al observarlas en conjunto, estas formaran una siluet[...]

Posteriormente, trabajé en los diferentes comportamientos de las partículas para diferenciar visualmente cada estímulo:

- **Rojo:** intensidad, velocidad, sobreestimulación e inestabilidad.
- **Azul:** fluidez, movimiento, organización y transformación.
- **Blanco:** estado inicial y neutralidad.

También incorporé interacción mediante el teclado, permitiendo que el espectador tomara decisiones y observara cómo estas modificaban el comportamiento del sistema.

## 4. Resultados y descubrimientos

Uno de los aspectos más interesantes de la exploración fue descubrir cómo un mismo conjunto de partículas podía comunicar sensaciones diferentes dependiendo de su color, movimiento y comportamien[...]

La transformación final del cerebro es uno de los elementos principales de la obra:

### Resultado D — Dopamina fácil

Cuando se activa este estímulo y posteriormente se presiona la barra espaciadora, el cerebro se desestabiliza y sus partículas se dispersan.

Esta transformación representa metafóricamente lo que puede suceder cuando buscamos únicamente obtener resultados inmediatos sin involucrarnos en el proceso de aprendizaje.

### Resultado E — Dopamina con esfuerzo

Cuando se activa este estímulo y posteriormente se presiona la barra espaciadora, el cerebro se transforma en un cielo lleno de estrellas.

Esta transformación representa el conocimiento, las posibilidades y las conexiones que pueden surgir a partir del esfuerzo y la experimentación.

La intención no es ofrecer una respuesta definitiva, sino permitir que el espectador experimente ambas posibilidades y reflexione sobre ellas.

## 5. Aprendizajes

Durante el desarrollo del proyecto exploré diferentes conceptos de programación creativa:

- Sistemas de partículas.
- Representación de objetos en un espacio tridimensional.
- Movimiento y comportamiento de partículas.
- Interacción mediante controles de teclado.
- Cambios de estado dentro de una simulación.
- Transformaciones progresivas de elementos gráficos.

Además, comprendí que programar una simulación no consiste únicamente en conseguir que los elementos se muevan, sino en establecer una relación entre el comportamiento técnico y la idea que se q[...]

Pequeñas decisiones, como modificar el color, la velocidad o la dirección de las partículas, pueden cambiar completamente la percepción de una experiencia visual.

## 6. Reflexión final — ¿Para qué tomarse el trabajo?

Con este proyecto quiero plantear que el esfuerzo no debería entenderse simplemente como una dificultad que debemos evitar. Muchas veces, es precisamente durante ese proceso cuando desarrollamos habi[...]

No considero que utilizar inteligencia artificial esté mal, ni que debamos evitar las herramientas que nos facilitan el trabajo. Sin embargo, creo que es importante preguntarnos cuánto estamos deleg[...]

Para mí, tomarse el trabajo significa darle valor al proceso, experimentar, equivocarse y aprender algo que permanezca después de terminar una actividad.

Por eso, **DOPAMINE** no busca decir que una opción sea completamente buena y la otra completamente mala. Busca generar una pregunta:

> **Si podemos obtener el resultado sin hacer el recorrido, ¿qué estamos dejando de aprender durante el camino?**

---

## 7. Registro visual del proceso

### Estado inicial
<!-- Agregar captura del cerebro con partículas blancas -->

### Dopamina fácil — Estímulo D
<!-- Agregar captura del cerebro en estado rojo -->

### Dopamina con esfuerzo — Estímulo E
<!-- Agregar captura del cerebro en estado azul -->

### Transformación final — Resultado D
<!-- Agregar captura de la dispersión de partículas -->

### Transformación final — Resultado E
<!-- Agregar captura del cielo de estrellas -->

---

## 8. Herramientas y recursos

- [p5.js](https://p5js.org/)
- [Editor web de p5.js](https://editor.p5js.org/)
- Charla de referencia: Robert Hodgin, *Why Bother? Making Art in the Age of AI*.

---

**DOPAMINE — Why Bother?**  
*Una exploración interactiva sobre la recompensa, el esfuerzo y el valor de aprender durante el proceso.*

[Ver proyecto DOPAMINE en p5.js](https://editor.p5js.org/ibanezherrerajuandavid17/sketches/ek9S3P318)
