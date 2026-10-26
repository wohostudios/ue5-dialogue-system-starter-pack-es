# 5. Preguntas frecuentes y problemas comunes

[← Volver al README](../README.md)

### La conversación no comienza

Confirma que el jugador tenga `AC_Dialogue`, que `Dialogue Create Widget` se ejecute antes de `Dialogue Play Conversation`, que ambos nodos tengan el `Target` conectado a `AC_Dialogue` y que `Conversation` tenga una Data Table válida.

### El diálogo se ejecuta, pero no veo la interfaz

Verifica que `Dialogue Create Widget` se haya ejecutado. Revisa el orden de los nodos y que estés utilizando el personaje que efectivamente posee el componente.

### Las líneas aparecen en un orden inesperado

Revisa la propiedad `Order` de todas las filas y sus valores. Recuerda que `Row Name` y `Order` son propiedades distintas.

### Un evento (`TriggerEvent`) no funciona

Verifica el nombre exacto, la implementación de `BPI_DialogueEvents`, los casos de `Switch on Name` y el receptor del mensaje. Consulta [Eventos](03-eventos.md). La interfaz debe estar implementada en un actor que exista en el mundo cuando se lance el evento.

### `AllowSkip` aparece, pero no hace nada

Es normal: **la omisión configurable por línea es exclusiva de Full**. El campo aparece en Free para mantener la compatibilidad de `ST_DialogueLine`.

### Veo columnas `Audio_EN`, `Audio_ES` y `Text_ES`. ¿Free incluye voces y localización?

No. Las columnas se conservan en la estructura compartida; las funciones avanzadas de voces y localización están reservadas para Full.

### ¿Puedo integrar el sistema en una plantilla First Person o Third Person?

Sí: agrega `AC_Dialogue` al Blueprint de tu personaje y llama a las funciones descritas en [Instalación](01-instalacion.md). La manera de iniciar las conversaciones por interacción puede variar entre plantillas.

### ¿Necesito reemplazar `GameInstance`?

No. Ambas ediciones emplean un Actor Component y no requieren el antiguo `BP_DialogueGameInstance`.

### ¿Perderé mis diálogos al pasar a Full?

No necesitas recrear tus conversaciones: las Data Tables son compatibles. Haz una copia de seguridad e importa Full cuidadosamente para conservar los recursos existentes. Lee [Migración](04-migracion-full.md).

### ¿Dónde consigo ayuda?

[Discord de soporte (español)](https://discord.gg/JY5JTQaWqn) · [Ficha gratuita en Fab](https://www.fab.com/listings/1d39c10d-b6b0-4dd1-b704-8b3d60658e23)
