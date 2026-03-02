# Preguntas - BE U2

## Maven

- ¿Qué es Maven y cuál es su propósito principal?
- ¿Qué es un archivo `pom.xml` y qué información contiene?
- ¿Cómo maneja Maven las dependencias de un proyecto?

## Maven - Archivos de configuración
- ¿Cuál es la función principal del archivo `pom.xml` en un proyecto Maven?
- ¿Dónde se encuentra típicamente el archivo `settings.xml` y qué propósito sirve?
- ¿Cómo se definen las dependencias en un proyecto Maven?

## Maven - Ciclo de vida
- ¿Cuáles son las fases principales del ciclo de vida de Maven y qué hace cada una?
- ¿Cómo se relacionan los plugins con las fases del ciclo de vida de Maven?

## Maven - Plugins
- ¿Qué es un plugin en Maven y cuál es su propósito?
- ¿Cómo se configura un plugin en el archivo `pom.xml`?

## Maven - Gestión de dependencias
- ¿Cómo se declaran las dependencias en un proyecto Maven?
- ¿Qué son las dependencias transitivas y cómo se gestionan en Maven?
- ¿Cuál es la diferencia entre una dependencia y un plugin en Maven?

## Maven - Archetype
- ¿Qué es un archetype en Maven y cuál es su propósito?
- ¿Cómo se utiliza un archetype para crear un nuevo proyecto en Maven?

## Maven - Instalación
- ¿Cuáles son los pasos básicos para instalar Maven en un sistema?
- ¿Qué variables de entorno son necesarias para que Maven funcione correctamente?

## Testing

## Testing - Introducción y fundamentos
- ¿Qué es el testing y cuál es su objetivo principal?
- ¿Cuáles son las herramientas de testing más populares en Java?
- ¿Cuáles son los principales tipos de testing y en qué etapa se aplican?
- ¿Qué características debe tener una buena prueba?
- ¿Cuál es la diferencia entre pruebas unitarias y pruebas de integración?
- ¿Qué son las pruebas de regresión y por qué son importantes?

## Testing - Tests unitarios
- ¿Qué es el testing unitario y cuál es su objetivo?
- ¿Cuál es la diferencia entre JUnit y Mockito?
- ¿Por qué es importante aislar las dependencias en pruebas unitarias?
- ¿Qué significa el patrón Arrange-Act-Assert?

## Testing - Writing tests (JUnit)
- ¿Qué anotación se usa para marcar un método como prueba en JUnit?
- ¿Cuál es la diferencia entre `@BeforeEach` y `@BeforeAll`?
- ¿Para qué sirve la anotación `@DisplayName`?
- ¿Cómo se deshabilita temporalmente una prueba en JUnit?
- ¿Qué permite hacer la anotación `@Tag`?

## Mockito

## Mockito - mock() y @Mock
- ¿Qué es un mock y para qué se utiliza?
- ¿Cuáles son las dos formas de crear un mock en Mockito?
- ¿Qué diferencia hay entre `@Mock` y `mock()`?

## Mockito - spy() y @Spy
- ¿Qué es un spy en Mockito y cómo difiere de un mock?
- ¿Cuándo conviene usar un spy en lugar de un mock?
- ¿Por qué se recomienda usar `doReturn()` en vez de `when()` con spies?

## Mockito - @InjectMocks
- ¿Qué hace la anotación `@InjectMocks`?
- ¿En qué orden intenta Mockito inyectar los mocks?
- ¿Qué limitaciones tiene `@InjectMocks`?

## Mockito - when() y stubbing
- ¿Para qué sirve el método `when()` en Mockito?
- ¿Cómo se configura un mock para que lance una excepción?
- ¿Qué son los argument matchers y cuándo se usan?

## Mockito - thenReturn() y thenThrow()
- ¿Para qué sirve `thenReturn()` en Mockito?
- ¿Cómo se configuran múltiples retornos consecutivos?
- ¿Para qué sirve `thenThrow()` en Mockito?

## Mockito - doNothing()
- ¿Para qué sirve `doNothing()` en Mockito?
- ¿Por qué no se puede usar `when().thenReturn()` con métodos void?

## Mockito - verify()
- ¿Para qué sirve `verify()` en Mockito?
- ¿Cómo se verifica que un método fue llamado exactamente N veces?
- ¿Cómo se verifica que un método nunca fue llamado?

## Reflection

## Reflection - Concepto
- ¿Qué es Reflection y para qué se utiliza?
- ¿Por qué se considera mala práctica usar reflection para acceder a miembros privados?
- ¿Cómo se accede a un método privado usando reflection?
- ¿Qué método se usa para permitir el acceso a miembros privados?

## Reflection - ReflectionSupport (JUnit)
- ¿Para qué sirve la clase `ReflectionSupport` de JUnit?
- ¿Qué método se usa para buscar un método privado?
- ¿Qué retorna `findMethod()` si no encuentra el método?
- ¿Cómo se invoca un método privado usando `ReflectionSupport`?

## Respuestas (opcional)

### ¿Qué es Maven y cuál es su propósito principal?
Respuesta: Maven es una herramienta de build y gestión de proyectos Java; su objetivo es estandarizar compilación, tests, empaquetado y dependencias.

### ¿Qué es un archivo `pom.xml` y qué información contiene?
Respuesta: Es el descriptor del proyecto Maven; define coordenadas (`groupId`, `artifactId`, `version`), dependencias, plugins y configuración del build.

### ¿Cómo maneja Maven las dependencias de un proyecto?
Respuesta: Las resuelve desde repositorios usando lo declarado en `pom.xml`, incluyendo transitivas y su alcance (`scope`).

### ¿Cuál es la función principal del archivo `pom.xml` en un proyecto Maven?
Respuesta: Centralizar la configuración del proyecto y decirle a Maven qué construir, con qué dependencias y con qué plugins.

### ¿Dónde se encuentra típicamente el archivo `settings.xml` y qué propósito sirve?
Respuesta: Suele estar en `~/.m2/settings.xml` (o en `${MAVEN_HOME}/conf` global); configura repositorios, mirrors, proxies y credenciales del usuario.

### ¿Cómo se definen las dependencias en un proyecto Maven?
Respuesta: Dentro de `<dependencies>` en `pom.xml`, indicando al menos `groupId`, `artifactId`, `version` y opcionalmente `scope`.

### ¿Cuáles son las fases principales del ciclo de vida de Maven y qué hace cada una?
Respuesta: Las más usadas son `validate`, `compile`, `test`, `package`, `verify`, `install` y `deploy`; cada una avanza el proceso hasta publicar artefactos.

### ¿Cómo se relacionan los plugins con las fases del ciclo de vida de Maven?
Respuesta: Los plugins aportan goals que se enlazan a fases; al ejecutar una fase, Maven dispara automáticamente los goals asociados.

### ¿Qué es un plugin en Maven y cuál es su propósito?
Respuesta: Es un componente que extiende Maven para ejecutar tareas concretas (compilar, testear, empaquetar, generar reportes, etc.).

### ¿Cómo se configura un plugin en el archivo `pom.xml`?
Respuesta: En la sección `<build><plugins>`, declarando el plugin y, si hace falta, `<configuration>` y `<executions>`.

### ¿Cómo se declaran las dependencias en un proyecto Maven?
Respuesta: Se agregan como entradas `<dependency>` en `pom.xml` con sus coordenadas y alcance.

### ¿Qué son las dependencias transitivas y cómo se gestionan en Maven?
Respuesta: Son dependencias de tus dependencias; Maven las incluye automáticamente y podés controlarlas con `exclusions` o `dependencyManagement`.

### ¿Cuál es la diferencia entre una dependencia y un plugin en Maven?
Respuesta: La dependencia la usa tu aplicación/código; el plugin lo usa Maven durante el proceso de build.

### ¿Qué es un archetype en Maven y cuál es su propósito?
Respuesta: Es una plantilla de proyecto que genera una estructura inicial estándar con archivos base.

### ¿Cómo se utiliza un archetype para crear un nuevo proyecto en Maven?
Respuesta: Con comandos como `mvn archetype:generate`, eligiendo archetype y datos del proyecto (`groupId`, `artifactId`, etc.).

### ¿Cuáles son los pasos básicos para instalar Maven en un sistema?
Respuesta: Instalar JDK, descargar Maven, descomprimirlo, configurar variables de entorno y verificar con `mvn -v`.

### ¿Qué variables de entorno son necesarias para que Maven funcione correctamente?
Respuesta: Principalmente `JAVA_HOME` y agregar `bin` de Maven al `PATH` (opcionalmente `M2_HOME`/`MAVEN_HOME`).

### ¿Qué es el testing y cuál es su objetivo principal?
Respuesta: Es la práctica de validar el software con pruebas; busca detectar fallos y asegurar que el comportamiento cumpla requisitos.

### ¿Cuáles son las herramientas de testing más populares en Java?
Respuesta: JUnit 5 para ejecutar pruebas, Mockito para mocks, AssertJ/Hamcrest para aserciones y Testcontainers para integración.

### ¿Cuáles son los principales tipos de testing y en qué etapa se aplican?
Respuesta: Unitario (desarrollo), integración (unión de componentes), sistema/E2E (flujo completo) y aceptación (validación funcional final).

### ¿Qué características debe tener una buena prueba?
Respuesta: Debe ser clara, determinística, rápida, aislada y verificar un comportamiento concreto con aserciones precisas.

### ¿Cuál es la diferencia entre pruebas unitarias y pruebas de integración?
Respuesta: La unitaria prueba una pieza aislada (con mocks); la de integración prueba interacción real entre módulos o servicios.

### ¿Qué son las pruebas de regresión y por qué son importantes?
Respuesta: Son pruebas repetidas tras cambios para confirmar que nada existente se rompió; previenen reintroducción de bugs.

### ¿Qué es el testing unitario y cuál es su objetivo?
Respuesta: Es probar unidades pequeñas de código de forma aislada para verificar su lógica rápidamente y con confianza.

### ¿Cuál es la diferencia entre JUnit y Mockito?
Respuesta: JUnit estructura/ejecuta tests y aserciones; Mockito crea mocks/spies y define/verifica interacciones.

### ¿Por qué es importante aislar las dependencias en pruebas unitarias?
Respuesta: Evita efectos externos (DB, red, tiempo), haciendo pruebas más rápidas, repetibles y enfocadas en una sola unidad.

### ¿Qué significa el patrón Arrange-Act-Assert?
Respuesta: Organiza el test en tres pasos: preparar datos/escenario, ejecutar la acción y verificar resultados.

### ¿Qué anotación se usa para marcar un método como prueba en JUnit?
Respuesta: `@Test`.

### ¿Cuál es la diferencia entre `@BeforeEach` y `@BeforeAll`?
Respuesta: `@BeforeEach` corre antes de cada test; `@BeforeAll` corre una sola vez antes de todos.

### ¿Para qué sirve la anotación `@DisplayName`?
Respuesta: Permite asignar un nombre legible al test o clase para mejorar reportes y comprensión.

### ¿Cómo se deshabilita temporalmente una prueba en JUnit?
Respuesta: Con `@Disabled`, opcionalmente indicando el motivo.

### ¿Qué permite hacer la anotación `@Tag`?
Respuesta: Etiquetar tests para filtrarlos por grupos (por ejemplo, `unit`, `integration`, `slow`).

### ¿Qué es un mock y para qué se utiliza?
Respuesta: Un objeto simulado que reemplaza una dependencia real para controlar su comportamiento en pruebas aisladas.

### ¿Cuáles son las dos formas de crear un mock en Mockito?
Respuesta: Con `Mockito.mock(Clase.class)` o con `@Mock` (inicializado con extensión/runner de Mockito).

### ¿Qué diferencia hay entre `@Mock` y `mock()`?
Respuesta: `@Mock` es declarativo por anotación; `mock()` crea el mock de forma explícita por código.

### ¿Qué es un spy en Mockito y cómo difiere de un mock?
Respuesta: Un spy envuelve un objeto real y ejecuta su comportamiento por defecto; un mock no ejecuta lógica real salvo stubbing.

### ¿Cuándo conviene usar un spy en lugar de un mock?
Respuesta: Cuando querés conservar comportamiento real de la clase pero sobreescribir algunos métodos puntuales.

### ¿Por qué se recomienda usar `doReturn()` en vez de `when()` con spies?
Respuesta: Porque `when(spy.metodo())` ejecuta el método real al stubear; `doReturn()` evita ese efecto colateral.

### ¿Qué hace la anotación `@InjectMocks`?
Respuesta: Crea la instancia bajo prueba e inyecta en ella los mocks/spies disponibles automáticamente.

### ¿En qué orden intenta Mockito inyectar los mocks?
Respuesta: Primero por constructor, luego por setters y por último por campos.

### ¿Qué limitaciones tiene `@InjectMocks`?
Respuesta: No resuelve toda la DI real ni casos complejos; puede fallar con dependencias ambiguas, finales o no configurables.

### ¿Para qué sirve el método `when()` en Mockito?
Respuesta: Para definir stubbing: indicar qué devolver o lanzar cuando un mock recibe cierta llamada.

### ¿Cómo se configura un mock para que lance una excepción?
Respuesta: Con `when(...).thenThrow(...)` o `doThrow(...).when(mock).metodoVoid(...)` si el método es `void`.

### ¿Qué son los argument matchers y cuándo se usan?
Respuesta: Son predicados como `any()` o `eq()` para flexibilizar argumentos al stubear/verificar cuando no importa un valor exacto.

### ¿Para qué sirve `thenReturn()` en Mockito?
Respuesta: Define el valor que devolverá el mock para una invocación configurada.

### ¿Cómo se configuran múltiples retornos consecutivos?
Respuesta: Encadenando valores: `thenReturn(v1, v2, v3)` o varios `thenReturn()` seguidos.

### ¿Para qué sirve `thenThrow()` en Mockito?
Respuesta: Configura un mock para lanzar una excepción ante una llamada específica.

### ¿Para qué sirve `doNothing()` en Mockito?
Respuesta: Para definir explícitamente que un método `void` no haga nada (útil en spies o para documentar intención).

### ¿Por qué no se puede usar `when().thenReturn()` con métodos void?
Respuesta: Porque `when()` necesita un valor de retorno; los `void` se stubbean con la familia `do...` (`doNothing`, `doThrow`, etc.).

### ¿Para qué sirve `verify()` en Mockito?
Respuesta: Para comprobar que un mock recibió ciertas llamadas con argumentos y cantidad esperada.

### ¿Cómo se verifica que un método fue llamado exactamente N veces?
Respuesta: Con `verify(mock, times(N)).metodo(...)`.

### ¿Cómo se verifica que un método nunca fue llamado?
Respuesta: Con `verify(mock, never()).metodo(...)` o `times(0)`.

### ¿Qué es Reflection y para qué se utiliza?
Respuesta: API de Java para inspeccionar y manipular clases, métodos y campos en tiempo de ejecución.

### ¿Por qué se considera mala práctica usar reflection para acceder a miembros privados?
Respuesta: Rompe encapsulamiento, aumenta acoplamiento y puede degradar mantenibilidad, seguridad y rendimiento.

### ¿Cómo se accede a un método privado usando reflection?
Respuesta: Se obtiene con `getDeclaredMethod(...)`, se habilita acceso y se invoca con `invoke(...)`.

### ¿Qué método se usa para permitir el acceso a miembros privados?
Respuesta: `setAccessible(true)`.

### ¿Para qué sirve la clase `ReflectionSupport` de JUnit?
Respuesta: Facilita buscar e invocar miembros por reflection en tests, con una API más cómoda que la reflexión pura.

### ¿Qué método se usa para buscar un método privado?
Respuesta: `ReflectionSupport.findMethod(...)`.

### ¿Qué retorna `findMethod()` si no encuentra el método?
Respuesta: Retorna un `Optional` vacío (`Optional.empty()`).

### ¿Cómo se invoca un método privado usando `ReflectionSupport`?
Respuesta: Se localiza el método con `findMethod(...)` y luego se invoca con `ReflectionSupport.invokeMethod(...)`.
