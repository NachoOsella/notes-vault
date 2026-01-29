# Mockito - when()

## Definición
El método `when()` se utiliza para configurar el comportamiento de un objeto mock o spy cuando se llama a un método en particular. Es el inicio del proceso de **stubbing**.

## Explicación
- *Qué problema resuelve*
    Permite definir qué debe hacer un mock cuando se invoca uno de sus métodos, en lugar de devolver el valor por defecto (null/0/false).
- *Cómo funciona por arriba*
    Se especifica la llamada al método que queremos configurar y luego se encadena con `thenReturn()`, `thenThrow()`, etc. para definir la respuesta.
- *Qué implica / qué permite*
    - Simular respuestas exitosas con `thenReturn()`.
    - Simular errores con `thenThrow()`.
    - Controlar el flujo del test sin depender de implementaciones reales.

## Sintaxis básica
```java
when(mock.metodo(argumentos)).thenReturn(valor);
when(mock.metodo(argumentos)).thenThrow(excepcion);
```

## Ejemplos

### Retornar un valor
```java
List<String> mockList = mock(List.class);
when(mockList.size()).thenReturn(3);

assertEquals(3, mockList.size()); // Siempre devuelve 3
```

### Lanzar una excepción
```java
when(mockList.get(0)).thenThrow(new IndexOutOfBoundsException());

assertThrows(IndexOutOfBoundsException.class, () -> mockList.get(0));
```

### Con argumentos específicos
```java
when(repository.findById(1)).thenReturn(new Entity(1, "Test"));
when(repository.findById(2)).thenReturn(new Entity(2, "Otro"));

// Solo matchea con el argumento exacto
```

### Con argument matchers
```java
when(repository.findById(anyInt())).thenReturn(new Entity());
when(service.process(any(String.class))).thenReturn(true);
```

## Encadenamiento de respuestas
Se pueden definir múltiples respuestas consecutivas:
```java
when(mock.metodo())
    .thenReturn("primera llamada")
    .thenReturn("segunda llamada")
    .thenThrow(new RuntimeException("tercera llamada"));
```

## Palabras clave
- when()
- Stubbing
- thenReturn
- thenThrow
- Argument matchers
- any()
- anyInt()

## Comparaciones típicas
- vs [[Mockito - thenReturn()]]: `when(...)` arranca el stubbing; `thenReturn(...)` define el valor devuelto.
- vs [[Mockito - verify()]]: stubbing (`when`) define comportamiento **antes** de ejecutar; verify valida interacciones **después**.

## Preguntas de examen
- ¿Para qué sirve el método `when()` en Mockito?
- ¿Cómo se configura un mock para que lance una excepción?
- ¿Qué son los argument matchers y cuándo se usan?

## Errores comunes
- Usar `when()` con un objeto real en vez de un mock (no funciona).
- Mezclar argument matchers con valores literales: si usás un matcher, todos los argumentos deben ser matchers.
  ```java
  // MAL:
  when(mock.metodo(anyInt(), "literal")).thenReturn(x);
  // BIEN:
  when(mock.metodo(anyInt(), eq("literal"))).thenReturn(x);
  ```
- Usar `when()` con spies sin cuidado (puede ejecutar el método real). Usar `doReturn()` en su lugar.

## Mini-ejemplo (mental)
`when()` es como darle un guión a un actor. Le decís: "Cuando te pregunten X, respondé Y". El actor (mock) no piensa por sí mismo, solo sigue el guión que le diste. Si no le das guión para una pregunta, responde con silencio (null).
