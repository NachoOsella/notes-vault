# Maven - Instalación y configuración

## Definición
La instalación y configuración de Maven implica descargar e instalar el software en el sistema, así como configurar variables de entorno y archivos de configuración necesarios para su correcto funcionamiento.

## Explicación
- *Qué problema resuelve*
Facilita la gestión de proyectos Java al proporcionar una herramienta estandarizada para la construcción, gestión de dependencias y despliegue.
- *Cómo funciona por arriba*
Requiere la instalación del software Maven, la configuración de variables de entorno como `MAVEN_HOME` y `PATH`, y la edición del archivo `settings.xml` para personalizar la configuración global o del usuario.
- *Qué implica / qué permite*
Permite a los desarrolladores utilizar Maven para automatizar tareas de construcción, gestionar dependencias y ejecutar plugins de manera eficiente en sus proyectos Java.

## Palabras clave
- Instalación
- Configuración
- Variables de entorno
- `settings.xml`
- `MAVEN_HOME`
- PATH

## Comparaciones típicas
- vs [[04 - Maven - Conceptos básicos]]: instalación/config es el “cómo lo hago andar”; conceptos es el “para qué sirve”.
- vs [[06 - Maven - Archivos de configuración]]: config de entorno (PATH, `settings.xml`) vs config del proyecto (`pom.xml`).

## Preguntas de examen
- ¿Cuáles son los pasos básicos para instalar Maven en un sistema?
- ¿Qué variables de entorno son necesarias para que Maven funcione correctamente?
- ¿Dónde se encuentra el archivo `settings.xml` y qué propósito cumple?

## Errores comunes
- No configurar correctamente las variables de entorno, lo que impide que Maven se ejecute desde la línea de comandos.
- No editar el archivo `settings.xml` para personalizar la configuración según las necesidades del usuario
- No verificar la instalación de Java antes de instalar Maven, ya que Maven depende de Java para funcionar.

## Mini-ejemplo (mental)
Es como instalar una nueva herramienta en tu computadora: descargas el software, configuras las variables necesarias para que el sistema la reconozca, y ajustas las configuraciones para que funcione según tus necesidades. Una vez hecho esto, puedes empezar a usar Maven para gestionar tus proyectos Java de manera eficiente.
