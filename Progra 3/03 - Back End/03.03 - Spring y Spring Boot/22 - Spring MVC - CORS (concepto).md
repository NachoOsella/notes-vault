# Spring MVC - CORS (concepto)

## Definicion
CORS (Cross-Origin Resource Sharing) es la politica del navegador que controla si un frontend puede llamar a un backend de otro origen.

## Explicacion
- *Que problema resuelve*
    Protege al usuario frente a solicitudes cruzadas no autorizadas.
- *Como funciona por arriba*
    El backend responde headers CORS (origenes, metodos, headers permitidos).
- *Que implica / que permite*
    Habilita integracion frontend-backend en dominios distintos de forma controlada.

## Palabras clave
- CORS
- Origin
- preflight
- Access-Control-Allow-Origin

## Comparaciones tipicas
- vs autenticacion: CORS no autentica usuarios; solo controla origen del navegador.
- vs firewall: firewall opera a nivel red; CORS a nivel navegador HTTP.

## Preguntas de examen
- Que es un "origen" en CORS?
- Por que una API puede funcionar en Postman pero fallar en navegador?

## Errores comunes
- Abrir CORS con `*` en produccion sin criterio.
- Confundir CORS con permisos de negocio.
