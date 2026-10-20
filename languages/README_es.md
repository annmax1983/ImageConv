# ImageConv

[English](../README.md) | [中文](README_zh.md) | Español | [Deutsch](README_de.md) | [日本語](README_ja.md) | [Français](README_fr.md)

Una extensión ligera para el navegador que convierte imágenes entre los formatos PNG, JPG, WEBP y AVIF — todo localmente, sin subir datos a ningún servidor.

> Basada en Chromium · Manifest V3 · Sin rastreo · Procesamiento completo en el navegador

---

## ¿Por qué ImageConv?

La mayoría de herramientas de conversión de imágenes requieren subir tus archivos a un servidor remoto. ImageConv hace todo dentro de tu navegador usando la Canvas API — tus imágenes nunca salen de tu navegador.

| Ventaja | Detalle |
|---------|--------|
| 🔒 **Privacidad ante todo** | Todo el procesamiento ocurre en la memoria de tu navegador. Sin subidas, sin rastreo. La única petición saliente es la validación opcional de la licencia. |
| ⚡ **Conversión instantánea** | Imágenes de hasta 5 MB se convierten en menos de 500 ms. Sin esperas de ida y vuelta al servidor. |
| 🎯 **Cero dependencias** | Construida con JavaScript vanilla y APIs nativas de Chrome. Sin frameworks, sin peso muerto. |
| 🌍 **6 idiomas** | Detecta automáticamente el idioma de tu navegador: inglés, español, alemán, japonés, francés y chino. |
| 📋 **Copiar y guardar** | Clic derecho en cualquier imagen para guardarla como archivo o copiarla directamente al portapapeles. |
| 📁 **Arrastrar y soltar** | Arrastra imágenes locales al popup para una conversión rápida. |
| 🖼️ **Exportación por lotes** | Lista todas las imágenes ya cargadas de una página, elige las que quieras y expórtalas de una vez. |

---

## Funcionalidades

### Funcionalidades gratuitas

| Funcionalidad | Descripción |
|---------|-------------|
| 🖼️ **Conversión por clic derecho** | Convierte cualquier imagen de una página web a PNG, JPG, WEBP o AVIF desde el menú contextual |
| 📱 **Soporte HEIC/HEIF** | Convierte fotos de iPhone directamente — arrastrar y soltar, pegar o clic derecho. Decodificación local mediante decodificador WASM integrado |
| 📐 **Redimensionar** | Escala por porcentaje o dimensiones exactas en píxeles (deja un campo vacío para mantener la proporción). Aplica a conversiones del popup y del clic derecho |
| 📋 **Copiar al portapapeles** | Clic derecho → Copiar como PNG — pega en correos, chats o documentos |
| 📊 **Comparación de tamaño** | Notificación emergente que muestra el tamaño original vs. el convertido con el porcentaje de ahorro (basado en tamaños reales) |
| 🎚️ **Ajuste de calidad** | Ajusta fino la calidad de exportación para JPG, WEBP y AVIF con controles deslizantes en el popup |
| 🔗 **Limpieza inteligente de enlaces** | Elimina parámetros de rastreo de CDN para obtener las imágenes originales |
| 🌐 **Soporte cross-origin** | Obtiene imágenes de cualquier sitio web a través del Service Worker |
| 🔤 **i18n en 6 idiomas** | El menú contextual y la interfaz se adaptan automáticamente al idioma de tu navegador |
| 🛡️ **Relleno blanco para JPG** | Rellena automáticamente los fondos transparentes con blanco al convertir PNG → JPG |
| ⏱️ **Protección contra duplicados** | Ignora clics repetidos sobre la misma imagen en un intervalo de 2 segundos |

### Funcionalidades Pro (requieren licencia)

| Funcionalidad | Descripción |
|---------|-------------|
| ♾️ **Conversión local por lotes ilimitada** | Los lotes gratuitos con varios archivos convierten hasta 5 archivos por ejecución; Pro elimina el límite local |
| 📦 **Exportaciones web grandes** | Exporta hasta 100 imágenes de una página en una sola ejecución (gratis: 5) |
| 🗜️ **Exportación en archivo ZIP** | Empaqueta un lote web en un único archivo `.zip`. Si el empaquetado falla o el archivo supera 4 GB, las imágenes completadas se guardan por separado |
| 🗂️ **Presets de lote** | Guarda hasta 12 presets de formato/calidad/redimensionado en el diálogo Opciones del lote y reaplícalos con un clic |
| 🏷️ **Plantillas de nombre de archivo** | Nombra las descargas web por lotes con `{name}`, `{index}`, `{format}`, `{date}`, `{width}` y `{height}`. La extensión se añade automáticamente y las colisiones reciben `-2`, `-3` |

La edición de formato, calidad y redimensionado en el diálogo Opciones del lote sigue siendo gratuita. Los presets, la asignación de nombres y la entrega en ZIP son Pro y se aplican a la página de exportación por lotes, no a arrastrar y soltar en el popup.

---

## Gratis vs Pro

| | Gratis | Pro |
|---|:---:|:---:|
| Conversión de imágenes web por clic derecho | ✅ | ✅ |
| Copiar al portapapeles | ✅ Solo PNG | ✅ Solo PNG |
| Ajuste de calidad | ✅ | ✅ |
| Entrada HEIC/HEIF | ✅ | ✅ |
| Redimensionar | ✅ | ✅ |
| Obtención de imágenes cross-origin | ✅ | ✅ |
| Arrastrar y soltar / pegar imágenes locales | ✅ Un solo archivo | ✅ Un solo archivo |
| Conversión local por lotes | Hasta 5 por ejecución | Ilimitada |
| Exportar imágenes de una página web | Hasta 5 por ejecución | Hasta 100 por ejecución |
| Formato / calidad / redimensionado por lotes | ✅ | ✅ |
| Presets de lote | — | ✅ Hasta 12 |
| Plantillas de nombre de archivo (página de lote) | — | ✅ |
| Entrega en archivo ZIP (página de lote) | — | ✅ |

---

## Vista previa

<!-- Reemplazar con capturas de pantalla reales -->
<p align="center">
  <img src="../screenshots/popup.png" alt="ImageConv Popup" width="360">
</p>

<p align="center">
  <img src="../screenshots/context-menu.png" alt="Menú contextual de ImageConv">
</p>

---

## Navegadores compatibles

| Navegador | Estado |
|---------|--------|
| Google Chrome | ✅ Totalmente compatible |
| Microsoft Edge | ✅ Totalmente compatible |
| Brave | ✅ Compatible |
| Opera | ✅ Compatible |
| Vivaldi | ✅ Compatible |
| Cualquier navegador basado en Chromium | ✅ Compatible (Manifest V3) |

---

## Instalación

### Desde código fuente (modo desarrollador)

1. Abre la página de extensiones de tu navegador:
   - **Chrome**: `chrome://extensions/`
   - **Edge**: `edge://extensions/`
2. Activa el **modo de desarrollador** (interruptor arriba a la derecha)
3. Haz clic en **Cargar descomprimida** y selecciona la carpeta `pic-convert`
4. El icono ✨ de ImageConv aparecerá en tu barra de herramientas

---

## Uso

### Conversión por clic derecho

1. Haz clic derecho en cualquier imagen de una página web
2. Selecciona **ImageConv** en el menú contextual
3. Elige **Guardar como** (PNG/JPG/WEBP/AVIF) o **Copiar como PNG**
4. Listo — el archivo se descarga al instante, o la imagen se copia al portapapeles como PNG

### Arrastrar y soltar / Pegar (gratis)

1. Haz clic en el icono de ImageConv en tu barra de herramientas para abrir el popup
2. Arrastra un archivo de imagen local a la zona de soltar, o pégalo con Ctrl+V
3. Selecciona el formato de destino
4. El archivo convertido se descarga automáticamente

Las imágenes sueltas siempre son gratis. En el plan gratis, soltar varios archivos convierte los primeros 5; una licencia Pro elimina ese límite por ejecución. Los presets de lote, las plantillas de nombre y la entrega en ZIP solo están disponibles en la página de exportación por lotes web, no en arrastrar y soltar del popup.

### Exportación por lotes de imágenes web (gratis 5, Pro 100)

1. Abre la página cuyas imágenes quieras exportar (deben estar ya cargadas)
2. Haz clic en el icono de ImageConv y luego en **Exportar imágenes de esta página**
3. Se abre una pestaña nueva con todas las imágenes encontradas, de mayor a menor: marca las que quieras
4. Haz clic en **Opciones** para definir formato, calidad y redimensionado. Todos pueden editarlos; Pro además puede aplicar o guardar un preset, editar la plantilla de nombre y elegir **Un archivo ZIP** en Entrega
5. Haz clic en **Exportar seleccionadas** (el botón pasa a **Exportar ZIP** cuando la entrega en ZIP está activa)

Los archivos individuales se descargan en `ImageConv/` con la plantilla de nombre. Las ejecuciones ZIP descargan un `ImageConv/<host>-YYYYMMDD-HHmm.zip`; si el empaquetado falla o el archivo supera 4 GB, las imágenes completadas se guardan por separado.

Las imágenes de menos de 100 px se ocultan por defecto (iconos, avatares, píxeles de seguimiento); ajusta el filtro en la barra superior. El plan gratis exporta hasta 5 imágenes por ejecución; Pro eleva el límite a 100.

### Ajustes de calidad

Abre el popup para ajustar la calidad de exportación de JPG, WEBP y AVIF con los controles deslizantes. PNG siempre es sin pérdida. Los ajustes se guardan automáticamente.

### Redimensionar

La sección **Redimensionar** del popup permite escalar por porcentaje (5 %–200 %) o definir dimensiones exactas en píxeles. Deja un campo vacío para mantener la proporción. El ajuste se aplica tanto a la conversión por arrastrar y soltar como al clic derecho; por defecto se mantiene el tamaño original.

### HEIC/HEIF (fotos de iPhone)

Arrastra o pega archivos `.heic` / `.heif` en el popup, o haz clic derecho sobre una imagen HEIC mostrada en una página, para guardarla como PNG/JPG/WEBP. La decodificación ocurre completamente en local mediante WASM — nada se sube a ningún servidor. La entrada HEIC es gratis en todos los planes.

---

## Estructura del menú contextual

```
ImageConv
├── Guardar como PNG (Sin pérdida)
├── Guardar como JPG (Alta calidad)
├── Guardar como WEBP (Compacto)
├── Guardar como AVIF (Mejor compresión)
└── Copiar como PNG (Sin pérdida)
```

Los menús **Guardar como** y **Copiar como PNG** solo aparecen al hacer clic derecho sobre una imagen, incluida una imagen dentro de un enlace. Los enlaces simples a archivos de imagen no muestran el menú. La salida al portapapeles es solo PNG.

---

## Privacidad

ImageConv está construida con la privacidad como principio fundamental:

- ✅ **Cero subida de datos** — Todo el procesamiento de imágenes ocurre en la memoria de tu navegador
- ✅ **Sin analíticas** — Sin rastreo ni telemetría. La única solicitud saliente es la validación de licencia (clave de licencia + un identificador de instalación aleatorio) al activar o cuando caduca la comprobación en caché de 2 h — los datos de imagen nunca se transmiten
- ✅ **Sin cookies** — Sin lectura ni escritura de cookies del navegador
- ✅ **Sin historial de navegación** — Sin acceso a tus datos de navegación
- ✅ **Solo memoria temporal** — Las imágenes existen en memoria durante la conversión y se destruyen inmediatamente después
- ✅ **Permisos mínimos** — Solo lo que necesita cada función: `contextMenus`, `downloads`, `offscreen`, `storage`, `scripting`, `clipboardWrite`, más `<all_urls>` para obtener la imagen en la que hiciste clic y escanear una página para la exportación por lotes

---

## Cómo funciona

```
Clic derecho en imagen
       ↓
El Service Worker obtiene el blob de la imagen (gestiona cross-origin)
       ↓
Envía el blob al Offscreen Document (DOM oculto con acceso a Canvas)
       ↓
Canvas dibuja la imagen a resolución nativa
       ↓
Exporta como formato de destino con la calidad especificada
       ↓
Devuelve la URL de datos → lanza la descarga o copia al portapapeles
       ↓
Destruye todos los recursos temporales (blob, canvas, elemento de imagen)
```

> **¿Por qué Offscreen?** El Manifest V3 de Chrome ejecuta el fondo como un Service Worker, que no tiene acceso al DOM. La Canvas API requiere un DOM, así que usamos la Offscreen API de Chrome para crear un documento oculto para el procesamiento de imágenes.

---

## Valores predeterminados de calidad de exportación

| Formato | Calidad | Notas |
|--------|---------|-------|
| PNG | Sin pérdida | Sin ajuste de calidad — siempre preserva la máxima calidad y transparencia |
| JPG | 92 | Alta calidad, buen equilibrio entre tamaño y nitidez |
| WEBP | 90 | Formato moderno, ~25-35% más pequeño que JPG con calidad equivalente |
| AVIF | 70 | Formato de última generación, ~20-30% más pequeño que WEBP, ideal para web |

Todos los valores de calidad son ajustables mediante controles deslizantes en el popup (rango: 10–100).

> ℹ️ AVIF se genera mediante un codificador WASM integrado (el Canvas de Chromium no puede codificar AVIF de forma nativa). Las imágenes demasiado grandes (más de 25 megapíxeles) se convierten automáticamente a WEBP con un aviso.

---

## Aviso de derechos de autor

Esta extensión solo proporciona capacidades locales de conversión de formato de imagen para el procesamiento personal y sin conexión de los usuarios. Todas las imágenes, fotos y recursos gráficos de las páginas web pertenecen al propietario original de los derechos de autor. Los usuarios no deberían utilizar las imágenes convertidas para reproducción comercial, distribución no autorizada, creación derivada u otros actos que infrinjan los derechos de autor. Toda responsabilidad legal derivada del uso indebido recaerá exclusivamente sobre el usuario.

## Recordatorio sobre imágenes cross-origin

La función de obtención de imágenes cross-origin se utiliza únicamente para obtener recursos de imagen para la conversión de formato local. Está prohibido usar esta función para extraer masivamente recursos de imagen de sitios web, lo cual podría violar las reglas de acceso del sitio.

---

## Aviso sobre el código fuente

> ⚠️ **Este repositorio no publica código fuente.** Contiene únicamente documentación de uso, notas de lanzamiento y recursos de soporte. La extensión se distribuye exclusivamente a través de Chrome Web Store. No se proporcionan paquetes de instalación sin conexión ni código fuente para usuarios finales.

---

## Licencia

Copyright © 2026 ImageConv. Todos los derechos reservados.

### Cómo funciona la licencia

ImageConv utiliza un sistema de licencia basado en activaciones:

1. **Compra** una clave de licencia en [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activa** haciendo clic en el botón 🔑 del popup e introduciendo tu clave
3. Cada activación cubre una instalación de navegador; desactiva una instalación antigua en el popup para liberar un espacio para una nueva
4. La licencia se valida online cada 2 horas; si no se puede alcanzar el servidor, la licencia en caché sigue funcionando

### Qué es gratis vs de pago

| Funcionalidad | Gratis | Pro |
|---------|:----:|:---:|
| Conversión de imágenes web por clic derecho | ✅ | ✅ |
| Guardar como PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copiar al portapapeles | ✅ Solo PNG | ✅ Solo PNG |
| Controles deslizantes de ajuste de calidad | ✅ | ✅ |
| Entrada HEIC/HEIF (decodificación WASM) | ✅ | ✅ |
| Redimensionar (porcentaje / píxeles exactos) | ✅ | ✅ |
| Obtención de imágenes cross-origin | ✅ | ✅ |
| Limpieza inteligente de enlaces | ✅ | ✅ |
| Arrastrar y soltar / pegar archivos locales | ✅ Un solo archivo | ✅ Un solo archivo |
| Conversión local de archivos por lotes | Hasta 5 por ejecución | Ilimitada |
| Exportar imágenes de una página web | Hasta 5 por ejecución | Hasta 100 por ejecución |
| Formato / calidad / redimensionado por lotes | ✅ | ✅ |
| Presets de lote | — | ✅ Hasta 12 |
| Plantillas de nombre de archivo (página de lote) | — | ✅ |
| Entrega en archivo ZIP (página de lote) | — | ✅ |

**Resumen**: La conversión por clic derecho, arrastrar y soltar o pegar una sola imagen, hasta 5 imágenes por ejecución por lotes y la edición de formato/calidad/redimensionado en el diálogo Opciones del lote son **gratis**. Una **licencia Pro** elimina el límite local por lotes (hasta 100 imágenes web por ejecución) y desbloquea presets de lote, plantillas de nombre y entrega en ZIP.

---

## ❤️ Apoyo

Si te resulta útil ImageConv, ¡considera apoyar el proyecto!

**[👉 Apoyar en Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Sitio web oficial](https://www.annmax1983.com/extensions/imageconv)**
