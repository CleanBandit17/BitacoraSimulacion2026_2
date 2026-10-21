# Bitácora de Desarrollo - Unidad 4: El Gobierno Opresor

## Link: [Simulador en P5.js](https://editor.p5js.org/CleanBandit18/sketches/pqE6RIs9E)

## Cumplimiento de Requisitos Mínimos

* **8 Agentes Simultáneos:** 8 ciudadanos autónomos gobernados por el modelo de Kuramoto en la calle, junto a un 9no agente estático (el Dictador) en el balcón.
* **4 Personalidades Audiovisuales:** 
  1. *Rebelde:* Silueta circular blanca + percusión seca (`MembraneSynth`, G2).
  2. *Obrero:* Silueta ancha gris + sonido metálico (`MetalSynth`, 300Hz).
  3. *Burocrata:* Silueta esbelta oscura + bajo FM (`FMSynth`, C2).
  4. *Propagandista:* Silueta con visor amarillo + *beep* agudo (`Synth`, C5).
* **Manifestación Audiovisual:** Al completar cada ciclo de fase ($\theta_i \bmod 2\pi = 0$), el agente dispara su nota sonora y un halo/destello amarillo en su contorno. Representa el impacto del paso contra el suelo.
* **2 Variables en Vivo:** Sliders interactivos para el Nivel de Vigilancia ($K$, acoplamiento) y la Velocidad del Régimen ($\omega$, frecuencia base).
* **2 Modos de Interacción:** 
  * *Global:* Ajuste continuo de sliders $K$ y $\omega$.
  * *Individual:* Clic sobre un agente para "arrestarlo" (desfasa su ciclo y lo desplaza físicamente).
* **1 Mecanismo de Perturbación:** Botón **"PERTURBAR (Motín)"** que desincroniza a toda la población ($\theta_i = \text{random}$) para observar la reestructuración del colectivo.
* **3 Estados Colectivos e Indicador:**
  * *Anarquía ($R < 0.4$):* Polirritmia caótica y libre tránsito espacial.
  * *Organización Parcial ($0.4 \le R < 0.8$):* Subgrupos rítmicos y atracción paulatina a los carriles.
  * *Control Total ($R \ge 0.8$):* Unísono rítmico militar y alineación geométrica rígida.
  * *Indicador:* Estado explícito en la UI (texto y color según el valor de $R$).

## Justificación de Diseño

* **Alineación en Carriles:** A medida que $K$ aumenta, el sistema fuerza a los agentes a abandonar su movimiento libre y alinearse en 4 carriles rígidos. Representa cómo la sincronización rítmica del Estado priva al individuo de su libertad espacial.
* **Halo de Paso:** El destello amarillo al sonar refleja la visibilidad y sumisión del ciudadano ante el régimen; en sincronía, todos los halos brillan unificados anulando la individualidad.

## Respuesta a la Pregunta Central

> **¿Por qué Kuramoto y no un reloj global?**  
Un reloj global solo conmuta secuencias predeterminadas. Con Kuramoto, el paso del caos al unísono es una **emergencia orgánica**: al subir $K$, el usuario escucha la negociación matemática de los pasos entre agentes, y tras un "Motín", la masa se reorganiza sola mediante las ecuaciones de fase.

## Autoevaluación

| Criterio de Autoevaluación | Puntaje | Cumplimiento |
| :--- | :---: | :---: |
| **1.** Leí y verifiqué que mi proyecto cumple con los requisitos mínimos de la unidad. | 25 pts | Sí cumple con ellos. |
| **2.** Puedo explicar claramente qué representa cada variable del modelo de Kuramoto en mi proyecto. | 25 pts | En efecto, puedo explicarlo. |
| **3.** Puedo explicar claramente cómo las variables del modelo producen el comportamiento observado en mi proyecto. | 25 pts | Si puedo. Es sencillo. |
| **4.** Puedo demostrar que mi proyecto cumple con los objetivos establecidos en la unidad. | 25 pts | Cumple con cada uno. |
