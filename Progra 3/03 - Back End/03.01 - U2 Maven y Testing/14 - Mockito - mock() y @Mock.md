# Mockito - mock() y @Mock

## Definición
Un **mock** es un objeto simulado que se utiliza en lugar de un objeto real para aislar la funcionalidad que se está probando y controlar el comportamiento de dependencias externas.

## Explicación
- *Qué problema resuelve*
    Permite aislar el código bajo prueba de sus dependencias (bases de datos, servicios web, etc.), haciendo los tests más rápidos, predecibles y enfocados.
- *Cómo funciona por arriba*
    Se crea un objeto simulado con `mock()` o `@Mock`. Este objeto no ejecuta el código real, sino que permite definir qué debe devolver cuando se llaman sus métodos.
- *Qué implica / qué permite*
    - Simular objetos que aún no existen.
    - Probar código sin depender de recursos externos.
    - Controlar el comportamiento de las dependencias.
    - Verificar interacciones (qué métodos se llamaron y con qué argumentos).

## Formas de crear un mock

### Con @Mock (recomendado)
La anotación se coloca sobre una variable de instancia. Mockito crea el mock automáticamente.
```java
@Mock
private MyDependency myDependency;

@BeforeEach
void setUp() {
    MockitoAnnotations.openMocks(this);
}
```

### Con mock()
Se usa el método estático `Mockito.mock()` pasando la clase o interfaz.
```java
MyDependency myDependency = mock(MyDependency.class);
```

## Proceso de uso de Mockito
1. **Crear el mock**: Con `mock()` o `@Mock`.
2. **Definir comportamiento**: Con `when(...).thenReturn(...)` o `when(...).thenThrow(...)`.
3. **Verificar interacciones**: Con `verify(mock).metodo()`.

## Ejemplo completo
```java
@ExtendWith(MockitoExtension.class)
class MyServiceTest {
    
    @Mock
    private Repository repository;
    
    @InjectMocks
    private MyService myService;
    
    @Test
    void testGetData() {
        // Arrange - definir comportamiento del mock
        when(repository.findById(1)).thenReturn(new Entity(1, "Test"));
        
        // Act
        Entity result = myService.getById(1);
        
        // Assert
        assertEquals("Test", result.getName());
        verify(repository).findById(1);
    }
}
```

## Palabras clave
- Mock
- Objeto simulado
- Aislamiento
- Dependencias
- @Mock
- mock()
- Stubbing

## Comparaciones típicas
- vs [[15 - Mockito - spy() y @Spy]]: mock reemplaza todo el comportamiento (métodos devuelven null/0/false por default); spy envuelve un objeto real y podés stubear solo partes.
- vs [[16 - Mockito - @InjectMocks]]: `@Mock` crea dependencias falsas; `@InjectMocks` crea el objeto bajo test e inyecta esos mocks automáticamente.

## Preguntas de examen
- ¿Qué es un mock y para qué se utiliza?
- ¿Cuáles son las dos formas de crear un mock en Mockito?
- ¿Qué diferencia hay entre `@Mock` y `mock()`?
- ¿Por qué es importante aislar dependencias en pruebas unitarias?

## Errores comunes
- Olvidar inicializar los mocks con `MockitoAnnotations.openMocks(this)` o `@ExtendWith(MockitoExtension.class)`.
- No definir el comportamiento del mock: por defecto los métodos devuelven `null`, `0` o `false`.
- Mockear clases finales o métodos estáticos sin configuración adicional (requiere mockito-inline).
- Usar mocks cuando no son necesarios (si la dependencia es simple, a veces es mejor usar el objeto real).

## Mini-ejemplo (mental)
Un mock es como un actor de reparto en una película. En vez de traer al presidente real para una escena, usás un actor que "hace de" presidente. El actor sigue el guión que le das (el stubbing) y después podés verificar si dijo sus líneas correctamente (verify).
