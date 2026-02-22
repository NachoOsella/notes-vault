# Spring Boot - Auto-configuration

## Definicion
La autoconfiguracion ajusta automaticamente beans y settings segun dependencias y propiedades detectadas.

## Explicacion
- *Que problema resuelve*
    Evita escribir configuracion base repetitiva para componentes comunes.
- *Como funciona por arriba*
    Boot evalua el classpath y condiciones (`@Conditional...`) para activar configuraciones por defecto.
- *Que implica / que permite*
    Productividad alta sin perder control (se puede sobrescribir).

## Palabras clave
- auto-configuration
- condiciones
- classpath
- convencion

## Comparaciones tipicas
- vs configuracion manual total: auto-config acelera el inicio.
- vs [[10 - Spring - Configuracion (@Configuration @Bean)]]: auto-config cubre base; `@Configuration` customiza.

## Preguntas de examen
- Que mira Spring Boot para decidir autoconfiguraciones?
- Se puede desactivar o reemplazar una autoconfiguracion?

## Errores comunes
- Asumir que todo se configura "magicamente" sin entender defaults.
- Duplicar beans sin necesidad.
