<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-05">Día 5</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-07">Día 7</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml6.png">
</h1>

# Día 6: Comentarios y Buenas Prácticas – Código limpio y mantenible

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

---

## Índice

- [Día 6: Comentarios y Buenas Prácticas – Código limpio y mantenible](#día-6-comentarios-y-buenas-prácticas--código-limpio-y-mantenible)
  - [Índice](#índice)
  - [Descripción](#descripción)
  - [Objetivos del Día](#objetivos-del-día)
  - [Conceptos Clave](#conceptos-clave)
    - [Comentarios en HTML](#comentarios-en-html)
    - [Cómo usar los comentarios:](#cómo-usar-los-comentarios)
  - [Buenas Prácticas de Código HTML](#buenas-prácticas-de-código-html)
    - [Ejemplo: Código desordenado vs limpio](#ejemplo-código-desordenado-vs-limpio)
  - [Ejercicios del Día](#ejercicios-del-día)
  - [Ejercicio 1: Ordena y comenta ⭐](#ejercicio-1-ordena-y-comenta-)
  - [Ejercicio 2: Proyecto pequeño con comentarios ⭐⭐](#ejercicio-2-proyecto-pequeño-con-comentarios-)
    - [Ejercicio 3: Checklist de buenas prácticas ⭐⭐⭐](#ejercicio-3-checklist-de-buenas-prácticas-)
  - [Buenas Prácticas Resumidas](#buenas-prácticas-resumidas)

---

## Descripción

Escribir código HTML funcional es solo una parte del desarrollo web. Tan importante como que funcione es que sea **comprensible, mantenible y fácil de modificar** para ti o cualquier otra persona que lo lea en el futuro. En este día aprenderás a incluir comentarios y a aplicar buenas prácticas para que tu HTML sea elegante, semántico y profesional.

---

## Objetivos del Día

- Documentar tu código usando comentarios en HTML
- Adoptar buenas prácticas visuales y semánticas
- Facilitar la lectura, mantenimiento y trabajo en equipo

---

## Conceptos Clave

### Comentarios en HTML

Los comentarios sirven para dejar notas, explicar secciones del código, desactivar fragmentos temporalmente o marcar “pendiente” (TODO). Lo que escribas entre los delimitadores de comentario **no aparece en el navegador**.

```html
<!-- Esto es un comentario en HTML --> <p>Contenido visible</p> 
``` 

### Cómo usar los comentarios:

- Para explicar partes complejas o poco evidentes
- Para dividir secciones largas del documento
- Para anotar pendientes o tareas futuras:

```html
<!-- TODO: Añadir sección de testimonios aquí -->
```

## Buenas Prácticas de Código HTML

1. Indplementación correcta y consistente
   - Usa espacios (preferiblemente 2 o 4) y mantén todo el código alineado para que la estructura sea clara.
```html
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
</ul>
```

2. Etiquetas siempre en minúsculas
    - Aunque no es obligatorio, usar minúsculas es estándar y evita errores.
```html
<title>Mi sitio web</title>
```

3. Cerrar todas las etiquetas (hasta donde corresponda)
   - No olvides cerrar elementos como `<li>`, `<p>`, `<html>`, `<body>`, etc.
<br>

4. Evita anidar mal etiquetas
    - Respeta el orden: cada etiqueta debe cerrarse después de su hija, no antes.
```html
<!-- Correcto -->
<p><strong>Importante:</strong> Este es el mensaje.</p>

<!-- Incorrecto -->
<p><strong>Importante:</p></strong>
```

5. Usa atributos descriptivos
    - Nombra las clases, IDs y textos alternativos de forma significativa.
```html
<img src="logo.png" alt="Logo de la empresa">
```

6. Comenta secciones clave
    - Especialmente en documentos grandes.
<br>

7. No abuses de los comentarios
   - Cuando todo está autoexplicado con HTML semántico, sobran aclaraciones.

### Ejemplo: Código desordenado vs limpio

- Código desordenado:
```html
<html>
<body>
<ul><li>Inicio<li>Contacto<li>Proyectos</ul>
<p>
Bienvenido!    Aprende HTML en 30 días.

<a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub</a>
</body>
</html>
```

- Código limpio y comentado
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Proyecto limpio</title>
</head>
<body>
  <!-- Menú de navegación principal -->
  <nav>
    <ul>
      <li>Inicio</li>
      <li>Contacto</li>
      <li>Proyectos</li>
    </ul>
  </nav>

  <!-- Mensaje de bienvenida -->
  <p>Bienvenido. Aprende HTML en 30 días.</p>
  
  <!-- Enlace externo a GitHub -->
  <a href="https://github.com/" target="_blank" rel="noopener noreferrer">GitHub</a>
</body>
</html>
```

## Ejercicios del Día

## Ejercicio 1: Ordena y comenta ⭐
Copia el siguiente código, endéntalo correctamente, ciérralo donde falte y agrega al menos dos comentarios útiles:
```html
<html>
<ul>
<li>Inicio
<li>Sobre mí
<li>Contacto
</ul>
<p>Bienvenido!</p>
</html>
```

## Ejercicio 2: Proyecto pequeño con comentarios ⭐⭐
Prepara un archivo HTML que tenga:
- Un título con <title>
- Un menú usando <ul> o <ol>
- Al menos un comentario identificando cada parte
- Una línea de contenido con tu nombre

### Ejercicio 3: Checklist de buenas prácticas ⭐⭐⭐
Haz una revisión de un archivo HTML antiguo que hayas hecho o toma uno de internet. Marca y corrige:
- Problemas de indentación
- Etiquetas sin cerrar
- Falta de comentarios útiles
- Anota antes/después en comentarios para practicar la autorreflexión.

## Buenas Prácticas Resumidas
- Mantén tu código ordenado, endentado y documentado
- Usa comentarios para ayudar (no para llenar el código)
- Escribe etiquetas, atributos y clases en minúscula
- No repitas código ni escribas cosas innecesarias
- Un código limpio inspira confianza y evita errores en equipo

<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-05">Día 5</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-07">Día 7</a>
</h4>
