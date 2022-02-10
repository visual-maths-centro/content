# Variables y tipos de datos

Una variable representa un dato que se debe recordar en un punto del código, para ser usado más adelante. Se guarda en la memoria de la computadora y se hace referencia a ese dato con un nombre. Entonces, una variable siempre es un VALOR + NOMBRE.

En una variable podemos guardar la localización de una figura, su color, su tamaño, etc.

### ¿Qué es una variable?

Una variable representa un dato que se debe recordar en un punto del código, para ser usado más adelante. Se guarda en la memoria de la computadora y se hace referencia a ese dato con un nombre. Entonces, una variable siempre es un VALOR + NOMBRE.

En una variable podemos guardar la localización de una figura, su color, su tamaño, etc.

### Declaración de variable

A la instrucción que usamos para decir: "¡Hey Javascript! Crea un espacio para guardar esta variable", se le llama declaración de variable y su sintaxis es:

```js
let nombre;
```

#### Ejemplos

```js
let myAge;
let x;
let debt;
let scorePlayer1;
let isRaining;
```

#### Reglas para los nombres

- Debe ser una sola palabra (sin espacios).
- Debe empezar con una letra MINÚSCULA.
- Puede llevar números y guión bajo.
- Si se desea emplear más de una palabra, las palabras siguientes deben de comenzar con una mayúscula (Camel case).
- No puede haber dos variables con un mismo nombre en un mismo alcance.

### Asignación de valores

Lo interesante en una variable es poderle asignar un valor y cambiarlo más adelante. Por esa razón se llaman variables. Para asignar un valor a una variable usamos la sintaxis:

```js
variable = valor;
```

Donde el símbolo `=` es el operador de asignación, que asigna el valor que está del lado derecho a la variable que aparece en el lado izquierdo.

### Tipos de datos

Así podemos guardar:

- Números enteros o con decimales (`3`, `10.23`).
- Cadenas de texto (se debe usar comillas simples `'texto'`).
- Valores booleanos (`true` o `false`).

#### Ejemplo de asignación:

```js
let myAge;
myAge = 29;

let myName;
myName = 'Diego';
```

### Declaración y Asignación

Cuando es es el primer valor que le asignamos a una variable, se puede declarar la variable junto con su valor inicial.

#### Ejemplo:

```js
let myAge = 29;
let myName = 'Diego';
```

### Consola

Una herramienta muy simple pero eficaz para verificar que nuestras variables tienen el valor correcto es imprimir su valor.

Para ello usaremos la sintaxis: `console.log(variable);`. Donde entre los paréntesis pondremos la variable a imprimir.

De hecho se puede imprimir cualquier tipo de mensaje.

#### Ejemplo

```js
let x = 130;
console.log(x);

console.log('Hola mundo');

console.log(x + 10);
```

### Asignación usando expresiones

También podemos asignar el resultado de una operación aritmética. Antes de asignar el valor, Javascript calculará el resultado de las operaciones. En caso de que la operación involucre alguna variable, primero se sustituye su valor y después se calcula.

#### Ejemplo:

```js
let widthRect = 110.9;
let heightRect = 20.1;
let areaRect = widthRect * heightRect;
```

Las operaciones aritméticas básicas, ordenadas de menor a mayor precedencia, son:

- Suma (`+`)
- Resta (`-`)
- Multiplicación (`*`)
- División (`/`)
- Agrupación (`()`)

### Uso de una variable

Antes de aprender variables, aprendiste a usar comandos de dibujo de p5.js como ellipse, donde usabas números como coordenadas y tamaños de una elipse.

Cuando usas un número fijo, decimos que ese es un valor _hard coded_, porque es un valor que nunca va a cambiar.

¿Qué tal que queremos que la elipse esté en una posición que dependa de otro dibujo?¿o que cambie con el tiempo?

Para eso, podemos usar una variable y sustituirla como parámetro en la llamada del comando de dibujo. Así, Javascript tomará el valor de la variable y lo usará para dibujar.

#### Ejemplo:

```js
ellipse(50, 300, 100, 300); // Valores hardcoded

let xPosition = 20;
ellipse(xPosition, 300, 100, 300); // Usando una variable
```

Lo interesante al hacer esto, es que podemos actualizar la variable como nosotros queramos (como al final del draw) y hacer lindas animaciones.

### Variables de sistema

p5.js ya tiene definida algunas variables que guardan valores muy útiles.
Algunas de ellas son:

- `width`: Guarda el ancho del canvas actual.
- `height`: Guarda el ancho del canvas actual.
- `mouseX`: Guarda la posición en x del mouse, se actualiza cada frame.
- `mouseY`: Guarda la posición en y del mouse, se actualiza cada frame.
- `mouseIsPressed`: Un valor booleano, si está presionado o no, un botón del mouse.
