# Día 1: Introducción a HTML

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## Índice del curos.
* [Objetivo](#Objetivo)
* [Que es html](#qué-es-html)
* [Ejemplo](#Ejemplo)

## 📖 Descripción

HTML (HyperText Markup Language) es el lenguaje de marcado estándar para crear páginas web. Es la base fundamental de todo sitio web en Internet y define la estructura y el contenido de las páginas. HTML no es un lenguaje de programación, sino un lenguaje de marcado que utiliza etiquetas para describir el contenido.

En este primer día aprenderás la estructura básica de un documento HTML, comprenderás cada uno de sus componentes esenciales y crearás tu primera página web funcional.

<a name="Objetivo"></a>

## 🎯 Objetivos del Día

Al finalizar este día serás capaz de:
- Comprender qué es HTML y para qué se utiliza
- Conocer la estructura básica de un documento HTML5
- Identificar las etiquetas fundamentales: `<!DOCTYPE>`, `<html>`, `<head>`, `<body>`
- Crear tu primer documento HTML válido

## 📚 Conceptos Clave

<a name="Que-es-html"></a>
### ¿Qué es HTML?

HTML son las siglas de **HyperText Markup Language** (Lenguaje de Marcado de Hipertexto). Es el código que se utiliza para estructurar y desplegar contenido en la web. El contenido puede ser estructurado en párrafos, listas, imágenes, tablas de datos, entre otros.

### Estructura Básica de un Documento HTML

Todo documento HTML5 sigue una estructura estándar que consta de cinco elementos fundamentales[web:25]:

1. **`<!DOCTYPE html>`** - Declaración del tipo de documento
2. **`<html>`** - Elemento raíz
3. **`<head>`** - Metadatos del documento
4. **`<title>`** - Título de la página
5. **`<body>`** - Contenido visible

### 1. Declaración DOCTYPE

```html
<!DOCTYPE html>
```


La declaración `<!DOCTYPE html>` debe ser la primera línea de cada documento HTML[web:21][web:25]. Le indica al navegador que el documento está escrito en HTML5, la versión más reciente del estándar HTML[web:28].

### 2. Elemento `<html>`

```html
<html lang="es"> ```
```

El elemento <html> es el elemento raíz que contiene todo el documento HTML[web:21]. El atributo lang="es" especifica el idioma del contenido (en este caso, español), lo cual es importante para los motores de búsqueda y la accesibilidad.

### 3. Elemento <head>

El elemento <head> contiene metadatos sobre el documento que no se muestran directamente en la página[web:21][web:25]. Incluye:

<meta charset="UTF-8"> - Define la codificación de caracteres (UTF-8 soporta la mayoría de caracteres de todos los idiomas)[web:21][web:26]

<meta name="viewport"> - Controla el diseño en dispositivos móviles[web:21]

<title> - Define el título que aparece en la pestaña del navegador[web:25][web:26]

### 4. Elemento <body>

```html
<body>
    <!-- Aquí va el contenido visible de la página -->
</body>
```

El elemento <body> contiene todo el contenido visible de la página web: texto, imágenes, enlaces, videos, etc

<a name="Ejemplo"></a>

### 💻 Ejemplos Prácticos

#### Ejemplo 1: Documento HTML Mínimo
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Primera Página</title>
</head>
<body>
    <h1>¡Hola Mundo!</h1>
    <p>Esta es mi primera página web en HTML.</p>
</body>
</html>
```

Explicación: Este es el documento HTML más básico posible. Incluye la declaración DOCTYPE, los elementos raíz, la cabecera con metadatos básicos, y el cuerpo con un encabezado y un párrafo

#### Ejemplo 2: Documento HTML Completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página de inicio del curso de HTML">
    <meta name="author" content="Tu Nombre">
    <title>Curso de HTML - Día 1</title>
</head>
<body>
    <h1>Bienvenido al Curso de HTML</h1>
    <p>En este curso aprenderás HTML desde cero en 30 días.</p>
    <p>HTML es el lenguaje fundamental para crear sitios web.</p>
</body>
</html>
```

Explicación: Este ejemplo incluye metadatos adicionales como description (descripción de la página) y author (autor), que son útiles para SEO y documentación.

### ✏️ Ejercicios del Día

#### Ejercicio 1: Crear tu Primera Página HTML ⭐
Objetivo: Crear un documento HTML básico con la estructura correcta.

Instrucciones:
```
- Crea un archivo llamado mi-primera-pagina.html
- Escribe la estructura básica HTML5 con <!DOCTYPE html>
- Añade un <title> con tu nombre
- En el <body>, incluye un encabezado <h1> con el texto "Mi Primera Página Web"
- Añade un párrafo <p> con una breve descripción sobre ti
- Pista: Recuerda incluir la etiqueta <meta charset="UTF-8"> para evitar problemas con caracteres especiales.
```
[Solución](mi-primera-pagina.html)

#### Ejercicio 2: Página de Presentación ⭐⭐
Objetivo: Crear una página HTML con metadatos completos.

Requisitos:
```
- Estructura HTML5 válida
- Atributo lang configurado en español
- Meta etiquetas: charset, viewport, description y author
- Título descriptivo
- Al menos 2 encabezados (<h1> y <h2>)
- Al menos 3 párrafos con contenido
```
[Solución](ejercicio2.html)

### 🎓 Resumen
- HTML es el lenguaje de marcado estándar para crear páginas web
- Todo documento HTML5 comienza con <!DOCTYPE html>
- La estructura básica incluye: <html>, <head>, <title> y <body>
- El <head> contiene metadatos no visibles, mientras que <body> contiene el contenido visible
- Los metadatos como charset, viewport y title son esenciales para un documento HTML válido


<h4 align="center">[INICIO](../README.md) || [DIA 2](./dia-02)</h4>