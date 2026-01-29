# ReflectionSupport (JUnit)

## Definición
`ReflectionSupport` es una clase utilitaria del paquete `org.junit.platform.commons.support` que proporciona métodos para trabajar con reflection de manera simplificada en el contexto de pruebas unitarias con JUnit.

## Explicación
- *Qué problema resuelve*
    Simplifica el uso de reflection en tests, proporcionando métodos de alto nivel para invocar métodos privados, acceder a campos privados, etc.
- *Cómo funciona por arriba*
    Ofrece métodos estáticos como `findMethod()`, `invokeMethod()`, `findField()`, `getFieldValue()` que encapsulan la complejidad de la API de reflection de Java.
- *Qué implica / qué permite*
    - Testear métodos privados sin escribir código de reflection manual.
    - Acceder y modificar campos privados fácilmente.
    - Código de test más limpio y legible.

## Métodos principales

### findMethod()
Busca un método en una clase por nombre y tipos de parámetros.
```java
Optional<Method> metodo = ReflectionSupport.findMethod(
    MiClase.class, 
    "metodoPrivado", 
    String.class  // tipos de parámetros (opcional)
);
```
- **Retorna**: `Optional<Method>` (puede estar vacío si no encuentra el método).

### invokeMethod()
Invoca un método en una instancia de una clase.
```java
Object resultado = ReflectionSupport.invokeMethod(
    metodo,      // Method obtenido con findMethod
    instancia,   // objeto sobre el que invocar
    "argumento"  // argumentos del método (varargs)
);
```
- **Retorna**: El resultado de la invocación (o `null` si es void).

### findField()
Busca un campo en una clase por nombre.
```java
Optional<Field> campo = ReflectionSupport.findField(
    MiClase.class,
    "campoPrivado"
);
```
- **Retorna**: `Optional<Field>`.

### getFieldValue()
Obtiene el valor de un campo en una instancia.
```java
Object valor = ReflectionSupport.getFieldValue(
    campo,       // Field obtenido con findField
    instancia    // objeto del que obtener el valor
);
```

### setFieldValue() (no estándar, pero útil)
Para establecer valores, se puede usar:
```java
Field field = findField(MiClase.class, "campo").orElseThrow();
field.setAccessible(true);
field.set(instancia, nuevoValor);
```

## Ejemplo completo: Invocar método privado
```java
@Test
void testMetodoPrivado() throws Exception {
    MiClase instancia = new MiClase();
    
    // Buscar el método privado
    Method metodo = ReflectionSupport
        .findMethod(MiClase.class, "metodoPrivado")
        .orElseThrow();
    
    // Invocar el método
    Object resultado = ReflectionSupport.invokeMethod(metodo, instancia);
    
    // Verificar resultado
    assertEquals(valorEsperado, resultado);
}
```

## Ejemplo completo: Obtener campo privado
```java
@Test
void testCampoPrivado() {
    MiClase instancia = new MiClase();
    
    // Buscar el campo
    Field campo = ReflectionSupport
        .findField(MiClase.class, "campoPrivado")
        .orElseThrow();
    
    // Obtener valor
    Object valor = ReflectionSupport.getFieldValue(campo, instancia);
    
    assertEquals(valorEsperado, valor);
}
```

## Palabras clave
- ReflectionSupport
- findMethod
- invokeMethod
- findField
- getFieldValue
- Optional
- org.junit.platform.commons.support

## Comparaciones típicas
- vs [[Reflection - Concepto]]: ReflectionSupport es una utilidad que simplifica reflection; el concepto es el mecanismo base de Java.
- vs [[Testing - Writing tests]]: ReflectionSupport aparece para casos especiales (métodos privados); writing tests cubre el caso normal con métodos públicos.

## Preguntas de examen
- ¿Para qué sirve la clase `ReflectionSupport` de JUnit?
- ¿Qué método se usa para buscar un método privado?
- ¿Qué retorna `findMethod()` si no encuentra el método?
- ¿Cómo se invoca un método privado usando `ReflectionSupport`?

## Errores comunes
- No manejar el `Optional` vacío cuando el método/campo no existe.
- Olvidar que `findMethod` requiere especificar los tipos de parámetros si el método los tiene.
- Confundir `findMethod` (busca) con `invokeMethod` (ejecuta).
- No tener la dependencia correcta de JUnit Platform en el proyecto.

## Mini-ejemplo (mental)
`ReflectionSupport` es como un kit de herramientas profesional para cerrajeros (testers). En vez de fabricar tu propia ganzúa (escribir código de reflection), usás herramientas pre-hechas: `findMethod` es el detector de cerraduras (encuentra el método), `invokeMethod` es la ganzúa (abre la cerradura/ejecuta el método). Es más seguro y rápido que hacerlo a mano.
