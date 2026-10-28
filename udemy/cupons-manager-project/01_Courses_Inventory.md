# Descripciones de cursos — Portal de instructor Udemy

Descripciones amplias de 13 cursos, elaboradas a partir del temario publicado de cada uno (secciones y clases). Se excluyó *Aprende las Corrutinas y Flows de Kotlin a profundidad 2023*.

**Índice**

1. [Domina las Estructuras de Datos & Java API Collections 2026](#1-domina-las-estructuras-de-datos--java-api-collections-2026)
2. [Claude Code: Spec-Driven Development | Edición Frontend](#2-claude-code-spec-driven-development--edición-frontend)
3. [Claude Code: Spec-Driven Development | Edición Backend](#3-claude-code-spec-driven-development--edición-backend)
4. [Spring Boot 4: DDD, CQRS, Hexagonal e AI Agents (Java 25)](#4-spring-boot-4-ddd-cqrs-hexagonal-e-ai-agents-java-25)
5. [Concurrencia Moderna en Java: Threads y Virtual Threads 2026](#5-concurrencia-moderna-en-java-threads-y-virtual-threads-2026)
6. [Master en Spring WebFlux y Programación Reactiva](#6-master-en-spring-webflux-y-programación-reactiva)
7. [El Arte de Spring Boot: Guía Definitiva Desde las Bases 2026](#7-el-arte-de-spring-boot-guía-definitiva-desde-las-bases-2026)
8. [Spring Data JPA y Hibernate: Persistencia de Datos con Java](#8-spring-data-jpa-y-hibernate-persistencia-de-datos-con-java)
9. [Diseño de Microservicios con Spring Boot y Spring Cloud](#9-diseño-de-microservicios-con-spring-boot-y-spring-cloud)
10. [Masterclass: OAuth 2.1 y JWT con Spring Security 7](#10-masterclass-oauth-21-y-jwt-con-spring-security-7)
11. [Tests Unitarios con Mockito y Spring Boot: Guía Definitiva](#11-tests-unitarios-con-mockito-y-spring-boot-guía-definitiva)
12. [Backend Profesional con Spring Boot 3 y Spring Framework 6](#12-backend-profesional-con-spring-boot-3-y-spring-framework-6)
13. [Domina la Programación Funcional en Java 2026](#13-domina-la-programación-funcional-en-java-2026)

---

## 1. Domina las Estructuras de Datos & Java API Collections 2026

*Entiende Collections API por dentro y aplícalo en proyectos reales y problemas de LeetCode.*

Este curso explica cómo funcionan por dentro las estructuras de datos de Java y cuándo conviene usar cada una. No se queda en memorizar métodos: parte de las limitaciones de los arreglos primitivos, repasa la programación genérica (la base de todas las colecciones) e introduce la notación de complejidad algorítmica (constante, lineal, cuadrática, exponencial y logarítmica) para que cada decisión de diseño se pueda justificar con números. Todo se practica sobre un proyecto base y con problemas clásicos de LeetCode.

**Temas principales**

- **Fundamentos:** limitaciones de los arreglos de tamaño fijo, genéricos `<T>` y medición de complejidad (Big O).
- **List (ArrayList y LinkedList):** el patrón Iterator y el contrato `Iterable`/`Iterator` que hace posible el for-each; CRUD en ambas implementaciones; ordenamiento con `Comparator` (comparadores compuestos, orden inverso y el algoritmo que usa Java internamente); búsqueda binaria; y una comparación práctica de rendimiento entre ArrayList y LinkedList según el tipo de operación.
- **El mecanismo hash (HashSet y HashMap):** por qué las búsquedas son casi instantáneas; operaciones de conjuntos (unión, intersección, diferencia); `merge()` para acumular valores por llave; diferencia de eficiencia entre `containsKey()` y `containsValue()`; y `LinkedHashSet`/`LinkedHashMap` para conservar el orden de inserción.
- **Pilas y colas:** LIFO vs FIFO, `Stack`, `Queue`, `Deque` y `PriorityQueue` con prioridad definida por `Comparator`, con casos reales como "deshacer".
- **Estructuras especializadas:** `TreeSet` y `TreeMap` con operaciones de navegación y rango (`first`, `last`, `floor`, `ceiling`, `headMap`, `tailMap`, `subMap`).
- **Colecciones concurrentes:** qué es una estructura thread-safe, condiciones de carrera y cómo resolverlas con `synchronized` y `ReentrantLock`, `CopyOnWriteArrayList` y operaciones atómicas en `ConcurrentHashMap` (`computeIfAbsent`).
- **Matrices:** arreglos de arreglos, recorrido por filas y columnas, transposición, recorrer una matriz cuadrada con un solo ciclo y suma de diagonales.

**Problemas de LeetCode resueltos:** Binary Search, Contains Duplicate, Valid Anagram, Two Sum, Valid Parentheses y suma de diagonales de una matriz.

**Lo más importante:** el alumno termina entendiendo el *porqué* del rendimiento de cada colección, con una base sólida para entrevistas técnicas y para escribir código más eficiente en proyectos reales, incluido el uso seguro de colecciones en entornos multihilo.

---

## 2. Claude Code: Spec-Driven Development | Edición Frontend

*Aprende Spec-Driven Development para React, Angular y Vue con Claude Code, MCP y Cypress.*

Un curso práctico para que desarrolladores frontend integren la IA en su flujo diario de trabajo de forma profesional. Combina los fundamentos teóricos de los modelos de lenguaje con una metodología concreta, Spec-Driven Development, en la que las especificaciones guían el trabajo de los agentes de Claude Code. Se construye un proyecto real (TicketFlow) que consume un backend existente, desde el diseño de UI/UX y la arquitectura hasta las pruebas End-to-End automatizadas.

**Temas principales**

- **Fundamentos de IA para ingenieros:** tokens, embeddings, transformers y el flujo completo de un LLM.
- **Prompt engineering y configuración de modelos:** Max Tokens, temperatura, Top-K y Top-P; técnicas de prompting como Zero-Shot, Chain-of-Thought, Role/Persona y salidas estructuradas o deterministas.
- **El ecosistema de Claude:** Markdown, los diferentes modelos de Claude, instalación de Claude Code y el marco AI Fluency de Anthropic (las 4 D), con bonus para obtener el certificado gratuito.
- **Preparación del proyecto:** cómo dar contexto efectivo a Claude, importar contratos de API desde Postman, entender el backend, y diseñar el flujo UI/UX y la arquitectura de la aplicación con ayuda de la IA.
- **Entorno profesional con Claude Code:** `CLAUDE.md`, subagentes especializados, comandos personalizados, `settings.json` y una estrategia de ramas de Git pensada para trabajar con agentes.
- **Desarrollo guiado por especificaciones:** integración con Jira y GitHub, pruebas unitarias, consumo de APIs con HTTP Client, login seguro, navegación con parámetros dinámicos, formularios, layout, paginación y corrección de bugs; con énfasis en que el code review lo haga un humano para evitar alucinaciones.
- **Pruebas E2E con Cypress:** creación de IDs para automatización, estructura del proyecto de pruebas, carga de contexto para generar pruebas más precisas y ejecución del flujo completo en un solo prompt.
- **Multi-Agent:** varios agentes trabajando en paralelo en el mismo proyecto usando Git Worktrees, con merge y limpieza.
- **MCP (Model Context Protocol):** integraciones con GitHub, Figma (diseño de UI), Notion y, de forma opcional, PostgreSQL; además de un caso real sobre los riesgos de seguridad de los agentes ("el día que un agente escapó del sandbox").

**Lo más importante:** no es un curso de "pedirle código a la IA", sino de cómo estructurar un flujo de trabajo repetible y controlado con agentes, aplicable a React, Angular o Vue, que incluye pruebas automatizadas y buenas prácticas de revisión.

---

## 3. Claude Code: Spec-Driven Development | Edición Backend

*Aprende Spec-Driven Development para Backend con Multi-Agent, MCP y desarrollo empresarial asistido por IA.*

La contraparte backend del curso de Spec-Driven Development. Enseña a usar Claude Code como herramienta de desarrollo empresarial: desde diseñar la base de datos, la arquitectura y las APIs RESTful de un sistema, hasta implementar features completas, generar pruebas unitarias y de integración, y coordinar varios agentes trabajando en paralelo.

**Temas principales**

- **Fundamentos de IA y LLMs:** tokens, embeddings, transformers y el flujo end-to-end de un modelo de lenguaje.
- **Prompt engineering:** parámetros del modelo (Max Tokens, temperatura, Top-K, Top-P) y técnicas como Zero-Shot, Chain-of-Thought, Role Prompting y Structured Output.
- **El mundo de Claude:** Markdown, modelos y planes de Claude, instalación de Claude Code, el marco AI Fluency y los nuevos paradigmas del desarrollo con IA.
- **Diseño del proyecto con IA:** definición de alcance y funcionalidades, diseño de la infraestructura de base de datos, diagramas de arquitectura, validación de la base de datos generada, diseño de APIs RESTful y de la capa de persistencia.
- **Ecosistema Spec-Driven:** configuración avanzada de Claude Code, `CLAUDE.md`, agentes especializados, estrategia de ramas Git para desarrollo con IA y comandos integrados con Jira.
- **Desarrollo por tareas:** features end-to-end, pruebas unitarias asistidas por IA, planificación y división estratégica de tareas, implementación de una tarea de nivel empresarial e integración de un chat contextual con agentes.
- **Pruebas de integración "one shot":** tipos de pruebas, especificaciones de pruebas de integración para múltiples features, agentes dedicados a pruebas y su ejecución y validación.
- **Multi-Agent:** orquestación de varios agentes con y sin Git Worktree, y estrategias de merge para consolidar cambios.
- **MCP y herramientas externas:** integración con Notion (implementar una tarea directamente desde Notion), PostgreSQL, Figma y GitHub, más un caso real sobre seguridad y sandboxing de agentes.

**Lo más importante:** el curso muestra un flujo completo y reproducible para llevar un backend de la especificación a código probado, con la IA como acelerador y el desarrollador como responsable del diseño y la revisión.

---

## 4. Spring Boot 4: DDD, CQRS, Hexagonal e AI Agents (Java 25)

*Crea un backend para tu portafolio con los módulos más demandados de Spring, arquitectura moderna, potenciado por AI.*

El curso más completo y actual del catálogo en cuanto a arquitectura backend. Se construye un sistema real con Spring Framework 7, Spring Boot 4 y Java 25, organizado como proyecto multi-módulo y aplicando Domain-Driven Design, CQRS y arquitectura hexagonal (puertos y adaptadores). A lo largo del proyecto se integran los módulos de Spring más demandados en el mercado y se usa la IA como herramienta de productividad (generación de mapeos, pruebas y agentes de código).

**Temas principales**

- **Stack moderno:** novedades de Spring Framework 7 y Spring Boot 4, fundamentos de LLMs en el backend y configuración de VS Code con plugins de IA.
- **Arquitectura y modularización:** diseño de un backend escalable, proyecto multi-módulo con separación por contextos y generación de módulos automatizada con IA.
- **Persistencia políglota:** infraestructura con Docker, Spring Data JPA con PostgreSQL y Spring Data MongoDB; mapeo de entidades (asistido por IA y por ingeniería inversa) y repositorios de Spring Data.
- **Domain-Driven Design:** entidades de dominio, eventos de dominio, aggregates y aggregate root, value objects, repositorios de solo lectura y pruebas unitarias del dominio (manuales, asistidas por IA y con un agente de código).
- **Integraciones externas con puertos y adaptadores:** almacenamiento de archivos en AWS S3 (con LocalStack y AWS CLI), consumo de APIs con REST Client y MapStruct, y envío de correos con Spring Mail y plantillas HTML.
- **CQRS:** modelo de escritura con comandos y casos de uso (crear, actualizar, cancelar órdenes) sobre PostgreSQL, y modelo de lectura optimizado sobre MongoDB con caché en Redis.
- **APIs profesionales:** diseño de contratos, versionado de API, endpoints GET/POST/PUT/PATCH, carga de imágenes a S3, `@ControllerAdvice`, pruebas con Postman y documentación con OpenAPI/Swagger.
- **Spring Batch:** jobs, steps, readers, processors y writers, programación con cron y precarga de caché.
- **Mensajería:** eventos con RabbitMQ y Spring AMQP para cerrar el flujo completo de CQRS.
- **Seguridad:** OAuth 2.1 y JWT con Spring Security (codificación y validación de tokens, hashing de contraseñas, resource server y auth controller).
- **Spring AI:** integración con modelos locales (Ollama) y en la nube (Gemini), potenciada con Spring AOP.
- **Agentes de IA con Claude Code:** casos de uso reales como mejora de logs, organización de dependencias, generación de pruebas unitarias y optimización de contenedores Docker.

**Lo más importante:** el alumno termina con un proyecto de portafolio que demuestra dominio de arquitecturas modernas (DDD + CQRS + Hexagonal) y de un amplio abanico de tecnologías del ecosistema Spring, con la IA integrada tanto en el producto (Spring AI) como en el proceso de desarrollo.

---

## 5. Concurrencia Moderna en Java: Threads y Virtual Threads 2026

*Domina desde los threads clásicos hasta los virtual threads, sincronización avanzada y concurrencia estructurada.*

Un recorrido completo por la programación concurrente en Java, desde los conceptos clásicos hasta las características más recientes del lenguaje. Se aprende mediante un sistema práctico de cupones que permite ver, reproducir y corregir problemas reales de concurrencia, y se cierra integrando virtual threads en una aplicación Spring Boot.

**Temas principales**

- **Fundamentos de threads:** el problema de la concurrencia, implementación de `Runnable` con enfoque imperativo y funcional, condiciones de carrera, `synchronized`, objetos thread-safe, coordinación con `wait`/`notify` y variables `volatile`.
- **Pools de threads con ExecutorService:** `FixedThreadPool`, `CachedThreadPool`, `ScheduledThreadPool` y `SingleThreadExecutor`, con sus casos de uso.
- **Virtual Threads:** diferencias con los platform threads, `Thread.ofVirtual()`/builder, `newVirtualThreadPerTaskExecutor` y el problema de *pinning* con sus soluciones.
- **Sincronización avanzada:** `CountDownLatch`, `CyclicBarrier`, `Semaphore` y `ReentrantLock` en profundidad.
- **CompletableFuture:** programación asíncrona aplicada al patrón Aggregator para combinar resultados de varias fuentes.
- **Concurrencia estructurada:** `ScopedValue` y `StructuredTaskScope`, las nuevas APIs de Java para manejar tareas concurrentes de forma segura y legible.
- **Spring Boot con Virtual Threads:** configuración y pruebas de una aplicación web que aprovecha los hilos virtuales.

**Lo más importante:** el curso conecta la teoría con problemas reproducibles (race conditions, pinning) y cubre tanto las herramientas clásicas que se siguen preguntando en entrevistas como las novedades de Java moderno que cambian la forma de escribir aplicaciones de alta concurrencia.

---

## 6. Master en Spring WebFlux y Programación Reactiva

*Domina Spring WebFlux y Project Reactor con el curso más completo de programación reactiva en español 100% actualizado.*

Un curso extenso que lleva al alumno desde los fundamentos de la programación reactiva hasta un ecosistema completo de microservicios reactivos. Empieza implementando el patrón Observer a mano para entender el modelo publicador-suscriptor, continúa con Project Reactor en profundidad y después construye con Spring WebFlux un sistema de reservaciones de restaurantes con bases de datos, caché, seguridad y mensajería, todo de forma no bloqueante.

**Temas principales**

- **Patrón Observer:** implementación de publishers, subscribers y suscripciones para entender la base de la reactividad.
- **Project Reactor:** `Mono` y `Flux`; pipelines con `map`, `filter` y `reduce`; `flatMap`, `concat`, `merge`, `zip` y `handle`; manejo de errores (`onErrorResume`, `onErrorReturn`), `retry` y `repeat`, callbacks, `Context`, y publishers *hot* y *cold*.
- **Reactor avanzado:** Sinks (One y Many) aplicados a un sistema de notificaciones, processors, y pruebas reactivas con `StepVerifier`, `defer`, `retry` y *virtual time*.
- **Spring WebFlux y ReactiveMongo:** cuándo usar WebFlux, MongoDB en Docker, configuración por properties y por Bean, repositorios reactivos, catálogo de restaurantes y CRUD completo de reservaciones.
- **Validación reactiva:** validaciones de negocio (disponibilidad de horarios) con el patrón Chain, y Javax Validation con un validador reactivo.
- **MapStruct reactivo** para mapear entidades y DTOs.
- **Router Functions y Handlers** como alternativa funcional a los controladores, con manejo global de errores.
- **Caché reactivo con Redis y paginación con Flux.**
- **WebClient y controladores reactivos** para consumir y exponer servicios REST (GET, POST, PUT, DELETE).
- **R2DBC con PostgreSQL** para acceso relacional reactivo.
- **Seguridad reactiva con JWT:** `WebFilterChain`, conversores de autenticación, `UserDetailsService`, registro de usuarios y endpoints para usuarios premium.
- **Spring Cloud Stream con Kafka:** Supplier, Function y Consumer reactivos, binders y bindings, y un flujo completo de calificaciones y reseñas basado en eventos.
- **Swagger en WebFlux** para controladores y router functions.
- **Cuestionarios** de evaluación sobre Project Reactor y Spring WebFlux.

**Lo más importante:** es una formación integral en programación reactiva: el alumno no solo aprende la API, sino a diseñar aplicaciones completas no bloqueantes con persistencia (Mongo y PostgreSQL), caché, seguridad y mensajería.

---

## 7. El Arte de Spring Boot: Guía Definitiva Desde las Bases 2026

*Descubre cómo funciona realmente Spring Boot y qué hay detrás de sus anotaciones, arquitectura y diseño.*

Un curso pensado para entender Spring "desde dentro" en lugar de usarlo como caja negra. Parte de los fundamentos de la programación orientada a objetos y de los patrones de diseño que Spring utiliza internamente, explica la inyección de dependencias y la inversión de control implementándolas a mano, y después recorre Spring Core, Spring Boot y el ciclo de vida de los beans, para terminar con un proyecto completo con los módulos más usados.

**Temas principales**

- **Repaso de POO:** herencia, polimorfismo, encapsulación y abstracción, con Lombok.
- **Patrones de diseño que usa Spring:** Singleton, Prototype (con `Cloneable` y `AutoCloseable`) y Factory Method.
- **DI e IoC:** inyección por setter, constructor y propiedad; problemas con polimorfismo y su solución; creación y destrucción de un contexto propio; y por qué usar Spring.
- **Spring Core y Context:** carga de beans vía XML, estereotipos, `BeanFactory` vs `ApplicationContext`, `@Autowired`, `@Qualifier`, clases de configuración, componentes y un ejemplo práctico de carga de Tomcat.
- **Spring Boot y sus anotaciones:** estructura del proyecto, starters, `application.properties`, `@Value`, `@PropertySource(s)`, configuración basada en propiedades, profiles y anotaciones condicionales (`@ConditionalOnProperty`, `@ConditionalOnBean`, `@ConditionalOnClass`).
- **Ciclo de vida de un bean:** `@PostConstruct`, `@PreDestroy`, inicialización lazy (local y global) y las interfaces *Aware* (ApplicationContext, Environment, BeanName, BeanFactory, ApplicationEventPublisher, ResourceLoader).
- **Proyecto integrador:** Spring Web, Spring Data JPA (mapeo de entidades y relaciones `@OneToMany`/`@OneToOne`, query methods, DTOs), CRUD completo y API REST, manejo de errores con `@ControllerAdvice` y excepciones personalizadas, manejo de archivos, Spring Security (`PasswordEncoder`, `UserDetailsService`, `SecurityFilterChain`) y pruebas con Spring Boot Test (`@MockBean`, happy y unhappy path).
- **Cierre y contenido avanzado:** buenas prácticas de logging con SLF4J, simulación y resolución de una entrevista técnica, por qué un bean singleton sin estado es thread-safe, aplicaciones con contextos padre e hijo y diferencias técnicas entre estereotipos.

**Lo más importante:** el alumno deja de "memorizar anotaciones" y entiende la mecánica detrás de Spring, lo que le permite depurar mejor, diseñar con criterio y responder con seguridad preguntas de entrevista sobre el framework.

---

## 8. Spring Data JPA y Hibernate: Persistencia de Datos con Java

*Implementa JPA y Hibernate, el ORM más usado en Java, con Spring Data y bases de datos relacionales.*

Un curso centrado por completo en la capa de persistencia. Comienza comparando JDBC con JPA para mostrar qué resuelve un ORM, construye una base de datos real en PostgreSQL con Docker y profundiza en el mapeo de entidades, las consultas, las transacciones y el ciclo de vida de las entidades, con un enfoque final en el diseño de entidades para microservicios.

**Temas principales**

- **Fundamentos:** JDBC vs JPA/Hibernate, lectura y escritura de entidades y pool de conexiones con HikariCP.
- **Base de datos del proyecto:** PostgreSQL en Docker (Windows y Linux), diagrama entidad-relación y script de creación.
- **Mapeo de entidades:** relaciones `@OneToOne` (incluida la circular), `@ManyToOne`/`@OneToMany` y `@ManyToMany`; `FetchType.LAZY`; operaciones en cascada (persist, merge, delete); `orphanRemoval`; UUIDs; enums; llaves primarias compuestas; y errores comunes como `StackOverflowError` e `InvalidDataAccessApiUsageException`.
- **Repositorios JPA:** búsqueda por ID y por nombre, operadores `LIKE`, `BETWEEN`, `AND` y `OR`, índices, joins en JPQL, manejo de fechas, `GROUP BY`, paginación y ordenamiento (incluida paginación personalizada) y llamadas a procedimientos almacenados.
- **CRUD con DTOs:** ModelMapper vs ObjectMapper, mapeos personalizados, cálculo de totales de factura y operaciones en batch.
- **Transacciones:** `@Transactional` a fondo, manejo de excepciones, niveles de propagación (`REQUIRED`, `NESTED`, `REQUIRES_NEW`, `NOT_SUPPORTED`) e aislamiento.
- **Ciclo de vida de la entidad:** callbacks `@PrePersist`, `@PostPersist`, `@PreUpdate`, `@PostUpdate`, `@PreRemove` y `@PostRemove`.
- **Caso práctico** integrador.
- **Bonus MapStruct:** mapeos simples y personalizados.
- **JPA Specification y Criteria API** para búsquedas dinámicas.
- **Diseño de entidades para microservicios:** mapeo de llaves foráneas por propiedad, joins manuales, separación por dominios y entidad raíz de agregado.

**Lo más importante:** el curso cubre desde lo básico hasta los temas que más problemas causan en producción (relaciones, lazy loading, cascadas, transacciones y propagación), y prepara al alumno para diseñar la persistencia pensando en arquitecturas de microservicios.

---

## 9. Diseño de Microservicios con Spring Boot y Spring Cloud

*Aprende a integrar Spring Boot y Spring Cloud en microservicios con Docker y DDD.*

Un curso práctico que construye paso a paso un ecosistema de microservicios con los componentes de Spring Cloud. Cada sección añade una pieza de la arquitectura (descubrimiento de servicios, configuración centralizada, gateway, tolerancia a fallos, mensajería, trazabilidad y seguridad) hasta tener todo el sistema dockerizado, y cierra con una introducción a Domain-Driven Design.

**Temas principales**

- **Introducción:** qué es Spring Cloud, fundamentos de microservicios y de Docker.
- **Primer microservicio:** CRUD de empresas con Spring Data JPA, PostgreSQL en Docker, Postman y Swagger.
- **Service Registry y Discovery con Eureka**, incluido el balanceo de carga.
- **Configuración centralizada con Spring Cloud Config Server**, usando repositorios de GitHub públicos y privados (token de acceso y llaves SSH) y profiles.
- **Comunicación entre servicios con OpenFeign** (GET, POST, DELETE) con balanceo de carga.
- **Spring Cloud Gateway** con rutas estáticas y dinámicas.
- **Circuit Breaker:** microservicio de fallback, integración con WebClient y circuit breaker en el gateway; además de un circuit breaker orientado a eventos para operaciones de escritura con Kafka.
- **Spring Cloud Stream con Kafka y MongoDB:** productores, listeners y guardado de reportes.
- **Trazabilidad distribuida:** observabilidad, métricas y trazas con Zipkin, incluidos spans personalizados.
- **Seguridad con OAuth2 y JWT:** authorization server, base de datos de usuarios, emisión y validación de tokens, secretos en el config server y el gateway como resource server.
- **Dockerización** de todos los microservicios (discovery, config, CRUD, fallback, report, listener, auth y gateway).
- **Domain-Driven Design:** dominio de una agencia de viajes (vuelos, hoteles, pagos y tours) con servicios de dominio.

**Lo más importante:** el alumno ve cómo encajan todas las piezas de una arquitectura de microservicios real y termina con un sistema completo, seguro, observable, tolerante a fallos y desplegable con Docker.

---

## 10. Masterclass: OAuth 2.1 y JWT con Spring Security 7

*Integra Spring Security 7 con filtros, roles, authorities, OIDC, JWT y OAuth 2.1.*

Una masterclass enfocada en la seguridad moderna de aplicaciones con la versión más reciente de Spring Security. Comienza con la teoría necesaria para entender por qué OAuth 2.1 es como es, implementa un Authorization Server y un Resource Server desde cero, incorpora mejoras mediante Spec-Driven Development con IA y termina con pruebas de seguridad automatizadas.

**Temas principales**

- **Arquitectura de OAuth 2.1:** evolución de la autenticación HTTP, diferencias entre hashing, encriptación y codificación, HMAC vs SHA-256, estructura de un JSON Web Token, PKCE y la arquitectura completa de OAuth 2.1 (incluida la eliminación de flujos obsoletos).
- **Authorization Server:** contraseñas con bcrypt y Argon2, `UserDetailsService`, `SecurityFilterChain`, CORS, firma con RSA y JWK, roles, scopes, refresh tokens, login personalizado y clientes privados.
- **Resource Server:** sesiones stateless, validación de JWT con JWK, dos formas de proteger rutas, roles vs scopes, lectura de claims del payload, controlador de depuración de sesión y excepciones personalizadas.
- **Spec-Driven Development con IA:** implementación de un sistema de reintentos y de autenticación básica para endpoints de usuarios guiados por especificaciones.
- **Pruebas con Spring Security Test:** jerarquía de roles, scopes, mock de JWT y pruebas de la configuración de seguridad.

**Lo más importante:** el curso combina fundamentos criptográficos y de protocolo con una implementación completa y actual, lo que permite al alumno no solo configurar Spring Security, sino entender y justificar cada decisión de seguridad.

---

## 11. Tests Unitarios con Mockito y Spring Boot: Guía Definitiva

*Testing unitario con Mockito, JUnit 5 y Spring Boot Test.*

Una guía práctica para escribir pruebas unitarias de calidad en proyectos Java y Spring Boot. Empieza dominando Mockito de forma aislada y después aplica lo aprendido a cada capa de una aplicación Spring: servicios, repositorios y controladores, buscando siempre aumentar la cobertura con pruebas significativas.

**Temas principales**

- **Mockito a fondo:** primer test y primer mock, valores por defecto, anotaciones, tests con varios mocks, argument matchers, `doReturn`, verificación de comportamiento, mock y verificación de métodos `void`, prueba de excepciones, `Spy` vs `Mock`, múltiples retornos, `ArgumentCaptor`, mock de métodos `final` y `static`, cobertura y estilo BDD.
- **Spring Boot Test (servicios):** configuración, pruebas de servicios con Mockito y con `@MockBean`, y reinicio de mocks.
- **Data JPA Test (repositorios):** cómo probar repositorios y qué vale la pena probar en un JPA repository.
- **MockMvc (controladores):** respuestas 200, validación de JSON (incluidos objetos anidados), envío de body, errores 400 y aumento de cobertura.

**Lo más importante:** el alumno aprende a probar cada capa de una aplicación Spring Boot con las herramientas adecuadas y a distinguir qué conviene probar y cómo, una habilidad clave para trabajar en equipos profesionales.

---

## 12. Backend Profesional con Spring Boot 3 y Spring Framework 6

*Crea proyectos empresariales con Spring Boot 3 y Spring Framework 6, dominando sus módulos y herramientas clave.*

Un curso amplio que recorre los módulos más utilizados del ecosistema Spring a través de un proyecto empresarial: una plataforma de agencia de viajes con vuelos, hoteles, tickets, reservaciones y tours. Cada sección incorpora un módulo nuevo, de modo que al final el alumno ha trabajado con prácticamente todas las herramientas habituales de un backend profesional.

**Temas principales**

- **Introducción:** ecosistema Spring, Docker (Linux, Windows y Mac), IntelliJ IDEA, Spring Initializr, inyección de dependencias e inversión de control.
- **Spring Data JPA:** PostgreSQL en Docker, mapeo de entidades y relaciones (incluidas relaciones inversas), repositorios, JPQL, joins, query methods y ciclo de vida de la entidad.
- **Spring Web:** DTOs, servicios CRUD, endpoints POST/GET/PUT/PATCH/DELETE, scripts de Postman, formato de fechas con Jackson, catálogos con paginación y filtros, y transaccionalidad.
- **Manejo de errores:** excepciones personalizadas, `@ControllerAdvice`, DTOs de error, validación de requests y manejo de errores 403.
- **Documentación con SpringDoc/OpenAPI (Swagger).**
- **WebClient** para consumir una API externa de tipos de cambio.
- **Spring Mail** con plantillas HTML.
- **Generación de reportes Excel con Apache POI.**
- **Spring Cache con Redis**, incluida la limpieza programada de caché.
- **Spring Data MongoDB** para usuarios y roles.
- **Seguridad con OAuth2 y JWT:** cifrado de contraseñas, filtros, proveedor de autenticación, registro de clientes, llaves RSA, JWK, payload personalizado, roles y autoridades.
- **Spring AOP** con anotaciones y aspectos personalizados.
- **Spring AMQP con RabbitMQ** para publicar y consumir mensajes.
- **Preguntas tipo examen** para desarrolladores Java Spring.

**Lo más importante:** es un curso de amplitud que da una visión completa y práctica de lo que se usa en un backend empresarial con Spring Boot 3, ideal para quien quiere pasar de conocimientos básicos a construir aplicaciones completas.

---

## 13. Domina la Programación Funcional en Java 2026

*Expresiones lambda, interfaces funcionales, Streams, Collectors, referencias a métodos y algoritmos.*

Un curso dedicado a dominar el estilo funcional en Java moderno. Construye la base paso a paso (interfaces, genéricos, clases anónimas), avanza hacia lambdas, referencias a métodos e interfaces funcionales del JDK, y profundiza en la API Stream y los Collectors, para terminar aplicando todo en patrones de diseño y en la resolución de algoritmos.

**Temas principales**

- **Fundamentos:** repaso opcional de POO, funcionamiento de las interfaces, `Comparator`, programación genérica e interfaces funcionales frente a clases anónimas.
- **Expresiones lambda:** con uno, varios o ningún parámetro, alcance (*scope*) y bloques de código.
- **Referencias a métodos:** de instancia, estáticos, constructores y métodos de objetos arbitrarios.
- **Interfaces funcionales del JDK:** `Consumer`/`BiConsumer`, `Supplier`, `Predicate`/`BiPredicate`, `Function`/`BiFunction`, `UnaryOperator`/`BinaryOperator`, `Comparator`, `Runnable` y `Callable`.
- **Patrones de diseño con lambdas:** Strategy, validadores (incluido uno basado en excepciones) y una alternativa funcional al `switch`.
- **API Stream a profundidad:** operaciones intermedias y terminales, `filter`, `map` vs `flatMap` (también en `Optional`), paginación, eliminación de duplicados, ordenamiento, `max`/`min`/`count`, `reduce`, operaciones *match*, `toList`/`toSet`/`toArray`, estadísticas, `takeWhile`/`dropWhile`, `findAny` y streams paralelos.
- **Collectors a profundidad:** `groupingBy`, `partitioningBy`, `mapping`, `summarizing`, `toMap`, `joining`, `collectingAndThen` y collectors anidados.
- **Algoritmos con lambdas:** problema Top-K URLs y un problema de LeetCode, más un examen práctico final.

**Lo más importante:** el alumno pasa de conocer la sintaxis de las lambdas a pensar de forma funcional, escribiendo código más expresivo y conciso, y aplicando Streams y Collectors a problemas reales y de entrevista.