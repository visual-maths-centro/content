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

### Variables y tipos de datos

Una variable representa un dato que se debe recordar en un punto del código, para ser usado más adelante. Se guarda en la memoria de la computadora y se hace referencia a ese dato con un nombre. Entonces, una variable siempre es un VALOR + NOMBRE.

En una variable podemos guardar la localización de una figura, su color, su tamaño, etc.

¿Qué es una variable?
Una variable representa un dato que se debe recordar en un punto del código, para ser usado más adelante. Se guarda en la memoria de la computadora y se hace referencia a ese dato con un nombre. Entonces, una variable siempre es un VALOR + NOMBRE.

En una variable podemos guardar la localización de una figura, su color, su tamaño, etc.

Declaración de variable
A la instrucción que usamos para decir: "¡Hey amigo Processing! Créa un espacio para guardar esta variable", se le llama declaración de variable y su sintaxis es:

let nombre;
Podemos guardar

Números enteros o con decimales.
Cadenas de texto.
Valores booleanos.
Ejemplos de declaración de variable:

let myAge;
let x;
let debt;
let scorePlayer1;
let isRainning;
Los nombres de variables deben seguir las siguientes reglas:

Debe ser una sola palabra (sin espacios).
Debe empezar con una letra MINUSCULA.
Puede llevar números y guión bajo.
Si se desea emplear más de una palabra, las palabras siguientes deben de comenzar con una mayúscula (Camel case).
No puede haber dos variables con un mismo nombre en un mismo alcance.
Asignación de valores
Lo interesante en una variable es poderle asignar un valor y cambiarlo más adelante. Por esa razón se llaman variables. Para asignar un valor a una variable usamos la sintaxis: variable = valor;. Donde el símbolo = es el operador de asignación, que asigna el valor que está del lado derecho a la variable que aparece en el lado izquierdo.

Ejemplo:

let myAge;
myAge = 29;
Cuando es es el primer valor que le asignamos a una variable, se puede declarar la variable junto con su valor inicial. Ejemplo:

let myAge = 29;
También podemos asignar el resultado de una operación aritmética. Antes de asignar el valor, Processing calculará el resultado de las operaciones. En caso de que la operación involucre alguna variable, primero se sustituye su valor y después se calcula. Ejemplo:

let widthRect = 110.9;
let heightRect = 20.10;
let areaRect = widthRect \* heightRect;
Las operaciones aritméticas básicas, ordenadas de menor a mayor precedencia, son:

Suma (+)
Resta (-)
Multiplicación (\*)
División (/)
Agrupación (/)
Uso de una variable
Antes de aprender variables, aprendiste a usar comandos de dibujo de p5.js como ellipse, donde usabas números como coordenadas y tamaños de una elipse. Cuando usas un número fijo, decimos que ese es un valor hard coded, porque es un valor que nunca va a cambiar. ¿Qué tal que queremos que la elipse esté en una posición que dependa de otro dibujo? ¿o que cambie con el tiempo?

Para eso, podemos usar una variable y sustituirla como parámetro en la llamada del comando de dibujo. Así, Processing tomará el valor de la variable y lo usará para dibujar. Ejemplo:

ellipse(50, 300, 100, 300); // Valores hardcoded

let xPosition = 20;
ellipse(xPosition, 300, 100, 300); // Usando una variable
Lo interesante al hacer esto, es que podemos actualizar la variable como nosotros queramos (como al final del draw) y hacer lindas animaciones.

Variables de sistema
Processing ya tiene definida algunas variables que guardan valores muy útiles. Algunas de ellas son:

width: Guarda el ancho del canvas actual.
height: Guarda el ancho del canvas actual.
mouseX: Guarda la posición en x del mouse, se actualiza cada frame.
mouseY: Guarda la posición en y del mouse, se actualiza cada frame.
mouseIsPressed: Un valor booleano, si está presionado o no, un botón del mouse.

### Condicionales

### Repeticiones (iteraciones)

### Funciones
