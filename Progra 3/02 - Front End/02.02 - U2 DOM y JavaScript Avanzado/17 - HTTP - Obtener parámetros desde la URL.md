# HTTP - Obtener parámetros desde la URL

## Definición

Los parámetros de URL (query string o query params) son datos que se envían en la URL después del signo `?`. Permiten transmitir información entre páginas o a un servidor mediante la URL, siendo el método más antiguo y universal de pasar datos en la web.

## Explicación

- *Qué problema resuelve*
    Permite compartir estado entre páginas sin necesidad de almacenamiento persistente, filtrar y ordenar resultados en búsquedas, paginar contenido, y personalizar la experiencia del usuario basándose en parámetros configurables directamente en la URL (bookmarkable state).

- *Cómo funciona por arriba*
    - La URL tiene la estructura: `protocolo://dominio/ruta?param1=valor1&param2=valor2`
    - Todo lo que viene después de `?` es la query string
    - Los parámetros son pares `clave=valor` separados por `&`
    - Los valores deben estar codificados en URL (encodeURIComponent) si contienen caracteres especiales
    - JavaScript proporciona la API `URLSearchParams` para leer y manipular estos parámetros fácilmente
    - Los parámetros son visibles para el usuario y tienen límite de longitud (~2000 caracteres)

- *Qué implica / qué permite*
    - Compartir enlaces con estado específico (ej: buscar "laptops" filtrado por precio)
    - Implementar filtros, ordenamientos y paginación en listados
    - Guardar preferencias temporales en la URL
    - Rastrear campañas de marketing (UTM params)
    - Permitir que el usuario use el botón "atrás" manteniendo el estado

## Estructura de una URL con parámetros

```
https://tienda.com/productos?categoria=laptops&precio_max=50000&ordenar=precio_asc
│           │              │         │              │              │
│           │              │         │              │              └─ Parámetro 3
│           │              │         │              └─ Parámetro 2
│           │              │         └─ Parámetro 1
│           │              └─ Separador de query string
│           └─ Dominio
└─ Protocolo
```

## Uso de URLSearchParams en JavaScript

```javascript
// URL de ejemplo: https://ejemplo.com/buscar?q=javascript&categoria=frontend

// 1. Obtener todos los parámetros
const params = new URLSearchParams(window.location.search);

// 2. Leer un parámetro específico
const busqueda = params.get('q'); // 'javascript'
const categoria = params.get('categoria'); // 'frontend'

// 3. Verificar si existe un parámetro
if (params.has('filtro')) {
  console.log('Hay filtro aplicado');
}

// 4. Obtener todos los valores de un parámetro (si hay duplicados)
const tags = params.getAll('tag'); // ['js', 'web'] para ?tag=js&tag=web

// 5. Iterar sobre todos los parámetros
for (const [clave, valor] of params) {
  console.log(`${clave}: ${valor}`);
}
```

## Modificar parámetros dinámicamente

```javascript
const params = new URLSearchParams(window.location.search);

// Agregar o modificar un parámetro
params.set('pagina', '2');
params.set('orden', 'descendente');

// Agregar múltiples valores
params.append('filtro', 'nuevo');

// Eliminar un parámetro
params.delete('categoria');

// Actualizar la URL sin recargar la página
const nuevaUrl = `${window.location.pathname}?${params.toString()}`;
window.history.pushState({}, '', nuevaUrl);
```

## Casos de uso comunes

| Caso | Ejemplo de URL | Descripción |
|------|----------------|-------------|
| **Búsqueda** | `?q=javascript` | Término de búsqueda |
| **Filtros** | `?categoria=laptops&marca=apple` | Filtrar resultados |
| **Paginación** | `?page=2&limit=20` | Navegar por páginas |
| **Ordenamiento** | `?sort=precio&order=asc` | Ordenar resultados |
| **Tracking** | `?utm_source=google&utm_campaign=verano` | Marketing/analytics |
| **Estado de UI** | `?modal=abierto&tab=perfil` | Estado de interfaz |

## Codificación de parámetros

```javascript
// Codificar valores especiales
const busqueda = 'javascript & typescript';
const url = `https://ejemplo.com/buscar?q=${encodeURIComponent(busqueda)}`;
// Resultado: https://ejemplo.com/buscar?q=javascript%20%26%20typescript

// Decodificar
const params = new URLSearchParams('?q=javascript%20%26%20typescript');
const valor = params.get('q'); // 'javascript & typescript'
```

## Palabras clave

- Query string
- URLSearchParams
- GET parameters
- URL encoding
- window.location
- Search params
- Codificación URL

## Comparaciones típicas

- vs [[13 - Storage - localStorage]]: los parámetros de URL son públicos y temporales; localStorage es privado y persistente
- vs POST/[[12 - HTTP - Body]]: los parámetros GET tienen límite de tamaño y son visibles; POST usa body para datos grandes/sensibles
- vs [[15 - Cookies - Crear y usar cookies en JS]]: cookies se envían automáticamente al servidor; parámetros de URL deben ser procesados manualmente

## Preguntas de examen

- ¿Cómo se accede a los parámetros de la URL en JavaScript moderno?
- ¿Cuál es la diferencia entre `params.get()` y `params.getAll()`?
- ¿Por qué es importante usar `encodeURIComponent()` al construir URLs con parámetros?
- ¿Qué método se usa para modificar la URL sin recargar la página?
- ¿Cuál es el límite aproximado de caracteres en una URL y por qué es relevante?

## Errores comunes

- No codificar valores que contienen caracteres especiales (espacios, &, =, etc.)
- Asumir que los parámetros siempre existen sin verificar con `has()` o manejar `null`
- No validar/sanitizar los valores recibidos antes de usarlos (riesgo de XSS)
- Intentar enviar datos sensibles por URL (contraseñas, tokens) ya que quedan en el historial del navegador
- Olvidar que URLSearchParams no funciona en Internet Explorer (requiere polyfill)
- Usar parámetros de URL para datos que deberían ir en POST (datos grandes o sensibles)

## Mini-ejemplo (mental)

Los parámetros de URL son como **etiquetas en una caja de archivos**: la URL es la dirección del archivo, y los parámetros son notas adhesivas que especifican "categoría: facturas, año: 2024, ordenado por: fecha". Cualquiera que vea la caja sabe exactamente qué hay dentro sin abrirla, y puedes compartir la ubicación exacta con alguien más.
