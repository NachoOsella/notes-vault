# Preguntas - Spring y Spring Boot

## Spring (Core)
- Que es Spring Framework y que problema busca resolver?
- Que significa "Spring" (framework vs ecosistema de proyectos)?
- Que es IoC y por que se dice "inversion de control"?
- Como se relacionan IoC y DI?
- Que es un Bean en Spring?
- Que scopes de beans conoces y cual es el default?
- Que es el `ApplicationContext` y que responsabilidades tiene?
- Para que sirve el component scanning?
- Diferencias entre `@Component`, `@Service`, `@Repository`, `@Controller`.
- Que hace `@Configuration` y para que se usa `@Bean`?
- Que es un profile y como se activa?
- Como funciona la configuracion por properties/yaml (fuentes y precedencia)?
- Que es AOP y que tipo de problemas suele resolver?

## Spring MVC (REST)
- Que es Spring MVC?
- Que rol cumple `DispatcherServlet`?
- Diferencia entre `@Controller` y `@RestController`.
- Para que se usan `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.?
- Diferencia entre `@PathVariable`, `@RequestParam` y `@RequestBody`.
- Que es un DTO y por que conviene usarlo?
- Que es Bean Validation y como se activa con `@Valid`?
- Que hace `@ControllerAdvice` y para que sirve `@ExceptionHandler`?
- Que es CORS y por que puede bloquear un frontend?

## Persistencia (JPA + Spring Data)
- Que es Spring Data JPA?
- Que es un Repository y que te ahorra escribir?
- Que es una derived query method y como se arma el nombre?
- Para que sirve `@Entity` y `@Id`?
- Diferencia entre `@OneToMany` y `@ManyToOne`.
- Que significa FetchType LAZY vs EAGER?
- Para que sirve Cascade y que riesgos tiene?
- Que hace `@Transactional` y por que suele implementarse con AOP?

## Spring Boot
- Que es Spring Boot y por que se usa?
- Que significa autoconfiguracion?
- Que es un "starter"?
- `application.properties` vs `application.yml`: ventajas y desventajas.
- Que hace `@ConfigurationProperties` y cuando conviene vs `@Value`?
- Como se ejecuta una app Spring Boot empaquetada como jar?
- Que es Actuator y para que sirve en runtime?

## Testing
- Para que sirve `@SpringBootTest` y cuando conviene usarlo?
- Que es MockMvc y que tipo de pruebas habilita?
- Que son los slice tests (`@WebMvcTest`, `@DataJpaTest`) y que aislan?

## Microservicios (U4)
- Que es un microservicio y en que se diferencia de un monolito?
- Diferencia entre microservicios y SOA (enfoque y alcance).
- Beneficios principales de microservicios (tecnicos y organizacionales).
- Desafios comunes al pasar a microservicios.
- Por que microservicios requieren DevOps/CI-CD?
- Que rol cumplen contenedores (Docker) y un orquestador (Kubernetes)?
- Para que sirve un API Gateway?
- Cuando conviene mensajeria/streaming de eventos vs llamadas REST?
- Que es "serverless" y en que se parece/difiere de microservicios?
- Explica el patron BFF.
- Que es el patron Strangler?
- Menciona antipatrones comunes (p. ej. microservicios demasiado chicos).

## Respuestas (opcional)

### Que es Spring Framework y que problema busca resolver?
Respuesta: Es un framework para aplicaciones Java que simplifica la arquitectura empresarial. Resuelve el acoplamiento fuerte y la complejidad de configuración.

### Que significa "Spring" (framework vs ecosistema de proyectos)?
Respuesta: Spring Framework es el núcleo (IoC, AOP, MVC), mientras que Spring como ecosistema incluye proyectos como Boot, Data, Security y Cloud.

### Que es IoC y por que se dice "inversion de control"?
Respuesta: IoC significa que el control de crear y cablear objetos pasa del código de negocio al contenedor de Spring.

### Como se relacionan IoC y DI?
Respuesta: DI es la forma práctica de aplicar IoC: el contenedor inyecta dependencias en vez de que la clase las instancie.

### Que es un Bean en Spring?
Respuesta: Es un objeto administrado por el contenedor de Spring, con ciclo de vida y dependencias gestionadas.

### Que scopes de beans conoces y cual es el default?
Respuesta: Los más comunes son singleton, prototype, request, session y application; el scope por defecto es singleton.

### Que es el `ApplicationContext` y que responsabilidades tiene?
Respuesta: Es el contenedor principal de Spring: crea beans, resuelve dependencias, maneja eventos y acceso a configuración.

### Para que sirve el component scanning?
Respuesta: Sirve para detectar automáticamente clases anotadas (`@Component` y derivadas) y registrarlas como beans.

### Diferencias entre `@Component`, `@Service`, `@Repository`, `@Controller`.
Respuesta: Todas registran beans, pero expresan rol: genérico (`@Component`), lógica de negocio (`@Service`), acceso a datos (`@Repository`) y capa web (`@Controller`).

### Que hace `@Configuration` y para que se usa `@Bean`?
Respuesta: `@Configuration` marca una clase de configuración; `@Bean` declara manualmente objetos que Spring debe gestionar.

### Que es un profile y como se activa?
Respuesta: Un profile permite cargar configuraciones según entorno (dev/test/prod). Se activa con `spring.profiles.active` o variable de entorno.

### Como funciona la configuracion por properties/yaml (fuentes y precedencia)?
Respuesta: Spring combina fuentes (archivos, variables de entorno, argumentos, etc.) y aplica precedencia: las fuentes más específicas sobrescriben las generales.

### Que es AOP y que tipo de problemas suele resolver?
Respuesta: AOP aplica lógica transversal sin ensuciar el negocio, como logs, seguridad, métricas, transacciones y auditoría.

### Que es Spring MVC?
Respuesta: Es el módulo web de Spring para construir apps HTTP/REST con patrón modelo-vista-controlador.

### Que rol cumple `DispatcherServlet`?
Respuesta: Es el front controller: recibe requests, decide qué controlador ejecutar y coordina la respuesta.

### Diferencia entre `@Controller` y `@RestController`.
Respuesta: `@Controller` suele devolver vistas; `@RestController` devuelve datos (JSON/XML) porque incluye `@ResponseBody` implícito.

### Para que se usan `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.?
Respuesta: Sirven para mapear rutas y métodos HTTP a métodos del controlador.

### Diferencia entre `@PathVariable`, `@RequestParam` y `@RequestBody`.
Respuesta: `@PathVariable` toma valores de la URL, `@RequestParam` de query/form y `@RequestBody` del cuerpo de la petición.

### Que es un DTO y por que conviene usarlo?
Respuesta: Es un objeto de transferencia de datos entre capas/API; evita exponer entidades internas y mejora validación/versionado.

### Que es Bean Validation y como se activa con `@Valid`?
Respuesta: Es la validación declarativa con anotaciones (`@NotNull`, `@Size`, etc.); se ejecuta al usar `@Valid` en parámetros.

### Que hace `@ControllerAdvice` y para que sirve `@ExceptionHandler`?
Respuesta: `@ControllerAdvice` centraliza lógica transversal de controladores; `@ExceptionHandler` define cómo convertir excepciones en respuestas HTTP.

### Que es CORS y por que puede bloquear un frontend?
Respuesta: CORS es la política del navegador para origen cruzado; bloquea requests si el backend no permite explícitamente ese origen/método/header.

### Que es Spring Data JPA?
Respuesta: Es una capa sobre JPA que reduce boilerplate de persistencia y facilita repositorios con interfaces.

### Que es un Repository y que te ahorra escribir?
Respuesta: Es una abstracción para acceso a datos; te ahorra implementar CRUD y consultas comunes manualmente.

### Que es una derived query method y como se arma el nombre?
Respuesta: Es una consulta generada por nombre de método, por ejemplo `findByEmailAndActivoTrue`, siguiendo convenciones de propiedades.

### Para que sirve `@Entity` y `@Id`?
Respuesta: `@Entity` marca una clase persistible en tabla y `@Id` define su clave primaria.

### Diferencia entre `@OneToMany` y `@ManyToOne`.
Respuesta: `@OneToMany` modela una entidad con muchos hijos; `@ManyToOne` modela muchos registros que apuntan a un padre.

### Que significa FetchType LAZY vs EAGER?
Respuesta: LAZY carga relaciones bajo demanda; EAGER las carga junto con la entidad principal.

### Para que sirve Cascade y que riesgos tiene?
Respuesta: Cascade propaga operaciones (persist/remove/etc.) a entidades relacionadas. Mal usado puede borrar o modificar datos no deseados.

### Que hace `@Transactional` y por que suele implementarse con AOP?
Respuesta: Delimita una transacción con commit/rollback automáticos. Se implementa con AOP para envolver métodos sin acoplar lógica transaccional.

### Que es Spring Boot y por que se usa?
Respuesta: Es una capa de Spring que acelera el arranque con convención sobre configuración y servidor embebido.

### Que significa autoconfiguracion?
Respuesta: Spring Boot configura beans automáticamente según dependencias y propiedades presentes en el proyecto.

### Que es un "starter"?
Respuesta: Es una dependencia agregadora que trae un conjunto coherente de librerías para una capacidad (web, data, security, etc.).

### `application.properties` vs `application.yml`: ventajas y desventajas.
Respuesta: `properties` es simple y explícito; `yml` es más legible para estructuras jerárquicas pero sensible a indentación.

### Que hace `@ConfigurationProperties` y cuando conviene vs `@Value`?
Respuesta: Mapea grupos de propiedades tipadas a una clase; conviene para configs grandes, mientras `@Value` sirve para valores puntuales.

### Como se ejecuta una app Spring Boot empaquetada como jar?
Respuesta: Se ejecuta con `java -jar nombre-app.jar`, levantando el servidor embebido y el contexto de Spring.

### Que es Actuator y para que sirve en runtime?
Respuesta: Expone endpoints operativos (health, metrics, info, etc.) para monitoreo, observabilidad y diagnóstico en producción.

### Para que sirve `@SpringBootTest` y cuando conviene usarlo?
Respuesta: Levanta el contexto completo para pruebas de integración. Conviene cuando querés validar interacción real entre capas.

### Que es MockMvc y que tipo de pruebas habilita?
Respuesta: Permite testear controladores HTTP sin servidor real, verificando status, headers y payload de respuestas.

### Que son los slice tests (`@WebMvcTest`, `@DataJpaTest`) y que aislan?
Respuesta: Son tests acotados por capa: `@WebMvcTest` aísla web/controladores y `@DataJpaTest` aísla persistencia/repositorios.

### Que es un microservicio y en que se diferencia de un monolito?
Respuesta: Es un servicio pequeño y desplegable de forma independiente; un monolito concentra todo en una sola aplicación/unidad de despliegue.

### Diferencia entre microservicios y SOA (enfoque y alcance).
Respuesta: SOA suele ser más empresarial y centralizada (ESB), mientras microservicios priorizan autonomía, despliegue independiente y menor acoplamiento.

### Beneficios principales de microservicios (tecnicos y organizacionales).
Respuesta: Escalado por servicio, despliegues más rápidos, aislamiento de fallos y equipos autónomos alineados por dominio.

### Desafios comunes al pasar a microservicios.
Respuesta: Aumentan complejidad operativa, observabilidad, consistencia de datos, latencia de red y necesidad de automatización.

### Por que microservicios requieren DevOps/CI-CD?
Respuesta: Porque hay muchos servicios que construir, testear, desplegar y monitorear continuamente de forma confiable.

### Que rol cumplen contenedores (Docker) y un orquestador (Kubernetes)?
Respuesta: Docker empaqueta ejecución consistente; Kubernetes coordina despliegue, escalado, networking y autorecuperación.

### Para que sirve un API Gateway?
Respuesta: Centraliza entrada a APIs: ruteo, autenticación, rate limiting, agregación y políticas transversales.

### Cuando conviene mensajeria/streaming de eventos vs llamadas REST?
Respuesta: Mensajería/eventos conviene para desacoplar y procesos asíncronos; REST para consulta/comando inmediato y respuesta directa.

### Que es "serverless" y en que se parece/difiere de microservicios?
Respuesta: Serverless ejecuta funciones administradas por proveedor y escala automática; comparte modularidad con microservicios pero con menor control de infraestructura.

### Explica el patron BFF.
Respuesta: Backend For Frontend crea un backend específico por cliente (web/móvil) para adaptar datos y reducir complejidad en frontend.

### Que es el patron Strangler?
Respuesta: Es una migración gradual donde partes del monolito se reemplazan por servicios nuevos hasta retirar el sistema viejo.

### Menciona antipatrones comunes (p. ej. microservicios demasiado chicos).
Respuesta: Microservicios demasiado finos, base de datos compartida entre servicios, comunicación síncrona excesiva y falta de observabilidad.
