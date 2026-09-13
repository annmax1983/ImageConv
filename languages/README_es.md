# ImageConv

[English](../README.md) | [中文](README_zh.md) | Español | [Deutsch](README_de.md) | [日本語](README_ja.md) | [Français](README_fr.md)

Una extensión ligera para el navegador que convierte imágenes entre los formatos PNG, JPG, WEBP y AVIF — todo localmente, sin subir datos a ningún servidor.

> Basada en Chromium · Manifest V3 · Sin rastreo · Procesamiento completo en el navegador

---

## ¿Por qué ImageConv?

La mayoría de herramientas de conversión de imágenes requieren subir tus archivos a un servidor remoto. ImageConv hace todo dentro de tu navegador usando la Canvas API — tus datos nunca salen de tu máquina.

| Ventaja | Detalle |
|---------|--------|
| 🔒 **Privacidad ante todo** | Todo el procesamiento ocurre en la memoria de tu navegador. Sin servidores, sin subidas, sin rastreo. |
| ⚡ **Conversión instantánea** | Imágenes de hasta 5 MB se convierten en menos de 500 ms. Sin esperas de ida y vuelta al servidor. |
| 🎯 **Cero dependencias** | Construida con JavaScript vanilla y APIs nativas de Chrome. Sin frameworks, sin peso muerto. |
| 🌍 **6 idiomas** | Detecta automáticamente el idioma de tu navegador: inglés, español, alemán, japonés, francés y chino. |
| 📋 **Copiar y guardar** | Clic derecho en cualquier imagen para guardarla como archivo o copiarla directamente al portapapeles. |
| 📁 **Arrastrar y soltar** | Arrastra imágenes locales al popup para una conversión rápida. |

---

## Funcionalidades

### Funcionalidades gratuitas

| Funcionalidad | Descripción |
|---------|-------------|
| 🖼️ **Conversión por clic derecho** | Convierte cualquier imagen de una página web a PNG, JPG, WEBP o AVIF desde el menú contextual |
| 📱 **Soporte HEIC/HEIF** | Convierte fotos de iPhone directamente — arrastrar y soltar, pegar o clic derecho. Decodificación local mediante decodificador WASM integrado |
| 📐 **Redimensionar** | Escala por porcentaje o dimensiones exactas en píxeles (deja un campo vacío para mantener la proporción). Aplica a conversiones del popup y del clic derecho |
| 📋 **Copiar al portapapeles** | Clic derecho → Copiar como PNG/JPG/WEBP/AVIF — pega en correos, chats o documentos |
| 📊 **Comparación de tamaño** | Notificación emergente que muestra el tamaño original vs. el convertido con el porcentaje de ahorro (basado en tamaños reales) |
| 🎚️ **Ajuste de calidad** | Ajusta fino la calidad de exportación para JPG, WEBP y AVIF con controles deslizantes en el popup |
| 🔗 **Limpieza inteligente de enlaces** | Elimina parámetros de rastreo de CDN para obtener las imágenes originales |
| 🌐 **Soporte cross-origin** | Obtiene imágenes de cualquier sitio web a través del Service Worker |
| 🔤 **i18n en 6 idiomas** | El menú contextual y la interfaz se adaptan automáticamente al idioma de tu navegador |
| 🛡️ **Relleno blanco para JPG** | Rellena automáticamente los fondos transparentes con blanco al convertir PNG → JPG |
| ⏱️ **Protección contra duplicados** | Ignora clics repetidos sobre la misma imagen en un intervalo de 2 segundos |

### Funcionalidades Premium (requieren licencia)

| Funcionalidad | Descripción |
|---------|-------------|
| ⭐ **Conversión por arrastrar y soltar** | Arrastra o pega (Ctrl+V) imágenes locales al popup para una conversión rápida |
| 📁 **Conversión local por lotes** | Convierte varios archivos locales de una sola vez |

---

## Gratis vs Premium

| | Gratis | Premium |
|---|:---:|:---:|
| Conversión de imágenes web por clic derecho | ✅ | ✅ |
| Copiar al portapapeles | ✅ | ✅ |
| Ajuste de calidad | ✅ | ✅ |
| Entrada HEIC/HEIF | ✅ | ✅ |
| Redimensionar | ✅ | ✅ |
| Obtención de imágenes cross-origin | ✅ | ✅ |
| Conversión local por arrastrar y soltar | — | ✅ |
| Conversión local por lotes | — | ✅ |

---

## Vista previa

<!-- Reemplazar con capturas de pantalla reales -->
<p align="center">
  <img src="screenshots/popup.png" alt="ImageConv Popup" width="360">
</p>

<p align="center">
  <img src="screenshots/context-menu.png" alt="Menú contextual de ImageConv">
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
3. Elige **Guardar como** o **Copiar como**
4. Selecciona tu formato: PNG, JPG, WEBP o AVIF
5. Listo — el archivo se descarga al instante, o la imagen se copia al portapapeles

### Arrastrar y soltar (Premium)

> ⚠️ Arrastrar y soltar es una funcionalidad premium. Se requiere una clave de licencia.

1. Haz clic en el icono de ImageConv en tu barra de herramientas para abrir el popup
2. Haz clic en el botón 🔑 en la esquina superior derecha para introducir tu clave de licencia
3. Una vez activada, arrastra un archivo de imagen local a la zona de soltar
4. Selecciona el formato de destino
5. El archivo convertido se descarga automáticamente

Puedes adquirir una clave de licencia en [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv).

### Ajustes de calidad

Abre el popup para ajustar la calidad de exportación de JPG, WEBP y AVIF con los controles deslizantes. PNG siempre es sin pérdida. Los ajustes se guardan automáticamente.

### Redimensionar

La sección **Redimensionar** del popup permite escalar por porcentaje (5 %–200 %) o definir dimensiones exactas en píxeles. Deja un campo vacío para mantener la proporción. El ajuste se aplica tanto a la conversión por arrastrar y soltar como al clic derecho; por defecto se mantiene el tamaño original.

### HEIC/HEIF (fotos de iPhone)

Arrastra archivos `.heic` / `.heif` al popup (o convierte un enlace de imagen HEIC en cualquier página web) para guardarlos como PNG/JPG/WEBP. La decodificación ocurre completamente en local mediante WASM — nada se sube a ningún servidor.

---

## Estructura del menú contextual

```
ImageConv
├── Guardar como PNG (Sin pérdida)
├── Guardar como JPG (Alta calidad)
├── Guardar como WEBP (Compacto)
├── Guardar como AVIF (Mejor compresión)
├── Copiar como PNG (Sin pérdida)
├── Copiar como JPG (Alta calidad)
├── Copiar como WEBP (Compacto)
└── Copiar como AVIF (Mejor compresión)
```

Los menús **Copiar como** y **Guardar como** solo aparecen al hacer clic derecho sobre imágenes o enlaces que apuntan a archivos de imagen (`.png`, `.jpg`, `.jpeg`, `.webp`, `.avif`, `.gif`, `.bmp`, `.jfif`, `.svg`).

---

## Privacidad

ImageConv está construida con la privacidad como principio fundamental:

- ✅ **Cero subida de datos** — Todo el procesamiento de imágenes ocurre en la memoria de tu navegador
- ✅ **Sin analíticas** — Sin rastreo, sin telemetría, sin llamadas remotas
- ✅ **Sin cookies** — Sin lectura ni escritura de cookies del navegador
- ✅ **Sin historial de navegación** — Sin acceso a tus datos de navegación
- ✅ **Solo memoria temporal** — Las imágenes existen en memoria durante la conversión y se destruyen inmediatamente después
- ✅ **Permisos mínimos** — Solo solicita lo estrictamente necesario: `contextMenus`, `downloads`, `offscreen`, `storage`, `clipboardWrite`

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

ImageConv utiliza un sistema de licencia basado en dispositivo:

1. **Compra** una clave de licencia en [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activa** haciendo clic en el botón 🔑 del popup e introduciendo tu clave
3. La clave se vincula a tu dispositivo (huella de hardware) — una clave, un dispositivo
4. La licencia se valida online cada 24 horas; funciona sin conexión hasta 7 días

### Qué es gratis vs de pago

| Funcionalidad | Gratis | Premium |
|---------|:----:|:-------:|
| Conversión de imágenes web por clic derecho | ✅ | ✅ |
| Guardar como PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copiar al portapapeles | ✅ | ✅ |
| Controles deslizantes de ajuste de calidad | ✅ | ✅ |
| Entrada HEIC/HEIF (decodificación WASM) | ✅ | ✅ |
| Redimensionar (porcentaje / píxeles exactos) | ✅ | ✅ |
| Obtención de imágenes cross-origin | ✅ | ✅ |
| Limpieza inteligente de enlaces | ✅ | ✅ |
| Conversión local de archivos por arrastrar y soltar | ❌ | ✅ |
| Conversión local de archivos por lotes | ❌ | ✅ |

**Resumen**: Todas las funcionalidades de imágenes web (guardar/copiar por clic derecho) son **gratuitas**. La conversión de archivos locales (arrastrar y soltar) requiere una **licencia premium**.

---

## ❤️ Apoyo

Si te resulta útil ImageConv, ¡considera apoyar el proyecto!

**[👉 Apoyar en Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Sitio web oficial](https://www.annmax1983.com/extensions/imageconv)**
