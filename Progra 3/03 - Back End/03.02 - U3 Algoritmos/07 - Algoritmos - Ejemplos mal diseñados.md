# Algoritmos - Ejemplos mal diseñados

## Definición
Un algoritmo mal diseñado puede ser correcto, pero desperdicia recursos por decisiones ineficientes.

## Explicación

- *Qué problema resuelve*
    Sirve como contrapunto pedagógico para entender qué NO hacer y por qué ciertas soluciones simples son problemáticas
- *Cómo funciona por arriba*
    **Ejemplo: No aprovechar estructuras de datos adecuadas - Búsqueda de usuario por email**:
    ```java
    String buscarEmail(String[] emailUsuarios, String email) {
        for (String e : emailUsuarios) {
            if (e.equals(email)) return e;
        }
        return null;
    }
    ```
    - **¿Qué hace?**: Recorre uno por uno el arreglo comparando cada email
    - **Problemas**:
        - Búsqueda lineal O(n): en el peor caso recorre todos los elementos
        - Si hay 10.000 usuarios y el email está al final, hace 10.000 comparaciones
        - Escala mal con listas grandes: el rendimiento se degrada rápidamente
    - **Solución**: Usar estructuras de datos adecuadas como Set o HashSet que permiten acceso directo O(1) en lugar de recorrido completo
- *Qué implica / qué permite*
    Aprender a detectar code smells algorítmicos; entender que "funciona" no implica "es adecuado"; desarrollar intuición sobre cuándo una solución naive necesita optimización; elegir las estructuras de datos correctas para el problema

## Comparaciones típicas
- vs [[11 - Big-O - Notación]]: muestra un caso real de por qué medir complejidad evita malas decisiones de diseño
- vs [[21 - Fibonacci - Complejidad recursiva]]: ejemplo clásico de mal diseño por recálculo redundante sin memoización

## Palabras clave
- solución naive
- ineficiencia
- estructura de datos
- recálculo
- optimización

## Preguntas de examen
- ¿Qué señales indican que un algoritmo funciona pero está mal diseñado?
- ¿Qué mejora concreta aporta cambiar de arreglo a HashSet en búsquedas?

## Errores comunes
- Confundir corrección con calidad algorítmica.
- No medir complejidad antes de llevar código a producción.

## Mini-ejemplo (mental)
- Buscar una persona en agenda desordenada hoja por hoja en vez de usar índice alfabético.

