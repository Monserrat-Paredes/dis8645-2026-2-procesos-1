# sesion-06b

2026-09-25

## Ejemplo clase anterior

Estudiante Catalina Oyanedel

 1. **Sustancia:** Mi termo
 2. **Cantidad:** 800ml (también puede ser 1, dependiendo de cómo se considere)
 3. **Cualidad:** Blanco, metálico (acero inoxidable), térmico
 4. **Relación:** Contenedor de té Ceylan
 5. **Lugar:** Favorito, conmigo, a la izquierda de mi mano izquierda
 6. **Tiempo:** ~~Aquí~~ **Ahora**, siempre pronto
 7. **Posición:** Vertical
 8. **Posesión:** Es mío, pero también puede ser lo que posee, por ende, puede ser "liquido"
 9. **Acción:** Mantener el calor
 10. **Pasión:** Ser llenado para transportar líquido

## Ejemplo Wokwi

```c
 // tenemos que copiar y pegar este archivo
 // ojo que está entre "<>"
 // esto significa que este archivo está en un lugar lejano
 // y tiene que ver con C

#include <stdio.h>

 // 

#include "pico/stdlib.h"

 // podemos escribir nuestra propia funcion
 // tipo "void"
 // nombre
 // murcielagos
 // top-down
 // de lo macro a lo micro

 int prueba() {

  int x = 3;
  int y = 6;
  int resultado = x * y;
  return resultado;

 }
 

 // la funcion es main()
 // se identifica por los parentesis ()
 // es de tipo int
 // y cuando corren
 // retornan a un entero

int main() {

 // esta funcion inicializa la raspi
 // si no esta llamado en esta funcion
 // no va a ocurrir

  stdio_init_all();
  while (true) {

    // printf("Hello, Wokwi!\n");
    // convertir de int a chars

    // printf("resultado: %d\n, prueba()");

    printf("%d\n", prueba());
    prueba();
    sleep_ms(250);
  }
}
```

## encargos

## lectura
