# Fibonacci - Qué es

## Definición
Fibonacci es una sucesión donde cada término se obtiene sumando los dos anteriores.

## Explicación

- *Qué problema resuelve*
    Proporciona un ejemplo matemático clásico de secuencia recursiva que aparece en múltiples contextos naturales y sirve como caso de estudio para algoritmos
- *Cómo funciona por arriba*
    - **Origen**: Debe su nombre a Leonardo de Pisa (siglo XIII), matemático italiano. Presentó la secuencia en su libro "Liber Abaci" (1202)
    - **Problema original**: "¿Cuántos pares de conejos se pueden generar en un año a partir de una sola pareja, si cada mes cada pareja produce una nueva pareja que se vuelve fértil al segundo mes?"
    - **Secuencia**: 1, 1, 2, 3, 5, 8, 13, 21, 34, ... (cada número es la suma de los dos anteriores)
    - **Definición formal**: F(0)=0, F(1)=1, F(n)=F(n-1)+F(n-2)
- *Qué implica / qué permite*
    - **En la naturaleza**: Se observan patrones similares en la disposición de hojas, ramas, pétalos de flores, espiral de conchas
    - **En finanzas**: Modelos de predicción de mercados usan proporciones basadas en Fibonacci
    - **En arte y arquitectura**: La "razón áurea" está relacionada con Fibonacci
    - Sirve como problema didáctico para enseñar recursión y programación dinámica

## Comparaciones típicas
- vs [[20 - Fibonacci - Recursivo]]: concepto matemático vs implementación algorítmica
- vs [[22 - Fibonacci - Programación dinámica]]: definición del problema vs técnicas de optimización
- vs [[20 - Fibonacci - Recursivo]]: teoría de la sucesión vs implementación computacional

## Palabras clave
- sucesión
- recursión
- F(n)
- casos base
- patrón

## Preguntas de examen
- ¿Cuál es la definición formal de Fibonacci con casos base?
- ¿Por qué Fibonacci se usa tanto para enseñar algoritmos?

## Errores comunes
- Iniciar mal la sucesión (confundir F(0) y F(1)).
- Quedarse solo con lo matemático sin analizar costo computacional.

## Mini-ejemplo (mental)
- Escalera donde cada peldaño depende de combinar los dos anteriores.

