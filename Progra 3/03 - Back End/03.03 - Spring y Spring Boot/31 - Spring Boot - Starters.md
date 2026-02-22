# Spring Boot - Starters

## Definicion
Los starters son paquetes de dependencias prearmadas para casos comunes (`web`, `data-jpa`, `security`, etc.).

## Explicacion
- *Que problema resuelve*
    Evita seleccionar y versionar manualmente decenas de librerias relacionadas.
- *Como funciona por arriba*
    Al agregar un starter, Boot incorpora dependencias compatibles y habilita autoconfiguraciones asociadas.
- *Que implica / que permite*
    Menos conflictos de versiones y arranque mas rapido.

## Palabras clave
- starter
- dependency management
- spring-boot-starter-web
- spring-boot-starter-data-jpa

## Comparaciones tipicas
- vs dependencias manuales: starter simplifica y estandariza.
- vs [[32 - Spring Boot - Auto-configuration]]: starter aporta libs; auto-config decide configuracion.

## Preguntas de examen
- Que ventaja practica tiene un starter?
- Menciona starters comunes y su uso.

## Errores comunes
- Agregar starters sin necesitarlos.
- No revisar el impacto en classpath y arranque.
