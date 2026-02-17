# Guía - Ejercicios de programación Java

## Definición

Una guía de ejercicios es un conjunto de prácticas para aplicar conceptos (variables, control, POO) y ganar fluidez resolviendo problemas concretos.

## Explicación

- *Qué problema resuelve*
    Convierte teoría en habilidad: obliga a practicar lectura de enunciados, modelado, implementación y validación con casos simples.

- *Cómo funciona por arriba*
    - Se resuelve por bloques (estructurada → POO)
    - Cada ejercicio practica 2-5 conceptos clave
    - Se recomienda avanzar en orden (de lo simple a lo complejo)

- *Qué implica / qué permite*
    - Identificar puntos débiles (loops, condicionales, modelado de clases)
    - Generar mini-soluciones reutilizables (helpers, validaciones, métodos)
    - Prepararse para parciales/prácticos con ejercicios tipo

## Introducción

Esta guía práctica incluye ejercicios divididos en dos secciones:
1. **Programación Estructurada**: Variables, operadores, estructuras de control
2. **Programación Orientada a Objetos**: Clases, objetos, atributos y métodos

## Programación Estructurada

### Variables y Operadores

**Ejercicio 1 - Operaciones básicas**
Declarar dos variables enteras, cargar valores por teclado e informar:
- Suma
- Diferencia  
- Producto
- Cociente

**Conceptos aplicados:**
- Variables enteras
- Operadores aritméticos
- Entrada por teclado (Scanner)

**Ejercicio 2 - Cálculo con IVA**
Ingresar precio de un artículo y calcular precio con IVA.

**Conceptos aplicados:**
- Variables decimales (double)
- Operaciones con porcentajes
- Constantes (tasa de IVA)

**Ejercicio 3 - Facturación**
Ingresar datos de una factura con tres artículos. De cada uno: precio unitario y cantidad. Imprimir total de la factura.

**Conceptos aplicados:**
- Múltiples variables
- Acumuladores
- Formato de salida

### Estructuras Condicionales

**Ejercicio 4 - Comparación**
Ingresar nombre y altura de dos personas. Informar el nombre de la más alta.

**Conceptos aplicados:**
- Condicional if-else
- Comparación de valores
- Variables String

**Ejercicio 5 - Cálculo con horas extras**
Ingresar horas trabajadas y sueldo por hora. Calcular total a cobrar considerando:
- Si trabajó más de 180 horas, las excedentes se pagan con 50% de aumento

**Conceptos aplicados:**
- Condicionales
- Cálculo con porcentajes
- Acumuladores

**Ejercicio 6 - Año bisiesto**
Ingresar un año e indicar si es bisiesto.
- Regla: múltiplo de 4 Y NO múltiplo de 100, O múltiplo de 400

**Conceptos aplicados:**
- Operadores lógicos (&&, ||)
- Operador módulo (%)
- Condicionales complejos

**Ejercicio 7 - Alquiler de autos**
Cobrar $300 por día si no se superan 200 km.
- Km extra hasta 1000: $5 adicionales por km
- Km extra a partir de 1000: $10 adicionales por km

**Conceptos aplicados:**
- Condicionales anidados
- Cálculo progresivo
- Estructura if-else if-else

### Estructuras Repetitivas

**Ejercicio 8 - Suma y promedio**
Ingresar 10 números e informar su suma y promedio.

**Conceptos aplicados:**
- Bucle for
- Acumuladores
- Cálculo de promedio

**Ejercicio 9 - Conteo condicional**
Ingresar número n y a continuación n números positivos. Informar cantidad de mayores a 5.

**Conceptos aplicados:**
- Bucle for dinámico
- Contadores condicionales
- Validación de entrada

**Ejercicio 10 - Validación**
Ingresar un número y validar que sea positivo. Si no, seguir solicitándolo.

**Conceptos aplicados:**
- Bucle do-while
- Validación de datos
- Entrada repetida

**Ejercicio 11 - Clasificación F1**
Ingresar tiempo del ganador de clasificación. Luego ingresar tiempos de otros 9 corredores.
Informar cuántos disputarán la carrera (pueden participar si su tiempo no supera en 15% al ganador).

**Conceptos aplicados:**
- Bucles
- Cálculo porcentual
- Comparaciones
- Contadores

**Ejercicio 12 - Clasificación de autos**
Ingresar antigüedad de autos de una concesionaria. Finalizar con 0.
Por cada auto mostrar:
- 1-5 años: "NUEVO"
- 6-10 años: "POCO USO"
- 11-20 años: "MUCHO USO"
- Más de 20: "MUY ANTIGUO"

**Ejercicio 13 - Estadísticas**
Después de ejercicio 12, calcular y mostrar:
- Cantidad total de autos
- Cantidad de autos con poco uso
- Promedio de antigüedad de autos que NO sean muy antiguos

**Conceptos aplicados:**
- Bucles con condición de salida
- Contadores múltiples
- Acumuladores con filtros
- Cálculo de promedios condicionales

## Programación Orientada a Objetos

### Clases y Objetos Básicos

**Ejercicio 1 - Clase Persona**
Crear clase Persona con atributos: nombre, apellido, edad.
Programa que permita:
- Ingresar datos por teclado
- Crear instancias
- Mostrar estado de los objetos

**Conceptos aplicados:**
- Definición de clase
- Atributos
- Constructor
- Creación de objetos (new)
- Métodos (toString, getters)

**Ejercicio 2 - Clase Punto**
Crear clase Punto para representar coordenadas cartesianas (x, y).
Programa que:
- Ingrese datos de dos puntos
- Cree dos instancias
- Calcule y muestre la distancia entre ambos

**Conceptos aplicados:**
- Atributos numéricos
- Métodos de cálculo
- Fórmula de distancia: √((x2-x1)² + (y2-y1)²)
- Uso de Math.sqrt() y Math.pow()

**Ejercicio 3 - Índice de Masa Corporal**
Agregar a clase Persona:
- Atributos: peso, altura
- Método: calcularIMC()
- Fórmula: IMC = peso / (altura²)

**Ejercicio 4 - Clase Auto**
Crear clase Auto con:
- Atributos: marca, modelo, precio, kilometraje
- Método: calcularAntiguedad()

**Ejercicio 5 - Clase Equipo de Fútbol**
Crear clase Equipo con:
- Atributos: nombre, puntos, partidos ganados/empatados/perdidos, goles a favor/en contra, posición
- Representa un equipo en campeonato de liga

**Ejercicio 6 - Clase Partido**
Crear clase Partido con:
- Dos atributos de tipo Equipo (equipos contendientes)
- Atributos para indicar resultado
- Relación entre clases

**Ejercicio 7 - Perímetro de triángulo**
Crear clase Triangulo con:
- Atributos: tres lados
- Método: calcularPerimetro()
- En main(): determinar si perímetro es superior a 10

## Checklist de conceptos a aplicar

### En todos los ejercicios:
- [ ] Convenciones de nombres (CamelCase)
- [ ] Indentación correcta
- [ ] Comentarios descriptivos
- [ ] Manejo de Scanner (abrir y cerrar)
- [ ] Validaciones básicas de entrada

### POO específico:
- [ ] Encapsulamiento (private, getters, setters)
- [ ] Constructores apropiados
- [ ] Métodos coherentes con la clase
- [ ] Relaciones entre clases (cuando aplique)
- [ ] Uso de toString() para mostrar objetos

## Palabras clave

- Programación estructurada
- Programación orientada a objetos
- Ejercicios prácticos
- Scanner
- Clases y objetos
- Encapsulamiento
- Constructores
- Métodos

## Comparaciones típicas

- vs [[03 - Java - Sintaxis básica]]: la sintaxis explica reglas; la guía te obliga a aplicarlas en problemas.
- vs [[07 - Java - Estructuras de control]]: la teoría describe condicionales/bucles; los ejercicios entrenan cuándo y cómo usarlos.

## Preguntas de examen

- ¿Por qué conviene resolver ejercicios en orden (de estructurada a POO)?
- ¿Qué conceptos aparecen más seguido en ejercicios introductorios?
- ¿Qué buenas prácticas se deberían repetir en todos los ejercicios (validaciones, nombres, etc.)?

## Errores comunes

- Empezar por POO sin dominar condicionales/bucles (se traba todo el flujo).
- No probar con casos borde (0, negativos, vacíos, límites).
- Escribir todo en `main` sin separar en métodos (se vuelve ilegible).

## Mini-ejemplo (mental)

Estos ejercicios son como **practicar escalas antes de tocar una canción**: los primeros (estructurados) son notas individuales y progresiones básicas; los de POO son acordes y melodías que combinan múltiples notas (atributos y métodos) armónicamente. Cada uno construye sobre el anterior hasta que puedes improvisar (resolver problemas reales).
