# Preguntas - FE U4 Angular

## Introducción y SPA

- ¿Qué problema resuelven las Single Page Applications (SPA)?
- ¿Qué diferencia clave hay entre una SPA y una aplicación multipágina tradicional?
- ¿Qué ventajas de UX y rendimiento ofrece una SPA?
- ¿Por qué Angular es una buena opción para construir SPA?

## Angular y arquitectura

- ¿Qué es Angular y quién lo mantiene?
- ¿Qué significa que Angular tenga arquitectura basada en componentes?
- ¿Qué rol cumple la inyección de dependencias en Angular?
- ¿Qué ventaja práctica tiene usar servicios para separar lógica de UI?

## CLI, proyecto y componentes

- ¿Para qué sirve Angular CLI?
- ¿Qué hace `ng new` y qué hace `ng serve`?
- ¿Qué carpetas/archivos de un proyecto Angular son clave (`src`, `angular.json`, `package.json`)?
- ¿Qué diferencia hay entre un componente tradicional y uno standalone?
- ¿Qué ventajas traen los Standalone Components en Angular 17+?

## Data Binding y comunicación

- ¿Qué diferencia hay entre one-way binding y two-way binding?
- ¿Qué es interpolación y qué es property binding?
- ¿Qué rol cumple `ngModel` en el two-way binding?
- ¿Cómo se comunican componentes padre-hijo con `@Input` y `@Output`?
- ¿Cuándo conviene usar un servicio para comunicar componentes?

## HTTP, asincronismo y observables

- ¿Qué elementos componen una petición HTTP?
- ¿Qué verbos HTTP son más comunes y para qué se usan?
- ¿Qué es asincronismo y por qué es importante en frontend?
- ¿Qué es un observable y por qué Angular lo usa en `HttpClient`?
- ¿Qué callbacks puede recibir `subscribe`?
- ¿Cuándo hay que desuscribirse y cuándo no?

## RxJS

- ¿Qué es RxJS y por qué está integrado en Angular?
- ¿Para qué sirve `.pipe()`?
- ¿Qué hace `map`, `filter`, `tap`, `takeUntil` y `switchMap`?
- ¿Cuál es la diferencia entre `Subject` y `BehaviorSubject`?
- ¿Por qué `BehaviorSubject` es útil para estado compartido?

## Directivas y pipes

- ¿Qué diferencia hay entre directivas estructurales y de atributo?
- ¿Qué hacen `ngIf`, `ngFor`, `ngSwitch`, `ngClass` y `ngStyle`?
- ¿Qué aportan las nuevas directivas `@if`, `@for` y `@switch`?
- ¿Qué es un pipe y qué problema resuelve en templates?
- ¿Cuándo conviene crear un pipe personalizado?

## Formularios

- ¿Qué es un Template Driven Form?
- ¿Qué hacen `ngForm`, `ngModel` y `ngSubmit`?
- ¿Qué validaciones comunes soporta Angular en template-driven forms?
- ¿Qué significan estados como `valid`, `invalid`, `dirty`, `touched`?
- ¿Qué hace `ngModelGroup` en formularios anidados?

## Respuestas (opcional)

### ¿Qué diferencia hay entre SPA y multi-page app?
Respuesta: En SPA se carga una base y luego se actualiza contenido sin recargar toda la página; en multi-page cada navegación suele pedir una página completa al servidor. Ver: [[04 - Angular - SPA (Single Page Applications)]]

### ¿Qué diferencia hay entre `Subject` y `BehaviorSubject`?
Respuesta: `Subject` no entrega valores previos al nuevo suscriptor; `BehaviorSubject` sí entrega el último valor emitido (y exige valor inicial). Ver: [[19 - RxJS - Subject y BehaviorSubject]]

### ¿Cuándo debo desuscribirme?
Respuesta: En observables que no completan solos (eventos, `interval`, `Subject`, sockets). En `HttpClient` normal, usualmente no hace falta porque completa tras responder. Ver: [[11 - Angular - Observables y RxJS]]
