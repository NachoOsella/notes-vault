# Mockito - spy() y @Spy

## Definición
Un **spy** es un objeto simulado que se crea a partir de un objeto real. A diferencia de un mock, el spy mantiene el comportamiento original del objeto pero permite configurar comportamientos adicionales o sobrescribir métodos específicos.

## Explicación
- *Qué problema resuelve*
    Permite testear objetos reales mientras se controlan o monitorean partes específicas de su comportamiento, sin reemplazar todo el objeto.
- *Cómo funciona por arriba*
    Se envuelve un objeto real con `spy()`. Los métodos que no se stubeen ejecutan el código real. Se pueden stubear métodos específicos y verificar llamadas.
- *Qué implica / qué permite*
    - Registrar llamadas a métodos del objeto real.
    - Modificar el valor de retorno de métodos específicos.
    - Mantener el comportamiento real para la mayoría de los métodos.

## Formas de crear un spy

### Con spy()
Se pasa un objeto real como parámetro.
```java
List<String> myList = new ArrayList<>();
List<String> mySpy = spy(myList);
```

### Con @Spy
Se usa la anotación sobre una variable inicializada o con tipo concreto.
```java
@Spy
private ArrayList<String> mySpy = new ArrayList<>();

// O sin inicializar (Mockito crea la instancia):
@Spy
private MyClass mySpy;
```

## Diferencia clave con mock
| Aspecto | Mock | Spy |
|---------|------|-----|
| Comportamiento default | Métodos devuelven null/0/false | Métodos ejecutan código real |
| Objeto base | No hay objeto real | Envuelve un objeto real |
| Uso típico | Aislar dependencias externas | Testear parcialmente un objeto real |

## Ejemplo
```java
@Test
void testSpy() {
    List<String> myList = new ArrayList<>();
    List<String> mySpy = spy(myList);
    
    // El método real se ejecuta
    mySpy.add("uno");
    mySpy.add("dos");
    assertEquals(2, mySpy.size()); // Comportamiento real
    
    // Pero podemos stubear métodos específicos
    when(mySpy.size()).thenReturn(100);
    assertEquals(100, mySpy.size()); // Comportamiento stubeado
    
    // Verificar interacciones
    verify(mySpy).add("uno");
}
```

## Cuidado con when() en spies
Con spies, `when(spy.metodo())` puede ejecutar el método real antes de stubear. Para evitarlo, usar `doReturn()`:
```java
// Puede causar problemas:
when(spy.metodo()).thenReturn(valor);

// Forma segura:
doReturn(valor).when(spy).metodo();
```

## Palabras clave
- Spy
- Objeto parcialmente mockeado
- spy()
- @Spy
- doReturn
- Comportamiento real

## Comparaciones típicas
- vs [[Mockito - mock() y @Mock]]: spy mantiene comportamiento real por default; mock no tiene comportamiento (devuelve null/0/false).
- vs [[Mockito - when()]]: con spies, `when` puede ejecutar el método real (cuidado); a veces conviene usar `doReturn`/`doThrow`.

## Preguntas de examen
- ¿Qué es un spy en Mockito y cómo difiere de un mock?
- ¿Cuándo conviene usar un spy en lugar de un mock?
- ¿Por qué se recomienda usar `doReturn()` en vez de `when()` con spies?

## Errores comunes
- Usar `when()` con spies y que el método real se ejecute inesperadamente.
- Confundir spy con mock: el spy ejecuta código real si no se stubea.
- Crear un spy de una interfaz (no tiene sentido, usá mock).
- No inicializar el objeto antes de hacer spy (con `@Spy` sin inicialización, Mockito usa constructor sin args).

## Mini-ejemplo (mental)
Un spy es como poner un micrófono oculto a una persona real. La persona sigue comportándose normalmente (ejecuta código real), pero vos podés escuchar todo lo que dice (verificar llamadas) y, si querés, podés susurrarle qué decir en momentos específicos (stubear métodos puntuales).
