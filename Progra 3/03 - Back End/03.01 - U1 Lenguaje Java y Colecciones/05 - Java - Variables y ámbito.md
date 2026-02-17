# Java - Variables y ámbito

## Definición

Una variable guarda un dato; su ámbito (scope) define dónde puede usarse.

## Explicación

- *Qué problema resuelve*
    Permite trabajar con datos sin confundir nombres ni acceder a valores fuera de contexto.

- *Cómo funciona por arriba*
    - Variable local: existe dentro de un método o bloque
    - Variable de instancia: pertenece a cada objeto
    - Variable estática: pertenece a la clase

- *Qué implica / qué permite*
    - Mejor organización del código
    - Menos errores de acceso
    - Control de ciclo de vida de los datos

## Tipos por ámbito

| Tipo | Dónde se usa | Duración | Inicialización automática |
|---|---|---|---|
| Local | Método/bloque | Hasta salir del bloque | No |
| Instancia | Objeto | Vida del objeto | Sí |
| Estática | Clase | Vida del programa | Sí |
| Parámetro | Firma del método | Llamada actual | Viene asignado |

## Palabras clave

- Variable local
- Variable de instancia
- Variable estática
- Scope
- Ciclo de vida

## Comparaciones típicas

- vs [[04 - Java - Tipos de datos]]: el tipo define qué guarda; el ámbito define dónde vive
- vs [[02 - Java - JDK y JVM]]: ámbito no es herramienta de compilación/ejecución, es regla del lenguaje

## Preguntas de examen

- ¿Qué diferencia hay entre variable local y de instancia?
- ¿Cuál se comparte entre objetos de la misma clase?
- ¿Las variables locales se inicializan solas?

## Errores comunes

- Usar una local sin inicializar
- Querer usar una variable fuera de su bloque
- Confundir estática con de instancia

## Mini-ejemplo (mental)

Es como tener notas en distintos lugares: una nota en tu escritorio (local), una en cada carpeta personal (instancia) y una en el pizarrón común (estática).
