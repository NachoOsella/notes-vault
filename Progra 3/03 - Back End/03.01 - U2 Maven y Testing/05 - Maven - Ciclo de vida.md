# Maven - Ciclo de vida

## Definición
El ciclo de vida de Maven es una secuencia de fases que se ejecutan en un orden específico para construir, empaquetar y distribuir software. Las fases estan definidas por el archivo POM y son:
    - *Clean*: Limpia los archivos generados en compilaciones anteriores.
    - *Validate*: Verifica que el proyecto esté correctamente estructurado.
    - *Compile*: Compila el código fuente del proyecto.
    - *Test*: Ejecuta las pruebas unitarias del proyecto.
    - *Package*: Empaqueta el código compilado en un formato distribuible, como un JAR o WAR.
    - *Verify*: Realiza verificaciones adicionales en el paquete.
    - *Install*: Instala el paquete en el repositorio local de Maven.
    - *Deploy*: Copia el paquete final al repositorio remoto para compartirlo con otros desarrolladores.
    - *Site*: Genera documentación del proyecto.

## Explicación
- *Qué problema resuelve*
El ciclo de vida de Maven resuelve el problema de estandarizar y automatizar el proceso de construcción y gestión de proyectos de software, asegurando que todas las fases necesarias se ejecuten en el orden correcto.
- *Cómo funciona por arriba*
Maven utiliza el archivo POM (Project Object Model) para definir las fases del ciclo de vida y los plugins asociados a cada fase. Cuando se ejecuta un comando de Maven, este determina qué fases deben ejecutarse y llama a los plugins correspondientes para llevar a cabo las tareas definidas en cada fase.
- *Qué implica / qué permite*
El ciclo de vida de Maven permite a los desarrolladores automatizar el proceso de construcción, pruebas y despliegue de sus proyectos, reduciendo errores humanos y asegurando consistencia en las entregas. Además, facilita la integración continua y la colaboración entre equipos al proporcionar un marco común para la gestión de proyectos.

## Palabras clave
- Fases
- Plugins
- POM (Project Object Model)
- Construcción automatizada
- Gestión de proyectos

## Comparaciones típicas
- vs [[08 - Maven - Plugins]]: el ciclo de vida define fases; los plugins aportan los goals que se ejecutan en esas fases.
- vs [[06 - Maven - Archivos de configuración]]: el lifecycle es estándar; el POM decide qué plugins/goals corren en cada fase.

## Preguntas de examen
- ¿Cuáles son las fases principales del ciclo de vida de Maven y qué hace cada una?
- ¿Cómo se relacionan los plugins con las fases del ciclo de vida de Maven?

## Errores comunes
- Confundir fases del ciclo de vida con plugins: las fases son etapas del proceso, mientras que los plugins son herramientas que realizan tareas específicas en esas etapas.
- No entender el orden de las fases: ejecutar una fase sin haber completado las anteriores puede llevar a errores en la construcción del proyecto.

## Mini-ejemplo (mental)
Es como una receta de cocina donde cada fase es un paso en la preparación del platillo. Primero limpias la cocina (clean), luego preparas los ingredientes (validate), cocinas el platillo (compile), pruebas su sabor (test), lo empacas para llevar (package), verificas que todo esté bien (verify), lo guardas en tu despensa (install) y finalmente lo compartes con tus amigos (deploy). Cada paso debe seguirse en orden para que el platillo salga perfecto.
