# Repeticiones (Ciclos o iteraciones)

Las computadoras nos hacen la vida más fácil realizando tareas tediosas para nosotros. Ellas son especialmente buenas para automatizar procesos que son repetitivos, con mucha rapidez y precisión a comparación de forma manual.

¿Qué tan rápido? Pueden hacer aproximadamente 3,600,000,000 de operaciones al segundo (3.6 GHz). Es decir, muy rápido.

Como programadores podemos sacar ventaja de esa rapidez aprendiendo como hacer que la computadora repita tareas o instrucciones.

### Estructura `while`

Supongamos que queremos llenar el canvas de líneas verticales como se muestra en la imagen.

<img src="../img/loops/lines.png" alt="Lineas" height="250"/>

Una forma de lograrlo sería con el código:

```js
let x = 20;
line(x, 0, x, height);

x = x + 20;
line(x, 0, x, height);

x = x + 20;
line(x, 0, x, height);

// Hasta llenar el canvas...
```

Pero esto obviamente es muy poco practico. Si cambiamos el tamaño del canvas, tendríamos que agregar o quitar código. O si queremos cambiar la separación entre las líneas, tendríamos que modificar mucho código.

En este código hay dos instrucciones que se repiten: la actualización de la variable `x` y el dibujo de la línea. Podemos resumir nuestras intenciones con las instrucciones:

> Mientras que la x no llegue al final del canvas, avanza x en 20 y dibuja una línea vertical.

La frase _"mientras que"_, establece que se debe repetir instrucciones hasta que se cumpla una condición. En este caso la condición es que `x` no llegue al final (`x < width`).

El diagrama de flujo que representa este pequeño algoritmo es:

<img src="../img/loops/while.svg" alt="while" height="400"/>

#### Sintaxis

La sintaxis para indicar repeticiones hasta que, o mientras que se cumpla una condición es:

```js
while (condition) {
  // Instrucciones a repetir
}
```
Aplicado a nuestro ejemplos de las líneas verticales:

```js
let x = 0;
while (x < width) {
  x = x + 20;
  line(x, 0, x, height);
}
```

El código completo lo puedes encontrar [aquí](https://codesandbox.io/s/while-lines-rv772).

A cada repetición que hace un ciclo, le llamamos **iteración**.

### Ciclos infinitos

Recordemos que una característica de los algoritmos es que sean finitos. Tenemos que tener cuidado, porque con los ciclos podemos romper esto.

Imaginemos que dibujando las líneas se nos olvida actualizar la variable `x`.

```js
let x = 0;
while (x < width) {
  line(x, 0, x, height);
}
```

La condición `x < width` **NUNCA** dejara de ser verdadera y por lo tanto la computadora no podrá salir del ciclo. Y quedaremos atrapados en un bucle sin fin y nuestras almas penaran en el purgatorio hasta la eternidad.

A esto se le conoce como **ciclo infinito** y es algo que deseamos evitar.

Los ciclos son una herramienta poderosa, y _"un gran poder conlleva una gran responsabilidad"_. Así que asegurate de que las condiciones en el ciclo vayan a ser falsas en algún momento.

### Estructura `for`

La mayoría de los ciclos tienen la forma: inicialización de una variable, una condición y la actualización de la variable.

Por ejemplo:

```js
// Iniciar una variable
let d = 100;

// Condición
while (d > 10) {
  ellipse(300, 300, d, d);

  // Actualización de la variable
  d = d - 10;
}
```

Para que sea más fácil la lectura de estos ciclos, JavaScript tiene la directiva `for`, que sirve para comprimir estos pasos en una sola línea.

#### Sintaxis

La sintaxis del `for` es:

```js
for (init; condition; update) {
  // Lineas a repetir
}
```

El diagrama de flujo sería:

<img src="../img/loops/for.svg" alt="for" height="520"/>

#### Ejemplo

El ejemplo de las líneas verticales usando `for`, quedaría:

```js
for (let x = 0; x < width; x += 20) {
  line(x, 0, x, height);
}
```

Puedes encontrar el ejemplo completo [aquí](https://codesandbox.io/s/for-lines-1ht8m).
