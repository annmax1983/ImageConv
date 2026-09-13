# ImageConv

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | Deutsch | [日本語](README_ja.md) | [Français](README_fr.md)

Eine schlanke Browser-Erweiterung zum Konvertieren von Bildern zwischen PNG, JPG, WEBP und AVIF — komplett lokal, ohne Datenupload.

> Chromium-basiert · Manifest V3 · Kein Tracking · Verarbeitung vollständig im Browser

---

## Warum ImageConv?

Die meisten Bildkonvertierungstools verlangen, dass du deine Dateien auf einen Remote-Server hochlädst. ImageConv erledigt alles direkt in deinem Browser über die Canvas API — keine Daten verlassen jemals deinen Rechner.

| Vorteil | Details |
|---------|---------|
| 🔒 **Datenschutz zuerst** | Die gesamte Verarbeitung läuft im Arbeitsspeicher deines Browsers. Keine Server, keine Uploads, kein Tracking. |
| ⚡ **Sofortige Konvertierung** | Bilder ≤5MB werden in unter 500ms konvertiert. Kein Warten auf Server-Antworten. |
| 🎯 **Null Abhängigkeiten** | Gebaut mit Vanilla JavaScript und nativen Chrome APIs. Keine Frameworks, kein Ballast. |
| 🌍 **6 Sprachen** | Erkennt automatisch deine Browsersprache — Englisch, Spanisch, Deutsch, Japanisch, Französisch, Chinesisch. |
| 📋 **Kopieren & Speichern** | Rechtsklick auf ein beliebiges Bild, um es als Datei zu speichern ODER direkt in die Zwischenablage zu kopieren. |
| 📁 **Drag & Drop** | Ziehe lokale Bilder auf das Popup zur schnellen Konvertierung. |

---

## Funktionen

### Kostenlose Funktionen

| Funktion | Beschreibung |
|----------|--------------|
| 🖼️ **Rechtsklick-Konvertierung** | Konvertiere beliebige Webseiten-Bilder zu PNG, JPG, WEBP oder AVIF über das Kontextmenü |
| 📱 **HEIC/HEIF-Unterstützung** | iPhone-Fotos direkt konvertieren — per Drag & Drop, Einfügen oder Rechtsklick. Lokale Entschlüsselung über eingebauten WASM-Decoder |
| 📐 **Größenänderung** | Skalierung in Prozent oder exakte Pixelmaße (ein Feld leer lassen für Originalverhältnis). Gilt für Popup- und Rechtsklick-Konvertierung |
| 📋 **In Zwischenablage kopieren** | Rechtsklick → Als PNG/JPG/WEBP/AVIF kopieren — in E-Mails, Chats, Dokumente einfügen |
| 📊 **Dateigrößen-Vergleich** | Toast-Benachrichtigung zeigt Original- vs. konvertierte Größe mit Ersparnis-Prozent (basierend auf echten Dateigrößen) |
| 🎚️ **Qualitätseinstellung** | Feinabstimmung der Exportqualität für JPG, WEBP und AVIF über Schieberegler im Popup |
| 🔗 **Intelligentes Link-Cleaning** | Entfernt CDN-Tracking-Parameter, um Originalbilder zu laden |
| 🌐 **Cross-Origin-Unterstützung** | Lädt Bilder von jeder Website über den Service Worker |
| 🔤 **6-Sprachen-i18n** | Kontextmenü und UI passen sich automatisch an deine Browsersprache an |
| 🛡️ **JPG weißer Hintergrund** | Transparente Hintergründe werden beim Konvertieren von PNG → JPG automatisch weiß gefüllt |
| ⏱️ **Duplikat-Schutz** | Ignoriert wiederholte Klicks auf dasselbe Bild innerhalb von 2 Sekunden |

### Premium-Funktionen (Lizenz erforderlich)

| Funktion | Beschreibung |
|----------|--------------|
| ⭐ **Drag & Drop Konvertierung** | Lokale Bilder per Drag & Drop oder Einfügen (Strg+V) ins Popup ziehen |
| 📁 **Batch-Konvertierung** | Mehrere lokale Dateien auf einmal konvertieren |

---

## Kostenlos vs. Premium

| | Kostenlos | Premium |
|---|:---:|:---:|
| Rechtsklick-Bildkonvertierung | ✅ | ✅ |
| In Zwischenablage kopieren | ✅ | ✅ |
| Qualitätseinstellung | ✅ | ✅ |
| HEIC/HEIF-Eingabe | ✅ | ✅ |
| Größenänderung | ✅ | ✅ |
| Cross-Origin Bilder laden | ✅ | ✅ |
| Drag & Drop lokale Konvertierung | — | ✅ |
| Batch-Konvertierung lokaler Dateien | — | ✅ |

---

## Vorschau

<!-- Ersetzen durch tatsächliche Screenshots -->
<p align="center">
  <img src="screenshots/popup.png" alt="ImageConv Popup" width="360">
</p>

<p align="center">
  <img src="screenshots/context-menu.png" alt="ImageConv Kontextmenü">
</p>

---

## Unterstützte Browser

| Browser | Status |
|---------|--------|
| Google Chrome | ✅ Vollständig unterstützt |
| Microsoft Edge | ✅ Vollständig unterstützt |
| Brave | ✅ Unterstützt |
| Opera | ✅ Unterstützt |
| Vivaldi | ✅ Unterstützt |
| Jeder Chromium-basierte Browser | ✅ Unterstützt (Manifest V3) |

---

## Installation

### Aus dem Quellcode (Entwicklermodus)

1. Öffne die Erweiterungsseite deines Browsers:
   - **Chrome**: `chrome://extensions/`
   - **Edge**: `edge://extensions/`
2. Aktiviere den **Entwicklermodus** (Schalter oben rechts)
3. Klicke auf **Entpackte Erweiterung laden** und wähle den Ordner `pic-convert`
4. Das ✨ ImageConv-Symbol erscheint in deiner Toolbar

---

## Verwendung

### Rechtsklick-Konvertierung

1. Rechtsklick auf ein beliebiges Bild auf einer Webseite
2. Wähle **ImageConv** aus dem Kontextmenü
3. Wähle **Speichern als** oder **Kopieren als**
4. Wähle dein Format: PNG, JPG, WEBP oder AVIF
5. Fertig — die Datei wird sofort heruntergeladen oder das Bild in die Zwischenablage kopiert

### Drag & Drop (Premium)

> ⚠️ Drag & Drop ist eine Premium-Funktion. Ein Lizenzschlüssel ist erforderlich.

1. Klicke auf das ImageConv-Symbol in deiner Toolbar, um das Popup zu öffnen
2. Klicke auf die 🔑-Taste oben rechts, um deinen Lizenzschlüssel einzugeben
3. Sobald aktiviert, ziehe eine lokale Bilddatei auf die Dropzone
4. Wähle dein Zielformat
5. Die konvertierte Datei wird automatisch heruntergeladen

Du kannst einen Lizenzschlüssel unter [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv) erwerben.

### Qualitätseinstellungen

Öffne das Popup, um die Exportqualität für JPG, WEBP und AVIF über Schieberegler anzupassen. PNG ist immer verlustfrei. Einstellungen werden automatisch gespeichert.

### Größenänderung

Der Bereich „Größe ändern“ im Popup unterstützt Skalierung in Prozent (5 %–200 %) oder exakte Pixelmaße. Ein Feld leer lassen erhält das Originalverhältnis. Die Einstellung gilt für Drag & Drop und Rechtsklick-Konvertierung gleichermaßen; Standard ist die Originalgröße.

### HEIC/HEIF (iPhone-Fotos)

Ziehe `.heic`- / `.heif`-Dateien ins Popup (oder konvertiere einen HEIC-Bildlink auf einer Webseite), um sie als PNG/JPG/WEBP zu speichern. Die Entschlüsselung erfolgt vollständig lokal über WASM — nichts wird hochgeladen.

---

## Kontextmenü-Struktur

```
ImageConv
├── Speichern als PNG (Verlustfrei)
├── Speichern als JPG (Hohe Qualität)
├── Speichern als WEBP (Kompakt)
├── Speichern als AVIF (Beste Kompression)
├── Kopieren als PNG (Verlustfrei)
├── Kopieren als JPG (Hohe Qualität)
├── Kopieren als WEBP (Kompakt)
└── Kopieren als AVIF (Beste Kompression)
```

Die Menüs **Kopieren als** und **Speichern als** erscheinen nur bei Rechtsklick auf Bilder oder Links, die auf Bilddateien zeigen (`.png`, `.jpg`, `.jpeg`, `.webp`, `.avif`, `.gif`, `.bmp`, `.jfif`, `.svg`).

---

## Datenschutz

ImageConv wurde mit Datenschutz als Grundprinzip entwickelt:

- ✅ **Kein Datenupload** — Die gesamte Bildverarbeitung läuft im Arbeitsspeicher deines Browsers
- ✅ **Keine Analytik** — Kein Tracking, keine Telemetrie, keine Remote-Aufrufe
- ✅ **Keine Cookies** — Kein Lesen oder Schreiben von Browser-Cookies
- ✅ **Kein Verlauf** — Kein Zugriff auf deine Browserdaten
- ✅ **Nur temporärer Speicher** — Bilder existieren während der Konvertierung im Speicher und werden danach sofort gelöscht
- ✅ **Minimale Berechtigungen** — Nur das absolut Notwendige: `contextMenus`, `downloads`, `offscreen`, `storage`, `clipboardWrite`

---

## So funktioniert es

```
Rechtsklick auf Bild
       ↓
Service Worker holt Bild-Blob (behandelt Cross-Origin)
       ↓
Sendet Blob an Offscreen Document (verstecktes DOM mit Canvas-Zugriff)
       ↓
Canvas zeichnet Bild in nativer Auflösung
       ↓
Exportiert als Zielformat mit angegebener Qualität
       ↓
Gibt Data URL zurück → löst Download aus oder kopiert in Zwischenablage
       ↓
Zerstört alle temporären Ressourcen (Blob, Canvas, Image-Element)
```

> **Warum Offscreen?** Chromes Manifest V3 führt den Hintergrund als Service Worker aus, der keinen DOM-Zugriff hat. Die Canvas API benötigt einen DOM, daher verwenden wir Chromes Offscreen API, um ein verstecktes Dokument für die Bildverarbeitung zu erstellen.

---

## Standard-Exportqualität

| Format | Qualität | Anmerkungen |
|--------|----------|-------------|
| PNG | Verlustfrei | Keine Qualitätseinstellung — immer volle Qualität und Transparenz |
| JPG | 92 | Hohe Qualität, gute Balance zwischen Größe und Schärfe |
| WEBP | 90 | Modernes Format, ~25-35% kleiner als JPG bei gleicher Qualität |
| AVIF | 70 | Nächstes Generation-Format, ~20-30% kleiner als WEBP, ideal für Web |

Alle Qualitätswerte sind über Schieberegler im Popup anpassbar (Bereich: 10–100).

> ℹ️ AVIF wird über einen eingebauten WASM-Encoder erzeugt (Chromes Canvas kann nativ kein AVIF encodieren). Überdimensionale Bilder (über 25 Megapixel) werden automatisch als WEBP ausgegeben, mit Hinweis.

---

## Urheberrechtshinweis

Diese Erweiterung bietet nur lokale Bildformat-Konvertierung für die persönliche Offline-Verarbeitung. Alle Bilder, Fotos und grafischen Ressourcen auf Webseiten gehören dem jeweiligen Urheberrechtsinhaber. Nutzer dürfen konvertierte Bilder nicht für kommerzielle Vervielfältigung, unbefugte Verbreitung, Nachbearbeitung oder andere urheberrechtsverletzende Handlungen verwenden. Alle rechtlichen Folgen aus missbräuchlicher Nutzung trägt allein der Nutzer.

## Cross-Origin-Hinweis

Die Cross-Origin-Bildlade-Funktion dient ausschließlich dem Abruf von Bildressourcen für die lokale Formatkonvertierung. Es ist verboten, diese Funktion zum massenhaften Auslesen von Website-Bildressourcen zu verwenden, da dies gegen die Zugriffsregeln der Website verstoßen könnte.

---

## Quellcode-Hinweis

> ⚠️ **Dieses Repository veröffentlicht keinen Quellcode.** Es enthält nur Nutzerdokumentation, Versionshinweise und Support-Ressourcen. Die Erweiterung wird ausschließlich über den Chrome Web Store vertrieben. Es werden keine Offline-Installationspakete oder Endbenutzer-Quellcodes bereitgestellt.

---

## Lizenz

Copyright © 2026 ImageConv. Alle Rechte vorbehalten.

### So funktioniert die Lizenzierung

ImageConv verwendet ein gerätebasiertes Lizenzsystem:

1. **Kauf** eines Lizenzschlüssels unter [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Aktivierung** durch Klick auf die 🔑-Taste im Popup und Eingabe deines Schlüssels
3. Der Schlüssel wird an dein Gerät gebunden (Hardware-Fingerprint) — ein Schlüssel, ein Gerät
4. Die Lizenz wird alle 24 Stunden online validiert; funktioniert offline bis zu 7 Tage

### Was ist kostenlos vs. kostenpflichtig?

| Funktion | Kostenlos | Premium |
|----------|:---------:|:-------:|
| Rechtsklick-Bildkonvertierung (Web-Bilder) | ✅ | ✅ |
| Speichern als PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| In Zwischenablage kopieren | ✅ | ✅ |
| Qualitätseinstellung per Schieberegler | ✅ | ✅ |
| HEIC/HEIF-Eingabe (WASM-Entschlüsselung) | ✅ | ✅ |
| Größenänderung (Prozent / Pixel) | ✅ | ✅ |
| Cross-Origin Bilder laden | ✅ | ✅ |
| Intelligentes Link-Cleaning | ✅ | ✅ |
| Drag & Drop lokale Dateikonvertierung | ❌ | ✅ |
| Batch-Konvertierung lokaler Dateien | ❌ | ✅ |

**Zusammenfassung**: Alle Web-Bildfunktionen (Rechtsklick Speichern/Kopieren) sind **kostenlos**. Lokale Dateikonvertierung (Drag & Drop) erfordert eine **Premium-Lizenz**.

---

## ❤️ Support

Wenn dir ImageConv hilft, unterstütze das Projekt gerne!

**[👉 Support auf Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Offizielle Website](https://www.annmax1983.com/extensions/imageconv)**
