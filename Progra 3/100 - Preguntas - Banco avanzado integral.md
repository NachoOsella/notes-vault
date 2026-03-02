# Preguntas - Banco avanzado integral

## Fundamentos Web (arquitectura, HTTP y APIs)
- ¿Qué consecuencias de diseño tiene que HTTP sea stateless cuando necesitás continuidad de sesión y trazabilidad?
- Si un endpoint recibe reintentos automáticos por timeout, ¿cómo garantizás idempotencia real en operaciones de escritura?
- ¿Cuándo usarías `PUT` vs `PATCH` en una API REST y cómo cambia eso la estrategia de validación?
- ¿Qué riesgos aparecen si devolvés siempre `200 OK` y codificás errores en el body?
- ¿Cómo modelarías correctamente errores de dominio para diferenciar `400`, `404`, `409` y `422`?
- ¿Qué tradeoffs hay entre versionado de API por URI (`/v1`) vs headers?
- ¿Cómo afectan proxies y caches intermedias al diseño de headers (`Cache-Control`, `ETag`, `Vary`)?
- ¿En qué escenarios conviene exponer recursos anidados vs recursos planos con filtros?
- ¿Qué rompe en un sistema si ignorás semántica HTTP y tratás todos los endpoints como RPC?
- ¿Cuándo preferís REST sobre SOAP hoy, y en qué casos SOAP sigue siendo razonable?
- ¿Qué diferencia práctica hay entre autenticación y autorización al diseñar una API pública?
- ¿Cómo justificarías técnicamente CORS como política del navegador y no del protocolo HTTP?

## Front End U1/U2 (HTML, CSS, DOM, eventos y browser)
- ¿Qué impacto real tiene usar HTML semántico en accesibilidad, SEO y mantenibilidad?
- ¿Cómo diagnosticarías y reducirías reflows/repaints excesivos en una UI dinámica?
- ¿Cuándo `position: sticky` falla en layouts reales y por qué?
- ¿Qué problemas de UX puede introducir un diseño “responsive” basado solo en breakpoints de ancho?
- ¿Cómo cambia el flujo de eventos si combinás captura, bubbling y `stopPropagation()` en componentes anidados?
- ¿Qué diferencias de costo hay entre delegación de eventos y listeners por nodo en listas grandes?
- ¿Cómo evitar condiciones de carrera cuando dos `fetch` actualizan el mismo estado del DOM?
- ¿Qué patrones usás para cancelar requests en curso al navegar entre vistas?
- ¿Qué compromisos de seguridad implica usar `innerHTML` con contenido no confiable?
- ¿Cuándo `localStorage`, `sessionStorage` y cookies son una mala elección aunque “funcionen”?
- ¿Cómo diseñarías expiración y revocación de sesión si solo contás con capacidades del navegador?
- ¿Qué ventajas y limitaciones tiene modelar asincronismo con Promises frente a streams de eventos?

## TypeScript y tooling
- ¿Cómo decidir entre `interface` y `type` en un dominio que evoluciona con frecuencia?
- ¿Qué riesgos reales introduce `any` en refactors grandes y cómo migrar fuera de `any` gradualmente?
- ¿Cómo usarías tipos de unión y narrowing para modelar estados de UI sin flags inconsistentes?
- ¿Qué errores evita `strictNullChecks` y por qué suele romper código legacy al activarlo?
- ¿Cuándo conviene usar `readonly` para forzar inmutabilidad a nivel de diseño?
- ¿Qué diferencia conceptual hay entre herencia (`extends`) y composición tipada en TS?
- ¿Cómo diseñarías contratos de DTO compartidos entre frontend y backend sin acoplamiento frágil?
- ¿Qué problemas evita separar tipos de runtime (validación) y tipos estáticos (compilación)?
- ¿Qué impacto tiene `tsconfig` en calidad de código más allá de “compilar o no compilar”?
- ¿Cómo justificarías usar `unknown` en lugar de `any` para entradas externas?
- ¿Qué tradeoff hay entre APIs muy genéricas con generics vs APIs explícitas más verbosas?
- ¿Cómo evitarías romper consumidores al reorganizar exports/imports en un proyecto grande?

## Angular + RxJS (arquitectura, estado, formularios)
- ¿Qué criterio usarías para decidir si una funcionalidad va en componente, servicio o feature module?
- ¿Qué ventajas y costos trae usar Standalone Components frente a organización modular clásica?
- ¿Cómo evitás memory leaks por suscripciones en componentes de vida corta?
- ¿Cuándo un `BehaviorSubject` para estado compartido se vuelve anti-patrón?
- ¿Qué bug típico aparece al encadenar requests HTTP sin `switchMap`?
- ¿Cómo compararías `switchMap`, `mergeMap` y `concatMap` en términos de concurrencia y consistencia?
- ¿Qué diferencia hay entre manejar errores en `subscribe` vs dentro del pipeline (`catchError`)?
- ¿Cómo modelarías retries sin duplicar efectos colaterales en operaciones no idempotentes?
- ¿Qué señales indican que un componente está haciendo demasiada lógica de negocio?
- ¿Cuándo preferís reactive forms sobre template-driven forms en términos de testabilidad?
- ¿Cómo diseñar validaciones asincrónicas sin degradar UX ni saturar backend?
- ¿Qué problemas de rendimiento pueden aparecer con `ngFor` sin estrategia de tracking?
- ¿Cómo impacta el ciclo de vida del componente en integración con librerías externas?
- ¿Cuándo crearías un pipe personalizado y cuándo debería ser una función utilitaria?
- ¿Cómo diseñar comunicación entre componentes lejanos evitando acoplamiento por eventos en cadena?
- ¿Qué estrategia usarías para testear flujos RxJS complejos de forma determinística?

## Java y Colecciones
- ¿Qué criterio usarías para elegir entre `ArrayList` y `LinkedList` en un caso real y no teórico?
- ¿Cómo afecta `equals`/`hashCode` mal implementado al comportamiento de `HashSet` y `HashMap`?
- ¿Cuándo `TreeMap` justifica su costo frente a `HashMap`?
- ¿Qué problemas de concurrencia aparecen al compartir colecciones mutables entre hilos?
- ¿Cómo evitarías `NullPointerException` sistemáticamente en una API de dominio?
- ¿Qué tradeoffs existen entre arrays primitivos y colecciones boxed en performance/memoria?
- ¿Cómo decidir entre diseño orientado a objetos puro y estructuras de datos más directas?
- ¿Qué señales muestran que una clase viola SRP aunque “funcione”?
- ¿Cómo diseñarías una jerarquía de excepciones útil para capa de servicio?
- ¿Qué ventajas concretas trae encapsular colecciones en lugar de exponerlas directamente?

## Maven, Testing y Mockito
- ¿Cómo impactan dependencias transitivas no controladas en seguridad y estabilidad del build?
- ¿Qué diferencia práctica hay entre `mvn test` y `mvn verify` en pipelines CI?
- ¿Cómo definirías una estrategia de versionado de dependencias para minimizar regresiones?
- ¿Qué anti-patrón aparece cuando los tests unitarios dependen de detalles internos de implementación?
- ¿Cuándo un mock es correcto y cuándo te está ocultando un problema de diseño?
- ¿Qué riesgos trae abusar de `spy` sobre clases complejas?
- ¿Cómo escribirías tests que resistan refactors sin perder sensibilidad a bugs reales?
- ¿Qué cobertura falta cuando solo testeás “happy path” con Mockito?
- ¿Cómo diseñarías tests de excepción para validar mensaje, tipo y contexto útil?
- ¿Qué diferencia hay entre validar interacciones (`verify`) y validar estado final?
- ¿Cómo evitar tests flaky cuando hay tiempo, asincronismo o IO involucrado?
- ¿Cuándo usarías tests de integración aunque ya tengas alta cobertura unitaria?

## Algoritmos y complejidad
- ¿Cómo justificarías una solución O(n²) si el dominio parece exigir O(n log n)?
- ¿Qué trampas comunes aparecen al estimar complejidad ignorando estructura de datos subyacente?
- ¿Cómo cambia la elección algorítmica cuando el cuello es memoria y no CPU?
- ¿Cuándo la búsqueda binaria deja de ser óptima en sistemas reales con datos no estáticos?
- ¿Cómo compararías top-down memoization vs bottom-up DP en costo y mantenibilidad?
- ¿Qué condiciones tienen que cumplirse para que greedy sea correcto y no solo rápido?
- ¿Cómo detectarías que un problema necesita backtracking en vez de divide and conquer?
- ¿Qué heurísticas usarías para podar ramas en backtracking sin perder completitud?
- ¿Cómo argumentarías formalmente que una optimización no altera la correctitud del algoritmo?
- ¿Qué diferencia conceptual hay entre complejidad amortizada y peor caso?
- ¿Cómo evaluarías tradeoffs entre exactitud y rendimiento en problemas NP-hard?
- ¿Qué costo oculto introduce la recursión profunda y cómo lo mitigás?
- ¿Cómo diseñar benchmarks de algoritmos evitando sesgos de entrada “fáciles”?
- ¿Qué errores de interpretación de Big-O son más frecuentes en entrevistas/orales?

## Spring, Spring Boot, JPA y arquitectura
- ¿Qué diferencia real hay entre IoC y DI cuando se baja a código concreto?
- ¿Cómo decidirías entre inyección por constructor, campo o setter en una app enterprise?
- ¿Qué riesgos introduce un uso excesivo de `@Autowired` implícito sin contratos claros?
- ¿Cuándo un `@RestController` debería devolver entidad, DTO o proyección?
- ¿Cómo diseñarías manejo global de errores consistente para toda la API?
- ¿Qué límites pondrías entre Controller, Service y Repository para evitar lógica cruzada?
- ¿Cómo evitarías exponer detalles internos de persistencia en contratos REST?
- ¿Qué problemas aparecen con `FetchType.EAGER` en relaciones complejas?
- ¿Cuándo usar cascade ayuda y cuándo produce borrados/actualizaciones peligrosas?
- ¿Cómo elegir nivel de aislamiento transaccional según tipo de inconsistencia tolerable?
- ¿Qué diferencia hay entre validación de entrada (API) y validación de reglas de negocio (dominio)?
- ¿Cuándo una derived query method deja de escalar y conviene pasar a query explícita?
- ¿Qué estrategia usarías para paginación estable bajo escrituras concurrentes?
- ¿Cómo separar configuración por ambiente sin duplicación y sin filtrar secretos?
- ¿Qué criterios usarías para exponer endpoints de Actuator en producción?
- ¿Cómo decidir entre `RestTemplate` y `WebClient` en un servicio I/O intensivo?
- ¿Qué validarías con `@SpringBootTest` que un slice test no cubre?
- ¿Cómo diseñarías tests de repositorio para detectar problemas de mapeo JPA temprano?

## Microservicios, integración y operación
- ¿Cuándo un monolito modular es técnicamente superior a microservicios?
- ¿Qué señales objetivas indican que un bounded context merece extraerse como servicio?
- ¿Cómo evitarías acoplamiento temporal entre servicios síncronos?
- ¿Qué estrategia usarías para consistencia de datos sin transacciones distribuidas?
- ¿Cuándo elegirías eventos asíncronos frente a llamadas REST directas?
- ¿Qué riesgos operativos aparecen al multiplicar servicios sin observabilidad madura?
- ¿Cómo diseñarías trazabilidad end-to-end para debugging distribuido?
- ¿Qué métricas mínimas exigirías antes de escalar una arquitectura a microservicios?
- ¿Cómo usarías un API Gateway sin convertirlo en punto único de falla lógica?
- ¿Qué rol cumple BFF cuando hay múltiples clientes (web, mobile, admin)?
- ¿Cómo aplicarías Strangler Pattern minimizando riesgo de regresión funcional?
- ¿Qué anti-patrón ves en “microservicios demasiado pequeños” y cómo lo medís?
- ¿Cómo diseñarías despliegues progresivos (blue/green o canary) en un pipeline CI/CD?
- ¿Qué estrategia usarías para versionar contratos entre servicios sin romper consumidores?
- ¿Cómo abordarías resiliencia: timeouts, retries, circuit breaker y bulkheads en conjunto?
- ¿Qué cambia en seguridad cuando pasás de app monolítica a malla de servicios?

## Preguntas integradoras de oral (cruce de unidades)
- ¿Cómo conectás decisiones de modelado HTTP en frontend con transacciones en backend?
- ¿Qué relación hay entre calidad de tipos en TypeScript y estabilidad de contratos API en Spring?
- ¿Cómo justificarías una decisión de arquitectura usando costo algorítmico y costo operativo a la vez?
- ¿Qué errores de diseño se detectan tarde si no combinás tests unitarios, de integración y E2E?
- ¿Cómo defenderías técnicamente una solución completa desde navegador hasta base de datos?
- ¿Qué tradeoff priorizarías primero ante conflicto entre rendimiento, mantenibilidad y time-to-market?

## Respuestas (opcional)

> Banco de respuestas completo:
> [[101 - Respuestas - Banco avanzado integral]]

![[101 - Respuestas - Banco avanzado integral]]
