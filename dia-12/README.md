<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-11">Día 11</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-13">Día 13</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml12.png">
</h1>

# Día 12: Divs y Spans - Contenedores genéricos

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)


## Indice
- [Día 12: Divs y Spans - Contenedores genéricos](#día-12-divs-y-spans---contenedores-genéricos)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [Comprendiendo los tipos de elementos HTML](#comprendiendo-los-tipos-de-elementos-html)
  - [Elementos de bloque vs. elementos en línea](#elementos-de-bloque-vs-elementos-en-línea)
    - [Elementos de bloque (block-level)](#elementos-de-bloque-block-level)
    - [Elementos en línea (inline)](#elementos-en-línea-inline)
  - [Etiqueta `<div>`](#etiqueta-div)
    - [Características de `<div>`](#características-de-div)
    - [Usos principales de `<div>`](#usos-principales-de-div)
    - [Atributos comunes con `<div>`](#atributos-comunes-con-div)
  - [Etiqueta `<span>`](#etiqueta-span)
    - [Características de `<span>`](#características-de-span)
    - [Usos principales de `<span>`](#usos-principales-de-span)
    - [Atributos comunes con `<span>`](#atributos-comunes-con-span)
  - [Diferencias clave entre `<div>` y `<span>`](#diferencias-clave-entre-div-y-span)
    - [Regla práctica](#regla-práctica)
  - [💻 Ejemplos Prácticos](#-ejemplos-prácticos)
    - [Ejemplo 1: Div simple para agrupar contenido](#ejemplo-1-div-simple-para-agrupar-contenido)
    - [Ejemplo 2: Span para destacar texto](#ejemplo-2-span-para-destacar-texto)
    - [Ejemplo 3: Estructura de página con divs](#ejemplo-3-estructura-de-página-con-divs)
    - [Ejemplo 4: Combinando div y span](#ejemplo-4-combinando-div-y-span)
    - [Ejemplo 5: Divs anidados para layout complejo](#ejemplo-5-divs-anidados-para-layout-complejo)
    - [Ejemplo 6: Spans para formato de texto variado](#ejemplo-6-spans-para-formato-de-texto-variado)
    - [Ejemplo 7: Divs con clases para tarjetas](#ejemplo-7-divs-con-clases-para-tarjetas)
    - [Ejemplo 8: Span para etiquetas y badges](#ejemplo-8-span-para-etiquetas-y-badges)
  - [✏️ Ejercicios del Día](#️-ejercicios-del-día)
    - [Ejercicio 1: Estructura básica con divs ⭐](#ejercicio-1-estructura-básica-con-divs-)
    - [Ejercicio 2: Formato de texto con spans ⭐⭐](#ejercicio-2-formato-de-texto-con-spans-)
    - [Ejercicio 3: Tarjetas de productos completas ⭐⭐⭐](#ejercicio-3-tarjetas-de-productos-completas-)
  - [🔍 Buenas Prácticas](#-buenas-prácticas)


## 📖 Descripción

Los elementos `<div>` y `<span>` son los contenedores genéricos más utilizados en HTML. Aunque no tienen significado semántico por sí mismos, son fundamentales para organizar y estructurar el contenido de una página web. El elemento `<div>` se utiliza para agrupar bloques de contenido, mientras que `<span>` sirve para agrupar pequeñas porciones de texto o elementos en línea.

Dominar el uso de estos elementos es esencial para crear estructuras HTML flexibles que después puedan estilizarse con CSS y manipularse con JavaScript. Son la base sobre la cual se construyen layouts complejos y diseños web modernos.


## 🎯 Objetivos del Día

Al acabar este día podrás:

- Entender la diferencia entre elementos de bloque y elementos en línea
- Utilizar `<div>` para agrupar bloques de contenido
- Aplicar `<span>` para marcar porciones de texto en línea
- Combinar ambos elementos para estructurar páginas web
- Identificar cuándo usar `<div>` y cuándo usar `<span>`
- Preparar el terreno para aplicar estilos CSS

## 📚 Conceptos Clave

### Comprendiendo los tipos de elementos HTML

## Elementos de bloque vs. elementos en línea

Antes de profundizar en `<div>` y `<span>`, es crucial entender la diferencia entre elementos de bloque y elementos en línea.

### Elementos de bloque (block-level)

Los elementos de bloque tienen las siguientes características:

- Comienzan en una nueva línea
- Ocupan todo el ancho disponible (se extienden de izquierda a derecha)
- Pueden contener otros elementos de bloque y elementos en línea
- Ejemplos: `<div>`, `<p>`, `<h1>` a `<h6>`, `<ul>`, `<ol>`, `<section>`, `<article>`, `<header>`, `<footer>`, `<form>`

```html
<p>Este es un párrafo (elemento de bloque).</p>
<p>Este es otro párrafo que aparece en una nueva línea.</p>

```

### Elementos en línea (inline)

Los elementos en línea tienen estas características:

- No empiezan en una nueva línea
- Solo ocupan el ancho necesario para su contenido
- No pueden contener elementos de bloque (solo otros elementos en línea o texto)
- Ejemplos: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<input>`, `<label>`

```html
<p>Este es un texto con <span>una porción en línea</span> que continúa en la misma línea.</p>

```

## Etiqueta `<div>`

El elemento `<div>` (división) es el contenedor genérico de bloque más utilizado en HTML. Su nombre es la abreviatura de "division" (división).

```html
<div>
  <!-- Contenido del bloque -->
</div>
```

### Características de `<div>`

- Es un elemento de bloque
- No tiene significado semántico propio
- Se utiliza para agrupar otros elementos con fines de organización y estilizado
- Ocupa todo el ancho disponible por defecto
- Siempre empieza en una nueva línea

### Usos principales de `<div>`

**1. Agrupar contenido relacionado:**

```html
<div>
  <h2>Título de la sección</h2>
  <p>Contenido de la sección.</p>
  <img src="imagen.jpg" alt="Imagen">
</div>
```

**2. Crear estructura de layout:**

```html
<div class="header">
  <!-- Contenido del encabezado -->
</div>
<div class="main-content">
  <!-- Contenido principal -->
</div>
<div class="footer">
  <!-- Contenido del pie de página -->
</div>
```

**3. Aplicar estilos CSS a grupos de elementos:**

```html
<div class="caja-destacada">
  <h3>Oferta especial</h3>
  <p>Descuento del 50% en productos seleccionados.</p>
</div>
```

**4. Manipular grupos de elementos con JavaScript:**

```html
<div id="contenido-dinamico">
  <!-- Contenido que puede cambiar dinámicamente -->
</div>
```

### Atributos comunes con `<div>`

**class**: Para aplicar estilos CSS reutilizables:

```html
<div class="contenedor">Contenido</div>
```

**id**: Identificador único para el elemento:

```html
<div id="cabecera-principal">Contenido</div>
```

**style**: Para estilos en línea (no recomendado como práctica habitual):

```html
<div style="background-color: blue;">Contenido</div>
```


## Etiqueta `<span>`

El elemento `<span>` es el contenedor genérico para elementos en línea. Se utiliza para agrupar pequeñas porciones de texto o elementos dentro de una línea.

```html
<span>Texto en línea</span>

```

### Características de `<span>`

- Es un elemento en línea
- No tiene significado semántico propio
- No interrumpe el flujo del texto (no crea saltos de línea)
- Solo ocupa el ancho necesario para su contenido
- Se utiliza para aplicar estilos a porciones específicas de texto

### Usos principales de `<span>`

**1. Aplicar estilos a palabras o frases específicas:**

```html
<p>Este texto tiene una <span style="color: red;">palabra en rojo</span> dentro.</p>
```

**2. Marcar texto para identificación:**

```html
<p>El precio es <span class="precio">\$19.99</span> por unidad.</p>

```

**3. Destacar información importante:**

```html
<p>Atención: <span class="importante">la fecha límite es el 30 de noviembre</span>.</p>
```

**4. Agrupar elementos inline para manipulación con JavaScript:**

```html
<p>Tu puntuación: <span id="puntuacion">0</span> puntos</p>
```

### Atributos comunes con `<span>`

Los mismos que `<div>`: `class`, `id`, `style`, entre otros.

```html
<span class="etiqueta">Nuevo</span><span id="contador">100</span>
```

## Diferencias clave entre `<div>` y `<span>`

| Característica      | `<div>`                              | `<span>`                            |
| ------------------- | ------------------------------------ | ----------------------------------- |
| **Tipo**            | Elemento de bloque                   | Elemento en línea                   |
| **Salto de línea**  | Sí, empieza en nueva línea           | No, continúa en la misma línea      |
| **Ancho**           | Ocupa todo el ancho disponible       | Solo el ancho de su contenido       |
| **Uso principal**   | Agrupar bloques grandes de contenido | Marcar porciones pequeñas de texto  |
| **Puede contener**  | Elementos de bloque y en línea       | Solo elementos en línea y texto     |
| **Ejemplos de uso** | Secciones, contenedores de layout    | Palabras, frases dentro de párrafos |

### Regla práctica

- Usa `<div>` cuando necesites agrupar **grandes secciones** o **bloques completos** de contenido
- Usa `<span>` cuando necesites marcar o estilizar **palabras específicas** o **pequeñas porciones** dentro de una línea de texto

## 💻 Ejemplos Prácticos

### Ejemplo 1: Div simple para agrupar contenido

```html
<div>
  <h2>Artículo sobre HTML</h2>
  <p>HTML es el lenguaje de marcado estándar para crear páginas web.</p>
  <p>Con HTML puedes estructurar tu contenido de forma semántica.</p>
</div>
```

### Ejemplo 2: Span para destacar texto

```html
<p>El <span style="font-weight: bold;">elemento span</span> es muy útil para
aplicar estilos a <span style="color: blue;">palabras específicas</span> dentro
de un párrafo.</p>
```

### Ejemplo 3: Estructura de página con divs

```html
<div class="contenedor-principal">
  <div class="cabecera">
    <h1>Mi Sitio Web</h1>
    <p>Bienvenido a mi página</p>
  </div>
  
  <div class="contenido">
    <h2>Contenido principal</h2>
    <p>Este es el contenido de la página.</p>
  </div>
  
  <div class="pie-pagina">
    <p>© 2025 - Todos los derechos reservados</p>
  </div>
</div>
```

### Ejemplo 4: Combinando div y span

```html
<div class="tarjeta-producto">
  <h3>Producto: <span class="nombre-producto">Laptop Pro</span></h3>
  <p>Precio: <span class="precio">$999</span></p>
  <p>Estado: <span class="estado disponible">Disponible</span></p>
  <p>Descripción: Una laptop <span style="font-style: italic;">potente y moderna</span> 
  para profesionales.</p>
</div>
```

### Ejemplo 5: Divs anidados para layout complejo

```html
<div class="pagina">
  <div class="encabezado">
    <div class="logo">
      <img src="logo.png" alt="Logo">
    </div>
    <div class="menu">
      <a href="#">Inicio</a>
      <a href="#">Productos</a>
      <a href="#">Contacto</a>
    </div>
  </div>
  <div class="cuerpo">
    <div class="barra-lateral">
      <h3>Categorías</h3>
      <ul>
        <li>Electrónica</li>
        <li>Ropa</li>
        <li>Libros</li>
      </ul>
    </div>
    <div class="contenido-principal">
      <h2>Productos destacados</h2>
      <p>Aquí están nuestros mejores productos.</p>
    </div>
  </div>
  <div class="pie">
    <p>Contacto: info@ejemplo.com</p>
  </div>
</div>
```

### Ejemplo 6: Spans para formato de texto variado

```html
<p>
  Esta frase tiene <span style="color: red;">texto en rojo</span>, 
  <span style="background-color: yellow;">texto con fondo amarillo</span>, 
  y <span style="font-size: 20px;">texto más grande</span>.
</p>
```

### Ejemplo 7: Divs con clases para tarjetas

```html
<div class="contenedor-tarjetas">
  <div class="tarjeta">
    <h3>Tarjeta 1</h3>
    <p>Contenido de la primera tarjeta.</p>
  </div>
  <div class="tarjeta">
    <h3>Tarjeta 2</h3>
    <p>Contenido de la segunda tarjeta.</p>
  </div>
  <div class="tarjeta">
    <h3>Tarjeta 3</h3>
    <p>Contenido de la tercera tarjeta.</p>
  </div>
</div>
```

### Ejemplo 8: Span para etiquetas y badges

```html
<div class="articulo">
  <h2>Nuevo producto lanzado <span class="badge nuevo">NUEVO</span></h2>
  <p>
    Este producto está en <span class="etiqueta oferta">OFERTA</span> 
    por tiempo limitado. Solo quedan <span class="cantidad">5 unidades</span>.
  </p>
  <p>
    Categorías: 
    <span class="categoria">Tecnología</span>
    <span class="categoria">Gadgets</span>
    <span class="categoria">Novedades</span>
  </p>
</div>
```

## ✏️ Ejercicios del Día


### Ejercicio 1: Estructura básica con divs ⭐
Crea una página HTML con una estructura básica usando divs: un encabezado con un título, un área de contenido principal con dos párrafos, y un pie de página con información de copyright. Usa clases descriptivas para cada div.

[Solución](ejercicio1.html)

### Ejercicio 2: Formato de texto con spans ⭐⭐
Crea un párrafo de al menos 5 líneas sobre tu ciudad favorita. Usa span para aplicar diferentes estilos en línea (sin CSS externo) a: 3 palabras en negrita (font-weight: bold), 2 palabras en color rojo, 1 frase con fondo amarillo, y 2 palabras en cursiva (font-style: italic).

[Solución](ejercicio2.html)

### Ejercicio 3: Tarjetas de productos completas ⭐⭐⭐
Crea un contenedor principal con 3 tarjetas de productos usando divs anidados. Cada tarjeta debe incluir: un título del producto, una descripción de al menos 2 líneas, un precio (usando span con clase "precio"), un estado de disponibilidad (usando span con clase "estado"), y al menos 2 etiquetas/categorías (usando span con clase "categoria"). Organiza todo con una estructura clara de divs con clases apropiadas y usa spans para resaltar información específica dentro del texto.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa `<div>` solo cuando no exista un elemento semántico más apropiado (`<section>`, `<article>`, `<header>`, `<nav>`, etc.).
- Usa `<span>` solo cuando no haya un elemento en línea más específico (`<strong>`, `<em>`, `<mark>`, etc.).
- Siempre añade clases o IDs descriptivos a tus divs y spans para facilitar el mantenimiento del código.
- No abuses de divs anidados innecesariamente; mantén la estructura lo más simple posible.
- Evita usar estilos inline (atributo `style`); prefiere hojas de estilo CSS externas o internas.
- Los divs son ideales para crear layouts con CSS (Grid, Flexbox) que aprenderás más adelante.
- Usa spans para aplicar estilos a palabras o frases específicas dentro de párrafos.
- Recuerda que `<div>` y `<span>` no tienen significado semántico; son solo contenedores visuales.
- Documenta tu código con comentarios cuando uses múltiples divs anidados para estructuras complejas.
- Verifica que tu estructura de divs y spans sea lógica antes de comenzar a aplicar estilos CSS.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-11">Día 11</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-13">Día 13</a>
</h4>