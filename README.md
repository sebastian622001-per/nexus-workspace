# NEXUS Workspace v0.1

PWA personal de coste cero para Campus y ATLAS. Archivos estáticos; no requiere Firebase ni API.

## Instalación

1. Crea un repositorio nuevo en GitHub, por ejemplo `nexus-workspace` (no uses el repositorio AUREX).
2. Sube `index.html`, `app.js`, `sw.js` y `manifest.webmanifest` a la raíz.
3. Settings → Pages → Deploy from branch → main → /(root).
4. Abre la URL HTTPS de GitHub Pages en Safari y usa Compartir → Añadir a pantalla de inicio. En Windows, abre la misma URL con Edge o Chrome y usa Instalar aplicación.

## Limitaciones importantes

- Los datos viven en localStorage de **cada navegador y dispositivo**, no se sincronizan automáticamente.
- Exporta JSON periódicamente y restáuralo en el otro dispositivo si lo deseas. Restaurar reemplaza todos los datos actuales, no fusiona cambios.
- No hay acceso a archivos de universidad, ni IA integrada, ni notificaciones en segundo plano.
- El temporizador se corrige con reloj al volver a la página, pero el sistema puede suspender la página en segundo plano.
- No guardar contraseñas ni datos sensibles.
- La app puede funcionar sin conexión después de una primera visita con conexión y de que se instale el service worker.

## Prueba de aceptación

1. Añade Econometría, una tarea con fecha y un examen.
2. Guarda un apunte y verifica que aparece tras recargar.
3. Crea un proyecto ATLAS, cambia su estado, registra una decisión y una tarea.
4. Completa una tarea y verifica el contador de Inicio.
5. Prueba el temporizador (25 min o reduce temporalmente para desarrollo).
6. Exporta JSON, abre el archivo para confirmar su contenido, y prueba restaurarlo en otro navegador con datos no importantes.
7. Desactiva internet y comprueba que carga después de la primera visita online.
