<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-29">Día 29</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/proyecto-final">Proyecto Final</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml30.png">
</h1>

# Día 30: CSS Grid y Proyecto Final

![Nivel](https://img.shields.io/badge/nivel-avanzado-red)
![Tiempo](https://img.shields.io/badge/tiempo-3%20horas-blue)

## 📖 Descripción

CSS Grid es el sistema de diseño bidimensional más poderoso de CSS. Permite crear layouts complejos con filas y columnas simultáneamente, algo que era muy difícil con técnicas anteriores. En este día final, aprenderás Grid y aplicarás todo lo aprendido en un proyecto completo.

## 🎯 Objetivos del Día

- Dominar CSS Grid Layout
- Entender la diferencia entre Grid y Flexbox
- Crear layouts complejos bidimensionales
- Aplicar todos los conocimientos en un proyecto final
- Completar el curso con un portafolio funcional

## 📚 Conceptos de CSS Grid

### Contenedor Grid

```css
.contenedor {
    display: grid;
    grid-template-columns: 200px 200px 200px;  /* 3 columnas de 200px */
    grid-template-rows: 100px 100px;           /* 2 filas de 100px */
    gap: 20px;                                 /* Espacio entre celdas */
}
```

## 🔧 Propiedades del Contenedor Grid

### grid-template-columns / grid-template-rows

```css
.grid {
    /* Tamaños fijos */
    grid-template-columns: 200px 300px 200px;
    
    /* Fracciones (fr) - espacio disponible */
    grid-template-columns: 1fr 2fr 1fr;
    
    /* Repetir */
    grid-template-columns: repeat(3, 1fr);
    
    /* Auto-fit / Auto-fill */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    
    /* Mezclar unidades */
    grid-template-columns: 200px 1fr 2fr;
}
```

### grid-template-areas

Define áreas nombradas.

```css
.grid {
    grid-template-areas:
        "header header header"
        "sidebar main main"
        "footer footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

### gap

```css
.grid {
    gap: 20px;              /* row-gap y column-gap */
    row-gap: 20px;
    column-gap: 30px;
}
```

### justify-items / align-items

Alineación de elementos dentro de sus celdas.

```css
.grid {
    justify-items: start | end | center | stretch;
    align-items: start | end | center | stretch;
}
```

### justify-content / align-content

Alineación del grid completo.

```css
.grid {
    justify-content: start | end | center | space-between | space-around;
    align-content: start | end | center | space-between | space-around;
}
```

## 🎨 Propiedades de los Elementos Grid

### grid-column / grid-row

```css
.item {
    grid-column: 1 / 3;     /* Ocupa columnas 1 y 2 */
    grid-row: 1 / 2;        /* Ocupa fila 1 */
    
    /* Shorthand con span */
    grid-column: span 2;    /* Ocupa 2 columnas */
    grid-row: span 3;       /* Ocupa 3 filas */
}
```

### grid-area

```css
.item {
    grid-area: header;  /* Usa área nombrada */
    
    /* O especifica posición */
    grid-area: 1 / 1 / 2 / 3;  /* row-start / col-start / row-end / col-end */
}
```

## 🆚 Grid vs Flexbox

| Aspecto | Flexbox | Grid |
|---------|---------|------|
| **Dimensiones** | Unidimensional (fila O columna) | Bidimensional (filas Y columnas) |
| **Uso ideal** | Componentes, barras de navegación | Layouts de página completa |
| **Alineación** | En un eje a la vez | En ambos ejes simultáneamente |
| **Orden de elementos** | Sigue el flujo del documento | Posicionamiento explícito |
| **Mejor para** | Distribución de espacio | Estructura de layout |

**Recomendación:** Usa Grid para el layout general y Flexbox para componentes internos.

## 💻 Patrones Comunes con Grid

### 1. Layout de Página Clásico

```css
.page {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
    grid-template-columns: 250px 1fr;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
}
```

### 2. Grid Responsivo Automático

```css
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
}
```

### 3. Grid de 12 Columnas

```css
.grid {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 20px;
}

.item-6 {
    grid-column: span 6;  /* Ocupa 6 columnas (50%) */
}
```

## 🚀 Proyecto Final

Crea un sitio web completo de portafolio personal que incluya:

### Requisitos del Proyecto:

1. **Estructura HTML Semántica**
   - Header, nav, main, sections, footer
   - Uso correcto de article, aside
   - Meta tags para SEO

2. **Estilos CSS Completos**
   - Variables CSS para colores y tamaños
   - Google Fonts (mínimo 2 fuentes)
   - Grid para layout principal
   - Flexbox para componentes internos
   - Box model correcto (box-sizing: border-box)

3. **Páginas/Secciones**
   - Hero section con presentación
   - Sobre mí con foto y descripción
   - Habilidades (lista o grid)
   - Portafolio/Proyectos (grid de tarjetas)
   - Contacto (formulario o información)
   - Footer con redes sociales

4. **Diseño Responsivo**
   - Mobile-first approach
   - Media queries para tablet y desktop
   - Grid y Flexbox responsivos

5. **Buenas Prácticas**
   - Código limpio y comentado
   - Paleta de colores consistente
   - Tipografía jerárquica
   - Espaciados consistentes
   - Accesibilidad básica

[Ver Proyecto Final](proyecto-final/index.html)

## 🔍 Buenas Prácticas

- Usa Grid para layouts bidimensionales complejos
- Combina Grid con Flexbox para mejores resultados
- Aprovecha `grid-template-areas` para layouts legibles
- Usa `fr` para distribución flexible de espacio
- `repeat(auto-fit, minmax())` para grids responsivos automáticos
- Mantén la simplicidad: no uses Grid si Flexbox es suficiente
- Usa `gap` en lugar de margins para espaciado en Grid
- Considera el soporte de navegadores (Grid es ampliamente soportado)
- Planifica tu grid en papel antes de codificar
- Usa herramientas de desarrollo para visualizar el grid

## 🎉 ¡Felicitaciones!

Has completado el curso de HTML y CSS. Ahora tienes las habilidades fundamentales para:

- Crear estructuras HTML semánticas y accesibles
- Diseñar layouts modernos con Flexbox y Grid
- Aplicar estilos profesionales con CSS
- Construir sitios web responsivos
- Seguir mejores prácticas de desarrollo web

**Próximos pasos sugeridos:**
- Practica creando más proyectos
- Aprende JavaScript para interactividad
- Explora frameworks como React o Vue
- Estudia preprocesadores CSS (Sass)
- Aprende sobre animaciones CSS avanzadas

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-29">Día 29</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/proyecto-final">Proyecto Final</a>
</h4>
