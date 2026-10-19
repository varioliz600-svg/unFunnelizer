# unFunnelizer

Este repositorio contiene la extensión Chrome "unFunnelizer" y el metadato mínimo para que Claude lo reconozca como un plugin/entrada de marketplace.

Componentes declarados

- frontend: Extensión Chrome (manifest.json, content_script.js, service_worker.js, popup.html, popup.js, popup.css)
- metadata: `.claude-plugin/plugin.json` (metadatos del plugin) — incluye nombre, descripción, iconos y manifest_url
- ai-manifest (opcional): `.well-known/ai-plugin.json` y `.well-known/openapi.yaml` (manifiesto de plugin/placeholder) referenciado desde `.claude-plugin/plugin.json`
- iconos: `icons/icon48.svg`, `icons/icon128.svg`

Propósito

La extensión detecta y elimina overlays/funnels/modales que bloquean la navegación y desbloquea el scroll. El paquete incluye metadatos que permiten a Claude (o a su validador de marketplace) reconocer este repositorio como una entrada de plugin.

Notas para empaquetado (ZIP)

- Si vas a subir el repositorio como ZIP a Claude, asegúrate de que el ZIP incluya la ruta exacta `.claude-plugin/plugin.json` en la raíz del ZIP, o que exista `SKILL.md` (este archivo) en la raíz del ZIP; cualquiera de los dos satisface el requisito de declaración del plugin.
- Comando para crear ZIP desde la raíz del proyecto (macOS/Linux):
  zip -r ../unFunnelizer-main.zip .

Contacto y edición

Si quieres que actualice los campos de `.claude-plugin/plugin.json` (por ejemplo contact_email o manifest_url) o que genere un ZIP y te lo entregue, dímelo y lo hago.