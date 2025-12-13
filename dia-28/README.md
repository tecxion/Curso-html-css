<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-27">Día 27</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-29">Día 29</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml28.png">
</h1>

# Día 28: Tipografía y Colores

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-2%20horas-blue)

## Índice
* [Objetivo](#objetivo)
* [Propiedades de Fuentes](#fuentes)
* [Google Fonts](#google-fonts)
* [Propiedades de Texto](#texto)
* [Unidades en CSS](#unidades)
* [Sistemas de Color](#colores)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

La tipografía y el color son dos de los aspectos más importantes del diseño web. Una buena tipografía mejora la legibilidad y la experiencia del usuario, mientras que una paleta de colores bien elegida puede transmitir emociones y reforzar la identidad de marca. En este día aprenderás a controlar todos los aspectos de la tipografía y el color en CSS.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

- Dominar las propiedades de fuentes (font-family, size, weight, style)
- Integrar Google Fonts en tus proyectos
- Controlar propiedades de texto (align, decoration, transform, spacing)
- Comprender y usar diferentes unidades CSS (px, em, rem, %, vh, vw)
- Trabajar con sistemas de color (hex, rgb, rgba, hsl, hsla)
- Crear diseños tipográficos atractivos

<a name="fuentes"></a>

## 🔤 Propiedades de Fuentes

### font-family

Define la familia de fuentes a usar. Siempre incluye fuentes de respaldo.

```css
p {
    font-family: 'Helvetica', Arial, sans-serif;
}
```

**Familias genéricas:**
- `serif` - Con remates (Times New Roman)
- `sans-serif` - Sin remates (Arial, Helvetica)
- `monospace` - Ancho fijo (Courier)
- `cursive` - Cursiva (Comic Sans)
- `fantasy` - Decorativa

### font-size

Tamaño de la fuente.

```css
h1 { font-size: 2.5rem; }
p { font-size: 16px; }
small { font-size: 0.875em; }
```

### font-weight

Grosor de la fuente (100-900 o palabras clave).

```css
p { font-weight: normal; }    /* 400 */
strong { font-weight: bold; }  /* 700 */
h1 { font-weight: 300; }       /* Light */
```

**Valores:** `100`, `200`, `300`, `400` (normal), `500`, `600`, `700` (bold), `800`, `900`

### font-style

Estilo de la fuente.

```css
em { font-style: italic; }
p { font-style: normal; }
```

### Shorthand font

```css
p {
    font: italic bold 16px/1.5 'Arial', sans-serif;
    /* style weight size/line-height family */
}
```

<a name="google-fonts"></a>

## 🌐 Google Fonts

Google Fonts ofrece cientos de fuentes gratuitas.

**Paso 1:** Visita [fonts.google.com](https://fonts.google.com)

**Paso 2:** Selecciona una fuente y copia el enlace:

```html
<head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
```

**Paso 3:** Usa la fuente en CSS:

```css
body {
    font-family: 'Roboto', sans-serif;
}
```

**Fuentes populares:**
- Roboto, Open Sans, Lato (sans-serif modernas)
- Montserrat, Poppins, Inter (sans-serif elegantes)
- Merriweather, Playfair Display (serif elegantes)
- Fira Code, Source Code Pro (monospace para código)

<a name="texto"></a>

## 📝 Propiedades de Texto

### text-align

Alineación horizontal del texto.

```css
h1 { text-align: center; }
p { text-align: justify; }
/* left | right | center | justify */
```

### text-decoration

Decoración del texto.

```css
a { text-decoration: none; }
del { text-decoration: line-through; }
u { text-decoration: underline; }
```

### text-transform

Transformación de mayúsculas/minúsculas.

```css
h1 { text-transform: uppercase; }
p { text-transform: capitalize; }
/* uppercase | lowercase | capitalize | none */
```

### line-height

Altura de línea (espaciado vertical entre líneas).

```css
p {
    line-height: 1.6;  /* 1.6 veces el tamaño de fuente */
}
```

**Buena práctica:** 1.5-1.8 para texto de párrafo.

### letter-spacing

Espaciado entre letras.

```css
h1 {
    letter-spacing: 2px;
}
```

### word-spacing

Espaciado entre palabras.

```css
p {
    word-spacing: 3px;
}
```

<a name="unidades"></a>

## 📏 Unidades en CSS

### Unidades Absolutas

**px (píxeles):** Unidad fija.
```css
p { font-size: 16px; }
```

### Unidades Relativas

**em:** Relativo al tamaño de fuente del elemento padre.
```css
div { font-size: 16px; }
p { font-size: 1.5em; }  /* 24px */
```

**rem:** Relativo al tamaño de fuente del elemento raíz (`<html>`).
```css
html { font-size: 16px; }
h1 { font-size: 2rem; }  /* 32px */
p { font-size: 1rem; }   /* 16px */
```

**% (porcentaje):** Relativo al elemento padre.
```css
div { width: 50%; }
```

**vh (viewport height):** 1vh = 1% de la altura del viewport.
```css
section { height: 100vh; }  /* Altura completa de la pantalla */
```

**vw (viewport width):** 1vw = 1% del ancho del viewport.
```css
div { width: 50vw; }  /* 50% del ancho de la pantalla */
```

**Recomendación:** Usa `rem` para tamaños de fuente (escalabilidad) y `px` para bordes/sombras.

<a name="colores"></a>

## 🎨 Sistemas de Color

### Nombres de Colores

```css
p { color: red; }
div { background-color: lightblue; }
```

### Hexadecimal

```css
h1 { color: #667eea; }
p { color: #333; }
```

### RGB

```css
div { background-color: rgb(102, 126, 234); }
```

### RGBA (con transparencia)

```css
div { background-color: rgba(102, 126, 234, 0.5); }
```

### HSL (Hue, Saturation, Lightness)

```css
h1 { color: hsl(240, 75%, 66%); }
```

### HSLA (con transparencia)

```css
div { background-color: hsla(240, 75%, 66%, 0.8); }
```

### Propiedades de Color

```css
p {
    color: #333;                    /* Color del texto */
    background-color: #f0f0f0;      /* Color de fondo */
    border-color: #667eea;          /* Color del borde */
}
```

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Tipografía con Google Fonts

```html
<head>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            font-size: 16px;
            line-height: 1.6;
            color: #333;
        }
        
        h1 {
            font-size: 3rem;
            font-weight: 600;
            letter-spacing: -1px;
        }
        
        p {
            font-weight: 300;
        }
    </style>
</head>
```

### Ejemplo 2: Paleta de Colores

```css
:root {
    --primary: #667eea;
    --secondary: #764ba2;
    --accent: #f093fb;
    --text: #333;
    --bg: #f8f9fa;
}

body {
    background-color: var(--bg);
    color: var(--text);
}

.button {
    background-color: var(--primary);
    color: white;
}
```

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día

### Ejercicio 1: Tipografía básica ⭐
Crea una página con un artículo que incluya título, subtítulo y 3 párrafos. Integra Google Fonts (elige 2 fuentes: una para títulos, otra para texto). Aplica: font-size de 2.5rem al título, 1.5rem al subtítulo, 1rem a párrafos, line-height de 1.8 en párrafos, letter-spacing de 1px en el título, y text-align justify en párrafos.

[Solución](ejercicio1.html)

### Ejercicio 2: Paleta de colores y unidades ⭐⭐
Crea una landing page con header, 3 secciones y footer. Define una paleta de 3 colores usando variables CSS (--primary, --secondary, --accent). Usa: rem para tamaños de fuente, vh para altura del header (100vh), vw para anchos de elementos, y rgba para fondos semi-transparentes. Cada sección debe tener un color de fondo diferente de tu paleta.

[Solución](ejercicio2.html)

### Ejercicio 3: Diseño tipográfico completo ⭐⭐⭐
Crea una página de revista digital con: header con título y navegación, artículo principal con título grande, subtítulo, autor, fecha, imagen destacada y 5 párrafos con diferentes estilos (primer párrafo con drop cap usando ::first-letter, citas destacadas, texto resaltado), sidebar con artículos relacionados, y footer. Usa: 3 Google Fonts diferentes, variables CSS para colores y tamaños, todas las unidades aprendidas (rem, em, vh, vw, %), propiedades de texto avanzadas (text-transform, letter-spacing, word-spacing), y una paleta de colores armoniosa con al menos 5 colores.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa máximo 2-3 fuentes diferentes en un proyecto
- Mantén una jerarquía tipográfica clara (h1 > h2 > h3 > p)
- Line-height de 1.5-1.8 para texto de párrafo
- Usa `rem` para tamaños de fuente (mejor accesibilidad)
- Limita tu paleta de colores a 3-5 colores principales
- Asegura suficiente contraste entre texto y fondo (WCAG AA: 4.5:1)
- Usa variables CSS para colores y tamaños repetidos
- Carga solo los pesos de fuente que necesites de Google Fonts
- Considera la legibilidad en dispositivos móviles
- Usa `preconnect` para mejorar la carga de Google Fonts

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-27">Día 27</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-29">Día 29</a>
</h4>
