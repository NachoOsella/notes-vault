# Storage - sessionStorage

## Definición

`sessionStorage` guarda datos temporales en el navegador, solo para la pestaña actual.

## Explicación

- *Qué problema resuelve*
    Conserva estado breve durante navegación sin persistir datos entre sesiones.

- *Cómo funciona por arriba*
    - API: `window.sessionStorage`
    - Guarda clave-valor como texto
    - Sobrevive a recargas (F5)
    - Se borra al cerrar la pestaña

- *Qué implica / qué permite*
    - Flujos de formulario o estado temporal
    - Aislamiento por pestaña
    - Menos riesgo de arrastrar datos viejos

## API básica

- `setItem(clave, valor)`
- `getItem(clave)`
- `removeItem(clave)`
- `clear()`
- `length`

## Comparación rápida

| Aspecto | sessionStorage | localStorage |
|---|---|---|
| Duración | Hasta cerrar pestaña | Persistente |
| Compartido entre pestañas | No | Sí |
| Uso típico | Estado temporal | Preferencias/caché |

## Palabras clave

- sessionStorage
- Sesión de pestaña
- Temporal
- Web Storage
- Aislamiento

## Comparaciones típicas

- vs [[13 - Storage - localStorage]]: sessionStorage no persiste al cerrar pestaña
- vs [[15 - Cookies - Crear y usar cookies en JS]]: sessionStorage no se envía automáticamente al servidor

## Preguntas de examen

- ¿Cuándo se eliminan los datos de sessionStorage?
- ¿Se comparte entre pestañas del mismo sitio?
- ¿Qué caso de uso típico tiene?

## Errores comunes

- Creer que comparte datos entre pestañas
- Confundir sesión de navegador con sesión backend
- Guardar datos sensibles

## Mini-ejemplo (mental)

Es una pizarra en tu mesa actual: sirve mientras estás ahí; al cerrar esa mesa, se borra.
