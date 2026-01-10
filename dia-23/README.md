<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-22">Día 22</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-24">Día 24</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml23.png">
</h1>

# Día 23: Atributos Globales

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

Los atributos globales pueden usarse en cualquier elemento HTML. Aprenderás a usar class, id, data-*, style y otros atributos esenciales.

## 🎯 Objetivos del Día

- Comprender los atributos globales más importantes
- Usar `class` e `id` correctamente
- Implementar atributos `data-*` personalizados
- Conocer otros atributos globales útiles

## Atributo `class`

Asigna una o más clases CSS:

```html
<div class="container">Contenedor</div>
<p class="text-large text-bold">Texto grande y negrita</p>
```

## Atributo `id`

Identificador único en la página:

```html
<div id="header">Encabezado</div>
<section id="main-content">Contenido principal</section>
```

**Reglas:**
- Debe ser único en la página
- Útil para enlaces internos y JavaScript
- Preferir `class` para estilos

## Atributos `data-*`

Almacenan datos personalizados:

```html
<article data-author="Juan Pérez" data-date="2025-01-08" data-category="HTML">
  <h2>Título del artículo</h2>
</article>

<button data-action="delete" data-id="123">Eliminar</button>

<script>
const article = document.querySelector('article');
console.log(article.dataset.author); // "Juan Pérez"
console.log(article.dataset.date); // "2025-01-08"
</script>
```

## Atributo `style`

Estilos CSS en línea (evitar cuando sea posible):

```html
<p style="color: red; font-size: 18px;">Texto rojo</p>
```

## Atributo `title`

Información adicional (tooltip):

```html
<abbr title="HyperText Markup Language">HTML</abbr>
<button title="Guardar cambios">💾</button>
```

## Atributo `hidden`

Oculta el elemento:

```html
<div hidden>Este contenido está oculto</div>
```

## Atributo `contenteditable`

Hace el contenido editable:

```html
<div contenteditable="true">
  Puedes editar este texto
</div>
```

## Atributo `draggable`

Permite arrastrar el elemento:

```html
<div draggable="true">Arrástra me</div>
```

## Atributo `lang`

Especifica el idioma:

```html
<p lang="es">Texto en español</p>
<p lang="en">Text in English</p>
```

## Atributo `dir`

Dirección del texto:

```html
<p dir="ltr">Izquierda a derecha</p>
<p dir="rtl">Derecha a izquierda (árabe, hebreo)</p>
```

## Atributo `tabindex`

Controla el orden de tabulación:

```html
<div tabindex="0">Puede recibir foco</div>
<div tabindex="-1">Foco programático</div>
```

## Ejemplo Completo

```html
<article 
  id="article-123"
  class="blog-post featured"
  data-author="Juan Pérez"
  data-date="2025-01-08"
  data-views="1500"
  lang="es">
  
  <h2 title="Publicado el 8 de enero de 2025">
    Atributos Globales en HTML
  </h2>
  
  <p>Contenido del artículo...</p>
  
  <button 
    data-action="like" 
    data-post-id="123"
    title="Me gusta este artículo">
    👍 Me gusta
  </button>
</article>
```

## ✏️ Ejercicios

### Ejercicio 1: Uso de class e id
Crea una página usando class e id apropiadamente.

### Ejercicio 2: Data attributes
Crea una galería de imágenes usando data-* para almacenar información.

### Ejercicio 3: Atributos combinados
Crea una página que use múltiples atributos globales de forma práctica.

## 📚 Recursos adicionales

- [MDN - Global Attributes](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes)
- [MDN - data-* attributes](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/data-*)

---

**¡Continúa aprendiendo!** Mañana veremos rutas y enlaces.
