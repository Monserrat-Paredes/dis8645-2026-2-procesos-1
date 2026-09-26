# sesion-06a

## apuntes sesión

# Diseño y Máquinas Computacionales

## De variables a clases

### Variables

Una **variable** sirve para guardar un dato.

Se puede pensar como un contenedor. El tipo de variable define qué tipo de dato puede guardar.

### Tipos de variables

#### `bool`

Tiene solo dos estados:

`true` o `false`

Sirve para representar presencia / ausencia o si algo se cumple o no.

```cpp
bool caminar = true;
bool pasarloBien = false;
```

#### `int`

Guarda números enteros.

```cpp
int cantidad = 3;
```

Se puede pensar como una **escalera**, porque va de un número entero a otro.

`1 → 2 → 3 → 4`

#### `float`

Guarda números con decimales.

```cpp
float valor = 1.5;
```

Se puede pensar como una **rampa**, porque entre dos números pueden existir valores intermedios.

`1.0 → 1.1 → 1.2 → 1.3...`

#### `uint`

Significa `unsigned integer`.

Es un número entero sin signo negativo.

Puede ser:

`0, 1, 2, 3...`

pero no:

`-1, -2, -3...`

## Clases

Una `class` no es una variable.

Una clase permite juntar:

- **datos**
- **acciones**

O sea:

**lo que algo tiene o es + lo que algo puede hacer**

Ejemplo:

```cpp
class Estudiante {

};
```

El nombre de una clase empieza con **mayúscula**.

Ejemplos:

`Estudiante`, `Perrito`, `Poodle`

La clase se escribe en singular.

## Atributos

Los **atributos** son los datos o características que están dentro de una clase.

Responden cosas como:

- qué tiene
- cómo es
- en qué estado está

Ejemplo:

```cpp
class Perrito {

    bool hambre;
    bool durmiendo;
    int pelaje;

};
```

`hambre`, `durmiendo` y `pelaje` son atributos.

Una variable dentro de una clase pasa a llamarse **atributo**.

**datos → variables → atributos dentro de una clase**

## Métodos

Los **métodos** son las acciones que puede hacer algo.

Ejemplos:

```cpp
comer();
dormir();
ladrar();
```

Una forma de distinguirlos:

- **sustantivos / características → atributos**
- **verbos / acciones → métodos**

## Funciones y métodos

Una **función** es un bloque de código que tiene un nombre y una serie de instrucciones.

Se reconoce porque lleva `()`.

```cpp
void ladrar() {

}
```

Cuando una función está dentro de una clase, se llama **método**.

```cpp
class Perrito {

    void ladrar() {

    }

};
```

Una función también puede recibir datos.

```cpp
void ladrar(int volumen, int frecuencia) {

}
```

`volumen` y `frecuencia` son datos que recibe la función.

## Clase e instancia

La **clase** es el molde.

La **instancia** es una cosa concreta creada a partir de ese molde.

Por ejemplo:

- `Poodle` → clase
- `Copito` → instancia
- `Pelusa` → instancia

```cpp
Poodle copito;
Poodle pelusa;
```

Los dos son objetos de la clase `Poodle`.

```text
Poodle
│
├── Copito
└── Pelusa
```

La clase define qué atributos y métodos existen.

Cada instancia después puede tener sus propios valores.

## Superclass

Una **superclass** es una clase más general.

Por ejemplo:

`Perro → Poodle → Copito`

- `Perro` → clase más general
- `Poodle` → clase más específica
- `Copito` → instancia

## Arrays

Un **array** permite guardar varios elementos del mismo tipo.

```cpp
Poodle perrites[] = {
    copito,
    pelusa
};
```

Acá:

- `Poodle` → tipo
- `perrites` → nombre del array
- `copito` y `pelusa` → elementos

## `for`

El `for` sirve para recorrer varios elementos y repetir una acción.

```cpp
for (Poodle perrite : perrites) {
    perrite.ladrar();
}
```

La idea sería:

**por cada `perrite` dentro de `perrites`, ejecutar `ladrar()`**

Entonces se recorre:

- `copito`
- `pelusa`

sin tener que escribir la acción para cada uno por separado.

## Ejercicio: clase `Estudiante`

En clase tuvimos que pensar una clase `Estudiante`.

```cpp
class Estudiante {

};
```

La clase es el molde y cada alumno sería una instancia.

```text
Estudiante
│
├── yo
├── estudiante 2
└── estudiante 3
```

Había que pensar atributos y métodos.

### Atributos

Los atributos representan cómo es o en qué estado está el estudiante.

Por ejemplo:

```cpp
class Estudiante {

    bool sentado;
    bool tienePelo;
    bool tieneRulos;

};
```

Cada estudiante tiene esos atributos, pero los valores pueden ser distintos.

Por ejemplo:

```text
sentado = true
tienePelo = true
tieneRulos = true
```

## Métodos de `Estudiante`

Los métodos son las acciones.

Por ejemplo:

```cpp
ponerseCrema();
```

La idea es que los métodos tengan relación con los atributos.

En este caso:

`ponerseCrema()` → `tieneRulos`

Los métodos pueden leer o modificar atributos.

## Flechas del diagrama

Las flechas van desde los **métodos** hacia los **atributos**.

**método → atributo**

Porque el método actúa sobre el atributo.

Por ejemplo:

`ponerseCrema()` → `tieneRulos`

## Mi clase

En mis apuntes tenía estas ideas:

### Atributos

- `misListas` → array
- `miedos` → array
- `caminar` → bool
- `pasarloBien`
- `amistades`

Podría verse así:

```cpp
class Estudiante {

    string misListas[];
    string miedos[];
    bool caminar;
    bool pasarloBien;
    string amistades[];

};
```

### Métodos

- `crearLista()`
- `crearMiedo()`
- cambiar `caminar` a `true`
- agregar amistades

Relaciones:

- `crearLista()` → `misListas`
- `crearMiedo()` → `miedos`
- método de caminar → `caminar`
- método de amistades → `amistades`

La lógica sería:

```text
CLASE
│
├── ATRIBUTOS
│   └── datos
│
└── MÉTODOS
    └── acciones
```

## Mayúsculas y nombres

Los nombres de las clases empiezan con **mayúscula**:

```cpp
Perrito
Poodle
Estudiante
```

Los atributos, variables y métodos empiezan con **minúscula**:

```cpp
hambre
pelaje
ladrar
crearLista
```

Si tienen más de una palabra:

```cpp
pasarloBien
crearMiedo
misListas
```

Para el computador:

`Perrito`

y

`perrito`

son nombres distintos.

## `int main()`

`main()` es donde comienza a ejecutarse el programa.

```cpp
int main() {

}
```

Por ejemplo:

```cpp
int main() {

    Poodle copito;

    copito.ladrar();

}
```

Desde `main()` se pueden crear objetos y ejecutar sus métodos.

El punto `.` permite acceder a algo que pertenece al objeto.

```cpp
copito.ladrar();
```

## Materia y energía

- **las cosas → materia**
- **las cosas que mueven las cosas → energía**

En programación se puede relacionar con:

- **objeto** → la cosa
- **atributos** → sus datos
- **métodos** → sus acciones

La idea de la clase es pasar de trabajar con variables sueltas a agrupar datos y acciones dentro de objetos.

## Resumen

- **variable** → guarda un dato
- **`bool`** → `true` o `false`
- **`int`** → número entero
- **`float`** → número con decimales
- **`uint`** → número entero sin signo negativo
- **class** → agrupa datos y acciones
- **atributo** → variable dentro de una clase
- **método** → función dentro de una clase
- **objeto / instancia** → objeto concreto creado desde una clase
- **array** → conjunto de elementos
- **`for`** → recorre elementos y repite una acción
- **superclass** → clase más general

## encargos
- Elegir un objeto y analizarlo de forma aristotélica.
- Pensarlo desde sus propiedades físicas usando las categorías de Aristóteles.
- Descargar mis datos desde una red social.

¿Qué es analizar algo de forma aristotélica? 
"aristotelismo incluye una concentración en el conocimiento, ya sea accesible por medios naturales o explicable por la razón ; un enfoque inductivo y analítico. El empirismo , o énfasis en la experiencia, en el estudio de la naturaleza —incluido el estudio de los seres humanos, su comportamiento y sus organizaciones— que conduce desde la percepción de sucesos individuales contingentes hasta el descubrimiento de patrones permanentes y universales; y la primacía de lo universal, aquello que se expresa en términos comunes o generales."
Minio-Paluello, L. (9 de enero de 2019). Aristotelismo . Enciclopedia Británica . https://www.britannica.com/topic/Aristotelianismo

# Objeto: cabina telefónica

INSERTAR FOTO

## Qué es
Una cabina telefónica pública, es una estructura que contiene un teléfono y permite hacer llamadas desde un espacio público.

## Material
- metal
- vidrio o plástico transparente
- cable
- teléfono
- botones
- componentes electrónicos

## Forma
Es una estructura vertical, cerrada por paneles transparentes.

Tiene:
- techo
- paneles laterales
- teléfono
- teclado de teléfono
- espacio para que una persona se ubique al frente

## Para qué sirve
Su función principal es permitir hacer llamadas telefónicas en un espacio público.

También sirve para:
- marcar un punto de comunicación
- proteger el teléfono
- dar un espacio delimitado a la persona que lo usa

## Cómo se relaciona con otras cosas
La cabina no funciona sola, solo funciona con: 
- la persona que la usa
- la red telefónica
- el espacio público
- la electricidad
- otra persona que recibe la llamada

## Acciones
- marcar un número
- llamar
- hablar
- escuchar
- colgar

También puede: 
- estar ocupada
- estar libre
- funcionar
- estar fuera de servicio

esto: Descargar mis datos desde una red social. Todavía no puedo hacerlo porque olvidé todas mis cuentas 
## lectura
