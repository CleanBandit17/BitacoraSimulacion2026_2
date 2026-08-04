
### UNIDAD 2 (RETO DE DISEÑO)

# 1. Intención

## Tensión

> **Quiero explorar la tensión entre la búsqueda intencional del afecto, el desarrollo personal y la influencia de intereses externos en la construcción de los vínculos.**

## Descripción

Este sistema generativo utiliza un sistema de partículas como metáfora para explorar distintas dinámicas que pueden surgir durante la construcción de relaciones humanas. En lugar de representar personas de manera literal, cada población de partículas simboliza un conjunto de comportamientos que interactúan mediante reglas de atracción, repulsión e indiferencia, permitiendo que el significado emerja a partir de las relaciones entre ellas y no de elementos narrativos o visuales.

La propuesta parte de una idea central: no todos los vínculos aparecen como consecuencia de buscarlos activamente. Dentro del sistema, las partículas que buscan constantemente establecer conexiones ejercen una fuerte atracción sobre otras partículas; sin embargo, esta misma insistencia provoca comportamientos de rechazo, dificultando la formación de vínculos estables. En contraste, las partículas que permanecen enfocadas en su propio recorrido no persiguen a las demás, sino que continúan explorando el espacio de manera autónoma. Es precisamente a partir de esos recorridos independientes donde comienzan a surgir encuentros espontáneos, representando la posibilidad de que algunas conexiones aparezcan como consecuencia del recorrido y no de la persecución.

El sistema también incorpora variables externas que modifican estas dinámicas sin controlar directamente a las partículas. Mediante deslizadores, el usuario puede alterar la intensidad de la búsqueda, el miedo al rechazo, el desarrollo personal y la influencia de incentivos económicos. Estas variables modifican las fuerzas de interacción entre las distintas poblaciones, produciendo reorganizaciones colectivas que emergen únicamente de la aplicación continua de las reglas del sistema.

De esta manera, la propuesta busca representar cómo pequeñas modificaciones en las condiciones iniciales o en las reglas de interacción pueden transformar completamente el comportamiento colectivo de un mismo sistema. Aunque cada ejecución produce resultados diferentes, todas conservan la misma identidad conceptual: explorar cómo las decisiones individuales y las influencias externas afectan la aparición de conexiones dentro de un entorno dinámico.

Finalmente, este proyecto no pretende afirmar que las relaciones humanas funcionen de una única manera ni ofrecer una explicación definitiva sobre el amor. Su propósito es utilizar el diseño generativo como una herramienta para explorar una posible interpretación de estas dinámicas mediante un sistema de reglas y comportamientos emergentes. **El sistema no intenta responder cómo funciona el amor, sino explorar cómo diferentes reglas de interacción pueden producir formas distintas de encuentro, rechazo y conexión.**


# 2. Entidades

El sistema está compuesto por tres poblaciones de partículas. Cada una representa un comportamiento distinto dentro de la metáfora propuesta y posee reglas específicas que determinan la forma en que interactúa con las demás. Estas entidades no representan personas de manera literal, sino diferentes dinámicas que pueden influir en la construcción de vínculos.

---

## ❤️ Buscadores

Las partículas **Buscadoras** representan a quienes orientan gran parte de su comportamiento hacia la búsqueda activa de una conexión afectiva.

Su característica principal es que identifican partículas cercanas y ejercen una fuerza de atracción constante hacia ellas. Sin embargo, esta búsqueda persistente genera una respuesta de rechazo por parte de las partículas enfocadas, produciendo una paradoja: cuanto mayor es el esfuerzo por alcanzar un vínculo, menor es la probabilidad de que este ocurra de manera estable.

Estas partículas poseen una velocidad media-alta y una mayor sensibilidad a las fuerzas de interacción, haciendo que sus trayectorias sean más directas e insistentes.

---

## 🌱 Enfocados

Las partículas **Enfocadas** representan a quienes priorizan su propio desarrollo personal antes que la búsqueda activa de una relación.

A diferencia de los buscadores, no persiguen otras partículas. Su movimiento está determinado por fuerzas internas y pequeñas variaciones aleatorias, permitiéndoles recorrer el espacio de forma libre y explorar nuevas regiones del sistema.

Su comportamiento favorece la aparición de encuentros espontáneos, ya que al no perseguir constantemente a otras partículas aumentan las probabilidades de coincidir naturalmente con ellas. Además, son las únicas partículas cuyo comportamiento puede verse alterado por variables externas como el desarrollo personal y los incentivos económicos.

---

## 💰 Intereses Económicos

Las partículas de **Intereses Económicos** representan oportunidades o incentivos materiales presentes dentro del entorno.

Su comportamiento es completamente pasivo. No buscan otras partículas, no reaccionan a fuerzas externas y permanecen distribuidas en el espacio como puntos de influencia potencial.

Cuando el parámetro **Incentivo Económico** aumenta, las partículas enfocadas comienzan a sentirse atraídas hacia ellas, modificando sus trayectorias y reduciendo la frecuencia con la que aparecen encuentros espontáneos. De esta forma, estas entidades representan cómo un factor externo puede reorganizar completamente la dinámica del sistema sin alterar directamente las reglas fundamentales de las demás poblaciones.

---

## Comportamiento emergente: Conexiones

Las **conexiones** no constituyen una población independiente del sistema, sino un comportamiento emergente que aparece como consecuencia de las reglas de interacción entre las partículas.

Cuando dos partículas enfocadas coinciden de manera natural y permanecen próximas durante un tiempo suficiente, el sistema interpreta este encuentro como la formación de un vínculo y lo representa visualmente mediante un halo o una conexión luminosa temporal.

Esta decisión busca reforzar la idea central del proyecto: las conexiones no están programadas para existir desde el inicio, sino que emergen únicamente cuando las condiciones del sistema lo permiten. De esta manera, el vínculo deja de ser una entidad diseñada y pasa a ser el resultado de la interacción continua entre las distintas reglas que gobiernan el comportamiento colectivo.

---

| Entidad | Representación | Comportamiento principal |
|----------|----------------|--------------------------|
| ❤️ Buscadores | Búsqueda activa del afecto | Persiguen constantemente a las partículas enfocadas, generando dinámicas de atracción y rechazo. |
| 🌱 Enfocados | Desarrollo personal | Recorren el espacio de forma autónoma y favorecen la aparición de encuentros espontáneos. |
| 💰 Intereses Económicos | Incentivos externos | Permanecen pasivos y atraen a las partículas enfocadas cuando aumenta el parámetro de incentivo económico. |

> **Nota de diseño:** Las conexiones no son una entidad independiente, sino un comportamiento emergente del sistema. Su aparición depende exclusivamente de las reglas de interacción entre las partículas y de las condiciones que se generan durante la simulación.


# 3. Relaciones

Las relaciones constituyen el núcleo del sistema generativo. Cada población de partículas responde de manera diferente ante las demás mediante fuerzas de atracción, repulsión o indiferencia. Estas relaciones no buscan representar comportamientos individuales, sino explorar cómo distintas reglas de interacción producen dinámicas colectivas emergentes.

La intensidad de cada interacción se encuentra normalizada entre **-1** (repulsión máxima) y **1** (atracción máxima), donde los valores cercanos a cero representan una influencia muy baja o indiferencia.

---

## Matriz de relaciones

|                     | ❤️ Buscadores | 🌱 Enfocados | 💰 Intereses Económicos |
|---------------------|:------------:|:-----------:|:-----------------------:|
| ❤️ **Buscadores** | -0.20 | **0.85** | 0.00 |
| 🌱 **Enfocados** | **-0.60** | 0.15 | Variable *(Slider: Incentivo Económico)* |
| 💰 **Intereses Económicos** | 0.00 | 0.00 | 0.00 |

---

# 3. Justificación de cada relación

### ❤️ Buscadores → ❤️ Buscadores (-0.20)

Los buscadores presentan una ligera repulsión entre sí para evitar que se agrupen permanentemente. Esto favorece que cada uno continúe explorando el sistema y dirija su atención hacia las partículas enfocadas.

---

### ❤️ Buscadores → 🌱 Enfocados (+0.85)

Esta es la relación de atracción más fuerte del sistema.

Los buscadores intentan acercarse constantemente a las partículas enfocadas, representando la búsqueda activa de una conexión. Sin embargo, esta atracción no garantiza que el vínculo ocurra, ya que la respuesta de las partículas enfocadas es diferente.

---

### 🌱 Enfocados → ❤️ Buscadores (-0.60)

Esta es la **relación asimétrica** principal del sistema.

Mientras los buscadores sienten una fuerte atracción hacia los enfocados, estos responden con una fuerza de repulsión moderada cuando perciben una persecución constante.

Esta diferencia entre ambas direcciones representa la tensión principal del proyecto: una misma interacción es interpretada de forma distinta por cada población.

---

### 🌱 Enfocados → 🌱 Enfocados (+0.15)

Las partículas enfocadas sienten una atracción muy suave entre ellas.

No buscan agruparse deliberadamente, pero esta pequeña fuerza aumenta la probabilidad de que permanezcan próximas durante algunos instantes.

Cuando esa proximidad se mantiene el tiempo suficiente, el sistema interpreta el encuentro como una conexión espontánea.

---

### 🌱 Enfocados → 💰 Intereses Económicos (Variable)

Esta relación depende completamente del deslizador **Incentivo Económico**.

Cuando el valor del deslizador es bajo, la fuerza de atracción es prácticamente nula y las partículas enfocadas continúan su recorrido natural.

A medida que aumenta el incentivo, las partículas enfocadas comienzan a modificar su trayectoria para acercarse a los intereses económicos.

Esto permite observar cómo un factor externo puede reorganizar completamente las dinámicas del sistema sin modificar la naturaleza de las demás relaciones.

---

### 💰 Intereses Económicos

Las partículas que representan intereses económicos no reaccionan ante ninguna otra población.

No buscan, no persiguen y no generan fuerzas propias.

Su única función consiste en convertirse en un punto de atracción potencial cuando el parámetro correspondiente aumenta.

---

## Relación asimétrica

La contradicción central del sistema se encuentra en la relación entre Buscadores y Enfocados.

Los Buscadores sienten una fuerte atracción hacia los Enfocados.

Los Enfocados, en cambio, responden con una fuerza de repulsión.

Esta asimetría produce un comportamiento emergente donde la insistencia dificulta la formación de conexiones, mientras que los encuentros espontáneos aparecen únicamente cuando las trayectorias coinciden sin persecución directa.

De esta manera, el significado del sistema no depende del nombre de las partículas, sino de las reglas que gobiernan sus interacciones.


# 4. Entradas

Las entradas corresponden a los elementos capaces de modificar el comportamiento del sistema sin controlar directamente el movimiento de las partículas. En lugar de determinar el resultado final, estas variables alteran las reglas de interacción, permitiendo que el comportamiento colectivo emerja de manera diferente en cada ejecución.

El sistema cuenta con cinco entradas principales: una interna (el tiempo) y cuatro controladas por el usuario mediante deslizadores.

---

## ⏳ Tiempo

El tiempo constituye la entrada permanente del sistema.

Cada frame actualiza la posición, velocidad y aceleración de todas las partículas, permitiendo que las fuerzas de atracción y repulsión produzcan nuevas configuraciones de manera continua. Gracias al paso del tiempo, el sistema nunca permanece estático y las relaciones evolucionan constantemente.

---

## ❤️ Intensidad de la búsqueda

Este parámetro controla la fuerza con la que las partículas **Buscadoras** intentan acercarse a las partículas **Enfocadas**.

Valores bajos producen búsquedas más moderadas, mientras que valores altos incrementan la intensidad de la persecución. Debido a la relación asimétrica del sistema, un aumento en la intensidad de búsqueda suele generar mayores comportamientos de rechazo y disminuye la probabilidad de que aparezcan conexiones espontáneas.

Este parámetro no controla las trayectorias individuales, sino la intensidad de una de las fuerzas presentes en la matriz de relaciones.

---

## 😰 Miedo al rechazo

Este deslizador modifica el comportamiento de las partículas **Buscadoras** frente a la posibilidad de ser rechazadas.

Cuando su valor aumenta, las partículas reducen progresivamente la intensidad con la que persiguen a las partículas enfocadas y mantienen una mayor distancia antes de intentar aproximarse nuevamente. Como consecuencia, sus movimientos se vuelven más cautelosos y menos insistentes.

El parámetro representa cómo una modificación en la estrategia de interacción puede alterar el comportamiento colectivo del sistema.

---

## 🌱 Desarrollo personal

Este parámetro representa el grado de atención que las partículas **Enfocadas** dedican a su propio recorrido.

Al aumentar su valor, estas partículas incrementan su velocidad y su capacidad de exploración, recorriendo regiones más amplias del espacio. Paralelamente, las partículas **Buscadoras** reducen ligeramente su actividad, permitiendo que el sistema favorezca encuentros menos condicionados por la persecución directa.

Esta variable modifica el ritmo general del sistema sin imponer trayectorias específicas.

---

## 💰 Incentivo económico

Este parámetro controla la intensidad de la atracción que sienten las partículas **Enfocadas** hacia las entidades que representan **Intereses Económicos**.

Cuando el valor del deslizador es bajo, dichas entidades permanecen prácticamente ignoradas. A medida que el incentivo aumenta, las partículas enfocadas comienzan a modificar sus trayectorias para acercarse a ellas, reorganizando el comportamiento colectivo del sistema y reduciendo la frecuencia con la que ocurren encuentros espontáneos.

De esta manera, el sistema explora cómo un incentivo externo puede modificar las dinámicas existentes sin alterar directamente las reglas fundamentales de las demás poblaciones.

---

## Reflexión sobre las entradas

Ninguna de estas entradas controla directamente el resultado de la simulación. Cada una modifica únicamente uno o varios parámetros del sistema, como la intensidad de una fuerza, la velocidad de una población o la influencia de una entidad externa.

Las configuraciones que emergen después de estos cambios siguen siendo consecuencia de la interacción continua entre todas las partículas, conservando el carácter generativo del proyecto y permitiendo que cada ejecución produzca resultados diferentes sin perder su identidad conceptual.


# 5. Reglas

Las reglas describen el proceso mediante el cual el sistema actualiza el estado de cada partícula en cada frame. A partir de la repetición continua de estas reglas emergen todos los comportamientos observados durante la simulación, sin que exista una trayectoria predeterminada para ninguna partícula.

Cada actualización sigue la siguiente secuencia:

---

## 1. Identificación del entorno

Cada partícula analiza las entidades que se encuentran dentro de su radio de interacción. Únicamente las partículas cercanas pueden ejercer una influencia sobre su movimiento, haciendo que las relaciones dependan de la distancia entre ellas.

---

## 2. Consulta de la matriz de relaciones

Una vez identificadas las partículas vecinas, el sistema consulta la matriz de relaciones para determinar el tipo de interacción correspondiente.

Dependiendo del tipo de partícula y de la intensidad definida en la matriz, se calcula una fuerza de:

- Atracción.
- Repulsión.
- Indiferencia.

Estas fuerzas representan la intención de movimiento de cada entidad frente a las demás.

---

## 3. Aplicación de fuerzas externas

Después de calcular las relaciones entre partículas, el sistema incorpora la influencia de las variables modificables por el usuario.

Los deslizadores alteran parámetros como:

- Intensidad de la búsqueda.
- Miedo al rechazo.
- Desarrollo personal.
- Incentivo económico.

Estas variables no modifican directamente la posición de las partículas, sino la intensidad de las fuerzas que actúan sobre ellas.

---

## 4. Actualización del movimiento

La suma de todas las fuerzas genera una aceleración para cada partícula.

Posteriormente se actualizan:

- Velocidad.
- Dirección.
- Posición.

Antes de mover cada partícula se aplica un factor de fricción y un límite de velocidad máxima, evitando aceleraciones infinitas y manteniendo un comportamiento estable durante toda la simulación.

---

## 5. Generación de conexiones emergentes

Cuando dos partículas Enfocadas permanecen próximas durante un tiempo determinado sin haber existido una persecución directa entre ellas, el sistema interpreta este encuentro como una conexión.

Las conexiones no constituyen una entidad independiente, sino un comportamiento emergente que aparece únicamente cuando las condiciones del sistema lo permiten.

Estas conexiones son temporales y desaparecen después de algunos segundos, permitiendo que el sistema continúe evolucionando.

---

## 6. Repetición continua

El proceso se repite en cada frame de la simulación.

Como las posiciones cambian constantemente, también cambian las partículas que interactúan entre sí, generando nuevas configuraciones y comportamientos colectivos.

No existe un estado final ni una solución única. El sistema permanece en evolución permanente, permitiendo que las dinámicas de atracción, rechazo y encuentro continúen emergiendo de manera diferente en cada ejecución.

---

## Resultado esperado

La repetición constante de estas reglas permite que el comportamiento global del sistema no sea programado explícitamente, sino que emerja de la interacción local entre las partículas y de las modificaciones realizadas sobre sus parámetros.

De esta manera, fenómenos como el rechazo, la formación de conexiones espontáneas o la influencia de incentivos externos no son animaciones predefinidas, sino consecuencias naturales de las reglas que gobiernan el sistema.
