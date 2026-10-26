# Dialogue System — Starter Pack (Free)

**Sistema gratuito de diálogos para Unreal Engine 5 · 100 % Blueprints · Actor Component · Data Tables**

Crea conversaciones secuenciales, muestra diálogos en pantalla y ejecuta acciones de juego mediante Blueprint Interfaces. El Starter Pack está pensado para aprender, prototipar y utilizar diálogos en proyectos propios.

> **Empieza gratis. Actualiza cuando quieras. Conserva tus conversaciones.**
>
> Las Data Tables de conversaciones creadas con esta edición son compatibles con **Dialogue System Framework (Full)**. Para actualizar, conserva tus Data Tables y conéctalas al componente de diálogo de Full: **no necesitas volver a escribir las conversaciones**.

**[Probar demo jugable (MEGA)](https://mega.nz/file/VjxkjD6R#zBJXSqZcaMePbTdpOoSafXH3vYIR1wc4s2NQn0zwyWk)** · **[Descargar Starter Pack gratuito en Fab](https://www.fab.com/listings/1d39c10d-b6b0-4dd1-b704-8b3d60658e23)** · **[Ver Framework completo en Fab](https://www.fab.com/listings/e6c1f535-2990-4551-8303-c3405ebd7aad)**

## Contenido de esta documentación

1. [Instalación e inicio rápido](docs/01-instalacion.md)
2. [Creación de conversaciones y Data Tables](docs/02-conversaciones.md)
3. [Eventos con Blueprint Interfaces](docs/03-eventos.md)
4. [Comparación Free vs Full y migración](docs/04-migracion-full.md)
5. [Preguntas frecuentes y solución de problemas](docs/05-problemas-frecuentes.md)

## Características de Free

- Sistema de diálogos secuenciales basado en **Data Tables**.
- Implementación **100 % Blueprint**, sin programar C++.
- Componente `AC_Dialogue`, que se agrega directamente al Blueprint del jugador.
- No es necesario reemplazar `GameInstance`, `GameMode` ni `PlayerController`.
- Nombres de personajes y una interfaz de diálogo incluida.
- Duración de línea (`Duration`) y pausa posterior (`DelayAfter`).
- Eventos de juego mediante `BPI_DialogueEvents` y `TriggerEvent`.
- Estructura de datos preparada para actualizar a la edición completa.

El componente está diseñado para integrarse con las plantillas habituales de Unreal Engine, incluyendo primera y tercera persona. **La configuración de entrada y la integración pueden variar según la plantilla**; consulta la [guía de instalación](docs/01-instalacion.md).

## Tu primera conversación en tres pasos

1. Agrega `AC_Dialogue` al Blueprint de tu personaje.
2. En `BeginPlay`, llama a `Dialogue Create Widget` usando `AC_Dialogue` como `Target`.
3. Llama a `Dialogue Play Conversation`, con el mismo `Target`, y selecciona la **Data Table** en el pin `Conversation`.

```text
Event BeginPlay
    └─ Dialogue Create Widget  (Target: AC_Dialogue)
          └─ Dialogue Play Conversation  (Target: AC_Dialogue)
                └─ Conversation: tu Data Table
```

Este ejemplo reproduce un diálogo automáticamente al iniciar el nivel. En un juego puedes iniciar la conversación con otro evento, como la interacción con un NPC.

## Free vs Full

| Funcionalidad | Free | Full |
|---|:---:|:---:|
| 100 % Blueprints | ✅ | ✅ |
| Conversaciones con Data Tables | ✅ | ✅ |
| Nombre de personajes | ✅ | ✅ |
| Diálogos secuenciales | ✅ | ✅ |
| Eventos mediante Blueprint Interfaces | ✅ | ✅ |
| `Duration` / `DelayAfter` | ✅ | ✅ |
| Actor Component sin GameInstance personalizado | ✅ | ✅ |
| Migración de Data Tables Free → Full | ✅ | ✅ |
| Múltiples interfaces de diálogo | — | ✅ |
| Sistema de decisiones con Common UI | — | ✅ |
| Decisiones definidas mediante Data Tables | — | ✅ |
| Rich Text: palabras resaltadas con colores | — | ✅ |
| Voces y sincronización de audio | — | ✅ |
| Localización español/inglés | — | ✅ |
| Omisión configurable por línea (`AllowSkip`) | — | ✅ |

**Importante:** La estructura `ST_DialogueLine` incluye columnas usadas por Full aunque algunas **no ejecutan su funcionalidad en Free**. Se conservan para mantener la compatibilidad. Consulta [los detalles de los campos](docs/02-conversaciones.md).

### ¿Cuándo conviene actualizar?

Cuando necesites **decisiones interactivas, Rich Text, diferentes interfaces de diálogo, audio sincronizado o localización**, puedes actualizar sin recrear tus Data Tables de conversaciones.

**[Ver Dialogue System Framework (Full) en Fab](https://www.fab.com/listings/e6c1f535-2990-4551-8303-c3405ebd7aad)**

## Demo jugable

**[Descargar la demo jugable desde MEGA](https://mega.nz/file/VjxkjD6R#zBJXSqZcaMePbTdpOoSafXH3vYIR1wc4s2NQn0zwyWk)**. La demo permite probar el sistema antes de incorporarlo a un proyecto. Es opcional y no sustituye el paquete de Unreal Engine distribuido en Fab. **Antes de anunciar su plataforma y requisitos definitivos, comprueba el contenido descargado en un equipo limpio.**

## Soporte

- [Comunidad en Discord (español)](https://discord.gg/JY5JTQaWqn)
- [Producto gratuito en Fab](https://www.fab.com/listings/1d39c10d-b6b0-4dd1-b704-8b3d60658e23)

## Estado de la guía

**Versión de revisión en español.** Los pasos principales están documentados con los nombres observados en el proyecto. El recorrido de `ExecuteDialogueEvent` en `AC_Dialogue` está documentado a partir de las capturas del Blueprint: el componente busca actores con `BPI_DialogueEvents` y envía el mensaje a cada uno. Consulta la [guía de eventos](docs/03-eventos.md).

También añadiremos capturas originales del sistema a `images/` y publicaremos la traducción al inglés cuando esta versión haya sido revisada.
