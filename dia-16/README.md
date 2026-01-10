<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-15">Día 15</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-17">Día 17</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml16.png">
</h1>

# Día 16: Elementos Multimedia - Audio y Video

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)

## Índice
* [Objetivo](#objetivo)
* [Elemento audio](#audio)
* [Elemento video](#video)
* [Formatos y compatibilidad](#formatos)
* [Atributos comunes](#atributos)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

HTML5 introdujo elementos nativos para reproducir audio y video sin necesidad de plugins externos como Flash. Los elementos `<audio>` y `<video>` permiten incrustar contenido multimedia directamente en las páginas web de forma estándar y accesible.

En este día aprenderás a utilizar estos elementos, sus atributos, formatos soportados y mejores prácticas para ofrecer una experiencia multimedia óptima a tus usuarios.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Utilizar el elemento `<audio>` para reproducir archivos de audio
- Utilizar el elemento `<video>` para reproducir archivos de video
- Conocer los formatos de audio y video compatibles
- Implementar controles personalizados y nativos
- Proporcionar múltiples fuentes para compatibilidad
- Mejorar la accesibilidad con subtítulos y transcripciones
- Optimizar el rendimiento de contenido multimedia

## 📚 Conceptos Clave

<a name="audio"></a>

## Elemento `<audio>`

El elemento `<audio>` permite incrustar contenido de audio en una página web.

### Sintaxis básica

```html
<audio src="audio.mp3" controls>
  Tu navegador no soporta el elemento audio.
</audio>
```

### Atributos principales

- **`src`**: URL del archivo de audio
- **`controls`**: Muestra los controles de reproducción (play, pause, volumen)
- **`autoplay`**: Reproduce automáticamente al cargar (usar con precaución)
- **`loop`**: Reproduce en bucle continuo
- **`muted`**: Inicia silenciado
- **`preload`**: Indica cómo precargar el audio (`none`, `metadata`, `auto`)

### Ejemplo básico

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Tu navegador no soporta el elemento audio.
</audio>
```

### Múltiples fuentes

Para máxima compatibilidad, proporciona múltiples formatos:

```html
<audio controls preload="metadata">
  <source src="podcast.mp3" type="audio/mpeg">
  <source src="podcast.ogg" type="audio/ogg">
  <source src="podcast.wav" type="audio/wav">
  <p>Tu navegador no soporta audio HTML5. 
     <a href="podcast.mp3">Descarga el audio</a>
  </p>
</audio>
```

### Reproductor de audio personalizado

```html
<figure>
  <figcaption>Escucha nuestro último podcast:</figcaption>
  <audio controls src="podcast-episodio-15.mp3">
    Tu navegador no soporta el elemento audio.
  </audio>
</figure>
```

### Audio con descripción

```html
<article>
  <h2>Episodio 15: HTML Semántico</h2>
  <audio controls>
    <source src="episodio-15.mp3" type="audio/mpeg">
    <source src="episodio-15.ogg" type="audio/ogg">
  </audio>
  <p><strong>Duración:</strong> 45 minutos</p>
  <p><strong>Descripción:</strong> En este episodio exploramos el HTML semántico...</p>
</article>
```

<a name="video"></a>

## Elemento `<video>`

El elemento `<video>` permite incrustar contenido de video en una página web.

### Sintaxis básica

```html
<video src="video.mp4" controls width="640" height="360">
  Tu navegador no soporta el elemento video.
</video>
```

### Atributos principales

- **`src`**: URL del archivo de video
- **`controls`**: Muestra los controles de reproducción
- **`autoplay`**: Reproduce automáticamente (requiere `muted` en muchos navegadores)
- **`loop`**: Reproduce en bucle
- **`muted`**: Inicia silenciado
- **`poster`**: Imagen que se muestra antes de reproducir
- **`width`** y **`height`**: Dimensiones del video
- **`preload`**: Cómo precargar el video (`none`, `metadata`, `auto`)

### Ejemplo básico con poster

```html
<video controls width="640" height="360" poster="thumbnail.jpg">
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Tu navegador no soporta el elemento video.
</video>
```

### Video responsive

```html
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <video controls style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
  </video>
</div>
```

### Video con subtítulos

```html
<video controls width="640" height="360">
  <source src="pelicula.mp4" type="video/mp4">
  <source src="pelicula.webm" type="video/webm">
  
  <!-- Subtítulos en diferentes idiomas -->
  <track kind="subtitles" src="subtitulos-es.vtt" srclang="es" label="Español" default>
  <track kind="subtitles" src="subtitles-en.vtt" srclang="en" label="English">
  <track kind="subtitles" src="sous-titres-fr.vtt" srclang="fr" label="Français">
  
  <!-- Descripción de audio para accesibilidad -->
  <track kind="descriptions" src="descripcion.vtt" srclang="es" label="Descripción de audio">
  
  Tu navegador no soporta el elemento video.
</video>
```

### Video con figura y caption

```html
<figure>
  <video controls width="100%" poster="poster.jpg">
    <source src="tutorial.mp4" type="video/mp4">
    <source src="tutorial.webm" type="video/webm">
  </video>
  <figcaption>
    Tutorial: Cómo crear una página web con HTML5
  </figcaption>
</figure>
```

<a name="formatos"></a>

## Formatos y Compatibilidad

### Formatos de Audio

| Formato | Extensión | Tipo MIME | Compatibilidad |
|---------|-----------|-----------|----------------|
| MP3 | .mp3 | audio/mpeg | Excelente (todos los navegadores) |
| OGG Vorbis | .ogg | audio/ogg | Buena (Firefox, Chrome, Opera) |
| WAV | .wav | audio/wav | Buena (sin compresión, archivos grandes) |
| AAC | .aac, .m4a | audio/aac | Buena (Safari, Chrome) |

**Recomendación:** Usar MP3 como formato principal y OGG como alternativa.

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
</audio>
```

### Formatos de Video

| Formato | Extensión | Tipo MIME | Compatibilidad |
|---------|-----------|-----------|----------------|
| MP4 (H.264) | .mp4 | video/mp4 | Excelente (todos los navegadores modernos) |
| WebM | .webm | video/webm | Buena (Chrome, Firefox, Opera) |
| OGG Theora | .ogv | video/ogg | Moderada (Firefox, Chrome, Opera) |

**Recomendación:** Usar MP4 (H.264) como formato principal y WebM como alternativa.

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
</video>
```

<a name="atributos"></a>

## Atributos Comunes Detallados

### `controls`

Muestra los controles nativos del navegador (play, pause, volumen, progreso).

```html
<video src="video.mp4" controls></video>
```

### `autoplay`

Reproduce automáticamente. **Nota:** La mayoría de navegadores requieren `muted` para permitir autoplay.

```html
<!-- Autoplay funciona con muted -->
<video src="video.mp4" autoplay muted></video>

<!-- Autoplay puede ser bloqueado sin muted -->
<video src="video.mp4" autoplay></video>
```

### `loop`

Reproduce en bucle continuo.

```html
<video src="background.mp4" loop muted autoplay></video>
```

### `preload`

Controla cómo se precarga el contenido:

- **`none`**: No precarga nada (ahorra ancho de banda)
- **`metadata`**: Solo precarga metadatos (duración, dimensiones)
- **`auto`**: Precarga todo el archivo (por defecto)

```html
<!-- Bueno para páginas con muchos videos -->
<video src="video.mp4" controls preload="metadata"></video>

<!-- Para video de fondo que debe estar listo -->
<video src="hero.mp4" autoplay muted preload="auto"></video>
```

### `poster` (solo video)

Imagen que se muestra antes de reproducir el video.

```html
<video src="video.mp4" controls poster="thumbnail.jpg"></video>
```

### `muted`

Inicia el audio silenciado.

```html
<video src="video.mp4" controls muted></video>
```

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Reproductor de podcast

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Podcast - Desarrollo Web</title>
</head>
<body>
  <header>
    <h1>Podcast: Desarrollo Web Moderno</h1>
  </header>
  
  <main>
    <article>
      <h2>Episodio 15: HTML Semántico</h2>
      <p>Publicado el <time datetime="2025-01-08">8 de enero, 2025</time></p>
      
      <figure>
        <audio controls preload="metadata">
          <source src="episodio-15.mp3" type="audio/mpeg">
          <source src="episodio-15.ogg" type="audio/ogg">
          Tu navegador no soporta el elemento audio.
        </audio>
        <figcaption>Duración: 45 minutos</figcaption>
      </figure>
      
      <section>
        <h3>Descripción</h3>
        <p>En este episodio exploramos el HTML semántico y cómo utilizarlo correctamente...</p>
      </section>
      
      <section>
        <h3>Temas tratados</h3>
        <ul>
          <li>Elementos article, section y aside</li>
          <li>Mejores prácticas de HTML semántico</li>
          <li>Beneficios para SEO y accesibilidad</li>
        </ul>
      </section>
    </article>
  </main>
</body>
</html>
```

### Ejemplo 2: Galería de videos

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tutoriales en Video</title>
</head>
<body>
  <header>
    <h1>Tutoriales de Desarrollo Web</h1>
  </header>
  
  <main>
    <section>
      <h2>Últimos Tutoriales</h2>
      
      <article>
        <h3>Introducción a HTML5</h3>
        <video controls width="640" height="360" poster="html5-poster.jpg" preload="metadata">
          <source src="html5-intro.mp4" type="video/mp4">
          <source src="html5-intro.webm" type="video/webm">
          <track kind="subtitles" src="html5-es.vtt" srclang="es" label="Español" default>
          <track kind="subtitles" src="html5-en.vtt" srclang="en" label="English">
          Tu navegador no soporta el elemento video.
        </video>
        <p><strong>Duración:</strong> 15 minutos</p>
        <p>Aprende los fundamentos de HTML5 en este tutorial completo.</p>
      </article>
      
      <article>
        <h3>CSS Grid Layout</h3>
        <video controls width="640" height="360" poster="css-grid-poster.jpg" preload="metadata">
          <source src="css-grid.mp4" type="video/mp4">
          <source src="css-grid.webm" type="video/webm">
          <track kind="subtitles" src="css-grid-es.vtt" srclang="es" label="Español" default>
          Tu navegador no soporta el elemento video.
        </video>
        <p><strong>Duración:</strong> 22 minutos</p>
        <p>Domina CSS Grid con ejemplos prácticos.</p>
      </article>
    </section>
  </main>
</body>
</html>
```

### Ejemplo 3: Video de fondo (hero section)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Página con Video de Fondo</title>
  <style>
    .hero {
      position: relative;
      height: 100vh;
      overflow: hidden;
    }
    
    .hero-video {
      position: absolute;
      top: 50%;
      left: 50%;
      min-width: 100%;
      min-height: 100%;
      width: auto;
      height: auto;
      transform: translate(-50%, -50%);
      z-index: -1;
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
      color: white;
      text-align: center;
      padding-top: 40vh;
    }
  </style>
</head>
<body>
  <section class="hero">
    <video class="hero-video" autoplay muted loop playsinline>
      <source src="hero-background.mp4" type="video/mp4">
      <source src="hero-background.webm" type="video/webm">
    </video>
    
    <div class="hero-content">
      <h1>Bienvenido a Nuestro Sitio</h1>
      <p>Creando experiencias digitales increíbles</p>
      <button>Conoce más</button>
    </div>
  </section>
</body>
</html>
```

<a name="ejercicio"></a>

## ✏️ Ejercicios

### Ejercicio 1: Reproductor de audio básico
Crea una página con un reproductor de audio que incluya:
- Múltiples fuentes de audio (MP3 y OGG)
- Controles nativos
- Información sobre el audio (título, duración, descripción)

### Ejercicio 2: Galería de videos con subtítulos
Crea una galería de videos que incluya:
- Al menos 2 videos con controles
- Imágenes poster para cada video
- Subtítulos en español
- Descripciones de cada video

### Ejercicio 3: Página multimedia completa
Crea una página que combine audio y video:
- Sección de podcast con reproductor de audio
- Sección de tutoriales con videos
- Video de fondo en la sección hero
- Todo con accesibilidad (subtítulos, descripciones)

## 🎯 Resumen

- **`<audio>`**: Para reproducir archivos de audio
- **`<video>`**: Para reproducir archivos de video
- **`controls`**: Muestra controles nativos
- **`<source>`**: Proporciona múltiples formatos para compatibilidad
- **`<track>`**: Añade subtítulos y descripciones
- **Formatos recomendados:** MP3 para audio, MP4 para video

### Mejores Prácticas

1. ✅ Siempre proporciona múltiples formatos
2. ✅ Usa `preload="metadata"` para ahorrar ancho de banda
3. ✅ Incluye subtítulos para accesibilidad
4. ✅ Proporciona contenido alternativo para navegadores antiguos
5. ✅ Usa `poster` en videos para mejor experiencia
6. ❌ Evita `autoplay` con sonido (mala experiencia de usuario)
7. ❌ No uses archivos muy grandes sin optimizar

## 📚 Recursos adicionales

- [MDN - audio](https://developer.mozilla.org/es/docs/Web/HTML/Element/audio)
- [MDN - video](https://developer.mozilla.org/es/docs/Web/HTML/Element/video)
- [MDN - track](https://developer.mozilla.org/es/docs/Web/HTML/Element/track)
- [Can I Use - HTML5 Audio](https://caniuse.com/audio)
- [Can I Use - HTML5 Video](https://caniuse.com/video)

---

**¡Continúa aprendiendo!** Mañana veremos elementos embebidos (iframe y embed).


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-15">Día 15</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-17">Día 17</a>
</h4>