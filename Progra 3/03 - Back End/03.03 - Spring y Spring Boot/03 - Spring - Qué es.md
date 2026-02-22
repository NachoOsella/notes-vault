# Spring - Que es

## Definicion
Spring Framework es un framework open source para Java que aporta un modelo de programacion y configuracion para aplicaciones empresariales, enfocandose en la infraestructura ("plumbing") para que el codigo se centre en la logica de negocio.

## Explicacion
- *Que problema resuelve*
    Evita configuracion repetitiva y acoplamiento a infraestructura (servidores, persistencia, integraciones), ofreciendo un contenedor que arma y conecta componentes.
- *Como funciona por arriba*
    El nucleo es el contenedor IoC: registra beans, resuelve dependencias (DI) y aplica funcionalidades transversales con proxies (AOP).
- *Que implica / que permite*
    - Modularizar la aplicacion en capas y componentes reutilizables.
    - Cambiar decisiones de infraestructura via configuracion (sin tocar el dominio).
    - Construir apps web (Spring MVC), acceso a datos (Spring Data), seguridad, etc.

## Notas utiles (del material)
- Desde Spring Framework 6, Spring requiere Java 17+.
- "Spring" suele referirse a toda la familia de proyectos (no solo Spring Framework).

## Palabras clave
- IoC
- DI
- Bean
- ApplicationContext
- AOP

## Comparaciones tipicas
- vs [[30 - Spring Boot - Que es]]: Spring es el framework base; Boot es una forma "opinionada" y rapida de armar apps listas para correr.
- vs Jakarta EE: Spring es un ecosistema/framework; Jakarta EE es un conjunto de especificaciones estandar.

## Preguntas de examen
- Que es Spring Framework y que rol cumple en una app Java?
- Por que se dice que Spring se enfoca en la infraestructura de aplicacion?

## Errores comunes
- Confundir Spring (framework) con Spring Boot (herramienta para acelerar el setup).
- Pensar que Spring es solo "anotaciones": el valor esta en el contenedor y el modelo.
