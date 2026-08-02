---
name: ultimas-tareas
description: Reconstruye qué se hizo en las sesiones recientes del ecosistema VenBraX/Benbrax a partir de fuentes verificables (Drive, Routines, git, PRs) — no de transcripts de chat, que no son recuperables entre sesiones. Úsalo cuando Alfonso pregunte "qué se hizo últimamente", "últimas tareas", o pida un resumen de conversaciones recientes que ya no puede encontrar en la interfaz.
---

# Últimas tareas del ecosistema VenBraX

## Limitación de fondo (decirlo si Alfonso pregunta por qué no se puede "leer" un chat viejo)

Esta sesión de Claude Code NO tiene acceso al contenido de otras conversaciones/sesiones de
Alfonso, ni siquiera de este mismo repo. No existe una herramienta para listar o leer
transcripts de chats pasados. Si una conversación se cerró de golpe (crash, error de página,
etc.) y no llegó a escribir en el HANDOFF MAESTRO, ese contenido se considera perdido — no se
puede "reconstruir" palabra por palabra.

Lo que SÍ se puede hacer es reconstruir la actividad real reciente a partir de rastros objetivos
que las sesiones dejan aunque hayan crasheado. Ese es el propósito de este comando.

## Pasos a ejecutar

1. **HANDOFF MAESTRO (Drive)** — buscar el documento "VenBraX — HANDOFF MAESTRO" (Google Drive
   search_files, `fullText contains 'HANDOFF MAESTRO'`), leerlo completo. Es la fuente de verdad
   más reciente confirmada por sesiones que sí cerraron bien. Anotar su fecha de última
   actualización — todo lo posterior a esa fecha es lo que hay que reconstruir con los pasos
   siguientes.

2. **Routines (Claude Code Remote)** — `list_triggers` y revisar `last_fired_at` de cada Routine
   activa (Reporte diario AM/PM, Auditor de Oportunidades, Daily Ecosystem Check, Content 24/7
   Engine, etc.). Esto dice CUÁNDO corrió cada una por última vez, aunque no el contenido
   completo de esa corrida — para el contenido, cruzar con el HANDOFF si esa Routine lo actualiza.

3. **Git — actividad real por repo** — para cada repo disponible en el entorno actual
   (`venbratech.github.io`, `machine-force`, `nextjs-boilerplate`, u otros que Alfonso mencione):
   ```
   git log --since=72.hours.ago --oneline --all
   ```
   Esto es la evidencia más confiable de "qué se hizo" — un commit no se pierde aunque la sesión
   que lo generó se haya caído después.

4. **Pull Requests (GitHub)** — `list_pull_requests` / `search_pull_requests` en los repos de
   `venbraproyeccion-code1` para ver PRs abiertos o mergeados recientemente, y su estado de CI.

5. **Compilar el reporte** — en español, breve, con esta estructura:
   - Última actualización confirmada del HANDOFF MAESTRO (fecha).
   - Actividad detectada DESPUÉS de esa fecha (commits, PRs, fires de Routines) — con links
     directos siempre (regla permanente del handoff).
   - Vacíos explícitos: qué ventana de tiempo no tiene ningún rastro verificable (ej. "sesión de
     hoy ~10am no dejó commits ni actualización de handoff — contenido no recuperable").
   - Si corresponde, sugerir integrar lo encontrado al HANDOFF MAESTRO (misma versión, mismo
     título, pedir a Alfonso que borre la anterior) para que no se vuelva a perder.

## Regla de honestidad

Nunca presentar esta reconstrucción como si fuera "la conversación recuperada". Es un resumen de
artefactos objetivos. Si no hay rastro de algo que Alfonso recuerda haber hecho o hablado, decirlo
así de claro en vez de inventar contenido (regla permanente #6 del handoff: no inventar
capacidades ni datos).
