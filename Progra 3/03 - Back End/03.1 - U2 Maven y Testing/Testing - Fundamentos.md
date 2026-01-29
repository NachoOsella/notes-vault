# Testing - Fundamentos

## Definición
Los fundamentos del testing son los conceptos básicos y principios que se deben comprender para llevar a cabo el proceso de evaluación y verificación de software de manera efectiva.

## Explicación
- *Qué problema resuelve*
    Proporciona un marco mental y metodológico para diseñar, ejecutar y analizar pruebas de forma sistemática y eficiente.
- *Cómo funciona por arriba*
    Se establecen objetivos claros, se seleccionan tipos de prueba apropiados, se diseñan casos de prueba que cubran escenarios relevantes, se ejecutan y se analizan los resultados para retroalimentación.
- *Qué implica / qué permite*
    Garantiza que las pruebas sean objetivas, reproducibles y completas. Permite detectar errores de forma consistente y mejorar continuamente la calidad del software.

## Objetivo del testing
Identificar errores, bugs o problemas para mejorar la calidad del software y garantizar que cumple con los requerimientos especificados.

## Tipos de testing
| Tipo | Descripción | Etapa |
|------|-------------|-------|
| **Pruebas Unitarias** | Verifican unidades individuales de código (clases, métodos) de forma aislada | Desarrollo |
| **Pruebas de Integración** | Verifican la interacción entre diferentes unidades/módulos | Integración |
| **Pruebas de Sistema** | Verifican que el software cumple los requerimientos en el entorno de producción | Sistema |
| **Pruebas de Aceptación** | Realizadas por el usuario/cliente para validar que cumple sus necesidades | Aceptación |
| **Pruebas de Regresión** | Verifican que cambios nuevos no rompan funcionalidades existentes | Todo el ciclo |
| **Pruebas Exploratorias** | Pruebas ad-hoc para descubrir errores no previstos | Sistema/Aceptación |
| **Pruebas de Carga** | Verifican el comportamiento bajo condiciones extremas (picos de tráfico, etc.) | Sistema |

## Características de una buena prueba
- **Repetibilidad**: Produce los mismos resultados cada vez que se ejecuta.
- **Cobertura**: Cubre una amplia gama de casos para probar todas las funcionalidades relevantes.
- **Precisión**: Mide exactamente lo que se pretende probar.
- **Independencia**: No depende de otras pruebas para ejecutarse.
- **Facilidad de mantenimiento**: Fácil de entender, modificar y actualizar.
- **Complejidad adecuada**: Suficiente para detectar errores, pero no tan compleja que sea difícil de entender.
- **Claridad y documentación**: Bien documentada para facilitar su comprensión.

## Ciclo de vida del testing
1. **Planificación**: Identificar requerimientos y funcionalidades a probar.
2. **Diseño**: Crear casos de prueba que cubran todos los escenarios.
3. **Ejecución**: Ejecutar los casos de prueba y recopilar resultados.
4. **Análisis**: Identificar errores y reportarlos.
5. **Mejora continua**: Usar la información para mejorar el software.

## Palabras clave
- Tipos de testing
- Casos de prueba
- Cobertura
- Repetibilidad
- Independencia
- Ciclo de vida
- Regresión

## Comparaciones típicas
- vs [[Testing - Introducción]]: fundamentos profundiza en conceptos (tipos, características, ciclo de vida); intro es más contextual.
- vs [[Testing - Tests unitarios]]: fundamentos aplica a todo tipo de testing; unit tests son un caso concreto (aislado, rápido, determinista).

## Preguntas de examen
- ¿Cuáles son los principales tipos de testing y en qué etapa se aplican?
- ¿Qué características debe tener una buena prueba?
- ¿Cuál es la diferencia entre pruebas unitarias y pruebas de integración?
- ¿Qué son las pruebas de regresión y por qué son importantes?

## Errores comunes
- Confundir tipos de testing: unitario prueba aislado, integración prueba interacción.
- Diseñar pruebas que dependen de otras pruebas (rompe independencia).
- No actualizar las pruebas cuando cambia el código (pruebas obsoletas).
- Creer que más pruebas = mejor calidad (importa la cobertura de escenarios, no la cantidad).

## Mini-ejemplo (mental)
Pensá en un auto antes de salir a la calle. Las pruebas unitarias son como verificar cada pieza por separado (motor, frenos, luces). Las pruebas de integración verifican que las piezas funcionen juntas (motor + transmisión). Las pruebas de sistema verifican que el auto completo funcione en la ruta. Las pruebas de aceptación son cuando el dueño lo prueba y dice "sí, esto es lo que pedí".
