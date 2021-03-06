# Funciones

A medida que un programa crece y realiza muchas tareas, se vuelve necesario tener una forma eficiente de organizar el código. Aunque cada lenguaje de programación tiene sus formas de hacerlo, en casi todas, la unidad mínima de organización son las _funciones_.

Una **función** es un bloque de código aislado que se utiliza para realizar una sola tarea.

En algunos lenguajes puede ser llamado método, subrutina o subprograma.

### Declaración y uso

Para declarar una función en JavaScript se usa la sintaxis:

```js
function functionName () {
  // Código de la función
}
```

El nombre debe seguir las mismas reglas que el nombre de una variable.

Una vez definida la función, se puede usar poniendo su nombre seguido de paréntesis:

```js
functionName();
```

Al hecho de usar una función, también se le dice _invocar_ o _llamar_ a una función.

#### Ejemplo

```js
function draw() {
  background(220);

  randomBlackCircle();
  randomBlackCircle();
  randomBlackCircle();
}

function randomBlackCircle() {
  let diameter = random(30, 60);
  fill(0);
  noStroke();
  ellipse(random(width), random(height), diameter, diameter);
}
```

Este ejemplo lo puedes encontrar [aquí](https://codesandbox.io/s/black-circles-70ld2).

### Propiedades de una función

Las funciones tienen tres principales particularidades: _modularidad_, _abstracción_ y _reusabilidad_.

* **Modularidad**

  Las funciones permiten descomponer y separar la totalidad de un programa en pequeñas porciones mas simples. Al concentrarnos en resolver y programar una sola tarea reducimos la complejidad, y limitamos los errores.

  Una vez que nos aseguramos que las pequeñas partes funcionan, se unen y combinan para crear tareas mas complejas.

* **Abstracción** 

  Como consecuencia de la modularidad añadimos capas de abstracción a nuestro código. Al delegar la implementación de cada tarea a su función, nos dejamos de preocupar por los detalles específicos y solo nos preocupamos por como usarlos.

  En el ejemplo de los círculos negros, solo mandamos a llamar `randomBlackCircle` y nos olvidamos de cómo esta implementado. Solo nos interesa saber que dibujar un circulo negro aleatorio.

* **Reusabilidad**

  Una vez definida una función se puede usar tantas veces como uno quiera. Esto es muy útil pues evita que repitamos código que hace lo mismo una y otra vez.

  Existe un principio en la programación: _DRY (Don't repeat yourself)_.

### Modelo IPO

Las funciones siguen el modelo IPO: _Input, Process, Output_.

<img src="../img/functions/ipo.svg" alt="Lineas" height="250"/>

Son como cajas que reciben, o no, datos de entrada (input). Dentro ejecutan instrucciones (process). Y regresan, o no, datos de salida (output).

### Parámetros

A los datos de entrada que recibe una función los llamamos **parámetros**.

La sintaxis para aceptar parámetros en una función es la siguiente:

```js
function name (param1, param2, ..., paramN) {
  // Código de la función
}
```

Los parámetros son como variables cuyo valor es dado cuando se invoca a la función. Estos valores se conocen como **argumentos**.

Los argumentos se asignan a los parámetros en el orden que aparecen.

<img src="../img/functions/params-args.svg" alt="Lineas" height="200"/>

#### Ejemplo

```js
let size = 100;

function eye(x, y, eyeSize) {
  noStroke();

  fill(255);
  ellipse(x, y, eyeSize, eyeSize);

  fill(0);
  ellipse(x + eyeSize * 0.25, y, eyeSize * 0.5, eyeSize * 0.5);

  fill(255);
  ellipse(x + eyeSize * 0.4, y - eyeSize * 0.1, eyeSize * 0.1, eyeSize * 0.1);
}

function draw () {
  background(200);

  eye(300, 400, 100);
  eye(550, 400, size);
  eye(mouseX, mouseY, 75);
}
```

Puedes encontrar el ejemplo completo [aquí](https://codesandbox.io/s/eyes-function-jkowc).

### Regreso de valores

Para completar el modelo IPO, hace falta aprender como una función regresa un valor. Son equivalentes las frases: _"valor de regreso"_ y _"valor de salida"_.

Para regresar un valor usamos la palabra `return`.

```js
function name(args) {
  // Código de la función

  return value;
}
```

Podemos regresar una valor literal como `return 10;`. O podemos regresar el valore de una variable: `return variable;`.

#### Ejemplo

```js
// Función que regresa el mínimo de dos números
function min(a, b) {
  if (a < b) {
    return a;
  }

  return b;
}

// Función que convierte el código de país a su nombre
function countryName (countryCode) {
  if (countryCode === 'MX') {
    return 'Mexico';
  } else if (countryCode === 'US') {
    return 'United States';
  }

  return 'Unknown';
}
```

#### Algunas notas

* La instrucción `return` será la ultima en ejecutarse de la función.
* Si hay más líneas debajo de `return`, estas no se ejecutarán.
* Una función puede no regresar ningún valor. En cuyo caso se puede usar `return` solo.

#### Ejemplo

```js
function draw() {
  if (!mouseIsPressed) {
    return;
  }

  let x = getGridX();
  let y = getGridY();

  noStroke();
  fill(random(130, 200), 90, 60);
  circle(x, y, 20);
}

function getGridX() {
  let stepX = width / n;
  return floor(mouseX / stepX) * stepX;
}

function getGridY() {
  let stepY = width / n;
  return floor(mouseY / stepY) * stepY;
}
```

Puedes ver el ejemplo completo [aquí](https://codesandbox.io/s/grid-dots-qfwvz?file=/sketch.js).

### Funciones como valores

JavaScript es un lenguaje muy flexible (a veces es bueno, a veces no tanto). Una de las cosas muy buenas que tiene es que las funciones son tratadas como otro _tipo de dato_.
Es decir, pueden ser:

* Asignadas a una variable.
* Pasadas como un argumento a otra función.
* Regresadas por una función.

Por lo tanto, la siguiente expresión es valida en JavaScript:

```js
let sayHello = function () {
  console.log("hello world");
};

sayHello();
```

En este ejemplo, asignamos a una variable una función. Cuando una función no tiene nombre decimos que es **anónima**.

#### Ejemplo

```js
function draw() {
  background(220);

  drawOnMouse(drawSquare);
  drawOnMouse(drawCircle);
  drawOnMouse(function () {
    fill(random(255));
    circle(0, 0, random(75, 100));
  });
}

function drawOnMouse(drawFunction) {
  push();
  translate(mouseX, mouseY);
  drawFunction();
  pop();
}

function drawSquare() {
  rectMode(CENTER);
  fill(20, 10, 255);
  square(0, 0, 200);
}

function drawCircle() {
  fill(255, 0, 0);
  circle(0, 0, 175);
}
```

En este ejemplo tenemos la función `drawOnMouse` que recibe una función como argumento. Y en `draw`, la invocamos con dos funciones definidas y con una función anónima como argumentos.

El ejemplo completo lo puedes encontrar [aquí](https://codesandbox.io/s/first-class-fn-htshi).
