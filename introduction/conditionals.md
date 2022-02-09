# Condicionales

### Expresiones booleanas y proposiciones

En el estudio de la Lógica, a las oraciones que se les puede conceder el valor de falso o verdadero se le conoce como **proposiciones**.

En los ejemplos:

1. Tengo hambre.
2. ¡Viva la Revolución!
3. Esta lloviendo.
4. x = y + 2
5. 50 > 10

Las oraciones 1, 3 y 5 son proposiciones; mientras que 2, y 4 no lo son.

A las proposiciones también se les conoce como **expresiones booleanas**. Dado que el estudio de este tipo de expresiones y su relación con la computación fue hecha por _George Boole_.

A los valores _falso_ o _verdadero_ se les conoce como valores booleanos, y en Javascript los podemos guardar en variables como los valores `false` o `true`.

### Operadores de comparación

Las expresiones booleanas más comunes que escribiremos en código son comparaciones de valores. A continuación ponemos los operadores de comparación que se usan en Javascript:

- Mayor que (`>`)
- Mayor que (`<`)
- Mayor o igual que (`>=`)
- Menor o igual que (`<=`)
- Es igual que (`===`)\*
- Es diferente que (`!==`)\*

\* Javascript es un lenguaje algo rarito, y se sugiere usar estos operadores a diferencia de `==` y `!=`.

Estos operadores se pueden combinar igual usando la asociación (), como sucede con los operadores aritméticos.

### Condicionales

En la mayoría de los programas (y algoritmos) se necesitan tomar decisiones. Se decide si se debe ejecutar o no ciertas instrucciones en base al estado de las variables o al contexto. Es decir, ciertos pasos del algoritmos están condicionados.

Las condiciones es algo con lo que estamos acostumbrados a lidiar todos los días de nuestra vida. Tanto en la vida real, como en los programas, las condicionales tienen la misma forma: Si es cierto que _A_, entonces sucede _B_.

Por ejemplo:

- Si tengo hambre entonces como una hamburguesa. Si no tengo hambre, pero tengo sed, entonces bebo agua.
- Si estudio, seguro aprobaré la materia.
- Si el usuario da click sobre la nave y no ha perdido, entonces dispara.

### Condicional simple

Una condicional simple tiene la forma que hemos discutido anteriormente:

> Si es cierto que _A_, entonces ejecuta _B_.

Donde _A_ es la **condición** y siempre es una expresión booleana. Mientras que _B_ es el bloque de líneas de código que se ejecuta cuando _A_ es verdadero.

Si vemos esto como un diagrama de flujo:

<img src="../img/conditionals/simple_conditional.svg" alt="Simple conditional" height="400"/>

#### Sintaxis

En sintaxis de Javascript se escribiría como:

```js
if (A) {
  // B
}
```

#### Ejemplos

```js
let a = 10;
if (a > 3) {
  console.log('La variable a es mayor que 3');
}

let b = 20;
if (a + 10 === b) {
  console.log('Es cierto');
}

if (b < a>) {
  console.log('b es menor que a');
}
```

```js
let x = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(255);

  ellipse(x, 200, 20, 20);

  x = x + 4;

  // Si x es mayor que el ancho
  if (x > width) {
    // x regresa al cero
    x = 0;
  }
}
```

Puedes ver el resultado de este ejemplo [aquí](https://codesandbox.io/s/conditionals-1-ieeu4?file=/sketch.js).

### Condicional completa

La condicional simple solo ejecuta el código que hayamos puesto entre las llaves si la condición es cierta. Pero que tal que queremos también cubrir el caso en el que sea falsa.

Para eso usaremos la **condicional completa**, que se lee de la siguiente forma:

> Si es cierto que _A_, entonces ejecuta _B_. En otro caso, ejecuta _C_.

Donde _C_ es el bloque de instrucciones que se ejecutará si _A_ es falso.

Si vemos esto como un diagrama de flujo:

<img src="../img/conditionals/conditional_complete.svg" alt="Simple conditional" height="400" />

#### Sintaxis

Para contemplar el caso falso, usaremos la sintaxis `else`, que significa en inglés _"en otro caso"_ o _"de otra manera"_. La palabra `else` se debe de poner después de cerrar el bloque del `if`, e inaugura un nuevo bloque.

```js
if (A) {
  // B
} else {
  // C
}
```

#### Ejemplos

```js
let myName = 'Diego';

if (myName === 'Ana') {
  console.log('Te llamas Ana');
} else {
  console.log('No te llamas Ana');
}
```

```js
let x = 0;

function setup() {
  createCanvas(600, 600);
  noStroke();
}

function draw() {
  background(220);

  // Si x es menor que la mitad de la pantalla
  if (x < width * 0.5) {
    fill(255, 0, 0); // Entonces dibuja de rojo
  } else {
    fill(0, 0, 255); // En otro caso dibuja de azul
  }

  ellipse(x, 300, 20, 20);

  x = x + 2;

  if (x > width) {
    x = 0;
  }
}
```

Puedes ver el resultado de este ejemplo [aquí](https://codesandbox.io/s/conditional-complete-06qt6?file=/sketch.js).

### Condicional múltiple

Supongamos que necesitamos analizar mas de una condicional. Es decir, si una condicional falla, queremos evaluar otra. Podemos pensar que "encadenamos" las condicionales.

Lógicas que tienen la siguiente forma:

> Si es cierto que _A_, entonces ejecuta _B_. Si no, pero pasa _C_, ejecuta _D_.

A esto lo llamamos **condicional múltiple**, y podemos observalo en el siguiente diagrama de flujo.

<img src="../img/conditionals/multiple_conditional.svg" alt="Multiple conditional" height="550" />

#### Sintaxis

Para hacer las demás condicionales usamos la palabra `else if`, seguida de otra condicional:

```js
if (A) {
  // B
} else if (C) {
  // D
}
```

El segundo `if` actúa como el primero, por lo que podemos añadir un `else` para que quede cubierto el caso en el que _C_ sea falso.

```js
if (A) {
  // B
} else if (C) {
  // D
} else {
  // E
}
```

El diagrama de flujo de este último ejemplo es:

<img src="../img/conditionals/multiple_conditional_b.svg" alt="Multiple conditional" height="550" />

La condicional múltiple permite evaluar muchos posibles valores o casos.

#### Ejemplos

```js
let myAge = 20;

if (myAge >= 21) {
  console.log('You can drink');
} else if (myAge >= 16) {
  console.log('You can drive');
}
```

```js
function setup() {
  createCanvas(600, 600);
  rectMode(CENTER);
}

function draw() {
  background(200);

  stroke(0);
  line(200, 0, 200, height);
  line(400, 0, 400, height);

  noStroke();

  // Si el mouseX esta en el primer tercio
  if (mouseX <= 200) {
    fill(255, 0, 0);
    rect(300, 300, 150, 150);
  }
  // Si el mouseX esta en el segundo tercio
  else if (mouseX <= 400) {
    fill(23, 125, 21);
    ellipse(300, 300, 150, 150);
  }
  // El mouseX esta en el tercer cuadrante (porque no esta en el 1ero ni en el 2do)
  else {
    fill(0, 0, 255);
    triangle(300, 225, 375, 375, 225, 375);
  }
}
```

Puedes ver el resultado de este ejemplo [aquí](https://codesandbox.io/s/multiple-conditional-vzlfo?file=/sketch.js).
