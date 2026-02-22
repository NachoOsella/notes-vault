# Spring - AOP (concepto)

## Definicion
AOP (Aspect Oriented Programming) es un enfoque para modularizar preocupaciones transversales (logging, transacciones, seguridad) sin mezclar ese codigo con la logica de negocio.

## Explicacion
- *Que problema resuelve*
    Evita duplicar codigo transversal en muchos metodos y mantiene las capas mas limpias.
- *Como funciona por arriba*
    Spring suele aplicar AOP creando proxies alrededor de beans: cuando llamas un metodo, el proxy ejecuta "advice" antes/despues/durante excepciones.
- *Que implica / que permite*
    - Implementar transacciones con `@Transactional`.
    - Logging y metricas sin ensuciar servicios.
    - Politicas de seguridad o reintentos.

## Palabras clave
- Aspect
- Pointcut
- Advice
- Proxy

## Comparaciones tipicas
- vs herencia: AOP aplica comportamiento sin modificar la jerarquia de clases.
- vs decorador manual: AOP automatiza el armado de decoradores/proxies.

## Preguntas de examen
- Que es AOP y que casos de uso tiene?
- Por que `@Transactional` suele implementarse con AOP?

## Errores comunes
- Esperar que AOP funcione en llamadas internas del mismo bean (self-invocation) sin configuracion especial.
