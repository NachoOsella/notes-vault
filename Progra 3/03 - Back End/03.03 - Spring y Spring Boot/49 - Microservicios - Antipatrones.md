# Microservicios - Antipatrones

## Definicion
Son decisiones frecuentes que parecen correctas al inicio pero empeoran mantenimiento, costo y confiabilidad.

## Explicacion
- *No empezar por microservicios si no hay dolor real de monolito*
    Primero validar complejidad real.
- *No hacer microservicios sin DevOps/nube gestionada*
    Operacion manual multiplica fallas.
- *No fragmentar demasiado los servicios*
    Exceso de "micro" aumenta acoplamiento distribuido.
- *No convertirlo en SOA pesado*
    Evitar burocracia y complejidad organizacional excesiva.
- *No intentar copiar a Netflix ciegamente*
    Ajustar arquitectura a escala y contexto propios.

## Palabras clave
- antipatron
- sobrearquitectura
- complejidad accidental
- sobredimensionamiento

## Comparaciones tipicas
- vs [[48 - Microservicios - Patrones comunes]]: patrones guian buenas practicas; antipatrones muestran trampas.
- vs [[45 - Microservicios - Beneficios y desafíos]]: desafios son naturales; antipatrones son errores evitables.

## Preguntas de examen
- Menciona antipatrones tipicos en microservicios.
- Por que "no intentes ser Netflix" es una recomendacion valida?

## Errores comunes
- Introducir microservicios sin capacidad operativa.
- Medir exito por cantidad de servicios y no por valor entregado.
