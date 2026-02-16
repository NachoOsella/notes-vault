# Mockito - verify()

## Definición
El método `verify()` se utiliza para comprobar que un método de un mock o spy fue llamado durante la ejecución del test, opcionalmente verificando cuántas veces y con qué argumentos.

## Explicación
- *Qué problema resuelve*
    Permite validar que el código bajo prueba interactúa correctamente con sus dependencias, verificando que se llaman los métodos esperados.
- *Cómo funciona por arriba*
    Después de ejecutar el código bajo prueba, se usa `verify(mock).metodo()` para confirmar que el método fue invocado. Mockito registra todas las llamadas internamente.
- *Qué implica / qué permite*
    - Verificar que se llamó a un método específico.
    - Verificar cuántas veces se llamó.
    - Verificar con qué argumentos se llamó.
    - Verificar que un método nunca fue llamado.

## Sintaxis básica
```java
verify(mock).metodo();
verify(mock, times(n)).metodo();
verify(mock, never()).metodo();
verify(mock, atLeast(n)).metodo();
verify(mock, atMost(n)).metodo();
```

## Ejemplos

### Verificar que se llamó una vez (default)
```java
@Test
void testSave() {
    myService.saveUser(new User("Juan"));
    
    verify(userRepository).save(any(User.class));
}
```

### Verificar número exacto de llamadas
```java
verify(mock, times(3)).metodo(); // Exactamente 3 veces
verify(mock, times(1)).metodo(); // Equivalente a verify(mock).metodo()
```

### Verificar que nunca se llamó
```java
verify(emailService, never()).sendEmail(any());
```

### Verificar rango de llamadas
```java
verify(mock, atLeast(2)).metodo();  // Al menos 2 veces
verify(mock, atMost(5)).metodo();   // Como máximo 5 veces
verify(mock, atLeastOnce()).metodo(); // Al menos una vez
```

### Verificar argumentos específicos
```java
verify(calculator).add(2, 3); // Verifica que se llamó con estos argumentos exactos
verify(userRepository).save(argThat(user -> user.getName().equals("Juan")));
```

### Ejemplo completo
```java
@Test
void testProcess() {
    Calculator calculator = mock(Calculator.class);
    when(calculator.add(2, 3)).thenReturn(5);
    
    // Act
    int result = calculator.add(2, 3);
    
    // Assert valor
    assertEquals(5, result);
    
    // Verify interacción
    verify(calculator).add(2, 3);
    verify(calculator, times(1)).add(anyInt(), anyInt());
}
```

## Palabras clave
- verify
- Verificación de interacciones
- times()
- never()
- atLeast()
- atMost()
- Argument matchers

## Comparaciones típicas
- vs [[17 - Mockito - when()]]: `when/then...` define comportamiento del mock **antes**; `verify` valida llamadas **después**.
- vs [[12 - Testing - Tests unitarios]]: verify es útil en unit tests orientados a interacción (verificar colaboradores) más que a estado (verificar resultado).

## Preguntas de examen
- ¿Para qué sirve `verify()` en Mockito?
- ¿Cómo se verifica que un método fue llamado exactamente N veces?
- ¿Cómo se verifica que un método nunca fue llamado?
- ¿Cuál es la diferencia entre `times(1)` y no especificar cantidad?

## Errores comunes
- Llamar a `verify()` antes de ejecutar el código bajo prueba (no hay nada que verificar).
- Confundir stubbing (`when`) con verificación (`verify`): stubbing va antes, verify va después.
- Verificar demasiado: no es necesario verificar cada llamada, solo las relevantes para el test.
- Usar `verify()` como sustituto de aserciones de estado (ambos son complementarios).

## Mini-ejemplo (mental)
`verify()` es como revisar las cámaras de seguridad después de un evento. No cambia lo que pasó, solo te permite confirmar: "¿La persona entró por la puerta principal?" (verify llamada), "¿Cuántas veces pasó por el pasillo?" (times(n)), "¿Nunca tocó la caja fuerte?" (never()).
