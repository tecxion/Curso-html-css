<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-28">Día 28</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-30">Día 30</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml29.png">
</h1>

# Día 29: Flexbox - Layouts Flexibles

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-2.5%20horas-blue)

## 📖 Descripción

Flexbox (Flexible Box Layout) es un sistema de diseño unidimensional que facilita la creación de layouts flexibles y responsivos. Permite distribuir espacio entre elementos y alinearlos de manera eficiente, incluso cuando sus tamaños son desconocidos o dinámicos. Es perfecto para barras de navegación, tarjetas, galerías y componentes de UI.

## 🎯 Objetivos del Día

- Comprender el modelo Flexbox
- Dominar propiedades del contenedor flex
- Controlar propiedades de los elementos flex
- Crear layouts responsivos con Flexbox
- Aplicar Flexbox a casos de uso reales

## 📚 Conceptos de Flexbox

### Contenedor Flex y Elementos Flex

```html
<div class="contenedor">  <!-- Flex container -->
    <div class="item">1</div>  <!-- Flex item -->
    <div class="item">2</div>
    <div class="item">3</div>
</div>
```

```css
.contenedor {
    display: flex;  /* Activa Flexbox */
}
```

## 🔧 Propiedades del Contenedor Flex

### display

```css
.contenedor {
    display: flex;        /* Flexbox en bloque */
    display: inline-flex; /* Flexbox en línea */
}
```

### flex-direction

Dirección del eje principal.

```css
.contenedor {
    flex-direction: row;            /* → (default) */
    flex-direction: row-reverse;    /* ← */
    flex-direction: column;         /* ↓ */
    flex-direction: column-reverse; /* ↑ */
}
```

### flex-wrap

Permite que los elementos se envuelvan en múltiples líneas.

```css
.contenedor {
    flex-wrap: nowrap;       /* No envolver (default) */
    flex-wrap: wrap;         /* Envolver */
    flex-wrap: wrap-reverse; /* Envolver invertido */
}
```

### justify-content

Alineación en el eje principal.

```css
.contenedor {
    justify-content: flex-start;    /* Inicio */
    justify-content: flex-end;      /* Final */
    justify-content: center;        /* Centro */
    justify-content: space-between; /* Espacio entre */
    justify-content: space-around;  /* Espacio alrededor */
    justify-content: space-evenly;  /* Espacio uniforme */
}
```

### align-items

Alineación en el eje transversal.

```css
.contenedor {
    align-items: stretch;     /* Estirar (default) */
    align-items: flex-start;  /* Inicio */
    align-items: flex-end;    /* Final */
    align-items: center;      /* Centro */
    align-items: baseline;    /* Línea base */
}
```

### gap

Espacio entre elementos.

```css
.contenedor {
    gap: 20px;              /* Espacio uniforme */
    row-gap: 20px;          /* Espacio vertical */
    column-gap: 30px;       /* Espacio horizontal */
}
```

## 🎨 Propiedades de los Elementos Flex

### flex-grow

Capacidad de crecer.

```css
.item {
    flex-grow: 0;  /* No crece (default) */
    flex-grow: 1;  /* Crece proporcionalmente */
}
```

### flex-shrink

Capacidad de encogerse.

```css
.item {
    flex-shrink: 1;  /* Puede encogerse (default) */
    flex-shrink: 0;  /* No se encoge */
}
```

### flex-basis

Tamaño base del elemento.

```css
.item {
    flex-basis: auto;   /* Tamaño automático (default) */
    flex-basis: 200px;  /* Tamaño específico */
}
```

### flex (shorthand)

```css
.item {
    flex: 1;              /* flex-grow: 1, flex-shrink: 1, flex-basis: 0 */
    flex: 0 1 auto;       /* grow shrink basis */
}
```

### align-self

Alineación individual.

```css
.item-especial {
    align-self: flex-end;  /* Sobrescribe align-items */
}
```

### order

Orden de aparición.

```css
.item-primero {
    order: -1;  /* Aparece primero */
}
.item-ultimo {
    order: 1;   /* Aparece último */
}
```

## 💻 Patrones Comunes con Flexbox

### 1. Barra de Navegación

```css
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

### 2. Centrado Perfecto

```css
.contenedor {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
```

### 3. Grid de Tarjetas

```css
.grid {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.tarjeta {
    flex: 1 1 300px;  /* Crece, se encoge, base 300px */
}
```

### 4. Layout de 3 Columnas

```css
.contenedor {
    display: flex;
}

.sidebar {
    flex: 0 0 250px;  /* No crece, no se encoge, 250px fijo */
}

.main {
    flex: 1;  /* Ocupa el espacio restante */
}
```

## ✏️ Ejercicios del Día

### Ejercicio 1: Barra de navegación responsive ⭐
Crea una barra de navegación con logo a la izquierda y menú a la derecha usando Flexbox. El menú debe tener 4 enlaces con espacio uniforme entre ellos. Usa `justify-content: space-between` para separar logo y menú, y `gap` para espaciar los enlaces.

[Solución](ejercicio1.html)

### Ejercicio 2: Grid de tarjetas flexible ⭐⭐
Crea una galería de 6 tarjetas de productos que se adapten automáticamente al ancho disponible. Cada tarjeta debe tener imagen, título, descripción y precio. Usa `flex-wrap: wrap`, `gap` para espaciado, y `flex: 1 1 300px` en las tarjetas para que se ajusten responsivamente.

[Solución](ejercicio2.html)

### Ejercicio 3: Layout completo con Flexbox ⭐⭐⭐
Crea un layout de aplicación con: header fijo (logo, navegación, botón de usuario), main con sidebar izquierdo (250px fijo) y área de contenido (flexible), el contenido debe tener tarjetas en grid flexible, y footer con 3 columnas de información. Usa Flexbox para todo el layout, demuestra uso de `flex-direction: column` para la estructura principal, `justify-content` y `align-items` para alineaciones, y `flex-grow` para distribución de espacio.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Usa Flexbox para layouts unidimensionales (filas o columnas)
- Combina `flex-wrap` con `gap` para grids responsivos
- Prefiere `gap` sobre margins para espaciado entre elementos
- Usa `flex: 1` para elementos que deben ocupar espacio disponible
- Combina Flexbox con media queries para diseños responsivos
- Evita usar Flexbox para layouts bidimensionales complejos (usa Grid)
- Usa `align-items: center` para centrado vertical fácil
- Aprovecha `order` para reordenar elementos en responsive
- Usa `flex-basis` en lugar de `width` para tamaños base
- Combina Flexbox con Grid según las necesidades del layout

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-28">Día 28</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-30">Día 30</a>
</h4>
