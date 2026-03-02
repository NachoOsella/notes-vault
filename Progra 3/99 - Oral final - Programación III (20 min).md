# Oral final - Programación III (20 min)

## Objetivo del oral
- Mostrar dominio integral del recorrido: fundamentos web -> frontend -> backend -> arquitectura moderna con Spring y microservicios.
- Explicar decisiones técnicas (no solo definiciones): por qué se usa cada tecnología y qué tradeoff resuelve.

## Guion cronometrado (20 minutos)

### 0:00-1:30 | Apertura y mapa general
- "Voy a recorrer Programación III desde la base de la web hasta una solución moderna full stack."
- "La secuencia es: Fundamentos Web, Front End, Back End Java, Testing/Algoritmos y Spring Boot con microservicios."
- "La idea central es conectar conceptos: protocolo -> interfaz -> lógica -> persistencia -> despliegue."

### 1:30-4:00 | Fundamentos Web (U1 anexos)
- Arquitectura cliente-servidor: cliente solicita, servidor responde, cada uno con responsabilidades separadas.
- HTTP: protocolo stateless; request (método, URL, headers, body) y response (estado, headers, body).
- Métodos y códigos clave: GET/POST/PUT/PATCH/DELETE y familias 2xx, 4xx, 5xx.
- APIs: contrato de comunicación entre sistemas. REST como estilo orientado a recursos; comparación breve con SOAP.
- Cierre puente: "Con esto, ya tengo cómo viajan los datos; ahora paso a cómo se construye la interfaz."

### 4:00-8:30 | Front End (FE U1, U2, U3, U4)
- FE U1 (HTML/CSS/JS): estructura semántica, estilos (box model, responsive), lógica base con funciones y control de flujo.
- FE U2 (DOM + HTTP + asincronismo): manipulación del DOM, eventos (capturing/target/bubbling), Fetch API y Promises.
- Persistencia en cliente: localStorage vs sessionStorage vs cookies (incluyendo impacto en seguridad).
- FE U3 (TypeScript): tipado estático, interfaces, clases, módulos, `tsconfig`, npm; mejora mantenibilidad y reduce errores.
- FE U4 (Angular + RxJS): SPA, componentes (standalone), data binding, servicios, HttpClient, directivas, pipes, formularios.
- RxJS: observables, operadores y diferencia Subject vs BehaviorSubject para estado compartido.
- Cierre puente: "El frontend consume APIs; ahora explico cómo se diseñan y prueban en backend."

### 8:30-11:30 | Back End U1 (Java y Colecciones)
- Java y JVM: portabilidad por bytecode (WORA), rol de JDK/JRE/JVM.
- Sintaxis, tipos, scope y control de flujo como base del lenguaje.
- Estructuras: arrays vs colecciones.
- List/Set/Map: cuándo elegir cada una.
- Comparaciones típicas: ArrayList vs LinkedList, HashMap vs TreeMap, HashSet para unicidad.

### 11:30-14:00 | Back End U2 (Maven y Testing)
- Maven: `pom.xml`, ciclo de vida, plugins, dependencias y transitivas.
- Testing: diferencia unitario e integración; patrón Arrange-Act-Assert.
- JUnit: estructura de pruebas y aserciones.
- Mockito: mock, spy, `@InjectMocks`, stubbing (`when/thenReturn/thenThrow`) y verificación (`verify`).
- Idea fuerte: "Sin testing, el cambio es riesgoso; con testing, el cambio es controlado."

### 14:00-16:00 | Back End U3 (Algoritmos y complejidad)
- Qué es un algoritmo y cómo se evalúa su eficiencia.
- Big-O: O(1), O(n), O(log n), O(n²) y orden relativo de eficiencia.
- Búsqueda lineal vs binaria (tradeoff: binaria requiere datos ordenados).
- Caso Fibonacci: recursivo naive vs programación dinámica (memoización/bottom-up).
- Estrategias: divide and conquer, greedy, backtracking, programación dinámica.

### 16:00-19:30 | Spring, Spring Boot y Microservicios
- Spring Core: IoC/DI, beans, `ApplicationContext`, estereotipos y configuración.
- Spring MVC REST: `@RestController`, mappings, DTO, validación, manejo global de errores, CORS.
- Persistencia: JPA (`@Entity`, relaciones, fetch/cascade), repositories y `@Transactional`.
- Spring Boot: starters, autoconfiguración, configuración externa, Actuator, empaquetado `jar`.
- Testing en Spring: `@SpringBootTest`, MockMvc y slice tests.
- Microservicios: beneficios (escalabilidad/autonomía) y desafíos (complejidad operativa, observabilidad, CI/CD).
- Patrones: API Gateway, BFF, Strangler; antipatrones como microservicios demasiado pequeños.

### 19:30-20:00 | Cierre final
- "Programación III me da una visión de punta a punta: desde HTTP y el navegador hasta servicios escalables en Spring."
- "El criterio principal que me llevo es elegir tecnología por contexto: rendimiento, mantenibilidad, escalabilidad y calidad."

## Frases puente (para sonar fluido)
- "Esto se conecta con..."
- "La decisión técnica acá es..."
- "El tradeoff principal es..."
- "En un caso real, lo aplicaría así..."

## Mini banco de cierre (si te preguntan '¿qué fue lo más importante?')
- Entender contratos HTTP y diseño de APIs.
- Separar responsabilidades (UI, negocio, persistencia).
- Medir costo algorítmico antes de optimizar.
- Asegurar calidad con testing automatizado.
- Diseñar pensando en evolución (Spring Boot y microservicios con criterio).

## Preguntas difíciles típicas y respuesta corta
- ¿Cuándo NO usar microservicios?
Respuesta: cuando el dominio aún cambia mucho o el equipo/operación es pequeño; un monolito modular suele ser mejor inicio.

- ¿Por qué TypeScript si JavaScript ya funciona?
Respuesta: porque agrega seguridad de tipos y reduce errores en refactor, sobre todo en proyectos grandes.

- ¿Cuándo usar búsqueda binaria?
Respuesta: cuando la colección está ordenada y necesitás consultas frecuentes; sino lineal puede ser suficiente.

- ¿Mock vs integración real?
Respuesta: unitarios con mocks para feedback rápido; integración para validar wiring real y contratos.
