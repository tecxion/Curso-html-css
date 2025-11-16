<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-10">Día 10</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-12">Día 12</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml11.png">
</h1>

# Día 11: Formularios Parte 3 - Validación HTML5

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Indice

- [Día 11: Formularios Parte 3 - Validación HTML5](#día-11-formularios-parte-3---validación-html5)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [Validación nativa del navegador](#validación-nativa-del-navegador)
  - [Atributo `required`](#atributo-required)
  - [Atributos de longitud de texto](#atributos-de-longitud-de-texto)
    - [`minlength` - Longitud mínima](#minlength---longitud-mínima)
    - [`maxlength` - Longitud máxima](#maxlength---longitud-máxima)
    - [Combinando minlength y maxlength](#combinando-minlength-y-maxlength)
  - [Atributos para valores numéricos](#atributos-para-valores-numéricos)
    - [`min` - Valor mínimo](#min---valor-mínimo)
    - [`max` - Valor máximo](#max---valor-máximo)
    - [`step` - Incrementos permitidos](#step---incrementos-permitidos)
    - [Ejemplos combinados](#ejemplos-combinados)
  - [Atributo `pattern` - Expresiones regulares](#atributo-pattern---expresiones-regulares)
    - [Sintaxis básica de expresiones regulares](#sintaxis-básica-de-expresiones-regulares)
    - [Ejemplos comunes de pattern](#ejemplos-comunes-de-pattern)
    - [Atributo `title` con pattern](#atributo-title-con-pattern)
  - [Tipos de input especializados con validación automática](#tipos-de-input-especializados-con-validación-automática)
    - [`type="email"` - Correo electrónico](#typeemail---correo-electrónico)
    - [`type="url"` - URL](#typeurl---url)
    - [`type="number"` - Número](#typenumber---número)
    - [`type="date"` - Fecha](#typedate---fecha)
    - [`type="time"` - Hora](#typetime---hora)
    - [`type="range"` - Rango](#typerange---rango)
    - [`type="color"` - Color](#typecolor---color)
  - [💻 Ejemplos Prácticos](#-ejemplos-prácticos)
    - [Ejemplo 1: Formulario de registro con validaciones básicas](#ejemplo-1-formulario-de-registro-con-validaciones-básicas)
    - [Ejemplo 2: Validación con pattern y expresiones regulares](#ejemplo-2-validación-con-pattern-y-expresiones-regulares)
    - [Ejemplo 3: Formulario de reserva con validaciones de fecha](#ejemplo-3-formulario-de-reserva-con-validaciones-de-fecha)
    - [Ejemplo 4: Contraseña segura con validación avanzada](#ejemplo-4-contraseña-segura-con-validación-avanzada)
    - [Ejemplo 5: Formulario completo con múltiples validaciones](#ejemplo-5-formulario-completo-con-múltiples-validaciones)
  - [✏️ Ejercicios del Día](#️-ejercicios-del-día)
    - [Ejercicio 1: Formulario de contacto validado ⭐](#ejercicio-1-formulario-de-contacto-validado-)
    - [Ejercicio 2: Formulario de datos personales con pattern ⭐⭐](#ejercicio-2-formulario-de-datos-personales-con-pattern-)
    - [Ejercicio 3: Sistema de registro completo con validación avanzada ⭐⭐⭐](#ejercicio-3-sistema-de-registro-completo-con-validación-avanzada-)
  - [🔍 Buenas Prácticas](#-buenas-prácticas)


## 📖 Descripción

La validación de formularios es fundamental para garantizar que los usuarios proporcionen información correcta y en el formato esperado. HTML5 introdujo un potente sistema de validación nativa que permite validar datos del lado del cliente sin necesidad de JavaScript. En este día aprenderás a utilizar los atributos de validación más importantes como `required`, `min`, `max`, `minlength`, `maxlength`, y `pattern`, además de conocer tipos de input especializados que incluyen validación automática.

Con la validación HTML5 mejorarás la experiencia del usuario al proporcionar feedback inmediato sobre errores en los datos, reducirás la carga del servidor validando antes de enviar, y crearás formularios más robustos y profesionales.


## 🎯 Objetivos del Día

Al acabar este día podrás:

- Hacer campos obligatorios con el atributo `required`
- Controlar la longitud de texto con `minlength` y `maxlength`
- Validar rangos numéricos con `min` y `max`
- Crear validaciones personalizadas con `pattern` y expresiones regulares
- Utilizar tipos de input especializados con validación automática
- Mejorar la experiencia del usuario con mensajes de validación nativos

## 📚 Conceptos Clave

### Validación nativa del navegador

HTML5 permite validar formularios directamente en el navegador sin necesidad de JavaScript, proporcionando feedback inmediato al usuario antes de enviar los datos al servidor.


## Atributo `required`

El atributo `required` es el más básico y fundamental. Hace que un campo sea obligatorio: el formulario no se puede enviar si este campo está vacío.

```html
<input type="text" name="nombre" required>
```

Se puede aplicar a:
- `<input>` (la mayoría de tipos)
- `<textarea>`
- `<select>`

```html

<label for="email">Email (obligatorio):</label>
<input type="email" id="email" name="email" required>

<label for="mensaje">Mensaje (obligatorio):</label>
<textarea id="mensaje" name="mensaje" required></textarea>

<label for="pais">País (obligatorio):</label>
<select id="pais" name="pais" required>

<option value="">-- Selecciona --</option>
<option value="es">España</option>
<option value="mx">México</option>
</select>

```

**Nota importante:** La primera opción de un `<select>` con atributo `required` debe tener un `value` vacío para que la validación funcione correctamente.


## Atributos de longitud de texto

Estos atributos controlan el número de caracteres permitidos en campos de texto.

### `minlength` - Longitud mínima

Especifica el número mínimo de caracteres que debe tener el campo.

```html

<input type="text" name="usuario" minlength="3" required>
```

### `maxlength` - Longitud máxima

Especifica el número máximo de caracteres permitidos. A diferencia de `minlength`, este atributo impide físicamente escribir más caracteres.

```html

<input type="text" name="usuario" maxlength="20">
```

### Combinando minlength y maxlength

```html
<label for="usuario">Nombre de usuario (3-15 caracteres):</label>

<input type="text" id="usuario" name="usuario" 
       minlength="3" maxlength="15" required>

<label for="password">Contraseña (8-20 caracteres):</label>

<input type="password" id="password" name="password" 
       minlength="8" maxlength="20" required>

```

Estos atributos funcionan con:
- `<input type="text">`
- `<input type="email">`
- `<input type="password">`
- `<input type="url">`
- `<input type="tel">`
- `<textarea>`


## Atributos para valores numéricos

Estos atributos permiten controlar rangos de números y fechas.

### `min` - Valor mínimo

Especifica el valor mínimo aceptado.

```html

<input type="number" name="edad" min="18">
<input type="date" name="fecha" min="2025-01-01">
```

### `max` - Valor máximo

Especifica el valor máximo aceptado.

```html

<input type="number" name="edad" max="100">
<input type="date" name="fecha" max="2025-12-31">
```

### `step` - Incrementos permitidos

Define los incrementos válidos entre valores. Útil para números decimales o intervalos específicos.

```html

<!-- Solo acepta múltiplos de 5 -->
<input type="number" name="cantidad" min="0" max="100" step="5">
<!-- Permite decimales de 0.01 (para precios) -->
<input type="number" name="precio" min="0" step="0.01">
<!-- Solo números pares -->
<input type="number" name="par" min="0" step="2">
```

### Ejemplos combinados


```html
<label for="edad">Edad (18-65 años):</label>

<input type="number" id="edad" name="edad" 
       min="18" max="65" required>

<label for="precio">Precio ($0.00 - $9999.99):</label>

<input type="number" id="precio" name="precio" 
       min="0" max="9999.99" step="0.01" required>

<label for="fecha-nacimiento">Fecha de nacimiento:</label>

<input type="date" id="fecha-nacimiento" name="fecha" 
       min="1950-01-01" max="2007-12-31" required>

```

## Atributo `pattern` - Expresiones regulares

El atributo `pattern` permite definir un patrón de validación personalizado usando expresiones regulares (regex). Es la herramienta más poderosa y flexible para validación.

```html
<input type="text" name="codigo" pattern="[A-Z]{3}[0-9]{4}">
```

### Sintaxis básica de expresiones regulares

- `[A-Z]` - Una letra mayúscula
- `[a-z]` - Una letra minúscula
- `[0-9]` - Un dígito
- `[A-Za-z]` - Una letra (mayúscula o minúscula)
- `{n}` - Exactamente n repeticiones
- `{n,m}` - Entre n y m repeticiones
- `+` - Una o más repeticiones
- `*` - Cero o más repeticiones
- `^` - Inicio de la cadena
- `$` - Final de la cadena
- `.` - Cualquier carácter
- `|` - O (alternativa)

### Ejemplos comunes de pattern

**Código postal español (5 dígitos):**

```html
<input type="text" name="cp" pattern="[0-9]{5}" 
       placeholder="28001" required>
```

**DNI español (8 dígitos y una letra):**
```html
<input type="text" name="dni" pattern="[0-9]{8}[A-Z]" 
       placeholder="12345678A" required>
```

**Teléfono móvil español:**
```html
<input type="tel" name="movil" pattern="[6-7][0-9]{8}" 
       placeholder="612345678" required>
```

**Solo letras (sin números ni símbolos):**
```html
<input type="text" name="nombre" pattern="[A-Za-záéíóúÁÉÍÓÚñÑ\s]+" 
       placeholder="Juan García" required>
```

**Nombre de usuario (letras, números, guión y guión bajo):**
```html
<input type="text" name="usuario" pattern="[A-Za-z0-9_-]{3,16}" 
       placeholder="usuario_123" required>
```

**Contraseña fuerte (mínimo 8 caracteres, al menos una mayúscula, una minúscula y un número):**
```html
<input type="password" name="password" 
       pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" 
       title="Mínimo 8 caracteres, con al menos una mayúscula, una minúscula y un número" 
       required>
```

**Matrícula de coche española:**
```html
<input type="text" name="matricula" pattern="[0-9]{4}[A-Z]{3}" 
       placeholder="1234ABC" required>
```

### Atributo `title` con pattern

El atributo `title` proporciona un mensaje personalizado que se muestra cuando la validación falla.

```html
<input type="text" name="codigo-postal" pattern="[0-9]{5}" 
       title="Debe ser un código postal válido de 5 dígitos" 
       placeholder="28001" required>
```

## Tipos de input especializados con validación automática

HTML5 incluye tipos de input que proporcionan validación automática sin necesidad de atributos adicionales.

### `type="email"` - Correo electrónico

Valida automáticamente el formato de email.

```html
<input type="email" name="correo" required>
```

### `type="url"` - URL

Valida automáticamente que sea una URL válida (debe empezar con http://, https://, etc.).

```html
<input type="url" name="sitio-web" placeholder="https://ejemplo.com" required>
```

### `type="number"` - Número

Solo acepta valores numéricos.

```html
<input type="number" name="cantidad" min="1" max="100" required>
```

### `type="date"` - Fecha

Proporciona un selector de fecha nativo del navegador.

```html
<input type="date" name="fecha-nacimiento" min="1900-01-01" max="2007-12-31" required>
```

### `type="time"` - Hora

Selector de hora nativo.

```html
<input type="time" name="hora-cita" min="09:00" max="18:00" required>
```

### `type="range"` - Rango

Control deslizante para seleccionar valores numéricos.

```html
<label for="volumen">Volumen (0-100):</label>

<input type="range" id="volumen" name="volumen" min="0" max="100" value="50">
```

### `type="color"` - Color

Selector de color nativo.

```html
<label for="color-favorito">Color favorito:</label>

<input type="color" id="color-favorito" name="color" value="#ff0000">
```


## 💻 Ejemplos Prácticos

### Ejemplo 1: Formulario de registro con validaciones básicas

```html

<form action="/registro" method="post">

  <label for="usuario">Usuario (3-15 caracteres):</label>

  <input type="text" id="usuario" name="usuario" 
         minlength="3" maxlength="15" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="password">Contraseña (mínimo 8 caracteres):</label>
  <input type="password" id="password" name="password" 
         minlength="8" required>
  

  <label for="edad">Edad (18-100):</label>

  <input type="number" id="edad" name="edad" 
         min="18" max="100" required>
  
  <button type="submit">Registrarse</button>
</form>
```

### Ejemplo 2: Validación con pattern y expresiones regulares

```html
<form action="/validar" method="post">
  <label for="dni">DNI (8 dígitos + letra mayúscula):</label>
  <input type="text" id="dni" name="dni" 
         pattern="[0-9]{8}[A-Z]" 
         placeholder="12345678A"
         title="Formato: 8 números seguidos de una letra mayúscula" 
         required>
  
  <label for="cp">Código Postal (5 dígitos):</label>
  <input type="text" id="cp" name="cp" 
         pattern="[0-9]{5}" 
         placeholder="28001"
         title="Debe contener exactamente 5 dígitos" 
         required>
  
  <label for="telefono">Teléfono móvil español:</label>
  <input type="tel" id="telefono" name="telefono" 
         pattern="[6-7][0-9]{8}" 
         placeholder="612345678"
         title="Debe empezar por 6 o 7 y tener 9 dígitos en total" 
         required>
  
  <button type="submit">Enviar</button>
</form>
```

### Ejemplo 3: Formulario de reserva con validaciones de fecha

```html
<form action="/reservar" method="post">
  <label for="nombre">Nombre completo:</label>
  <input type="text" id="nombre" name="nombre" 
         pattern="[A-Za-záéíóúÁÉÍÓÚñÑ\s]+" 
         title="Solo se permiten letras y espacios" 
         required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="fecha-entrada">Fecha de entrada:</label>

  <input type="date" id="fecha-entrada" name="fecha-entrada" 
         min="2025-11-17" max="2025-12-31" required>
  

  <label for="fecha-salida">Fecha de salida:</label>

  <input type="date" id="fecha-salida" name="fecha-salida" 
         min="2025-11-18" max="2026-01-15" required>
  
  <label for="huespedes">Número de huéspedes (1-6):</label>
  <input type="number" id="huespedes" name="huespedes" 
         min="1" max="6" value="2" required>
  
  <button type="submit">Reservar ahora</button>
</form>
```

### Ejemplo 4: Contraseña segura con validación avanzada

```html
<form action="/cambiar-password" method="post">

  <label for="password-actual">Contraseña actual:</label>

  <input type="password" id="password-actual" name="password-actual" required>
  

  <label for="password-nueva">Nueva contraseña:</label>

  <input type="password" id="password-nueva" name="password-nueva" 
         pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" 
         title="Mínimo 8 caracteres, al menos una mayúscula, una minúscula y un número" 
         required>
  
  <label for="password-confirmar">Confirmar contraseña:</label>
  <input type="password" id="password-confirmar" name="password-confirmar" 
         pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" 
         required>
  
  <button type="submit">Cambiar contraseña</button>
</form>
```

### Ejemplo 5: Formulario completo con múltiples validaciones

```html
<form action="/suscripcion" method="post">
  <fieldset>
    <legend>Datos personales</legend>
    
    <label for="nombre">Nombre (solo letras):</label>
    <input type="text" id="nombre" name="nombre" 
           pattern="[A-Za-záéíóúÁÉÍÓÚñÑ\s]+" 
           minlength="2" maxlength="50" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="web">Sitio web (opcional):</label>
    <input type="url" id="web" name="web" placeholder="https://tusitio.com">
    

    <label for="fecha-nacimiento">Fecha de nacimiento:</label>

    <input type="date" id="fecha-nacimiento" name="fecha-nacimiento" 
           min="1950-01-01" max="2007-12-31" required>
  </fieldset>
  
  <fieldset>
    <legend>Preferencias</legend>
    
    <label for="frecuencia">Frecuencia de emails (días):</label>
    <input type="number" id="frecuencia" name="frecuencia" 
           min="1" max="30" value="7" step="1" required>
    

    <label for="color-tema">Color del tema:</label>

    <input type="color" id="color-tema" name="color-tema" value="#3498db">
  </fieldset>
  
  <button type="submit">Suscribirse</button>
  <button type="reset">Limpiar</button>
</form>
```

## ✏️ Ejercicios del Día

### Ejercicio 1: Formulario de contacto validado ⭐
Crea un formulario de contacto que incluya: nombre (obligatorio, solo letras, 2-50 caracteres), email (obligatorio), teléfono (opcional, 9 dígitos) y mensaje (obligatorio, mínimo 10 caracteres). Usa los atributos de validación apropiados.

[Solución](ejercicio1.html)

### Ejercicio 2: Formulario de datos personales con pattern ⭐⭐
Crea un formulario que valide: DNI español (8 números + letra mayúscula), código postal (5 dígitos), teléfono móvil (9 dígitos empezando por 6 o 7), y fecha de nacimiento (entre 1950 y 2007). Incluye atributos `title` con instrucciones claras y `placeholder` con ejemplos.

[Solución](ejercicio2.html)

### Ejercicio 3: Sistema de registro completo con validación avanzada ⭐⭐⭐
Crea un formulario completo de registro que incluya: nombre de usuario (3-15 caracteres, solo letras, números, guión y guión bajo), email, contraseña segura (mínimo 8 caracteres con mayúscula, minúscula y número), confirmación de contraseña (mismo patrón), edad (18-100), fecha de registro (solo fechas futuras desde hoy), número de referidos (0-999), URL del perfil de LinkedIn (opcional), y color favorito. Usa `<fieldset>` para agrupar secciones, incluye validaciones con `pattern` donde sea necesario, y asegúrate de que todos los campos obligatorios tengan mensajes de error personalizados con `title`.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa `required` para todos los campos obligatorios en lugar de depender solo de JavaScript.
- Combina `minlength` y `maxlength` para establecer rangos de caracteres claros.
- Siempre usa `min` y `max` con campos numéricos y de fecha para limitar valores.
- Proporciona el atributo `title` cuando uses `pattern` para explicar el formato esperado.
- Usa `placeholder` con ejemplos realistas del formato correcto.
- Elige el tipo de `input` más específico posible (`email`, `url`, `tel`, etc.) para obtener validación automática.
- No confíes únicamente en la validación del cliente; siempre valida también en el servidor.
- Prueba tus expresiones regulares cuidadosamente antes de implementarlas.
- Usa `step` con números decimales para controlar la precisión (ej: `step="0.01"` para precios).
- Agrupa validaciones relacionadas visualmente con `<fieldset>` y `<legend>`.
- Considera la experiencia del usuario: mensajes de error claros son esenciales.
- Recuerda que la validación HTML5 puede ser deshabilitada; usa `novalidate` solo para testing.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-10">Día 10</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-12">Día 12</a>
</h4>