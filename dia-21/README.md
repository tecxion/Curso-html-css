<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-20">Día 20</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-22">Día 22</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml21.png">
</h1>

# Día 21: Formularios Avanzados

![Nivel](https://img.shields.io/badge/nivel-avanzado-red)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)

## 📖 Descripción

HTML5 introdujo nuevos tipos de input y elementos de formulario que mejoran la experiencia del usuario y la validación. Aprenderás a usar datalist, output, y tipos de input avanzados.

## 🎯 Objetivos del Día

- Utilizar el elemento `<datalist>` para autocompletado
- Implementar el elemento `<output>` para resultados
- Usar nuevos tipos de input de HTML5
- Crear formularios interactivos y dinámicos

## Elemento `<datalist>`

Proporciona opciones de autocompletado:

```html
<label for="navegador">Elige tu navegador:</label>
<input list="navegadores" id="navegador" name="navegador">
<datalist id="navegadores">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
  <option value="Edge">
  <option value="Opera">
</datalist>
```

## Elemento `<output>`

Muestra el resultado de un cálculo:

```html
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="number" id="a" value="0"> +
  <input type="number" id="b" value="0"> =
  <output name="result" for="a b">0</output>
</form>
```

## Tipos de Input Avanzados

### Color
```html
<label for="color">Elige un color:</label>
<input type="color" id="color" name="color" value="#4A90E2">
```

### Range (Slider)
```html
<label for="volumen">Volumen:</label>
<input type="range" id="volumen" name="volumen" min="0" max="100" value="50">
<output for="volumen">50</output>
```

### Date, Time, DateTime-Local
```html
<label for="fecha">Fecha:</label>
<input type="date" id="fecha" name="fecha">

<label for="hora">Hora:</label>
<input type="time" id="hora" name="hora">

<label for="fechahora">Fecha y Hora:</label>
<input type="datetime-local" id="fechahora" name="fechahora">
```

### Week y Month
```html
<label for="semana">Semana:</label>
<input type="week" id="semana" name="semana">

<label for="mes">Mes:</label>
<input type="month" id="mes" name="mes">
```

## Atributos Avanzados

### `pattern`
```html
<input type="text" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" 
       placeholder="123-456-7890" title="Formato: 123-456-7890">
```

### `min`, `max`, `step`
```html
<input type="number" min="0" max="100" step="5">
```

### `multiple`
```html
<input type="file" multiple>
<input type="email" multiple>
```

### `autocomplete`
```html
<input type="email" autocomplete="email">
<input type="tel" autocomplete="tel">
```

## Ejemplo Completo

```html
<form>
  <h2>Calculadora de Propina</h2>
  
  <label for="total">Total de la cuenta:</label>
  <input type="number" id="total" min="0" step="0.01" value="50">
  
  <label for="propina">Propina (%):</label>
  <input type="range" id="propina" min="0" max="30" value="15" 
         oninput="calcular()">
  <output id="porcentaje">15</output>%
  
  <p>Total con propina: <output id="resultado">57.50</output>€</p>
</form>
```

## ✏️ Ejercicios

### Ejercicio 1: Formulario con datalist
Crea un formulario de búsqueda con autocompletado usando datalist.

### Ejercicio 2: Calculadora interactiva
Crea una calculadora usando range inputs y output.

### Ejercicio 3: Formulario de reserva
Crea un formulario de reserva con date, time y otros inputs avanzados.

## 📚 Recursos adicionales

- [MDN - Input Types](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)
- [MDN - datalist](https://developer.mozilla.org/es/docs/Web/HTML/Element/datalist)

---

**¡Continúa aprendiendo!** Mañana veremos Canvas y SVG.
