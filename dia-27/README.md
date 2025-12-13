<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-26">Día 26</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-28">Día 28</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml27.png">
</h1>

# Día 27: Modelo de Caja (Box Model)

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-2%20horas-blue)

## Índice
* [Objetivo](#objetivo)
* [¿Qué es el Box Model?](#box-model)
* [Componentes del Box Model](#componentes)
* [Box-sizing](#box-sizing)
* [Margin Collapse](#margin-collapse)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

El Modelo de Caja (Box Model) es uno de los conceptos más fundamentales de CSS. Cada elemento HTML se representa como una caja rectangular que consta de cuatro áreas: contenido, padding, border y margin. Comprender cómo funciona el box model es esencial para controlar el espaciado, tamaño y posicionamiento de los elementos en una página web.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

- Comprender el concepto del Box Model
- Dominar padding, margin, border y content
- Utilizar la propiedad box-sizing
- Entender el margin collapse
- Crear layouts precisos controlando espaciados

<a name="box-model"></a>

## 📦 ¿Qué es el Box Model?

Cada elemento HTML es una caja rectangular compuesta por cuatro capas:

```
┌─────────────────────────────────────┐
│           MARGIN (transparente)      │
│  ┌──────────────────────────────┐  │
│  │     BORDER (visible)         │  │
│  │  ┌───────────────────────┐  │  │
│  │  │   PADDING (transparente) │  │
│  │  │  ┌─────────────────┐  │  │  │
│  │  │  │   CONTENT       │  │  │  │
│  │  │  │  (texto/imagen) │  │  │  │
│  │  │  └─────────────────┘  │  │  │
│  │  └───────────────────────┘  │  │
│  └──────────────────────────────┘  │
└─────────────────────────────────────┘
```

<a name="componentes"></a>

## 🔧 Componentes del Box Model

### 1. Content (Contenido)

El área donde aparece el contenido (texto, imágenes, etc.).

```css
div {
    width: 300px;
    height: 200px;
}
```

### 2. Padding (Relleno)

Espacio transparente entre el contenido y el borde.

```css
/* Padding en todos los lados */
div {
    padding: 20px;
}

/* Padding individual */
div {
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 10px;
    padding-left: 15px;
}

/* Shorthand (arriba, derecha, abajo, izquierda) */
div {
    padding: 10px 15px 10px 15px;
}

/* Shorthand (vertical, horizontal) */
div {
    padding: 10px 15px;
}
```

### 3. Border (Borde)

Línea que rodea el padding y el contenido.

```css
/* Border completo */
div {
    border: 2px solid #667eea;
}

/* Border individual */
div {
    border-width: 2px;
    border-style: solid;
    border-color: #667eea;
}

/* Bordes específicos */
div {
    border-top: 1px solid black;
    border-right: 2px dashed red;
    border-bottom: 3px dotted blue;
    border-left: 4px double green;
}

/* Border radius (esquinas redondeadas) */
div {
    border-radius: 10px;
}
```

**Estilos de border:**
- `solid` - Línea sólida
- `dashed` - Línea discontinua
- `dotted` - Puntos
- `double` - Línea doble
- `groove`, `ridge`, `inset`, `outset` - Efectos 3D
- `none` - Sin borde

### 4. Margin (Margen)

Espacio transparente fuera del borde, separa el elemento de otros elementos.

```css
/* Margin en todos los lados */
div {
    margin: 20px;
}

/* Margin individual */
div {
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 10px;
    margin-left: 15px;
}

/* Centrar horizontalmente */
div {
    width: 300px;
    margin: 0 auto;
}

/* Margin negativo (acerca elementos) */
div {
    margin-top: -10px;
}
```

<a name="box-sizing"></a>

## 📏 Box-sizing

Por defecto, `width` y `height` solo afectan al **content**. Padding y border se añaden al tamaño total.

### Problema con box-sizing: content-box (default)

```css
div {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
}
/* Ancho total = 300px + 40px (padding) + 10px (border) = 350px */
```

### Solución: box-sizing: border-box ✅

```css
div {
    box-sizing: border-box;
    width: 300px;
    padding: 20px;
    border: 5px solid black;
}
/* Ancho total = 300px (incluye padding y border) */
```

**Mejor práctica:** Aplicar a todos los elementos

```css
* {
    box-sizing: border-box;
}
```

<a name="margin-collapse"></a>

## 🔄 Margin Collapse

Los márgenes verticales de elementos adyacentes se "colapsan" (fusionan), tomando el valor del margen mayor.

```html
<div class="caja1">Caja 1</div>
<div class="caja2">Caja 2</div>
```

```css
.caja1 {
    margin-bottom: 30px;
}

.caja2 {
    margin-top: 20px;
}
/* Espacio entre cajas = 30px (no 50px) */
```

**Casos donde NO ocurre margin collapse:**
- Elementos con `float` o `position: absolute`
- Elementos flex o grid items
- Elementos con `overflow` diferente de `visible`

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Box Model Básico

```html
<div class="caja">
    <p>Contenido de la caja</p>
</div>
```

```css
.caja {
    width: 300px;
    padding: 20px;
    border: 3px solid #667eea;
    margin: 30px;
    background-color: #f0f0f0;
}
```

### Ejemplo 2: Tarjetas con Box Model

```html
<div class="tarjeta">
    <h3>Título</h3>
    <p>Descripción de la tarjeta</p>
</div>
```

```css
* {
    box-sizing: border-box;
}

.tarjeta {
    width: 300px;
    padding: 25px;
    margin: 20px;
    border: 1px solid #ddd;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.tarjeta h3 {
    margin-top: 0;
    margin-bottom: 15px;
}

.tarjeta p {
    margin: 0;
}
```

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día

### Ejercicio 1: Cajas básicas con box model ⭐
Crea una página con 3 divs que representen cajas de colores diferentes. Cada caja debe tener: width de 200px, height de 150px, padding de 20px, border de 3px solid (color diferente para cada una), margin de 15px, y un color de fondo diferente. Aplica `box-sizing: border-box` a todos los elementos y observa cómo afecta el tamaño total.

[Solución](ejercicio1.html)

### Ejercicio 2: Tarjetas de productos ⭐⭐
Crea una página con 3 tarjetas de productos en línea (usa `display: inline-block`). Cada tarjeta debe incluir: una imagen placeholder, título del producto, descripción breve, y precio. Usa el box model para: padding interno de 20px, border de 1px con color suave, margin entre tarjetas de 15px, border-radius de 8px, y box-shadow para profundidad. Asegúrate de que todas las tarjetas tengan el mismo tamaño usando box-sizing.

[Solución](ejercicio2.html)

### Ejercicio 3: Layout completo con espaciados ⭐⭐⭐
Crea una página de blog con: header (padding 30px, border-bottom 3px), main con 2 columnas usando float (artículo principal 70% width, sidebar 25% width, margin entre ellas 5%), cada artículo con padding 25px y margin-bottom 30px, sidebar con widgets (cada uno con padding 15px, margin-bottom 20px, border 1px), y footer (padding 20px, border-top 2px, margin-top 40px). Demuestra comprensión del margin collapse y usa box-sizing: border-box para todo.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa `box-sizing: border-box` en todos tus proyectos para cálculos más intuitivos
- Prefiere padding para espaciado interno y margin para separación entre elementos
- Usa margin auto para centrar elementos horizontalmente
- Recuerda que padding y border afectan el área clickeable de un elemento
- Utiliza border-radius para esquinas redondeadas modernas
- Ten en cuenta el margin collapse al espaciar elementos verticalmente
- Usa herramientas de desarrollo del navegador para visualizar el box model
- Evita anchos fijos cuando sea posible; usa max-width para responsividad
- Considera usar rem o em para padding/margin en lugar de px para mejor escalabilidad

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-26">Día 26</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-28">Día 28</a>
</h4>
