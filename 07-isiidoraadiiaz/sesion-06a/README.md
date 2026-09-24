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

## lectura
