# Preguntas - FE U4 Angular

- ¿Qué problema resuelven las Single Page Applications (SPA)?
- ¿Qué diferencia clave hay entre una SPA y una aplicación multipágina tradicional?
- ¿Qué ventajas de UX y rendimiento ofrece una SPA?
- ¿Por qué Angular es una buena opción para construir SPA?
- ¿Qué es Angular y quién lo mantiene?
- ¿Qué significa que Angular tenga arquitectura basada en componentes?
- ¿Qué rol cumple la inyección de dependencias en Angular?
- ¿Qué ventaja práctica tiene usar servicios para separar lógica de UI?
- ¿Para qué sirve Angular CLI?
- ¿Qué hace `ng new` y qué hace `ng serve`?
- ¿Qué carpetas/archivos de un proyecto Angular son clave (`src`, `angular.json`, `package.json`)?
- ¿Qué diferencia hay entre un componente tradicional y uno standalone?
- ¿Qué ventajas traen los Standalone Components en Angular 17+?
- ¿Qué diferencia hay entre one-way binding y two-way binding?
- ¿Qué es interpolación y qué es property binding?
- ¿Qué rol cumple `ngModel` en el two-way binding?
- ¿Cómo se comunican componentes padre-hijo con `@Input` y `@Output`?
- ¿Cuándo conviene usar un servicio para comunicar componentes?
- ¿Qué elementos componen una petición HTTP?
- ¿Qué verbos HTTP son más comunes y para qué se usan?
- ¿Qué es asincronismo y por qué es importante en frontend?
- ¿Qué es un observable y por qué Angular lo usa en `HttpClient`?
- ¿Qué callbacks puede recibir `subscribe`?
- ¿Cuándo hay que desuscribirse y cuándo no?
- ¿Qué es RxJS y por qué está integrado en Angular?
- ¿Para qué sirve `.pipe()`?
- ¿Qué hace `map`, `filter`, `tap`, `takeUntil` y `switchMap`?
- ¿Cuál es la diferencia entre `Subject` y `BehaviorSubject`?
- ¿Por qué `BehaviorSubject` es útil para estado compartido?
- ¿Qué diferencia hay entre directivas estructurales y de atributo?
- ¿Qué hacen `ngIf`, `ngFor`, `ngSwitch`, `ngClass` y `ngStyle`?
- ¿Qué aportan las nuevas directivas `@if`, `@for` y `@switch`?
- ¿Qué es un pipe y qué problema resuelve en templates?
- ¿Cuándo conviene crear un pipe personalizado?
- ¿Qué es un Template Driven Form?
- ¿Qué hacen `ngForm`, `ngModel` y `ngSubmit`?
- ¿Qué validaciones comunes soporta Angular en template-driven forms?
- ¿Qué significan estados como `valid`, `invalid`, `dirty`, `touched`?
- ¿Qué hace `ngModelGroup` en formularios anidados?

## Respuestas (opcional)

### ¿Qué problema resuelven las Single Page Applications (SPA)?
Respuesta: Evitan recargar páginas completas en cada navegación y reducen esperas, logrando una experiencia más fluida y reactiva.

### ¿Qué diferencia clave hay entre una SPA y una aplicación multipágina tradicional?
Respuesta: En SPA se carga una base y luego se actualiza contenido sin recargar toda la página; en multipágina cada navegación suele pedir una página completa al servidor.

### ¿Qué ventajas de UX y rendimiento ofrece una SPA?
Respuesta: Navegación más rápida, menor latencia percibida y transiciones más suaves; además puede reutilizar recursos ya cargados.

### ¿Por qué Angular es una buena opción para construir SPA?
Respuesta: Ofrece estructura completa (routing, DI, formularios, HTTP, CLI) y buenas prácticas integradas para apps grandes y mantenibles.

### ¿Qué es Angular y quién lo mantiene?
Respuesta: Angular es un framework frontend TypeScript para aplicaciones web; lo mantiene Google junto con su comunidad.

### ¿Qué significa que Angular tenga arquitectura basada en componentes?
Respuesta: La UI se divide en piezas reutilizables con lógica, template y estilos propios, facilitando escalabilidad y mantenimiento.

### ¿Qué rol cumple la inyección de dependencias en Angular?
Respuesta: Permite proveer servicios a componentes/clases sin instanciarlos manualmente, desacoplando código y mejorando testeo.

### ¿Qué ventaja práctica tiene usar servicios para separar lógica de UI?
Respuesta: Centraliza lógica de negocio/datos fuera del componente, evita duplicación y deja componentes más simples.

### ¿Para qué sirve Angular CLI?
Respuesta: Para crear, generar, ejecutar, testear y compilar proyectos Angular con comandos estandarizados.

### ¿Qué hace `ng new` y qué hace `ng serve`?
Respuesta: `ng new` crea un proyecto Angular nuevo; `ng serve` levanta un servidor de desarrollo con recarga automática.

### ¿Qué carpetas/archivos de un proyecto Angular son clave (`src`, `angular.json`, `package.json`)?
Respuesta: `src` contiene el código fuente; `angular.json` define configuración de build/serve; `package.json` gestiona scripts y dependencias.

### ¿Qué diferencia hay entre un componente tradicional y uno standalone?
Respuesta: El tradicional depende de un `NgModule`; el standalone se declara con `standalone: true` y se importa directo.

### ¿Qué ventajas traen los Standalone Components en Angular 17+?
Respuesta: Menos boilerplate, imports explícitos por componente y arquitectura más simple para escalar y lazy-load.

### ¿Qué diferencia hay entre one-way binding y two-way binding?
Respuesta: One-way fluye en una dirección (modelo->vista o vista->evento); two-way sincroniza modelo y vista en ambos sentidos.

### ¿Qué es interpolación y qué es property binding?
Respuesta: Interpolación (`{{ }}`) muestra texto evaluado en template; property binding (`[prop]`) asigna valores a propiedades del DOM/componente.

### ¿Qué rol cumple `ngModel` en el two-way binding?
Respuesta: Con `[(ngModel)]` enlaza el valor del control con una propiedad del componente y mantiene ambos sincronizados.

### ¿Cómo se comunican componentes padre-hijo con `@Input` y `@Output`?
Respuesta: El padre envía datos al hijo con `@Input`; el hijo emite eventos al padre con `@Output` y `EventEmitter`.

### ¿Cuándo conviene usar un servicio para comunicar componentes?
Respuesta: Cuando no tienen relación directa (hermandad/lejanos) o cuando el estado debe compartirse globalmente.

### ¿Qué elementos componen una petición HTTP?
Respuesta: URL, método, headers, body (opcional), query params y, como resultado, código de estado + respuesta.

### ¿Qué verbos HTTP son más comunes y para qué se usan?
Respuesta: `GET` leer, `POST` crear, `PUT/PATCH` actualizar y `DELETE` eliminar recursos.

### ¿Qué es asincronismo y por qué es importante en frontend?
Respuesta: Es ejecutar tareas sin bloquear la UI; permite esperar red/IO manteniendo la app interactiva.

### ¿Qué es un observable y por qué Angular lo usa en `HttpClient`?
Respuesta: Es un flujo de datos en el tiempo al que te suscribís; Angular lo usa para modelar respuestas async y componerlas con RxJS.

### ¿Qué callbacks puede recibir `subscribe`?
Respuesta: Puede recibir `next`, `error` y `complete`, ya sea como funciones separadas u objeto observador.

### ¿Cuándo hay que desuscribirse y cuándo no?
Respuesta: En observables que no completan solos (eventos, `interval`, `Subject`, sockets). En `HttpClient` normal, usualmente no hace falta porque completa tras responder.

### ¿Qué es RxJS y por qué está integrado en Angular?
Respuesta: Es una librería de programación reactiva con observables; Angular la integra para manejar asincronismo y eventos complejos.

### ¿Para qué sirve `.pipe()`?
Respuesta: Para encadenar operadores de RxJS y transformar/controlar un observable antes de consumirlo.

### ¿Qué hace `map`, `filter`, `tap`, `takeUntil` y `switchMap`?
Respuesta: `map` transforma, `filter` filtra, `tap` ejecuta efectos secundarios, `takeUntil` corta suscripción y `switchMap` cambia al último observable cancelando el anterior.

### ¿Cuál es la diferencia entre `Subject` y `BehaviorSubject`?
Respuesta: `Subject` no entrega valores previos al nuevo suscriptor; `BehaviorSubject` sí entrega el último valor emitido y requiere valor inicial.

### ¿Por qué `BehaviorSubject` es útil para estado compartido?
Respuesta: Porque nuevos suscriptores reciben el estado actual inmediatamente, ideal para sincronizar componentes.

### ¿Qué diferencia hay entre directivas estructurales y de atributo?
Respuesta: Las estructurales agregan/quitan elementos del DOM; las de atributo modifican apariencia o comportamiento de elementos existentes.

### ¿Qué hacen `ngIf`, `ngFor`, `ngSwitch`, `ngClass` y `ngStyle`?
Respuesta: `ngIf` condiciona render, `ngFor` itera listas, `ngSwitch` evalúa casos, `ngClass` maneja clases y `ngStyle` estilos inline.

### ¿Qué aportan las nuevas directivas `@if`, `@for` y `@switch`?
Respuesta: Sintaxis de control de flujo más clara y cercana a lenguaje, con mejor legibilidad y optimizaciones modernas.

### ¿Qué es un pipe y qué problema resuelve en templates?
Respuesta: Es un transformador de datos en vista (fecha, moneda, texto), evitando lógica repetida en el template.

### ¿Cuándo conviene crear un pipe personalizado?
Respuesta: Cuando una transformación se repite en varias vistas o necesitás encapsular formato de dominio.

### ¿Qué es un Template Driven Form?
Respuesta: Un enfoque de formularios guiado por directivas en el template, donde Angular crea y gestiona el modelo automáticamente.

### ¿Qué hacen `ngForm`, `ngModel` y `ngSubmit`?
Respuesta: `ngForm` representa el formulario, `ngModel` vincula controles con modelo y `ngSubmit` captura el envío.

### ¿Qué validaciones comunes soporta Angular en template-driven forms?
Respuesta: `required`, `minlength`, `maxlength`, `pattern`, `email`, además de validadores personalizados.

### ¿Qué significan estados como `valid`, `invalid`, `dirty`, `touched`?
Respuesta: `valid/invalid` indican validez; `dirty` marca que cambió el valor y `touched` que el campo perdió foco.

### ¿Qué hace `ngModelGroup` en formularios anidados?
Respuesta: Agrupa controles relacionados bajo un subobjeto lógico, facilitando validación y organización de datos anidados.
