# Mockito - @InjectMocks

## Definición
La anotación `@InjectMocks` crea una instancia de la clase bajo prueba e inyecta automáticamente los mocks y spies (creados con `@Mock` y `@Spy`) en sus dependencias.

## Explicación
- *Qué problema resuelve*
    Automatiza la inyección de dependencias mockeadas en el objeto que queremos testear, evitando tener que hacerlo manualmente.
- *Cómo funciona por arriba*
    Mockito busca en la clase anotada con `@InjectMocks` los campos que coincidan con los mocks/spies disponibles y los inyecta por constructor, setter o campo directo.
- *Qué implica / qué permite*
    - Simplifica la configuración de tests.
    - Reduce código boilerplate.
    - Mockito resuelve las dependencias automáticamente.

## Ejemplo
```java
@ExtendWith(MockitoExtension.class)
class MyServiceTest {
    
    @Mock
    private Repository repository;  // Dependencia mockeada
    
    @Mock
    private EmailService emailService;  // Otra dependencia mockeada
    
    @InjectMocks
    private MyService myService;  // Objeto bajo test
    
    @Test
    void testProcess() {
        // Los mocks ya están inyectados en myService
        when(repository.findAll()).thenReturn(List.of(new Entity()));
        
        myService.process();
        
        verify(repository).findAll();
        verify(emailService).sendNotification(any());
    }
}
```

## Algoritmo de inyección de Mockito
Mockito intenta inyectar en este orden:
1. **Constructor**: Busca un constructor que acepte los mocks.
2. **Setter**: Busca setters que coincidan con los tipos de los mocks.
3. **Campo directo**: Inyecta directamente en los campos (usa reflection).

## Limitaciones importantes
- **Solo funciona con instancias de clase**, no con objetos creados con `new` dentro del test.
- No siempre se garantiza que se usen las mismas instancias de mocks en todas las pruebas.
- Si hay múltiples mocks del mismo tipo, Mockito puede confundirse.

## Palabras clave
- @InjectMocks
- Inyección de dependencias
- Objeto bajo test
- Autowiring de mocks
- Constructor injection

## Comparaciones típicas
- vs [[14 - Mockito - mock() y @Mock]]: `@Mock` crea dependencias falsas; `@InjectMocks` crea el objeto bajo test e inyecta esas dependencias.
- vs [[22 - Reflection - Concepto]]: la inyección de Mockito usa reflection internamente para acceder a constructores/campos/setters.

## Preguntas de examen
- ¿Qué hace la anotación `@InjectMocks`?
- ¿En qué orden intenta Mockito inyectar los mocks?
- ¿Qué limitaciones tiene `@InjectMocks`?

## Errores comunes
- Usar `@InjectMocks` en una interfaz (debe ser una clase concreta).
- Tener múltiples mocks del mismo tipo sin diferenciarlos (Mockito puede inyectar el incorrecto).
- Olvidar que `@InjectMocks` crea una nueva instancia (no usar junto con `new`).
- No usar `@ExtendWith(MockitoExtension.class)` o `MockitoAnnotations.openMocks(this)`.

## Mini-ejemplo (mental)
`@InjectMocks` es como un armador de muebles IKEA automatizado. Le das las piezas sueltas (los `@Mock`) y él arma el mueble completo (el objeto bajo test) conectando cada pieza donde corresponde. Vos solo tenés que darle las piezas correctas y él hace el trabajo de ensamblado.
