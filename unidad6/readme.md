# Bitácora de Desarrollo - Unidad 6: Agentes Autónomos e Interpretación Visual

## [Link al Simulador](https://cleanbandit17.github.io/Unidad6/)

## Concepto y Gramática Visual

El sistema utiliza la metáfora de un **Diagrama de Inercia y Radar Espacial / Cronofotografía Vectorial**. Mediante agentes autónomos, simula el movimiento de una armada de naves espaciales y registra sus trayectorias geométricas sobre un radar táctico.

- **Naves / Agentes (Triángulos Vectoriales y Nodos):** Entidades autónomas que perciben su entorno y ajustan su dirección.
- **Radar Espacial (Ejes y Anillos Concéntricos):** Marco de referencia táctico y rítmico para las fuerzas del sistema.
- **Physarum / Estelas (Arcos Curvos y Chispas):** Memoria gráfica del espacio donde el paso de los agentes deja trazos de curvatura y destellos de luz.

## Mapeo de Algoritmos

| **Algoritmo** | **Percepción del Agente** | **Cálculo / Acción** | **Expresión Visual** |
|---|---|---|---|
| **Steering Behaviors** | Posición del atractor (mouse). | Viraje limitado para orbitar el centro. | Órbitas elípticas alrededor del radar. |
| **Flow Fields** | Vector de vórtice local. | Fuerza perpendicular a la distancia radial. | Rotación helicoidal de la escuadra. |
| **Flocking (Alineación)** | Velocidad de vecinos (50–90px). | Promedia dirección y se alinea al grupo. | Formación militar en cian con aros indicadores. |
| **Flocking (Separación)** | Distancia a vecinos (<28px). | Fuerza de repulsión según cercanía. | Vuelo abierto sin amontonamiento. |
| **Physarum (Memoria)** | Historial de movimiento del agente. | Deposita arcos y chispas con disipación. | Estelas curvas y destellos que se disuelven. |

## Registro de Cambios e Interacción con la AI

### Versión Inicial

- Fondo gris plano sin ambientación ni radar.
- Agentes representados como círculos negros idénticos (`#1E2A38`).
- Sin reproducción de audio integrada en la aplicación.
- Flocking sin separación, provocando que los agentes colapsaran en una sola masa negra.

### Modificaciones e Iteraciones Realizadas

1. **Diferenciación de Agentes (Opciones A, B y C):**
   - **Opción A (Velocidad):** Cambio de color de Azul Grafito a Rojo Óxido/Fosforescente según aceleración.
   - **Opción B (Flocking):** Color cian y aros de indicación al volar en escuadra (≥3 vecinos).
   - **Opción C (Roles):** 10% de la población como *Naves Guía* con retícula en cruz y estela más gruesa.

2. **Entorno Espacial Dual (Claro / Oscuro):**
   - Diseño de un mapa de radar con ejes, marcas de coordenadas y micro-estrellas adaptativas.
   - Tecla `T` para alternar entre *Carta Astronómica Clara* y *Abismo Estelar Oscuro*.

3. **Calibración de Flocking (Anti-Amontonamiento):**
   - Integración de la regla de *Separación de Reynolds* para mantener espacio personal entre naves.

4. **Integración Directa de Audio:**
   - Carga fija y reproducción automática de `assets/Rihanna - We Found Love (Lyrics) ft. Calvin Harris.mp3` desde la primera interacción.

## Autoevaluación

| **Criterio de Autoevaluación** | **Puntaje** | **Sustentación / Evidencias** |
|---|---|---|
| **1. Cumplimiento del encargo:** Mi instrumento utiliza tecnología web, funciona en tiempo real y permite interpretar la pieza musical elegida. | **/ 25 pts** | Todo funciona en tiempo real y se puede realizar una muestra en vivo con la musica. |
| **2. Comprensión y verificación:** Puedo explicar y defender cómo está construido el sistema, qué perciben los agentes y cómo calculan sus acciones. Puedo predecir y verificar los cambios al modificar un parámetro. | **/ 25 pts** | Hay una tabla que explica el sistema y como los agentes se mueven con base a los parámetros. |
| **3. Diseño e intención:** Puedo justificar la selección y combinación de comportamientos y relacionarlos con mi interpretación musical. | **/ 25 pts** | Si puedo. |
| **4. Interpretación humana:** Mi score y mis controles permiten conducir el sistema en vivo y responder a su comportamiento. | **/ 25 pts** | Claro q puedo profe. |
| **TOTAL** | **/ 100 pts** | |
