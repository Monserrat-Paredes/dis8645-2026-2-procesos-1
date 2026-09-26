# sesion-06a

## apuntes sesión

Estuve enferma y no pude ir a esta clase 😭 así que me puse a buscar en los apuntes y materiales de la sesión jijiji para no perderme tanto y entender más o menos qué habían visto.

# Apuntes sesión

## Variables y tipos de datos

Partimos hablando de los **tipos de datos**, que básicamente sirven para decirle al computador **qué tipo de información queremos guardar y cuánto espacio necesita para hacerlo**.

Se explicó con una metáfora del súper:

Si vas al súper y compras un chicle, perfectamente puedes llevártelo en el bolsillo. Pero si compras una tabla de madera de tres metros, claramente necesitas una camioneta o un flete.

Ahora, ¿podrías contratar un flete solamente para llevarte el chicle? Sí, pero sería totalmente innecesario.

Con los datos pasa algo parecido. Tenemos que elegir un tipo de dato que tenga sentido para lo que queremos guardar, porque usar uno mucho más grande de lo necesario también significa ocupar memoria innecesariamente.

### `int`

`int` es un **tipo de dato para guardar números enteros**, o sea, números sin decimales.

Puede guardar números positivos, negativos y también el cero.

Por ejemplo:

```cpp
int edad = 23;
```

Acá:

* `int` dice qué tipo de dato vamos a guardar.
* `edad` es el nombre de la variable.
* `23` es el valor que tiene esa variable.

Entonces en realidad `int` no es la variable, sino que es **el tipo de dato de la variable**.

También existe `uint`, que significa *unsigned integer*. La diferencia es que no utiliza números negativos, por lo que parte desde el cero y puede aprovechar ese espacio para guardar números positivos más grandes.

Por ejemplo, tendría sentido usarlo para algo que sabemos que nunca va a ser negativo, como una cantidad de objetos.

La idea nuevamente es ocupar **el tipo de dato que realmente necesitamos** y no pedirle al computador más memoria de la necesaria.

### `bool`

`bool` es un tipo de dato muchísimo más simple.

Se comparó con **ese bolsillo mini que está dentro del bolsillo del jeans** JAJJA.

Sirve cuando solamente necesitamos guardar **dos posibilidades**:

* verdadero → `true`
* falso → `false`

Internamente podemos pensarlo como `1` y `0`.

Por ejemplo:

```cpp
bool hambre = true;
bool durmiendo = false;
```

En este caso no necesitamos guardar números gigantes ni palabras, solamente necesitamos saber si algo **está ocurriendo o no está ocurriendo**.

### `char`

`char` sirve para guardar **un solo carácter**.

Por ejemplo:

```cpp
char letra = 'A';
```

Puede ser una letra, un número escrito como carácter o algún símbolo.

La diferencia importante es que guarda **un carácter individual**, no una palabra completa.

# Datos, variables y funciones

Después empezamos a relacionar esto con los objetos y las clases.

Una forma bastante fácil de entenderlo es pensar que una cosa puede tener:

* **datos / variables / atributos** → cosas que la describen o información que tiene.
* **funciones / métodos** → acciones que esa cosa puede realizar.

Los métodos normalmente los reconocemos porque aparecen con `()`.

También vimos que, por convención, cuando escribimos el nombre de una **clase**, este suele comenzar con mayúscula.

Para entenderlo hicimos ejemplos con personas.

### Matías

Podríamos imaginar una clase o un objeto que represente a Matías.

Sus **atributos** serían características que tiene.

Por ejemplo:

* Qué tan piti es.
* Qué tanto le cuesta pronunciar ciertas palabras.

Si quisiéramos representar algo como "qué tan piti", podríamos utilizar un `float`, porque podría expresarse como un porcentaje y necesitar decimales.

Después estarían los **métodos**, que serían cosas que Matías puede hacer.

Por ejemplo:

```cpp
ponerseLentes();
```

La diferencia entonces sería:

**atributo:** información sobre Matías.
**método:** algo que Matías hace.


### Mi ejemplo

Para entenderlo mejor:

Mis **atributos** podrían ser:

* Soy diseñadora publicitaria.
* Tengo el pelo ondulado, aunque a veces se pone medio mañoso y parece más enredado que ondulado.
* Cumplo años en diciembre.

Por ejemplo, si quisiéramos guardar **qué tan ondulado está mi pelo ese día**, podríamos usar un `float`, porque podría expresarse como un porcentaje y no siempre sería exactamente igual.

Un día podría ser:

```cpp
float peloOndulado = 90.0;
```

y otro día:

```cpp
float peloOndulado = 45.0;
```

Dependiendo de si cooperó o decidió hacer lo que quería ese día.

Después estarían mis **métodos**, que serían acciones que hago:

```cpp
irATrabajar();
leerEnCelular();
irAUniversidad();
```

Entonces:

**atributos** → cosas que me describen o información sobre mí.
**métodos** → cosas que hago.

Esto me ayuda a entender que cuando programamos un objeto **no tenemos que describirlo absolutamente entero**, sino solamente las características y acciones que sean relevantes para lo que estamos tratando de representar.

# Clases e herencia

Después vimos las **clases** y apareció el concepto de **herencia**.

Una clase sería como una especie de **modelo o definición general** que establece qué características y comportamientos tienen ciertos objetos.

Por ejemplo, podríamos tener una clase:

```cpp
class Perrite {
    bool hambre = true;
    bool durmiendo = true;

    comer();
    dormir();
}
```

Esta clase nos está diciendo que los objetos que sean `Perrite` pueden tener ciertos atributos y realizar ciertas acciones.

Después podríamos crear una clase más específica, como:

```cpp
class Poodle
```

Un poodle sigue siendo un perrito, por lo tanto no tendría mucho sentido volver a escribir desde cero todas las cosas que ya sabemos que puede tener un `Perrite`.

Ahí aparece la **herencia**.

Podemos hacer que `Poodle` herede características de `Perrite`.

Entonces podríamos pensar algo así:

```cpp
class Poodle : public Perrite {
    ladrar();
}
```

Esto significa que `Poodle` puede utilizar las características y métodos que ya existen en `Perrite`, pero además puede agregar cosas propias.

La lógica sería:

**Perrite**
↓
características generales de todos los perritos

**Poodle**
↓
hereda esas características + puede tener otras propias

Esto nos permite organizar mejor el código y evitar repetir información.

## Clase vs. instancia

Otra diferencia importante fue entender **clase e instancia**, porque al principio suenan casi como lo mismo pero no lo son.

La **clase** es el modelo general.

La **instancia** es un objeto específico creado utilizando ese modelo.

Por ejemplo:

```cpp
Poodle copito;
```

Acá:

`Poodle` → es la clase.

`copito` → es una instancia de esa clase.

Podríamos tener después:

```cpp
Poodle copito;
Poodle luna;
Poodle pelusa;
```

Los tres pertenecen a la misma clase `Poodle`, pero son **tres objetos distintos**.

Es parecido a tener un molde: el molde es la clase y cada cosa que hacemos utilizando ese molde es una instancia.

# `for` y objetos

También vimos que podemos tener varios objetos y hacer que una misma acción ocurra con todos ellos utilizando un `for`.

Por ejemplo, imaginemos que tenemos varios perritos:

```cpp
for (perrite in perrites) {
    perrite.ladrar();
}
```

La idea sería algo como:

> toma un perrito → haz que ladre → pasa al siguiente → haz que ladre → sigue hasta terminar.

Entonces no tenemos que escribir manualmente:

```cpp
copito.ladrar();
luna.ladrar();
pelusa.ladrar();
```

Podemos recorrer el conjunto completo automáticamente.

Ahí entendí un poco mejor para qué sirven los `for`: no solamente para repetir números o instrucciones porque sí, sino también para **hacer una acción con muchos objetos que pertenecen a un mismo conjunto**.

# Cómo describir un objeto

Algo importante de esta parte fue entender que cuando creamos un objeto en programación **no necesitamos describir absolutamente todo lo que existe sobre él**.

Tenemos que preguntarnos:

**¿Qué información realmente necesito para lo que estoy haciendo?**

Por ejemplo, si estamos haciendo un programa sobre perritos donde solamente importa si tienen hambre y cuándo comen, probablemente no necesitamos guardar:

* el largo exacto de cada uña;
* cuántas pestañas tienen;
* el nombre del veterinario de su abuela.

Aunque sean características reales, **no aportan al funcionamiento del proyecto**.

Entonces programar también implica decidir **qué información es importante representar y cuál podemos ignorar**.

# Raspberry Pi y placas

Después pasamos a hablar más de hardware.

Vimos **Raspberry Pi** y también cómo los profes están intentando desarrollar sus propias placas para algunos proyectos.

La gracia de hacer una placa específica es que puedes dejar **solamente los componentes que realmente necesitas**, en vez de tener una placa llena de cosas que nunca vas a ocupar.

Además, esto puede hacer que sea bastante más barato.

La protoboard básicamente está pensada para probar circuitos y hacer prototipos antes de llegar a una solución más definitiva.

## MicroPython

También hablamos de **MicroPython**.

MicroPython permite programar microcontroladores utilizando una versión de Python, por lo que escribir el código puede ser mucho más fácil para nosotros. (PROHIBIDO)

La razón no es solamente porque "sea demasiado fácil", sino porque también hay una diferencia entre lo fácil que es para nosotros escribir el código y lo fácil que es para el microcontrolador ejecutarlo.

MicroPython necesita una capa adicional para poder interpretar ese código y eso también ocupa memoria y recursos.

Como nosotros vamos a trabajar con placas donde la memoria es limitada, nos conviene utilizar herramientas más cercanas a lo que el microcontrolador puede procesar directamente.

Y además:

**la memoria cuesta plata.**

Entonces mientras menos recursos innecesarios necesitemos, mejor.

# Pico SDK

Para empezar a trabajar con estas placas vamos a utilizar **Pico SDK**.

El SDK básicamente nos entrega herramientas, estructuras y ejemplos para programar la Raspberry Pi Pico utilizando C/C++.

Vamos a trabajar harto a partir de los **Pico SDK examples**, porque podemos tomar ejemplos que ya funcionan y empezar a entenderlos, modificarlos y probar cosas desde ahí.

La idea no es inventar absolutamente todo desde cero.


# `int main()`

En los programas vamos a encontrarnos con algo como:

```cpp
int main()
```

`main` es básicamente **el punto principal desde donde comienza a ejecutarse el programa**.

Podemos imaginarlo como el lugar que organiza lo que tiene que ir ocurriendo.

Por ejemplo, podríamos tener una lógica como:

```text
¿El usuario presionó el botón?
          ↓
         sí
          ↓
   reproducir sonido
```

El programa está constantemente revisando qué ocurre y, dependiendo de ciertas condiciones, ejecuta acciones.

Por ejemplo:

```cpp
if (botonPresionado) {
    reproducirSonido();
}
```

Entonces podemos pensar que `main` funciona como una especie de **centro de control**.

Desde ahí podemos revisar entradas, tomar decisiones y llamar otras funciones.

Y esto igual empieza a conectar todo lo anterior:

* tenemos **datos** que guardan información;
* tenemos **objetos** con atributos;
* tenemos **funciones** que realizan acciones;
* y tenemos una lógica general que decide **cuándo ocurre cada cosa**.

## encargos

## Aristóteles y sus categorías

Para esta tarea elegí **mi cepillo de pelo**, porque es un objeto que uso todos los días y siento que sirve para entender las categorías de Aristóteles de una forma mucho más simple.

Aristóteles propone distintas categorías que permiten describir una cosa desde varios aspectos. No solamente importa decir **qué es**, sino también cómo es, cuánto mide, dónde está, qué hace o qué le puede pasar.

### Objeto: mi cepillo de pelo

#### 1. Sustancia — ¿qué es?

Es un **cepillo de pelo**.

Esta sería como la descripción principal del objeto. Antes de decir su color, tamaño o dónde está, primero necesito saber qué cosa estoy describiendo.

#### 2. Cantidad — ¿cuánto?

Tengo **un cepillo**.

También puedo describir cosas que se pueden medir o contar, por ejemplo:

- Tiene un mango.
- Tiene una cabeza.
- Tiene muchas cerdas.
- Mide cierta cantidad de centímetros de largo.

Entonces esta categoría tiene que ver con **cuánto hay, cuántas partes tiene o cuánto mide algo**.

#### 3. Cualidad — ¿cómo es?

Mi cepillo es:

- De color lila.
- De plástico.
- Liviano.
- Tiene una forma alargada.
- La cabeza es ancha y con los bordes redondeados.
- Tiene muchas cerdas delgadas y flexibles.
- Las cerdas tienen pequeñas puntitas redondeadas.

Acá describo las **características que tiene el objeto**, o sea, cómo es físicamente.

#### 4. Relación — ¿con respecto a qué?

Mi cepillo se relaciona principalmente conmigo y con mi pelo.

Por ejemplo:

- Es **mi** cepillo.
- Lo uso en mi pelo.
- Es más pequeño que un secador de pelo.
- Lo puedo usar junto con otros productos para el pelo.

Esta categoría me costó un poco más al principio, pero básicamente se trata de describir una cosa **en relación con otra**.

#### 5. Lugar — ¿dónde está?

Depende del momento.

Puede estar:

- En mi pieza.
- En el baño.
- Sobre mi cama.
- Dentro de mi cartera.
- En mi mano cuando lo estoy usando.

El objeto sigue siendo el mismo, pero podemos describir **dónde se encuentra en un momento determinado**.

#### 6. Tiempo — ¿cuándo?

Uso mi cepillo en distintos momentos del día.

Por ejemplo:

- En la mañana antes de salir.
- Después de lavarme el pelo.
- Antes de ir a trabajar o a la universidad.
- Cuando llego a mi casa y tengo el pelo medio enredado.

Esta categoría permite ubicar el objeto o una acción **en un momento determinado**.

#### 7. Posición — ¿cómo está colocado?

El cepillo puede estar:

- Acostado sobre una mesa o la cama.
- Parado.
- Dentro de un cajón.
- En mi mano de forma vertical mientras me peino.

Aunque cambie de posición, sigue siendo exactamente el mismo cepillo.

#### 8. Estado o posesión — ¿qué tiene?

Mi cepillo puede tener:

- Pelos atrapados entre las cerdas.
- Agua si lo acabo de lavar.
- Productos del pelo entre las cerdas.
- Algunas cerdas un poco dobladas por el uso.

Esta categoría habla de cosas que el objeto **tiene o lleva consigo en cierto momento**.

#### 9. Acción — ¿qué hace?

Mi cepillo sirve para:

- Desenredar el pelo.
- Ordenarlo.
- Separar mechones.
- Ayudarme a peinarlo.

Cuando lo paso por mi pelo, las cerdas van separando los mechones y ayudando a soltar los nudos.

Acá estamos pensando en **lo que el objeto hace o para qué actúa**.

#### 10. Pasión — ¿qué le ocurre?

Esta categoría es al revés de la anterior. En vez de pensar qué hace el cepillo, pienso en **qué cosas le pueden pasar**.

Por ejemplo:

- Se le doblan las cerdas.
- Se ensucia.
- Se moja.
- Se cae al suelo.
- Se puede rayar.
- Se puede romper alguna cerda.
- Se llena de pelos después de usarlo.

Entonces lo entendí así:

**acción** → lo que hace el cepillo.  
**pasión** → lo que le ocurre al cepillo.

Al final, usar las categorías de Aristóteles me ayudó a darme cuenta de que incluso un objeto tan simple como un cepillo se puede describir desde muchas partes distintas. No solamente por **qué es**, sino también por cómo es, cuánto tiene, dónde está, con qué se relaciona, qué hace y qué cosas le pueden pasar.

## lectura

En estas páginas entendí más que nada que las máquinas de dibujo empezaron a cambiar mucho la forma de trabajar con geometría. Antes hacer curvas o formas complejas requería bastante conocimiento y tiempo, pero estas herramientas comenzaron a tener ese conocimiento casi incorporado en su funcionamiento. Me llamó la atención que así el dibujo se vuelve menos dependiente de la mano y la intuición de la persona, porque la máquina podía repetir formas muy complejas de manera mucho más precisa. Siento que acá ya empieza a aparecer una idea muy parecida a lo que pasa hoy con herramientas digitales, donde no siempre necesitamos entender todo lo que ocurre detrás para poder usarlas.

“Mechanization made absurdly complex drawings a quotidian affair.”- pág.45

“The most exact sensitivities of the architectural eye were satisfied through calculation rather than intuition.”- pág.45
