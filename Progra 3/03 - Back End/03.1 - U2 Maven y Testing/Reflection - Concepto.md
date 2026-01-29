# Reflection - Concepto

## Definición
Reflection es una técnica de Java que permite a un programa inspeccionar y manipular objetos en tiempo de ejecución, incluso si no se conoce su tipo en tiempo de compilación. Permite examinar la estructura de clases (campos, métodos, constructores) y manipular sus objetos dinámicamente.

## Explicación
- *Qué problema resuelve*
    Permite acceder a miembros de una clase (incluyendo privados) en tiempo de ejecución, lo cual es útil para frameworks de testing, inyección de dependencias y serialización.
- *Cómo funciona por arriba*
    Se obtiene el objeto `Class<?>` de una clase, y a partir de él se pueden obtener `Field`, `Method`, `Constructor`. Estos objetos permiten leer/escribir campos, invocar métodos y crear instancias.
- *Qué implica / qué permite*
    - Inspeccionar la estructura de clases desconocidas.
    - Acceder a campos y métodos privados.
    - Crear instancias sin conocer el tipo en compilación.
    - Implementar frameworks genéricos (JUnit, Spring, Hibernate).

## Uso en testing
En testing, reflection se usa principalmente para:
1. **Testear métodos privados**: Acceder a métodos que no son públicos.
2. **Modificar campos privados**: Inyectar valores de prueba.
3. **Frameworks de mock**: Mockito usa reflection para inyectar mocks.

## Ejemplo básico
```java
// Obtener la clase
Class<?> clazz = MiClase.class;

// Obtener un método privado
Method metodo = clazz.getDeclaredMethod("metodoPrivado", String.class);
metodo.setAccessible(true); // Permitir acceso a privados

// Invocar el método
Object resultado = metodo.invoke(instancia, "argumento");

// Obtener un campo privado
Field campo = clazz.getDeclaredField("campoPrivado");
campo.setAccessible(true);
Object valor = campo.get(instancia);
```

## Advertencias importantes
- **Rompe encapsulamiento**: Acceder a miembros privados es considerado mala práctica en producción.
- **Problemas de mantenimiento**: El código que usa reflection es frágil ante refactors.
- **Rendimiento**: Es más lento que el acceso directo.
- **Usar con precaución**: Solo cuando no hay alternativa (testing de legacy code, frameworks).

## Palabras clave
- Reflection
- Introspección
- Tiempo de ejecución
- Class
- Field
- Method
- setAccessible
- getDeclaredMethod

## Comparaciones típicas
- vs [[ReflectionSupport (JUnit)]]: reflection es el concepto general de Java; ReflectionSupport es una utilidad de JUnit que simplifica su uso en tests.
- vs [[Mockito - @InjectMocks]]: Mockito usa reflection internamente para inyectar mocks en campos/constructores automáticamente.

## Preguntas de examen
- ¿Qué es Reflection y para qué se utiliza?
- ¿Por qué se considera mala práctica usar reflection para acceder a miembros privados?
- ¿Cómo se accede a un método privado usando reflection?
- ¿Qué método se usa para permitir el acceso a miembros privados?

## Errores comunes
- Olvidar llamar a `setAccessible(true)` antes de acceder a miembros privados.
- No manejar las excepciones de reflection (`NoSuchMethodException`, `IllegalAccessException`, etc.).
- Usar reflection como solución habitual en vez de como último recurso.
- Hardcodear nombres de métodos/campos como strings (se rompe con refactors).

## Mini-ejemplo (mental)
Reflection es como tener una llave maestra que abre todas las puertas de un edificio. Normalmente, solo deberías entrar por las puertas que te corresponden (métodos públicos). Pero con la llave maestra (reflection) podés abrir cualquier puerta, incluso las privadas. Es útil para mantenimiento (testing), pero no deberías usarla para el día a día porque rompe las reglas de seguridad del edificio (encapsulamiento).
