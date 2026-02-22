# Spring Boot - Logging

## Definicion
Spring Boot integra logging por defecto (SLF4J + Logback) para registrar eventos y diagnosticar problemas.

## Explicacion
- *Que problema resuelve*
    Da trazabilidad de ejecucion y facilita debugging en desarrollo y produccion.
- *Como funciona por arriba*
    Se configuran niveles (`ERROR`, `WARN`, `INFO`, `DEBUG`, `TRACE`) por paquete o clase.
- *Que implica / que permite*
    Diagnostico mas rapido y auditoria tecnica basica.

## Palabras clave
- SLF4J
- Logback
- log levels
- trazas

## Comparaciones tipicas
- vs `System.out.println`: logging es estructurado y configurable.
- vs [[35 - Spring Boot - Actuator]]: logging registra eventos; Actuator publica estado/metricas.

## Preguntas de examen
- Que nivel usar por defecto en produccion y por que?
- Como cambiar el nivel de log por paquete?

## Errores comunes
- Loggear datos sensibles.
- Dejar `DEBUG` global activo en produccion.
