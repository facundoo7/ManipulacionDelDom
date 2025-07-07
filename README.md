# ManipulacionDelDom
# Gestor de Tarjetas Dinámicas

Este es un proyecto web simple que permite a los usuarios crear, editar, agregar imágenes y eliminar tarjetas de contenido dinámicamente desde el navegador.

---

## Descripción

La aplicación consiste en una interfaz mínima con un botón para crear tarjetas. Cada tarjeta cuenta con controles individuales que permiten:

- **Editar** el contenido.
- **Agregar una imagen** desde una URL.
- **Eliminar** la tarjeta.

Todo esto se gestiona dinámicamente mediante JavaScript puro, sin dependencias externas.

## Funcionalidades con Referencias al Código

### 1. Crear tarjeta

- **Archivo:** `app.js`  
- **Línea relevante:** `const nuevaTarjeta = document.createElement("div");`

Al hacer clic en el botón con ID `botonCrear`, se genera una nueva tarjeta con clase `tarjeta`.

```js
const button = document.getElementById('botonCrear');
button.addEventListener('click', () => {
  const nuevaTarjeta = document.createElement("div");
  nuevaTarjeta.className = "tarjeta";

### 2. Manejo del Evento Submit
formulario.addEventListener("submit", function(evento) {
  evento.preventDefault();
});
Se captura el envío del formulario.

Se evita que la página se recargue.

Se inicia el proceso de creación de una nueva tarjeta dinámica.

### 3. Creación de Elementos Dinámicos
Dentro del evento submit se crean varios elementos HTML usando JavaScript:

Inputs: para ingresar el título (inputTitulo), descripción (inputDescripcion) y la URL de la imagen (inputImagen).

Botones:

btnGuardar: guarda la tarjeta y la convierte en vista fija.

btnEliminar: elimina la tarjeta antes de guardarla.

Todos estos elementos se agrupan en un div con la clase tarjeta, que representa una tarjeta individual.

### 4. Funcionalidad del Botón "Guardar"
btnGuardar.addEventListener("click", function () {
  // Obtener valores, mostrar imagen, texto final y nuevos botones
});
Cuando el usuario hace clic en Guardar:

Se capturan los valores de los inputs.

Se reemplazan los inputs por:

Una imagen (<img>)

Un título (<h3>)

Una descripción (<p>)

Se agregan dos nuevos botones:

Editar

Eliminar

Esto transforma la tarjeta al "modo visual".

### 5. Funcionalidad del Botón "Editar"
btnEditar.addEventListener("click", function () {
  // Revertir a inputs editables
});
Permite volver al estado de edición original.

Se eliminan los elementos visuales (imagen, título y descripción).

Se restauran los inputs y los botones Guardar y Eliminar.

### 6. Funcionalidad del Botón "Eliminar"
contenedor.removeChild(tarjeta);
Existen dos botones "Eliminar":

Uno en modo edición.

Otro en la vista final después de hacer clic en "Guardar".

Ambos eliminan la tarjeta del DOM al ejecutar:

js
contenedor.removeChild(tarjeta);

###7. Limpieza del Formulario
formulario.reset();
Una vez que la tarjeta es creada y agregada al contenedor, el formulario original se limpia para permitir al usuario ingresar nuevos datos.

