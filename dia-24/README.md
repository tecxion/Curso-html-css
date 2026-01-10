<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-23">Día 23</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-25">Día 25</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml24.png">
</h1>

# Día 24: Rutas y Enlaces - Absolutas y Relativas

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

Comprender las rutas es fundamental para vincular archivos, imágenes y páginas. Aprenderás la diferencia entre rutas absolutas y relativas, y cuándo usar cada una.

## 🎯 Objetivos del Día

- Comprender rutas absolutas y relativas
- Navegar por la estructura de directorios
- Vincular archivos correctamente
- Usar rutas para imágenes, CSS y JavaScript

## Rutas Absolutas

Una ruta absoluta especifica la ubicación completa desde la raíz.

### URL Completa

```html
<a href="https://www.ejemplo.com/pagina.html">Enlace externo</a>
<img src="https://www.ejemplo.com/images/foto.jpg" alt="Foto">
```

### Ruta desde la raíz del servidor

```html
<a href="/contacto.html">Contacto</a>
<img src="/images/logo.png" alt="Logo">
<link rel="stylesheet" href="/css/styles.css">
```

**Ventajas:**
- Funcionan desde cualquier ubicación
- Claras y explícitas

**Desventajas:**
- No portables (dependen del dominio)
- Más largas

## Rutas Relativas

Una ruta relativa es relativa a la ubicación del archivo actual.

### Mismo Directorio

```html
<!-- Archivo actual: /paginas/index.html -->
<a href="sobre-nosotros.html">Sobre Nosotros</a>
<img src="banner.jpg" alt="Banner">
```

### Subdirectorio

```html
<!-- Archivo actual: /index.html -->
<a href="paginas/contacto.html">Contacto</a>
<img src="images/logo.png" alt="Logo">
<link rel="stylesheet" href="css/styles.css">
```

### Directorio Padre

```html
<!-- Archivo actual: /paginas/blog/post.html -->
<a href="../index.html">Inicio</a>
<a href="../../index.html">Raíz</a>
<img src="../images/foto.jpg" alt="Foto">
```

**Ventajas:**
- Portables (funcionan en cualquier servidor)
- Más cortas
- Fáciles de mantener

**Desventajas:**
- Pueden ser confusas con muchos niveles

## Estructura de Ejemplo

```
mi-sitio/
├── index.html
├── contacto.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── images/
│   ├── logo.png
│   └── banner.jpg
└── paginas/
    ├── sobre-nosotros.html
    └── blog/
        └── post.html
```

## Ejemplos desde Diferentes Ubicaciones

### Desde `/index.html`

```html
<!-- Mismo nivel -->
<a href="contacto.html">Contacto</a>

<!-- Subdirectorios -->
<link rel="stylesheet" href="css/styles.css">
<img src="images/logo.png" alt="Logo">
<a href="paginas/sobre-nosotros.html">Sobre Nosotros</a>
```

### Desde `/paginas/sobre-nosotros.html`

```html
<!-- Directorio padre -->
<a href="../index.html">Inicio</a>
<a href="../contacto.html">Contacto</a>

<!-- Otros subdirectorios -->
<img src="../images/logo.png" alt="Logo">
<link rel="stylesheet" href="../css/styles.css">

<!-- Mismo directorio -->
<a href="blog/post.html">Blog</a>
```

### Desde `/paginas/blog/post.html`

```html
<!-- Dos niveles arriba -->
<a href="../../index.html">Inicio</a>
<a href="../../contacto.html">Contacto</a>

<!-- Otros subdirectorios -->
<img src="../../images/logo.png" alt="Logo">
<link rel="stylesheet" href="../../css/styles.css">

<!-- Un nivel arriba -->
<a href="../sobre-nosotros.html">Sobre Nosotros</a>
```

## Enlaces Internos (Anclas)

```html
<!-- Enlace a sección en la misma página -->
<a href="#seccion1">Ir a Sección 1</a>

<section id="seccion1">
  <h2>Sección 1</h2>
</section>

<!-- Enlace a sección en otra página -->
<a href="contacto.html#formulario">Ir al formulario</a>
```

## Mejores Prácticas

### ✅ Hacer

- Usar rutas relativas para archivos del mismo proyecto
- Usar rutas absolutas para recursos externos
- Mantener estructura de carpetas organizada
- Usar nombres de archivo descriptivos y en minúsculas
- Evitar espacios en nombres de archivo (usar guiones)

### ❌ Evitar

- Mezclar rutas absolutas y relativas sin razón
- Rutas muy largas con muchos `../`
- Espacios en nombres de archivo
- Caracteres especiales en rutas

## Ejemplo Completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi Sitio Web</title>
  
  <!-- Ruta relativa a CSS -->
  <link rel="stylesheet" href="css/styles.css">
  
  <!-- Ruta absoluta a fuente externa -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto" rel="stylesheet">
</head>
<body>
  <!-- Ruta relativa a imagen -->
  <img src="images/logo.png" alt="Logo">
  
  <!-- Enlaces internos -->
  <nav>
    <a href="index.html">Inicio</a>
    <a href="paginas/sobre-nosotros.html">Sobre Nosotros</a>
    <a href="contacto.html">Contacto</a>
  </nav>
  
  <!-- Enlace externo absoluto -->
  <a href="https://www.ejemplo.com">Sitio Externo</a>
  
  <!-- Ruta relativa a JavaScript -->
  <script src="js/script.js"></script>
</body>
</html>
```

## ✏️ Ejercicios

### Ejercicio 1: Estructura de sitio
Crea una estructura de carpetas y vincula páginas con rutas relativas.

### Ejercicio 2: Navegación multinivel
Crea un sitio con múltiples niveles de carpetas y navegación correcta.

### Ejercicio 3: Recursos externos e internos
Crea una página que combine rutas absolutas y relativas apropiadamente.

## 📚 Recursos adicionales

- [MDN - URL](https://developer.mozilla.org/es/docs/Learn/Common_questions/What_is_a_URL)
- [MDN - Links](https://developer.mozilla.org/es/docs/Web/HTML/Element/a)

---

**¡Continúa aprendiendo!** Mañana veremos validación HTML.
