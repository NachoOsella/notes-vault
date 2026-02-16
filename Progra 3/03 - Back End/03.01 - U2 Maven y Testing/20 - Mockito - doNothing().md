# Mockito - doNothing()

## Definición
El método `doNothing()` se utiliza para configurar un mock de manera que no haga nada cuando se llama a un método `void`. Es especialmente útil para spies y métodos que no retornan valor.

## Explicación
- *Qué problema resuelve*
    Permite stubear métodos `void` para que no ejecuten su código real (útil en spies) o para ignorar efectos secundarios no deseados en el test.
- *Cómo funciona por arriba*
    Se usa con la sintaxis `doNothing().when(mock).metodo()`. Cuando el método es invocado, simplemente no hace nada (no ejecuta código, no lanza excepciones).
- *Qué implica / qué permite*
    - Ignorar llamadas a métodos que tienen efectos secundarios (enviar emails, escribir logs, etc.).
    - Evitar que spies ejecuten el código real de métodos void.
    - Verificar que el método fue llamado sin que realmente haga algo.

## Sintaxis
```java
doNothing().when(mock).metodoVoid();
doNothing().when(mock).metodoVoid(argumentos);
```

## Ejemplos

### Ignorar un método void en un mock
```java
@Mock
private EmailService emailService;

@Test
void testProcess() {
    doNothing().when(emailService).sendEmail(any());
    
    myService.process(); // Internamente llama a emailService.sendEmail()
    
    verify(emailService).sendEmail(any()); // Verificamos que se llamó
}
```

### Evitar ejecución real en un spy
```java
List<String> realList = new ArrayList<>();
List<String> spyList = spy(realList);

// Sin doNothing, clear() realmente vaciaría la lista
doNothing().when(spyList).clear();

spyList.add("elemento");
spyList.clear(); // No hace nada

assertEquals(1, spyList.size()); // El elemento sigue ahí
```

### Caso típico: evitar envío de emails en tests
```java
@Spy
private EmailSender emailSender;

@Test
void testNotification() {
    doNothing().when(emailSender).send(any());
    
    notificationService.notifyUser(user);
    
    // Verificamos que se intentó enviar, pero no se envió realmente
    verify(emailSender).send(any());
}
```

## Comparación con otros métodos do*
| Método | Uso |
|--------|-----|
| `doNothing()` | El método void no hace nada |
| `doThrow()` | El método void lanza una excepción |
| `doReturn()` | Retorna un valor (útil para spies) |
| `doAnswer()` | Ejecuta lógica custom |

## Palabras clave
- doNothing
- Métodos void
- Stubbing
- Efectos secundarios
- Spy

## Comparaciones típicas
- vs [[18 - Mockito - thenReturn()]]: `doNothing` aplica a métodos `void`; `thenReturn` aplica a métodos con retorno.
- vs [[19 - Mockito - thenThrow()]]: `doNothing` simula "no pasa nada"; `doThrow` simula error en métodos void.

## Preguntas de examen
- ¿Para qué sirve `doNothing()` en Mockito?
- ¿Por qué no se puede usar `when().thenReturn()` con métodos void?
- ¿Cuándo es necesario usar `doNothing()` con spies?

## Errores comunes
- Intentar usar `when(mock.metodoVoid()).thenReturn(...)` (no compila, void no retorna).
- Olvidar usar `doNothing()` en spies y que el método void real se ejecute.
- Confundir con mocks: en mocks puros, los métodos void ya no hacen nada por defecto.

## Mini-ejemplo (mental)
`doNothing()` es como poner un cartel de "fuera de servicio" en una máquina. Cuando alguien intenta usarla (llamar al método), la máquina no hace nada: no dispensa producto, no cobra, no hace ruido. Pero podés verificar que alguien intentó usarla revisando las cámaras de seguridad (verify).
