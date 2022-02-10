# Fundamentos de la programación

En esta sección repasaremos los conocimientos que debes tener en
programación.

### ¿Qué es programar?

La idea central de programar es comunicar una serie de instrucciones a la computadora. Aunque estas instrucciones en realidad, pueden ser hechas por cualquier persona.

Estas instrucciones deben de ser ordenadas, finitas y claras para el que las vaya a ejecutar. Son una serie de pasos, al que llamamos **algoritmo**.

Los algoritmos son ideas que no dependen de cómo están escritos, pude ser en español. Programar es escribir algoritmos en un lenguaje de programación.

### ¿Qué es un lenguaje de programación?

Es un lenguaje formal en el que se escriben instrucciones. Esta definido por sintaxis y semántica.

La **sintaxis** define los símbolos y la forma correcta de usarlos para poder programar, es decir, define la forma. Es como la gramática en un lenguaje natural.

La **semántica** es el significado de los símbolos. Muchos lenguajes de programación comparten el significado con cambios mínimos en los símbolos, es por ello que la semántica es lo mas importante.

### Javascript y P5.js

_Javascript_ es un lenguaje de programación ampliamente usado en la web. De hecho, es el lenguaje que interpretan los navegadores para manejar las interacciones de todas las páginas web.

_P5.js_ es una biblioteca de Javascript que sirve para crear experiencias visuales y código creativo en la web. Esta inspirado en Processing.

### Lineas de código

Cada línea de código representa una instrucción en el programa, o bien modifica su flujo. Es importante que notes que las líneas están numeradas, esto ayuda para darnos una idea del orden de los pasos.

La mayoría de las instrucciones están encerradas en **bloques de código** delimitados por llaves: `{}`. También deben llevar un punto y coma (`;`) que indica que hemos terminado una instrucción.

### Comentarios

Podemos escribir líneas dentro de nuestro código cuyo propósito es ser leído por humanos y no por la computadora. Esto puede ser útil si queremos dejar notas indicando qué es lo que está queriendo hacer el programa, para referencia a otros programadores o para nuestro yo del futuro.

También es útil, pero no recomendable, usarlo para desactivar código.

Estas líneas deben comenzar con dos diagonales: `\\`.

#### Ejemplo

```js
// Esto es un comentario

let x = 0;
// x = 100;

// Calculando el area de un circulo de radio 30
let PI = 3.1416;
let radius = 30;
let area = PI * radius * radius;
```

Si se desea comentar un párrafo entero, se encierra entre `/*` y `*/`.

#### Ejemplo

```js
/*
 Esta es un comentario.
 Con mucho texto.
 Lorem ipsum
*/
```

### Principios de la programación

- [Variables](./variables.md)
- [Condicionales](./conditionals.md)
- [Iteraciones o ciclos](./loops.md)
- [Funciones](./functions.md)
