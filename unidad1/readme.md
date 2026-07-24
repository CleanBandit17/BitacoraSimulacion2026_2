# Bitácora – Reto de diseño: Navegar la incertidumbre

## Intención conceptual

El objetivo de esta propuesta fue representar la idea de que la incertidumbre no significa ausencia de reglas, sino que diferentes formas de aleatoriedad producen comportamientos distintos. En lugar de ilustrar literalmente los cinco conceptos del enunciado, se diseñó un sistema de partículas cuyo comportamiento cambia mediante probabilidades y reglas de movimiento. La interacción del visitante modifica estas probabilidades, pero nunca controla completamente el sistema.

---

## Momento 1 – Posibilidad

Inicialmente, cada partícula realiza una caminata aleatoria. En este estado todas las direcciones tienen la misma probabilidad de ocurrir, por lo que el sistema transmite una sensación de apertura y múltiples posibilidades sin una trayectoria dominante.

---

## Momento 2 – Tendencia

Se incorporó un pequeño vector de dirección constante que influye sobre todas las partículas. Aunque este cambio es muy sutil, al repetirse continuamente genera una dirección predominante. La intención es mostrar cómo una pequeña preferencia puede producir un comportamiento colectivo sin eliminar la incertidumbre.

---

## Momento 3 – Normalidad

Las partículas nacen utilizando una distribución normal (`randomGaussian()`), lo que hace que la mayoría aparezca cerca del centro y pocas se ubiquen en posiciones alejadas. Además, el movimiento se suaviza mediante ruido Perlin, generando trayectorias continuas y naturales. Este estado representa que los eventos más comunes suelen concentrarse alrededor de un comportamiento esperado.

---

## Momento 4 – Excepción

De manera poco frecuente, algunas partículas realizan un salto de Lévy. Estos desplazamientos largos permiten que el sistema explore regiones completamente nuevas del espacio. La excepción rompe temporalmente el patrón dominante y evidencia que los eventos improbables también transforman el comportamiento del sistema.

---

## Momento 5 – Influencia

La presencia del visitante se representa mediante el cursor del mouse. El usuario no controla directamente las partículas; en cambio, modifica las probabilidades del sistema. Al acercar el cursor, aumenta la influencia sobre el comportamiento colectivo, las partículas cambian gradualmente hacia tonos rojos y las conexiones desaparecen para enfatizar la transformación del sistema. De esta manera, la interacción altera las reglas, pero mantiene la incertidumbre como parte esencial de la experiencia.

---

## Experimentos realizados

Durante el desarrollo se probaron varias alternativas. Inicialmente las partículas solo realizaban caminatas aleatorias, lo que generaba un comportamiento demasiado caótico. Posteriormente se añadieron ruido Perlin y una ligera tendencia direccional para obtener recorridos más orgánicos. También se implementaron conexiones entre partículas y estelas para mejorar la lectura visual del movimiento. Finalmente se ajustó el comportamiento cuando el visitante interactúa para evitar problemas de rendimiento y reforzar visualmente el cambio de estado mediante el color.

---

## Dificultades y soluciones

La principal dificultad fue el rendimiento cuando muchas partículas convergían en una misma región. El exceso de conexiones provocaba una disminución considerable de la velocidad de ejecución. Como solución, se desactivan las conexiones cuando la influencia del visitante es muy alta y se reemplazan por un cambio de color y un incremento en el brillo de las partículas, conservando el significado conceptual sin afectar el desempeño.

---

## Uso de IA generativa

La IA generativa se utilizó como apoyo para proponer la arquitectura inicial del sistema, sugerir estrategias de implementación en p5.js y explorar distintas alternativas visuales. Posteriormente se realizaron modificaciones manuales sobre el código, ajustando el comportamiento de las partículas, la interacción con el usuario, la representación visual y la optimización del rendimiento para obtener el resultado final.

---

### Link de P5.js con el código completo

https://editor.p5js.org/natureofcode/sketches/u4vTwZuhT
