# Spring - Bean y ciclo de vida

## Definicion
Un bean es un objeto administrado por el contenedor de Spring. Spring se encarga de crearlo, configurarlo, inyectar dependencias y (segun scope) destruirlo.

## Explicacion
- *Que problema resuelve*
    Centraliza la creacion/configuracion y evita que cada clase tenga que "armar" su grafo de objetos.
- *Como funciona por arriba*
    - Spring registra beans (por scanning o `@Bean`).
    - Resuelve dependencias.
    - Ejecuta callbacks de inicializacion y destruccion.
- *Que implica / que permite*
    - Gestionar recursos (conexiones, clients, caches).
    - Aplicar features via proxies (AOP) sin cambiar el bean.

## Ciclo de vida (idea)
- Definicion del bean
- Instanciacion
- Inyeccion de dependencias
- Inicializacion (p. ej. `@PostConstruct`)
- Uso
- Destruccion (p. ej. `@PreDestroy`) si aplica

## Scopes comunes
- `singleton` (default): una instancia por `ApplicationContext`.
- `prototype`: una instancia por request al contenedor.

## Palabras clave
- Bean
- Scope
- `@PostConstruct`
- `@PreDestroy`

## Comparaciones tipicas
- vs objetos "a mano": con beans el contenedor administra el ciclo de vida.

## Preguntas de examen
- Que es un bean?
- Cual es el scope default y que significa?

## Errores comunes
- Asumir que `prototype` se destruye automaticamente (no siempre: depende del uso y del contenedor).
