# Operaciones básicas y sus propiedades

A continuación revisaremos las operaciones básicas usadas en las expresiones algebraicas y sus propiedades.

### Suma

La suma se usa para agregar cantidades. También está relacionada con "mover" o "empujar" un _offset_.

En matemáticas y en programación se usa el signo _+_.

https://user-images.githubusercontent.com/2686914/154769575-46f3157b-907c-482b-b1ac-cd173279b88e.mp4

En el caso de un rango de números que están entre _a_ y _b_, al sumar una cantidad, estamos "recorriendo" todos los números del rango.

https://user-images.githubusercontent.com/2686914/154863728-8e993a82-b189-4613-83a9-c78c0d220523.mp4

#### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;&plus;&space;0&space;=&space;a" title="\inline a + 0 = a" />
2. _(Simetría)_ <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;&plus;&space;b&space;=&space;b&space;&plus;&space;a" title="\inline a + b = b + a" />
3. _(Asociatividad)_ <img src="https://latex.codecogs.com/svg.image?a&space;&plus;&space;(b&space;&plus;&space;c)&space;=&space;(a&space;&plus;&space;b)&space;&plus;&space;c" title="a + (b + c) = (a + b) + c" />
4. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?a&space;&plus;&space;c&space;=&space;b&space;&plus;&space;c" title="a + c = b + c" />.

### Resta

La resta es usada para disminuir cantidades, pero también sirve es una medida para determinar que tan diferentes son dos cantidades. De ahí que también se llame "la diferencia".

En matemáticas y en programación su símbolo es _-_.

Igual que la suma, visualmente lo podemos relacionar con mover, o empujar pero en el sentido contrario.

Con la resta, podemos determinar la longitud de un rango de números.

<img src="../img/algebra/len-range.png" width="85%"/>

#### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;0&space;=&space;a" title="\inline a - 0 = a" />
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;b&space;=&space;a&space;&plus;&space;(-b)" title="\inline a - b = a + (-b)" />
3. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;a&space;-&space;c&space;=&space;b&space;-&space;c" title="\inline a - c = b - c" />.

### Multiplicación

La multiplicación esta relacionada con "escalar" una cantidad, puede ser que ampliemos la cantidad, o la reduzcamos.

La notación de la multiplicación en matemáticas se simboliza omitiendo el símbolo, o con paréntesis: <img src="https://latex.codecogs.com/svg.image?\inline&space;2x" title="\inline 2x" /> o <img src="https://latex.codecogs.com/svg.image?\inline&space;a(b)(c)" title="\inline a(b)(c)" />. Mientras que en programación, se usa el asterisco `*`: `2 * x` o `a * b * c`.

Cuando multiplicamos un rango, lo podemos ampliar o reducir por un factor.

https://user-images.githubusercontent.com/2686914/155642053-bef7ceb6-d062-417e-93d2-ccad58027aff.mp4

#### Propiedades

Sean _a_, _b_ y _c_ tres números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;a0&space;=&space;0" title="\inline a0 = 0" />.
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;a1&space;=&space;a" title="\inline a1 = a" />.
3. <img src="https://latex.codecogs.com/svg.image?\inline&space;ab&space;=&space;ba" title="\inline ab = ba" />.
4. <img src="https://latex.codecogs.com/svg.image?\inline&space;a(bc)&space;=&space;(ab)c" title="\inline a(bc) = (ab)c" />.
5. <img src="https://latex.codecogs.com/svg.image?\inline&space;a(b&space;&plus;&space;c)&space;=&space;ab&space;&plus;&space;ac" title="\inline a(b + c) = ab + ac" />.
6. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;ac&space;=&space;bc" title="\inline ac = bc" />.

### División

El significado clásico de la división es la de "repartir" o "distribuir" una cantidad sobre otra. También se le conoce como la operación inversa a la multiplicación.

En matemáticas usamos la notación <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}&space;" title="\inline \frac{a}{b}" />, mientras que en código, se usa `/`: `a / b`.

A la cantidad a repartir se le conoce como numerador, y a la cantidad entre la que se reparte es el denominador.

El denominador NUNCA puede ser _0_.

#### Propiedades

Sean _a_, _b_, _c_ y _d_ cuatro números cualesquiera.

1. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{1}&space;=&space;a" title="\inline \frac{a}{1} = a" />.
2. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{a}&space;=&space;1" title="\inline \frac{a}{a} = 1" />.
3. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}&space;&plus;&space;\frac{c}{d}&space;=&space;\frac{ad&space;&plus;&space;bc}{bd}" title="\inline \frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}" />.
4. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}&space;-&space;\frac{c}{d}&space;=&space;\frac{ad&space;-&space;bc}{bd}" title="\inline \frac{a}{b} - \frac{c}{d} = \frac{ad - bc}{bd}" />.
5. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{b}\frac{c}{d}&space;=&space;\frac{ac}{bd}" title="\inline \frac{a}{b}\frac{c}{d} = \frac{ac}{bd}" />.
6. <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{\frac{a}{b}}{\frac{c}{d}}&space;=&space;\frac{ad}{bc}" title="\inline \frac{\frac{a}{b}}{\frac{c}{d}} = \frac{ad}{bc}" />.
7. Si <img src="https://latex.codecogs.com/svg.image?a&space;=&space;b" title="a = b" />, entonces <img src="https://latex.codecogs.com/svg.image?\inline&space;\frac{a}{c}&space;=&space;\frac{b}{c}" title="\inline \frac{a}{c} = \frac{b}{c}" />.
