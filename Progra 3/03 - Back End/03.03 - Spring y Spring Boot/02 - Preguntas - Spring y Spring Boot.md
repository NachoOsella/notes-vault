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
