# Spring Boot - Actuator

## Definicion
Actuator expone endpoints de monitoreo y gestion de una app Spring Boot en runtime.

## Explicacion
- *Que problema resuelve*
    Permite observar salud, metricas y estado sin codigo custom para cada chequeo.
- *Como funciona por arriba*
    Con `spring-boot-starter-actuator` habilita endpoints como `/actuator/health`, `/actuator/info`, `/actuator/metrics`.
- *Que implica / que permite*
    Mejor operacion, diagnostico y observabilidad.

## Palabras clave
- Actuator
- health
- metrics
- observabilidad

## Comparaciones tipicas
- vs logging: logging muestra eventos; Actuator expone estado operativo.
- vs monitoreo externo puro: Actuator da señal interna util para integraciones.

## Preguntas de examen
- Que endpoints de Actuator son los mas usados?
- Que cuidado de seguridad requiere Actuator?

## Errores comunes
- Exponer todos los endpoints en produccion.
- No proteger endpoints sensibles.
