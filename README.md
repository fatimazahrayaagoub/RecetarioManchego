# Documento de reflexión – Recetario Manchego

### 1. ¿Por qué es importante reutilizar bloques de UI en lugar de duplicar código?

Es importante porque así no tenemos que escribir el mismo código varias veces. En mi aplicación he creado bloques reutilizables como BloqueFoto, BloqueResumen, BloqueIngredientes y BloquePasos.

De esta manera puedo utilizar los mismos bloques en diferentes partes de la aplicación. Además, si quiero cambiar algo, solo tengo que modificarlo en un sitio y es más fácil mantener el código.

### 2. ¿Qué ocurre si giras el dispositivo estando en la ficha de una receta? ¿Se pierde el estado? ¿Por qué?

Cuando giro el dispositivo estando dentro de una receta, la aplicación cambia su diseño para adaptarse a la orientación horizontal.

La información de la receta no se pierde. Esto ocurre porque utilizo ViewModel para mantener los datos y Navigation para controlar la pantalla en la que estoy.

Además, tengo dos diseños diferentes: uno vertical y otro horizontal. Los dos utilizan los mismos bloques de información.

### 3. ¿Cómo se aplica UDF en este proyecto? Identifica los tres niveles: ViewModel, pantalla y bloques reutilizables.

En mi proyecto aplico UDF separando las responsabilidades en tres niveles:

- **ViewModel:** guarda y controla el estado de las recetas. También se encarga de cambiar las recetas favoritas y controlar qué tarjeta está expandida.

- **Pantalla:** muestra la información y recoge las acciones del usuario. Por ejemplo, permite buscar recetas, abrir una ficha o marcar una receta como favorita.

- **Bloques reutilizables:** muestran partes de la interfaz, como las fotos, los ingredientes, los pasos y los resúmenes. Reciben los datos y muestran la información.

