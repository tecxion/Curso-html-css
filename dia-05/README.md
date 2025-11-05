<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-04">Día 4</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-06">Día 6</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml5.png">
</h1>

# Día 6: Imágenes - Etiqueta `<img>`, atributos `src` y `alt`, optimización de imágenes

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)


## Indice
* [Objetivo](#objetivo)
* [Atributo src](#atrisrc)
* [Atributo alt](#atrialt)
* [Optimización](#optimizacion)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)


## 📖 Descripción

Las imágenes son elementos fundamentales para hacer las páginas web más atractivas y comunicar visualmente ideas o información. En HTML, la etiqueta `<img>` permite insertar imágenes en tu documento. Es un elemento vacío, lo que significa que no tiene etiqueta de cierre y se escribe con un solo tag.

Los dos atributos más importantes para la etiqueta `<img>` son:

- `src`: indica la ruta o URL de la imagen a mostrar.
- `alt`: proporciona un texto alternativo que describe la imagen, esencial para la accesibilidad y SEO.

Además, hablaremos brevemente sobre cómo optimizar imágenes para mejorar la carga y experiencia del usuario.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Insertar imágenes usando la etiqueta `<img>`
- Utilizar correctamente los atributos `src` y `alt`
- Entender la importancia del texto alternativo para accesibilidad
- Conocer buenas prácticas para optimizar imágenes en la web

## 📚 Conceptos Clave

### La etiqueta `<img>`

La etiqueta HTML para imágenes es:

```html
<img src="ruta-de-la-imagen" alt="Descripción de la imagen">
```
Porque es un elemento vacío, no necesita etiqueta de cierre.

<a name="atrisrc"></a>

### Atributo src

El atributo `src` (source) indica la ubicación de la imagen. Puede ser una ruta relativa (en tu proyecto) o una URL absoluta (en Internet). Ejemplos:

```html
<img src="imagenes/foto.jpg" alt="Foto descriptiva">
<img src="https://ejemplo.com/logo.png" alt="Logo del sitio">
```

Si el archivo no se encuentra, el navegador mostrará el texto del atributo alt en su lugar.

<a name="atrialt"></a>

### Atributo alt
El atributo alt (alternative text) es fundamental para describir la imagen cuando esta no puede cargarse o para asistentes de lectura (por ejemplo, personas con discapacidad visual que usan lectores de pantalla).

Ejemplo:
```html
<img src="perro.jpg" alt="Perro jugando en el parque">
```
El texto en alt debe ser breve pero descriptivo y relevante al contexto de la imagen, ayudando a entender su contenido o función.

#### ¿Por qué es importante el atributo alt?
- Mejora la accesibilidad: lectores de pantalla leen el texto para personas con discapacidad visual.
- Ayuda a SEO: los motores de búsqueda pueden indexar imágenes si tienen texto alternativo adecuado.
- Proporciona información cuando la imagen no carga.
- Si la imagen es decorativa y no aporta información, se recomienda poner alt="" (atributo vacío) para que sea ignorada por lectores de pantalla.

<a name="optimizacion"></a>

## Optimización básica de imágenes

- Usa imágenes comprimidas en formatos adecuados (JPEG para fotos, PNG para gráficos con pocos colores, WebP para web moderna).
- Controla el tamaño con atributos width y height para evitar desplazamientos durante la carga.
- Usa imágenes de tamaño adecuado, ni demasiado grandes ni demasiado pequeñas.
- Considera la carga diferida (loading="lazy") para mejorar el rendimiento cuando hay muchas imágenes.

Ejemplo básico con optimización:
```html
<img src="imagenes/logo.webp" alt="Logo del sitio" width="200" height="100" loading="lazy">
```
<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Imagen simple
```html
<img src="imagenes/playa.jpg" alt="Vista de una playa al atardecer">
```

### Ejemplo 2: Logo con dimensiones y carga diferida

```html
<img src="imagenes/logo.png" alt="Logo de la empresa" width="150" height="50" loading="lazy">
```

### Ejemplo 3: Imagen decorativa (sin alt, para accesibilidad)

```html
<img src="imagenes/fondo-degradado.jpg" alt="" role="presentation">
```

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día


### Ejercicio 1: Inserta una imagen básica ⭐
Crea un archivo HTML con una imagen usando `<img>`. Usa una imagen de tu equipo o una URL pública. Añade un texto alt descriptivo.

[Solución](ejercicio1.html)

### Ejercicio 2: Imagen con atributos de tamaño y carga diferida ⭐⭐
Crea un HTML que incluya una imagen con width, height y loading="lazy". Observa cómo mejora la carga al tener varias imágenes (puedes duplicar la imagen).

[Solución](ejercicio2.html)

### Ejercicio 3: Diferencia entre imagen informativa y decorativa ⭐⭐⭐
Crea dos imágenes: una con alt descriptivo para contenido y otra con alt="" para imagen decorativa. Explica por qué es importante esta diferenciación.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas
- El atributo alt es obligatorio para accesibilidad y SEO.
- Describe la imagen concisamente en alt.
- Usa rutas relativas o absolutas válidas en src.
- Controla dimensiones para evitar cambios en la disposición durante la carga.
- Para imágenes no informativas, pon alt="" para ignorarlas en lectores de pantalla.
- Optimiza tamaño y formato para una carga rápida.
- Usa loading="lazy" para diferir carga de imágenes fuera de pantalla.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-04">Día 4</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-06">Día 6</a>
</h4>