<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-14">Día 14</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-16">Día 16</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml15.png">
</h1>

# Día 15: HTML Semántico Parte 2 - article, section, aside

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)

## Índice
* [Objetivo](#objetivo)
* [Elemento article](#article)
* [Elemento section](#section)
* [Elemento aside](#aside)
* [Combinando elementos semánticos](#combinando)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

En el día anterior aprendimos sobre los elementos estructurales principales: `<header>`, `<nav>`, `<main>` y `<footer>`. Hoy profundizaremos en otros tres elementos semánticos fundamentales que nos ayudan a organizar el contenido de forma más específica: `<article>`, `<section>` y `<aside>`.

Estos elementos son esenciales para crear páginas web bien estructuradas, accesibles y optimizadas para SEO. Aprenderás cuándo usar cada uno, cómo combinarlos correctamente y las mejores prácticas para su implementación.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Comprender la diferencia entre `<article>`, `<section>` y `<aside>`
- Utilizar correctamente cada elemento según el contexto
- Combinar elementos semánticos para crear estructuras complejas
- Identificar cuándo usar cada elemento semántico
- Crear layouts de blog, noticias y páginas de contenido
- Mejorar la accesibilidad y SEO de tus páginas web

## 📚 Conceptos Clave

<a name="article"></a>

## Elemento `<article>`

El elemento `<article>` representa una composición **independiente y autocontenida** en un documento. Debe tener sentido por sí mismo y ser distribuible o reutilizable de forma independiente.

### Características de `<article>`

- Es un elemento de bloque
- Representa contenido independiente y autocontenido
- Debe poder ser extraído y reutilizado sin perder contexto
- Puede contener sus propios `<header>`, `<footer>`, `<section>`, etc.
- Puede haber múltiples `<article>` en una página

### ¿Cuándo usar `<article>`?

Usa `<article>` cuando el contenido:
- Tiene sentido por sí solo
- Podría ser sindicado (RSS, redes sociales)
- Podría ser reutilizado en otro contexto
- Es independiente del resto del contenido

### Ejemplos de uso apropiado

✅ **Usar para:**
- Artículos de blog
- Noticias
- Comentarios de usuarios
- Publicaciones en foros
- Tarjetas de productos
- Widgets independientes

❌ **No usar para:**
- Secciones que dependen del contexto de la página
- Contenido que no tiene sentido por sí solo
- Agrupaciones genéricas de contenido

### Sintaxis básica

```html
<article>
  <h2>Título del artículo</h2>
  <p>Contenido del artículo...</p>
</article>
```

### Ejemplos prácticos

**1. Artículo de blog:**

```html
<article>
  <header>
    <h2>Cómo aprender HTML en 30 días</h2>
    <p>Por Juan Pérez - <time datetime="2025-01-08">8 de enero, 2025</time></p>
  </header>
  
  <p>HTML es el lenguaje fundamental de la web. En este artículo te mostraré cómo dominarlo en solo 30 días...</p>
  
  <section>
    <h3>Semana 1: Fundamentos</h3>
    <p>Durante la primera semana aprenderás...</p>
  </section>
  
  <section>
    <h3>Semana 2: Elementos avanzados</h3>
    <p>En la segunda semana profundizaremos en...</p>
  </section>
  
  <footer>
    <p>Categorías: <a href="#">HTML</a>, <a href="#">Desarrollo Web</a></p>
    <p>Compartir: <a href="#">Twitter</a> | <a href="#">Facebook</a></p>
  </footer>
</article>
```

**2. Tarjeta de producto:**

```html
<article class="producto">
  <img src="laptop.jpg" alt="Laptop Pro X15">
  <h3>Laptop Pro X15</h3>
  <p>Potente laptop para profesionales con procesador de última generación.</p>
  <p class="precio">€1,299.99</p>
  <button>Añadir al carrito</button>
</article>
```

**3. Comentario de usuario:**

```html
<article class="comentario">
  <header>
    <img src="avatar.jpg" alt="Avatar de María">
    <h4>María García</h4>
    <time datetime="2025-01-08T14:30">Hace 2 horas</time>
  </header>
  <p>Excelente artículo, muy útil para principiantes. ¡Gracias por compartir!</p>
  <footer>
    <button>Me gusta (15)</button>
    <button>Responder</button>
  </footer>
</article>
```

**4. Múltiples artículos en una página:**

```html
<main>
  <h1>Últimas noticias</h1>
  
  <article>
    <h2>Nueva versión de HTML lanzada</h2>
    <p>La W3C ha anunciado...</p>
  </article>
  
  <article>
    <h2>CSS4 en desarrollo</h2>
    <p>El futuro de CSS incluye...</p>
  </article>
  
  <article>
    <h2>JavaScript alcanza nueva popularidad</h2>
    <p>Según las últimas estadísticas...</p>
  </article>
</main>
```

### Anidación de `<article>`

Los artículos pueden contener otros artículos cuando tienen una relación jerárquica:

```html
<article>
  <h2>Artículo principal sobre HTML</h2>
  <p>Contenido del artículo...</p>
  
  <section>
    <h3>Comentarios</h3>
    
    <article>
      <h4>Comentario de Juan</h4>
      <p>Gran artículo...</p>
    </article>
    
    <article>
      <h4>Comentario de María</h4>
      <p>Muy útil...</p>
    </article>
  </section>
</article>
```

<a name="section"></a>

## Elemento `<section>`

El elemento `<section>` representa una sección genérica de un documento o aplicación. Es una agrupación temática de contenido, típicamente con un encabezado.

### Características de `<section>`

- Es un elemento de bloque
- Agrupa contenido relacionado temáticamente
- Generalmente debe tener un encabezado (`<h1>`-`<h6>`)
- Representa una sección del documento
- Puede contener múltiples elementos, incluidos otros `<section>`

### ¿Cuándo usar `<section>`?

Usa `<section>` cuando:
- Agrupes contenido relacionado temáticamente
- El contenido tenga un encabezado natural
- Quieras crear divisiones lógicas en tu documento
- El contenido forme parte de un esquema del documento

### Ejemplos de uso apropiado

✅ **Usar para:**
- Capítulos de un documento
- Pestañas de contenido
- Secciones numeradas
- Agrupaciones temáticas con encabezado

❌ **No usar para:**
- Contenido independiente (usar `<article>`)
- Agrupaciones puramente estilísticas (usar `<div>`)
- Contenido sin encabezado natural

### Sintaxis básica

```html
<section>
  <h2>Título de la sección</h2>
  <p>Contenido de la sección...</p>
</section>
```

### Ejemplos prácticos

**1. Secciones de una página de inicio:**

```html
<main>
  <section id="hero">
    <h1>Bienvenido a nuestro sitio</h1>
    <p>Ofrecemos las mejores soluciones tecnológicas</p>
  </section>
  
  <section id="servicios">
    <h2>Nuestros Servicios</h2>
    <article>
      <h3>Desarrollo Web</h3>
      <p>Creamos sitios web modernos...</p>
    </article>
    <article>
      <h3>Diseño UX/UI</h3>
      <p>Diseñamos experiencias increíbles...</p>
    </article>
  </section>
  
  <section id="testimonios">
    <h2>Lo que dicen nuestros clientes</h2>
    <blockquote>
      <p>"Excelente servicio"</p>
      <footer>- Cliente satisfecho</footer>
    </blockquote>
  </section>
</main>
```

**2. Secciones dentro de un artículo:**

```html
<article>
  <h1>Guía completa de HTML</h1>
  
  <section>
    <h2>Introducción</h2>
    <p>HTML es el lenguaje de marcado...</p>
  </section>
  
  <section>
    <h2>Elementos básicos</h2>
    <p>Los elementos básicos incluyen...</p>
  </section>
  
  <section>
    <h2>Elementos avanzados</h2>
    <p>Una vez dominados los básicos...</p>
  </section>
  
  <section>
    <h2>Conclusión</h2>
    <p>HTML es fundamental para...</p>
  </section>
</article>
```

**3. Secciones con subsecciones:**

```html
<section>
  <h2>Capítulo 1: Fundamentos de HTML</h2>
  
  <section>
    <h3>1.1 ¿Qué es HTML?</h3>
    <p>HTML significa...</p>
  </section>
  
  <section>
    <h3>1.2 Historia de HTML</h3>
    <p>HTML fue creado en...</p>
  </section>
  
  <section>
    <h3>1.3 Versiones de HTML</h3>
    <p>A lo largo de los años...</p>
  </section>
</section>
```

### `<section>` vs `<div>`

**Usa `<section>` cuando:**
- El contenido tiene un significado semántico
- Hay un encabezado natural
- Forma parte del esquema del documento

**Usa `<div>` cuando:**
- Solo necesitas agrupar para estilos
- No hay significado semántico
- Es un contenedor puramente presentacional

```html
<!-- Correcto: section con significado semántico -->
<section>
  <h2>Servicios</h2>
  <p>Ofrecemos...</p>
</section>

<!-- Correcto: div para estilos -->
<div class="container">
  <div class="row">
    <div class="col">Contenido</div>
  </div>
</div>
```

<a name="aside"></a>

## Elemento `<aside>`

El elemento `<aside>` representa contenido que está **tangencialmente relacionado** con el contenido que lo rodea. Es contenido complementario o secundario.

### Características de `<aside>`

- Es un elemento de bloque
- Representa contenido relacionado pero no esencial
- Puede ser removido sin afectar el contenido principal
- Frecuentemente usado para barras laterales
- Puede aparecer múltiples veces en una página

### ¿Cuándo usar `<aside>`?

Usa `<aside>` para:
- Barras laterales (sidebars)
- Contenido relacionado
- Información complementaria
- Publicidad
- Citas destacadas (pull quotes)
- Glosarios
- Información adicional

### Ejemplos de uso apropiado

✅ **Usar para:**
- Barras laterales con contenido relacionado
- Widgets de "artículos relacionados"
- Información biográfica del autor
- Publicidad contextual
- Definiciones o glosarios

❌ **No usar para:**
- Contenido principal
- Navegación principal (usar `<nav>`)
- Contenido esencial para entender la página

### Sintaxis básica

```html
<aside>
  <h3>Contenido relacionado</h3>
  <p>Información complementaria...</p>
</aside>
```

### Ejemplos prácticos

**1. Barra lateral con artículos relacionados:**

```html
<main>
  <article>
    <h1>Artículo principal sobre HTML</h1>
    <p>Contenido del artículo...</p>
  </article>
  
  <aside>
    <h2>Artículos relacionados</h2>
    <ul>
      <li><a href="#">Introducción a CSS</a></li>
      <li><a href="#">JavaScript para principiantes</a></li>
      <li><a href="#">Diseño web responsive</a></li>
    </ul>
  </aside>
</main>
```

**2. Información del autor dentro de un artículo:**

```html
<article>
  <h1>Guía de HTML Semántico</h1>
  <p>El HTML semántico es fundamental...</p>
  
  <aside>
    <h3>Sobre el autor</h3>
    <img src="autor.jpg" alt="Foto del autor">
    <p><strong>Juan Pérez</strong> es desarrollador web con 10 años de experiencia.</p>
  </aside>
  
  <p>Continuando con el artículo...</p>
</article>
```

**3. Cita destacada (pull quote):**

```html
<article>
  <h1>El futuro del desarrollo web</h1>
  <p>El desarrollo web está evolucionando rápidamente...</p>
  
  <aside class="pull-quote">
    <blockquote>
      "El HTML semántico es la base de una web accesible"
    </blockquote>
  </aside>
  
  <p>Como mencionamos anteriormente...</p>
</article>
```

**4. Barra lateral con múltiples widgets:**

```html
<aside class="sidebar">
  <section>
    <h3>Categorías</h3>
    <ul>
      <li><a href="#">HTML</a> (25)</li>
      <li><a href="#">CSS</a> (18)</li>
      <li><a href="#">JavaScript</a> (32)</li>
    </ul>
  </section>
  
  <section>
    <h3>Artículos populares</h3>
    <article>
      <h4><a href="#">Cómo aprender HTML</a></h4>
      <p>Publicado hace 2 días</p>
    </article>
  </section>
  
  <section>
    <h3>Newsletter</h3>
    <form>
      <input type="email" placeholder="Tu email">
      <button>Suscribirse</button>
    </form>
  </section>
</aside>
```

**5. Aside dentro de un article:**

```html
<article>
  <h1>Historia de HTML</h1>
  <p>HTML fue creado por Tim Berners-Lee en 1991...</p>
  
  <aside>
    <h3>Dato curioso</h3>
    <p>La primera página web todavía está disponible en línea en el CERN.</p>
  </aside>
  
  <p>A lo largo de los años, HTML ha evolucionado...</p>
</article>
```

<a name="combinando"></a>

## Combinando elementos semánticos

La verdadera potencia del HTML semántico viene de combinar correctamente estos elementos.

### Estructura típica de un blog

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi Blog</title>
</head>
<body>
  <header>
    <h1>Mi Blog de Tecnología</h1>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#articulos">Artículos</a>
      <a href="#sobre-mi">Sobre mí</a>
    </nav>
  </header>
  
  <main>
    <article>
      <header>
        <h2>Título del artículo principal</h2>
        <p>Por Juan Pérez - <time>8 de enero, 2025</time></p>
      </header>
      
      <section>
        <h3>Introducción</h3>
        <p>Contenido de la introducción...</p>
      </section>
      
      <section>
        <h3>Desarrollo</h3>
        <p>Contenido del desarrollo...</p>
        
        <aside>
          <h4>Nota importante</h4>
          <p>Información complementaria...</p>
        </aside>
      </section>
      
      <section>
        <h3>Conclusión</h3>
        <p>Contenido de la conclusión...</p>
      </section>
      
      <footer>
        <p>Etiquetas: HTML, Semántica, Web</p>
      </footer>
    </article>
    
    <aside>
      <h2>Artículos relacionados</h2>
      <article>
        <h3><a href="#">Artículo relacionado 1</a></h3>
        <p>Resumen breve...</p>
      </article>
      <article>
        <h3><a href="#">Artículo relacionado 2</a></h3>
        <p>Resumen breve...</p>
      </article>
    </aside>
  </main>
  
  <footer>
    <p>&copy; 2025 Mi Blog. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
```

### Decisión: ¿article o section?

**Pregunta clave:** ¿El contenido tiene sentido por sí solo?

- **SÍ** → Usa `<article>`
- **NO** → Usa `<section>`

```html
<!-- Article: tiene sentido por sí solo -->
<article>
  <h2>Receta de paella valenciana</h2>
  <p>Ingredientes: arroz, pollo, azafrán...</p>
  <p>Preparación: primero...</p>
</article>

<!-- Section: es parte de un todo mayor -->
<article>
  <h1>Libro de cocina española</h1>
  
  <section>
    <h2>Entrantes</h2>
    <p>Los entrantes tradicionales...</p>
  </section>
  
  <section>
    <h2>Platos principales</h2>
    <p>Los platos principales incluyen...</p>
  </section>
</article>
```

### Decisión: ¿aside o section?

**Pregunta clave:** ¿El contenido es complementario o esencial?

- **Complementario** → Usa `<aside>`
- **Esencial** → Usa `<section>`

```html
<!-- Section: contenido esencial -->
<article>
  <h1>Tutorial de HTML</h1>
  
  <section>
    <h2>Paso 1: Estructura básica</h2>
    <p>Primero crea la estructura...</p>
  </section>
  
  <section>
    <h2>Paso 2: Añadir contenido</h2>
    <p>Ahora añade el contenido...</p>
  </section>
</article>

<!-- Aside: contenido complementario -->
<article>
  <h1>Tutorial de HTML</h1>
  <p>En este tutorial aprenderás...</p>
  
  <aside>
    <h2>Recursos adicionales</h2>
    <ul>
      <li><a href="#">Documentación MDN</a></li>
      <li><a href="#">W3C Validator</a></li>
    </ul>
  </aside>
</article>
```

### Jerarquía y anidación

```html
<body>
  <header><!-- Header de la página --></header>
  
  <main>
    <article>
      <header><!-- Header del artículo --></header>
      
      <section>
        <h2>Sección 1</h2>
        <aside><!-- Aside relacionado con la sección --></aside>
      </section>
      
      <section>
        <h2>Sección 2</h2>
      </section>
      
      <footer><!-- Footer del artículo --></footer>
    </article>
    
    <aside><!-- Aside relacionado con el main --></aside>
  </main>
  
  <footer><!-- Footer de la página --></footer>
</body>
```

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Página de noticias

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Noticias Tech</title>
</head>
<body>
  <header>
    <h1>Noticias Tech</h1>
    <nav>
      <a href="#tecnologia">Tecnología</a>
      <a href="#ciencia">Ciencia</a>
      <a href="#innovacion">Innovación</a>
    </nav>
  </header>
  
  <main>
    <section id="destacadas">
      <h2>Noticias destacadas</h2>
      
      <article>
        <header>
          <h3>Nueva versión de HTML anunciada</h3>
          <p>Por María García - <time>8 de enero, 2025</time></p>
        </header>
        <p>La W3C ha anunciado oficialmente la nueva versión de HTML...</p>
        <a href="#">Leer más</a>
      </article>
      
      <article>
        <header>
          <h3>JavaScript alcanza nuevo récord de popularidad</h3>
          <p>Por Juan Pérez - <time>7 de enero, 2025</time></p>
        </header>
        <p>Según las últimas estadísticas, JavaScript continúa siendo...</p>
        <a href="#">Leer más</a>
      </article>
    </section>
    
    <aside>
      <h2>Más leídas</h2>
      <ol>
        <li><a href="#">Guía completa de CSS Grid</a></li>
        <li><a href="#">10 trucos de JavaScript</a></li>
        <li><a href="#">Cómo mejorar el SEO</a></li>
      </ol>
    </aside>
  </main>
  
  <footer>
    <p>&copy; 2025 Noticias Tech</p>
  </footer>
</body>
</html>
```

### Ejemplo 2: Portfolio personal

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Portfolio de Ana López</title>
</head>
<body>
  <header>
    <h1>Ana López</h1>
    <p>Desarrolladora Web Full Stack</p>
    <nav>
      <a href="#sobre-mi">Sobre mí</a>
      <a href="#proyectos">Proyectos</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>
  
  <main>
    <section id="sobre-mi">
      <h2>Sobre mí</h2>
      <p>Soy una desarrolladora apasionada por crear experiencias web increíbles...</p>
      
      <aside>
        <h3>Habilidades</h3>
        <ul>
          <li>HTML5 & CSS3</li>
          <li>JavaScript (ES6+)</li>
          <li>React & Vue.js</li>
          <li>Node.js</li>
        </ul>
      </aside>
    </section>
    
    <section id="proyectos">
      <h2>Mis Proyectos</h2>
      
      <article>
        <h3>E-commerce de moda</h3>
        <img src="proyecto1.jpg" alt="Captura del proyecto">
        <p>Tienda online completa con carrito de compras y pasarela de pago.</p>
        <p><strong>Tecnologías:</strong> React, Node.js, MongoDB</p>
        <a href="#">Ver proyecto</a>
      </article>
      
      <article>
        <h3>App de gestión de tareas</h3>
        <img src="proyecto2.jpg" alt="Captura del proyecto">
        <p>Aplicación web para gestionar tareas con drag & drop.</p>
        <p><strong>Tecnologías:</strong> Vue.js, Firebase</p>
        <a href="#">Ver proyecto</a>
      </article>
    </section>
  </main>
  
  <footer>
    <p>Contacto: ana@ejemplo.com</p>
    <p>&copy; 2025 Ana López</p>
  </footer>
</body>
</html>
```

<a name="ejercicio"></a>

## ✏️ Ejercicios

### Ejercicio 1: Blog personal básico
Crea una página de blog con:
- Un artículo principal con header, secciones y footer
- Una barra lateral con información del autor
- Navegación principal

### Ejercicio 2: Página de noticias
Crea una página de noticias con:
- Múltiples artículos de noticias
- Sección de noticias destacadas
- Barra lateral con noticias relacionadas y categorías

### Ejercicio 3: Portfolio completo
Crea un portfolio personal con:
- Sección "Sobre mí" con aside de habilidades
- Sección de proyectos con múltiples articles
- Sección de experiencia laboral
- Barra lateral con información de contacto

## 🎯 Resumen

- **`<article>`**: Contenido independiente y autocontenido (artículos, noticias, comentarios)
- **`<section>`**: Agrupación temática de contenido relacionado (capítulos, secciones)
- **`<aside>`**: Contenido tangencialmente relacionado (barras laterales, información complementaria)

### Reglas de oro

1. Si el contenido tiene sentido por sí solo → `<article>`
2. Si agrupa contenido relacionado temáticamente → `<section>`
3. Si es contenido complementario → `<aside>`
4. Si es solo para estilos → `<div>`

## 📚 Recursos adicionales

- [MDN - article](https://developer.mozilla.org/es/docs/Web/HTML/Element/article)
- [MDN - section](https://developer.mozilla.org/es/docs/Web/HTML/Element/section)
- [MDN - aside](https://developer.mozilla.org/es/docs/Web/HTML/Element/aside)
- [HTML5 Doctor - Flowchart](http://html5doctor.com/downloads/h5d-sectioning-flowchart.pdf)

---

**¡Continúa aprendiendo!** Mañana veremos elementos multimedia en HTML5.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-14">Día 14</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-16">Día 16</a>
</h4>