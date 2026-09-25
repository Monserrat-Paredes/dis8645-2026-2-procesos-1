# sesion-06b

## apuntes sesión
2026-09-25

raspberry pi pico
 
- Wokwi 
- <stdio.h> 
- st= standard  io= ingresar información y soltar información
stdlib.h 


 **int main**
acá se trabaja.
- Esta funciona inicia el raspico. 
- Aca no existe ni setup, ni loop.  
- int cuando corren, después retornan un número entero.
- Como se escribe mi propia funcion **tipo nombre, paréntesis murcielago**
 ```cpp
int prueba() []
 ```
- Como llamar a una función: printf(prueba) 
- \n es enter.

 ```cpp
%d
```
- convierte de string a chars.
- siempre hay que explicar antes la funcion y despues pedirle para que funcione.  

**ejemplo profe en Wokwi** 

 ```cpp
// copia y pega ese archivo
// ojo que esta entre <>
// este archivo esta en un lugar lejano
// que tiene que ver con C
#include <stdio.h>
// este otro esta entre ""
// entre "" es literalmente
// en ese lugar
// en este caso
// al lado de este archivo
// hay una carpeta pico/
// y adentro esta stdlib.h
#include "pico/stdlib.h"


// mi propia funcion
// tipo nombre
// parentesis murcielagos
// diseno top-down
int prueba() {
  int x = 3;
  int y = 6;
  int resultado = x * y;
  return resultado;
}


// funcion main()
// es de tipo int
// las int cuando corren
// retornan un entero
int main() {
  // esta funcion
  // inicializa raspico
  stdio_init_all();
  while (true) {
    // printf("Hello, Wokwi!\n");
    // convertir de int a chars
    printf("%d\n", prueba());
    sleep_ms(250);
  }
}
 ```
- int posicion;
- Todo public ya que puedes cambiarle el valor 
- Este semestre solo public 
- void abrir() y void cerrar()
- myObj le das valor
- 
 ```cpp
termo elDeCatalina;
termo elDeMati;
 ```
- en main se pone sus caracteristicas y se pueden confirmar

 ```cpp
bool existencia; 
int posicion;
int cantidadML;
float temperatura;
 ```
**Que hace un constructor: (bob)** 
- Es un método automático cuando se crea un objeto
- Es solo el constructor 
- Se le puede pedir parámetros al constructor
- Class 



**Charla Rodrigo Toro**

- Porque es bueno hacer maquinas 
- Fracasos 
- Siempre hay que llegar, aunque salga mal 
- Autómata manos de cobre 
- Rodamientos 
- Siempre tener cuidado al diseñar ya que los usuarios siempre pueden romper el diseño.
- modulo berlín ( un lápiz lópez más bacán en europa)
- “la invención de morel” libro recomendado 
- Puentes h
- Fotoliptófono (referente)
- ruedas y rodamientos 

## encargos
**seleccionar un objeto y clasificarlo según las categorías del ser de aristóteles**

investigación:

 Las Categorías clasifican todo objeto de la comprensión humana en una de diez categorías. Aristóteles pretendía que enumeraran todo aquello que puede expresarse sin composición ni estructura, es decir, todo lo que puede ser sujeto o predicado de una proposición.
 
-  “lo que es se dice de muchas maneras”
- Aristóteles nos dice que la Filosofía primera estudia “lo que es en tanto que es”
- son los modos en que el ser se presenta y existe, son “flexiones del ser”.
- “ser se dice de muchas maneras”
  
 Para Aristóteles, el hecho de que el ser tenga muchos significados no le impediría ser objeto de ciencia, porque sus múltiples significados no son simplemente homónimos, o sea, no tienen solo un nombre en común, sino que tienen en común también otra cosa, que es la referencia común a una determinada realidad que es una: la entidad (ousía).

Ahora bien, las categorías se pueden poner en correspondencia con las operaciones y con los resultados de las operaciones, lo que nos obliga a asociarlas con los objetos y con la verdad y la falsedad, por lo que, ante todo, estarían remitiendo a la realidad –realidad desde la perspectiva de la clasificación y la totalización (Gustavo Bueno, TCC 2, 62). En este sentido, vemos, pues, cómo la cuestión de las categorías atañe a las ciencias en función de la realidad y de la verdad. Asimismo, es necesario tener en cuenta el problema de la génesis y estructura de las categorías aristotélicas atendiendo paralelamente a la involucración entre los conceptos y las ideas.


**Elemento elegido: el tocadiscos de mi papa** 

| Categoría Aristotélica | Pregunta Clave | Análisis |
| :--- | :--- | :--- |
| **1. Sustancia** (*Ousía*) | ¿Qué es? |   La sustancia es el conjunto de materia y forma funcional que forman al objeto |
| **2. Cantidad** (*Posón*) | ¿Cuánto / De qué medida es? | Mide 35 cm de largo x 35 cm de ancho x 10 cm de alto. |
| **3. Cualidad** (*Poión*) | ¿Cómo es? | Cuerpo gris con botones negros, tiene una carcasa protectora transparente rota por mi gata. |
| **4. Relación** (*Pros ti*) | ¿Con qué se vincula? | Se relaciona con la red eléctrica (cable/energía), con los parlantes para amplificar el audio y, esencialmente, con el vinilo como soporte materialpara reproducir la música. |
| **5. Lugar** (*Pou*) | ¿Dónde está? | En la sala de mi casa, apoyado sobre un velador largo de madera, al lado del reproductor de música y de los parlantes. |
| **6. Tiempo** (*Poté*) | ¿Cuándo es / existe? |Existe en la época actual y se encuentra operando en tiempo presente. |
| **7. Posición** (*Keisthai*) | ¿En qué postura está? | Apoyado de forma horizontal sobre la mesa. |
| **8. Posesión** (*Echein*) | ¿Qué lleva puesto / tiene adjunto? |Actualmente colocado sobre su plato un disco de vinilo del álbum *"Canción Animal"* de Soda Stereo. |
| **9. Acción** (*Poiein*) | ¿Qué hace? |Hace girar el plato, procesa vibraciones mecánicas/electromagnéticas y emite sonido al entorno. |
| **10. Pasión** (*Paschein*) | ¿Qué recibe o padece? |Recibe el impacto que rompió su carcasa, tiene la accion física del usuario para utilizarlo (encendido, selección de vinilo) y absorbe corriente eléctrica. |


Bibliografia 
https://sedici.unlp.edu.ar/bitstream/handle/10915/177649/Documento_completo.pdf?sequence=1

https://www.fgbueno.es/efo/efo316.htm

https://filosofia.net/piezas/categorias.htm
## lectura
