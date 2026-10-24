# Mi TV Launcher — proyecto inicial

Proyecto Android para un TV Box genérico con Android 10. Incluye un launcher sencillo con navegación por control remoto y una lista de apps instaladas que Android expone como lanzables.

## Compilar el APK desde GitHub Actions (sin computador)
1. Crea un repositorio nuevo en GitHub, preferiblemente **Private**.
2. Sube los archivos y carpetas de este proyecto al repositorio, conservando su estructura.
3. En la pestaña **Actions**, habilita los workflows si GitHub te lo solicita.
4. Abre **Build Mi TV Launcher APK** y pulsa **Run workflow** (o espera a que se ejecute al subir cambios).
5. Cuando termine en verde, abre esa ejecución, baja a **Artifacts** y descarga `mi-tv-launcher-debug-apk`.
6. Descomprime el artefacto descargado; dentro estará `app-debug.apk`.

## Importante para subirlo desde celular
GitHub móvil no siempre permite subir una carpeta completa conservando su estructura. **No basta con subir este ZIP como un archivo al repositorio**, porque GitHub Actions no lo descomprime automáticamente.
Si el navegador móvil permite “Upload files”, descomprime primero el ZIP en una app de archivos y sube el contenido conservando la estructura. Si no permite carpetas, se puede abrir un Codespace desde el repositorio y extraer el ZIP en la terminal web.

## Instalar
Copia `app-debug.apk` a un USB, abre el archivo en el TV Box y permite la instalación desde esa fuente si Android lo solicita. Luego pulsa Home para elegir el launcher si el sistema lo permite.

## Limitaciones
- Es un APK de depuración para pruebas, no una versión de distribución firmada con una clave privada propia.
- No se garantiza compatibilidad con todos los TV Box. Debe probarse en el Orion.
- Algunas apps (incluida Xuper Hydra u otras apps de TV) podrían no aparecer si no exponen una actividad lanzable a Android.
