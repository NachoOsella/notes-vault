# Spring Boot - Empaquetado y ejecucion (jar)

## Definicion
Spring Boot permite empaquetar la app como JAR ejecutable con servidor embebido y ejecutarla con `java -jar`.

## Explicacion
- *Que problema resuelve*
    Simplifica despliegue al evitar instalar servidor externo para casos comunes.
- *Como funciona por arriba*
    Maven/Gradle genera un "fat jar" con dependencias; se inicia como proceso standalone.
- *Que implica / que permite*
    Entrega mas simple y portable entre entornos.

## Palabras clave
- fat jar
- java -jar
- servidor embebido
- despliegue

## Comparaciones tipicas
- vs WAR en servlet container: JAR es mas autonomo; WAR depende del contenedor externo.
- vs [[30 - Spring Boot - Que es]]: esta nota aplica Boot al momento de release/ejecucion.

## Preguntas de examen
- Que ventajas tiene un JAR ejecutable en Spring Boot?
- En que caso preferirias empaquetar como WAR?

## Errores comunes
- No configurar perfiles/variables por entorno al ejecutar el jar.
- Suponer que jar implica automaticamente buena observabilidad.
