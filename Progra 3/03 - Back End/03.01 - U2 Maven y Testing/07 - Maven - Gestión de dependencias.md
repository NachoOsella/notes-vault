# Maven - Gestión de dependencias

## Definición
Proceso clave en la construcción de un proyecto. Las dependencias son bibliotecas y módulos externos de código que se utilizan a lo largo del desarrollo de software para evitar reinventar la rueda y aprovechar soluciones ya existentes. La gestión de dependencias consiste en administrar estas bibliotecas de manera eficiente, asegurando que las versiones correctas estén disponibles y que no haya conflictos entre ellas.
### Agregar dependencias
En Maven, las dependencias se declaran en el archivo `pom.xml` del proyecto. Cada dependencia se especifica con un grupo, un artefacto y una versión.
```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-core</artifactId>
    <version>5.3.8</version>
</dependency>
```

### Excluir dependencias transitivas
A veces, una dependencia que agregás puede traer otras dependencias (transitivas) que no querés. Podés excluirlas así:
```xml
<dependency>
    <groupId>com.example</groupId>
    <artifactId>example-lib</artifactId>
    <version>1.0.0</version>
    <exclusions>
        <exclusion>
            <groupId>org.unwanted</groupId>
            <artifactId>unwanted-lib</artifactId>
        </exclusion>
    </exclusions>
</dependency>
```

## Explicación
- *Qué problema resuelve*
    La gestión de dependencias en Maven resuelve el problema de manejar múltiples bibliotecas y sus versiones en un proyecto de software. Sin una gestión adecuada, los desarrolladores podrían enfrentar conflictos de versiones, duplicación de código y dificultades para mantener el proyecto actualizado con las últimas mejoras y correcciones de errores.
- *Cómo funciona por arriba*
    Maven utiliza un archivo de configuración llamado `pom.xml` (Project Object Model) para declarar las dependencias del proyecto. Cuando se construye el proyecto, Maven descarga automáticamente las bibliotecas necesarias desde repositorios remotos (como Maven Central) y las incluye en el classpath del proyecto. Además, Maven maneja las dependencias transitivas, lo que significa que si una dependencia tiene sus propias dependencias, Maven también las descargará y gestionará.
- *Qué implica / qué permite*
    La gestión de dependencias en Maven permite a los desarrolladores centrarse en escribir código en lugar de preocuparse por la integración de bibliotecas externas. Facilita la colaboración en equipos, ya que todos los miembros pueden trabajar con las mismas versiones de las dependencias. Además, permite una fácil actualización y mantenimiento del proyecto, ya que las dependencias pueden ser actualizadas simplemente cambiando la versión en el `pom.xml`.

## Palabras clave
- Dependencias
- Transitive dependencies
- Repositorios
- POM (Project Object Model)
- Plugins
- Build lifecycle
- Classpath

## Comparaciones típicas
- vs [[06 - Maven - Archivos de configuración]]: declarás dependencias en `pom.xml`; Maven las resuelve/descarga desde repos.
- vs [[08 - Maven - Plugins]]: dependencias son código que tu app usa; plugins son herramientas del build (compilación, tests, empaquetado).

## Preguntas de examen
- ¿Cómo se declaran las dependencias en un proyecto Maven?
- ¿Qué son las dependencias transitivas y cómo se gestionan en Maven?
- ¿Cuál es la diferencia entre una dependencia y un plugin en Maven?

## Errores comunes
- No declarar correctamente las dependencias en el `pom.xml`, lo que puede llevar a errores de compilación o ejecución.
- No gestionar las versiones de las dependencias, lo que puede causar conflictos entre diferentes bibliotecas.
- Olvidar excluir dependencias transitivas no deseadas, lo que puede aumentar innecesariamente el tamaño del proyecto o causar conflictos.

## Mini-ejemplo (mental)
La gestion de dependencias es como tener una lista de ingredientes para una receta. En lugar de comprar cada ingrediente por separado, tenés una lista que indica qué ingredientes necesitás y en qué cantidad. Maven se encarga de ir a la tienda (repositorio) y traer todos los ingredientes (dependencias) necesarios para preparar tu plato (proyecto). Si un ingrediente tiene otros ingredientes necesarios (dependencias transitivas), Maven también los trae automáticamente, asegurándose de que todo esté listo para cocinar sin conflictos.
