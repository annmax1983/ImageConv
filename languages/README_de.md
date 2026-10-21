# ImageConv

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | Deutsch | [日本語](README_ja.md) | [Français](README_fr.md)

Eine schlanke Browser-Erweiterung zum Konvertieren von Bildern zwischen PNG, JPG, WEBP und AVIF — komplett lokal, ohne Datenupload.

> Chromium-basiert · Manifest V3 · Kein Tracking · Verarbeitung vollständig im Browser

---

## Warum ImageConv?

Die meisten Bildkonvertierungstools verlangen, dass du deine Dateien auf einen Remote-Server hochlädst. ImageConv erledigt alles direkt in deinem Browser über die Canvas API — keine Bilddaten verlassen jemals deinen Rechner.

| Vorteil | Details |
|---------|---------|
| 🔒 **Datenschutz zuerst** | Die gesamte Verarbeitung läuft im Arbeitsspeicher deines Browsers. Keine Uploads, kein Tracking. Die einzige ausgehende Anfrage ist die optionale Lizenzprüfung. |
| ⚡ **Sofortige Konvertierung** | Bilder ≤5MB werden in unter 500ms konvertiert. Kein Warten auf Server-Antworten. |
| 🎯 **Null Abhängigkeiten** | Gebaut mit Vanilla JavaScript und nativen Chrome APIs. Keine Frameworks, kein Ballast. |
| 🌍 **6 Sprachen** | Erkennt automatisch deine Browsersprache — Englisch, Spanisch, Deutsch, Japanisch, Französisch, Chinesisch. |
| 📋 **Kopieren & Speichern** | Rechtsklick auf ein beliebiges Bild, um es als Datei zu speichern ODER direkt in die Zwischenablage zu kopieren. |
| 📁 **Drag & Drop** | Ziehe lokale Bilder auf das Popup zur schnellen Konvertierung. |
| 🖼️ **Stapelexport** | Listet alle bereits geladenen Bilder einer Seite auf, du wählst aus und exportierst sie auf einmal. |

---

## Funktionen

### Kostenlose Funktionen

| Funktion | Beschreibung |
|----------|--------------|
| 🖼️ **Rechtsklick-Konvertierung** | Konvertiere beliebige Webseiten-Bilder zu PNG, JPG, WEBP oder AVIF über das Kontextmenü |
| 📱 **HEIC/HEIF-Unterstützung** | iPhone-Fotos direkt konvertieren — per Drag & Drop, Einfügen oder Rechtsklick. Lokale Entschlüsselung über eingebauten WASM-Decoder |
| 📐 **Größenänderung** | Skalierung in Prozent oder exakte Pixelmaße (ein Feld leer lassen für Originalverhältnis). Gilt für Popup- und Rechtsklick-Konvertierung |
| 📋 **In Zwischenablage kopieren** | Rechtsklick → Als PNG kopieren — in E-Mails, Chats, Dokumente einfügen |
| 📊 **Dateigrößen-Vergleich** | Toast-Benachrichtigung zeigt Original- vs. konvertierte Größe mit Ersparnis-Prozent (basierend auf echten Dateigrößen) |
| 🎚️ **Qualitätseinstellung** | Feinabstimmung der Exportqualität für JPG, WEBP und AVIF über Schieberegler im Popup |
| 🔗 **Intelligentes Link-Cleaning** | Entfernt CDN-Tracking-Parameter, um Originalbilder zu laden |
| 🌐 **Cross-Origin-Unterstützung** | Lädt Bilder von jeder Website über den Service Worker |
| 🔤 **6-Sprachen-i18n** | Kontextmenü und UI passen sich automatisch an deine Browsersprache an |
| 🛡️ **JPG weißer Hintergrund** | Transparente Hintergründe werden beim Konvertieren von PNG → JPG automatisch weiß gefüllt |
| ⏱️ **Duplikat-Schutz** | Ignoriert wiederholte Klicks auf dasselbe Bild innerhalb von 2 Sekunden |

### Pro-Funktionen (Lizenz erforderlich)

| Funktion | Beschreibung |
|----------|--------------|
| ♾️ **Unbegrenzte lokale Batch-Konvertierung** | Kostenlose Mehrfach-Drops konvertieren bis zu 5 Dateien pro Durchlauf; Pro hebt das lokale Limit auf |
| 📦 **Große Web-Exporte** | Bis zu 100 Bilder einer Seite pro Durchlauf exportieren (kostenlos: 5) |
| 🗜️ **ZIP-Archiv-Export** | Ein Web-Batch als eine `.zip`-Datei. Schlägt das Packen fehl oder überschreitet das Archiv 4 GB, werden fertige Bilder einzeln gespeichert |
| 🗂️ **Batch-Presets** | Bis zu 12 Presets für Format/Qualität/Größe im Batch-Dialog „Optionen“ speichern und mit einem Klick erneut anwenden |
| 🏷️ **Dateinamen-Vorlagen** | Batch-Webdownloads mit `{name}`, `{index}`, `{format}`, `{date}`, `{width}` und `{height}` benennen. Die Erweiterung wird automatisch ergänzt, Namenskollisionen erhalten `-2`, `-3` |

Format-, Qualitäts- und Größenbearbeitung im Batch-Dialog „Optionen“ bleibt kostenlos. Presets, Dateibenennung und ZIP-Auslieferung sind Pro und gelten nur für die Batch-Exportseite, nicht für Drag & Drop im Popup.

---

## Kostenlos vs. Pro

| | Kostenlos | Pro |
|---|:---:|:---:|
| Rechtsklick-Bildkonvertierung | ✅ | ✅ |
| In Zwischenablage kopieren | ✅ Nur PNG | ✅ Nur PNG |
| Qualitätseinstellung | ✅ | ✅ |
| HEIC/HEIF-Eingabe | ✅ | ✅ |
| Größenänderung | ✅ | ✅ |
| Cross-Origin Bilder laden | ✅ | ✅ |
| Drag & Drop / Einfügen lokaler Bilder | ✅ Bis zu 5 Dateien | ✅ Unbegrenzt |
| Batch-Konvertierung lokaler Dateien | Bis zu 5 pro Durchlauf | Unbegrenzt |
| Bilder einer Webseite im Stapel exportieren | Bis zu 5 pro Durchlauf | Bis zu 100 pro Durchlauf |
| Batch-Format / -Qualität / -Größe | ✅ | ✅ |
| Batch-Presets | — | ✅ Bis zu 12 |
| Dateinamen-Vorlagen (Batch-Seite) | — | ✅ |
| ZIP-Archiv-Auslieferung (Batch-Seite) | — | ✅ |

---

## Vorschau

<!-- Ersetzen durch tatsächliche Screenshots -->
<p align="center">
  <img src="../screenshots/popup.png" alt="ImageConv Popup" width="360">
</p>

<p align="center">
  <img src="../screenshots/context-menu.png" alt="ImageConv Kontextmenü">
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
3. Wähle **Speichern als** (PNG/JPG/WEBP/AVIF) oder **Kopieren als PNG**
4. Fertig — die Datei wird sofort heruntergeladen oder das Bild als PNG in die Zwischenablage kopiert

### Drag & Drop / Einfügen (kostenlos)

1. Klicke auf das ImageConv-Symbol in deiner Toolbar, um das Popup zu öffnen
2. Ziehe eine lokale Bilddatei auf die Dropzone oder füge sie mit Strg+V ein
3. Wähle dein Zielformat
4. Die konvertierte Datei wird automatisch heruntergeladen

Einzelne Bilder sind immer kostenlos. Im kostenlosen Plan konvertiert ein Mehrfach-Drop die ersten 5 Dateien; eine Pro-Lizenz hebt das Limit pro Durchlauf auf. Batch-Presets, Dateinamen-Vorlagen und ZIP-Auslieferung gibt es nur auf der Web-Batch-Seite, nicht bei Drag & Drop im Popup.

### Stapelexport von Web-Bildern (kostenlos 5, Pro 100)

1. Öffne die Seite, deren Bilder du exportieren möchtest (sie müssen bereits geladen sein)
2. Klicke auf das ImageConv-Symbol und dann auf **Bilder dieser Seite exportieren**
3. Ein neuer Tab listet alle gefundenen Bilder auf, die größten zuerst — markiere die gewünschten
4. Klicke auf **Optionen**, um Format, Qualität und Größe einzustellen. Alle können diese bearbeiten; Pro kann zusätzlich ein Preset anwenden oder speichern, die Dateinamen-Vorlage bearbeiten und unter Auslieferung **Ein ZIP-Archiv** wählen
5. Klicke auf **Auswahl exportieren** (bei aktiver ZIP-Auslieferung heißt der Button **ZIP exportieren**)

Einzelne Dateien werden mit der Namensvorlage unter `ImageConv/` gespeichert. ZIP-Läufe laden eine `ImageConv/<host>-YYYYMMDD-HHmm.zip` herunter; schlägt das Packen fehl oder überschreitet das Archiv 4 GB, werden fertige Bilder einzeln gespeichert.

Bilder unter 100 px werden standardmäßig ausgeblendet (Symbole, Avatare, Tracking-Pixel) — passe den Filter in der Symbolleiste an. Kostenlos sind bis zu 5 Bilder pro Durchlauf möglich, mit Pro bis zu 100.

### Qualitätseinstellungen

Öffne das Popup, um die Exportqualität für JPG, WEBP und AVIF über Schieberegler anzupassen. PNG ist immer verlustfrei. Einstellungen werden automatisch gespeichert.

### Größenänderung

Der Bereich „Größe ändern“ im Popup unterstützt Skalierung in Prozent (5 %–200 %) oder exakte Pixelmaße. Ein Feld leer lassen erhält das Originalverhältnis. Die Einstellung gilt für Drag & Drop und Rechtsklick-Konvertierung gleichermaßen; Standard ist die Originalgröße.

### HEIC/HEIF (iPhone-Fotos)

Ziehe `.heic`- / `.heif`-Dateien ins Popup oder füge sie ein, oder klicke mit der rechten Maustaste auf ein auf einer Seite angezeigtes HEIC-Bild, um es als PNG/JPG/WEBP zu speichern. Die Entschlüsselung erfolgt vollständig lokal über WASM — nichts wird hochgeladen. HEIC-Eingabe ist in jedem Plan kostenlos.

---

## Kontextmenü-Struktur

```
ImageConv
├── Speichern als PNG (Verlustfrei)
├── Speichern als JPG (Hohe Qualität)
├── Speichern als WEBP (Kompakt)
├── Speichern als AVIF (Beste Kompression)
└── Kopieren als PNG (Verlustfrei)
```

Die Menüs **Speichern als** und **Kopieren als PNG** erscheinen nur beim Rechtsklick auf ein Bild, auch auf ein Bild innerhalb eines Links. Reine Links zu Bilddateien zeigen das Menü nicht. Die Zwischenablage-Ausgabe ist nur PNG.

---

## Datenschutz

ImageConv wurde mit Datenschutz als Grundprinzip entwickelt:

- ✅ **Kein Datenupload** — Die gesamte Bildverarbeitung läuft im Arbeitsspeicher deines Browsers
- ✅ **Keine Analytik** — Kein Tracking, keine Telemetrie. Die einzige ausgehende Anfrage ist die Lizenzprüfung (Lizenzschlüssel + eine zufällige Installationskennung) beim Aktivieren oder wenn die zwischengespeicherte 2-Stunden-Prüfung abläuft — Bilddaten werden nie übertragen
- ✅ **Keine Cookies** — Kein Lesen oder Schreiben von Browser-Cookies
- ✅ **Kein Verlauf** — Kein Zugriff auf deine Browserdaten
- ✅ **Nur temporärer Speicher** — Bilder existieren während der Konvertierung im Speicher und werden danach sofort gelöscht
- ✅ **Minimale Berechtigungen** — Nur was die jeweilige Funktion braucht: `contextMenus`, `downloads`, `offscreen`, `storage`, `scripting`, `clipboardWrite`, plus `<all_urls>`, um das angeklickte Bild zu laden und eine Seite für den Stapelexport zu scannen

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

ImageConv verwendet ein aktivierungsbasiertes Lizenzsystem:

1. **Kauf** eines Lizenzschlüssels unter [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Aktivierung** durch Klick auf die 🔑-Taste im Popup und Eingabe deines Schlüssels
3. Jede Aktivierung gilt für eine Browser-Installation; deaktiviere eine alte Installation im Popup, um einen Platz für eine neue freizugeben
4. Die Lizenz wird alle 2 Stunden online validiert; ist der Server nicht erreichbar, funktioniert die gecachte Lizenz weiter

### Was ist kostenlos vs. kostenpflichtig?

| Funktion | Kostenlos | Pro |
|----------|:---------:|:---:|
| Rechtsklick-Bildkonvertierung (Web-Bilder) | ✅ | ✅ |
| Speichern als PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| In Zwischenablage kopieren | ✅ Nur PNG | ✅ Nur PNG |
| Qualitätseinstellung per Schieberegler | ✅ | ✅ |
| HEIC/HEIF-Eingabe (WASM-Entschlüsselung) | ✅ | ✅ |
| Größenänderung (Prozent / Pixel) | ✅ | ✅ |
| Cross-Origin Bilder laden | ✅ | ✅ |
| Intelligentes Link-Cleaning | ✅ | ✅ |
| Drag & Drop / Einfügen lokaler Dateien | ✅ Bis zu 5 Dateien | ✅ Unbegrenzt |
| Batch-Konvertierung lokaler Dateien | Bis zu 5 pro Durchlauf | Unbegrenzt |
| Bilder einer Webseite im Stapel exportieren | Bis zu 5 pro Durchlauf | Bis zu 100 pro Durchlauf |
| Batch-Format / -Qualität / -Größe | ✅ | ✅ |
| Batch-Presets | — | ✅ Bis zu 12 |
| Dateinamen-Vorlagen (Batch-Seite) | — | ✅ |
| ZIP-Archiv-Auslieferung (Batch-Seite) | — | ✅ |

**Zusammenfassung**: Rechtsklick-Konvertierung, einzelne Drag & Drop-/Einfüge-Vorgänge, bis zu 5 Bilder pro Batch-Durchlauf und die Bearbeitung von Format/Qualität/Größe im Batch-Dialog „Optionen“ sind **kostenlos**. Eine **Pro-Lizenz** hebt das lokale Batch-Limit auf (bis zu 100 Web-Bilder pro Durchlauf) und schaltet Batch-Presets, Dateinamen-Vorlagen und ZIP-Auslieferung frei.

---

## ❤️ Support

Wenn dir ImageConv hilft, unterstütze das Projekt gerne!

**[👉 Support auf Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Offizielle Website](https://www.annmax1983.com/extensions/imageconv)**
