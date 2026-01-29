# Preguntas - BE U2

## Maven

### Conceptos básicos
- ¿Qué es Maven y cuál es su propósito principal?
- ¿Qué es un archivo `pom.xml` y qué información contiene?
- ¿Cómo maneja Maven las dependencias de un proyecto?

### Archivos de configuración
- ¿Cuál es la función principal del archivo `pom.xml` en un proyecto Maven?
- ¿Dónde se encuentra típicamente el archivo `settings.xml` y qué propósito sirve?
- ¿Cómo se definen las dependencias en un proyecto Maven?

### Ciclo de vida
- ¿Cuáles son las fases principales del ciclo de vida de Maven y qué hace cada una?
- ¿Cómo se relacionan los plugins con las fases del ciclo de vida de Maven?

### Plugins
- ¿Qué es un plugin en Maven y cuál es su propósito?
- ¿Cómo se configura un plugin en el archivo `pom.xml`?

### Gestión de dependencias
- ¿Cómo se declaran las dependencias en un proyecto Maven?
- ¿Qué son las dependencias transitivas y cómo se gestionan en Maven?
- ¿Cuál es la diferencia entre una dependencia y un plugin en Maven?

### Archetype
- ¿Qué es un archetype en Maven y cuál es su propósito?
- ¿Cómo se utiliza un archetype para crear un nuevo proyecto en Maven?

### Instalación
- ¿Cuáles son los pasos básicos para instalar Maven en un sistema?
- ¿Qué variables de entorno son necesarias para que Maven funcione correctamente?

---

## Testing

### Introducción y fundamentos
- ¿Qué es el testing y cuál es su objetivo principal?
- ¿Cuáles son las herramientas de testing más populares en Java?
- ¿Cuáles son los principales tipos de testing y en qué etapa se aplican?
- ¿Qué características debe tener una buena prueba?
- ¿Cuál es la diferencia entre pruebas unitarias y pruebas de integración?
- ¿Qué son las pruebas de regresión y por qué son importantes?

### Tests unitarios
- ¿Qué es el testing unitario y cuál es su objetivo?
- ¿Cuál es la diferencia entre JUnit y Mockito?
- ¿Por qué es importante aislar las dependencias en pruebas unitarias?
- ¿Qué significa el patrón Arrange-Act-Assert?

### Writing tests (JUnit)
- ¿Qué anotación se usa para marcar un método como prueba en JUnit?
- ¿Cuál es la diferencia entre `@BeforeEach` y `@BeforeAll`?
- ¿Para qué sirve la anotación `@DisplayName`?
- ¿Cómo se deshabilita temporalmente una prueba en JUnit?
- ¿Qué permite hacer la anotación `@Tag`?

---

## Mockito

### mock() y @Mock
- ¿Qué es un mock y para qué se utiliza?
- ¿Cuáles son las dos formas de crear un mock en Mockito?
- ¿Qué diferencia hay entre `@Mock` y `mock()`?

### spy() y @Spy
- ¿Qué es un spy en Mockito y cómo difiere de un mock?
- ¿Cuándo conviene usar un spy en lugar de un mock?
- ¿Por qué se recomienda usar `doReturn()` en vez de `when()` con spies?

### @InjectMocks
- ¿Qué hace la anotación `@InjectMocks`?
- ¿En qué orden intenta Mockito inyectar los mocks?
- ¿Qué limitaciones tiene `@InjectMocks`?

### when() y stubbing
- ¿Para qué sirve el método `when()` en Mockito?
- ¿Cómo se configura un mock para que lance una excepción?
- ¿Qué son los argument matchers y cuándo se usan?

### thenReturn() y thenThrow()
- ¿Para qué sirve `thenReturn()` en Mockito?
- ¿Cómo se configuran múltiples retornos consecutivos?
- ¿Para qué sirve `thenThrow()` en Mockito?

### doNothing()
- ¿Para qué sirve `doNothing()` en Mockito?
- ¿Por qué no se puede usar `when().thenReturn()` con métodos void?

### verify()
- ¿Para qué sirve `verify()` en Mockito?
- ¿Cómo se verifica que un método fue llamado exactamente N veces?
- ¿Cómo se verifica que un método nunca fue llamado?

---

## Reflection

### Concepto
- ¿Qué es Reflection y para qué se utiliza?
- ¿Por qué se considera mala práctica usar reflection para acceder a miembros privados?
- ¿Cómo se accede a un método privado usando reflection?
- ¿Qué método se usa para permitir el acceso a miembros privados?

### ReflectionSupport (JUnit)
- ¿Para qué sirve la clase `ReflectionSupport` de JUnit?
- ¿Qué método se usa para buscar un método privado?
- ¿Qué retorna `findMethod()` si no encuentra el método?
- ¿Cómo se invoca un método privado usando `ReflectionSupport`?

---

## Respuestas rápidas

### ¿Qué es un mock?
Un objeto simulado que reemplaza una dependencia real para aislar el código bajo prueba.

### ¿Qué es un spy?
Un objeto que envuelve un objeto real, permitiendo stubear métodos específicos mientras mantiene el comportamiento real para el resto.

### ¿Diferencia mock vs spy?
- **Mock**: No ejecuta código real, todo es simulado.
- **Spy**: Ejecuta código real por defecto, solo simula lo que se stubea explícitamente.

### ¿Para qué sirve @InjectMocks?
Crea una instancia de la clase bajo prueba e inyecta automáticamente los mocks creados con @Mock.

### ¿Diferencia when() vs verify()?
- **when()**: Configura comportamiento **antes** de ejecutar el test.
- **verify()**: Valida interacciones **después** de ejecutar el test.

### ¿Qué es Reflection?
Técnica de Java para inspeccionar y manipular clases/objetos en tiempo de ejecución, incluyendo miembros privados.
