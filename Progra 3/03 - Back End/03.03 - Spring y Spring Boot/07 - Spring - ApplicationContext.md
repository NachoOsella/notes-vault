# Spring - ApplicationContext

## Definicion
`ApplicationContext` es la interfaz principal del contenedor IoC en Spring. Representa el contexto de la aplicacion: configuracion, beans, profiles y recursos.

## Explicacion
- *Que problema resuelve*
    Provee un punto unico para resolver dependencias y acceder a configuracion.
- *Como funciona por arriba*
    Al iniciar, carga configuracion (clases `@Configuration`, scanning, properties) y crea/arma beans segun necesidad.
- *Que implica / que permite*
    - Publicar/escuchar eventos.
    - Integrar features (AOP, transacciones, MVC) sobre el mismo contenedor.

## Palabras clave
- IoC container
- BeanFactory vs ApplicationContext
- Profiles

## Comparaciones tipicas
- vs BeanFactory: `ApplicationContext` es mas completo (events, i18n, etc.).

## Preguntas de examen
- Que es `ApplicationContext` y que hace?
