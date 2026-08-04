
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

# 2. Entidades

| Entidad | Representación | Comportamiento principal |
|----------|----------------|--------------------------|
| ❤️ Buscadores | Búsqueda activa del afecto | Persiguen constantemente a las partículas enfocadas, generando dinámicas de atracción y rechazo. |
| 🌱 Enfocados | Desarrollo personal | Recorren el espacio de forma autónoma y favorecen la aparición de encuentros espontáneos. |
| 💰 Intereses Económicos | Incentivos externos | Permanecen pasivos y atraen a las partículas enfocadas cuando aumenta el parámetro de incentivo económico. |

> **Nota de diseño:** Las conexiones no son una entidad independiente, sino un comportamiento emergente del sistema. Su aparición depende exclusivamente de las reglas de interacción entre las partículas y de las condiciones que se generan durante la simulación.
