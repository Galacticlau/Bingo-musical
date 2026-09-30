# Bingo musical · El show de los 80

Interfaz en español para el Día del Asistente de la Educación. Incluye 52 canciones y los cartones B01–B50 de Claudia, con «Filo contigo — Miguelo» corregido.

## Abrir

Descarga `index.html` y ábrelo con Chrome o Edge. No requiere instalación, servidor ni conexión para jugar. Para usar una dirección web, activa GitHub Pages en **Settings → Pages → Deploy from a branch → main → / (root) → Save**.

## Preparar

1. Pulsa **Cargar canciones** y selecciona directamente **Canciones Bingo.zip**, o los archivos de audio descomprimidos. No subas los audios a este repositorio.
2. Revisa las 52 asociaciones: los títulos de los archivos se comparan con los de las canciones. Los 52 archivos del ZIP proporcionado ya tienen asociaciones verificadas. Se ignoran los archivos auxiliares de Mac y se admite MP4. Las coincidencias dudosas de otros archivos quedan para selección manual.
3. Pulsa **Barajar y guardar orden**. El orden se decide una vez y se guarda en este navegador. Puedes exportarlo e importarlo en otro computador.
4. Pulsa **Sortear canción**. La animación sigue ese orden, sin volver a barajar. El título queda oculto al comenzar el audio; **Revelar canción** lo añade al historial.
5. Para automatizar el show, activa el avance automático y ajusta fragmento y pausa. El fragmento comienza desde el inicio del archivo. Prueba volumen y archivos antes del evento.
6. **Proyectar** oculta la configuración y el reproductor; conserva los botones del show. Escape sale de pantalla completa.

**¡BINGO!** detiene el audio y el avance automático. Ingresa el número de cartón para verificar sus 12 canciones contra el historial revelado. Muestra también todos los cartones completos. Tener combinaciones diferentes no garantiza que haya un solo ganador; acuerda un desempate antes de jugar.

## Recuperar una partida

El progreso y el orden se guardan en el navegador. Tras recargar, selecciona nuevamente los audios: por privacidad no se guardan ni se suben. Puedes continuar el audio actual desde el inicio. El JSON exportado contiene solo el orden, no el progreso ni los archivos. Reiniciar conserva los audios cargados y el orden, pero borra las canciones reveladas.

## Código

Todo está en `index.html`: HTML estructura las pantallas; CSS dibuja el estilo ochentero; JavaScript administra el orden, los audios, el historial y la comprobación. `DATA.songs` contiene las canciones y `DATA.cards` las combinaciones exactas de los 50 cartones. `localStorage` conserva el progreso localmente. Las URL de audio temporales permiten reproducir los archivos sin enviarlos a internet.

## Validación

Se comprobó la descompresión del ZIP real, 52 asociaciones únicas y pistas de audio en los 52 archivos. Se probaron la generación del orden, el bloqueo por archivos faltantes y la comprobación de cartones completos e incompletos. La reproducción y el aspecto visual deben comprobarse en el navegador del evento.
