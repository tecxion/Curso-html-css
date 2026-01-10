<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-17">Día 17</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-19">Día 19</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml18.png">
</h1>

# Día 18: Meta Etiquetas y SEO

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)

## 📖 Descripción

Las meta etiquetas son elementos HTML que proporcionan metadatos sobre la página web. Son fundamentales para el SEO (Search Engine Optimization) y para controlar cómo se muestra tu sitio en redes sociales y motores de búsqueda.

## 🎯 Objetivos del Día

- Comprender qué son las meta etiquetas y su importancia
- Implementar meta etiquetas esenciales para SEO
- Configurar Open Graph para redes sociales
- Utilizar Twitter Cards
- Optimizar páginas web para motores de búsqueda

## Meta Etiquetas Esenciales

### Charset

Define la codificación de caracteres:

```html
<meta charset="UTF-8">
```

### Viewport

Esencial para diseño responsive:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Description

Descripción que aparece en resultados de búsqueda:

```html
<meta name="description" content="Aprende HTML y CSS desde cero con nuestro curso completo de 30 días. Tutoriales, ejemplos y ejercicios prácticos.">
```

**Mejores prácticas:**
- Longitud: 150-160 caracteres
- Incluye palabras clave relevantes
- Describe claramente el contenido
- Única para cada página

### Keywords

Palabras clave (menos importante actualmente):

```html
<meta name="keywords" content="HTML, CSS, desarrollo web, tutorial, curso">
```

### Author

Autor del contenido:

```html
<meta name="author" content="Juan Pérez">
```

### Robots

Controla la indexación:

```html
<!-- Permitir indexación y seguimiento de enlaces -->
<meta name="robots" content="index, follow">

<!-- No indexar esta página -->
<meta name="robots" content="noindex, nofollow">
```

## Open Graph (Facebook, LinkedIn)

Meta etiquetas para compartir en redes sociales:

```html
<!-- Título -->
<meta property="og:title" content="Curso de HTML y CSS - 30 Días">

<!-- Descripción -->
<meta property="og:description" content="Aprende desarrollo web desde cero con nuestro curso completo">

<!-- Imagen -->
<meta property="og:image" content="https://ejemplo.com/imagen.jpg">

<!-- URL -->
<meta property="og:url" content="https://ejemplo.com/curso-html">

<!-- Tipo de contenido -->
<meta property="og:type" content="website">

<!-- Nombre del sitio -->
<meta property="og:site_name" content="Academia Web">

<!-- Idioma -->
<meta property="og:locale" content="es_ES">
```

## Twitter Cards

Meta etiquetas específicas para Twitter:

```html
<!-- Tipo de tarjeta -->
<meta name="twitter:card" content="summary_large_image">

<!-- Usuario de Twitter del sitio -->
<meta name="twitter:site" content="@usuario">

<!-- Título -->
<meta name="twitter:title" content="Curso de HTML y CSS">

<!-- Descripción -->
<meta name="twitter:description" content="Aprende desarrollo web desde cero">

<!-- Imagen -->
<meta name="twitter:image" content="https://ejemplo.com/imagen.jpg">
```

## Ejemplo Completo de Head Optimizado

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <!-- Charset y Viewport -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Título -->
  <title>Curso de HTML y CSS - Aprende Desarrollo Web en 30 Días</title>
  
  <!-- Meta SEO -->
  <meta name="description" content="Curso completo de HTML y CSS desde cero. 30 días de tutoriales, ejemplos prácticos y ejercicios para dominar el desarrollo web.">
  <meta name="keywords" content="HTML, CSS, desarrollo web, curso, tutorial, programación">
  <meta name="author" content="Academia Web">
  <meta name="robots" content="index, follow">
  
  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://ejemplo.com/curso-html-css">
  <meta property="og:title" content="Curso de HTML y CSS - 30 Días">
  <meta property="og:description" content="Aprende desarrollo web desde cero con nuestro curso completo de HTML y CSS">
  <meta property="og:image" content="https://ejemplo.com/images/curso-preview.jpg">
  <meta property="og:site_name" content="Academia Web">
  <meta property="og:locale" content="es_ES">
  
  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:url" content="https://ejemplo.com/curso-html-css">
  <meta name="twitter:title" content="Curso de HTML y CSS - 30 Días">
  <meta name="twitter:description" content="Aprende desarrollo web desde cero">
  <meta name="twitter:image" content="https://ejemplo.com/images/curso-preview.jpg">
  <meta name="twitter:site" content="@academiaweb">
  
  <!-- Favicon -->
  <link rel="icon" type="image/png" href="/favicon.png">
  <link rel="apple-touch-icon" href="/apple-touch-icon.png">
  
  <!-- Canonical URL -->
  <link rel="canonical" href="https://ejemplo.com/curso-html-css">
  
  <!-- Stylesheet -->
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Contenido de la página -->
</body>
</html>
```

## Mejores Prácticas de SEO

### 1. Título de la Página

```html
<title>Palabra Clave Principal - Palabra Secundaria | Nombre del Sitio</title>
```

- Longitud: 50-60 caracteres
- Incluye palabras clave principales
- Único para cada página
- Descriptivo y atractivo

### 2. Estructura de Encabezados

```html
<h1>Solo un H1 por página - Título Principal</h1>
<h2>Subtítulo de Sección</h2>
<h3>Subsección</h3>
```

- Solo un `<h1>` por página
- Jerarquía lógica (h1 → h2 → h3)
- Incluye palabras clave relevantes

### 3. Enlaces Internos y Externos

```html
<!-- Enlace interno -->
<a href="/otra-pagina">Texto descriptivo del enlace</a>

<!-- Enlace externo -->
<a href="https://ejemplo.com" rel="noopener noreferrer" target="_blank">Sitio externo</a>
```

### 4. Imágenes Optimizadas

```html
<img src="imagen.jpg" alt="Descripción detallada de la imagen" width="800" height="600" loading="lazy">
```

- Siempre incluye atributo `alt`
- Usa nombres de archivo descriptivos
- Optimiza el tamaño de las imágenes
- Usa `loading="lazy"` para imágenes below the fold

## ✏️ Ejercicios

### Ejercicio 1: Página con SEO básico
Crea una página HTML con todas las meta etiquetas esenciales para SEO.

### Ejercicio 2: Optimización para redes sociales
Crea una página optimizada para compartir en Facebook y Twitter con Open Graph y Twitter Cards.

### Ejercicio 3: Blog post optimizado
Crea un artículo de blog completamente optimizado para SEO con estructura correcta de encabezados, meta etiquetas y contenido semántico.

## 🎯 Resumen

- Las meta etiquetas son esenciales para SEO
- `description` y `title` son las más importantes
- Open Graph optimiza para redes sociales
- Twitter Cards mejora la apariencia en Twitter
- La estructura semántica ayuda al SEO

## 📚 Recursos adicionales

- [Google SEO Starter Guide](https://developers.google.com/search/docs/beginner/seo-starter-guide)
- [Open Graph Protocol](https://ogp.me/)
- [Twitter Cards Documentation](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards)
- [MDN - Meta Tags](https://developer.mozilla.org/es/docs/Web/HTML/Element/meta)

---

**¡Continúa aprendiendo!** Mañana veremos caracteres especiales y entidades HTML.
