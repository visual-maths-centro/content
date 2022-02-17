# Álgebra

### Objetivo de la Unidad

Repasar los conceptos básicos del álgebra y usarla como herramienta para abstraer ideas visuales en operaciones numéricas como el manejo de rangos.

### ¿Que estudian las Matemáticas?

Las **Matemáticas** son una disciplina muy antigua, cuyas ideas han ido evolucionado a lo largo de la historia de la humanidad. Es quizá uno de los mayores logros intelectuales que como colectivo hemos conseguido.

<img src="../img/algebra/geometria.png" alt="Geometria" height="300"/>

Su trascendencia se debe a que nuestra naturaleza física está diseñada para detectar patrones y tener capacidad de abstracción. Pero sobre todo porque son muy prácticas y nos ayudan a sortear las multiples dificultades de este mundo caótico.

<img src="../img/algebra/fine.png" alt="This is Fine" height="300"/>

La primer necesidad humana que fue cubierta por las Matemáticas fue la necesidad de contar. Establecer una relación entre una cantidad física y una abstracta nos ayudo a distribuir y administrar bienes. Sin ello, no se hubieran podido crear sociedades avanzadas. De aquí surgió el concepto de **número**.

<img src="../img/algebra/quipu.png" alt="Quipu" height="300"/>

Mas adelante surgieron mas formas de abstraer patrones del mundo real y después se estudiaron mas a fondo.

> _"Las Matemáticas estudian, partiendo de axiomas y la lógica, las propiedades, relaciones y estructuras de entidades abstractas."_

### ¿Que es el álgebra?

Alrededor del año 820, en la ciudad de Bagdad, el matemático Al-Khwarizmi (en español Al-Juarismi) publicó un tratado llamado _Hisāb al-ŷabr wa'l muqābala_, que significa _Compendio de cálculo por compleción y comparación_.

<img src="../img/algebra/algebr.jpeg" alt="Algebra" height="350"/>

En este libro Al-Juarismi expone muchos métodos para resolver problemas de la vida cotidiana del imperio islámico de su época. Los problemas que resolvía se centraban en cálculos de cantidades de dinero, de bienes, de propiedades, etc.

De esta obra nace el término **álgebra**, y establece muchas ideas actuales de esta area.

Y lamentamos romper ilusiones y creencias, pero el señor de la portada de este libro ¡no es Baldor!. Es Al-Juarismi.

<img src="../img/algebra/Baldor.jpeg" alt="Baldor" height="400"/>

#### Abstracción

El proceso de _abstraer_ es capturar la **esencia** de un objeto vive en el mundo real o concreto. Es decir, queremos dejar de lado los detalles innecesarios y superfluos para describir una idea o concepto.

Usemos de ejemplo la descripción de una silla. Si yo busco la palabra "silla" en Google Imágenes, encontrare estos resultados.

<img src="../img/algebra/sillas.png" alt="Sillas" width="600"/>

Todas estas imágenes son ejemplos de sillas muy distintas y concretas. Lo importante para definir la idea "silla" son sus similitudes y su esencia.

Lo mismo pasa con las cantidades. El número 5, tiene muchas formas de ser representado con objetos concretos, pero la esencia es la cantidad.

Mas aún, el 1, 200, -20 son ejemplos concretos del concepto "número". Que podemos simbolizar con la letra "x".

#### Del lenguaje común a expresiones algebraicas

Una vez entendido que las letras pueden abstraer una cantidad, podemos crear expresiones simbólicas que representen relaciones de cantidades.

Imaginemos que voy al tianguis y veo que la verdura tiene un descuento del 30% de descuento. El kilo de limones esta en $20 pesos, por lo tanto el descuento si compro un kilo es:

<img src="https://latex.codecogs.com/svg.image?descuento&space;=&space;0.3&space;*&space;20&space;=&space;6" title="descuento = 0.3 * 20 = 6" />

Si yo generalizo el descuento para cualquier porcentaje y cualquier verdura puedo escribirlo como:

<img src="https://latex.codecogs.com/svg.image?d&space;=&space;p&space;*&space;x" title="d = p * x" />

Si d es el descuento, p es el porcentaje y x es el precio de la verdura.

Esta es una **expresión algebraica**. En ellas se usan símbolos para representar cantidades y operaciones. Los símbolos que mas comúnmente se usan son las letras: x, y, z para cantidades desconocidas o variables; y a, b, c para cantidades conocidas o constantes.

### Operaciones básicas y sus propiedades

A continuación revisaremos las operaciones básicas usadas en las expresiones algebraicas y sus propiedades.

#### Suma

La suma se usa para agregar cantidades. Visualmente, cuando hablamos de posiciones, está relacionada con "mover" o "empujar" un _offset_.

En matemáticas y en programación se usa el signo `+`.

#### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;&plus;&space;0&space;=&space;a" title="\inline a + 0 = a" />
2. _(Simetría)_ <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;&plus;&space;b&space;=&space;b&space;&plus;&space;a" title="\inline a + b = b + a" />
3. _(Asociatividad)_ <img src="https://latex.codecogs.com/svg.image?a&space;&plus;&space;(b&space;&plus;&space;c)&space;=&space;(a&space;&plus;&space;b)&space;&plus;&space;c" title="a + (b + c) = (a + b) + c" />
4. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?a&space;&plus;&space;c&space;=&space;b&space;&plus;&space;c" title="a + c = b + c" />.

#### Resta

La resta es usada para disminuir cantidades, pero también sirve es una medida para determinar que tan diferentes son dos cantidades. De ahí que también se llame "la diferencia".

Por ejemplo, el 8 esta a 1 de ser diferente del 9.

En matemáticas y en programación su símbolo es `-`.

#### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;0&space;=&space;a" title="\inline a - 0 = a" />
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;b&space;=&space;a&space;&plus;&space;(-b)" title="\inline a - b = a + (-b)" />
3. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;c&space;=&space;b&space;-&space;c" title="\inline a - c = b - c" />.

#### Multiplicación

La multiplicación esta relacionada con "escalar" una cantidad.

La notación de la multiplicación en matemáticas se simboliza omitiendo el símbolo, o con paréntesis: <img src="https://latex.codecogs.com/svg.image?\inline&space;2x" title="\inline 2x" /> o <img src="https://latex.codecogs.com/svg.image?\inline&space;a(b)(c)" title="\inline a(b)(c)" />.

En programación, se usa el asterisco `*`: `2 * x` o `a * b * c`.

### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a0&space;=&space;0" title="\inline a0 = 0" />.
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;a1&space;=&space;a" title="\inline a1 = a" />.
3. <img src="https://latex.codecogs.com/svg.image?\inline&space;ab&space;=&space;ba" title="\inline ab = ba" />.
4. <img src="https://latex.codecogs.com/svg.image?\inline&space;a(bc)&space;=&space;(ab)c" title="\inline a(bc) = (ab)c" />.
5. <img src="https://latex.codecogs.com/svg.image?\inline&space;a(b&space;&plus;&space;c)&space;=&space;ab&space;&plus;&space;ac" title="\inline a(b + c) = ab + ac" />.
6. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;ac&space;=&space;bc" title="\inline ac = bc" />.

#### División

#### Propiedades

Sean _a_, _b_, _c_ y _d_ cuatro números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{1}&space;=&space;a" title="\inline \frac{a}{1} = a" />.
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{a}&space;=&space;1" title="\inline \frac{a}{a} = 1" />.
3. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}&space;&plus;&space;\frac{c}{d}&space;=&space;\frac{ad&space;&plus;&space;bc}{bd}" title="\inline \frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}" />.
4. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}&space;-&space;\frac{c}{d}&space;=&space;\frac{ad&space;-&space;bc}{bd}" title="\inline \frac{a}{b} - \frac{c}{d} = \frac{ad - bc}{bd}" />.
5. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}\frac{c}{d}&space;=&space;\frac{ac}{bd}" title="\inline \frac{a}{b}\frac{c}{d} = \frac{ac}{bd}" />.
6. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{\frac{a}{b}}{\frac{c}{d}}&space;=&space;\frac{ad}{bc}" title="\inline \frac{\frac{a}{b}}{\frac{c}{d}} = \frac{ad}{bc}" />.
7. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{c}&space;=&space;\frac{b}{c}" title="\inline \frac{a}{c} = \frac{b}{c}" />.

### Ecuaciones de primer grado

### Rangos de números
