# 4. De Starter Pack (Free) a Framework (Full)

[← Volver al README](../README.md)

> **Start Free. Upgrade Anytime. Keep Your Conversations.**

Ambas ediciones usan Data Tables de conversaciones compatibles. Si ya creaste conversaciones en Free, **puedes conservarlas al actualizar** a Full.

## Qué se conserva

- Tus Data Tables de conversación basadas en `ST_DialogueLine`.
- Los nombres de fila, el orden y el texto introducido.
- Los identificadores de eventos ya configurados, sujetos a mantener los receptores y su configuración.

## Migración paso a paso

1. **Haz una copia de seguridad** de tu proyecto antes de importar la nueva edición.
2. Incorpora **Dialogue System Framework (Full)** al proyecto conforme a su paquete de Fab.
3. Conserva las Data Tables de conversaciones creadas con Free.
4. En el Blueprint del jugador, utiliza el Actor Component de la edición Full.
5. Inicializa la interfaz de Full según su documentación y conecta tus Data Tables existentes a la función de reproducción correspondiente.
6. Prueba una conversación para verificar los textos, el orden, los tiempos y los eventos.
7. Configura las nuevas funciones de Full que quieras utilizar (decisiones, Rich Text, localización, voces o estilos de interfaz).

**Importante al importar:** si Unreal Engine solicita sobrescribir recursos con el mismo nombre, no aceptes automáticamente. Conserva copias y verifica las referencias de las Data Tables a la estructura adecuada en tu versión instalada.

No hay necesidad de transcribir de nuevo las conversaciones. La migración exacta de recursos del proyecto puede requerir revisar referencias según la manera en que se hayan importado ambas ediciones.

## Free vs Full

| Función | Free | Full |
|---|:---:|:---:|
| Actor Component en el jugador | ✅ | ✅ |
| Data Tables de conversaciones | ✅ | ✅ |
| Diálogos secuenciales | ✅ | ✅ |
| Eventos mediante Blueprint Interfaces | ✅ | ✅ |
| `Duration` y `DelayAfter` | ✅ | ✅ |
| Diferentes interfaces de diálogo | — | ✅ |
| Sistema de decisiones con Common UI | — | ✅ |
| Opciones de decisión mediante Data Tables | — | ✅ |
| Rich Text con colores | — | ✅ |
| Audio de voces sincronizado | — | ✅ |
| Localización EN/ES | — | ✅ |
| `AllowSkip` | — | ✅ |

## ¿Dónde se compra Full?

**[Dialogue System Framework (Full) en Fab](https://www.fab.com/listings/e6c1f535-2990-4551-8303-c3405ebd7aad)** — precio de referencia indicado por el autor: **USD 14.99** (consulta Fab para el precio vigente).

La edición Free continúa siendo gratuita y útil por sí misma; actualizar es opcional.
