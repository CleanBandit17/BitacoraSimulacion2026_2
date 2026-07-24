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

### Código de P5.js
```js
let particles = [];
let influence = 0;

function setup() {
  createCanvas(540, 960);
  background(5);

  for (let i = 0; i < 180; i++) {
    particles.push(new Particle());
  }
}

function draw() {

  // No limpiamos completamente el fondo
  // para crear estelas
  background(5, 12);

  influence = map(
    dist(mouseX, mouseY, width / 2, height / 2),
    0,
    width / 2,
    1,
    0
  );

  influence = constrain(influence, 0, 1);

  drawConnections();

  for (let p of particles) {
    p.update();
    p.display();
  }

  drawVisitor();
}

function drawConnections() {

  // Cuando la influencia es muy alta
  // dejamos de dibujar conexiones.
  if (influence > 0.75) return;

  strokeWeight(1);

  for (let i = 0; i < particles.length; i++) {

    for (let j = i + 1; j < particles.length; j++) {

      let d = dist(
        particles[i].pos.x,
        particles[i].pos.y,
        particles[j].pos.x,
        particles[j].pos.y
      );

      if (d < 40) {

        let alpha = map(d, 0, 40, 80, 0);

        stroke(255, alpha);

        line(
          particles[i].pos.x,
          particles[i].pos.y,
          particles[j].pos.x,
          particles[j].pos.y
        );
      }
    }
  }
}

function drawVisitor(){

  noFill();

  stroke(255,0,0,120);

  strokeWeight(2);

  circle(mouseX,mouseY,60+influence*120);

}

class Particle {

  constructor() {

    this.pos = createVector(
      randomGaussian(width / 2, width / 8),
      randomGaussian(height / 2, height / 8)
    );

    this.previous = this.pos.copy();

    this.offset = random(1000);

    this.size = random(2, 5);
  }

  update() {

    this.previous = this.pos.copy();

    // POSIBILIDAD
    let angle = random(TWO_PI);
    let randomStep = p5.Vector.fromAngle(angle);

    // TENDENCIA
    let tendency = createVector(0.25, 0);
    randomStep.add(tendency);

    // NORMALIDAD + PERLIN
    let n = noise(this.offset, frameCount * 0.003);

    let perlinAngle = map(n, 0, 1, -PI, PI);

    let perlin = p5.Vector.fromAngle(perlinAngle);

    let velocity = p5.Vector.add(randomStep, perlin);

    velocity.setMag(1.4);

    // EXCEPCIÓN
    let levyProbability = 0.002 + influence * 0.03;

    if (random() < levyProbability) {

      let jump = random(70, 180);

      let dir = p5.Vector.random2D();

      dir.mult(jump);

      this.pos.add(dir);
    }

    // INFLUENCIA
    if (influence > 0) {

      let mouse = createVector(mouseX, mouseY);

      let attraction = p5.Vector.sub(mouse, this.pos);

      attraction.normalize();

      attraction.mult(influence * 1.8);

      velocity.add(attraction);
    }

    this.pos.add(velocity);

    this.offset += 0.01;

    // BORDES
    if (this.pos.x < 0) this.pos.x = width;
    if (this.pos.x > width) this.pos.x = 0;
    if (this.pos.y < 0) this.pos.y = height;
    if (this.pos.y > height) this.pos.y = 0;
  }

  display() {

  let dMouse = dist(this.pos.x, this.pos.y, mouseX, mouseY);

  // Color dinámico
  let r = 255;
  let g = map(dMouse,0,180,40,255);
  let b = map(dMouse,0,180,40,255);

  g = constrain(g,40,255);
  b = constrain(b,40,255);

  // Cuando la influencia es alta,
  // todas se vuelven rojas.
  if(influence > 0.75){

    r = 255;
    g = 40;
    b = 40;

  }

  // Estela
  stroke(r,g,b,50);
  strokeWeight(1.5);

  line(
    this.previous.x,
    this.previous.y,
    this.pos.x,
    this.pos.y
  );

  // Halo
  noStroke();
  fill(r,g,b,50);
  circle(
    this.pos.x,
    this.pos.y,
    this.size*3
  );

  // Núcleo
  fill(r,g,b,220);
  circle(
    this.pos.x,
    this.pos.y,
    this.size
  );

}
}
```
