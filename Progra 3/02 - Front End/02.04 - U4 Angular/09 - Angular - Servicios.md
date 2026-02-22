# Angular - Servicios

## Definición

Un servicio en Angular es una clase para encapsular lógica compartida, acceso a datos y funcionalidades reutilizables entre componentes.

## Explicación

- *Qué problema resuelve*
    Evita duplicación y separa lógica de negocio del código de presentación.

- *Cómo funciona por arriba*
    Se crea con `ng g s`, se marca con `@Injectable` y se consume por inyección de dependencias.

- *Qué implica / qué permite*
    Permite reutilización, mejor testeo, manejo centralizado de estado y comunicación indirecta entre componentes.

## Alcance y provisión

- `providedIn: 'root'`: singleton global por defecto.
- `providers` en componente: instancia local al componente y su árbol.

## Palabras clave

- `@Injectable`
- Inyección de dependencias
- Singleton
- Reutilización
- Separación de responsabilidades

## Comparaciones típicas

- vs [[06 - Angular - Componentes]]: servicios no renderizan UI.
- vs [[15 - Angular - Comunicación entre componentes]]: servicio es alternativa cuando no hay relación padre-hijo directa.

## Preguntas de examen

- ¿Qué ventaja aporta `providedIn: 'root'`?
- ¿Cuándo conviene proveer un servicio a nivel de componente?

## Errores comunes

- Poner en servicios lógica que debería vivir en componentes (UI específica).
- Crear muchos servicios sin fronteras claras de responsabilidad.

## Mini-ejemplo (mental)

Servicio es como una “oficina central”: varios componentes consultan ahí en vez de duplicar reglas por separado.
