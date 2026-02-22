# Microservicios - Tecnologias clave

## Definicion
Microservicios suelen apoyarse en un conjunto de tecnologias base para ejecucion, comunicacion y operacion.

## Explicacion
- *Contenedores (Docker) y orquestacion (Kubernetes)*
    Empaquetan servicios y escalan/reinician automaticamente.
- *API Gateway*
    Punto de entrada unico: enruta, autentica y aplica politicas.
- *Mensajeria y event streaming*
    Facilita comunicacion asincrona desacoplada (brokers, Kafka).
- *Serverless (FaaS)*
    Funciones muy pequenas para tareas puntuales bajo demanda.

## Palabras clave
- Docker
- Kubernetes
- API Gateway
- Kafka
- serverless

## Comparaciones tipicas
- vs [[43 - Integración - Consumir APIs REST (RestTemplate vs WebClient)]]: esa nota mira cliente HTTP; esta mira stack de plataforma.
- vs [[50 - Microservicios - Servicios y nube]]: tecnologias son piezas; nube es modelo de provision y costos.

## Preguntas de examen
- Que rol cumple Kubernetes en microservicios?
- Cuando conviene mensajeria en vez de REST sincrono?

## Errores comunes
- Adoptar herramientas complejas sin necesidad real.
- Usar demasiadas tecnologias distintas sin estandar de equipo.
