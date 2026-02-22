# Microservicios - Que son

## Definicion
Los microservicios son una arquitectura donde una app se divide en servicios pequenos, independientes y acoplados de forma flexible.

## Explicacion
- *Que problema resuelve*
    Reduce el acoplamiento de un monolito grande y facilita evolucion por partes.
- *Como funciona por arriba*
    Cada servicio suele tener su propia logica, despliegue y, a menudo, su propia base de datos; se comunican por API/eventos.
- *Que implica / que permite*
    Despliegues independientes, escalado puntual y autonomia de equipos.

## Palabras clave
- microservicios
- independencia
- contexto limitado
- API/eventos

## Comparaciones tipicas
- vs monolito: monolito despliega todo junto; microservicios despliegan por servicio.
- vs SOA: microservicios suelen ser por aplicacion; SOA busca estandarizacion a escala empresa.

## Preguntas de examen
- Que caracteriza a un microservicio?
- Diferencias clave con arquitectura monolitica.

## Errores comunes
- Confundir microservicio con "cualquier modulo".
- Dividir sin limites de negocio claros.
