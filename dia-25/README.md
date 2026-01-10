<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-24">Día 24</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-26">Día 26</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml25.png">
</h1>

# Día 25: Validación HTML - W3C Validator

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

La validación HTML asegura que tu código cumple con los estándares web. Aprenderás a usar el W3C Validator y a corregir errores comunes.

## 🎯 Objetivos del Día

- Comprender la importancia de la validación HTML
- Usar el W3C Markup Validation Service
- Identificar y corregir errores comunes
- Escribir HTML válido y conforme a estándares

## ¿Por qué Validar HTML?

### Beneficios

1. **Compatibilidad entre navegadores**
2. **Mejor SEO**
3. **Accesibilidad mejorada**
4. **Mantenimiento más fácil**
5. **Rendimiento optimizado**
6. **Profesionalismo**

## W3C Markup Validation Service

### Cómo Usar

1. Visita: https://validator.w3.org/
2. Opciones:
   - **Validate by URI**: Introduce la URL
   - **Validate by File Upload**: Sube el archivo HTML
   - **Validate by Direct Input**: Pega el código

## Errores Comunes

### 1. Falta DOCTYPE

❌ **Incorrecto:**
```html
<html>
<head>
  <title>Mi Página</title>
</head>
```

✅ **Correcto:**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <title>Mi Página</title>
</head>
```

### 2. Etiquetas sin Cerrar

❌ **Incorrecto:**
```html
<p>Párrafo sin cerrar
<div>Contenido</div>
```

✅ **Correcto:**
```html
<p>Párrafo cerrado</p>
<div>Contenido</div>
```

### 3. Atributos sin Comillas

❌ **Incorrecto:**
```html
<img src=imagen.jpg alt=Foto>
```

✅ **Correcto:**
```html
<img src="imagen.jpg" alt="Foto">
```

### 4. Atributos Duplicados

❌ **Incorrecto:**
```html
<div id="contenedor" id="main">
```

✅ **Correcto:**
```html
<div id="contenedor" class="main">
```

### 5. Elementos Anidados Incorrectamente

❌ **Incorrecto:**
```html
<p>Texto <div>dentro</div> de párrafo</p>
```

✅ **Correcto:**
```html
<p>Texto <span>dentro</span> de párrafo</p>
```

### 6. IDs Duplicados

❌ **Incorrecto:**
```html
<div id="header">Encabezado 1</div>
<div id="header">Encabezado 2</div>
```

✅ **Correcto:**
```html
<div id="header1">Encabezado 1</div>
<div id="header2">Encabezado 2</div>
```

### 7. Atributo alt Faltante en Imágenes

❌ **Incorrecto:**
```html
<img src="foto.jpg">
```

✅ **Correcto:**
```html
<img src="foto.jpg" alt="Descripción de la foto">
```

### 8. Caracteres Especiales sin Escapar

❌ **Incorrecto:**
```html
<p>5 < 10 & 10 > 5</p>
```

✅ **Correcto:**
```html
<p>5 &lt; 10 &amp; 10 &gt; 5</p>
```

## Ejemplo de HTML Válido

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Página de ejemplo válida">
  <title>Página Válida</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Mi Sitio Web</h1>
    <nav>
      <ul>
        <li><a href="index.html">Inicio</a></li>
        <li><a href="sobre-nosotros.html">Sobre Nosotros</a></li>
        <li><a href="contacto.html">Contacto</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <article>
      <h2>Título del Artículo</h2>
      <p>Este es un párrafo de ejemplo con HTML válido.</p>
      <img src="imagen.jpg" alt="Descripción de la imagen" width="600" height="400">
    </article>
  </main>
  
  <footer>
    <p>&copy; 2025 Mi Sitio Web. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
```

## Mejores Prácticas

### ✅ Hacer

1. Siempre incluir `<!DOCTYPE html>`
2. Especificar el idioma con `lang`
3. Usar UTF-8 como charset
4. Cerrar todas las etiquetas
5. Usar comillas en atributos
6. Incluir `alt` en todas las imágenes
7. Validar regularmente durante el desarrollo
8. Usar HTML semántico
9. Mantener IDs únicos
10. Anidar elementos correctamente

### ❌ Evitar

1. Omitir DOCTYPE
2. Etiquetas sin cerrar
3. Atributos sin comillas
4. IDs duplicados
5. Anidación incorrecta
6. Caracteres especiales sin escapar
7. Atributos obsoletos
8. Uso excesivo de `<div>` y `<span>`

## Herramientas de Validación

### Online
- [W3C Markup Validator](https://validator.w3.org/)
- [HTML5 Validator](https://html5.validator.nu/)

### Extensiones de Navegador
- **W3C Web Validator** (Chrome/Firefox)
- **HTML Validator** (Firefox)

### Editores de Código
- **VS Code**: HTMLHint, W3C Validation
- **Sublime Text**: SublimeLinter-html-tidy

## ✏️ Ejercicios

### Ejercicio 1: Validar HTML
Crea una página HTML válida y valídala con W3C Validator.

### Ejercicio 2: Corregir errores
Toma un HTML con errores y corrígelos hasta que pase la validación.

### Ejercicio 3: Proyecto completo validado
Crea un sitio web completo de múltiples páginas, todas validadas.

## 🎯 Resumen

- La validación HTML es esencial para calidad y compatibilidad
- W3C Validator es la herramienta estándar
- Errores comunes: etiquetas sin cerrar, atributos sin comillas, IDs duplicados
- HTML válido mejora SEO, accesibilidad y mantenimiento
- Validar regularmente durante el desarrollo

## 📚 Recursos adicionales

- [W3C Markup Validator](https://validator.w3.org/)
- [MDN - HTML Validation](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML)
- [HTML Best Practices](https://github.com/hail2u/html-best-practices)

---

**¡Felicidades!** Has completado el curso de HTML. Mañana comenzarás con CSS.
