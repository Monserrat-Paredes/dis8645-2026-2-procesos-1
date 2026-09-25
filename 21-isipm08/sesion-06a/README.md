# sesion-06a

# apuntes sesión
## variable
- conciencia del contenedor, importancia
- definir contenedor que ocupa en la memoria del computador
- retener datos ingresados por el usuario
- optimizan proceso programación
- contenedor o espacio de la memoria física o virtual, almacena distintos tipos de datos -- valores
- se le asigna nombre descriptivo o identificador -- refiriéndose al valor guardado
- datos almacenados pueden cambiar de valor o ser constantes

## tipos de variables
- estas dependen del lenguaje de programación
1. variable númerica ```int```: almacena números enteros
2. variable de punto flotante ```float```: guardan números con decimales
3. variables de caracteres ```char```: representan símbolos o caracteres
4. variables de cadena de caracteres ```string```: que contienen palabras y textos
5. variables lógicas o booleanas ```bool```: almacenar valores lógicos (verdadero o falso).

## declaración variable
- siempre hay que declararla, reservando un espacio en la memoria de la computadora para poder almacenar su valor
1. elegir nombre descriptivo: evitar usar palabras claves dentro del lenguaje de programación, se puede incluir letras o caracteres (no puede empezar con número), no empezar ni terminar con punto, utilizar _ para la separación de palabras o notación camello
2. especificar tipo de dato que se va a almacenar
3. ```int edad=21;``` el signo ```=``` se utiliza para almacenar el valor

---

### **bool**
- cabe algo o nada
- presencia/ausencia
- sí/no
- verdadero/falso

### **int**
- variable que solo acepta números
- enteros
- ¿por qué categorizar?
- datos duros

### **float**
- números con punto decimal
- rampa
- lugar de infinitas resoluciones

### **uint**
- centrados en torno al 0

### **array**
- colección valores internos

```
u = unsigned
```

---

## Clase
- class -- super estructura de información
- primera letra mayúscula
- distintas estructuras computacionales puedan interactuar entre sí
- tipo de plantilla la cual permite crear objetos con características y comportamientos comunes
- representar entidades o conceptos 

- permite hacer dos grandes cosas:
1. palabras que son datos(nombre humano)/variables(nombre programación)/atributos: definen característica del objeto
2. palabras con () y con algunas palabras dentro, acciones/funciones/métodos: funciones o acciones que el objeto puede realizar 

- modelo -- maneras de tratar de entender la realidad
- herencia -- existen clases que tiene como super clase (sub variedad): facilitan la creación de objetos a partir de otros ya existentes, subclase obtiene todo el comportamiento y atributos de su superclase
- ```.``` acceder para algo que esta viviendo dentro

```
bool tengo crochet y lana -- atributo
tejo un chaleco (); -- método
```

los métodos pueden leer atributos o escribir otro

los datos no afectan directamente al método

### bibliografía apuntes

<https://ebac.mx/blog/variable-en-programacion>

<https://es.wikipedia.org/wiki/Variable_(programaci%C3%B3n)>

<https://es.wikipedia.org/wiki/Clase_(inform%C3%A1tica)>

<https://es.wikipedia.org/wiki/Herencia_(inform%C3%A1tica)>

## encargos

seleccionar un objeto y clasificarlo según las categorías del ser de aristóteles 

### 10 categorías
- 10 modos en que se puede expresar y predicar la realidad de algo
1. sustancia: ser principal, no necesita de otro para existir
2. cantidad: dimensiones, número, medidad
3. cualidad: característica o propiedad
4. relación: vínculo o comparación
5. lugar: espacio o sitio dónde se encuentra
6. tiempo: momento o temporalidad de la existencia
7. posición: postura o disposición espacial
8. posesión: lleva puesto o adquirido de forma externa
9. acción: efecto o cambio que ejerce sobre otro
10. pasión: recibir o sufrir una acción de algo externo

### objeto
1. sustancia: botella buffer flask
2. cantidad: 830ml
3. cualidad: térmica, rosada, con mango para llevarla en la mano 
4. relación: contenedor de agua fría (generalmente)
5. lugar: dentro de mi mochila
6. tiempo: ahora, hasta que quizá se rompa y deje de cumplir su función
7. posición: postura fija, depende de mi para su movimiento
8. posesión: líquido
9. acción: mantener líquido frío, mejorar mi hábito de tomar agua
10. pasión: ser llenado y transportada diariamente

<https://www.sodimac.cl/sodimac-cl/articulo/146181110/vaso-tumbler-termico-botella-agua-buffer-inox-830-ml-rosa-claro/146181111>

<https://en.wikipedia.org/wiki/Categories_(Aristotle)>

<https://stgb.substack.com/p/aristotles-ten-categories-of-being>

## lectura

### Mindstorms: Children, Computers and Powerful Ideas - Seymour Papert
- empecé un nuevo capítulo llamado "Turtle Geometry: A Mathematics Made for Learning", igual es largo, entonces solo empecé con un par de páginas y lo que quede del resto del capítulo lo retomaré en la siguiente lectura

*apuntes lectura*
- geometría de totuga -- estilo computacional de geometría
  1. dinámica
  2. cabezal
  3. primer representante de las matemáticas para un niño, los cuales se pueden representar o identificarse con esta
  4. capaces de aceptar comandos en un lenguaje "turtle talk"
- establece la relación corporal de los niños mediante este objto lúdico "geomtería corporal"
- la finalidad de este es desarrollar ideas sobre la forma en que se mueven en el espacio
- conexión entre la actividad personal -- creación conocimiento formal
  
### turtle talk
- adelante: se moverá hacia adelante según la posición en que se encuentre (adelante 1 -- movimiento pequeño/ adelante 100 -- movimiento más grande)
- atrás
- izquierda -- cambie de rumbo mientras se mantiene en el mismo lugar
- derecha -- cambie de rumbo mientras se mantiene en el mismo lugar
- forward 
- Euclides -- estilo axiomático, "punto" entidad que tiene una posición pero no tiene otras propiedades
- Descartes -- analítico, estilo algebraico 

**comandos cuadrado**
```
adelante 100
derecho 90
adelante 100
derecho 90
adelante 100
derecho 90
adelante 100
derecho 90
```


