# VenBraX / VenBraTech — Protocolo para cualquier sesión de Claude en este repo

Este archivo se carga automáticamente al inicio de toda sesión de Claude Code/Cowork en este
repositorio. No depende de que Alfonso diga ninguna palabra clave para activarse.

## Fuente de verdad del estado del ecosistema

El estado real (qué está hecho, qué está pendiente, credenciales, arquitectura) vive en Google
Drive, documento **"VenBraX — HANDOFF MAESTRO (documento único — actualizar siempre aquí)"**.
Es UN solo documento, se actualiza en el mismo archivo (nunca se crean copias nuevas).

## Palabras clave (Alfonso las usa como atajo verbal — reconócelas siempre)

| Dice Alfonso | Acción inmediata |
|---|---|
| "handoff" | Buscar y leer completo el HANDOFF MAESTRO en Drive antes de hacer cualquier otra cosa. Dar estado del ecosistema + últimas tareas. |
| "últimas tareas" / "qué se hizo últimamente" | Correr el skill `/ultimas-tareas` (ver `.claude/skills/ultimas-tareas/`) — reconstruye actividad real vía Drive + Routines + git + PRs. NUNCA inventar contenido de una conversación que no se puede recuperar. |
| "venbrax" (a secas, sin pregunta clara) | No asumir qué quiere decir — pedir que aclare, salvo que el contexto inmediato ya lo deje claro. |

Si Alfonso repite alguna instrucción varias veces como regla fija ("esto siempre debe ser así"),
proponer añadirla a esta tabla o a las REGLAS PERMANENTES del handoff en la misma sesión en que la
diga, no esperar a que la repita de nuevo en el futuro.

## Reglas permanentes que aplican a este repo específico

1. Este repo (`venbratech.github.io`) es la fuente de GitHub Pages para venbratech.com. Su
   visibilidad (público/privado) tiene una restricción real: Pages gratuito solo funciona con
   repo público. Antes de cambiar la visibilidad, confirmar con Alfonso el plan elegido (ver
   handoff, sección ARQUITECTURA) — no cambiarla unilateralmente ni recomendarla sin advertir esta
   consecuencia.
2. Nunca inventar capacidades, datos, ventas ni métricas — solo lo verificado con comando/captura
   real (regla permanente #5/#6 del handoff).
3. Toda tarea para Alfonso lleva siempre su link directo (regla permanente #6 del handoff).
4. Esta sesión de Claude NO tiene herramienta para cambiar GitHub Settings (Pages, visibilidad,
   webhooks) — eso lo hace Alfonso directo en el navegador.
5. Antes de dar por buena una afirmación de arquitectura (dónde vive un servicio, qué lo hostea),
   verificar con DNS/API real, no asumir.

## Al cerrar una sesión que tocó algo relevante del ecosistema

Actualizar el HANDOFF MAESTRO en Drive (misma versión, mismo título, pedir a Alfonso que borre la
anterior) — no dejar que el conocimiento de la sesión se pierda si la conversación se cae o no se
vuelve a encontrar.
