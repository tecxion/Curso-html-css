<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-01">Día 1</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-03">Día 3</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml2.png">
</h1>

# Día 2: Etiquetas de Texto

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

### Índice Día 2

* [Concepto](#concepto)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

Las etiquetas de texto son fundamentales para estructurar y dar formato al contenido de una página web. HTML proporciona elementos específicos para encabezados, párrafos, énfasis y formato de texto que no solo controlan la apariencia visual, sino que también añaden significado semántico al contenido.

En este día aprenderás a utilizar los elementos de texto más importantes, comprenderás la diferencia entre etiquetas semánticas y visuales, y dominarás la jerarquía de encabezados que es crucial para la accesibilidad y el SEO.

## 🎯 Objetivos del Día

Al finalizar este día serás capaz de:
- Crear encabezados jerárquicos del `<h1>` al `<h6>`
- Estructurar contenido usando párrafos `<p>`
- Aplicar énfasis y formato a texto con etiquetas semánticas
- Diferenciar entre etiquetas semánticas (`<strong>`, `<em>`) y visuales (`<b>`, `<i>`)
- Utilizar saltos de línea y líneas horizontales apropiadamente

<a name="concepto"></a>

## 📚 Conceptos Clave

### Encabezados HTML (h1 - h6)

HTML ofrece seis niveles de encabezados, desde `<h1>` (el más importante) hasta `<h6>` (el menos importante). Estos elementos crean una jerarquía visual y semántica en tu contenido.

```html
<h1>Encabezado Principal</h1> <h2>Subencabezado</h2> <h3>Sub-subencabezado</h3> <h4>Encabezado de Nivel 4</h4> <h5>Encabezado de Nivel 5</h5> <h6>Encabezado de Nivel 6</h6> ```
```

#### Reglas importantes sobre encabezados:

- Usa solo un `<h1>` por página (generalmente para el título principal)
- No saltes niveles (no uses `<h4>` después de `<h2>`)
- Los encabezados representan la estructura del contenido, no solo el tamaño visual
- Son cruciales para SEO y accesibilidad

#### Párrafos
El elemento `<p>` define un párrafo de texto. Los párrafos son elementos de bloque, lo que significa que automáticamente añaden espacios antes y después.

```html
<p>Este es un párrafo completo de texto.</p>
<p>Este es otro párrafo separado del anterior.</p>
```

#### Énfasis y Texto Importante
Etiquetas Semánticas (Recomendadas)
- `<strong>`: Indica importancia fuerte, típicamente en negrita.
- `<em>`: Indica énfasis, típicamente en cursiva.

```html
<p>Este texto es <strong>muy importante</strong>.</p>
<p>Esto está <em>enfatizado</em>.</p>
```

La diferencia entre `<em>` y `<strong>` es significativa: `<em>` cambia el significado de una frase mediante énfasis vocal, mientras que `<strong>` añade importancia o urgencia al contenido.

##### Etiquetas Visuales (Solo Apariencia)
-`<b>`: Texto en negrita sin importancia semántica.
-`<i>`: Texto en cursiva sin énfasis semántico.

```html
<p>Este texto está en <b>negrita</b> solo visualmente.</p>
<p>Este texto está en <i>cursiva</i> solo visualmente.</p>
```

Recomendación: Usa etiquetas semánticas (`<strong>, <em>`) cuando quieras dar significado al texto, y etiquetas visuales (`<b>, <i>`) solo para estilo sin significado especial.

#### Otras Etiquetas de Formato
```html
<!-- Texto marcado/resaltado -->
<mark>Texto resaltado</mark>

<!-- Texto pequeño (letras pequeñas, avisos legales) -->
<small>Texto pequeño</small>

<!-- Texto eliminado -->
<del>Texto eliminado</del>

<!-- Texto insertado -->
<ins>Texto insertado</ins>

<!-- Subíndice -->
<p>H<sub>2</sub>O</p>

<!-- Superíndice -->
<p>E = mc<sup>2</sup></p>
```

#### Saltos de Línea y Líneas Horizontales
```html
<!-- Salto de línea -->
<p>Primera línea<br>Segunda línea</p>

<!-- Línea horizontal -->
<hr>
```

El elemento `<br>` inserta un salto de línea simple, mientras que <hr> crea una línea horizontal temática que separa contenido.

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Estructura de Artículo
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Artículo de Ejemplo</title>
</head>
<body>
    <h1>La Importancia del HTML Semántico</h1>
    
    <h2>Introducción</h2>
    <p>
        El HTML semántico es <strong>fundamental</strong> para crear 
        sitios web accesibles y optimizados. No se trata solo de cómo 
        se ve el contenido, sino de <em>qué significa</em>.
    </p>
    
    <h2>Beneficios Principales</h2>
    
    <h3>Accesibilidad</h3>
    <p>
        Los lectores de pantalla utilizan la estructura semántica para 
        ayudar a usuarios con discapacidades visuales a navegar el contenido.
    </p>
    
    <h3>SEO</h3>
    <p>
        Los motores de búsqueda comprenden mejor la <strong>jerarquía</strong> 
        y la importancia del contenido cuando usas etiquetas semánticas correctamente.
    </p>
</body>
</html>
```
Explicación: Este ejemplo muestra una jerarquía correcta de encabezados (h1 > h2 > h3) y el uso apropiado de `<strong>` y `<em>` para dar significado al texto.

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día

### Ejercicio 1: Página de Receta ⭐
Objetivo: Crear una página de receta usando encabezados y párrafos correctamente.

Instrucciones:
- Crea un archivo receta.html
- Usa un <h1> para el nombre de la receta
- Usa <h2> para secciones: "Ingredientes" y "Preparación"
- Usa párrafos <p> para las instrucciones
- Aplica <strong> a palabras clave importantes

Pista: Una buena jerarquía de encabezados ayuda a los usuarios a escanear rápidamente el contenido.

[Solución](receta.html)

### Ejercicio 2: Blog Post con Formato ⭐⭐
Objetivo: Crear una entrada de blog utilizando diversos elementos de formato de texto.

Requisitos:

- Título principal con `<h1>`
- Al menos 3 niveles de encabezados (h1, h2, h3)
- Mínimo 5 párrafos
- Usar `<strong>` y `<em>` apropiadamente
- Incluir `<mark>` para resaltar información importante
- Usar `<small>` para una nota al pie
- Separar secciones con `<hr>`

[Solución](blog.html)

### Ejercicio 3: Documento Académico ⭐⭐⭐
Objetivo: Crear un documento académico completo con formato profesional.

Instrucciones:
- Crea un documento sobre un tema científico o matemático
- Usa jerarquía de encabezados completa (h1-h4)
- Incluye fórmulas con `<sub>` y `<sup>`
- Muestra correcciones con `<del>` e `<ins>`
- Diferencia claramente entre `<strong>/<em>` y `<b>/<i>`
- Añade citas textuales apropiadas
- Usa saltos de línea `<br>` solo donde sea semánticamente correcto

[Solución](academico.html)

### 🎓 Resumen
- HTML tiene 6 niveles de encabezados (`<h1>` a `<h6>`) que crean jerarquía
- Los párrafos `<p>` son elementos de bloque que estructuran el texto
- `<strong>` y `<em>` son etiquetas semánticas que añaden significado
- `<b>` e `<i>` son etiquetas visuales sin significado semántico adicional
- Elementos como `<mark>, <small>, <del>, <ins>, <sub> y <sup>` añaden formato específico
- Una estructura semántica correcta mejora la accesibilidad y el SEO


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-03">Día 3</a>
</h4>


### Listas de etiquetas

```html
<!-- Elementos de Linea-->
<a> - Crear un enlace
<abbr> - Crear una abreviatura
<acronym> - Crear un acrónimo
<audio> - Crear o insertar un audio
<b> - Poner en negrita
<bdo> - Invertir un texto
<big> - Aumentar el tamaño del texto
<br> - Crear un salto de línea
<button> - Crear un botón
<cite> - Añadir cita
<code> - Escribir código en HTML
<dfn> - Escribir una definición usando HTML
<em> - Enfatizar
<i> - Poner en cursiva
<img> - Crear una imagen
<input> - Crear un campo de entrada
<kbd> - Definir entradas de teclado
<label> - Crear una etiqueta para los campos de entrada
<map> - Definir un mapa de imagen
<object> - Representar un recurso externo utilizado para multimedia, como audios, vídeos, imágenes, PDF, etc.
<output> - Representar el resultado de un cálculo
<q> - Abreviatura Cita
<samp> - Representa una salida de muestra
<script> - Escribir código JS
<select> - Seleccionar elementos
<small> - Escribir textos pequeños
<span> - Marcar o separar un texto
<strong> - Darle mayor importancia al texto
<sub> - Crear subíndice
<sup> - Crear superíndice
<textarea> - Crear un área de texto
<time> - Representa un período de tiempo específico
<tt> - Representar teletipo en línea
<var> - Define una variable
```
```html
<!--Elementos de bloque -->
<address></address> - Permite escribir información relacionada con una dirección.
<article></article> - Permite escribir artículos en una sección.
<aside></aside> - Permite crear una sección indirectamente relacionada con el documento.
<blockquote></blockquote> - Para crear texto como comillas.
<canvas></canvas> - Para crear canbas.
<dd></dd> - Para describir un término o nombre en una lista de descripciones.
<div></div> - Para crear una sección o cuadro.
<dl></dl> - Para crear una lista de descripciones.
<dt></dt> - Para describir un término en una lista de descripciones.
<fieldset></fieldset> - Para crear elementos relacionados en un formulario.
<figcaption></figcaption> - Para definir el título de una figura.
<figure></figure> - Para envolver una figura, diagrama, etc.
<footer></footer> - Para crear el pie de página de un documento.
<form> - Para crear un formulario.
<h1></h1> a <h6></h6> - a Crear encabezados de diferentes tamaños
<header></header> - Para crear el encabezado de un documento
<hr /> - Para crear una línea horizontal
<li></li> - Para crear una lista ordenada o desordenada
<main></main> - Para ajustar el contenido principal del documento
<nav><nav> - Para crear la navegación
<noscript></noscript> - Para describir un contenido alternativo que se mostrará a los usuarios cuando JavaScript esté deshabilitado en sus navegadores.
<ol></ol> - Para crear una lista ordenada
<p></p> - Para crear un párrafo
<pre></pre> - Para crear un contenido con espacios, por ejemplo, un poema
<section><section> - Para crear una sección
<table></table> - Para crear una tabla
<tfoot><tfoot> - Para crear un pie de tabla
<ul><ul> - Para ajustar o desordenar la lista
<video></video> - Para crear un video
```