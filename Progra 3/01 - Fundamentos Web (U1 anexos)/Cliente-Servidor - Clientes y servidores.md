# Cliente-Servidor - Clientes y servidores

## Definición
Diferenciación entre los roles de cliente (demandante) y servidor (proveedor) en la arquitectura cliente-servidor.

## Explicación
- *Qué problema resuelve*
    Aclara responsabilidades para distribuir procesamiento y datos, permitiendo que múltiples usuarios accedan a un mismo servicio.
- *Cómo funciona por arriba*
    El cliente es un equipo o aplicación que solicita servicios a través de Internet o una red interna. El servidor es una computadora con mayor capacidad que almacena archivos y ejecuta aplicaciones para responder a muchos clientes a la vez.
- *Qué implica / qué permite*
    Implica que el servidor concentra recursos y el cliente se enfoca en la interfaz. Permite acceso simultáneo y que un cliente actúe como servidor local guardando datos para tareas sencillas sin consultar continuamente.

## Palabras clave
- Cliente
- Servidor
- Capacidad
- Servicios
- Red
- Acceso remoto

## Comparaciones típicas
- vs [[Cliente-Servidor - Componentes]]: acá se explican roles; el otro lista todas las piezas (red, protocolo, servicio, BD, etc.).
- vs [[HTTP - User Agent (cliente)]]: el user agent es un tipo de cliente en HTTP (navegador/bot) que inicia requests.
- vs [[HTTP - Servidor Web]]: el servidor web es el servidor en el contexto de HTTP: espera requests y responde.

## Preguntas de examen
- ¿Qué diferencia principal hay entre un cliente y un servidor?
- ¿Por qué el servidor requiere mayor capacidad de hardware?
- ¿Puede un cliente cumplir funciones de servidor? ¿En qué caso?

## Errores comunes
- Pensar que cliente y servidor siempre son máquinas distintas (pueden ser procesos en la misma PC).
- Creer que el servidor inicia la comunicación (el cliente siempre inicia las peticiones).

## Mini-ejemplo (mental)
- En una empresa, cada PC de los empleados es cliente y el servidor central guarda los archivos y corre el sistema de correo.
