<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-13">Día 13</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-15">Día 15</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml14.png">
</h1>

# Día 14: HTML Semántico Parte 1 - header, nav, main, footer

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Índice
* [Objetivo](#objetivo)
* [¿Qué es HTML Semántico?](#semantico)
* [Beneficios del HTML Semántico](#beneficios)
* [Elemento header](#header)
* [Elemento nav](#nav)
* [Elemento main](#main)
* [Elemento footer](#footer)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)


## 📖 Descripción

El HTML semántico utiliza etiquetas que describen claramente el significado y propósito del contenido que contienen. A diferencia de los elementos genéricos como `<div>` y `<span>`, los elementos semánticos como `<header>`, `<nav>`, `<main>` y `<footer>` proporcionan información sobre la estructura y el tipo de contenido de una página web.

En este día aprenderás los elementos semánticos fundamentales que forman la estructura principal de cualquier página web moderna. Estos elementos no solo mejoran la legibilidad del código, sino que también benefician la accesibilidad, el SEO y el mantenimiento de tu sitio web.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Comprender qué es el HTML semántico y por qué es importante
- Utilizar correctamente los elementos `<header>`, `<nav>`, `<main>` y `<footer>`
- Estructurar páginas web de forma semántica y accesible
- Identificar cuándo y dónde usar cada elemento semántico
- Mejorar el SEO y la accesibilidad de tus páginas web
- Migrar estructuras basadas en `<div>` a HTML semántico

## 📚 Conceptos Clave

<a name="semantico"></a>

## ¿Qué es HTML Semántico?

HTML semántico se refiere al uso de etiquetas HTML que transmiten el **significado** del contenido que contienen, no solo su apariencia visual.

**Comparación:**

```html
<!-- HTML NO semántico -->
<div class="header">
  <div class="navigation">
    <a href="#">Inicio</a>
  </div>
</div>
<div class="content">
  <p>Contenido principal</p>
</div>
<div class="footer">
  <p>© 2025</p>
</div>
```

```html
<!-- HTML Semántico -->
<header>
  <nav>
    <a href="#">Inicio</a>
  </nav>
</header>
<main>
  <p>Contenido principal</p>
</main>
<footer>
  <p>© 2025</p>
</footer>
```

**Diferencias clave:**

- El HTML semántico describe **qué es** el contenido (un encabezado, navegación, contenido principal, pie de página)
- El HTML no semántico solo agrupa contenido sin describir su propósito
- Los elementos semánticos son más fáciles de leer y entender para desarrolladores
- Los navegadores, lectores de pantalla y motores de búsqueda entienden mejor el HTML semántico

<a name="beneficios"></a>

## Beneficios del HTML Semántico

### 1. **Accesibilidad mejorada**

Los lectores de pantalla y tecnologías asistivas pueden navegar mejor por el contenido cuando está estructurado semánticamente.

```html
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#servicios">Servicios</a></li>
  </ul>
</nav>
```

Un lector de pantalla puede anunciar "navegación" y permitir al usuario saltar directamente a esta sección.

### 2. **SEO optimizado**

Los motores de búsqueda como Google entienden mejor la estructura y jerarquía del contenido.

```html
<main>
  <article>
    <h1>Título principal del artículo</h1>
    <p>Contenido relevante...</p>
  </article>
</main>
```

Google sabe que el contenido dentro de `<main>` es el contenido principal de la página.

### 3. **Código más legible y mantenible**

Es más fácil entender la estructura de una página con elementos semánticos.

```html
<!-- Fácil de entender -->
<header>
  <nav>...</nav>
</header>

<!-- Menos claro -->
<div class="top-section">
  <div class="menu-container">...</div>
</div>
```

### 4. **Consistencia en el equipo**

Los elementos semánticos proporcionan un vocabulario común para todos los desarrolladores.

### 5. **Mejor compatibilidad futura**

Los navegadores y herramientas futuras podrán aprovechar mejor el HTML semántico.

<a name="header"></a>

## Elemento `<header>`

El elemento `<header>` representa un contenedor para contenido introductorio o de navegación. Típicamente contiene:

- Logotipos
- Títulos principales
- Navegación principal
- Formularios de búsqueda
- Información del autor

### Características de `<header>`

- Es un elemento de bloque
- Puede aparecer múltiples veces en una página
- Puede estar dentro de `<article>`, `<section>`, o directamente en `<body>`
- No puede contener otro `<header>` o `<footer>` dentro de sí mismo

### Sintaxis básica

```html
<header>
  <h1>Título del sitio</h1>
  <p>Descripción o eslogan</p>
</header>
```

### Usos comunes

**1. Header principal de la página:**

```html
<header>
  <img src="logo.png" alt="Logo de la empresa">
  <h1>Mi Sitio Web</h1>
  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#servicios">Servicios</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>
```

**2. Header de un artículo:**

```html
<article>
  <header>
    <h2>Título del artículo</h2>
    <p>Por Juan Pérez - 13 de diciembre, 2025</p>
  </header>
  <p>Contenido del artículo...</p>
</article>
```

**3. Header de una sección:**

```html
<section>
  <header>
    <h2>Nuestros servicios</h2>
    <p>Ofrecemos soluciones integrales</p>
  </header>
  <p>Descripción de servicios...</p>
</section>
```

### Buenas prácticas con `<header>`

✅ **Hacer:**
- Usar para contenido introductorio
- Incluir navegación principal en el header de la página
- Usar múltiples headers cuando sea apropiado (uno por página, artículo o sección)

❌ **Evitar:**
- Usar header solo para agrupar elementos sin propósito introductorio
- Anidar headers dentro de otros headers
- Confundir con `<head>` (que es para metadatos del documento)

<a name="nav"></a>

## Elemento `<nav>`

El elemento `<nav>` representa una sección de navegación que contiene enlaces a otras páginas o secciones dentro de la página actual.

### Características de `<nav>`

- Es un elemento de bloque
- Debe contener enlaces de navegación principales
- Puede haber múltiples elementos `<nav>` en una página
- Mejora la accesibilidad al identificar áreas de navegación

### Sintaxis básica

```html
<nav>
  <a href="#inicio">Inicio</a>
  <a href="#servicios">Servicios</a>
  <a href="#contacto">Contacto</a>
</nav>
```

### Usos comunes

**1. Navegación principal:**

```html
<nav>
  <ul>
    <li><a href="index.html">Inicio</a></li>
    <li><a href="productos.html">Productos</a></li>
    <li><a href="sobre-nosotros.html">Sobre Nosotros</a></li>
    <li><a href="contacto.html">Contacto</a></li>
  </ul>
</nav>
```

**2. Navegación secundaria (breadcrumbs):**

```html
<nav aria-label="Breadcrumb">
  <ol>
    <li><a href="/">Inicio</a></li>
    <li><a href="/productos">Productos</a></li>
    <li><a href="/productos/laptops">Laptops</a></li>
    <li aria-current="page">Laptop Pro X15</li>
  </ol>
</nav>
```

**3. Tabla de contenidos:**

```html
<nav aria-label="Tabla de contenidos">
  <h2>Contenido</h2>
  <ul>
    <li><a href="#introduccion">Introducción</a></li>
    <li><a href="#desarrollo">Desarrollo</a></li>
    <li><a href="#conclusion">Conclusión</a></li>
  </ul>
</nav>
```

**4. Navegación en el footer:**

```html
<footer>
  <nav aria-label="Enlaces del pie de página">
    <a href="/privacidad">Privacidad</a>
    <a href="/terminos">Términos</a>
    <a href="/ayuda">Ayuda</a>
  </nav>
</footer>
```

### Cuándo NO usar `<nav>`

No todos los grupos de enlaces necesitan estar en un `<nav>`. Usa `<nav>` solo para bloques de navegación **principales**.

❌ **No usar para:**
- Enlaces dentro de contenido regular
- Listas de enlaces en el footer que no son navegación principal
- Enlaces de redes sociales (a menos que sean navegación principal)

✅ **Usar para:**
- Menú principal del sitio
- Navegación de secciones importantes
- Breadcrumbs
- Tabla de contenidos de artículos largos

### Buenas prácticas con `<nav>`

✅ **Hacer:**
- Usar listas (`<ul>` o `<ol>`) dentro de `<nav>` para mejor estructura
- Añadir `aria-label` cuando hay múltiples `<nav>` para distinguirlos
- Usar para navegación principal y significativa

❌ **Evitar:**
- Usar para cualquier grupo de enlaces
- Incluir contenido que no sea de navegación
- Olvidar la accesibilidad en navegaciones complejas

<a name="main"></a>

## Elemento `<main>`

El elemento `<main>` representa el contenido principal y único de la página. Debe contener el contenido directamente relacionado con el tema central del documento.

### Características de `<main>`

- Es un elemento de bloque
- **Solo puede haber UNO por página**
- No debe estar dentro de `<article>`, `<aside>`, `<footer>`, `<header>`, o `<nav>`
- Debe contener contenido único (no repetido en otras páginas)
- Mejora significativamente la accesibilidad

### Sintaxis básica

```html
<main>
  <h1>Título principal del contenido</h1>
  <p>Contenido principal de la página...</p>
</main>
```

### Usos comunes

**1. Contenido principal de una página de blog:**

```html
<main>
  <article>
    <h1>Cómo aprender HTML en 30 días</h1>
    <p>Publicado el 13 de diciembre, 2025</p>
    <p>HTML es el lenguaje fundamental...</p>
  </article>
</main>
```

**2. Contenido principal de una página de productos:**

```html
<main>
  <h1>Nuestros Productos</h1>
  <section>
    <h2>Laptops</h2>
    <div class="producto">...</div>
    <div class="producto">...</div>
  </section>
  <section>
    <h2>Tablets</h2>
    <div class="producto">...</div>
  </section>
</main>
```

**3. Contenido principal con sidebar:**

```html
<main>
  <article>
    <h1>Artículo principal</h1>
    <p>Contenido del artículo...</p>
  </article>
  
  <aside>
    <h2>Artículos relacionados</h2>
    <ul>
      <li><a href="#">Artículo 1</a></li>
      <li><a href="#">Artículo 2</a></li>
    </ul>
  </aside>
</main>
```

### Qué incluir en `<main>`

✅ **Incluir:**
- Contenido único de la página
- Artículos principales
- Formularios principales
- Resultados de búsqueda
- Contenido central del documento

❌ **No incluir:**
- Navegación del sitio (usar `<nav>`)
- Información repetida en múltiples páginas
- Barras laterales con contenido secundario (a menos que sea el contenido principal)
- Encabezados del sitio (usar `<header>`)
- Pies de página del sitio (usar `<footer>`)

### Buenas prácticas con `<main>`

✅ **Hacer:**
- Usar solo una vez por página
- Colocar el contenido único y principal dentro
- Usar junto con elementos de encabezado apropiados (`<h1>`)

❌ **Evitar:**
- Usar múltiples elementos `<main>` en una página
- Incluir contenido repetitivo del sitio
- Anidar dentro de otros elementos semánticos estructurales

<a name="footer"></a>

## Elemento `<footer>`

El elemento `<footer>` representa el pie de página de su sección contenedora más cercana o del documento completo. Típicamente contiene información sobre el autor, copyright, enlaces relacionados, o información de contacto.

### Características de `<footer>`

- Es un elemento de bloque
- Puede aparecer múltiples veces en una página
- Puede estar dentro de `<article>`, `<section>`, o directamente en `<body>`
- No puede contener otro `<footer>` o `<header>` dentro de sí mismo

### Sintaxis básica

```html
<footer>
  <p>&copy; 2025 Mi Sitio Web. Todos los derechos reservados.</p>
</footer>
```

### Usos comunes

**1. Footer principal de la página:**

```html
<footer>
  <div class="footer-content">
    <div class="footer-section">
      <h3>Sobre nosotros</h3>
      <p>Somos una empresa dedicada...</p>
    </div>
    <div class="footer-section">
      <h3>Contacto</h3>
      <p>Email: info@ejemplo.com</p>
      <p>Teléfono: +34 123 456 789</p>
    </div>
    <div class="footer-section">
      <h3>Síguenos</h3>
      <a href="#">Facebook</a>
      <a href="#">Twitter</a>
      <a href="#">Instagram</a>
    </div>
  </div>
  <div class="footer-bottom">
    <p>&copy; 2025 Mi Empresa. Todos los derechos reservados.</p>
    <nav>
      <a href="/privacidad">Privacidad</a>
      <a href="/terminos">Términos</a>
    </nav>
  </div>
</footer>
```

**2. Footer de un artículo:**

```html
<article>
  <h2>Título del artículo</h2>
  <p>Contenido del artículo...</p>
  
  <footer>
    <p>Escrito por: María García</p>
    <p>Publicado: 13 de diciembre, 2025</p>
    <p>Categorías: <a href="#">HTML</a>, <a href="#">Web Development</a></p>
  </footer>
</article>
```

**3. Footer de una sección:**

```html
<section>
  <h2>Comentarios</h2>
  <p>Gracias por leer este artículo...</p>
  
  <footer>
    <p>Última actualización: 13/12/2025</p>
  </footer>
</section>
```

### Contenido típico del footer

✅ **Incluir:**
- Información de copyright
- Enlaces a políticas (privacidad, términos)
- Información de contacto
- Enlaces a redes sociales
- Información del autor
- Navegación secundaria
- Logotipos secundarios

❌ **No incluir:**
- Contenido principal de la página
- Navegación principal (debería estar en `<nav>` dentro de `<header>`)

### Buenas prácticas con `<footer>`

✅ **Hacer:**
- Usar para información complementaria o de cierre
- Incluir información de copyright y legal
- Puede contener elementos `<nav>` para enlaces del footer

❌ **Evitar:**
- Anidar footers dentro de otros footers
- Usar solo para estilizar (usar `<div>` si no tiene significado semántico)
- Incluir contenido principal

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Estructura básica de página completa

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Sitio Web</title>
</head>
<body>
  <header>
    <h1>Mi Sitio Web</h1>
    <nav>
      <ul>
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <h2>Bienvenido</h2>
    <p>Este es el contenido principal de mi página web.</p>
  </main>

  <footer>
    <p>&copy; 2025 Mi Sitio Web. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
```

### Ejemplo 2: Blog con múltiples headers y footers

```html
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
        <h2>Introducción a HTML Semántico</h2>
        <p>Por Juan Pérez - 13 de diciembre, 2025</p>
      </header>
      
      <p>El HTML semántico es fundamental para...</p>
      <p>En este artículo aprenderás...</p>
      
      <footer>
        <p>Etiquetas: <a href="#">HTML</a>, <a href="#">Semántica</a></p>
        <p>Compartir: <a href="#">Twitter</a> | <a href="#">Facebook</a></p>
      </footer>
    </article>

    <article>
      <header>
        <h2>CSS Grid vs Flexbox</h2>
        <p>Por María García - 10 de diciembre, 2025</p>
      </header>
      
      <p>Ambas tecnologías son poderosas...</p>
      
      <footer>
        <p>Etiquetas: <a href="#">CSS</a>, <a href="#">Layout</a></p>
      </footer>
    </article>
  </main>

  <footer>
    <p>&copy; 2025 Mi Blog. Todos los derechos reservados.</p>
    <nav>
      <a href="/privacidad">Privacidad</a>
      <a href="/terminos">Términos</a>
    </nav>
  </footer>
</body>
```

### Ejemplo 3: Página de empresa completa

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>TechSolutions - Soluciones Tecnológicas</title>
</head>
<body>
  <header>
    <img src="logo.png" alt="Logo TechSolutions">
    <h1>TechSolutions</h1>
    <p>Innovación y tecnología a tu alcance</p>
    
    <nav aria-label="Navegación principal">
      <ul>
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#proyectos">Proyectos</a></li>
        <li><a href="#equipo">Equipo</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="inicio">
      <h2>Bienvenido a TechSolutions</h2>
      <p>Somos líderes en desarrollo de software y consultoría tecnológica.</p>
    </section>

    <section id="servicios">
      <header>
        <h2>Nuestros Servicios</h2>
        <p>Ofrecemos soluciones integrales para tu negocio</p>
      </header>
      
      <article>
        <h3>Desarrollo Web</h3>
        <p>Creamos sitios web modernos y responsivos.</p>
      </article>
      
      <article>
        <h3>Aplicaciones Móviles</h3>
        <p>Apps nativas e híbridas para iOS y Android.</p>
      </article>
      
      <article>
        <h3>Consultoría IT</h3>
        <p>Asesoramiento tecnológico para tu empresa.</p>
      </article>
    </section>

    <section id="contacto">
      <h2>Contáctanos</h2>
      <p>Estamos aquí para ayudarte</p>
      <p>Email: contacto@techsolutions.com</p>
      <p>Teléfono: +34 900 123 456</p>
    </section>
  </main>

  <footer>
    <div class="footer-columns">
      <div>
        <h3>TechSolutions</h3>
        <p>Transformando ideas en realidad digital desde 2020</p>
      </div>
      
      <div>
        <h3>Enlaces rápidos</h3>
        <nav aria-label="Enlaces del footer">
          <ul>
            <li><a href="#servicios">Servicios</a></li>
            <li><a href="#proyectos">Proyectos</a></li>
            <li><a href="#blog">Blog</a></li>
          </ul>
        </nav>
      </div>
      
      <div>
        <h3>Legal</h3>
        <nav aria-label="Enlaces legales">
          <ul>
            <li><a href="/privacidad">Política de Privacidad</a></li>
            <li><a href="/terminos">Términos y Condiciones</a></li>
            <li><a href="/cookies">Política de Cookies</a></li>
          </ul>
        </nav>
      </div>
      
      <div>
        <h3>Síguenos</h3>
        <a href="https://facebook.com">Facebook</a>
        <a href="https://twitter.com">Twitter</a>
        <a href="https://linkedin.com">LinkedIn</a>
      </div>
    </div>
    
    <div class="footer-bottom">
      <p>&copy; 2025 TechSolutions. Todos los derechos reservados.</p>
    </div>
  </footer>
</body>
</html>
```

### Ejemplo 4: Migración de divs a HTML semántico

**Antes (sin semántica):**

```html
<div class="page-header">
  <div class="logo">Mi Sitio</div>
  <div class="menu">
    <a href="#inicio">Inicio</a>
    <a href="#sobre">Sobre</a>
  </div>
</div>

<div class="main-content">
  <div class="article">
    <div class="article-title">Título</div>
    <div class="article-content">Contenido...</div>
  </div>
</div>

<div class="page-footer">
  <div class="copyright">© 2025</div>
</div>
```

**Después (con semántica):**

```html
<header>
  <h1>Mi Sitio</h1>
  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#sobre">Sobre</a>
  </nav>
</header>

<main>
  <article>
    <h2>Título</h2>
    <p>Contenido...</p>
  </article>
</main>

<footer>
  <p>&copy; 2025</p>
</footer>
```

### Ejemplo 5: Página con navegación breadcrumb

```html
<body>
  <header>
    <h1>Tienda Online</h1>
    <nav aria-label="Navegación principal">
      <ul>
        <li><a href="/">Inicio</a></li>
        <li><a href="/productos">Productos</a></li>
        <li><a href="/ofertas">Ofertas</a></li>
        <li><a href="/contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <nav aria-label="Breadcrumb">
    <ol>
      <li><a href="/">Inicio</a></li>
      <li><a href="/productos">Productos</a></li>
      <li><a href="/productos/electronica">Electrónica</a></li>
      <li aria-current="page">Laptop Pro X15</li>
    </ol>
  </nav>

  <main>
    <article>
      <header>
        <h1>Laptop Pro X15</h1>
        <p>Modelo: LPX15-2025</p>
      </header>
      
      <section>
        <h2>Descripción</h2>
        <p>Laptop de alto rendimiento para profesionales...</p>
      </section>
      
      <section>
        <h2>Especificaciones</h2>
        <ul>
          <li>Procesador: Intel Core i7</li>
          <li>RAM: 16GB</li>
          <li>Almacenamiento: 512GB SSD</li>
        </ul>
      </section>
      
      <footer>
        <p>SKU: LPX15-001</p>
        <p>Categoría: Electrónica > Computadoras > Laptops</p>
      </footer>
    </article>
  </main>

  <footer>
    <nav aria-label="Enlaces del footer">
      <h2>Información</h2>
      <ul>
        <li><a href="/envios">Envíos</a></li>
        <li><a href="/devoluciones">Devoluciones</a></li>
        <li><a href="/garantia">Garantía</a></li>
      </ul>
    </nav>
    
    <p>&copy; 2025 Tienda Online. Todos los derechos reservados.</p>
  </footer>
</body>
```

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día


### Ejercicio 1: Estructura básica de página personal ⭐
Crea una página HTML personal con la siguiente estructura semántica: un `<header>` que contenga tu nombre en un `<h1>` y una navegación (`<nav>`) con enlaces a "Inicio", "Sobre mí" y "Contacto"; un `<main>` con un párrafo de bienvenida y una breve descripción tuya; y un `<footer>` con información de copyright y el año actual.

[Solución](ejercicio1.html)

### Ejercicio 2: Blog con múltiples artículos ⭐⭐
Crea una página de blog que incluya: un `<header>` principal con el título del blog y navegación; un `<main>` que contenga 2 artículos (`<article>`), donde cada artículo tenga su propio `<header>` con título y fecha de publicación, contenido con al menos 2 párrafos, y un `<footer>` con etiquetas/categorías; y un `<footer>` principal de la página con enlaces a redes sociales y copyright.

[Solución](ejercicio2.html)

### Ejercicio 3: Sitio web empresarial completo ⭐⭐⭐
Crea una página web completa para una empresa ficticia con la siguiente estructura: `<header>` con logo (puede ser texto), nombre de la empresa, eslogan, y navegación principal con al menos 4 enlaces; `<nav>` secundario con breadcrumbs (Inicio > Servicios > Desarrollo Web); `<main>` que contenga 3 secciones (`<section>`): una de bienvenida, una de servicios con 3 artículos de servicio (cada uno con su `<header>` y descripción), y una de contacto con información de email y teléfono; y un `<footer>` completo con 3 columnas: información de la empresa, navegación de enlaces útiles (usando `<nav>` con `aria-label`), y enlaces legales (privacidad, términos), más una línea final con copyright. Asegúrate de usar `aria-label` en todas las navegaciones para distinguirlas.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa elementos semánticos siempre que sea posible en lugar de `<div>` genéricos.
- El elemento `<main>` debe usarse solo una vez por página.
- Puedes tener múltiples `<header>`, `<nav>` y `<footer>` en una página (uno por sección).
- Usa `aria-label` cuando tengas múltiples elementos `<nav>` para distinguirlos.
- El `<header>` no es lo mismo que `<head>` (metadatos del documento).
- No todos los grupos de enlaces necesitan estar en `<nav>`; úsalo solo para navegación principal.
- El contenido dentro de `<main>` debe ser único para esa página.
- Los elementos semánticos mejoran el SEO, accesibilidad y mantenibilidad del código.
- Combina elementos semánticos con clases CSS para estilizado específico.
- Usa herramientas de validación HTML para verificar que tu estructura semántica sea correcta.
- Piensa en la estructura semántica antes de escribir el código HTML.
- Los lectores de pantalla se benefician enormemente del HTML semántico correcto.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-13">Día 13</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-15">Día 15</a>
</h4>
