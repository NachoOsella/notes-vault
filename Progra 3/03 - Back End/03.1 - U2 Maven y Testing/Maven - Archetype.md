# Maven - Archetype

## Definición
Un *archetype* es una plantilla o modelo de proyecto que sirve como punto de partida para crear nuevos proyectos con Maven. Proporciona una estructura de directorios y archivos predefinidos, así como configuraciones básicas en el `pom.xml`, facilitando la creación rápida de proyectos con una configuración estándar.

## Explicación
- *Qué problema resuelve*
    Facilita la creación de nuevos proyectos al proporcionar una estructura y configuración inicial predefinida, evitando la necesidad de configurar todo desde cero.
- *Cómo funciona por arriba*
    Maven ofrece una serie de archetypes predeterminados (como `maven-archetype-quickstart` para proyectos Java básicos) y permite a los usuarios crear sus propios archetypes personalizados. Al ejecutar el comando `mvn archetype:generate`, Maven presenta una lista de archetypes disponibles para elegir. Una vez seleccionado, Maven genera la estructura del proyecto y los archivos necesarios basándose en el archetype elegido.
- *Qué implica / qué permite*
    Permite a los desarrolladores iniciar nuevos proyectos de manera rápida y consistente, asegurando que todos los proyectos sigan una estructura estándar. Esto es especialmente útil en equipos donde se desea mantener uniformidad en la configuración y estructura de los proyectos.

## Palabras clave
- Plantillas
- Estructura de proyecto
- `mvn archetype:generate`

## Comparaciones típicas
- vs [[Maven - Conceptos básicos]]: archetype es “plantilla de proyecto”; Maven es el sistema de build/deps.
- vs [[Maven - Archivos de configuración]]: el archetype genera estructura inicial + `pom.xml` base.

## Preguntas de examen
- ¿Qué es un archetype en Maven y cuál es su propósito?
- ¿Cómo se utiliza un archetype para crear un nuevo proyecto en Maven?
- ¿Qué beneficios ofrece el uso de archetypes en el desarrollo de proyectos con Maven?

## Errores comunes
- No seleccionar el archetype adecuado para el tipo de proyecto que se desea crear.
- No personalizar el `pom.xml` generado según las necesidades específicas del proyecto.

## Mini-ejemplo (mental)
Es como usar una plantilla para crear un nuevo documento. En lugar de empezar desde una página en blanco, eliges una plantilla que ya tiene el formato y las secciones básicas que necesitas. De manera similar, al usar un archetype en Maven, seleccionas una plantilla de proyecto que ya tiene la estructura y configuración inicial, lo que te permite comenzar a trabajar en tu código más rápidamente.
