# sesion-06b

viernes 25-09:

## apuntes sesión

Las categorías de Aristóteles nos ayudarán a entender cómo hacer código.

Vemos Wokwi.

`#include <stdio.h>` está entre `<>` y este otro `#include "pico/stdlib.h"` entre `""`.

Ejemplo:

Las `void` ocurren y ya, pero las `int`, cuando corren, retornan un entero.

Ejemplo del profe con todo listo

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

## encargos

encargo:

viernes 25-09: 

seleccionar un objeto y clasificarlo según las categorías del ser de aristóteles

El objeto que elijo es un mouse porque es algo con lo que convivo todos los días para hacer tareas o jugar en el computador.

## 10 categorías de Aristóteles


| **Categoría**         | **Descripción**                                                                                                                                                      |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sustancia**         | Un mouse.                                                                                                                                                            |
| **Cantidad**          | Mide: largo: 132 mm (13,2 cm), ancho: 75 mm (7,5 cm) y alto: 40 mm (4,0 cm). Pesa 121 g sin pesas y 139 g si le pongo las cinco pesas adicionales de 3,6 g. Hay uno. |
| **Cualidad**          | Es de plástico duro, liso y suave, de color negro, con algunas piezas de color metálico.                                                                             |
| **Relación**          | Se relaciona o compara con un puntero o con un ratón por el tamaño y el cable, que parece una cola de ratón.                                                         |
| **Lugar**             | Está dentro de una habitación, al lado de un computador.                                                                                                             |
| **Tiempo**            | Se utiliza en cualquier momento del día, por ejemplo, en alguna actividad mientras se esté usando el computador.                                                     |
| **Posición**          | Está apoyado sobre su superficie más plana, con el plástico o vidrio transparente apuntando hacia la superficie plana en la que se apoya.                            |
| **Estado / posesión** | Tiene 10 botones, uno de ellos también gira. Se encuentra bastante desgastado.                                                                                       |
| **Acción**            | Permite ver un puntero en una pantalla para guiar en qué posición de la pantalla se encuentra el usuario.                                                            |
| **Pasión**            | Generalmente es envuelto por la palma de la mano por arriba de los botones.                                                                                          |


## lectura
