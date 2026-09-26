# sesion-06b

## apuntes sesión

signo % es contextual

rodrigo toro:

hizo un cuerpo de resina lleno de agua, parece un pulmón 

2013 tenia entrega seminario de titulo, se obsesionó de una idea, hizo una escultura en donde no le funcionó el circuito

mano autómata que se arrastra por el suelo, se mueve con un motor

en una exposición utilizó un vinilo en donde hablaba, el cual alguien debía estar preocupado de estar volviendo a poner la aguja en el lugar cuando terminaba de reproducirse el audio del vinilo, por lo que decidió ralentizar el audio para que dure una hora, por lo que el trabajo de volver a poner la aguja en el lugar era más relajado. para dejar de tener que necesitar gente que haga el trabajo de poner la aguja, lo cambió para que lo haga una inteligencia artificial.

> cualquier método es mejor que ninguno

> hagan cosas con ruedas y rodamientos

---

class es una variable pero más compleja. es una super variable.

```cpp
class Termo {
	public:
		bool existencia;
		int posición = 0 ; //si no le digo nada en main, asumirá que la posición está en 0
		int cantidadMl;    // con esto nos ahorramos tener que darle valor a cada uno de estos abajo kkkkkkk
		float temperatura;

	// constructor 
	Termo(int cuantosMl) {
		cantidadMl = cuantosMl;
	}
		
		void abrir();
		void cerrar();
};

int main() {

stdio_init_all();


// constructor con parámetros para cuántos ml
Termo elDeCatalina(800);
Termo elDeMisa(500); // al poner esto nos ahorramos lo comentado debajo

elDeMisa.existencia = true;
elDeCatalina.existencia = true;

// elDeCatalina.cantidadMl = 800;
// elDeMisa.cantidadMl = 500;
```
---

## lectura: Program Or Be Programmed: Ten Commands for a Digital Age - Douglas Rushkoff
