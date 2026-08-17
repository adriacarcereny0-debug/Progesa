# Progesa Seguridad — web corporativa

## Dominio pendiente

El dominio `progesa.es` se da por perdido; el cliente aún no ha decidido el
dominio nuevo. Mientras tanto, todas las URLs absolutas propias del sitio
usan el marcador `__DOMINIO__` (por ejemplo `__DOMINIO__/img/logo-512.png`)
en vez de una URL real, para poder hacer un único reemplazo en cuanto el
dominio se decida. Afecta a:

- `index.html`: `canonical`, Open Graph, Twitter Card, y los `@id`/`url` del
  JSON-LD.
- `sitemap.xml`
- `robots.txt` (línea `Sitemap:`)

Antes de publicar, sustituir `__DOMINIO__` por la URL real sin barra final
(p. ej. `https://www.progesa-nuevo.es`) en los tres archivos.

**Excepción:** los cuatro documentos legales (aviso legal, política de
privacidad, política de cookies y política de calidad) siguen enlazados al
dominio antiguo `https://www.progesa.es/...` porque ahí es donde están
alojados hoy. Cada enlace está marcado en el código con
`<!-- PENDIENTE: rehospedar en el dominio nuevo -->`. Cuando el cliente
entregue esos documentos para alojarlos en el dominio nuevo, actualizar esos
enlaces y quitar los comentarios.

## Si se recupera el dominio antiguo

Si el cliente llega a recuperar `progesa.es`, aunque sea temporalmente, hay
que configurar redirecciones 301 desde las URLs del dominio antiguo hacia
las equivalentes del dominio nuevo, para no perder el posicionamiento que
tuviera indexado. Sin esas redirecciones, cualquier enlace externo o
resultado de búsqueda que apunte al dominio antiguo dejará de funcionar.
