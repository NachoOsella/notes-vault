# Microservicios - DevOps y CI/CD

## Definicion
En microservicios, DevOps y CI/CD son practicas necesarias para automatizar build, test, deploy y operacion continua.

## Explicacion
- *Que problema resuelve*
    Sin automatizacion, coordinar multiples servicios se vuelve inviable.
- *Como funciona por arriba*
    Pipelines ejecutan pruebas, generan artefactos, despliegan y monitorean cada servicio.
- *Que implica / que permite*
    Entregas frecuentes, menos errores manuales y feedback rapido.

## Palabras clave
- DevOps
- CI/CD
- automatizacion
- despliegue continuo

## Comparaciones tipicas
- vs flujo manual: manual escala mal con muchos servicios.
- vs [[37 - Spring Boot - Empaquetado y ejecucion (jar)]]: empaquetado crea artefacto; CI/CD gestiona ciclo completo.

## Preguntas de examen
- Por que microservicios "requieren" DevOps?
- Que etapas minimas deberia tener un pipeline CI/CD?

## Errores comunes
- Tener CI sin CD (o viceversa) en sistemas muy distribuidos.
- No incluir observabilidad en el pipeline operativo.
