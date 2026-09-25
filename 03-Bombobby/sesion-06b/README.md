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

Luego del break llegó el invitado especial, Rodrigo Toro y empezó su charla
Dice que es bueno diseñar máquinas y que hay que tener cuidado con la manera en la que dejamos expuestos nuestros diseños, porque siempre habrán usuarios que toquen partes que no deberían.
Nos muestra sus asombrosas autómatas de manos de cobre y enfatiza en la importancia de comprar rodamientos.
Sus diseños que parecían toca discos, me recordó al examen que entregué en mi taller del año pasado en el museo de la memoria.

```
#include "pico/stdlib.h"
// todo lo que esté debajo de "public" será público y accesible desde fuera de la clase.
// cualquier parte de tu programa puede leer o modificar la variable posicion directamente.

class Termo {
  public:
// si agregamos un 0 a los atributos significa que lo dejamos en "por defecto"
    bool existencia;
    int posicion; 0
    int cantidadML;
    float temperatura;

    void abrir ();
    void cerrar ();

// class siempre tiene ; al final de los murcielagos
};

int main() {
stdio_init_all();

Termo elDeCatalina;
Termo elDeMatias;

elDeMatias.existencia = true;
elDeCatalina.existencia = true;

// el . es para llamar
elDeCatalina.cantidadML = 800;
elDeMatias.cantidadML = 500;

}
```
Como es latero escribir cada categoría vamos a usar el cout (bob), es decir el constructor, al que le podemos pedir parámetros.
```
bool existencia;
    int posicion; 0
    int cantidadML;
    float temperatura;
    int rodamientos; 5

// constructor bob
// con parametro
// para cuantosML

Termo(int cuantosML){
  cantidadML = cuantosML;
}

Termo elDeCatalina (800);
Termo elDeMatias (500);
```

## encargos

## lectura
