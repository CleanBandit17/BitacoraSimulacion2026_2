# Bitácora de Desarrollo - Unidad 4: Pizzería Kuramoto

## Link: [Simulador en P5.js](https://editor.p5js.org/CleanBandit18/sketches/pqE6RIs9E)

## Cumplimiento de Requisitos Mínimos

- **8 Agentes Simultáneos:** 8 empleados autónomos gobernados por el modelo de Kuramoto en la calle, junto a un 9no agente estático/interactivo (el Chef) en la puerta del local.
- **4 Personalidades Audiovisuales:** 
  1. *Masero:* Silueta humana naranja con gorro corto + percusión seca (`MembraneSynth`, G2).
  2. *Salsero:* Silueta humana roja + pulso sintético FM (`FMSynth`, C3).
  3. *Hornero:* Silueta humana verde + sonido metálico de pala (`MetalSynth`, 300Hz).
  4. *Repartidor:* Silueta humana azul con visera + timbre agudo (`Synth`, C5).
- **Manifestación Audiovisual:** Al completar cada ciclo de trabajo (fase mod 2π = 0), el agente dispara su nota sonora y lanza una mini-pizza al aire que cae por gravedad. Representa la finalización de una tarea de preparación en ritmo.
- **2 Variables en Vivo:** Sliders interactivos para el Nivel de Sincronización (K, acoplamiento de la brigada) y la Velocidad de Pedidos (ω, frecuencia base).
- **2 Modos de Interacción:** 
  * *Global:* Ajuste continuo de sliders K y ω.
  * *Individual:* Clic sobre un empleado para retrasar su tarea (fase aleatoria) y desplazarlo. Clic sobre el Chef para activar su respuesta por Campo Medio.
- **1 Mecanismo de Perturbación:** Botón **"HORA PICO (Caos)"** que desincroniza a toda la población (fase aleatoria) para imitar un alud repentino de pedidos y observar cómo la brigada se reestructura.
- **3 Estados Colectivos e Indicador:**
  * **Pesadilla en Cocina (R < 0.4):** Polirritmia caótica y movimiento libre desordenado.
  * **Encontrando el Ritmo (R entre 0.4 y 0.8):** Subgrupos rítmicos y atracción paulatina a los carriles.
  * **Línea Perfecta (R >= 0.8):** Unísono rítmico de producción y alineación geométrica fluida.
  * **Indicador:** Estado explícito en la UI (texto e indicador de color según el valor de R).

## Justificación de Diseño

- **Alineación en Carriles:** A medida que K aumenta, el sistema fuerza a los empleados a abandonar su tránsito caótico y alinearse en 4 carriles rígidos. Representa la transición de una cocina desorganizada a una línea de ensamblaje eficiente.
- **Lanzamiento de Pizzas:** El vuelo de las mini-pizzas hace visible el ritmo de trabajo de cada empleado; en sincronía total, todas las pizzas vuelan en unísono perfecto.
- **Easter Egg del Chef (Campo Medio):** El Chef vibra estresado en su puesto de forma predeterminada. Al hacerle clic, se acopla dinámicamente a la fase promedio del grupo (ψ) mediante la ecuación de campo medio `Velocidad_Chef = ω + K_chef * R * sin(ψ - θ_chef)`, demostrando cómo el ritmo global contamina a un oscilador pasivo sin alterar el sistema general.

## Respuesta a la Pregunta Central

> **¿Por qué Kuramoto y no un reloj global?**  
Un reloj global solo conmutaría secuencias predeterminadas. Con Kuramoto, la eficiencia de la cocina es una **emergencia orgánica**: al subir K, el usuario escucha la negociación matemática de tiempos entre las estaciones de preparación (masero, salsero, hornero, repartidor), y tras una "Hora Pico", la brigada reorganiza sus tiempos sola mediante las ecuaciones de fase.

## Autoevaluación

| Criterio de Autoevaluación | Puntaje | Cumplimiento |
| :--- | :---: | :---: |
| **1.** Leí y verifiqué que mi proyecto cumple con los requisitos mínimos de la unidad. | 25 pts | Sí cumple con ellos. |
| **2.** Puedo explicar claramente qué representa cada variable del modelo de Kuramoto en mi proyecto. | 25 pts | En efecto, puedo explicarlo. |
| **3.** Puedo explicar claramente cómo las variables del modelo producen el comportamiento observado en mi proyecto. | 25 pts | Si puedo. Es sencillo. |
| **4.** Puedo demostrar que mi proyecto cumple con los objetivos establecidos en la unidad. | 25 pts | Cumple con cada uno. |
