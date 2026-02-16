# Mockito - thenThrow()

## Definición
El método `thenThrow()` se utiliza para configurar un mock de manera que lance una excepción cuando se llama a un método específico. Se encadena después de `when()`.

## Explicación
- *Qué problema resuelve*
    Permite simular escenarios de error sin depender de condiciones reales que causen la excepción (conexión fallida, archivo no encontrado, etc.).
- *Cómo funciona por arriba*
    Cuando el método configurado es invocado, Mockito intercepta la llamada y lanza la excepción especificada en lugar de ejecutar código real.
- *Qué implica / qué permite*
    - Testear el manejo de errores del código.
    - Simular fallas de dependencias externas.
    - Verificar que el código responde correctamente ante excepciones.

## Sintaxis
```java
when(mock.metodo()).thenThrow(new MiExcepcion());
when(mock.metodo()).thenThrow(MiExcepcion.class);
```

## Ejemplos

### Lanzar excepción simple
```java
List<String> mockList = mock(List.class);
when(mockList.get(0)).thenThrow(new IndexOutOfBoundsException("Índice inválido"));

assertThrows(IndexOutOfBoundsException.class, () -> mockList.get(0));
```

### Lanzar excepción por clase
```java
when(repository.findById(anyInt())).thenThrow(EntityNotFoundException.class);
```

### Secuencia: éxito y luego error
```java
when(service.connect())
    .thenReturn(true)      // Primera llamada: éxito
    .thenReturn(true)      // Segunda llamada: éxito
    .thenThrow(new ConnectionException()); // Tercera: falla

assertTrue(service.connect());  // OK
assertTrue(service.connect());  // OK
assertThrows(ConnectionException.class, () -> service.connect()); // Error
```

### Testear manejo de excepciones
```java
@Test
void testHandleError() {
    when(externalService.call()).thenThrow(new ServiceException());
    
    // Verificar que nuestro código maneja la excepción correctamente
    Result result = myService.process();
    
    assertEquals(Status.FAILED, result.getStatus());
    assertNotNull(result.getErrorMessage());
}
```

## Palabras clave
- thenThrow
- Excepción
- Manejo de errores
- Escenarios de falla
- Edge cases

## Comparaciones típicas
- vs [[18 - Mockito - thenReturn()]]: `thenThrow` simula fallas/excepciones; `thenReturn` simula respuestas normales/exitosas.
- vs [[20 - Mockito - doNothing()]]: para métodos `void`, en vez de `thenThrow` se usa `doThrow().when(mock).metodo()`.

## Preguntas de examen
- ¿Para qué sirve `thenThrow()` en Mockito?
- ¿Cómo se testea que el código maneje correctamente una excepción?
- ¿Cuál es la diferencia entre pasar una instancia de excepción y pasar la clase?

## Errores comunes
- Lanzar checked exceptions en métodos que no las declaran (causa error de compilación).
- Usar `when().thenThrow()` con métodos void (usar `doThrow().when()` en su lugar).
- No verificar que el código realmente maneja la excepción (el test pasa pero el código no es robusto).

## Mini-ejemplo (mental)
`thenThrow()` es como simular un corte de luz en un ensayo de emergencia. En vez de esperar a que realmente se corte la luz, le decís al sistema: "Cuando intentes encender la luz, actuá como si no hubiera electricidad". Así podés verificar que las linternas de emergencia funcionan sin depender de un corte real.
