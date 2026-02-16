# Preguntas - FE U1

## HTML

### Que es HTML?
Respuesta: Lenguaje de marcado para estructurar contenido web con etiquetas. Ver: [[03 - HTML - Definición]]

### Para que sirve HTML?
Respuesta: Define la estructura y el contenido de una pagina web (texto, imagenes, enlaces, formularios).

### Cual es la diferencia entre HTML y CSS?
Respuesta: HTML estructura el contenido; CSS define la presentacion visual (colores, fuentes, margenes).

### Cual es la diferencia entre etiquetas semanticas y no semanticas?
Respuesta: Las semanticas aportan significado (header, nav, article, footer - mejoran accesibilidad/SEO); las no semanticas son genericas (div, span). Ver: [[05 - HTML - Etiquetas semánticas]]

### Cuales son las etiquetas HTML mas importantes?
Respuesta: Estructura (html, head, body), texto (h1-h6, p), listas (ul, ol, li), enlaces (a), imagenes (img), formularios (form, input). Ver: [[04 - HTML - Principales etiquetas]]

---

## CSS

### Que es CSS y que hace?
Respuesta: Define la presentacion visual separada de la estructura HTML (colores, fuentes, espaciado, layout). Ver: [[06 - CSS - Definición]]

### Que es un selector en CSS?
Respuesta: Patron que apunta a elementos HTML para aplicarles estilos (elemento, clase, id, atributo). Ver: [[07 - CSS - Selectores]]

### Que diferencia hay entre selectores y propiedades?
Respuesta: El selector apunta a elementos; las propiedades definen el estilo aplicado (color, margin, font-size).

### Que es el box model?
Respuesta: Modelo del tamanio de un elemento: content + padding + border + margin. Ver: [[09 - CSS - Box Model]]

### Que es diseno responsivo?
Respuesta: Tecnica para que la pagina se adapte a distintos tamanios de pantalla usando media queries, flexbox, grid. Ver: [[10 - CSS - Diseño responsivo]]

### Cuales son las propiedades CSS mas comunes?
Respuesta: color, background, margin, padding, border, font-size, display, position, flexbox/grid. Ver: [[08 - CSS - Propiedades comunes]]

---

## JavaScript

### Que es una funcion?
Respuesta: Bloque reutilizable que encapsula una tarea, puede recibir parametros y devolver un resultado. Ver: [[14 - JS - Funciones]]

### Cual es la diferencia entre parametros y valor de retorno?
Respuesta: Parametros son datos de entrada; el valor de retorno es el resultado que devuelve la funcion.

### Para que sirven las estructuras de control?
Respuesta: Controlan el flujo del programa: decisiones (if/else, switch) y repeticiones (for, while). Ver: [[13 - JS - Estructuras de control]]

### Cuando usar if/else vs un loop?
Respuesta: if/else para decisiones (ejecutar un camino u otro); loops para repetir acciones multiples veces.

---

## Tailwind

### Que es Tailwind?
Respuesta: Framework CSS de utilidades: compones estilos con clases en el HTML en vez de escribir reglas CSS separadas. Ver: [[11 - Tailwind - Conceptos clave]]

### Que significa utility-first?
Respuesta: Cada clase hace una sola cosa (ej: `text-red-500`, `p-4`); combinas muchas clases para crear el estilo completo.

### Que diferencia hay entre CSS puro y Tailwind?
Respuesta: CSS puro = escribis reglas en archivos .css; Tailwind = usas clases predefinidas directamente en el HTML.

### Como se aplica un estilo en Tailwind?
Respuesta: Con clases en el atributo class del HTML: `<div class="bg-blue-500 p-4 rounded">`. Ver: [[12 - Tailwind - Sintaxis básica]]

---

## Respuestas rapidas

| Pregunta | Respuesta corta |
|----------|-----------------|
| HTML vs CSS | HTML = estructura; CSS = estilo |
| HTML vs JS | HTML = contenido; JS = comportamiento |
| Etiqueta semantica | Aporta significado (header, nav, article) |
| Box model | content + padding + border + margin |
| Media query | Aplica estilos segun tamanio de pantalla |
| Funcion JS | Bloque reutilizable con parametros y retorno |
| Tailwind | Framework CSS utility-first |
