# Maven - Plugins

## Definición
Los plugins son componentes que extienden la funcionalidad de Maven, permitiendo automatizar tareas específicas durante el ciclo de vida del proyecto, como compilación, pruebas, empaquetado y despliegue.
Los plugins se configuran en el archivo `pom.xml` y pueden ser tanto oficiales como de terceros.
```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.8.1</version>
            <configuration>
                <source>1.8</source>
                <target>1.8</target>
            </configuration>
        </plugin>
    </plugins>
</build>
```

## Explicación
- *Qué problema resuelve*
    Permiten automatizar y estandarizar tareas comunes en el desarrollo de software, facilitando la gestión del ciclo de vida del proyecto.
- *Cómo funciona por arriba*
    Los plugins se integran en el ciclo de vida de Maven, ejecutándose en fases específicas (como compile, test, package) para realizar tareas definidas.
- *Qué implica / qué permite*
    Facilitan la configuración y ejecución de tareas complejas, mejorando la eficiencia del desarrollo y asegurando la consistencia en los procesos de construcción y despliegue.

## Palabras clave
- Automatización
- Ciclo de vida
- Tareas
- Extensibilidad
- Configuración

## Comparaciones típicas
- vs [[Maven - Gestión de dependencias]]: plugins = tareas del build; dependencias = librerías que se linkean/usan en código.
- vs [[Maven - Ciclo de vida]]: plugins se atan a fases (compile/test/package) para automatizar el pipeline.

## Preguntas de examen
- ¿Qué es un plugin en Maven y cuál es su propósito?
- ¿Cómo se configura un plugin en el archivo `pom.xml`?

## Errores comunes
- No especificar la versión del plugin, lo que puede llevar a inconsistencias en el build.
- Configurar incorrectamente las opciones del plugin, lo que puede causar fallos en la ejecución
- No asociar el plugin a la fase correcta del ciclo de vida, lo que puede resultar en tareas no ejecutadas.

## Mini-ejemplo (mental)
Los plugins son como herramientas especializadas que puedes agregar a tu caja de herramientas de Maven para realizar tareas específicas durante la construcción de tu proyecto. Por ejemplo, el `maven-compiler-plugin` se encarga de compilar el código fuente, mientras que el `maven-surefire-plugin` ejecuta las pruebas unitarias. Al configurar estos plugins en tu `pom.xml`, puedes automatizar todo el proceso de construcción y asegurarte de que cada paso se realice correctamente sin intervención manual.
