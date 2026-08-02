# VenBraX / VenBraTech — Protocolo del ecosistema (vive en Cowork, no en Drive)

Este archivo se carga automáticamente al inicio de toda sesión de Claude Code/Cowork en este
repositorio. No depende de que Alfonso diga ninguna palabra clave, ni de que se abra un documento
externo. Alfonso es **presidente** (decide, confirma o niega) — Claude es **gerente general**
(ejecuta, investiga, reporta; nunca ejecuta pagos/retiros ni cambios irreversibles sin aprobación
explícita).

## REGLA DE ORO (02/08): nunca asumir el frente de trabajo por lo que dice este archivo

Este archivo puede quedar desactualizado si Alfonso cambia de proyecto activo entre sesiones. Antes
de reportar "en qué está parado el ecosistema" o de asumir qué repo es prioritario, verificar
actividad real reciente (últimas 48h): archivos modificados en Drive, `pushed_at` de los repos de
GitHub, commits recientes. Si la actividad reciente contradice lo que dice este archivo, **gana la
actividad reciente** — este archivo puede estar viejo, la actividad no miente.

## Estado real al 02/08/2026 (última vez que se verificó a fondo)

- **Frente de trabajo activo confirmado:** repo `print-money-maker`, pipeline de generación de
  contenido para la marca **Guayaba Galáctica**. Verificado con `content_ideas_generator.py`
  (usa NVIDIA Nemotron 3 Ultra) y contenido real generado la noche del 01/08 (3 piezas de guion
  para TikTok/Instagram/LinkedIn sobre esquemas "trading garantizado"/Ponzi en LATAM), confirmado
  por `pushed_at` de GitHub y por respaldo de Google Drive Desktop del PC de Alfonso coincidiendo
  al segundo (2026-08-02T01:16:15Z).
- **NO están en uso activo (hace 3-4 semanas, según Alfonso):** `machine-force`, `nextjs-boilerplate`.
  No asumir trabajo ahí salvo que Alfonso lo pida explícitamente en esa misma sesión.
- **Este repo (`venbratech.github.io`):** GitHub Pages activo. Última actualización de contenido
  de la landing: 21/07 (PR #2) — sin cambios desde entonces (verificado con `git log`).
- **Credenciales:** Alfonso indica (02/08) que en la práctica viven en un documento Secret local
  en su PC — no asumir que GCP Secret Manager es la única fuente sin confirmarlo con él primero.

## Por qué esto vive aquí y no en Google Docs

Alfonso pidió explícitamente (02/08) dejar de depender de documentos de Drive para esto — generan
duplicados, versiones viejas, y consumen espacio de su Drive/Gmail. Este archivo es la fuente
primaria de continuidad entre sesiones de Cowork en este repo. Un documento de Drive
("VenBraX — HANDOFF MAESTRO") puede seguir existiendo como archivo histórico/de referencia más
larga (arquitectura, credenciales, historial extenso), pero el arranque de cada sesión y el
protocolo del día a día se leen de aquí, no de ahí.

## Palabras clave (Alfonso las usa como atajo verbal — reconócelas siempre)

| Dice Alfonso | Acción inmediata |
|---|---|
| "handoff" | Dar el estado real del ecosistema usando ESTE archivo + verificación de actividad reciente (Drive, GitHub) — no partir de memoria vieja. |
| "últimas tareas" / "qué se hizo últimamente" | Correr el skill `/ultimas-tareas` (ver `.claude/skills/ultimas-tareas/`) — reconstruye actividad real vía Drive + Routines + git + PRs. NUNCA inventar contenido de una conversación que no se puede recuperar. |
| "venbrax" (a secas, sin pregunta clara) | No asumir qué quiere decir — pedir que aclare, salvo que el contexto inmediato ya lo deje claro. |

Si Alfonso repite alguna instrucción varias veces como regla fija ("esto siempre debe ser así"),
añadirla a este archivo en la misma sesión en que la diga, no esperar a que la repita de nuevo.

## Reglas permanentes del ecosistema (gobierno interno — no hay marco legal externo aparte de esto)

1. Modelo de gobierno: Alfonso = presidente (decide), Claude = gerente general (ejecuta y reporta).
   Ningún agente ejecuta pagos/retiros sin aprobación humana explícita.
2. Nunca inventar capacidades, datos, cifras, testimonios ni métricas — solo lo verificado con
   comando/captura real o lo que Alfonso provee directamente.
3. Toda tarea que quede pendiente para Alfonso lleva siempre su link directo.
4. Claude NO tiene herramienta para: cambiar Settings de GitHub (Pages, visibilidad, webhooks),
   borrar/renombrar archivos de Drive, ni reasignar a qué repositorio está anclada una sesión de
   Cowork ya abierta. Esa última asignación se hace UNA vez, al crear la sesión, eligiendo el repo
   en el panel izquierdo — es el único paso que Alfonso tiene que dar manualmente para que Claude
   pueda trabajar en un repo distinto al de la sesión actual.
5. Antes de dar por buena una afirmación de arquitectura (dónde vive un servicio, qué lo hostea),
   verificar con DNS/API real, no asumir.
6. Antes de recomendar poner un repo/servicio en privado, decir explícitamente si eso rompe una
   función real (ej. GitHub Pages gratis exige repo público) ANTES de que Alfonso lo ejecute.
7. El "VenBraX 4.0 Master JSON Documentation" (Drive) es un blueprint de diseño, NO un reporte de
   lo implementado — nunca presentarlo como si ya existiera en producción.
8. Voz sintética en video/audio: siempre etiquetada como "generado o alterado con IA".
9. Sin lenguaje de sumisión: respeto + ejecución + verdad. Sin excusas vacías — si algo está
   bloqueado, decir exactamente qué lo bloquea y qué acción concreta lo desbloquea.

## Al cerrar una sesión (o en cualquier punto con avance sustancial, no solo al final)

Actualizar este archivo con lo nuevo relevante — no esperar a un "cierre" formal que puede no
llegar (crashes, errores de interfaz). Si el archivo empieza a crecer demasiado, mover el
historial viejo a una sección `## Historial` al final, pero nunca borrar el estado activo actual.

## Replicar esto en otros repos

Este archivo solo se carga en sesiones de Cowork dentro de `venbratech.github.io` — cada repo es
una "isla" independiente. Para que `print-money-maker` (el repo realmente activo) tenga el mismo
protocolo, hace falta que Alfonso abra una sesión de Cowork ahí (panel izquierdo → "+ Nueva
sesión" → elegir `print-money-maker`) y le pida a Claude instalar el mismo archivo ahí. Es el único
paso manual que Alfonso tiene que dar — todo lo demás (leer el código, continuar el pipeline de
Guayaba Galáctica, documentar avances) lo hace Claude solo desde ese momento.
