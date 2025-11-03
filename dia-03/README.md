<h4 align="center">
<a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-02">Día 2</a> || <a href="https://github.com/tecxion/Curso-html-css">Inicio</a> || <a href="https://github.com/tecxion/Curso-html-css/tree/main/dia-04">Día 4</a>
</h4>
<h1 align="center">
<img src="https://github.com/tecxion/Curso-html-css/blob/main/recursos/imagenes/CURSOhtml3.png">
</h1>

# Día 3: Enlaces e Hipervínculos

![Nivel](https://img.shields.io/badge/nivel-principiante-green)
![Tiempo](https://img.shields.io/badge/tiempo-1%20hora-blue)

### Índice del Día
* [Objetivo](#objetivo)
* [Concepto](#concepto)
* [Ejemplos](#ejemplo)
* [Ejercicios](#ejercicio)

## 📖 Descripción

Los enlaces son la esencia de la World Wide Web, permitiendo la navegación entre páginas y sitios web. La etiqueta `<a>` (anchor) es uno de los elementos más fundamentales de HTML, creando hipervínculos que conectan documentos y recursos.

En este día aprenderás a crear diferentes tipos de enlaces, comprenderás la diferencia entre URLs absolutas y relativas, y dominarás los atributos esenciales que hacen que los enlaces sean funcionales y accesibles.

<a name="objetivo"></a>


## 🎯 Objetivos del Día

Al finalizar este día serás capaz de:
- Crear enlaces básicos con la etiqueta `<a>` y el atributo `href`
- Diferenciar entre URLs absolutas y relativas
- Utilizar atributos como `target`, `title` y `rel`
- Crear enlaces internos dentro de la misma página
- Implementar enlaces de correo electrónico y teléfono
- Aplicar buenas prácticas de accesibilidad en enlaces


<a name="concepto"></a>


## 📚 Conceptos Clave

### La Etiqueta Anchor `<a>`

La etiqueta `<a>` crea hipervínculos que permiten a los usuarios navegar entre páginas. La sintaxis básica es:

```html
<a href="URL">Texto del enlace</a>
```

El atributo `href` (Hypertext Reference) es el más importante y **obligatorio** para que el enlace funcion. El texto entre las etiquetas de apertura y cierre es lo que el usuario ve y hace clic.

### URLs Absolutas vs Relativas

#### URLs Absolutas

Una **URL absoluta** contiene la dirección completa del recurso, incluyendo el protocolo (http/https) y el dominio:

```html
<a href="https://www.ejemplo.com/pagina.html">Enlace externo</a>
```

**Características**:
- Incluyen el protocolo completo (https://)
- Contienen el nombre del dominio
- Son necesarias para enlaces a sitios externos
- Funcionan independientemente de dónde esté el archivo

#### URLs Relativas

Una **URL relativa** especifica la ruta del recurso en relación con la ubicación actual:
```html
<!-- Archivo en la misma carpeta -->
<a href="pagina.html">Enlace local</a>

<!-- Archivo en subcarpeta -->
<a href="carpeta/pagina.html">Enlace en subcarpeta</a>

<!-- Archivo en carpeta padre -->
<a href="../pagina.html">Subir un nivel</a>

<!-- Archivo desde la raíz del sitio -->
<a href="/carpeta/pagina.html">Desde la raíz</a>
```


**Ventajas de URLs relativas**:
- Más cortas y fáciles de escribir
- Funcionan en desarrollo local y producción
- Facilitan mover el sitio completo
- Ideales para navegación interna

### Atributos Importantes del Enlace

#### Atributo `target`

El atributo `target` especifica dónde abrir el documento vinculado:

```html
<!-- Abre en la misma pestaña (por defecto) -->
<a href="https://ejemplo.com">Misma pestaña</a>

<!-- Abre en nueva pestaña -->
<a href="https://ejemplo.com" target="_blank">Nueva pestaña</a>

<!-- Otros valores -->
<a href="pagina.html" target="_self">Mismo marco (_self)</a>
<a href="pagina.html" target="_parent">Marco padre (_parent)</a>
<a href="pagina.html" target="_top">Ventana completa (_top)</a>
```


**Cuándo usar `target="_blank"`**:
- Enlaces a sitios externos para mantener al usuario en tu página
- Documentos PDF o archivos descargables
- Herramientas o recursos que el usuario necesitará consultar mientras navega

**Importante**: Cuando uses `target="_blank"`, siempre incluye `rel="noopener noreferrer"` por seguridad:

```html
<a href="https://ejemplo.com" target="_blank" rel="noopener noreferrer"> Enlace seguro externo </a> ```
```

#### Atributo title
Proporciona información adicional que aparece como tooltip al pasar el mouse

```html
<a href="https://ejemplo.com" title="Visita nuestro sitio web oficial">
  Ir al sitio
</a>
```

#### Atributo rel
Define la relación entre el documento actual y el vinculado

```html
<!-- Para enlaces externos -->
<a href="https://ejemplo.com" rel="nofollow">Enlace sin seguimiento</a>

<!-- Para enlaces patrocinados -->
<a href="https://sponsor.com" rel="sponsored">Enlace patrocinado</a>

<!-- Para contenido generado por usuarios -->
<a href="https://ugc.com" rel="ugc">Contenido de usuario</a>
```

### Enlaces Especiales

#### Enlaces de Correo Electrónico

```html
<a href="mailto:contacto@ejemplo.com">Enviar correo</a>

<!-- Con asunto y cuerpo predefinidos -->
<a href="mailto:contacto@ejemplo.com?subject=Consulta&body=Hola">
  Enviar consulta
</a>
```

#### Enlaces de Teléfono
```html
<a href="tel:+34123456789">Llamar ahora</a>
```

#### Enlaces de Whatsapp

```html
<a href="https://wa.me/34123456789">Chatear por WhatsApp</a>
```

<a name ="ejemplo"></a>

## 💻 Ejemplos Prácticos

### Ejemplo 1: Navegación Básica

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Navegación Básica</title>
</head>
<body>
    <h1>Mi Sitio Web</h1>
    
    <!-- Enlaces relativos internos -->
    <nav>
        <a href="index.html">Inicio</a> |
        <a href="sobre-mi.html">Sobre mí</a> |
        <a href="proyectos.html">Proyectos</a> |
        <a href="contacto.html">Contacto</a>
    </nav>
    
    <h2>Enlaces Externos</h2>
    
    <!-- Enlaces absolutos a sitios externos -->
    <p>
        Recursos útiles:
        <a href="https://developer.mozilla.org" target="_blank" rel="noopener noreferrer">
          MDN Web Docs
        </a> |
        <a href="https://www.w3schools.com" target="_blank" rel="noopener noreferrer">
          W3Schools
        </a>
    </p>
</body>
</html>
```

- Explicación: Muestra la diferencia entre enlaces internos (relativos) para navegación del sitio y enlaces externos (absolutos) que abren en nueva pestaña

### Ejemplo 2: Enlaces Internos con Anclas

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Índice de Contenidos</title>
</head>
<body>
    <h1>Artículo Largo</h1>
    
    <!-- Índice con enlaces internos -->
    <nav>
        <h2>Índice</h2>
        <ul>
            <li><a href="#introduccion">Introducción</a></li>
            <li><a href="#desarrollo">Desarrollo</a></li>
            <li><a href="#conclusiones">Conclusiones</a></li>
            <li><a href="#referencias">Referencias</a></li>
        </ul>
    </nav>
    
    <hr>
    
    <!-- Secciones con IDs -->
    <section id="introduccion">
        <h2>Introducción</h2>
        <p>Contenido de la introducción...</p>
        <a href="#" title="Volver arriba">↑ Ir arriba</a>
    </section>
    
    <section id="desarrollo">
        <h2>Desarrollo</h2>
        <p>Contenido del desarrollo...</p>
        <a href="#" title="Volver arriba">↑ Ir arriba</a>
    </section>
    
    <section id="conclusiones">
        <h2>Conclusiones</h2>
        <p>Contenido de las conclusiones...</p>
        <a href="#" title="Volver arriba">↑ Ir arriba</a>
    </section>
    
    <section id="referencias">
        <h2>Referencias</h2>
        <p>Lista de referencias...</p>
        <a href="#" title="Volver arriba">↑ Ir arriba</a>
    </section>
</body>
</html>
```

- Explicación: Demuestra cómo crear un índice navegable dentro de la misma página usando IDs y el símbolo #

### Ejemplo 3: Enlaces de Contacto

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Contacto</title>
</head>
<body>
    <h1>Contáctanos</h1>
    
    <h2>Información de Contacto</h2>
    
    <!-- Enlace de correo electrónico -->
    <p>
        <strong>Email:</strong> 
        <a href="mailto:info@ejemplo.com" title="Enviar correo electrónico">
          info@ejemplo.com
        </a>
    </p>
    
    <!-- Enlace de correo con asunto y cuerpo -->
    <p>
        <a href="mailto:ventas@ejemplo.com?subject=Consulta%20sobre%20productos&body=Hola,%20quisiera%20información%20sobre...">
          Enviar consulta de ventas
        </a>
    </p>
    
    <!-- Enlace de teléfono -->
    <p>
        <strong>Teléfono:</strong> 
        <a href="tel:+34912345678" title="Llamar por teléfono">
          +34 912 345 678
        </a>
    </p>
    
    <!-- Enlace de WhatsApp -->
    <p>
        <strong>WhatsApp:</strong> 
        <a href="https://wa.me/34912345678?text=Hola,%20tengo%20una%20consulta" 
           target="_blank" 
           rel="noopener noreferrer"
           title="Abrir chat de WhatsApp">
          Chatear por WhatsApp
        </a>
    </p>
    
    <!-- Redes sociales -->
    <h3>Síguenos en Redes Sociales</h3>
    <p>
        <a href="https://twitter.com/ejemplo" target="_blank" rel="noopener noreferrer">
          Twitter
        </a> |
        <a href="https://facebook.com/ejemplo" target="_blank" rel="noopener noreferrer">
          Facebook
        </a> |
        <a href="https://instagram.com/ejemplo" target="_blank" rel="noopener noreferrer">
          Instagram
        </a>
    </p>
</body>
</html>
```

- Explicación: Muestra diferentes tipos de enlaces de contacto incluyendo email, teléfono y WhatsApp.


<a name="ejercicio"></a>

## ✏️ Ejercicios del Día

### Ejercicio 1: Página de Navegación ⭐. [Solución](ejercicio1.html)

Objetivo: Crear una página con menú de navegación usando enlaces relativos.

Instrucciones:
- Crea un archivo index.html con un menú de navegación
- Añade enlaces a: Inicio, Servicios, Sobre Nosotros, Contacto
- Usa URLs relativas para simular la estructura
- Añade un enlace externo a tu red social favorita con target="_blank"
- Incluye el atributo title en todos los enlaces
- Pista: Los enlaces pueden apuntar a archivos que aún no existen; lo importante es practicar la sintaxis correcta.

### Ejercicio 2: Página de Artículo con Índice ⭐⭐ [Solución](ejercicio2.html)

Objetivo: Crear un artículo largo con índice navegable y enlaces internos.

Requisitos:
- Título principal del artículo
- Índice al inicio con enlaces internos a 5 secciones
- 5 secciones con IDs únicos
- Enlaces "volver arriba" en cada sección
- Al menos 2 enlaces externos relevantes al contenido
- Enlaces de correo en la sección de contacto

### Ejecicio 3: Página de Portfolio ⭐⭐⭐ [Solución](ejercicio3.html)

Objetivo: Crear una página completa de portfolio personal con diversos tipos de enlaces.

Instrucciones:
- Crea una estructura de navegación principal
- Incluye una sección "Sobre mí" con enlaces a redes sociales
- Sección "Proyectos" con enlaces externos a GitHub u otros proyectos
- Sección "Habilidades" con enlaces a recursos de aprendizaje
- Sección "Contacto" con:
- Enlace de email con asunto predefinido
- Enlace de teléfono
- Enlaces a redes sociales profesionales (LinkedIn, GitHub)
- Usa correctamente target, rel, y title en todos los enlaces
- Implementa navegación interna con anclas

## 🔍 Buenas Prácticas
✅ Usa texto descriptivo en los enlaces, no "haz clic aquí"<br>
✅ Añade rel="noopener noreferrer" cuando uses target="_blank"<br>
✅ Usa URLs relativas para enlaces internos del sitio<br>
✅ Incluye title para proporcionar contexto adicional<br>
✅ Abre enlaces externos en nueva pestaña con target="_blank"<br>
✅ Usa el atributo rel apropiado (nofollow, sponsored, ugc)<br>
✅ Verifica que los enlaces funcionen antes de publicar<br>

❌ No uses "haz clic aquí" o "más información" como texto de enlace<br>
❌ No abras todos los enlaces en nueva pestaña (confunde al usuario)<br>
❌ No uses JavaScript para enlaces simples (href="#" está bien para anclas)<br>
❌ No omitas el protocolo en URLs absolutas<br>

## 🎓 Resumen
- La etiqueta <a> con el atributo href crea hipervínculos
- Las URLs absolutas incluyen el dominio completo; las relativas son rutas locales
- target="_blank" abre enlaces en nueva pestaña (siempre con rel="noopener noreferrer")
- Los enlaces internos usan # seguido del ID del elemento destino
- Los enlaces especiales incluyen mailto:, tel: y https://wa.me/
- El texto del enlace debe ser descriptivo y significativo
- Los atributos title y rel mejoran la accesibilidad y SEO