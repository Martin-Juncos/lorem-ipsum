# Proyecto Lorem Ipsum Generator en JavaScript
https://martin-juncos.github.io/lorem-ipsum/
### Descripción del Proyecto

Este proyecto es una implementación de un generador de texto Lorem Ipsum utilizando JavaScript. El generador permite a los usuarios crear texto de relleno (dummy text) para utilizar en diseño web, maquetación y pruebas de contenido.

### Propósito del Proyecto

El propósito de este proyecto es proporcionar una herramienta simple y efectiva para generar texto Lorem Ipsum. Este tipo de texto es útil para diseñadores, desarrolladores y cualquier persona que necesite un texto temporal para probar diseños o presentar prototipos.

### Lógica del Código

El proyecto utiliza JavaScript para generar párrafos de texto Lorem Ipsum. A continuación, se describe la lógica principal del código:

1. **Configuración Inicial**:
   Se define una lista de oraciones Lorem Ipsum predefinidas. Esta lista se utiliza para generar los párrafos.

   ```javascript
   const loremText = [
     "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
     "Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
     "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
     // más oraciones...
   ];
   ```

2. **Generación de Párrafos**:
   Se selecciona un número de oraciones aleatorias de la lista para formar un párrafo. El número de oraciones puede ser especificado por el usuario.

   ```javascript
   function generateLoremIpsum(paragraphCount) {
     let paragraphs = [];
     for (let i = 0; i < paragraphCount; i++) {
       let paragraph = loremText
         .sort(() => 0.5 - Math.random())
         .slice(0, 5)
         .join(" ");
       paragraphs.push(paragraph);
     }
     return paragraphs;
   }
   ```

3. **Actualización de la Interfaz de Usuario**:
   Los párrafos generados se muestran en la interfaz de usuario actualizando el contenido de elementos HTML específicos.

   ```javascript
   function displayLoremIpsum() {
     const paragraphCount = document.getElementById("paragraph-count").value;
     const loremIpsumText = generateLoremIpsum(paragraphCount);
     document.getElementById("output").innerHTML =
       loremIpsumText.join("<br><br>");
   }
   ```

4. **Interacción del Usuario**:
   El usuario puede ingresar el número de párrafos que desea generar y hacer clic en un botón para generar el texto Lorem Ipsum.
   ```html
   <input type="number" id="paragraph-count" placeholder="Número de párrafos" />
   <button onclick="displayLoremIpsum()">Generar</button>
   <div id="output"></div>
   ```

### Uso del Generador de Lorem Ipsum

1. **Abrir el Archivo**:
   Abre el archivo `index.html` en tu navegador para ver el generador en acción.

2. **Generar Texto Lorem Ipsum**:
   Ingresa el número de párrafos que deseas generar en el campo de entrada y haz clic en el botón "Generar".

3. **Visualizar el Texto Generado**:
   El texto Lorem Ipsum generado se mostrará en la página debajo del botón.

### Modificación del Generador

Para modificar el comportamiento del generador de Lorem Ipsum, puedes cambiar el código JavaScript. También puedes modificar el CSS y el HTML para cambiar la apariencia de la página y del generador.

                            ©ProfMartinJuncos

```

```
