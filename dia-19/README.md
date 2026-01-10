<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-18">Día 18</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-20">Día 20</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml19.png">
</h1>

# Día 19: Caracteres Especiales y Entidades HTML

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

Las entidades HTML permiten mostrar caracteres especiales que tienen significado en HTML o que no están disponibles en el teclado. Aprenderás a usar entidades para símbolos, caracteres acentuados y caracteres reservados.

## 🎯 Objetivos del Día

- Comprender qué son las entidades HTML
- Usar entidades para caracteres reservados
- Mostrar símbolos especiales y matemáticos
- Trabajar con caracteres acentuados y de diferentes idiomas

## ¿Qué son las Entidades HTML?

Las entidades HTML son códigos que representan caracteres especiales. Comienzan con `&` y terminan con `;`.

### Sintaxis

```html
&nombre;    <!-- Entidad con nombre -->
&#número;   <!-- Entidad numérica decimal -->
&#xhexadecimal; <!-- Entidad numérica hexadecimal -->
```

## Caracteres Reservados

Estos caracteres tienen significado especial en HTML y deben ser escapados:

| Carácter | Entidad | Descripción |
|----------|---------|-------------|
| < | `&lt;` | Menor que |
| > | `&gt;` | Mayor que |
| & | `&amp;` | Ampersand |
| " | `&quot;` | Comillas dobles |
| ' | `&apos;` o `&#39;` | Apóstrofo |

### Ejemplo

```html
<p>Para escribir código HTML usa &lt;p&gt; y &lt;/p&gt;</p>
<p>Resultado: Para escribir código HTML usa <p> y </p></p>

<p>5 &lt; 10 &amp;&amp; 10 &gt; 5</p>
<p>Resultado: 5 < 10 && 10 > 5</p>
```

## Espacios y Saltos

| Entidad | Descripción |
|---------|-------------|
| `&nbsp;` | Espacio sin ruptura (non-breaking space) |
| `&ensp;` | Espacio en (mitad de em) |
| `&emsp;` | Espacio em |
| `&thinsp;` | Espacio fino |

### Ejemplo

```html
<p>Palabra1&nbsp;&nbsp;&nbsp;Palabra2</p>
<p>Nombre:&emsp;Juan Pérez</p>
```

## Símbolos Comunes

| Símbolo | Entidad | Descripción |
|---------|---------|-------------|
| © | `&copy;` | Copyright |
| ® | `&reg;` | Marca registrada |
| ™ | `&trade;` | Trademark |
| € | `&euro;` | Euro |
| £ | `&pound;` | Libra |
| ¥ | `&yen;` | Yen |
| ¢ | `&cent;` | Centavo |
| § | `&sect;` | Sección |
| ¶ | `&para;` | Párrafo |
| • | `&bull;` | Viñeta |
| … | `&hellip;` | Puntos suspensivos |
| – | `&ndash;` | Guion corto (en dash) |
| — | `&mdash;` | Guion largo (em dash) |

### Ejemplo

```html
<p>&copy; 2025 Mi Empresa. Todos los derechos reservados.</p>
<p>Precio: 99&euro;</p>
<p>Marca Registrada&reg;</p>
```

## Caracteres Acentuados

| Carácter | Entidad | Carácter | Entidad |
|----------|---------|----------|---------|
| á | `&aacute;` | Á | `&Aacute;` |
| é | `&eacute;` | É | `&Eacute;` |
| í | `&iacute;` | Í | `&Iacute;` |
| ó | `&oacute;` | Ó | `&Oacute;` |
| ú | `&uacute;` | Ú | `&Uacute;` |
| ñ | `&ntilde;` | Ñ | `&Ntilde;` |
| ü | `&uuml;` | Ü | `&Uuml;` |

**Nota:** Con UTF-8 puedes escribir estos caracteres directamente, pero las entidades son útiles para compatibilidad.

## Símbolos Matemáticos

| Símbolo | Entidad | Descripción |
|---------|---------|-------------|
| × | `&times;` | Multiplicación |
| ÷ | `&divide;` | División |
| ± | `&plusmn;` | Más/menos |
| ≠ | `&ne;` | No igual |
| ≤ | `&le;` | Menor o igual |
| ≥ | `&ge;` | Mayor o igual |
| ∞ | `&infin;` | Infinito |
| √ | `&radic;` | Raíz cuadrada |
| ∑ | `&sum;` | Suma |
| ∏ | `&prod;` | Producto |
| ∫ | `&int;` | Integral |

### Ejemplo

```html
<p>2 &times; 3 = 6</p>
<p>10 &divide; 2 = 5</p>
<p>x &ge; 0</p>
```

## Flechas y Símbolos

| Símbolo | Entidad | Descripción |
|---------|---------|-------------|
| ← | `&larr;` | Flecha izquierda |
| → | `&rarr;` | Flecha derecha |
| ↑ | `&uarr;` | Flecha arriba |
| ↓ | `&darr;` | Flecha abajo |
| ↔ | `&harr;` | Flecha doble |
| ♠ | `&spades;` | Picas |
| ♣ | `&clubs;` | Tréboles |
| ♥ | `&hearts;` | Corazones |
| ♦ | `&diams;` | Diamantes |
| ★ | `&#9733;` | Estrella |
| ☆ | `&#9734;` | Estrella vacía |

## 💻 Ejemplos Prácticos

### Ejemplo 1: Mostrar código HTML

```html
<pre>
<code>
&lt;!DOCTYPE html&gt;
&lt;html lang="es"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;title&gt;Mi Página&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Hola Mundo&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;
</code>
</pre>
```

### Ejemplo 2: Símbolos en contenido

```html
<footer>
    <p>&copy; 2025 Mi Empresa&reg;. Todos los derechos reservados.</p>
    <p>Precio: 99,99&euro; | Descuento: 10&percnt;</p>
    <p>Contacto: info@ejemplo.com &bull; Tel: +34 123 456 789</p>
</footer>
```

### Ejemplo 3: Fórmulas matemáticas

```html
<p>La fórmula del área de un círculo es: A = &pi;r&sup2;</p>
<p>Teorema de Pitágoras: a&sup2; + b&sup2; = c&sup2;</p>
<p>Límite: lim<sub>x&rarr;&infin;</sub> f(x) = L</p>
```

## ✏️ Ejercicios

### Ejercicio 1: Página con símbolos comunes
Crea una página que muestre diferentes símbolos de copyright, monedas y marcas.

### Ejercicio 2: Mostrar código HTML
Crea una página que muestre código HTML usando entidades.

### Ejercicio 3: Fórmulas matemáticas
Crea una página con fórmulas matemáticas usando entidades y elementos sub/sup.

## 🎯 Resumen

- Las entidades HTML representan caracteres especiales
- Comienzan con `&` y terminan con `;`
- Usa `&lt;` `&gt;` `&amp;` para caracteres reservados
- Disponibles para símbolos, matemáticas y caracteres especiales
- Con UTF-8 muchos caracteres se pueden escribir directamente

## 📚 Recursos adicionales

- [MDN - HTML Entities](https://developer.mozilla.org/es/docs/Glossary/Entity)
- [HTML Entity Reference](https://www.w3schools.com/html/html_entities.asp)
- [Complete HTML Entity List](https://html.spec.whatwg.org/multipage/named-characters.html)

---

**¡Continúa aprendiendo!** Mañana veremos accesibilidad web y ARIA.
