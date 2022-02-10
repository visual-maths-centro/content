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


### Dobles iteraciones
