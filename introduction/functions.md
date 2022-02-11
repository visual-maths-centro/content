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

### Modelo IPO

### Parámetros

### Regreso de valores

### Las funciones `setup` y `draw`

### Funciones de primer grado
