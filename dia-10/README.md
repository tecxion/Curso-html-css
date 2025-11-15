<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-09">Día 9</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-11">Día 11</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml10.png">
</h1>

# Día 10: Formularios Parte 2 - `<textarea>`, `<select>`, `<button>`

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Indice

- [Día 10: Formularios Parte 2 - `<textarea>`, `<select>`, `<button>`](#día-10-formularios-parte-2---textarea-select-button)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [Áreas de texto para contenido extenso](#áreas-de-texto-para-contenido-extenso)
  - [Etiqueta `<textarea>`](#etiqueta-textarea)
    - [Atributos principales de `<textarea>`](#atributos-principales-de-textarea)
  - [Etiqueta `<select>`](#etiqueta-select)


## 📖 Descripción

En la primera parte de formularios aprendiste los elementos básicos como `<input>` y sus tipos. Ahora es momento de ampliar tu conocimiento con elementos más especializados que ofrecen mayor flexibilidad y mejores experiencias de usuario. En este día descubrirás `<textarea>` para textos largos, `<select>` para crear menús desplegables con opciones, y `<button>` para crear botones más versátiles y personalizables.

Estos elementos son fundamentales para crear formularios completos y profesionales que cubran todas las necesidades de interacción con el usuario.


## 🎯 Objetivos del Día

Al acabar este día podrás:

- Crear áreas de texto multilínea con `<textarea>`
- Implementar menús desplegables con `<select>` y `<option>`
- Agrupar opciones con `<optgroup>`
- Utilizar la etiqueta `<button>` y sus diferentes tipos
- Combinar todos los elementos de formulario aprendidos hasta ahora

## 📚 Conceptos Clave

### Áreas de texto para contenido extenso


## Etiqueta `<textarea>`

La etiqueta `<textarea>` crea un área de texto multilínea donde los usuarios pueden escribir contenido extenso como comentarios, mensajes o descripciones.

```html
<textarea name="comentario" rows="5" cols="40"> Texto predeterminado aquí </textarea>
```

A diferencia de `<input>`, `<textarea>` tiene etiqueta de apertura y cierre. El contenido entre las etiquetas aparece como texto predeterminado.

### Atributos principales de `<textarea>`

**rows**: Especifica el número de líneas visibles (altura) del área de texto.

```html
<textarea rows="10"></textarea>
```

**cols**: Especifica el número de columnas (ancho) del área de texto en caracteres.
```html
<textarea cols="50"></textarea>
```

**name**: Identifica el campo cuando se envían los datos al servidor.

```html
<textarea name="mensaje"></textarea>
```

**placeholder**: Texto de ejemplo que desaparece cuando el usuario empieza a escribir.

```html
<textarea placeholder="Escribe tu mensaje aquí..."></textarea>
```

**required**: Hace que el campo sea obligatorio.

```html
<textarea required></textarea>
```

**maxlength**: Limita el número máximo de caracteres que se pueden escribir.

```html
<textarea maxlength="500"></textarea>
```

**readonly**: El campo es de solo lectura (no editable).

```html
<textarea readonly>Texto no editable</textarea>
```

**disabled**: Desactiva el campo completamente.

```html
<textarea disabled></textarea>
``` 

**wrap**: Controla cómo se ajusta el texto al enviarse. Valores: `soft` (por defecto) o `hard`.

```html
<textarea wrap="hard"></textarea>
```


## Etiqueta `<select>`

La etiqueta `<select>` crea un menú desplegable que permite al usuario elegir una o varias opciones de una lista predefinida.


