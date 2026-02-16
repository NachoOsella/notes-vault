# Qué es una API

## Definición
Conjunto de definiciones y protocolos que permite que dos aplicaciones de software se comuniquen entre sí y compartan información o funcionalidades de manera eficiente.

## Explicación
- *Qué problema resuelve*
    Permite que aplicaciones se comuniquen e intercambien datos sin necesidad de conocer los detalles internos de la otra aplicación, evitando tener que programar todas las funcionalidades desde cero.
- *Cómo funciona por arriba*
    Funciona como un intermediario o puente. Actúa como el "mesero" de un restaurante: recibe el pedido del cliente (aplicación), lo lleva a la cocina (servidor) y trae el resultado de vuelta.
- *Qué implica / qué permite*
    Permite integrar funciones de otros sistemas (como pagos, mapas o autenticación) en programas propios, ahorrando tiempo y esfuerzo en el desarrollo.

## Ejemplos comunes
- Login con Google o Facebook en un sitio web.
- Busqueda de vuelos en un comparador de precios.
- Pagos en linea con PayPal o MercadoPago.
- Mapas embebidos usando la API de Google Maps.

## Palabras clave
- Interfaz
- Protocolos
- Intermediario
- Abstracción
- Contrato

## Comparaciones típicas
- vs [[18 - API - Qué es un Servicio Web]]: servicio web es una API expuesta por red (normalmente HTTP); una API puede ser local (sin red).
- vs [[21 - API - Tipos de APIs (locales vs remotas vs web)]]: acá se define qué es una API; el otro clasifica APIs según dónde y cómo corren.
- vs [[19 - API - Arquitectura RESTful (API REST)]]: REST es una forma común de implementar servicios web (un tipo de API), no la definición de API en sí.

## Preguntas de examen
- ¿Qué es una API?
- ¿Para qué sirve una API?
- ¿Cuál es la analogía típica para explicar una API?

## Errores comunes
- Creer que solo existen APIs para web.
- Pensar que una API maneja la lógica de negocio en lugar de ser solo el intermediario.

## Mini-ejemplo (mental)
- Imagina que usas tu cuenta de Facebook para iniciar sesión en una web nueva: esa web usa la API de Facebook para verificar quién eres sin que Facebook le dé tu contraseña.
