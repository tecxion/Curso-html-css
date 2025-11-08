<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-06">Día 6</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-08">Día 8</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml7.png">
</h1>

# Día 7: Tablas básicas - Etiquetas `<table>`, `<tr>`, `<td>`, `<th>`

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

---

## Índice

- [Día 7: Tablas básicas - Etiquetas `<table>`, `<tr>`, `<td>`, `<th>`](#día-7-tablas-básicas---etiquetas-table-tr-td-th)
  - [Índice](#índice)
  - [Descripción](#descripción)
  - [Objetivos del Día](#objetivos-del-día)
  - [Conceptos Clave](#conceptos-clave)
    - [¿Qué es una tabla en HTML?](#qué-es-una-tabla-en-html)
    - [Estructura básica de una tabla](#estructura-básica-de-una-tabla)
  - [Ejemplos Prácticos](#ejemplos-prácticos)
    - [Ejemplo 1: Horario simple](#ejemplo-1-horario-simple)
    - [Ejemplo 2: Tabla de enlaces útiles](#ejemplo-2-tabla-de-enlaces-útiles)
    - [Ejemplo 3: Tabla de datos personales](#ejemplo-3-tabla-de-datos-personales)
  - [Ejercicios del Día](#ejercicios-del-día)
    - [Ejercicio 1: Mi primera tabla ⭐](#ejercicio-1-mi-primera-tabla-)
    - [Ejercicio 2: Tabla de contactos con enlaces ⭐⭐](#ejercicio-2-tabla-de-contactos-con-enlaces-)
    - [Ejercicio 3: Integra una tabla en tu página ⭐⭐⭐](#ejercicio-3-integra-una-tabla-en-tu-página-)
  - [Buenas Prácticas](#buenas-prácticas)
  - [Resumen](#resumen)

---

## Descripción

Las tablas en HTML se utilizan para mostrar información de forma estructurada, organizada en filas y columnas. Son ideales para representar datos ordenados, horarios, resultados, catálogos y mucho más.

---

## Objetivos del Día

- Aprender a construir una tabla HTML simple usando `<table>`, `<tr>`, `<td>` y `<th>`
- Diferenciar entre celdas de encabezado y celdas de datos
- Ordenar información en filas y columnas de manera clara
- Integrar tablas sencillas en tus páginas web

---

## Conceptos Clave

### ¿Qué es una tabla en HTML?

Una **tabla** es una estructura compuesta por filas y columnas que almacenan datos. En HTML, las tablas se crean con la etiqueta `<table>` y se componen de varias etiquetas internas para sus diferentes partes.

---

### Estructura básica de una tabla

```html
<table> <tr> <th>Encabezado 1</th> <th>Encabezado 2</th> </tr> <tr> <td>Dato 1</td> <td>Dato 2</td> </tr> </table>
```

`<th>`: Celda de Encabezado
Se usa para los títulos o nombres de las columnas o filas.

El contenido suele aparecer en negrita y centrado.

Deben estar dentro de `<tr>`.

`<tr>`: Fila de una tabla
Significa "table row" (fila de tabla).

Cada `<tr>` representa una fila de la tabla y contiene celdas de datos (`<td>`) o encabezado (`<th>`).

`<td>`: Celda de dato
Significa "table data" (dato de tabla).

Representan los datos normales de la tabla, dentro de una fila.

## Ejemplos Prácticos

### Ejemplo 1: Horario simple

```html
<table border="1">
  <tr>
    <th>Hora</th>
    <th>Lunes</th>
    <th>Martes</th>
  </tr>
  <tr>
    <td>09:00</td>
    <td>Matemáticas</td>
    <td>Lengua</td>
  </tr>
  <tr>
    <td>10:00</td>
    <td>Inglés</td>
    <td>Ciencias</td>
  </tr>
</table>
```

### Ejemplo 2: Tabla de enlaces útiles
```html
<table border="1">
  <tr>
    <th>Recurso</th>
    <th>Enlace</th>
  </tr>
  <tr>
    <td>MDN Web Docs</td>
    <td><a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer">Visitar</a></td>
  </tr>
  <tr>
    <td>W3Schools</td>
    <td><a href="https://www.w3schools.com/" target="_blank" rel="noopener noreferrer">Visitar</a></td>
  </tr>
</table>
```

### Ejemplo 3: Tabla de datos personales

```html
<table border="1">
  <tr>
    <th>Nombre</th>
    <th>Email</th>
    <th>País</th>
  </tr>
  <tr>
    <td>Ana</td>
    <td>ana@correo.com</td>
    <td>España</td>
  </tr>
  <tr>
    <td>Luis</td>
    <td>luis@correo.com</td>
    <td>México</td>
  </tr>
</table>
```

Resultado:
<table border="1">
  <tr>
    <th>Nombre</th>
    <th>Email</th>
    <th>País</th>
  </tr>
  <tr>
    <td>Ana</td>
    <td>ana@correo.com</td>
    <td>España</td>
  </tr>
  <tr>
    <td>Luis</td>
    <td>luis@correo.com</td>
    <td>México</td>
  </tr>
</table>


## Ejercicios del Día

### Ejercicio 1: Mi primera tabla ⭐
Crea una tabla con dos columnas: "Asignatura" y "Nota". Añade al menos tres filas con nombres de asignaturas y tus notas.

### Ejercicio 2: Tabla de contactos con enlaces ⭐⭐
Crea una tabla con columnas para "Nombre", "Email" y "Enlace a perfil". Pon al menos dos contactos, usando un enlace ficticio para cada perfil.

### Ejercicio 3: Integra una tabla en tu página ⭐⭐⭐
Toma cualquier página creada en días anteriores e incluye una tabla significativa para tu contenido (por ejemplo, un horario, una lista de recursos, etc.).

## Buenas Prácticas

- Usa <th> para encabezados y <td> para datos.
- Mantén la coherencia en el número de columnas por fila.
- Añade bordes a las tablas para visualizarlas mejor durante el desarrollo.
- Usa indentación y saltos de línea para mejorar la legibilidad del código.
- Evita tablas para maquetar (solo para datos tabulares).

## Resumen

Las tablas sirven para organizar y mostrar información tabular. Aprendiste a usar las etiquetas `<table>`, `<tr>`, `<td>` y `<th>`, a estructurar datos y a incorporar tablas prácticas en tus páginas.