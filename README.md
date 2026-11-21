# Guía Leonida · contenido público

Lo que lee la app sin publicar otra versión:

- `contenido.json`: toda la guía. Para actualizarla, edita este archivo, **sube `version` en 1** y súbelo. La app lo descarga sola (y al tirar hacia abajo en Inicio). Si el JSON está roto o su versión es menor, la app lo ignora y sigue con el que tiene.
- `privacidad.html`: política de privacidad (Google Play pide una URL pública).

Reglas del contenido: cada dato lleva `fuente` (`oficial`, `medios` o `rumor`), los spoilers van con `"spoiler": true`, y no se publican códigos de trucos hasta que coincidan dos medios serios.

## Imágenes

`imagenes/` tiene capturas oficiales del kit de prensa de Rockstar (rockstargames.com/VI/media), optimizadas a 1280 px. El JSON las referencia con rutas como `imagenes/jason-1.jpg` (campos `portada`, `regiones[].imagenes`, `personajes[].imagenes`) y muestra el crédito de `creditoImagenes`.

**Para quitarlas** (por ejemplo, si Rockstar o Google lo piden): borra esos campos del JSON, sube `version` en 1 y súbelo. Las apps dejan de mostrarlas sin publicar otra versión y vuelven a las ilustraciones propias. Luego puedes borrar la carpeta.

El **mapa oficial** (`imagenes/mapa-oficial.jpg` y `mapa-oficial-mini.jpg`, del kit de prensa de Rockstar) se referencia en el campo `mapaOficial` y en `regiones[].mapaOficial` (posición de cada pin). Para quitarlo, borra `mapaOficial`: la app vuelve al mapa ilustrado propio.
