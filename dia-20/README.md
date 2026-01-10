<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-19">Día 19</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-21">Día 21</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml20.png">
</h1>

# Día 20: Accesibilidad Web - ARIA y Diseño Inclusivo

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-2%20horas-blue)

## 📖 Descripción

La accesibilidad web asegura que todas las personas, incluidas aquellas con discapacidades, puedan usar la web. ARIA (Accessible Rich Internet Applications) proporciona atributos para mejorar la accesibilidad de aplicaciones web dinámicas.

## 🎯 Objetivos del Día

- Comprender la importancia de la accesibilidad web
- Utilizar atributos ARIA correctamente
- Implementar navegación por teclado
- Crear formularios accesibles
- Usar HTML semántico para mejor accesibilidad

## Atributos ARIA Esenciales

### `role`
```html
<nav role="navigation">
  <a href="#home">Inicio</a>
</nav>

<div role="button" tabindex="0">Botón personalizado</div>
```

### `aria-label`
```html
<button aria-label="Cerrar ventana">
  <span aria-hidden="true">&times;</span>
</button>
```

### `aria-labelledby` y `aria-describedby`
```html
<h2 id="section-title">Configuración</h2>
<div aria-labelledby="section-title">
  <input type="password" aria-describedby="password-help">
  <p id="password-help">Mínimo 8 caracteres</p>
</div>
```

## Navegación por Teclado

```html
<a href="#main-content" class="skip-link">Saltar al contenido</a>

<div tabindex="0">Elemento enfocable</div>
<div tabindex="-1">Enfocable programáticamente</div>
```

## Formularios Accesibles

```html
<form>
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" required aria-required="true">
  
  <fieldset>
    <legend>Género</legend>
    <input type="radio" id="m" name="genero" value="m">
    <label for="m">Masculino</label>
  </fieldset>
</form>
```

## ✏️ Ejercicios

### Ejercicio 1: Formulario accesible
Crea un formulario de contacto completamente accesible.

### Ejercicio 2: Navegación accesible
Crea una navegación con skip links y ARIA labels.

### Ejercicio 3: Página completa accesible
Crea una página web completa siguiendo todas las mejores prácticas de accesibilidad.

## 📚 Recursos adicionales

- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [MDN - ARIA](https://developer.mozilla.org/es/docs/Web/Accessibility/ARIA)

---

**¡Continúa aprendiendo!** Mañana veremos formularios avanzados.
