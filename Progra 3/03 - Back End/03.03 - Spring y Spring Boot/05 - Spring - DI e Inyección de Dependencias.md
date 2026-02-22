# Spring - DI e Inyeccion de Dependencias

## Definicion
DI (Dependency Injection) es un patron donde un objeto recibe sus dependencias desde afuera (por constructor, setter o campo), en vez de crearlas internamente.

## Explicacion
- *Que problema resuelve*
    - Baja acoplamiento.
    - Facilita tests unitarios.
    - Hace explicitas las dependencias.
- *Como funciona por arriba*
    Spring detecta componentes (o beans definidos) y, al instanciarlos, resuelve que dependencia inyectar segun el tipo (y qualifiers si aplica).
- *Que implica / que permite*
    - Cambiar implementaciones por configuracion.
    - Aplicar patrones por capas (Controller-Service-Repository).

## Formas comunes
- Inyeccion por constructor (recomendada): dependencias obligatorias.
- Inyeccion por setter: dependencias opcionales o reconfigurables.
- Inyeccion por campo: comoda, pero dificulta test y explicitar dependencias.

## Palabras clave
- `@Autowired`
- Constructor injection
- `@Qualifier`

## Comparaciones tipicas
- vs new(): con DI no instancias dependencias adentro; el contenedor las provee.
- vs [[04 - Spring - IoC e Inversion de Control]]: DI es una forma concreta de lograr IoC.

## Preguntas de examen
- Que ventajas tiene DI?
- Por que se recomienda constructor injection?

## Errores comunes
- Inyectar demasiadas dependencias: suele indicar una clase con demasiadas responsabilidades.
