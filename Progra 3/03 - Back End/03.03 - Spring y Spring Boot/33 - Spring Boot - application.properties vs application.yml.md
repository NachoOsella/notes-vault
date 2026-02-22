# Spring Boot - application.properties vs application.yml

## Definicion
Son dos formatos para configuracion externa en Spring Boot: `.properties` (clave=valor) y `.yml` (estructura jerarquica).

## Explicacion
- *Que problema resuelve*
    Permiten configurar sin recompilar y por entorno.
- *Como funciona por arriba*
    Boot carga ambos formatos con precedencia definida junto con variables de entorno y argumentos.
- *Que implica / que permite*
    Configuracion flexible para distintos despliegues.

## Comparaciones tipicas
- `properties`: simple y directo para pocas claves.
- `yml`: mas legible en configuraciones anidadas.
- vs [[12 - Spring - Properties y Environment]]: esta nota baja la idea al uso concreto en Boot.

## Palabras clave
- application.properties
- application.yml
- precedencia
- perfiles

## Preguntas de examen
- Cuando conviene YAML sobre properties?
- Que fuentes de configuracion pueden sobrescribir archivos?

## Errores comunes
- Mezclar formatos sin criterio en el mismo proyecto.
- Hardcodear secretos en archivos versionados.
