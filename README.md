# Portal Analista de OTAs · Loggro Alojamientos

Guía de consulta para que AM, Implementación y SAC sepan cuándo agendar una sesión con el Analista de OTAs, cuándo crear ticket y qué tener listo antes de hacerlo.

Es un solo archivo (`index.html`) con HTML, CSS y JavaScript. No necesita instalación ni servidor.

## Publicar con GitHub Pages

1. En GitHub, crea un repositorio nuevo (por ejemplo `portal-analista-otas`).
2. Sube `index.html` y este `README.md` a la rama `main` (botón **Add file → Upload files**).
3. Entra a **Settings → Pages**.
4. En **Build and deployment**, elige **Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. En uno o dos minutos GitHub muestra la URL del sitio, con el formato `https://<usuario-u-organización>.github.io/portal-analista-otas/`.

## Visibilidad

En los planes gratuitos, GitHub Pages publica el sitio en internet aunque el repositorio sea privado. El portal contiene links internos de HubSpot (calendario y formularios). Si debe quedar solo para personal de Loggro, valida con TI si la organización tiene GitHub Enterprise Cloud con control de acceso a Pages, o usa otra alternativa interna.

## Cómo actualizar

Todo lo editable está al inicio del bloque `<script>` de `index.html`:

| Qué cambiar | Dónde |
|---|---|
| Links del calendario y formularios | `CONFIG.links` (campo `url`; `null` muestra "Link pendiente") |
| Canal de Teams de Mantenimiento | `CONFIG.teamsChannel` |
| Rutas de cada área | `FLOWS` |
| Checklist de cada área | `CHECK` |
| Pestañas del menú | `PAGES` |

Los textos de cada pestaña están en el HTML, en los bloques `<div class="page" data-page="...">`.

Después de editar, haz commit en `main` y GitHub Pages publica el cambio solo.

## Pendiente conocido

Cuando termine la capacitación de OTAs para Implementación, hay que actualizar la ruta "Inconsistencia de OTAs" en la pestaña Implementación (`FLOWS.Implementacion`, el aviso de capacitación y la pestaña Alcance).
