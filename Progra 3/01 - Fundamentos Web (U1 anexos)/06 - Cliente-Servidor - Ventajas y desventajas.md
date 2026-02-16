# Cliente-Servidor - Ventajas y desventajas

## Definición
Análisis de los beneficios y limitaciones que ofrece la arquitectura cliente-servidor en el desarrollo de aplicaciones.

## Explicación
- *Qué problema resuelve*
    Ayuda a decidir cuándo es conveniente usar esta arquitectura frente a otras (como Peer-to-Peer) basándose en necesidades de control, seguridad y recursos.
- *Cómo funciona por arriba*
    Al centralizar datos y lógica, se gana control pero se crea un punto único de falla. Al distribuir la interfaz, se mejora la experiencia de usuario pero aumenta la complejidad de red.
- *Qué implica / qué permite*
    Permite el mantenimiento centralizado (solo actualizas el servidor) y la seguridad mejorada, pero implica dependencia de la conectividad de red.

## Ventajas
- Integracion entre sistemas y plataformas distintas con una interfaz unificada.
- Escalabilidad: se pueden sumar tecnologias complementarias ante alta demanda.
- Estructura modular que facilita agregar nuevas tecnologias sin rehacer todo.
- Acceso simultaneo de varios clientes a los mismos servicios.

## Desventajas
- Requiere personal con habilidades para reparar fallas de red o servidor.
- Riesgos de seguridad por canales compartidos y validaciones insuficientes.
- Costos altos de infraestructura por hardware y software especificos.

## Palabras clave
- Escalabilidad
- Mantenimiento centralizado
- Punto único de falla
- Latencia
- Seguridad
- Integracion
- Modularidad
- Costos

## Comparaciones típicas
- vs [[03 - Cliente-Servidor - Características y componentes]]: acá se evalúan tradeoffs (pros/contras); el otro describe cómo funciona el modelo.
- vs [[05 - Cliente-Servidor - Clientes y servidores]]: acá se analizan beneficios/costos; el otro define responsabilidades de roles.
- vs [[07 - HTTP - Sistemas basados en HTTP]]: HTTP es un ejemplo de cliente-servidor; sus ventajas (caché, capas) y costos (latencia) se ven en la práctica.

## Preguntas de examen
- Menciona 2 ventajas y 2 desventajas del modelo cliente-servidor.
- ¿Qué es un "punto único de falla" en esta arquitectura?
- ¿Por qué el mantenimiento es más sencillo?

## Errores comunes
- Creer que es la única arquitectura posible (existe P2P).
- Pensar que la escalabilidad es infinita sin costo.

## Mini-ejemplo (mental)
- Ventaja: Actualizas la base de datos de precios en el servidor y todos los clientes lo ven al instante. Desventaja: Si se cae Internet, nadie puede ver los precios.
