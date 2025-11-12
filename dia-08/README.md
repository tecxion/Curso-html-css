<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-07">Día 7</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-09">Día 9</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml8.png">
</h1>

# Día 8: Tablas Avanzadas - `colspan`, `rowspan`, `<thead>`, `<tbody>`, `<tfoot>`, accesibilidad

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1.5%20horas-blue)


## Indice

- [Día 8: Tablas Avanzadas - `colspan`, `rowspan`, `<thead>`, `<tbody>`, `<tfoot>`, accesibilidad](#día-8-tablas-avanzadas---colspan-rowspan-thead-tbody-tfoot-accesibilidad)
  - [Indice](#indice)
  - [📖 Descripción](#-descripción)
  - [🎯 Objetivos del Día](#-objetivos-del-día)
  - [📚 Conceptos Clave](#-conceptos-clave)
    - [Combinación de celdas con colspan y rowspan](#combinación-de-celdas-con-colspan-y-rowspan)
    - [Atributo colspan](#atributo-colspan)
    - [Atributo rowspan](#atributo-rowspan)
    - [Combinando colspan y rowspan](#combinando-colspan-y-rowspan)
  - [Estructura semántica de tablas](#estructura-semántica-de-tablas)
    - [`<thead>` - Encabezado de tabla](#thead---encabezado-de-tabla)
    - [`<tbody>` - Cuerpo de tabla](#tbody---cuerpo-de-tabla)
    - [`<tfoot>` - Pie de tabla](#tfoot---pie-de-tabla)
  - [Accesibilidad en tablas](#accesibilidad-en-tablas)
    - [Atributo scope](#atributo-scope)
    - [Atributos headers e id](#atributos-headers-e-id)
    - [Elemento `<caption>`](#elemento-caption)
  - [💻 Ejemplos Prácticos](#-ejemplos-prácticos)
  - [✏️ Ejercicios del Día](#️-ejercicios-del-día)
  - [🔍 Buenas Prácticas](#-buenas-prácticas)


## 📖 Descripción

Las tablas HTML pueden ser mucho más que simples cuadrículas de datos. Con técnicas avanzadas puedes crear estructuras complejas que se adapten a necesidades específicas de presentación de información. En este día aprenderás a usar `colspan` y `rowspan` para crear celdas que abarquen múltiples columnas o filas, a estructurar tablas con `<thead>`, `<tbody>` y `<tfoot>`, y a implementar prácticas de accesibilidad esenciales.

Las tablas avanzadas son fundamentales para presentar datos complejos de forma clara y organizada, manteniendo siempre la accesibilidad para todos los usuarios.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Utilizar `colspan` para combinar celdas horizontalmente
- Aplicar `rowspan` para combinar celdas verticalmente
- Estructurar tablas con `<thead>`, `<tbody>` y `<tfoot>`
- Implementar atributos de accesibilidad como `scope` y `headers`
- Crear tablas complejas y accesibles

## 📚 Conceptos Clave

### Combinación de celdas con colspan y rowspan

Los atributos `colspan` y `rowspan` permiten que una celda ocupe el espacio de múltiples columnas o filas respectivamente.

<a name="colrowspan"></a>

### Atributo colspan

El atributo `colspan` (column span) extiende una celda horizontalmente para abarcar varias columnas. Acepta un valor numérico que indica cuántas columnas ocupará.

<table> <tr> <th colspan="2">Datos del Estudiante</th> </tr> <tr> <td>Nombre</td> <td>Juan Pérez</td> </tr> </table> ```

- En este ejemplo, la celda de encabezado abarca 2 columnas completas.

### Atributo rowspan

- El atributo rowspan (row span) extiende una celda verticalmente para abarcar varias filas. También acepta un valor numérico.

```html
<table>
  <tr>
    <th rowspan="2">País</th>
    <th>Población</th>
  </tr>
  <tr>
    <td>45 millones</td>
  </tr>
</table>
```

- Visualización en la web:

<table>
  <tr>
    <th rowspan="2">País</th>
    <th>Población</th>
  </tr>
  <tr>
    <td>45 millones</td>
  </tr>
</table>

- Aquí, la celda "País" ocupa 2 filas verticalmente.

### Combinando colspan y rowspan
Puedes combinar ambos atributos en la misma celda para crear estructuras más complejas:

```html
<td colspan="2" rowspan="3">Celda grande</td>
``` 

## Estructura semántica de tablas

HTML proporciona elementos específicos para organizar el contenido de las tablas en secciones lógicas.

### `<thead>` - Encabezado de tabla

Agrupa las filas de encabezado de la tabla. Suele contener los títulos de las columnas.

```html
<thead>
  <tr>
    <th>Producto</th>
    <th>Precio</th>
  </tr>
</thead>
```

### `<tbody>` - Cuerpo de tabla

Contiene las filas principales con los datos de la tabla.

```html
<tbody>
  <tr>
    <td>Laptop</td>
    <td>$800</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>$20</td>
  </tr>
</tbody>
```

### `<tfoot>` - Pie de tabla

Agrupa las filas de resumen o totales. Útil para mostrar sumas, promedios o notas al pie.

```html
<tfoot>
  <tr>
    <td>Total</td>
    <td>$820</td>
  </tr>
</tfoot>
```

*Nota importante:* El orden recomendado en el código HTML es `<thead>`, `<tfoot>`, `<tbody>`, aunque visualmente el `<tfoot>` se mostrará al final de la tabla.

## Accesibilidad en tablas

La accesibilidad es crucial para que todos los usuarios, incluidos aquellos que usan lectores de pantalla, puedan entender el contenido de las tablas.

### Atributo scope
El atributo scope en elementos `<th>` indica si el encabezado se refiere a una columna, fila o grupo de columnas/filas.

- Valores posibles:
    - col: Encabezado de columna
    - row: Encabezado de fila
    - colgroup: Encabezado de grupo de columnas
    - rowgroup: Encabezado de grupo de filas

```html
<th scope="col">Mes</th>
<th scope="row">Enero</th>
```

### Atributos headers e id

Para tablas complejas, usa id en los encabezados y headers en las celdas de datos para establecer relaciones explícitas.

```html
<th id="producto">Producto</th>
<th id="precio">Precio</th>
<td headers="producto">Laptop</td>
<td headers="precio">$800</td>
```

### Elemento `<caption>`

Proporciona un título descriptivo para la tabla:
```html
<table>
  <caption>Ventas del primer trimestre 2025</caption>
  <!-- contenido de la tabla -->
</table>
``` 

## 💻 Ejemplos Prácticos

- Ejemplo 1: Tabla con colspan

```html
<table border="1">
  <thead>
    <tr>
      <th colspan="3">Información de Contacto</th>
    </tr>
    <tr>
      <th>Nombre</th>
      <th>Email</th>
      <th>Teléfono</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ana García</td>
      <td>ana@email.com</td>
      <td>555-1234</td>
    </tr>
  </tbody>
</table>
```

- Vista de la web:
<table border="1">
  <thead>
    <tr>
      <th colspan="3">Información de Contacto</th>
    </tr>
    <tr>
      <th>Nombre</th>
      <th>Email</th>
      <th>Teléfono</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ana García</td>
      <td>ana@email.com</td>
      <td>555-1234</td>
    </tr>
  </tbody>
</table>

- Ejemplo 2: Tabla con rowspan.

```html
<table border="1">
  <tr>
    <th rowspan="3">Lunes</th>
    <td>9:00 - Matemáticas</td>
  </tr>
  <tr>
    <td>10:00 - Historia</td>
  </tr>
  <tr>
    <td>11:00 - Inglés</td>
  </tr>
</table>
```

Vista de la web:
<table border="1">
  <tr>
    <th rowspan="3">Lunes</th>
    <td>9:00 - Matemáticas</td>
  </tr>
  <tr>
    <td>10:00 - Historia</td>
  </tr>
  <tr>
    <td>11:00 - Inglés</td>
  </tr>
</table>

- Ejemplo 3: Tabla completa con estructura y accesibilidad

```html
<table border="1">
  <caption>Ventas Mensuales 2025</caption>
  <thead>
    <tr>
      <th scope="col">Mes</th>
      <th scope="col">Ventas</th>
      <th scope="col">% Crecimiento</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Enero</th>
      <td>$50,000</td>
      <td>5%</td>
    </tr>
    <tr>
      <th scope="row">Febrero</th>
      <td>$55,000</td>
      <td>10%</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Total</th>
      <td>$105,000</td>
      <td>7.5%</td>
    </tr>
  </tfoot>
</table>
```

Vista en la web:
<table border="1">
  <caption>Ventas Mensuales 2025</caption>
  <thead>
    <tr>
      <th scope="col">Mes</th>
      <th scope="col">Ventas</th>
      <th scope="col">% Crecimiento</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Enero</th>
      <td>$50,000</td>
      <td>5%</td>
    </tr>
    <tr>
      <th scope="row">Febrero</th>
      <td>$55,000</td>
      <td>10%</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Total</th>
      <td>$105,000</td>
      <td>7.5%</td>
    </tr>
  </tfoot>
</table>

## ✏️ Ejercicios del Día

- Ejercicio 1: Tabla con colspan y rowspan ⭐
Crea una tabla de horario escolar que use colspan para el título principal y rowspan para los días de la semana. Debe tener al menos 3 días y 4 horas diferentes.

[Solución](ejercicio1.html)

- Ejercicio 2: Tabla estructurada con thead, tbody y tfoot ⭐⭐
Crea una tabla de factura que incluya `<thead>` con encabezados, `<tbody>` con productos y precios, y `<tfoot>` con el subtotal, IVA y total. Usa al menos 4 productos diferentes.

[Solución](ejercicio2.html)

- Ejercicio 3: Tabla accesible completa ⭐⭐⭐
Crea una tabla compleja que combine colspan, rowspan, estructura semántica (`<thead>, <tbody>, <tfoot>`) y atributos de accesibilidad (scope, caption). Ejemplo: tabla de resultados deportivos con equipos, partidos jugados, ganados, perdidos y puntos.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas
- Usa <thead>, <tbody> y <tfoot> para estructurar tablas complejas semánticamente.
- Añade siempre <caption> o aria-label para describir el propósito de la tabla.
- Utiliza el atributo scope en todos los encabezados <th> para mejorar accesibilidad.
- Para tablas muy complejas, usa headers e id para establecer relaciones explícitas.
- Verifica que colspan y rowspan no rompan la estructura lógica de la tabla.
- Evita tablas excesivamente complejas; considera dividirlas en tablas más simples.
- Usa CSS para el estilo visual; las tablas deben usarse solo para datos tabulares.
- Asegúrate de que las tablas sean responsivas y no causen scroll horizontal excesivo.
- Prueba tus tablas con lectores de pantalla para verificar la accesibilidad.

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-07">Día 7</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-09">Día 9</a>
</h4>