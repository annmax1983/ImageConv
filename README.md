# ImageConv

English | [中文](languages/README_zh.md) | [Español](languages/README_es.md) | [Deutsch](languages/README_de.md) | [日本語](languages/README_ja.md) | [Français](languages/README_fr.md)

A lightweight browser extension that converts images between PNG, JPG, WEBP, and AVIF formats — entirely locally, with zero data upload.

> Chromium-based · Manifest V3 · No tracking · Fully In-Browser Processing

---

## Why ImageConv?

Most image conversion tools require uploading your files to a remote server. ImageConv does everything inside your browser using the Canvas API — no image data ever leaves your machine.

| Advantage | Detail |
|-----------|--------|
| 🔒 **Privacy-First** | All processing happens in your browser's memory. No uploads, no tracking. The only outbound request is optional license validation. |
| ⚡ **Instant Conversion** | Images ≤5MB convert in under 500ms. No waiting for server round-trips. |
| 🎯 **Zero Dependencies** | Built with vanilla JavaScript and native Chrome APIs. No frameworks, no bloat. |
| 🌍 **6 Languages** | Auto-detects your browser language — English, Spanish, German, Japanese, French, Chinese. |
| 📋 **Copy & Save** | Right-click any image to save as a file OR copy directly to your clipboard. |
| 📁 **Drag & Drop** | Drop local images onto the popup for quick conversion. |
| 🖼️ **Batch Export** | List every image already loaded on a page, tick the ones you want, and export them all at once. |

---

## Features

### Free Features

| Feature | Description |
|---------|-------------|
| 🖼️ **Right-Click Conversion** | Convert any webpage image to PNG, JPG, WEBP, or AVIF via context menu |
| 📱 **HEIC/HEIF Support** | Convert iPhone photos directly — drag & drop, paste, or right-click. Decoded locally via built-in WASM decoder |
| 📐 **Resize** | Scale by percentage or set exact pixel dimensions (leave one field empty to keep aspect ratio). Applies to both popup and right-click conversions |
| 📋 **Copy to Clipboard** | Right-click → Copy as PNG — paste into emails, chats, documents |
| 📊 **File Size Comparison** | Toast notification shows original vs converted size with savings percentage (based on real file sizes) |
| 🎚️ **Adjustable Quality** | Fine-tune export quality for JPG, WEBP, and AVIF via sliders in the popup |
| 🔗 **Smart Link Cleaning** | Strips CDN tracking parameters to fetch original images |
| 🌐 **Cross-Origin Support** | Fetches images from any website via Service Worker |
| 🔤 **6-Language i18n** | Context menu and UI auto-match your browser language |
| 🛡️ **JPG White Fill** | Automatically fills transparent backgrounds with white when converting PNG → JPG |
| ⏱️ **Duplicate Guard** | Ignores repeated clicks on the same image within 2 seconds |
| 📦 **Batch Up to 5 per Run** | On the free plan, convert up to 5 local files per drop, or export up to 5 web images per run. Pro raises both limits |

### Pro Features (License Required)

| Feature | Description |
|---------|-------------|
| ♾️ **Unlimited Local Batch** | Free multi-file drops convert up to 5 files per run; Pro removes the local cap |
| 📦 **Large Web Exports** | Export up to 100 images from a page in one run (free: 5) |
| 🗜️ **ZIP Archive Export** | Bundle a web batch into one `.zip` file. If packaging fails or the archive would exceed 4 GB, completed images are saved individually |
| 🗂️ **Batch Presets** | Save up to 12 format/quality/resize presets in the batch Options dialog and reapply them in one click |
| 🏷️ **Filename Templates** | Name batch web downloads with `{name}`, `{index}`, `{format}`, `{date}`, `{width}`, and `{height}`. The extension is added automatically and collisions get `-2`, `-3` |

Format, quality, and resize editing in the batch Options dialog stays free. Presets, file naming, and ZIP delivery are Pro and apply to the batch export page, not to popup drag & drop.

---

## Free vs Pro

| | Free | Pro |
|---|:---:|:---:|
| Right-click image conversion | ✅ | ✅ |
| Copy to clipboard | ✅ PNG only | ✅ PNG only |
| Quality adjustment | ✅ | ✅ |
| HEIC/HEIF input | ✅ | ✅ |
| Resize | ✅ | ✅ |
| Cross-origin image fetch | ✅ | ✅ |
| Drag & drop / paste local images | ✅ Up to 5 files | ✅ Unlimited |
| Batch local file conversion | Up to 5 per run | Unlimited |
| Batch export images from a web page | Up to 5 per run | Up to 100 per run |
| Batch format / quality / resize | ✅ | ✅ |
| Batch presets | — | ✅ Up to 12 |
| Filename templates (batch page) | — | ✅ |
| ZIP archive delivery (batch page) | — | ✅ |

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
3. Choose **Save as** (PNG/JPG/WEBP/AVIF) or **Copy as PNG**
4. Done — the file downloads instantly, or the image is copied to clipboard as PNG

### Drag & Drop / Paste (Free)

1. Click the ImageConv icon in your toolbar to open the popup
2. Drag a local image file onto the drop zone, or paste with Ctrl+V
3. Select your target format
4. The converted file downloads automatically

Single images are always free. On the free plan a multi-file drop converts the first 5 files; a Pro license removes the per-run cap. Batch presets, filename templates, and ZIP delivery are only available on the web batch page, not for popup drag & drop.

### Batch Export Web Images (Free Up to 5, Pro Up to 100)

1. Open the page whose images you want (they must already be loaded)
2. Click the ImageConv icon, then **Batch export images on this page**
3. A new tab lists every image found, largest first — tick the ones you want
4. Click **Options** to set format, quality, and resize. Everyone can edit these; Pro can also apply or save a preset, edit the file-naming template, and choose **One ZIP archive** under Delivery
5. Click **Export selected** (the button becomes **Export ZIP** when ZIP delivery is on)

Individual files download to `ImageConv/` using the naming template. ZIP runs download one `ImageConv/<host>-YYYYMMDD-HHmm.zip`; if packaging fails or the archive would exceed 4 GB, completed images are saved individually.

Images smaller than 100 px are hidden by default (icons, avatars, tracking pixels) — adjust the filter in the toolbar. The free plan exports up to 5 images per run; Pro raises the limit to 100.

### Quality Settings

Open the popup to adjust export quality for JPG, WEBP, and AVIF using the sliders. PNG is always lossless. Settings are saved automatically.

### Resize

The **Resize** section in the popup supports scaling by percentage (5%–200%) or exact pixel dimensions. Leave one field empty to keep the aspect ratio. The setting applies to both drag & drop and right-click conversions; the default keeps the original size.

### HEIC/HEIF (iPhone Photos)

Drop or paste `.heic` / `.heif` files into the popup, or right-click a HEIC image displayed on a page, to save it as PNG/JPG/WEBP. Decoding happens entirely locally via WASM — nothing is uploaded. HEIC input is free on every plan.

---

## Context Menu Structure

```
ImageConv
├── Save as PNG (Lossless)
├── Save as JPG (High Quality)
├── Save as WEBP (Compact)
├── Save as AVIF (Best Compression)
└── Copy as PNG (Lossless)
```

The **Save as** and **Copy as PNG** menus only appear when right-clicking an image, including an image inside a link. Plain links to image files do not show the menu. Clipboard output is PNG only.

---

## Privacy

ImageConv is built with privacy as a core principle:

- ✅ **Zero data upload** — All image processing happens in your browser's memory
- ✅ **No analytics** — No tracking, no telemetry. The only outbound request is license validation (license key + a random install identifier) when you activate, or when the cached 2 h check expires — image data is never transmitted
- ✅ **No cookies** — No reading or writing of browser cookies
- ✅ **No browsing history** — No access to your browsing data
- ✅ **Temporary memory only** — Images exist in memory during conversion and are immediately destroyed after
- ✅ **Minimal permissions** — Only what each feature needs: `contextMenus`, `downloads`, `offscreen`, `storage`, `scripting`, `clipboardWrite`, plus `<all_urls>` so the extension can fetch the image you clicked and scan a page for image export

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

> ℹ️ AVIF is produced by a built-in WASM encoder (Chromium's Canvas cannot natively encode AVIF). Oversized images (over 25 megapixels) automatically fall back to WEBP with a notice.

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

ImageConv uses an activation-based license system:

1. **Purchase** a license key at [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activate** by clicking the 🔑 button in the popup and entering your key
3. Each activation covers one browser installation; deactivate an old installation in the popup to free a slot for a new one
4. License is validated online every 2 hours; if the server is unreachable, the cached license keeps working

### What's Free vs Paid

| Feature | Free | Pro |
|---------|:----:|:---:|
| Right-click image conversion (web images) | ✅ | ✅ |
| Save as PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copy to clipboard | ✅ PNG only | ✅ PNG only |
| Quality adjustment sliders | ✅ | ✅ |
| HEIC/HEIF input (WASM decode) | ✅ | ✅ |
| Resize (percent / exact pixels) | ✅ | ✅ |
| Cross-origin image fetch | ✅ | ✅ |
| Smart link cleaning | ✅ | ✅ |
| Drag & drop / paste local files | ✅ Up to 5 files | ✅ Unlimited |
| Batch local file conversion | Up to 5 per run | Unlimited |
| Batch export images from a web page | Up to 5 per run | Up to 100 per run |
| Batch format / quality / resize | ✅ | ✅ |
| Batch presets | — | ✅ Up to 12 |
| Filename templates (batch page) | — | ✅ |
| ZIP archive delivery (batch page) | — | ✅ |

**Summary**: Right-click conversion, single drag & drop/paste, up to 5 images per batch run, and batch format/quality/resize editing are **free**. A **Pro license** removes the local batch cap, raises web exports to 100 per run, and unlocks presets, filename templates, and ZIP delivery.

---

## ❤️ Support

If you find ImageConv helpful, consider supporting the project!

**[👉 Support on Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Official Website](https://www.annmax1983.com/extensions/imageconv)**

---

