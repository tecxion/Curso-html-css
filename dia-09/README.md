<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-08">Día 8</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-10">Día 10</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml9.png">
</h1>

# Día 9: Formularios Parte 1 - Elementos básicos: `<form>`, `<input>`, `<label>`, tipos básicos

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Indice
- [Día 9: Formularios Parte 1 - Elementos básicos: `<form>`, `<input>`, `<label>`, tipos básicos](#día-9-formularios-parte-1---elementos-básicos-form-input-label-tipos-básicos)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [La estructura de un formulario](#la-estructura-de-un-formulario)
  - [Etiqueta `<form>`](#etiqueta-form)
  - [Atributos principales de `<form>`](#atributos-principales-de-form)
  - [Etiqueta `<input>`](#etiqueta-input)
    - [Atributos esenciales de `<input>`](#atributos-esenciales-de-input)
  - [Etiqueta `<label>`](#etiqueta-label)
    - [¿Por qué usar `<label>`?](#por-qué-usar-label)
  - [Tipos básicos de `<input>`](#tipos-básicos-de-input)
    - [type="text" - Texto simple](#typetext---texto-simple)
    - [type="password" - Contraseña](#typepassword---contraseña)
    - [type="email" - Correo electrónico](#typeemail---correo-electrónico)
    - [type="number" - Número](#typenumber---número)
    - [type="tel" - Teléfono](#typetel---teléfono)
    - [type="url" - URL](#typeurl---url)
    - [type="submit" - Botón de envío](#typesubmit---botón-de-envío)
    - [type="reset" - Botón de reseteo](#typereset---botón-de-reseteo)
  - [💻 Ejemplos Prácticos](#-ejemplos-prácticos)
    - [Ejemplo 1: Formulario básico de contacto](#ejemplo-1-formulario-básico-de-contacto)
    - [Ejemplo 2: Formulario de registro](#ejemplo-2-formulario-de-registro)
    - [Ejemplo 3: Formulario de búsqueda](#ejemplo-3-formulario-de-búsqueda)
    - [Ejemplo 4: Formulario con diferentes tipos de input](#ejemplo-4-formulario-con-diferentes-tipos-de-input)
  - [✏️ Ejercicios del Día](#️-ejercicios-del-día)
    - [Ejercicio 1: Formulario de login ⭐](#ejercicio-1-formulario-de-login-)
    - [Ejercicio 2: Formulario de suscripción a newsletter ⭐⭐](#ejercicio-2-formulario-de-suscripción-a-newsletter-)
    - [Ejercicio 3: Formulario de reserva completo ⭐⭐⭐](#ejercicio-3-formulario-de-reserva-completo-)
  - [🔍 Buenas Prácticas](#-buenas-prácticas)


## 📖 Descripción

Los formularios son elementos fundamentales en la web moderna que permiten la interacción entre usuarios y aplicaciones. A través de ellos, los usuarios pueden enviar datos, realizar búsquedas, registrarse, iniciar sesión y mucho más. En este día aprenderás los conceptos básicos de formularios HTML, incluyendo la estructura principal con `<form>`, los campos de entrada con `<input>`, y cómo crear formularios accesibles con `<label>`.

Dominar los formularios es esencial para crear aplicaciones web interactivas y funcionales que recojan información de los usuarios de manera efectiva.


## 🎯 Objetivos del Día

Al acabar este día podrás:

- Crear formularios HTML básicos con la etiqueta `<form>`
- Utilizar diferentes tipos de campos `<input>`
- Asociar correctamente etiquetas `<label>` con inputs
- Implementar atributos esenciales como `name`, `id`, `placeholder` y `required`
- Entender la diferencia entre los métodos GET y POST

## 📚 Conceptos Clave

### La estructura de un formulario

Un formulario HTML actúa como contenedor para todos los elementos interactivos que permiten recopilar información del usuario.


## Etiqueta `<form>`

La etiqueta `<form>` es el contenedor principal de todos los elementos del formulario. Define cómo y dónde se enviarán los datos.

```html
<form action="/procesar" method="post"> <!-- Elementos del formulario aquí --> </form> 
```

## Atributos principales de `<form>`

- action: Especifica la URL donde se enviarán los datos del formulario cuando se envíe.

```html
<form action="/registro">
```

- method: Define el método HTTP para enviar los datos. Los valores más comunes son:
    * GET: Los datos se envían en la URL (visibles). Útil para búsquedas.
    * POST: Los datos se envían en el cuerpo de la petición (ocultos). Recomendado para datos sensibles.

```html
<form method="post">
```

- name: Identifica el formulario (útil cuando hay múltiples formularios en una página).

```html
<form name="formulario-contacto">
```

## Etiqueta `<input>`

- El elemento `<input>` crea campos de entrada donde los usuarios pueden introducir datos. Es un elemento vacío (no tiene etiqueta de cierre).

```html
<input type="text" name="nombre" id="nombre">
```

### Atributos esenciales de `<input>`

  * type: Define el tipo de dato que aceptará el campo.
  * name: Identifica el campo cuando se envían los datos al servidor.
  * id: Identificador único del elemento, necesario para asociarlo con su `<label>`.
  * placeholder: Texto de ejemplo que aparece dentro del campo antes de que el usuario escriba.

```html
<input type="text" placeholder="Ejemplo: Juan Pérez">
```

  * value: Valor predeterminado del campo.
```html
<input type="text" value="Texto por defecto">
```

  * required: Hace que el campo sea obligatorio antes de enviar el formulario.

```html
<input type="text" required>
```
  * disabled: Desactiva el campo (no se puede editar ni enviar).

```html
<input type="text" disabled>
```

  * readonly: El campo es de solo lectura (no se puede editar pero sí se envía).

```html
<input type="text" readonly value="No editable">
```

## Etiqueta `<label>`

La etiqueta `<label>` proporciona una etiqueta descriptiva para un campo de formulario, mejorando la accesibilidad y usabilidad.

```html
<label for="nombre">Nombre completo:</label>
<input type="text" id="nombre" name="nombre">
```

### ¿Por qué usar `<label>`?
- Mejora la accesibilidad para usuarios con lectores de pantalla
- Al hacer clic en el label, se activa el campo asociado
- Hace que los formularios sean más fáciles de usar en dispositivos móviles
- Nota importante: El atributo for del `<label>` debe coincidir exactamente con el id del `<input>` asociado.

## Tipos básicos de `<input>`

HTML5 proporciona múltiples tipos de input especializados que incluyen validación automática.

### type="text" - Texto simple
  - Campo de texto de una sola línea para texto general.
```html
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre" placeholder="Escribe tu nombre">
```

### type="password" - Contraseña
  - Campo para contraseñas donde los caracteres se ocultan automáticamente.
```html
<label for="pass">Contraseña:</label>
<input type="password" id="pass" name="pass" placeholder="Mínimo 8 caracteres">
```

### type="email" - Correo electrónico
  - Campo especializado para direcciones de email con validación automática del formato.

```html
<label for="correo">Email:</label>
<input type="email" id="correo" name="correo" placeholder="ejemplo@email.com">
```

### type="number" - Número
  - Campo para valores numéricos con controles de incremento/decremento.

```html
<label for="edad">Edad:</label>
<input type="number" id="edad" name="edad" min="18" max="100">
```

### type="tel" - Teléfono
  - Campo para números telefónicos.
```html
<label for="telefono">Teléfono:</label>
<input type="tel" id="telefono" name="telefono" placeholder="+34 600 000 000">
```

### type="url" - URL
- Campo para direcciones web con validación de formato de URL.

```html
<label for="web">Sitio web:</label>
<input type="url" id="web" name="web" placeholder="https://ejemplo.com">
```

### type="submit" - Botón de envío
  - Botón que envía el formulario.

```html
<input type="submit" value="Enviar">
```

### type="reset" - Botón de reseteo
  - Botón que restablece todos los campos del formulario a sus valores iniciales.

```html
<input type="reset" value="Limpiar">
```

## 💻 Ejemplos Prácticos

### Ejemplo 1: Formulario básico de contacto

```html
<form action="/enviar-contacto" method="post">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" placeholder="Tu nombre" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="tu@email.com" required>
  
  <input type="submit" value="Enviar">
</form>
```

### Ejemplo 2: Formulario de registro

```html
<form action="/registro" method="post" name="registro-usuario">
  <label for="usuario">Nombre de usuario:</label>
  <input type="text" id="usuario" name="usuario" placeholder="Usuario123" required>
  
  <label for="correo">Correo electrónico:</label>
  <input type="email" id="correo" name="correo" placeholder="ejemplo@mail.com" required>
  
  <label for="password">Contraseña:</label>
  <input type="password" id="password" name="password" placeholder="Mínimo 8 caracteres" required>
  
  <label for="edad">Edad:</label>
  <input type="number" id="edad" name="edad" min="18" max="120" required>
  
  <input type="submit" value="Crear cuenta">
  <input type="reset" value="Borrar todo">
</form>
```

### Ejemplo 3: Formulario de búsqueda

```html
<form action="/buscar" method="get">
  <label for="busqueda">Buscar:</label>
  <input type="text" id="busqueda" name="q" placeholder="¿Qué estás buscando?">
  
  <input type="submit" value="Buscar">
</form>
```

### Ejemplo 4: Formulario con diferentes tipos de input

```html
<form action="/procesar" method="post">
  <label for="nombre-completo">Nombre completo:</label>
  <input type="text" id="nombre-completo" name="nombre" required>
  
  <label for="email-contacto">Email:</label>
  <input type="email" id="email-contacto" name="email" required>
  
  <label for="telefono-movil">Teléfono:</label>
  <input type="tel" id="telefono-movil" name="telefono" placeholder="+34 123456789">
  
  <label for="sitio-web">Sitio web:</label>
  <input type="url" id="sitio-web" name="website" placeholder="https://tusitio.com">
  
  <label for="num-personas">Número de personas:</label>
  <input type="number" id="num-personas" name="personas" min="1" max="10" value="1">
  
  <input type="submit" value="Enviar formulario">
</form>
``` 

## ✏️ Ejercicios del Día
### Ejercicio 1: Formulario de login ⭐
Crea un formulario de inicio de sesión simple que incluya campos para nombre de usuario (text), contraseña (password) y un botón de envío. Todos los campos deben ser obligatorios y tener placeholders apropiados.

[Solución](ejercicio1.html)

### Ejercicio 2: Formulario de suscripción a newsletter ⭐⭐
Crea un formulario de suscripción que incluya campos para nombre (text), email (email) y un botón de suscripción. El formulario debe usar el método GET y todos los campos deben tener sus respectivos <label> correctamente asociados.

[Solución](ejercicio2.html)

### Ejercicio 3: Formulario de reserva completo ⭐⭐⭐
Crea un formulario de reserva de hotel que incluya los siguientes campos: nombre completo (text, requerido), email (email, requerido), teléfono (tel), número de huéspedes (number, mínimo 1, máximo 6), sitio web opcional (url), y botones de enviar y resetear. Usa placeholders descriptivos en todos los campos y asegúrate de que cada input tenga su label asociado correctamente.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas
* Siempre asocia cada <input> con un <label> usando los atributos for e id.
* Usa el atributo required para campos obligatorios en lugar de depender solo de JavaScript.
* Elige el tipo de input más apropiado para cada campo (email, tel, number, etc.) para aprovechar la validación nativa.
* Proporciona placeholder con ejemplos claros del formato esperado.
* Usa nombres descriptivos en el atributo name para facilitar el procesamiento en el servidor.
* El método GET es apropiado para búsquedas; usa POST para datos sensibles o grandes cantidades de información.
* No uses placeholder como sustituto de <label>; ambos tienen funciones diferentes.
* Agrupa campos relacionados visualmente para mejorar la experiencia del usuario.
* Proporciona feedback visual para campos obligatorios (puedes usar CSS más adelante).
* Verifica que tus formularios sean accesibles usando herramientas de validación y lectores de pantalla.

<h4 align="center"> <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-08">Día 8</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-10">Día 10</a> </h4>