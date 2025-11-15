<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-09">Día 9</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-11">Día 11</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml10.png">
</h1>

# Día 10: Formularios Parte 2 - `<textarea>`, `<select>`, `<button>`

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Indice

- [Día 10: Formularios Parte 2 - `<textarea>`, `<select>`, `<button>`](#día-10-formularios-parte-2---textarea-select-button)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [Áreas de texto para contenido extenso](#áreas-de-texto-para-contenido-extenso)
  - [Etiqueta `<textarea>`](#etiqueta-textarea)
    - [Atributos principales de `<textarea>`](#atributos-principales-de-textarea)
  - [Etiqueta `<select>`.](#etiqueta-select)
    - [Atributos principales de `<select>`](#atributos-principales-de-select)
  - [Etiqueta `<option>`](#etiqueta-option)
    - [Atributos de `<option>`](#atributos-de-option)
    - [Etiqueta ](#etiqueta-)
  - [Etiqueta ](#etiqueta--1)
    - [Tipos de `<button>`](#tipos-de-button)
    - [Atributos de ](#atributos-de-)
  - [💻 Ejemplos Prácticos](#-ejemplos-prácticos)
  - [✏️ Ejercicios del Día](#️-ejercicios-del-día)
  - [Buenas Prácticas](#buenas-prácticas)


## 📖 Descripción

En la primera parte de formularios aprendiste los elementos básicos como `<input>` y sus tipos. Ahora es momento de ampliar tu conocimiento con elementos más especializados que ofrecen mayor flexibilidad y mejores experiencias de usuario. En este día descubrirás `<textarea>` para textos largos, `<select>` para crear menús desplegables con opciones, y `<button>` para crear botones más versátiles y personalizables.

Estos elementos son fundamentales para crear formularios completos y profesionales que cubran todas las necesidades de interacción con el usuario.


## 🎯 Objetivos del Día

Al acabar este día podrás:

- Crear áreas de texto multilínea con `<textarea>`
- Implementar menús desplegables con `<select>` y `<option>`
- Agrupar opciones con `<optgroup>`
- Utilizar la etiqueta `<button>` y sus diferentes tipos
- Combinar todos los elementos de formulario aprendidos hasta ahora

## 📚 Conceptos Clave

### Áreas de texto para contenido extenso


## Etiqueta `<textarea>`

La etiqueta `<textarea>` crea un área de texto multilínea donde los usuarios pueden escribir contenido extenso como comentarios, mensajes o descripciones.

```html
<textarea name="comentario" rows="5" cols="40"> Texto predeterminado aquí </textarea>
```

A diferencia de `<input>`, `<textarea>` tiene etiqueta de apertura y cierre. El contenido entre las etiquetas aparece como texto predeterminado.

### Atributos principales de `<textarea>`

**rows**: Especifica el número de líneas visibles (altura) del área de texto.

```html
<textarea rows="10"></textarea>
```

**cols**: Especifica el número de columnas (ancho) del área de texto en caracteres.
```html
<textarea cols="50"></textarea>
```

**name**: Identifica el campo cuando se envían los datos al servidor.

```html
<textarea name="mensaje"></textarea>
```

**placeholder**: Texto de ejemplo que desaparece cuando el usuario empieza a escribir.

```html
<textarea placeholder="Escribe tu mensaje aquí..."></textarea>
```

**required**: Hace que el campo sea obligatorio.

```html
<textarea required></textarea>
```

**maxlength**: Limita el número máximo de caracteres que se pueden escribir.

```html
<textarea maxlength="500"></textarea>
```

**readonly**: El campo es de solo lectura (no editable).

```html
<textarea readonly>Texto no editable</textarea>
```

**disabled**: Desactiva el campo completamente.

```html
<textarea disabled></textarea>
``` 

**wrap**: Controla cómo se ajusta el texto al enviarse. Valores: `soft` (por defecto) o `hard`.

```html
<textarea wrap="hard"></textarea>
```

## Etiqueta `<select>`.

La etiqueta `<select>` crea un menú desplegable que permite al usuario elegir una o varias opciones de una lista predefinida.

```html
<select name="pais"> 
    <option value="es">España</option> 
    <option value="mx">México</option> 
    <option value="ar">Argentina</option> 
</select> 
```

### Atributos principales de `<select>`
- name: Identifica el campo para el envío de datos.
- id: Identificador único, necesario para asociarlo con un <label>.
- multiple: Permite seleccionar múltiples opciones (manteniendo Ctrl o Cmd).

```html
<select name="idiomas" multiple>
  <option value="es">Español</option>
  <option value="en">Inglés</option>
  <option value="fr">Francés</option>
</select>
```

- size: Especifica cuántas opciones son visibles simultáneamente.
```html
<select size="5">
  <!-- opciones -->
</select>
``` 

- required: Hace obligatoria la selección de una opción.
```html
<select required>
  <!-- opciones -->
</select>
```

- disabled: Desactiva el menú desplegable completo.

```html
<select disabled>
  <!-- opciones -->
</select>
```

## Etiqueta `<option>`

- Define cada opción individual dentro de un `<select>`.
```html
<option value="valor">Texto visible</option>
```

### Atributos de `<option>`
- value: El valor que se enviará al servidor cuando se seleccione esta opción.
- selected: Marca la opción como preseleccionada.
```html
<option value="es" selected>España</option>
```
- disabled: Desactiva una opción específica (no se puede seleccionar).
```html
<option value="na" disabled>No disponible</option>
```

### Etiqueta <optgroup>
Agrupa opciones relacionadas dentro de un `<select>`, mejorando la organización visual y la accesibilidad.

```html
<select name="destino">
  <optgroup label="Europa">
    <option value="es">España</option>
    <option value="fr">Francia</option>
  </optgroup>
  <optgroup label="América">
    <option value="mx">México</option>
    <option value="us">Estados Unidos</option>
  </optgroup>
</select>
```
El atributo label de `<optgroup>` define el título del grupo y no se puede seleccionar.

## Etiqueta <button>

La etiqueta `<button>` crea un botón más flexible y personalizable que `<input type="submit">`. Puede contener texto, imágenes y otros elementos HTML.

```html
<button type="submit">Enviar Formulario</button>
```

### Tipos de `<button>`
- El atributo type define el comportamiento del botón:
  - type="submit": Envía el formulario (comportamiento por defecto).
```html
<button type="submit">Enviar</button>
```
- type="reset": Restablece todos los campos del formulario a sus valores iniciales.
```html
<button type="reset">Limpiar formulario</button>
```
- type="button": Botón sin comportamiento predeterminado, útil para JavaScript
```html
<button type="button" onclick="alert('Hola')">Haz clic</button>
```

- Ventajas de `<button>` sobre `<input>`
  - Puede contener HTML (imágenes, iconos, texto formateado).
  - Más fácil de estilizar con CSS.
  - Semánticamente más claro.
```html
<button type="submit">
  <img src="icono.png" alt=""> Enviar formulario
</button>
```

### Atributos de <button>
- name y value: Identifican el botón cuando se envía el formulario.
```html
<button type="submit" name="accion" value="guardar">Guardar</button>
```
- disabled: Desactiva el botón.
```html
<button disabled>No disponible</button>
```
- form: Asocia el botón con un formulario específico (incluso si está fuera del `<form>`).
```html
<button type="submit" form="mi-formulario">Enviar</button>
```
Ejemplo: 
<button type="submit" form="mi-formulario">Enviar</button>

---

## 💻 Ejemplos Prácticos
- Ejemplo 1: Formulario de contacto con textarea.

Código:
```html
<form action="/contacto" method="post">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="mensaje">Mensaje:</label>
  <textarea id="mensaje" name="mensaje" rows="6" cols="50" placeholder="Escribe tu mensaje aquí..." required></textarea>
  
  <button type="submit">Enviar mensaje</button>
  <button type="reset">Borrar todo</button>
</form>
```
---

- Ejemplo 2: Select simple con opciones:
Código:
```html
<form action="/reserva" method="post">
  <label for="habitacion">Tipo de habitación:</label>
  <select id="habitacion" name="habitacion" required>
    <option value="">-- Selecciona una opción --</option>
    <option value="individual">Individual</option>
    <option value="doble">Doble</option>
    <option value="suite" selected>Suite</option>
  </select>
  
  <button type="submit">Reservar</button>
</form>
```

---

- Ejemplo 3: Select con optgroup.
Código:
```html
<form action="/comprar" method="post">
  <label for="producto">Selecciona un producto:</label>
  <select id="producto" name="producto" required>
    <option value="">-- Elige una categoría --</option>
    
    <optgroup label="Electrónica">
      <option value="laptop">Laptop</option>
      <option value="tablet">Tablet</option>
      <option value="smartphone">Smartphone</option>
    </optgroup>
    
    <optgroup label="Ropa">
      <option value="camisa">Camisa</option>
      <option value="pantalon">Pantalón</option>
      <option value="zapatos">Zapatos</option>
    </optgroup>
    
    <optgroup label="Libros">
      <option value="ficcion">Ficción</option>
      <option value="tecnico">Técnico</option>
      <option value="biografia">Biografía</option>
    </optgroup>
  </select>
  
  <button type="submit">Añadir al carrito</button>
</form>
```

--- 

- Ejemplo 4: Formulario completo de registro.
Código:
```html
<form action="/registro" method="post">
  <label for="usuario">Nombre de usuario:</label>
  <input type="text" id="usuario" name="usuario" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="password">Contraseña:</label>
  <input type="password" id="password" name="password" required>
  
  <label for="pais">País:</label>
  <select id="pais" name="pais" required>
    <option value="">-- Selecciona tu país --</option>
    <option value="es">España</option>
    <option value="mx">México</option>
    <option value="ar">Argentina</option>
    <option value="co">Colombia</option>
  </select>
  
  <label for="intereses">Intereses (múltiple):</label>
  <select id="intereses" name="intereses" multiple size="4">
    <option value="deportes">Deportes</option>
    <option value="musica">Música</option>
    <option value="tecnologia">Tecnología</option>
    <option value="viajes">Viajes</option>
  </select>
  
  <label for="biografia">Cuéntanos sobre ti:</label>
  <textarea id="biografia" name="biografia" rows="5" cols="40" placeholder="Escribe una breve biografía..." maxlength="500"></textarea>
  
  <button type="submit">Crear cuenta</button>
  <button type="reset">Limpiar formulario</button>
</form>
```

--- 

- Ejemplo 5: Diferentes tipos de botones
Código:
```html
<form action="/procesar" method="post">
  <label for="datos">Datos:</label>
  <input type="text" id="datos" name="datos">
  
  <!-- Botón de envío -->
  <button type="submit">Enviar</button>
  
  <!-- Botón de reseteo -->
  <button type="reset">Restablecer</button>
  
  <!-- Botón sin comportamiento (para JavaScript) -->
  <button type="button" onclick="alert('Guardado como borrador')">Guardar borrador</button>
</form>
```

---
## ✏️ Ejercicios del Día

- Ejercicio 1: Formulario de comentarios ⭐
Crea un formulario simple de comentarios que incluya campos para nombre (text), email (email) y un área de comentarios (textarea) con 8 filas y 60 columnas. Añade un botón de envío. Todos los campos deben ser obligatorios.

   - [Solución](ejercicio1.html)

- Ejercicio 2: Selector de país con grupos ⭐⭐
Crea un formulario con un select que agrupe países por continente usando `<optgroup>`. Incluye al menos 3 continentes con 3 países cada uno. Añade una primera opción deshabilitada que diga "-- Selecciona tu país --". Incluye botones de enviar y resetear.

  - [Solución](ejercicio2.html)

- Ejercicio 3: Formulario completo de encuesta ⭐⭐⭐
Crea un formulario de encuesta que incluya: nombre (text), email (email), edad (number entre 18 y 100), país de residencia (select con optgroups por continente), nivel de satisfacción (select del 1 al 10), intereses (select múltiple con al menos 6 opciones), y comentarios adicionales (textarea con máximo 300 caracteres). Todos los campos deben tener sus labels correspondientes y usar placeholders apropiados. Incluye tres botones: enviar, resetear y uno personalizado de tipo "button" que muestre una alerta de JavaScript.

   - [Solución](ejercicio3.html)

## Buenas Prácticas
- Usa `<textarea>` para textos largos (más de una línea); 
- Usa `<input type="text">` para textos cortos.
- Especifica siempre rows y cols en `<textarea>` para controlar el tamaño inicial.
- Utiliza maxlength en `<textarea>` para limitar la entrada si es necesario.
- En `<select>`, incluye una primera opción vacía o deshabilitada como instrucción ("-- Selecciona una opción --").
- Usa `<optgroup>` para organizar listas largas de opciones y mejorar la experiencia del usuario.
- Asocia siempre cada campo con un `<label>` usando for e id.
- Prefiere `<button>` sobre `<input type="submit">` por su mayor flexibilidad y facilidad de estilizado.
- Especifica siempre el atributo type en `<button>` para evitar comportamientos inesperados.
- Usa type="button" para botones que ejecutarán JavaScript sin enviar el formulario.
- Proporciona feedback visual para campos obligatorios y estados deshabilitados.
- Asegúrate de que los valores del atributo value en `<option>` sean descriptivos y útiles para el procesamiento backend.

<h4 align="center"> <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-09">Día 9</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-11">Día 11</a> </h4>