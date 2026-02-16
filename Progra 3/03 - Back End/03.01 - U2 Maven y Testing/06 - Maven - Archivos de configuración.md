# Maven - Archivos de configuración

## Definición
Maven utiliza diferentes archivos de configuración para gestionar proyectos Java. Los principales son:
    - `pom.xml`: Archivo principal que define el proyecto, sus dependencias, plugins y configuraciones.
    - `settings.xml`: Archivo de configuración global o de usuario que define configuraciones específicas del entorno Maven, como repositorios y perfiles. Se encuentra en el directorio `.m2` (generalmente en el home del usuario).

## Explicación
- *Qué problema resuelve*
    Permite definir y gestionar de manera centralizada las dependencias, plugins y configuraciones del proyecto, facilitando la construcción y mantenimiento del mismo.
- *Cómo funciona por arriba*
    El `pom.xml` es leído por Maven para entender cómo construir el proyecto, qué dependencias necesita y qué plugins utilizar. El `settings.xml` puede modificar el comportamiento de Maven a nivel global o de usuario.
- *Qué implica / qué permite*
    Facilita la gestión de proyectos Java, permitiendo a los desarrolladores centrarse en el código en lugar de en la configuración manual de dependencias y herramientas.

## Palabras clave
- POM (Project Object Model)
- Dependencias
- Plugins
- Repositorios
- Perfiles
- Configuración global

## Comparaciones típicas
- vs [[07 - Maven - Gestión de dependencias]]: dependencias se declaran en config (POM); gestión es la resolución/descarga/scopes.
- vs [[08 - Maven - Plugins]]: plugins se configuran en el POM; plugins son “tareas”, no librerías de runtime.

## Preguntas de examen
- ¿Cuál es la función principal del archivo `pom.xml` en un proyecto Maven?
- ¿Dónde se encuentra típicamente el archivo `settings.xml` y qué propósito sirve?
- ¿Cómo se definen las dependencias en un proyecto Maven?

## Errores comunes
- Confundir el `pom.xml` con el `settings.xml`.
- No declarar correctamente las dependencias en el `pom.xml`.

## Mini-ejemplo (mental)
El archivo `pom.xml` es como la receta de un pastel: indica qué ingredientes (dependencias) necesitas y cómo prepararlo (plugins y configuraciones). El `settings.xml` es como las preferencias de cocina personales, ajustando cómo se hacen las cosas en tu entorno específico.
