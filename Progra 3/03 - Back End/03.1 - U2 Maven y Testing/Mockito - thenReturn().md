# Mockito - thenReturn()

## Definición
El método `thenReturn()` se utiliza para configurar el valor que debe devolver un mock cuando se llama a un método stubeado. Se encadena después de `when()`.

## Explicación
- *Qué problema resuelve*
    Permite definir qué valor debe retornar un método mockeado, simulando una respuesta exitosa sin ejecutar código real.
- *Cómo funciona por arriba*
    Cuando el método configurado es invocado en el mock, Mockito intercepta la llamada y devuelve el valor especificado en `thenReturn()`.
- *Qué implica / qué permite*
    - Simular respuestas de dependencias externas.
    - Controlar los datos que fluyen en el test.
    - Testear diferentes escenarios cambiando el valor retornado.

## Sintaxis
```java
when(mock.metodo()).thenReturn(valor);
when(mock.metodo(args)).thenReturn(valor);
```

## Ejemplos

### Retorno simple
```java
List<String> mockList = mock(List.class);
when(mockList.size()).thenReturn(5);

assertEquals(5, mockList.size());
```

### Retorno de objeto
```java
when(userRepository.findById(1)).thenReturn(new User(1, "Juan"));

User user = userRepository.findById(1);
assertEquals("Juan", user.getName());
```

### Múltiples retornos consecutivos
```java
when(mock.getNext())
    .thenReturn("primero")
    .thenReturn("segundo")
    .thenReturn("tercero");

assertEquals("primero", mock.getNext()); // Primera llamada
assertEquals("segundo", mock.getNext()); // Segunda llamada
assertEquals("tercero", mock.getNext()); // Tercera y siguientes
assertEquals("tercero", mock.getNext()); // Sigue devolviendo el último
```

### Retorno condicional por argumento
```java
when(calculator.multiply(2, 3)).thenReturn(6);
when(calculator.multiply(5, 5)).thenReturn(25);

assertEquals(6, calculator.multiply(2, 3));
assertEquals(25, calculator.multiply(5, 5));
```

## Palabras clave
- thenReturn
- Stubbing
- Valor de retorno
- Mock response
- when().thenReturn()

## Comparaciones típicas
- vs [[Mockito - when()]]: `when(...).thenReturn(...)` es el combo típico para stubear retornos.
- vs [[Mockito - thenThrow()]]: `thenReturn` simula éxito/respuesta normal; `thenThrow` simula error/excepción.

## Preguntas de examen
- ¿Para qué sirve `thenReturn()` en Mockito?
- ¿Cómo se configuran múltiples retornos consecutivos?
- ¿Qué pasa si se llama al método más veces que los retornos configurados?

## Errores comunes
- Configurar `thenReturn(null)` cuando el método espera un primitivo (causa NullPointerException).
- Olvidar que el valor configurado se aplica solo para los argumentos exactos especificados.
- No configurar retorno y esperar que el mock devuelva algo útil (devuelve null por default).

## Mini-ejemplo (mental)
`thenReturn()` es como programar una máquina expendedora. Le decís: "Cuando aprieten el botón A1, entregá una gaseosa". La máquina no produce la gaseosa, solo la entrega cuando se la piden. Si no programaste el botón A2, no entrega nada (null).
