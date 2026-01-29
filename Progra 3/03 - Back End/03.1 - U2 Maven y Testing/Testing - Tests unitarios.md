# Testing - Tests unitarios

## Definición
El testing unitario es una técnica de prueba que se enfoca en comprobar el correcto funcionamiento de las unidades de código individualmente (clases, métodos, funciones), de forma aislada del resto del sistema.

## Explicación
- *Qué problema resuelve*
    Permite detectar errores en el código en una etapa temprana del desarrollo, antes de la integración con otras partes del sistema. Esto reduce costos y tiempo de desarrollo.
- *Cómo funciona por arriba*
    Se crean clases de prueba que contienen métodos que verifican el comportamiento del código bajo prueba. Cada método usa aserciones para comparar resultados esperados vs reales.
- *Qué implica / qué permite*
    Las pruebas son automatizadas y se ejecutan rápidamente, permitiendo mayor frecuencia de ejecución y retroalimentación inmediata del estado del código.

## Requisitos para unit tests efectivos
- **Código limpio y modular**: Alta cohesión, bajo acoplamiento.
- **Patrones de diseño**: Facilitan el aislamiento de dependencias.
- **Buenas prácticas de codificación**: Código fácil de testear.
- **Planificación adecuada**: Estrategia de pruebas y organización.

## Herramientas principales
| Herramienta | Propósito |
|-------------|-----------|
| **JUnit** | Framework de pruebas unitarias. Permite escribir y ejecutar tests automatizados. Compatible con IDEs como NetBeans e IntelliJ. |
| **Mockito** | Framework para simular objetos (mocks) y comportamientos. Facilita el aislamiento de dependencias. |

### JUnit
- Proporciona anotaciones (`@Test`, `@BeforeEach`, etc.) para definir pruebas.
- Usa **aserciones** para verificar el comportamiento del código.
- Puede ejecutarse con Maven/Gradle o desde el IDE.
- Permite ejecución de pruebas en paralelo.

### Mockito
- Se utiliza para **simular objetos y comportamientos** en las pruebas.
- Permite simular objetos que aún no se han implementado.
- Facilita probar objetos complejos (bases de datos, servicios web).
- Se integra bien con JUnit.

## Proceso general de un Unit Test
1. **Arrange** (Preparar): Configurar el estado inicial y los objetos necesarios.
2. **Act** (Actuar): Ejecutar el método o funcionalidad a probar.
3. **Assert** (Afirmar): Verificar que el resultado es el esperado.

## Palabras clave
- Pruebas unitarias
- Aislamiento
- Aserciones
- JUnit
- Mockito
- Automatización
- Arrange-Act-Assert

## Comparaciones típicas
- vs [[Testing - Fundamentos]]: unit tests implementan los principios de testing; fundamentos explica el marco mental general.
- vs [[Mockito - mock() y @Mock]]: unit tests suelen usar mocks para aislar dependencias externas.

## Preguntas de examen
- ¿Qué es el testing unitario y cuál es su objetivo?
- ¿Cuál es la diferencia entre JUnit y Mockito?
- ¿Por qué es importante aislar las dependencias en pruebas unitarias?
- ¿Qué significa el patrón Arrange-Act-Assert?

## Errores comunes
- No aislar las dependencias: si el test depende de una base de datos real, no es un unit test puro.
- Tests que dependen del orden de ejecución: cada test debe ser independiente.
- No usar mocks cuando corresponde: hace los tests lentos y frágiles.
- Testear implementación en vez de comportamiento: el test debe verificar "qué hace", no "cómo lo hace".

## Mini-ejemplo (mental)
Imagina que tenés una calculadora con un método `sumar(a, b)`. Un test unitario crearía una instancia de la calculadora, llamaría a `sumar(2, 3)` y verificaría que el resultado sea `5`. Si la calculadora dependiera de un servicio externo (como un logger), usarías un mock para simular ese servicio y mantener el test aislado.
