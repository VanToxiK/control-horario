# Mi Fichaje

App para el móvil que registra la hora de entrada y de salida. Calcula al minuto lo que se trabaja de más o de menos cada día y en todo el mes.

- Jornada de lunes a viernes: 8 h (turno de mañana o de tarde, se detecta por la hora de entrada).
- Un sábado al mes, de 10:00 a 13:00 (3 h).
- Los festivos, vacaciones o bajas se marcan como «día libre» y se descuentan de las horas del mes.
- Funciona sin conexión. Cada persona guarda sus datos solo en su propio móvil.

## Publicarla en GitHub Pages (una sola vez)

1. Entra en github.com y crea un repositorio nuevo, por ejemplo `mi-fichaje`. Márcalo como **Public**.
2. Pulsa **Add file → Upload files** y arrastra todo el contenido de esta carpeta: `index.html`, `manifest.json`, `sw.js`, los `.png` y las carpetas `android` y `.github`. Pulsa **Commit changes**.
3. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`. Pulsa **Save**.
4. En un par de minutos la app estará en `https://TU-USUARIO.github.io/mi-fichaje/`.

Ese enlace es el que compartes con tus compañeros.

Al subir los archivos, sube también las carpetas `android` y `.github`. Si arrastras desde el explorador, la carpeta `.github` puede quedar oculta: en Windows activa **Vista → Elementos ocultos** antes de arrastrar. Otra opción es crearla en GitHub con **Add file → Create new file**, escribir `.github/workflows/apk.yml` como nombre y pegar dentro el contenido del archivo.

## El APK (app para Android)

Cada vez que subes cambios al repositorio, GitHub compila el APK por su cuenta. Tarda unos 3 o 4 minutos.

1. En el repositorio, entra en la pestaña **Actions**. Verás «Compilar APK» en marcha; cuando acabe, aparece con un tic verde.
2. Ve a la página principal del repositorio y, a la derecha, pulsa **Releases**. Dentro está `MiFichaje.apk`, listo para descargar.
3. Para instalarlo, ábrelo en el móvil. Android pedirá permiso para «instalar apps desconocidas» desde el navegador o desde WhatsApp: acéptalo solo para esto. Si Play Protect avisa de que la app no es conocida, pulsa **Instalar de todos modos**.

El APK se puede pasar a los compañeros por WhatsApp o con el enlace de Releases. Cuando subas una versión nueva, se instala encima de la anterior y los fichajes se conservan.

Si la compilación falla (aparece una cruz roja en Actions), abre la ejecución, copia el error y pásaselo a Claude.

> La clave de firma (`android/app/fichaje.jks`) está dentro del repositorio para que todas las versiones se firmen igual. Para una app personal como esta no es un problema, pero no reutilices esa clave para otras apps.

## Instalarla en el móvil (versión web)

**Android (Chrome):** abre el enlace y pulsa el botón **Instalar** que aparece arriba en la app. Si no sale, abre el menú ⋮ y elige **Instalar aplicación** o **Añadir a pantalla de inicio**.

**iPhone (Safari):** abre el enlace, pulsa el botón Compartir y elige **Añadir a pantalla de inicio**.

Una vez instalada se abre como cualquier otra app, con su icono y sin la barra del navegador.

## Copias de seguridad

Los datos viven en el móvil. Si se borran los datos del navegador o se desinstala la app, se pierden. Usa **Guardar copia** de vez en cuando y guarda el archivo en Drive o similar. Con **Restaurar copia** se recuperan en el mismo móvil o en uno nuevo.

**Exportar mes a Excel (CSV)** genera una tabla con cada día, el tiempo trabajado y la diferencia en minutos.

## Actualizar la app

Sube los archivos nuevos al mismo repositorio. Los móviles reciben la versión nueva la próxima vez que abran la app con conexión. Los datos de cada persona no se tocan.
