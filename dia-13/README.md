<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-12">Día 12</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-14">Día 14</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml13.png">
</h1>

# Día 13: Estructura del DOM - Relaciones padre-hijo

![Nivel](https://img.shields.io/badge/nivel-intermedio-orange)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)


## Indice
* [Objetivo](#objetivo)
* [Qué es el DOM](#dom)
* [Estructura de árbol](#arbol)
* [Tipos de nodos](#nodos)
* [Relaciones jerárquicas](#relaciones)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)


## 📖 Descripción

El DOM (Document Object Model o Modelo de Objetos del Documento) es una representación estructurada de un documento HTML como un árbol jerárquico de nodos. Comprender cómo funciona el DOM es fundamental para entender cómo se organizan los elementos en una página web y cómo interactúan entre sí. En este día aprenderás sobre la estructura de árbol del DOM, los diferentes tipos de nodos, y las relaciones padre-hijo-hermano que existen entre los elementos HTML.

Aunque en este momento no trabajarás directamente con JavaScript, entender el DOM te preparará para cuando necesites manipular elementos dinámicamente y te ayudará a escribir HTML más estructurado y lógico.

<a name="objetivo"></a>

## 🎯 Objetivos del Día

Al acabar este día podrás:

- Entender qué es el DOM y por qué es importante
- Visualizar documentos HTML como árboles jerárquicos
- Identificar los diferentes tipos de nodos en el DOM
- Comprender las relaciones padre, hijo, hermano y descendiente
- Analizar la jerarquía de elementos en tus propios documentos HTML
- Escribir HTML más estructurado pensando en su representación en el DOM

## 📚 Conceptos Clave

### Introducción al Document Object Model

<a name="dom"></a>

## ¿Qué es el DOM?

El DOM (Document Object Model) es una interfaz de programación que representa un documento HTML o XML como una estructura de árbol. Cada elemento, atributo y texto del documento se convierte en un objeto (nodo) que puede ser accedido y manipulado.

**Características principales del DOM:**

- Es una representación estructurada del documento en forma de árbol
- Cada elemento HTML es un nodo en el árbol
- Define las relaciones jerárquicas entre elementos
- Permite que lenguajes como JavaScript accedan y modifiquen el contenido, estructura y estilos
- Es independiente del lenguaje de programación

**¿Por qué es importante?**

- Te ayuda a entender cómo se organizan los elementos en una página
- Es fundamental para trabajar con JavaScript y manipular páginas dinámicamente
- Facilita la comprensión de CSS y cómo se aplican los estilos
- Te permite planificar mejor la estructura de tus documentos HTML

<a name="arbol"></a>

## Estructura de árbol del DOM

El DOM representa un documento HTML como un árbol invertido, donde:

- La raíz del árbol es el nodo `document`
- Cada etiqueta HTML es un nodo de elemento
- El texto dentro de las etiquetas son nodos de texto
- Cada nodo puede tener nodos hijos

### Ejemplo visual de árbol DOM

Dado este HTML simple:

```

<!DOCTYPE html>
<html>
  <head>
    <title>Mi Página</title>
  </head>
  <body>
    <h1>Título</h1>
    <p>Un párrafo de texto.</p>
  </body>
</html>
```

**Se representa como árbol así:**

```

document
└── html
├── head
│   └── title
│       └── "Mi Página" (texto)
└── body
├── h1
│   └── "Título" (texto)
└── p
└── "Un párrafo de texto." (texto)

```

**Explicación:**

1. `document` es el nodo raíz
2. `html` es el primer elemento hijo
3. `head` y `body` son hijos de `html`
4. `title` es hijo de `head`
5. El texto dentro de cada elemento también es un nodo

<a name="nodos"></a>

## Tipos de nodos

En el DOM existen varios tipos de nodos, aunque los más importantes son:

### 1. Nodo Document

El nodo raíz que representa todo el documento. Es el punto de entrada al DOM.

```

document (el documento completo)

```

### 2. Nodos de Elemento (Element Nodes)

Representan las etiquetas HTML. Son los bloques de construcción del árbol.

```

<div>    ← Nodo de elemento
<p>      ← Nodo de elemento
<img>    ← Nodo de elemento

```

### 3. Nodos de Texto (Text Nodes)

Contienen el texto dentro de los elementos. Siempre son hijos de nodos de elemento.

```

<p>Este es un texto</p>
└─────────────┘
Nodo de texto

```

**Importante:** Los espacios en blanco y saltos de línea también son nodos de texto en el DOM.

### 4. Nodos de Atributo (Attribute Nodes)

Representan los atributos de los elementos (aunque técnicamente no son parte del árbol como tal).

```

<img src="foto.jpg" alt="Foto">
     └── atributos
    ```

### 5. Nodos de Comentario (Comment Nodes)

Los comentarios HTML también son nodos en el DOM.

```

<!-- Este es un comentario -->
```

<a name="relaciones"></a>

## Relaciones jerárquicas en el DOM

Los nodos en el DOM tienen relaciones similares a un árbol genealógico.

### Nodo Padre (Parent Node)

Un nodo que contiene directamente a otro nodo.

```

<div>           ← Padre
  <p>Texto</p>  ← Hijo
</div>
```

En este ejemplo, `<div>` es el padre de `<p>`.

### Nodo Hijo (Child Node)

Un nodo que está contenido directamente dentro de otro nodo.

```

<ul>                    ← Padre
  <li>Item 1</li>       ← Hijo
  <li>Item 2</li>       ← Hijo
  <li>Item 3</li>       ← Hijo
</ul>
```

Los tres `<li>` son hijos directos de `<ul>`.

### Nodos Hermanos (Sibling Nodes)

Nodos que comparten el mismo padre y están al mismo nivel en la jerarquía.

```

<div>
  <h1>Título</h1>    ← Hermano de p
  <p>Párrafo</p>     ← Hermano de h1
</div>
```

`<h1>` y `<p>` son hermanos porque ambos son hijos directos de `<div>`.

**Tipos de hermanos:**

- **Hermano anterior (Previous Sibling):** El nodo que está antes en el orden
- **Hermano siguiente (Next Sibling):** El nodo que está después en el orden

### Nodo Descendiente (Descendant Node)

Un nodo que está dentro de otro nodo, directa o indirectamente (hijo, nieto, bisnieto, etc.).

```

<div>                      ← Ancestro
  <section>                ← Hijo y descendiente
    <article>              ← Nieto y descendiente
      <p>Texto</p>         ← Bisnieto y descendiente
    </article>
  </section>
</div>
```

Todos los elementos dentro de `<div>` son descendientes de `<div>`.

### Nodo Ancestro (Ancestor Node)

Un nodo que contiene a otro nodo, directa o indirectamente (padre, abuelo, bisabuelo, etc.).

```

<html>                   ← Ancestro de todos
  <body>                 ← Ancestro de div, p
    <div>                ← Ancestro de p
      <p>Texto</p>       ← Descendiente de todos
    </div>
  </body>
</html>
```

`<html>`, `<body>` y `<div>` son ancestros de `<p>`.

### Visualización completa de relaciones

```

<div id="contenedor">
  <h2>Título</h2>
  <p>Primer párrafo</p>
  <p>Segundo párrafo</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
</div>
```

**Relaciones:**

- `<div>` es el **padre** de `<h2>`, `<p>` (ambos) y `<ul>`
- `<h2>`, los dos `<p>` y `<ul>` son **hijos** de `<div>`
- `<h2>`, los dos `<p>` y `<ul>` son **hermanos** entre sí
- `<ul>` es el **padre** de los dos `<li>`
- Los dos `<li>` son **hijos** de `<ul>` y **hermanos** entre sí
- Los dos `<li>` son **descendientes** de `<div>` (pero no hijos directos)
- `<div>` es **ancestro** de todos los elementos dentro de él

<a name="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Árbol DOM simple

**HTML:**
```

<html>
  <body>
    <h1>Bienvenido</h1>
    <p>Este es mi sitio web.</p>
  </body>
</html>
```

**Representación en árbol:**
```

document
└── html
└── body
├── h1
│   └── "Bienvenido"
└── p
└── "Este es mi sitio web."

```

**Análisis de relaciones:**
- `html` es padre de `body`
- `body` es padre de `h1` y `p`
- `h1` y `p` son hermanos
- El texto "Bienvenido" es hijo de `h1`

### Ejemplo 2: Estructura con lista

**HTML:**
```

<div class="contenedor">
  <h2>Mis tareas</h2>
  <ul>
    <li>Estudiar HTML</li>
    <li>Practicar ejercicios</li>
    <li>Hacer proyecto</li>
  </ul>
</div>
```

**Representación en árbol:**
```

div.contenedor
├── h2
│   └── "Mis tareas"
└── ul
├── li
│   └── "Estudiar HTML"
├── li
│   └── "Practicar ejercicios"
└── li
└── "Hacer proyecto"

```

**Análisis de relaciones:**
- `div` es padre de `h2` y `ul`
- `h2` y `ul` son hermanos
- `ul` es padre de los tres `li`
- Los tres `li` son hermanos entre sí
- Los tres `li` son descendientes de `div` (pero no hijos directos)

### Ejemplo 3: Estructura anidada compleja

**HTML:**
```

<article>
  <header>
    <h1>Título del artículo</h1>
    <p>Por Autor</p>
  </header>
  <section>
    <h2>Introducción</h2>
    <p>Este es el primer párrafo.</p>
    <p>Este es el segundo párrafo.</p>
  </section>
  <footer>
    <p>Publicado el 24/11/2025</p>
  </footer>
</article>
```

**Representación en árbol:**
```

article
├── header
│   ├── h1
│   │   └── "Título del artículo"
│   └── p
│       └── "Por Autor"
├── section
│   ├── h2
│   │   └── "Introducción"
│   ├── p
│   │   └── "Este es el primer párrafo."
│   └── p
│       └── "Este es el segundo párrafo."
└── footer
└── p
└── "Publicado el 24/11/2025"

```

**Análisis de relaciones:**
- `article` es el ancestro de todos los elementos
- `header`, `section` y `footer` son hijos de `article` y hermanos entre sí
- `h1` y `p` dentro de `header` son hermanos
- Los dos `p` dentro de `section` son hermanos
- Todos los elementos `p` son descendientes de `article`

### Ejemplo 4: Formulario con estructura DOM

**HTML:**
```

<form>
  <div class="campo">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre">
  </div>
  <div class="campo">
    <label for="email">Email:</label>
    <input type="email" id="email">
  </div>
  <button type="submit">Enviar</button>
</form>
```

**Representación en árbol:**
```

form
├── div.campo
│   ├── label
│   │   └── "Nombre:"
│   └── input
├── div.campo
│   ├── label
│   │   └── "Email:"
│   └── input
└── button
└── "Enviar"

```

**Análisis de relaciones:**
- `form` es padre de los dos `div` y del `button`
- Los dos `div.campo` son hermanos entre sí
- Dentro de cada `div`, `label` e `input` son hermanos
- Todos los `input` y `label` son descendientes de `form`

### Ejemplo 5: Tabla con estructura DOM

**HTML:**
```

<table>
  <thead>
    <tr>
      <th>Nombre</th>
      <th>Edad</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Juan</td>
      <td>25</td>
    </tr>
    <tr>
      <td>María</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
```

**Representación en árbol:**
```

table
├── thead
│   └── tr
│       ├── th
│       │   └── "Nombre"
│       └── th
│           └── "Edad"
└── tbody
├── tr
│   ├── td
│   │   └── "Juan"
│   └── td
│       └── "25"
└── tr
├── td
│   └── "María"
└── td
└── "30"

```

**Análisis de relaciones:**
- `table` es padre de `thead` y `tbody`
- `thead` y `tbody` son hermanos
- Cada `tr` es padre de sus `th` o `td`
- Los dos `th` del `thead` son hermanos
- Los `tr` dentro de `tbody` son hermanos
- Todos los `td` son descendientes de `table`

<a name="ejercicio"></a>

## ✏️ Ejercicios del Día


### Ejercicio 1: Dibujar árbol DOM básico ⭐
Crea un documento HTML con la siguiente estructura: un `div` que contenga un `h2` con el texto "Mi perfil", un `p` con tu descripción, y una imagen. Luego dibuja (en papel o comentario HTML) el árbol DOM mostrando todas las relaciones padre-hijo.

[Solución](ejercicio1.html)

### Ejercicio 2: Identificar relaciones ⭐⭐
Crea un documento HTML con una estructura de navegación (`nav`) que contenga una lista desordenada (`ul`) con 4 enlaces (`a`) dentro de elementos de lista (`li`). Debajo añade una sección (`section`) con un título (`h2`) y dos párrafos (`p`). En comentarios HTML, identifica: (1) todos los nodos padre, (2) todos los pares de hermanos, (3) al menos 3 relaciones descendiente-ancestro.

[Solución](ejercicio2.html)

### Ejercicio 3: Estructura compleja con análisis completo ⭐⭐⭐
Crea un documento HTML completo que represente una tarjeta de producto con la siguiente estructura: un `article` como contenedor principal, dentro un `header` con el nombre del producto (`h3`) y su precio (`span` con clase "precio"), luego un `div` con clase "contenido" que contenga una imagen del producto y una descripción (`p`) con al menos dos oraciones donde una palabra esté resaltada con `span`, después un `div` con clase "caracteristicas" que contenga una lista desordenada con 3 características, y finalmente un `footer` con un botón "Comprar" y un enlace "Ver más". Una vez creado el HTML, añade al final un comentario extenso donde: (1) dibujes el árbol DOM completo, (2) identifiques todos los hermanos, (3) menciones todos los descendientes del `article`, (4) expliques la diferencia entre hijos y descendientes usando ejemplos de tu código.

[Solución](ejercicio3.html)

## 🔍 Buenas Prácticas

- Visualiza mentalmente el árbol DOM mientras escribes HTML para mantener una estructura lógica.
- Mantén la jerarquía de elementos lo más simple posible; evita anidaciones innecesarias.
- Usa indentación consistente en tu código HTML para reflejar visualmente la estructura del DOM.
- Agrupa elementos relacionados bajo un padre común para facilitar el estilizado con CSS.
- Recuerda que los espacios en blanco y saltos de línea también crean nodos de texto en el DOM.
- Piensa en la estructura del DOM antes de escribir código, planifica la jerarquía.
- Usa elementos semánticos (`header`, `nav`, `section`, `article`) para crear árboles DOM más significativos.
- Considera cómo será la navegación entre nodos cuando uses JavaScript en el futuro.
- Los comentarios HTML pueden ayudarte a documentar estructuras DOM complejas.
- Una buena estructura DOM facilita tanto el CSS como el JavaScript posterior.
- Usa herramientas de desarrollo del navegador (F12) para visualizar el árbol DOM de tus páginas.


<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-12">Día 12</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-14">Día 14</a>
</h4>
