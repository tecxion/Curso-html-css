<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-16">Día 16</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-18">Día 18</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml17.png">
</h1>

# Día 17: Elementos Embebidos - iframe y embed

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

Los elementos `<iframe>` y `<embed>` permiten incrustar contenido externo en tus páginas web, como videos de YouTube, mapas de Google, documentos PDF y otros recursos multimedia. Aprenderás a usarlos correctamente y las consideraciones de seguridad importantes.

## 🎯 Objetivos del Día

- Utilizar `<iframe>` para embeber contenido externo
- Comprender los atributos de seguridad de iframe
- Embeber videos de YouTube, Vimeo y otros servicios
- Integrar mapas de Google Maps
- Conocer las mejores prácticas y consideraciones de seguridad

## Elemento `<iframe>`

El elemento `<iframe>` (inline frame) crea un marco en línea que incrusta otro documento HTML dentro del documento actual.

### Sintaxis básica

```html
<iframe src="https://ejemplo.com" width="600" height="400">
  Tu navegador no soporta iframes.
</iframe>
```

### Atributos principales

- **`src`**: URL del contenido a embeber
- **`width`** y **`height`**: Dimensiones del iframe
- **`title`**: Descripción del contenido (importante para accesibilidad)
- **`loading`**: Control de carga (`lazy` o `eager`)
- **`sandbox`**: Restricciones de seguridad
- **`allow`**: Permisos para características específicas

### Atributos de seguridad

```html
<iframe 
  src="https://ejemplo.com"
  sandbox="allow-scripts allow-same-origin"
  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
  loading="lazy"
  title="Descripción del contenido">
</iframe>
```

**Valores de `sandbox`:**
- `allow-forms`: Permite envío de formularios
- `allow-scripts`: Permite ejecución de scripts
- `allow-same-origin`: Permite acceso al mismo origen
- `allow-popups`: Permite ventanas emergentes
- `allow-modals`: Permite modales

### Embeber video de YouTube

```html
<iframe 
  width="560" 
  height="315" 
  src="https://www.youtube.com/embed/VIDEO_ID" 
  title="Título del video"
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen>
</iframe>
```

### Iframe responsive

```html
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe 
    src="https://www.youtube.com/embed/VIDEO_ID"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>
```

### Google Maps

```html
<iframe 
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3037.6!2d-3.7037902!3d40.4167754!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDI1JzAwLjQiTiAzwrA0MicxMy42Ilc!5e0!3m2!1ses!2ses!4v1234567890"
  width="600" 
  height="450" 
  style="border:0;" 
  allowfullscreen="" 
  loading="lazy"
  title="Mapa de ubicación">
</iframe>
```

## 💻 Ejemplos Prácticos

### Ejemplo 1: Página con video embebido

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tutorial en Video</title>
</head>
<body>
  <article>
    <h1>Tutorial: Introducción a HTML</h1>
    
    <div style="position: relative; padding-bottom: 56.25%; height: 0;">
      <iframe 
        src="https://www.youtube.com/embed/dQw4w9WgXcQ"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
        title="Tutorial de HTML"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
    </div>
    
    <p>En este tutorial aprenderás los fundamentos de HTML...</p>
  </article>
</body>
</html>
```

### Ejemplo 2: Página de contacto con mapa

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Contacto</title>
</head>
<body>
  <h1>Contáctanos</h1>
  
  <section>
    <h2>Nuestra ubicación</h2>
    <iframe 
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3037.6!2d-3.7037902!3d40.4167754"
      width="100%" 
      height="450" 
      style="border:0;" 
      allowfullscreen="" 
      loading="lazy"
      title="Ubicación de nuestra oficina">
    </iframe>
  </section>
  
  <section>
    <h2>Información de contacto</h2>
    <p>Email: info@ejemplo.com</p>
    <p>Teléfono: +34 123 456 789</p>
  </section>
</body>
</html>
```

## ⚠️ Consideraciones de Seguridad

1. **Usa `sandbox`**: Limita las capacidades del contenido embebido
2. **Especifica `title`**: Mejora la accesibilidad
3. **Valida el origen**: Solo embebe contenido de fuentes confiables
4. **Usa HTTPS**: Siempre que sea posible
5. **Implementa CSP**: Content Security Policy para mayor seguridad

## ✏️ Ejercicios

### Ejercicio 1: Embeber video de YouTube
Crea una página con un video de YouTube embebido de forma responsive.

### Ejercicio 2: Página de contacto con mapa
Crea una página de contacto que incluya un mapa de Google Maps y información de contacto.

### Ejercicio 3: Galería multimedia
Crea una página con múltiples iframes: videos, mapas y otros contenidos embebidos.

## 🎯 Resumen

- `<iframe>` permite embeber contenido externo
- Usa atributos de seguridad como `sandbox`
- Siempre incluye `title` para accesibilidad
- Haz los iframes responsive con CSS
- Ten cuidado con la seguridad al embeber contenido de terceros

## 📚 Recursos adicionales

- [MDN - iframe](https://developer.mozilla.org/es/docs/Web/HTML/Element/iframe)
- [YouTube Embed API](https://developers.google.com/youtube/iframe_api_reference)
- [Google Maps Embed API](https://developers.google.com/maps/documentation/embed)

---

**¡Continúa aprendiendo!** Mañana veremos meta etiquetas y SEO.
