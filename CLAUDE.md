# Reglas operativas del ecosistema VenBraX

Este repo (venbratech.github.io) es parte del ecosistema VenBraX. Cualquier
sesión de Claude Code que trabaje aquí sigue estas reglas fijas:

## Credenciales y secretos

- Ningún token, API key o credencial se escribe jamás en un archivo del
  repositorio, en un commit, ni en un doc compartido en texto plano — este
  repo es público (GitHub Pages).
- Las claves reales viven en **Google Cloud Secret Manager** (proyecto
  `venbrax`), no en Drive, no en el chat, no en el código.
- Antes de crear o usar cualquier token/API key, decir explícitamente en la
  conversación cuál se va a usar y para qué, antes de usarla. La aprobación
  ocurre de forma visible en el chat (no hay integración de Telegram/WhatsApp
  disponible para aprobar fuera de banda).
- Si hace falta una API key nueva, siempre se entrega primero el link directo
  de creación/registro y el paso a paso exacto que el usuario debe ejecutar
  él mismo — nunca asumir que Claude puede generarla o conseguirla solo.

## Límites de acceso reales

- Claude Code no tiene acceso al navegador, historial (Chrome/Edge) ni CPU
  local del usuario. Solo ve lo que ocurre en la sesión actual y lo que el
  usuario comparte explícitamente (texto, capturas, links).
- No existe acceso a otras conversaciones (claude.ai, otras sesiones de
  Claude Code) salvo que el usuario las pegue o las resuma.

## Infraestructura actual (ver Drive para detalle completo)

- n8n migrando a Google Cloud (proyecto `venbrax`, VM `venbratech-n8n`,
  zona us-central1-f) — Railway y Render quedaron sin capacidad gratuita.
- El documento de handoff completo vive en Google Drive: "VenBraX — Handoff
  y Estado del Sistema" + actualizaciones fechadas (ver carpeta raíz del
  Drive de venbraproyeccion@gmail.com).

## Continuidad entre sesiones — leer esto primero

Cualquier sesión nueva (Claude Code u otra) debe empezar leyendo, en este
orden, los docs de Google Drive en la carpeta raíz de
venbraproyeccion@gmail.com:

1. "VenBraX — Handoff y Estado del Sistema" (contexto general, arquitectura).
2. "VenBraX — Corrección de Estado: Dedicación 100% al Ecosistema" (Alfonso
   ya no trabaja en Kellanova desde marzo 2026, dedicación 100% al proyecto).
3. "VenBraX — Actualización de Sesión 2026-07-10" (sitio web, PR, Telegram bot).
4. "VenBraX — Inventario Secret Manager 2026-07-10" (qué API keys existen,
   sus nombres en Secret Manager — nunca los valores).
5. "VenBraX — Guayaba Galáctica: Setup Facebook/Instagram API 2026-07-10"
   (estado exacto del bloqueador pendiente: token de usuario del sistema
   `n8n-venbrax-bot` creado y guardado como secreto `facebook-system-user-token`,
   esperando que Meta propague permisos — última prueba dio error #100).

No asumir que "estoy aquí" o un mensaje corto del usuario ya trae este
contexto — pedirle que confirme qué se resolvió desde el último doc antes
de seguir, en vez de repetir pasos ya hechos.

## Monetización

- "Tokenizar" en este proyecto significa un sistema de puntos/recompensas
  interno, no un token cripto. Un token cripto real queda descartado salvo
  asesoría legal futura (el sitio se posiciona como "regulado por la SEC",
  lo que hace riesgoso lanzar un valor no registrado con la misma marca).
