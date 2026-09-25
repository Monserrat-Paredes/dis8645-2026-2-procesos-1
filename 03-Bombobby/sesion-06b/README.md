# sesion-06b

## apuntes sesión

```
#include <stdio.h>
```

Es antiguo y tiene que ver con C, std es por estándar e io es por input y out put

```
#include "pico/stdlib.h"
```
Este está entre "" por que es literalmente en ese lugar, al lado de este archivo hay una carpeta pico/ y adentro está stdlib.h

```

//mi propia funcion
void prueba() {
  int x = 3;
  int y = 6;
  int resultado = x * y;
  return resultado;
}

int main () {
// esta funcion inicializa raspico
stdio_init_all();
while (true) {
// printf("Hello,Wokwi!\n"; sleep_ms(250);
// \n" es enter 
printf("%d\n",prueba());
sleep_ms(250);
}
}
```

El profe intentó unas 5 veces hacer que el código funcionara y no lo hacía porque quería imprimir "prueba", sin embargo el concepto prueba no lo podía reconocer el pc porque prueba estaba después del int main (), lo cambió y... no funcionó

## encargos

## lectura
