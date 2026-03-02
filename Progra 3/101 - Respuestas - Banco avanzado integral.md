# Respuestas - Banco avanzado integral

## Fundamentos Web (arquitectura, HTTP y APIs)
1. HTTP stateless obliga a externalizar estado (token/sesión), diseñar idempotencia y correlación (`X-Request-Id`) para observabilidad.
2. Con claves de idempotencia persistidas por operación (`Idempotency-Key`) y deduplicación transaccional.
3. `PUT` reemplaza recurso completo e idealmente es idempotente; `PATCH` aplica cambios parciales y requiere validar coherencia parcial.
4. Perdés semántica protocolo, rompés caches/proxies/retries y complicás clientes automáticos.
5. `400` sintaxis inválida, `404` no existe, `409` conflicto de estado, `422` semántica inválida con formato correcto.
6. URI simplifica gateway/caching; headers reducen ruido de URL pero complican tooling y debugging.
7. Debés controlar frescura/variantes con `Cache-Control`, validación condicional (`ETag`) y `Vary` para evitar respuestas incorrectas.
8. Anidados cuando la relación padre-hijo es fuerte; planos con filtros cuando necesitás consultas cruzadas y menor acoplamiento de rutas.
9. Se pierde uniform interface, crece acoplamiento cliente-servidor y se reduce interoperabilidad HTTP.
10. REST para APIs web livianas y ecosistema JSON; SOAP cuando necesitás contrato estricto WS-* o integración enterprise legacy.
11. Autenticación verifica identidad; autorización define permisos sobre recursos/acciones concretas.
12. CORS lo impone el navegador para scripts cross-origin; no es restricción intrínseca del servidor HTTP entre backends.

## Front End U1/U2 (HTML, CSS, DOM, eventos y browser)
1. Mejora accesibilidad por roles implícitos, SEO por estructura semántica y mantenibilidad por claridad del documento.
2. Midiendo con DevTools Performance, minimizando cambios de layout, batch de escrituras DOM y uso de transform/opacity.
3. Falla por contenedor con `overflow`, falta de espacio de scroll o contexto de apilamiento no esperado.
4. Ignora densidad táctil, altura útil y contexto; puede verse correcto en ancho pero romper interacción real.
5. Captura ejecuta ancestros hacia abajo, target en nodo objetivo, bubbling sube; `stopPropagation` corta cadena posterior.
6. Delegación usa menos memoria y escala mejor; listeners por nodo facilitan aislamiento pero degradan en listas masivas.
7. Con cancelación (`AbortController`), secuenciación por versión de estado y descartando respuestas obsoletas.
8. `AbortController`, limpieza en desmontaje y políticas “latest wins” por navegación.
9. Riesgo XSS; mitigás con sanitización estricta, plantillas seguras y CSP.
10. Son malas para secretos sensibles, datos grandes o requerimientos fuertes de expiración/seguridad.
11. Cookie `HttpOnly` + expiración corta + rotación de tokens + invalidación server-side.
12. Promises modelan una resolución puntual; streams modelan múltiples eventos en el tiempo con composición reactiva.

## TypeScript y tooling
1. `interface` para contratos extensibles; `type` para uniones/intersecciones y modelado más expresivo.
2. `any` oculta errores de tipos y rompe refactors; migrás con `unknown`, tipos incrementales y reglas estrictas por módulo.
3. Con uniones discriminadas (`status: 'idle'|'loading'|...`) evitás combinaciones inválidas de flags.
4. Evita null/undefined accidentales en runtime; rompe legacy porque fuerza manejo explícito de ausencia.
5. Cuando el dominio no debe mutar tras creación (DTOs, config, estado derivado).
6. Herencia acopla jerarquía; composición tipada favorece flexibilidad y menor impacto de cambios.
7. Contrato compartido versionado (OpenAPI/schemas) + generación de tipos para evitar divergencia manual.
8. El tipado no valida runtime; separar evita confiar en datos externos no validados.
9. `tsconfig` define rigor del proyecto (strictness, module resolution, checks) y previene deuda técnica.
10. `unknown` obliga a validar antes de usar, manteniendo seguridad de tipos.
11. Genericidad excesiva complica lectura; APIs explícitas reducen flexibilidad pero mejoran claridad operativa.
12. Barrel files controlados, contratos públicos estables y deprecación gradual con compatibilidad temporal.

## Angular + RxJS (arquitectura, estado, formularios)
1. UI en componente, reglas de negocio en servicio y organización por feature cuando crece dominio/equipo.
2. Standalone reduce boilerplate y facilita lazy loading; requiere disciplina de imports y límites por feature.
3. `takeUntilDestroyed`, `async` pipe y cleanup explícito en recursos externos.
4. Cuando se vuelve store global improvisado sin eventos de dominio ni trazabilidad.
5. Respuestas viejas pisan estado nuevo (race condition).
6. `switchMap` cancela previos, `mergeMap` paraleliza, `concatMap` serializa manteniendo orden.
7. En `subscribe` tratás borde final; en pipeline componés recuperación/reintentos de forma reutilizable.
8. Retries condicionados + idempotency keys + separación entre efectos de escritura y lectura.
9. Muchos `if` de dominio, llamadas HTTP directas y estado compartido no encapsulado.
10. Reactive forms para formularios complejos/dinámicos y mejor test unitario.
11. Debounce + distinct + cancelación de request + feedback de estado al usuario.
12. Re-render innecesario; mitigás con `trackBy`/`@for(...; track ...)`.
13. Inicialización/destrucción incorrecta causa fugas, dobles handlers o estados inconsistentes.
14. Pipe para presentación pura en template; utilitaria para lógica reutilizable fuera de vista.
15. Servicio mediador (facade/store) en vez de cadenas largas de `@Output`.
16. Marble tests/TestScheduler para controlar tiempo y emisiones.

## Java y Colecciones
1. En práctica, `ArrayList` suele ganar por locality; `LinkedList` solo si hay inserciones/borrados frecuentes con iterador posicionado.
2. Rompe unicidad y lookup: objetos “iguales” pueden duplicarse o no encontrarse.
3. Cuando necesitás orden natural/rango y operaciones logarítmicas previsibles.
4. Race conditions, corrupción de estado y `ConcurrentModificationException`.
5. Diseñando contratos no-null, validación temprana y uso cuidadoso de `Optional`.
6. Arrays primitivos ahorran memoria/boxing; colecciones aportan flexibilidad y APIs ricas.
7. OO cuando importa modelado de dominio; estructuras directas cuando prima simplicidad/performance crítica.
8. Múltiples razones de cambio, dependencias cruzadas y métodos con responsabilidades mixtas.
9. Excepciones de dominio claras, separadas de técnicas, con contexto accionable.
10. Protege invariantes, evita mutaciones externas y facilita evolución interna.

## Maven, Testing y Mockito
1. Pueden introducir CVEs y conflictos de versión invisibles si no fijás/inspeccionás árbol de dependencias.
2. `test` ejecuta pruebas; `verify` además valida fases posteriores de calidad/integración del ciclo.
3. BOM/dependencyManagement + actualizaciones controladas + CI con pruebas/regresión.
4. Tests frágiles atados a implementación interna en vez de comportamiento observable.
5. Mock correcto en dependencia externa/no determinista; malo si reemplaza demasiada lógica del SUT.
6. `spy` puede ejecutar código real inesperado y volver tests frágiles/lentos.
7. Verificando comportamiento público, datos representativos y límites, no detalles internos.
8. Casos de error, bordes, concurrencia y contratos de integración.
9. Aserción de tipo de excepción, mensaje clave y efecto colateral esperado.
10. `verify` valida colaboración; estado final valida resultado funcional.
11. Aislando tiempo/IO, datos determinísticos y evitando dependencias de entorno.
12. Para validar wiring real, queries, serialización y configuración framework.

## Algoritmos y complejidad
1. Si restricciones reales (n pequeño, deadlines, claridad) priorizan entrega correcta mantenible.
2. Asumir `O(1)` en estructuras que degradan o ignorar costos de hash/resize/memoria.
3. Preferís algoritmos más compactos o streaming aunque aumente CPU si RAM es crítica.
4. Si los datos cambian, no están ordenados o el costo de mantener orden supera beneficio.
5. Top-down es más expresivo; bottom-up suele usar menos overhead y controlar mejor memoria.
6. Debe existir propiedad de elección local óptima que garantice óptimo global.
7. Si necesitás explorar combinaciones con restricciones y posibilidad de deshacer decisiones.
8. Bound heurístico, orden de variables y poda por factibilidad/costo mínimo restante.
9. Con invariantes, pruebas de equivalencia de estados y tests de regresión sobre casos límite.
10. Amortizada promedia secuencias; peor caso acota operación individual máxima.
11. Definiendo SLA de calidad y aceptando aproximaciones cuando exacto es inviable.
12. Riesgo stack overflow y overhead de llamadas; mitigás con iterativo o tail-call donde aplique.
13. Con datasets variados (peor/promedio/mejor), warmup y medición repetida controlada.
14. Confundir crecimiento asintótico con tiempo absoluto y olvidar constantes/contexto.

## Spring, Spring Boot, JPA y arquitectura
1. IoC es principio de control externo; DI es mecanismo concreto para inyectar dependencias.
2. Constructor por inmutabilidad/testabilidad; setter para opcionales; campo se evita por acoplamiento oculto.
3. Dependencias implícitas, difícil testeo y contratos difusos entre capas.
4. DTO casi siempre; entidad solo en casos internos controlados para no filtrar modelo persistente.
5. `@ControllerAdvice` + esquema de error estándar + mapeo consistente de excepciones.
6. Controller orquesta HTTP, Service reglas de negocio, Repository acceso a datos.
7. Mapeando entidad->DTO y evitando serializar relaciones/lazy internamente.
8. N+1 queries, sobrecarga de memoria y latencia innecesaria.
9. Ayuda en agregados coherentes; peligroso en relaciones amplias con borrados en cascada no deseados.
10. Según anomalías tolerables (dirty/non-repeatable/phantom) y costo de bloqueo.
11. Entrada valida formato/contrato; dominio valida invariantes de negocio.
12. Cuando nombres son inlegibles o consultas complejas: usar `@Query`/Specification/QueryDSL.
13. Cursor o keyset pagination para evitar saltos/duplicados bajo concurrencia.
14. Profiles + config centralizada + secretos en vault/env, no en repositorio.
15. Solo health/info mínimos autenticados; métricas sensibles restringidas por red/roles.
16. `WebClient` para no bloqueante/alto I/O; `RestTemplate` en apps simples legacy.
17. Contexto completo, wiring real, configuración, transacciones e integración entre capas.
18. `@DataJpaTest` con DB real de prueba y casos de relaciones/fetch/cascadas.

## Microservicios, integración y operación
1. Cuando dominio y equipo no justifican complejidad distribuida; monolito modular reduce costo operativo.
2. Alta cohesión interna, límites de cambio claros y necesidad de escalar/desplegar independiente.
3. Con asincronía, colas/eventos y tolerancia a degradación parcial.
4. Sagas, outbox pattern y compensaciones de negocio.
5. Eventos para desacople y resiliencia; REST para consultas síncronas de baja latencia.
6. Incidentes más difíciles, debugging distribuido y costos de plataforma crecientes.
7. Correlation IDs, tracing distribuido, logs estructurados y métricas por servicio.
8. Latencia p95/p99, error rate, MTTR, throughput y costo operativo por servicio.
9. Manteniendo lógica mínima, políticas transversales y redundancia/HA.
10. BFF adapta contrato/latencia por canal y evita lógica de presentación duplicada.
11. Extrayendo por verticales, con contratos estables y migración gradual de tráfico.
12. Exceso de llamadas/red y overhead de despliegue; medir por tamaño, autonomía y frecuencia de cambio.
13. Con feature flags, observabilidad fuerte y rollback automatizado.
14. Versionado semántico de contratos, compatibilidad backward y deprecación planificada.
15. Timeouts primero, retries con backoff, circuit breaker para fallas repetidas y bulkheads para aislamiento.
16. Aumenta superficie de ataque: identidad servicio-a-servicio, mTLS, secretos y políticas Zero Trust.

## Preguntas integradoras de oral (cruce de unidades)
1. HTTP define contrato externo; transacciones aseguran consistencia interna del cambio pedido por ese contrato.
2. Tipos estrictos en cliente reducen requests inválidas y estabilizan evolución de contratos backend.
3. Comparando complejidad algorítmica (CPU/RAM) con complejidad operativa (deploy, observabilidad, costo humano).
4. Bugs de contrato, configuración, integración y UX aparecen tarde sin pirámide de tests balanceada.
5. Explicando flujo completo: evento UI -> validación -> API -> servicio -> transacción -> persistencia -> respuesta.
6. Primero mantenibilidad mínima y correctitud; luego optimización guiada por métricas reales.
