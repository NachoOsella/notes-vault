# Maven - Conceptos básicos

## Definición
Maven es una herramienta de gestión de proyectos y automatización de compilación para proyectos Java (y otros lenguajes). Proporciona un modelo de construcción estandarizado, gestión de dependencias y un sistema de plugins para facilitar el desarrollo y la entrega de software.

## Explicación
- *Qué problema resuelve*
    Gestionar las dependencias de un proyecto, automatizar el proceso de construcción y estandarizar la estructura del proyecto.
- *Cómo funciona por arriba*
    Utiliza un archivo de configuración llamado `pom.xml` (Project Object Model) para definir las dependencias, plugins y configuraciones del proyecto. Maven descarga automáticamente las dependencias desde repositorios remotos(como Maven Central) y las almacena en un repositorio local.
- *Qué implica / qué permite*
    Permite a los desarrolladores centrarse en escribir código en lugar de gestionar manualmente las dependencias y el proceso de construcción. Facilita la colaboración en equipos al proporcionar una estructura de proyecto común y un sistema de gestión de versiones para las dependencias.

## Palabras clave
- POM (Project Object Model)
- Repositorio local
- Repositorio remoto
- Dependencias
- Plugins

## Comparaciones típicas

- vs [[06 - Maven - Archivos de configuración]]: Maven como herramienta vs los archivos donde se describe el proyecto/entorno (p. ej. `pom.xml`).
- vs [[07 - Maven - Gestión de dependencias]]: idea general de dependencias vs cómo se resuelven versiones, scopes y repos.

## Preguntas de examen
- ¿Qué es Maven y cuál es su propósito principal?
- ¿Qué es un archivo `pom.xml` y qué información contiene?
- ¿Cómo maneja Maven las dependencias de un proyecto?

## Errores comunes
- Confundir Maven con solo un sistema de construcción, cuando también es una herramienta de gestión de proyectos.
- No entender la estructura del `pom.xml` y cómo se configuran las dependencias y plugins.
- No aprovechar los beneficios de la gestión automática de dependencias y construcción que ofrece Maven.

## Mini-ejemplo (mental)
Maven es como un asistente de construcción para tu proyecto de software. Imagina que estás construyendo una casa (tu aplicación) y necesitas varios materiales (bibliotecas y dependencias). En lugar de buscar y comprar cada material por separado, le das a Maven una lista (el `pom.xml`) con todo lo que necesitas. Maven se encarga de ir a la tienda (repositorios remotos), recoger los materiales correctos y traerlos a tu sitio de construcción (repositorio local). Además, te ayuda a organizar el proceso de construcción, asegurándose de que todo esté en el lugar correcto y listo para usar cuando lo necesites.
