# Lyrics

**Español** · [English](#english)

Lyrics muestra en una ventana flotante, sobre cualquier programa, la letra sincronizada de la canción que suena en **YouTube Music** (Chrome). Es gratuita y funciona en **Windows 10/11 (64 bits)**.

Consta de dos piezas que se instalan una sola vez:

1. **App de escritorio**: la ventana con las letras.
2. **Extensión de Chrome**: le indica a la app qué canción suena.

## Descargar

Abre [Releases](https://github.com/ElnarDev/Lyrics-Releases/releases/latest), elige la versión más reciente y, en **Assets**, descarga:

- `Lyrics-Setup-<versión>-x64.exe`: instalador de la app.
- `Lyrics-Extension-<versión>.zip`: la extensión.

Si alguien te los envió directamente, usa esos archivos.

## 1. Instalar la app de escritorio

1. Haz doble clic en `Lyrics-Setup-<versión>-x64.exe`.
2. Windows puede mostrar «Windows protegió su PC», porque el instalador aún no tiene firma digital. Pulsa **Más información** y luego **Ejecutar de todas formas**.
3. Sigue el asistente. No requiere permisos de administrador.
4. Lyrics se abre y aparece su icono en la bandeja de Windows, junto al reloj. Si no lo ves, pulsa la flecha **^** de la barra de tareas.

Para abrirla en otro momento, búscala como **Lyrics** en el menú Inicio.

## 2. Instalar la extensión en Chrome

1. Haz clic derecho en `Lyrics-Extension-<versión>.zip` → **Extraer todo…** y guarda la carpeta en un lugar fijo, por ejemplo `Documentos\Lyrics-Extension`. **No la borres**: Chrome la usa mientras la extensión esté instalada.
2. En Chrome, escribe `chrome://extensions` en la barra de direcciones.
3. Activa **Modo de desarrollador** (arriba a la derecha).
4. Pulsa **Cargar descomprimida** y selecciona la carpeta extraída, la que contiene `manifest.json`.
5. Fija la extensión: pulsa el icono de la pieza de rompecabezas de Chrome y luego el alfiler junto a **Lyrics**.

## 3. Vincular la app y la extensión

Solo hay que hacerlo una vez:

1. Haz clic derecho en el icono de Lyrics de la bandeja → **Copiar clave de vinculación**.
2. En Chrome, pulsa el icono de la extensión Lyrics, pega la clave y pulsa **Guardar clave**.
3. El popup debe indicar que la conexión está activa.

## 4. Usarla

Abre [music.youtube.com](https://music.youtube.com) en Chrome (si ya estaba abierto, recarga la pestaña) y reproduce una canción. La letra aparece en la ventana de Lyrics y resalta la línea que suena.

Pasa el ratón por la ventana para ver los controles:

| Control | Para qué sirve |
| --- | --- |
| **Ventana** | Transparencia del fondo. |
| **Letras** | Transparencia del texto. |
| **− / +** | Reduce o aumenta el tamaño del texto de 1 en 1 (12–48 px). |
| **0 s** (desfase) | Si la letra se adelanta o se atrasa: clic izquierdo adelanta 0,5 s, clic derecho atrasa 0,5 s y Mayús + clic la restablece. |
| **×** | Oculta la ventana; vuelve con **Mostrar Lyrics** en la bandeja. |

Arrastra la ventana para moverla y sus bordes laterales para cambiar el ancho.

Atajos y menú de la bandeja (clic derecho en el icono):

- **Modo compacto** (`Ctrl+Alt+C`): muestra solo la línea actual.
- **Reintentar letras** (`Ctrl+Alt+X`): vuelve a buscar la letra de la canción actual.
- **Restablecer apariencia**: recupera el tamaño de texto y las transparencias predeterminados y muestra la ventana.
- **Salir**: cierra Lyrics del todo.

## ¿Qué versión tengo?

- App: menú de la bandeja → línea **Versión**, por ejemplo `Versión 0.1.0 (c27e6ae)`.
- Extensión: parte inferior del popup.

El número es la versión y lo que va entre paréntesis identifica el build exacto. Para comprobar si tienes la misma que otra persona, comparad esa línea completa. La app y la extensión deberían mostrar la misma.

## Actualizar

1. Descarga los archivos de la nueva versión.
2. Cierra Lyrics (bandeja → **Salir**) y ejecuta el nuevo instalador. Tus preferencias y la vinculación deberían conservarse; si el popup pide la clave, repite el paso 3.
3. Extrae el nuevo ZIP **en la misma carpeta**, reemplazando los archivos, y pulsa el botón de recarga ↻ de Lyrics en `chrome://extensions`. Recarga YouTube Music.

## Comprobar la descarga (opcional)

Cada versión incluye `SHA256SUMS.txt` con la «huella» de cada archivo. Sirve para confirmar que la descarga está completa y no fue modificada; **no** indica si es la versión más reciente. En PowerShell:

```powershell
Get-FileHash .\Lyrics-Setup-0.1.0-x64.exe -Algorithm SHA256
```

El valor debe coincidir (sin distinguir mayúsculas) con el de `SHA256SUMS.txt`.

## Problemas frecuentes

| Problema | Solución |
| --- | --- |
| «No se encontraron letras para esta canción» o «Hay letra, pero no una versión sincronizada» | Esa canción no está en LRCLIB o no tiene letra sincronizada. YouTube Music usa otros proveedores con licencia, así que puede mostrarla aunque Lyrics no. Puedes aportarla en [lrclib.net](https://lrclib.net). |
| «LRCLIB está limitando las solicitudes» o «No se pudo conectar con LRCLIB» | Espera unos minutos y pulsa `Ctrl+Alt+X`. Las letras ya encontradas se guardan en tu equipo y no vuelven a descargarse. |
| El popup no conecta | Comprueba que Lyrics esté abierta (icono en la bandeja), vuelve a copiar la clave y pégala con **Cambiar vinculación**. |
| La ventana no reacciona a la música | Recarga la pestaña de YouTube Music. |
| Chrome muestra «Could not load javascript» | Seleccionaste una carpeta equivocada; elige la que contiene `manifest.json`. |
| No veo la ventana | Bandeja → **Mostrar Lyrics**. |

Para informar de un fallo: bandeja → **Copiar diagnóstico** y pega el texto en tu mensaje. No incluye canciones, letras ni tu clave.

## Créditos

Las letras las proporciona [LRCLIB](https://lrclib.net), un servicio comunitario y gratuito. Lyrics es gratuita y no está afiliada a YouTube ni a Google.

---

## English

Lyrics shows the synced lyrics of the song playing in **YouTube Music** (Chrome) in a floating window on top of any program. It is free and runs on **Windows 10/11 (64-bit)**. The interface is in Spanish.

It has two parts, installed once:

1. **Desktop app**: the lyrics window.
2. **Chrome extension**: tells the app which song is playing.

### Download

Open [Releases](https://github.com/ElnarDev/Lyrics-Releases/releases/latest), pick the latest version and, under **Assets**, download `Lyrics-Setup-<version>-x64.exe` (app installer) and `Lyrics-Extension-<version>.zip` (extension).

### 1. Install the desktop app

1. Double-click `Lyrics-Setup-<version>-x64.exe`.
2. Windows may show "Windows protected your PC" because the installer is not digitally signed yet. Click **More info** → **Run anyway**.
3. Follow the wizard (no administrator rights required).
4. Lyrics opens and its icon appears in the system tray next to the clock (click the **^** arrow if hidden). Later, open it from the Start menu as **Lyrics**.

### 2. Install the Chrome extension

1. Right-click the ZIP → **Extract All…** and keep the folder in a permanent place, e.g. `Documents\Lyrics-Extension`. **Don't delete it**; Chrome uses it.
2. Go to `chrome://extensions` and turn on **Developer mode** (top right).
3. Click **Load unpacked** and select the extracted folder (the one containing `manifest.json`).
4. Pin it from Chrome's puzzle-piece menu.

### 3. Link the app and the extension (once)

1. Right-click the Lyrics tray icon → **Copiar clave de vinculación** (Copy pairing key).
2. Click the Lyrics extension icon, paste the key and click **Guardar clave** (Save key).

### 4. Use it

Open [music.youtube.com](https://music.youtube.com) (reload it if it was already open) and play a song. Hover over the window to show the controls:

- **Ventana / Letras**: background and text transparency.
- **− / +**: text size, 1 px at a time (12–48 px).
- **0 s** (offset): left-click +0.5 s, right-click −0.5 s, Shift+click resets.
- **×**: hides the window (tray → **Mostrar Lyrics** brings it back).
- `Ctrl+Alt+C`: compact mode (current line only). `Ctrl+Alt+X`: retry lyrics.
- Tray → **Restablecer apariencia** resets text size and transparency; **Salir** quits.

### Which version do I have?

Tray menu → **Versión** line (e.g. `Versión 0.1.0 (c27e6ae)`), and the bottom of the extension popup. The text in parentheses identifies the exact build; compare the full line with other people. App and extension should match.

### Updating

Quit Lyrics (tray → **Salir**), run the new installer (settings and pairing should be kept; if the popup asks for the key, repeat step 3), extract the new ZIP **over the same folder**, click reload ↻ on Lyrics in `chrome://extensions`, then reload YouTube Music.

### Verifying the download (optional)

`SHA256SUMS.txt` lists each file's fingerprint. It confirms the download is complete and unmodified; it does **not** tell you whether it is the latest version. Run `Get-FileHash .\<file> -Algorithm SHA256` in PowerShell and compare.

### Troubleshooting

- **"No se encontraron letras…"** (no lyrics found): the song is not on LRCLIB or has no synced lyrics. YouTube Music uses other licensed providers, so it may show lyrics that Lyrics can't. You can contribute them at [lrclib.net](https://lrclib.net).
- **"LRCLIB está limitando las solicitudes"** (rate-limited) or connection errors: wait a few minutes and press `Ctrl+Alt+X`. Lyrics already found are stored on your PC.
- **Popup doesn't connect**: make sure Lyrics is running, copy the key again and paste it via **Cambiar vinculación**.
- **"Could not load javascript"**: select the folder that contains `manifest.json`.
- To report a bug: tray → **Copiar diagnóstico** and paste the text. It contains no songs, lyrics or keys.

### Credits

Lyrics are provided by [LRCLIB](https://lrclib.net), a free community service. Lyrics is free and not affiliated with YouTube or Google.
