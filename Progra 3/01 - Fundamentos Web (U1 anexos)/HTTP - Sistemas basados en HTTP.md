# HTTP - Sistemas basados en HTTP

## Definición
Ecosistema de componentes que interactúan utilizando el protocolo HTTP para el intercambio de información en la Web, siguiendo un modelo cliente-servidor.

## Explicación
- *Qué problema resuelve*
    Permite que una página web no sea solo un archivo, sino una composición de múltiples recursos (texto, CSS, imágenes, scripts) obtenidos de forma independiente y eficiente.
- *Cómo funciona por arriba*
    El cliente (agente de usuario) inicia peticiones individuales. El servidor las gestiona y responde. En el medio, existen intermediarios (proxies, routers, módems) que facilitan el flujo.
- *Qué implica / qué permite*
    Implica una arquitectura en capas donde los dispositivos de red (routers) son transparentes para la capa de aplicación (HTTP). Permite la carga modular de sub-documentos para formar la experiencia final.

## Palabras clave
- Agente de usuario (User Agent)
- Servidor Web
- Proxies
- Arquitectura en capas
- Peticiones/Respuestas

## Comparaciones típicas
- vs [[HTTP - Características clave]]: este describe actores y capas (cliente/servidor/intermediarios); el otro describe reglas del protocolo (stateless, headers).
- vs [[Cliente-Servidor - Componentes]]: HTTP es un sistema cliente-servidor concreto; el otro define el modelo general y sus piezas.
- vs [[HTTP - Proxies]]: el proxy es un intermediario dentro del sistema; el sistema incluye muchos componentes (no solo proxies).

## Preguntas de examen
- ¿Qué elementos componen típicamente un sistema basado en HTTP?
- ¿Por qué se dice que los routers son "transparentes" para HTTP?
- ¿Cómo se forma una página web completa según este flujo?

## Errores comunes
- Pensar que la comunicación es un flujo continuo (son mensajes individuales).
- Olvidar que una sola página web puede disparar decenas de peticiones HTTP distintas.

## Mini-ejemplo (mental)
- Al entrar a una web, tu navegador pide el HTML. Al leerlo, ve que necesita un logo y un estilo CSS, así que hace dos peticiones más al servidor para completar la página.
