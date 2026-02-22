# Spring - Component Scanning

## Definicion
Component scanning es el mecanismo por el que Spring detecta clases anotadas (p. ej. `@Component`, `@Service`) y las registra como beans automaticamente.

## Explicacion
- *Que problema resuelve*
    Evita declarar manualmente cada bean.
- *Como funciona por arriba*
    Spring recorre packages (segun `@ComponentScan` / paquete base de la app) y registra componentes encontrados.
- *Que implica / que permite*
    - Organizar el proyecto por capas/paquetes.
    - Activar/desactivar componentes con profiles.

## Palabras clave
- `@ComponentScan`
- Base package
- Classpath scanning

## Comparaciones tipicas
- vs [[10 - Spring - Configuracion (@Configuration @Bean)]]: scanning detecta automaticamente; `@Bean` define beans en forma explicita.

## Preguntas de examen
- Que es el component scanning y como se configura?

## Errores comunes
- No incluir el paquete correcto y que "no aparezcan" beans.
