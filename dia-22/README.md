<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-21">Día 21</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-23">Día 23</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml22.png">
</h1>

# Día 22: Canvas y SVG

![Nivel](https://img.shields.io/badge/nivel-avanzado-red)
![Tiempo](https://img.shields.io/badge/tiempo-2%20horas-blue)

## 📖 Descripción

HTML5 proporciona dos formas de crear gráficos: Canvas (basado en píxeles) y SVG (basado en vectores). Aprenderás las diferencias y cuándo usar cada uno.

## 🎯 Objetivos del Día

- Comprender la diferencia entre Canvas y SVG
- Crear gráficos básicos con SVG
- Dibujar en Canvas con JavaScript
- Decidir cuándo usar cada tecnología

## SVG (Scalable Vector Graphics)

SVG es un formato de imagen vectorial basado en XML.

### Formas Básicas

```html
<svg width="200" height="200">
  <!-- Círculo -->
  <circle cx="100" cy="100" r="50" fill="blue" />
  
  <!-- Rectángulo -->
  <rect x="10" y="10" width="80" height="60" fill="red" />
  
  <!-- Línea -->
  <line x1="0" y1="0" x2="200" y2="200" stroke="black" stroke-width="2" />
  
  <!-- Polígono -->
  <polygon points="100,10 40,180 190,60 10,60 160,180" fill="green" />
</svg>
```

### Texto en SVG

```html
<svg width="300" height="100">
  <text x="10" y="50" font-family="Arial" font-size="24" fill="purple">
    Texto en SVG
  </text>
</svg>
```

### Gradientes

```html
<svg width="200" height="200">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />
    </linearGradient>
  </defs>
  <rect width="200" height="200" fill="url(#grad1)" />
</svg>
```

## Canvas

Canvas es un lienzo para dibujar gráficos con JavaScript.

### Configuración Básica

```html
<canvas id="miCanvas" width="400" height="300"></canvas>

<script>
const canvas = document.getElementById('miCanvas');
const ctx = canvas.getContext('2d');

// Rectángulo
ctx.fillStyle = 'blue';
ctx.fillRect(10, 10, 100, 50);

// Círculo
ctx.beginPath();
ctx.arc(200, 150, 50, 0, 2 * Math.PI);
ctx.fillStyle = 'red';
ctx.fill();

// Línea
ctx.beginPath();
ctx.moveTo(0, 0);
ctx.lineTo(400, 300);
ctx.strokeStyle = 'black';
ctx.lineWidth = 2;
ctx.stroke();
</script>
```

### Texto en Canvas

```html
<script>
ctx.font = '30px Arial';
ctx.fillStyle = 'purple';
ctx.fillText('Hola Canvas', 10, 50);
</script>
```

## SVG vs Canvas

| Característica | SVG | Canvas |
|----------------|-----|--------|
| Tipo | Vectorial | Rasterizado |
| Escalabilidad | Perfecta | Pixelado al escalar |
| Rendimiento | Mejor con pocos objetos | Mejor con muchos objetos |
| Manipulación | DOM (fácil) | JavaScript (complejo) |
| Eventos | Sí, en elementos | Solo en canvas completo |
| Uso ideal | Logos, iconos, gráficos | Juegos, visualizaciones |

## ✏️ Ejercicios

### Ejercicio 1: Formas SVG
Crea una composición con diferentes formas SVG.

### Ejercicio 2: Dibujo en Canvas
Crea un dibujo simple usando Canvas y JavaScript.

### Ejercicio 3: Gráfico comparativo
Crea el mismo gráfico con SVG y Canvas para comparar.

## 📚 Recursos adicionales

- [MDN - SVG](https://developer.mozilla.org/es/docs/Web/SVG)
- [MDN - Canvas](https://developer.mozilla.org/es/docs/Web/API/Canvas_API)

---

**¡Continúa aprendiendo!** Mañana veremos atributos globales.
