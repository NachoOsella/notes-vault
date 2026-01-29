# Testing - Writing tests

## Definición
Writing tests se refiere al proceso de escribir pruebas en JUnit, utilizando anotaciones y métodos de aserción para definir el comportamiento esperado del código bajo prueba.

## Explicación
- *Qué problema resuelve*
    Proporciona una estructura estandarizada para escribir, organizar y ejecutar pruebas automatizadas de forma consistente.
- *Cómo funciona por arriba*
    Se crean clases de prueba con métodos anotados con `@Test`. Dentro de cada método se usa el patrón Arrange-Act-Assert y se verifican resultados con `assertEquals`, `assertTrue`, etc.
- *Qué implica / qué permite*
    Permite automatizar la verificación del código, ejecutar pruebas con Maven/Gradle y obtener retroalimentación inmediata sobre el estado del software.

## Ejemplo básico
```java
class CalculatorTest {
    @Test
    void testAdd() {
        Calculator calculator = new Calculator();
        int result = calculator.add(2, 3);
        assertEquals(5, result);
    }
    
    @Test
    void testSubtract() {
        Calculator calculator = new Calculator();
        int result = calculator.subtract(5, 3);
        assertEquals(2, result);
    }
}
```

## Anotaciones principales de JUnit 5

### @Test
Identifica un método como prueba. El método debe contener aserciones que verifican el resultado esperado.
```java
@Test
void miPrueba() {
    // Si una aserción falla, el test falla
    assertEquals(esperado, actual);
}
```

### @DisplayName
Da un nombre legible al método de prueba para los reportes. Acepta caracteres Unicode y espacios.
```java
@Test
@DisplayName("Debería sumar dos números correctamente")
void testAdd() { ... }
```

### @BeforeEach
Se ejecuta **antes de cada método de prueba**. Útil para configurar el estado inicial.
```java
@BeforeEach
void setUp() {
    calculator = new Calculator();
}
```

### @AfterEach
Se ejecuta **después de cada método de prueba**. Útil para liberar recursos.
```java
@AfterEach
void tearDown() {
    calculator = null;
}
```

### @BeforeAll
Se ejecuta **una sola vez antes de todos los tests** de la clase. El método debe ser `static`.
```java
@BeforeAll
static void initAll() {
    // Inicialización costosa que se hace una sola vez
}
```

### @AfterAll
Se ejecuta **una sola vez después de todos los tests** de la clase. El método debe ser `static`.
```java
@AfterAll
static void tearDownAll() {
    // Limpieza final
}
```

### @Tag
Permite etiquetar pruebas para agruparlas y ejecutar subconjuntos.
```java
@Tag("fast")
class MyFastTests { ... }

// O a nivel de método:
@Test
@Tag("slow")
void testLento() { ... }
```

### @Disabled
Deshabilita temporalmente una prueba sin eliminarla del código.
```java
@Test
@Disabled("Bug pendiente de resolver")
void testDeshabilitado() { ... }
```

## Estructura de una clase de test estándar
```java
class MyClassTest {
    
    private MyClass myClass;
    
    @BeforeAll
    static void initAll() {
        // Inicialización global (una vez)
    }
    
    @BeforeEach
    void setUp() {
        myClass = new MyClass();
    }
    
    @Test
    @DisplayName("Debería hacer X cuando Y")
    void testMetodo() {
        // Arrange - ya hecho en setUp
        // Act
        var result = myClass.metodo();
        // Assert
        assertEquals(esperado, result);
    }
    
    @AfterEach
    void tearDown() {
        myClass = null;
    }
    
    @AfterAll
    static void tearDownAll() {
        // Limpieza global (una vez)
    }
}
```

## Palabras clave
- @Test
- @DisplayName
- @BeforeEach
- @AfterEach
- @BeforeAll
- @AfterAll
- @Tag
- @Disabled
- Aserciones
- assertEquals

## Comparaciones típicas
- vs [[Testing - Tests unitarios]]: writing tests se enfoca en el "cómo" (estructura, anotaciones); unit tests define el "qué" (concepto general).
- vs [[Mockito - when()]]: writing tests define el flujo del test; `when(...).then...` sirve para stubear dependencias dentro del test.

## Preguntas de examen
- ¿Qué anotación se usa para marcar un método como prueba en JUnit?
- ¿Cuál es la diferencia entre `@BeforeEach` y `@BeforeAll`?
- ¿Para qué sirve la anotación `@DisplayName`?
- ¿Cómo se deshabilita temporalmente una prueba en JUnit?
- ¿Qué permite hacer la anotación `@Tag`?

## Errores comunes
- Olvidar que `@BeforeAll` y `@AfterAll` requieren métodos `static`.
- No usar `@BeforeEach` para inicializar objetos, causando dependencias entre tests.
- Confundir `@BeforeEach` (se ejecuta antes de cada test) con `@BeforeAll` (se ejecuta una sola vez).
- Usar `@Disabled` como solución permanente en vez de arreglar el test.

## Mini-ejemplo (mental)
Pensá en `@BeforeEach` como preparar la mesa antes de cada comida (cada test empieza con platos limpios). `@BeforeAll` es como hacer las compras una vez para toda la semana. `@AfterEach` es lavar los platos después de comer, y `@AfterAll` es la limpieza profunda del domingo.
