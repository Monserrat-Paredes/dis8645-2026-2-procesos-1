# sesion-06b

## apuntes sesión
- el día de hoy no fui a clases, pero mi amiga Vanessa me compartió de sus apuntes y me explicó lo pasado en clases, de esta forma pude realizar mis apuntes

\n - significa enter 

int no es lo mismo que chars 


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

https://www.w3schools.com/cpp/cpp_constructors.asp

https://www.w3schools.com/cpp/cpp_classes.asp

https://wokwi.com/projects/476140065507309569
