<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-25">Día 25</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-27">Día 27</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml26.png">
</h1>

# Día 26: Introducción a CSS3

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-2%20horas-blue)

## Índice
* [Objetivo](#objetivo)
* [¿Qué es CSS?](#que-es-css)
* [Sintaxis de CSS](#sintaxis)
* [Formas de aplicar CSS](#formas)
* [Selectores básicos](#selectores)
* [Especificidad](#especificidad)
* [Colores en CSS](#colores)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

CSS (Cascading Style Sheets u Hojas de Estilo en Cascada) es el lenguaje que se utiliza para dar estilo y diseño a las páginas web. Mientras que HTML se encarga de la estructura y el contenido, CSS se encarga de la presentación visual: colores, fuentes, espaciados, posicionamiento y mucho más.

En este día aprenderás los fundamentos de CSS3, la versión más moderna de CSS que incluye características avanzadas como gradientes, animaciones, transformaciones y mucho más. Dominar CSS es esencial para crear sitios web atractivos y profesionales.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Comprender qué es CSS y para qué sirve
- Conocer la sintaxis básica de CSS
- Aplicar CSS de tres formas diferentes (inline, interno, externo)
- Utilizar selectores básicos (elemento, clase, ID, universal, descendente)
- Entender el concepto de especificidad
- Trabajar con diferentes formatos de colores
- Crear tus primeras hojas de estilo

<a name="que-es-css"></a>

## 📚 ¿Qué es CSS?

CSS (Cascading Style Sheets) es un lenguaje de hojas de estilo que describe cómo se deben mostrar los elementos HTML en la pantalla, papel u otros medios.

### ¿Por qué usar CSS?

**Separación de contenido y presentación:**
- HTML se encarga del contenido y estructura
- CSS se encarga del diseño y presentación visual

**Ventajas de CSS:**

1. **Reutilización**: Un mismo archivo CSS puede estilizar múltiples páginas HTML
2. **Mantenimiento**: Cambiar el diseño de todo un sitio editando un solo archivo
3. **Rendimiento**: Los archivos CSS se cachean en el navegador
4. **Accesibilidad**: Permite crear diseños adaptables a diferentes dispositivos
5. **Consistencia**: Mantiene un diseño uniforme en todo el sitio

### Ejemplo visual

**Sin CSS:**
```html
<h1>Título</h1>
<p>Este es un párrafo.</p>
```
Resultado: Texto negro sobre fondo blanco, fuente predeterminada del navegador.

**Con CSS:**
```html
<h1 style="color: #667eea; font-size: 2.5rem;">Título</h1>
<p style="color: #555; line-height: 1.6;">Este es un párrafo.</p>
```
Resultado: Título morado grande, párrafo gris con mejor espaciado.

<a name="sintaxis"></a>

## 🔤 Sintaxis de CSS

La sintaxis de CSS sigue un patrón simple:

```css
selector {
    propiedad: valor;
    propiedad: valor;
}
```

### Componentes de una regla CSS

```css
h1 {
    color: blue;
    font-size: 24px;
}
```

- **Selector** (`h1`): Indica qué elemento(s) HTML se van a estilizar
- **Declaración** (`color: blue;`): Una propiedad y su valor
- **Propiedad** (`color`): El aspecto que queremos cambiar
- **Valor** (`blue`): El valor que queremos asignar a la propiedad
- **Bloque de declaraciones** (`{ ... }`): Conjunto de declaraciones entre llaves

### Reglas importantes

- Cada declaración termina con punto y coma (`;`)
- Las propiedades y valores se separan con dos puntos (`:`)
- Se pueden escribir múltiples declaraciones en una regla
- Los espacios en blanco y saltos de línea son ignorados (útil para legibilidad)

<a name="formas"></a>

## 🎨 Formas de aplicar CSS

Existen tres formas principales de aplicar CSS a un documento HTML:

### 1. CSS Inline (en línea)

Se aplica directamente en el elemento HTML usando el atributo `style`.

```html
<p style="color: red; font-size: 18px;">Texto en rojo de 18px</p>
```

**Ventajas:**
- Rápido para pruebas o cambios específicos
- Máxima prioridad (especificidad)

**Desventajas:**
- ❌ No es reutilizable
- ❌ Dificulta el mantenimiento
- ❌ Mezcla contenido con presentación
- ❌ **No recomendado para producción**

### 2. CSS Interno (en el `<head>`)

Se define dentro de una etiqueta `<style>` en el `<head>` del documento HTML.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Página</title>
    <style>
        h1 {
            color: blue;
            text-align: center;
        }
        p {
            color: gray;
            line-height: 1.6;
        }
    </style>
</head>
<body>
    <h1>Título</h1>
    <p>Párrafo de texto.</p>
</body>
</html>
```

**Ventajas:**
- Útil para estilos específicos de una sola página
- No requiere archivo externo

**Desventajas:**
- ❌ No se reutiliza en otras páginas
- ❌ Aumenta el tamaño del HTML

### 3. CSS Externo (archivo separado) ✅ **RECOMENDADO**

Se crea un archivo `.css` separado y se vincula al HTML con `<link>`.

**Archivo: styles.css**
```css
h1 {
    color: blue;
    text-align: center;
}

p {
    color: gray;
    line-height: 1.6;
}
```

**Archivo: index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Página</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Título</h1>
    <p>Párrafo de texto.</p>
</body>
</html>
```

**Ventajas:**
- ✅ Reutilizable en múltiples páginas
- ✅ Fácil mantenimiento
- ✅ Mejor organización del código
- ✅ Se cachea en el navegador (mejor rendimiento)
- ✅ **Mejor práctica profesional**

<a name="selectores"></a>

## 🎯 Selectores Básicos de CSS

Los selectores determinan a qué elementos HTML se aplicarán los estilos.

### 1. Selector de Elemento (Tipo)

Selecciona todos los elementos de un tipo específico.

```css
p {
    color: blue;
}

h1 {
    font-size: 2rem;
}
```

Aplica a **todos** los `<p>` y `<h1>` del documento.

### 2. Selector de Clase

Selecciona elementos con un atributo `class` específico. Se usa un punto (`.`) antes del nombre.

```html
<p class="destacado">Texto destacado</p>
<p>Texto normal</p>
<div class="destacado">Div destacado</div>
```

```css
.destacado {
    background-color: yellow;
    font-weight: bold;
}
```

**Características:**
- Puede aplicarse a múltiples elementos
- Un elemento puede tener múltiples clases: `class="destacado importante"`
- Reutilizable

### 3. Selector de ID

Selecciona un elemento con un atributo `id` específico. Se usa almohadilla (`#`) antes del nombre.

```html
<div id="cabecera">Cabecera principal</div>
```

```css
#cabecera {
    background-color: navy;
    color: white;
    padding: 20px;
}
```

**Características:**
- Un ID debe ser **único** en la página
- Mayor especificidad que las clases
- Útil para elementos únicos (cabecera, pie de página, etc.)

### 4. Selector Universal

Selecciona **todos** los elementos del documento. Se usa asterisco (`*`).

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Útil para resetear estilos por defecto del navegador.

### 5. Selector Descendente

Selecciona elementos que están dentro de otros elementos.

```html
<div class="contenedor">
    <p>Este párrafo está dentro del contenedor</p>
</div>
<p>Este párrafo NO está dentro del contenedor</p>
```

```css
.contenedor p {
    color: red;
}
```

Solo el primer `<p>` será rojo.

### 6. Agrupación de Selectores

Aplica los mismos estilos a múltiples selectores separándolos con comas.

```css
h1, h2, h3 {
    color: navy;
    font-family: Arial, sans-serif;
}
```

<a name="especificidad"></a>

## ⚖️ Especificidad en CSS

Cuando múltiples reglas CSS se aplican al mismo elemento, la **especificidad** determina cuál prevalece.

### Orden de especificidad (de menor a mayor):

1. **Selector de elemento**: `p { }`
2. **Selector de clase**: `.clase { }`
3. **Selector de ID**: `#id { }`
4. **Estilos inline**: `style="..."`
5. **!important**: `color: red !important;` (evitar usar)

### Ejemplo:

```html
<p id="especial" class="destacado" style="color: green;">Texto</p>
```

```css
p { color: blue; }              /* Especificidad: 1 */
.destacado { color: yellow; }   /* Especificidad: 10 */
#especial { color: red; }       /* Especificidad: 100 */
```

**Resultado:** El texto será **verde** (estilo inline tiene máxima prioridad).

Si quitamos el estilo inline, será **rojo** (ID tiene más especificidad que clase).

<a name="colores"></a>

## 🌈 Colores en CSS

CSS ofrece múltiples formas de especificar colores:

### 1. Nombres de colores

CSS tiene 140 nombres de colores predefinidos.

```css
h1 { color: red; }
p { color: blue; }
div { background-color: lightgray; }
```

**Ejemplos:** `red`, `blue`, `green`, `yellow`, `purple`, `orange`, `pink`, `brown`, `black`, `white`, `gray`

### 2. Hexadecimal (Hex)

Formato: `#RRGGBB` donde RR (rojo), GG (verde), BB (azul) son valores hexadecimales (00-FF).

```css
h1 { color: #FF0000; }      /* Rojo */
p { color: #00FF00; }       /* Verde */
div { color: #0000FF; }     /* Azul */
span { color: #667eea; }    /* Morado personalizado */
```

**Forma corta:** Si los pares son iguales: `#FF0000` = `#F00`

### 3. RGB

Formato: `rgb(rojo, verde, azul)` donde cada valor va de 0 a 255.

```css
h1 { color: rgb(255, 0, 0); }       /* Rojo */
p { color: rgb(0, 255, 0); }        /* Verde */
div { color: rgb(102, 126, 234); }  /* Morado */
```

### 4. RGBA (con transparencia)

Como RGB pero con un cuarto valor (alpha) de 0 (transparente) a 1 (opaco).

```css
div {
    background-color: rgba(102, 126, 234, 0.5);  /* Morado semi-transparente */
}
```

### 5. HSL y HSLA

Formato: `hsl(matiz, saturación%, luminosidad%)`

```css
h1 { color: hsl(0, 100%, 50%); }        /* Rojo */
p { color: hsl(240, 100%, 50%); }       /* Azul */
div { background-color: hsla(240, 100%, 50%, 0.3); }  /* Azul transparente */
```

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: CSS Inline

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS Inline</title>
</head>
<body>
    <h1 style="color: #667eea; text-align: center;">Título con CSS Inline</h1>
    <p style="color: #555; font-size: 18px; line-height: 1.6;">
        Este párrafo usa CSS inline. No es la mejor práctica, pero funciona.
    </p>
</body>
</html>
```

### Ejemplo 2: CSS Interno

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS Interno</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        
        h1 {
            color: #667eea;
            text-align: center;
        }
        
        .destacado {
            background-color: #fffacd;
            padding: 10px;
            border-left: 4px solid #667eea;
        }
        
        #importante {
            color: red;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Título Principal</h1>
    <p class="destacado">Este párrafo está destacado con fondo amarillo.</p>
    <p id="importante">Este texto es importante y está en rojo.</p>
</body>
</html>
```

### Ejemplo 3: CSS Externo (Recomendado)

**Archivo: index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS Externo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Mi Sitio Web</h1>
        <nav>
            <a href="#inicio">Inicio</a>
            <a href="#sobre">Sobre</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>
    
    <main>
        <article class="tarjeta">
            <h2>Artículo 1</h2>
            <p>Contenido del artículo con estilos externos.</p>
        </article>
    </main>
    
    <footer id="pie-pagina">
        <p>&copy; 2025 Mi Sitio Web</p>
    </footer>
</body>
</html>
```

**Archivo: styles.css**
```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8f9fa;
    color: #333;
}

header {
    background-color: #667eea;
    color: white;
    padding: 20px;
    text-align: center;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 15px;
}

main {
    max-width: 800px;
    margin: 30px auto;
    padding: 20px;
}

.tarjeta {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

#pie-pagina {
    background-color: #2c3e50;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 40px;
}
```

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día

### Ejercicio 1: Primera hoja de estilos ⭐
Crea una página HTML simple con un título (`<h1>`), dos párrafos (`<p>`), y una lista desordenada con 3 elementos. Crea un archivo CSS externo llamado `style1.css` y aplica los siguientes estilos: color de fondo del body (#f0f0f0), color del título (#2c3e50), tamaño de fuente del título (2.5rem), color de los párrafos (#555), y tamaño de línea de los párrafos (1.6).

[Solución](ejercicio1.html)

### Ejercicio 2: Selectores y clases ⭐⭐
Crea una página HTML con una estructura de blog que incluya: un header con título del blog, un main con 2 artículos (cada artículo debe tener un h2 y 2 párrafos), y un footer. Crea un archivo CSS externo (`style2.css`) y utiliza: selector de elemento para estilizar el body, clases para estilizar los artículos (`.articulo`), clase para destacar el primer párrafo de cada artículo (`.intro`), y un ID para el footer (`#pie-pagina`). Aplica colores, márgenes y padding apropiados.

[Solución](ejercicio2.html)

### Ejercicio 3: Página completa con múltiples selectores ⭐⭐⭐
Crea una página web completa para un portafolio personal que incluya: header con nombre y navegación (4 enlaces), sección "Sobre mí" con foto (puedes usar placeholder) y descripción, sección "Habilidades" con lista de 5 habilidades, sección "Proyectos" con 3 tarjetas de proyecto (cada una con título, descripción y enlace), y footer con redes sociales. Crea un archivo CSS externo (`style3.css`) que utilice: reset universal (*), selectores de elemento, al menos 5 clases diferentes, al menos 2 IDs, selectores descendentes, y una paleta de colores consistente (elige 3 colores principales). La página debe verse profesional y moderna.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- **Usa CSS externo** siempre que sea posible para mejor mantenimiento y reutilización.
- **Nombra las clases de forma descriptiva**: `.boton-principal` es mejor que `.azul`.
- **Evita el uso excesivo de IDs** para estilos; prefiere clases para reutilización.
- **Organiza tu CSS** con comentarios y secciones lógicas.
- **Usa selectores específicos** pero no demasiado complejos.
- **Evita `!important`** a menos que sea absolutamente necesario.
- **Mantén la consistencia** en nombres y convenciones (kebab-case recomendado).
- **Agrupa selectores** cuando compartan estilos para reducir repetición.
- **Comenta tu código CSS** para explicar decisiones de diseño complejas.
- **Usa variables CSS** (custom properties) para colores y valores repetidos (lo veremos más adelante).
- **Valida tu CSS** con herramientas como el W3C CSS Validator.

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-25">Día 25</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-27">Día 27</a>
</h4>
