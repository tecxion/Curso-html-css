<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-03">Día 3</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-05">Día 5</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml4.png">
</h1>

# Día 4: Listas ordenadas y desordenadas

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

## 📖 Descripción

Las listas en HTML permiten agrupar y organizar información de forma estructurada y clara[web:51][web:67]. Se usan para mostrar colecciones de elementos relacionados, como pasos de instrucciones, menús de navegación o listados de características. HTML ofrece dos tipos principales: listas desordenadas (`<ul>`) y listas ordenadas (`<ol>`), ambas compuestas por elementos de lista `<li>`.

## 🎯 Objetivos del Día

Al finalizar este día serás capaz de:
- Crear listas desordenadas (bullets) con `<ul>`
- Crear listas ordenadas (números) con `<ol>`
- Utilizar la etiqueta `<li>` para cada elemento
- Integrar listas en tus páginas junto a encabezados, párrafos y enlaces

## 📚 Conceptos Clave

### Listas desordenadas (`<ul>`)
Las listas desordenadas muestran elementos sin un orden específico y cada ítem aparece con un icono de viñeta por defecto.


```html
<ul> <li>Primero</li> <li>Segundo</li> <li>Tercero</li> </ul>
```

### Listas ordenadas (`<ol>`)
Las listas ordenadas numeran automáticamente cada elemento para indicar un orden o secuencia.

```html
<ol>
  <li>Paso uno</li>
  <li>Paso dos</li>
  <li>Paso tres</li>
</ol>
```
Usa listas ordenadas cuando el orden de los ítems sí importa, como instrucciones o pasos a seguir.

### Elementos de lista (`<li>`)

Cada elemento de la lista se encierra en la etiqueta `<li>`. Puedes usar cualquier otro elemento dentro de ella, como texto, enlaces, o incluso otras listas.

## 💻 Ejemplos Prácticos

#### Ejemplo 1: Lista de secciones de tu primera web

```html
<h2>Secciones de mi página web</h2>
<ul>
  <li>Inicio</li>
  <li>Sobre mí</li>
  <li>Proyectos</li>
  <li>Contacto</li>
</ul>
```

Este ejemplo usa conceptos de navegación y estructura ya vistos en días anteriores.

#### Ejemplo 2: Pasos para crear una página HTML básica

```html
<h2>Cómo crear una página HTML</h2>
<ol>
  <li>Abre tu editor de código</li>
  <li>Crea un archivo <strong>index.html</strong></li>
  <li>Escribe la estructura básica con <code>&lt;!DOCTYPE html&gt;</code></li>
  <li>Agrega el contenido entre las etiquetas <code>&lt;body&gt;</code></li>
  <li>Guarda y abre el archivo en tu navegador</li>
</ol>
```

Este ejemplo integra encabezados, texto enfatizado y código visto en días anteriores.

#### Ejemplo 3: Lista con enlaces a recursos útiles

```html
<h2>Recursos recomendados</h2>
<ul>
  <li><a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer">MDN Web Docs</a></li>
  <li><a href="https://www.w3schools.com/" target="_blank" rel="noopener noreferrer">W3Schools</a></li>
  <li><a href="https://freecodecamp.org/" target="_blank" rel="noopener noreferrer">freeCodeCamp</a></li>
</ul>
``` 

## ✏️ Ejercicios del Día

#### Ejercicio 1: Lista de ingredientes ⭐
Crea una lista desordenada con los ingredientes de tu receta favorita, usando al menos 5 elementos y resaltando uno con `<strong>` y luego una lista ordenada con los pasos a seguir.

[Ver solución](ejercicio1.html)

#### Ejercicio 2: Pasos para realizar una tarea ⭐⭐

Crea un menú de navegación usando una lista desordenada, donde cada elemento es un enlace (pueden ser relativos, como index.html). Añade al menos 4 secciones (Inicio, Proyectos, Blog, Contacto) y utiliza atributos como title y target cuando corresponda.

[Ver solución](ejercicio2.html)

🔍 Buenas Prácticas<br>
✅ Usa `<ul>` para listas donde el orden no importa, y `<ol>` cuando el orden sí es importante<br>
✅ Siempre encierra cada ítem en `<li>`<br>
✅ Integra las listas junto a títulos, párrafos y enlaces para mejorar la estructura<br>
<br>
❌ No anides listas en este día (se verá más adelante)<br>
❌ No uses listas solo para el diseño visual, deben tener sentido semántico<br>

🎓 Resumen
Usa listas desordenadas para elementos sin secuencia.<br>
Usa listas ordenadas para indicar un paso a paso o prioridad.<br>
Los elementos de lista se crean con `<li>`.<br>
Puedes incluir texto, enlaces, encabezados y énfasis dentro de las listas.<br>