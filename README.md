# ImageConv

English | [中文](languages/README_zh.md) | [Español](languages/README_es.md) | [Deutsch](languages/README_de.md) | [日本語](languages/README_ja.md) | [Français](languages/README_fr.md)

A lightweight browser extension that converts images between PNG, JPG, WEBP, and AVIF formats — entirely locally, with zero data upload.

> Chromium-based · Manifest V3 · No tracking · Fully In-Browser Processing

---

## Why ImageConv?

Most image conversion tools require uploading your files to a remote server. ImageConv does everything inside your browser using the Canvas API — no data ever leaves your machine.

| Advantage | Detail |
|-----------|--------|
| 🔒 **Privacy-First** | All processing happens in your browser's memory. No servers, no uploads, no tracking. |
| ⚡ **Instant Conversion** | Images ≤5MB convert in under 500ms. No waiting for server round-trips. |
| 🎯 **Zero Dependencies** | Built with vanilla JavaScript and native Chrome APIs. No frameworks, no bloat. |
| 🌍 **6 Languages** | Auto-detects your browser language — English, Spanish, German, Japanese, French, Chinese. |
| 📋 **Copy & Save** | Right-click any image to save as a file OR copy directly to your clipboard. |
| 📁 **Drag & Drop** | Drop local images onto the popup for quick conversion. |

---

## Features

### Free Features

| Feature | Description |
|---------|-------------|
| 🖼️ **Right-Click Conversion** | Convert any webpage image to PNG, JPG, WEBP, or AVIF via context menu |
| 📋 **Copy to Clipboard** | Right-click → Copy as PNG/JPG/WEBP/AVIF — paste into emails, chats, documents |
| 📊 **File Size Comparison** | Toast notification shows original vs converted size with savings percentage |
| 🎚️ **Adjustable Quality** | Fine-tune export quality for JPG, WEBP, and AVIF via sliders in the popup |
| 🔗 **Smart Link Cleaning** | Strips CDN tracking parameters to fetch original images |
| 🌐 **Cross-Origin Support** | Fetches images from any website via Service Worker |
| 🔤 **6-Language i18n** | Context menu and UI auto-match your browser language |
| 🛡️ **JPG White Fill** | Automatically fills transparent backgrounds with white when converting PNG → JPG |
| ⏱️ **Duplicate Guard** | Ignores repeated clicks on the same image within 2 seconds |

### Premium Features (License Required)

| Feature | Description |
|---------|-------------|
| ⭐ **Drag & Drop Conversion** | Drop local image files onto the popup for quick format conversion |
| 📁 **Batch Local Conversion** | Convert multiple local files at once |

---

## Free vs Premium

| | Free | Premium |
|---|:---:|:---:|
| Right-click image conversion | ✅ | ✅ |
| Copy to clipboard | ✅ | ✅ |
| Quality adjustment | ✅ | ✅ |
| Cross-origin image fetch | ✅ | ✅ |
| Drag & Drop local conversion | — | ✅ |
| Batch local file conversion | — | ✅ |

---

## Preview

<!-- Replace with actual screenshots -->
<p align="center">
  <img src="screenshots/popup.png" alt="ImageConv Popup" width="360">
</p>

<p align="center">
  <img src="screenshots/context-menu.png" alt="ImageConv Context Menu">
</p>

---

## Supported Browsers

| Browser | Status |
|---------|--------|
| Google Chrome | ✅ Fully supported |
| Microsoft Edge | ✅ Fully supported |
| Brave | ✅ Supported |
| Opera | ✅ Supported |
| Vivaldi | ✅ Supported |
| Any Chromium-based browser | ✅ Supported (Manifest V3) |

---

## Installation

### From Source (Developer Mode)

1. Open your browser's extension page:
   - **Chrome**: `chrome://extensions/`
   - **Edge**: `edge://extensions/`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked** and select the `pic-convert` folder
4. The ✨ ImageConv icon will appear in your toolbar

---

## Usage

### Right-Click Conversion

1. Right-click any image on a webpage
2. Select **ImageConv** from the context menu
3. Choose **Save as** or **Copy as**
4. Pick your format: PNG, JPG, WEBP, or AVIF
5. Done — file downloads instantly, or image is copied to clipboard

### Drag & Drop (Premium)

> ⚠️ Drag & Drop is a premium feature. A license key is required.

1. Click the ImageConv icon in your toolbar to open the popup
2. Click the 🔑 button in the top-right corner to enter your license key
3. Once activated, drag a local image file onto the drop zone
4. Select your target format
5. The converted file downloads automatically

You can purchase a license key at [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv).

### Quality Settings

Open the popup to adjust export quality for JPG, WEBP, and AVIF using the sliders. PNG is always lossless. Settings are saved automatically.

---

## Context Menu Structure

```
ImageConv
├── Save as PNG (Lossless)
├── Save as JPG (High Quality)
├── Save as WEBP (Compact)
├── Save as AVIF (Best Compression)
├── Copy as PNG (Lossless)
├── Copy as JPG (High Quality)
├── Copy as WEBP (Compact)
└── Copy as AVIF (Best Compression)
```

The **Copy as** and **Save as** menus only appear when right-clicking on images or links that point to image files (`.png`, `.jpg`, `.jpeg`, `.webp`, `.avif`, `.gif`, `.bmp`, `.jfif`, `.svg`).

---

## Privacy

ImageConv is built with privacy as a core principle:

- ✅ **Zero data upload** — All image processing happens in your browser's memory
- ✅ **No analytics** — No tracking, no telemetry, no remote calls
- ✅ **No cookies** — No reading or writing of browser cookies
- ✅ **No browsing history** — No access to your browsing data
- ✅ **Temporary memory only** — Images exist in memory during conversion and are immediately destroyed after
- ✅ **Minimal permissions** — Only requests what's strictly necessary: `contextMenus`, `downloads`, `offscreen`, `storage`, `clipboardWrite`

---

## How It Works

```
Right-click image
       ↓
Service Worker fetches image blob (handles cross-origin)
       ↓
Sends blob to Offscreen Document (hidden DOM with Canvas access)
       ↓
Canvas draws image at native resolution
       ↓
Exports as target format with specified quality
       ↓
Returns data URL → triggers download or copies to clipboard
       ↓
Destroys all temporary resources (blob, canvas, image element)
```

> **Why Offscreen?** Chrome's Manifest V3 runs the background as a Service Worker, which has no DOM access. The Canvas API requires a DOM, so we use Chrome's Offscreen API to create a hidden document for image processing.

---

## Export Quality Defaults

| Format | Quality | Notes |
|--------|---------|-------|
| PNG | Lossless | No quality setting — always preserves full quality and transparency |
| JPG | 92 | High quality, good balance between size and clarity |
| WEBP | 90 | Modern format, ~25-35% smaller than JPG at equivalent quality |
| AVIF | 70 | Next-gen format, ~20-30% smaller than WEBP, best for web delivery |

All quality values are adjustable via sliders in the popup (range: 10–100).

---

## Copyright Disclaimer

This extension only provides local image format conversion capabilities for users' personal offline processing. All pictures, photos and graphic resources on web pages belong to the original copyright owner. Users shall not use converted images for commercial reproduction, unauthorized distribution, secondary creation and other copyright-infringing acts. All legal liabilities arising from improper use shall be borne solely by the user.

## Cross-origin Image Reminder

The cross-origin image fetch function is only used to obtain image resources for local format conversion. It is forbidden to use this function to mass crawl website image resources in batches, which may violate the website's access rules.

---

## Source Code Notice

> ⚠️ **This repository does not publish source code.** It contains only usage documentation, release notes, and support resources. The extension is distributed exclusively through the Chrome Web Store. No offline installation packages or end-user source code are provided.

---

## License

Copyright © 2026 ImageConv. All rights reserved.

### How Licensing Works

ImageConv uses a device-based license system:

1. **Purchase** a license key at [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activate** by clicking the 🔑 button in the popup and entering your key
3. The key is bound to your device (hardware fingerprint) — one key, one device
4. License is validated online every 24 hours; works offline for up to 7 days

### What's Free vs Paid

| Feature | Free | Premium |
|---------|:----:|:-------:|
| Right-click image conversion (web images) | ✅ | ✅ |
| Save as PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copy to clipboard | ✅ | ✅ |
| Quality adjustment sliders | ✅ | ✅ |
| Cross-origin image fetch | ✅ | ✅ |
| Smart link cleaning | ✅ | ✅ |
| Drag & drop local file conversion | ❌ | ✅ |
| Batch local file conversion | ❌ | ✅ |

**Summary**: All web image features (right-click save/copy) are **free**. Local file conversion (drag & drop) requires a **premium license**.

---

## ❤️ Support

If you find ImageConv helpful, consider supporting the project!

**[👉 Support on Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Official Website](https://www.annmax1983.com/extensions/imageconv)**

---

