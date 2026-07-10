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

## Monetización

- "Tokenizar" en este proyecto significa un sistema de puntos/recompensas
  interno, no un token cripto. Un token cripto real queda descartado salvo
  asesoría legal futura (el sitio se posiciona como "regulado por la SEC",
  lo que hace riesgoso lanzar un valor no registrado con la misma marca).
