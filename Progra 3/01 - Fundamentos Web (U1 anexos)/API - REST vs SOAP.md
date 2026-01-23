# REST vs SOAP

## Definición
Comparativa entre los dos estilos predominantes para la implementación de servicios web: REST (estilo arquitectónico ligero) y SOAP (protocolo estándar estructurado).

## Explicación
- *Qué problema resuelve*
    Ofrecen diferentes enfoques para la comunicación entre sistemas. REST prioriza la simplicidad y el rendimiento en la web, mientras que SOAP prioriza la seguridad formal y la fiabilidad en entornos corporativos.
- *Cómo funciona por arriba*
    REST usa verbos HTTP y JSON sobre URLs. SOAP encapsula cada mensaje en un "sobre" XML (Envelope) con reglas estrictas y suele requerir un contrato formal (WSDL).
- *Qué implica / qué permite*
    REST permite un desarrollo rápido y eficiente para aplicaciones web/móviles. SOAP permite transacciones complejas y seguridad avanzada (WS-Security) necesaria en banca o sistemas gubernamentales.

## Palabras clave
- Protocolo (SOAP) vs Estilo (REST)
- XML vs JSON
- WSDL
- Verbosidad
- WS-Security

## Comparaciones típicas
- **Formato:** REST usa JSON (ligero); SOAP usa exclusivamente XML (pesado/verboso).
- **Transporte:** REST usa casi siempre HTTP; SOAP puede usar HTTP, SMTP, JMS, etc.
- **Acoplamiento:** SOAP es más rígido (contrato WSDL); REST es más flexible y orientado a recursos.
- vs [[API - Qué es un Servicio Web]]: REST y SOAP son dos enfoques comunes para implementar servicios web.
- vs [[HTTP - Métodos de solicitud]]: REST explota verbos HTTP y semántica de recursos; SOAP no depende del modelo de verbos HTTP.

## Preguntas de examen
- ¿Cuál es el formato de datos exclusivo de SOAP?
- ¿Por qué REST suele tener mejor rendimiento en la web?
- ¿En qué casos se sigue prefiriendo SOAP sobre REST?
- ¿Qué es el WSDL en SOAP?

## Errores comunes
- Pensar que REST es siempre mejor (SOAP es superior en seguridad transaccional integrada).
- Creer que REST solo soporta JSON (también puede usar XML, aunque no es lo común).

## Mini-ejemplo (mental)
- REST es como enviar una postal (rápido, simple, directo). SOAP es como enviar un sobre certificado con sello de cera y un contrato legal adentro (pesado, pero muy seguro y formal).
