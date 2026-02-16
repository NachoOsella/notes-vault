# Cliente-Servidor - Componentes

## Definición
Elementos fundamentales que integran el modelo de arquitectura para permitir la comunicación y el intercambio de servicios en una red.

## Explicación
- *Qué problema resuelve*
    Establece las piezas necesarias para que la información fluya de manera organizada y segura entre diferentes entidades.
- *Cómo funciona por arriba*
    Se compone de **Clientes** (demandantes), **Servidores** (proveedores), una **Red** (medio de conexión), **Protocolos** (reglas de diálogo), **Servicios** (la información/función entregada) y **Bases de Datos** (almacenamiento).
- *Qué implica / qué permite*
    Implica que cada componente tiene un rol técnico específico. Permite que el sistema sea modular, facilitando el reemplazo o mejora de una pieza (ej. cambiar la base de datos) sin afectar a todo el modelo.

## Palabras clave
- Red
- Protocolo
- Cliente / Servidor
- Servicio
- Base de Datos

## Comparaciones típicas
- vs [[03 - Cliente-Servidor - Características y componentes]]: este enumera piezas (cliente/servidor/red/protocolo/servicio/BD); el otro explica rasgos del modelo (asimetría, intercambio).
- vs [[05 - Cliente-Servidor - Clientes y servidores]]: este describe el sistema completo; el otro compara responsabilidades de dos roles.
- vs [[07 - HTTP - Sistemas basados en HTTP]]: acá se habla del modelo abstracto; en HTTP los componentes se ven como user agent, servidor web e intermediarios.

## Preguntas de examen
- ¿Qué es un protocolo en el contexto de componentes?
- ¿Cuál es la diferencia entre un servicio y una base de datos?
- ¿Puede un cliente actuar como servidor? (Sí, para optimizar acciones sencillas guardando datos locales).

## Errores comunes
- Olvidar que el "Protocolo" es un componente lógico tan esencial como el hardware.
- Confundir el "Servicio" (la música, el mail) con el "Servidor" (quien lo envía).

## Mini-ejemplo (mental)
- Un sistema de streaming: El **Cliente** (tu app) usa la **Red** (Internet) y un **Protocolo** para pedir un **Servicio** (video) que el **Servidor** busca en su **Base de Datos**.
