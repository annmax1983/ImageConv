# ImageConv

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | [Deutsch](README_de.md) | [日本語](README_ja.md) | Français

Une extension légère qui convertit des images entre les formats PNG, JPG, WEBP et AVIF — entièrement en local, sans aucun envoi de données.

> Chromium · Manifest V3 · Aucun suivi · Traitement 100 % dans le navigateur

---

## Pourquoi ImageConv ?

La plupart des outils de conversion d'images nécessitent d'envoyer vos fichiers sur un serveur distant. ImageConv fait tout dans votre navigateur grâce au Canvas API — aucune donnée ne quitte votre machine.

| Avantage | Détail |
|-----------|--------|
| 🔒 **Confidentialité avant tout** | Tout le traitement se fait en mémoire dans votre navigateur. Pas de serveurs, pas d'envoi, pas de suivi. |
| ⚡ **Conversion instantanée** | Les images de 5 Mo ou moins sont converties en moins de 500 ms. Pas d'attente liée à un aller-retour serveur. |
| 🎯 **Zéro dépendance** | Développé en JavaScript vanilla et avec les APIs natives de Chrome. Aucun framework, aucun surplus. |
| 🌍 **6 langues** | Détecte automatiquement la langue de votre navigateur — anglais, espagnol, allemand, japonais, français, chinois. |
| 📋 **Copier et enregistrer** | Clic droit sur une image pour l'enregistrer ou la copier directement dans le presse-papiers. |
| 📁 **Glisser-déposer** | Déposez des images locales sur le popup pour une conversion rapide. |

---

## Fonctionnalités

### Fonctionnalités gratuites

| Fonctionnalité | Description |
|---------|-------------|
| 🖼️ **Conversion par clic droit** | Convertissez n'importe quelle image de page web en PNG, JPG, WEBP ou AVIF via le menu contextuel |
| 📱 **Prise en charge HEIC/HEIF** | Convertissez les photos iPhone directement — glisser-déposer, coller ou clic droit. Décodage local via décodeur WASM intégré |
| 📐 **Redimensionnement** | Mise à l'échelle en pourcentage ou dimensions exactes en pixels (laisser un champ vide pour conserver les proportions). S'applique aux conversions du popup et du clic droit |
| 📋 **Copier dans le presse-papiers** | Clic droit → Copier en PNG/JPG/WEBP/AVIF — collez dans vos e-mails, conversations, documents |
| 📊 **Comparaison de taille** | Une notification affiche la taille originale vs convertie avec le pourcentage d'économie (basé sur les tailles réelles) |
| 🎚️ **Qualité ajustable** | Réglez finement la qualité d'export pour JPG, WEBP et AVIF via des curseurs dans le popup |
| 🔗 **Nettoyage intelligent des liens** | Supprime les paramètres de suivi CDN pour récupérer l'image originale |
| 🌐 **Support cross-origin** | Récupère les images depuis n'importe quel site via le Service Worker |
| 🔤 **i18n en 6 langues** | Le menu contextuel et l'interface s'adaptent automatiquement à la langue de votre navigateur |
| 🛡️ **Remplissage blanc JPG** | Remplit automatiquement les fonds transparents en blanc lors de la conversion PNG → JPG |
| ⏱️ **Anti-doublon** | Ignore les clics répétés sur la même image dans un intervalle de 2 secondes |

### Fonctionnalités Premium (licence requise)

| Fonctionnalité | Description |
|---------|-------------|
| ⭐ **Conversion par glisser-déposer** | Déposez ou collez (Ctrl+V) des images locales dans le popup pour une conversion rapide |
| 📁 **Conversion locale par lot** | Convertissez plusieurs fichiers locaux en une seule fois |

---

## Gratuit vs Premium

| | Gratuit | Premium |
|---|:---:|:---:|
| Conversion d'images par clic droit | ✅ | ✅ |
| Copier dans le presse-papiers | ✅ | ✅ |
| Ajustement de la qualité | ✅ | ✅ |
| Entrée HEIC/HEIF | ✅ | ✅ |
| Redimensionnement | ✅ | ✅ |
| Récupération d'images cross-origin | ✅ | ✅ |
| Conversion locale par glisser-déposer | — | ✅ |
| Conversion de fichiers locaux par lot | — | ✅ |

---

## Aperçu

<!-- Remplacer par de vraies captures d'écran -->
<p align="center">
  <img src="screenshots/popup.png" alt="Popup ImageConv" width="360">
</p>

<p align="center">
  <img src="screenshots/context-menu.png" alt="Menu contextuel ImageConv">
</p>

---

## Navigateurs compatibles

| Navigateur | Statut |
|---------|--------|
| Google Chrome | ✅ Entièrement pris en charge |
| Microsoft Edge | ✅ Entièrement pris en charge |
| Brave | ✅ Pris en charge |
| Opera | ✅ Pris en charge |
| Vivaldi | ✅ Pris en charge |
| Tout navigateur basé sur Chromium | ✅ Pris en charge (Manifest V3) |

---

## Installation

### Depuis les sources (mode développeur)

1. Ouvrez la page des extensions de votre navigateur :
   - **Chrome** : `chrome://extensions/`
   - **Edge** : `edge://extensions/`
2. Activez le **mode Développeur** (bouton en haut à droite)
3. Cliquez sur **Charger le package décompressé** et sélectionnez le dossier `pic-convert`
4. L'icône ✨ ImageConv apparaît dans votre barre d'outils

---

## Utilisation

### Conversion par clic droit

1. Faites un clic droit sur une image dans une page web
2. Sélectionnez **ImageConv** dans le menu contextuel
3. Choisissez **Enregistrer sous** ou **Copier sous**
4. Sélectionnez le format : PNG, JPG, WEBP ou AVIF
5. C'est fait — le fichier se télécharge instantanément, ou l'image est copiée dans le presse-papiers

### Glisser-déposer (Premium)

> ⚠️ Le glisser-déposer est une fonctionnalité Premium. Une clé de licence est requise.

1. Cliquez sur l'icône ImageConv dans votre barre d'outils pour ouvrir le popup
2. Cliquez sur le bouton 🔑 en haut à droite pour saisir votre clé de licence
3. Une fois activé, déposez un fichier image local sur la zone de dépôt
4. Sélectionnez le format cible
5. Le fichier converti se télécharge automatiquement

Vous pouvez acheter une clé de licence sur [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv).

### Réglages de qualité

Ouvrez le popup pour ajuster la qualité d'export pour JPG, WEBP et AVIF à l'aide des curseurs. Le PNG est toujours sans perte. Les réglages sont sauvegardés automatiquement.

### Redimensionnement

La section **Redimensionner** du popup prend en charge la mise à l'échelle en pourcentage (5 %–200 %) ou des dimensions exactes en pixels. Laisser un champ vide conserve les proportions. Le réglage s'applique à la fois au glisser-déposer et aux conversions par clic droit ; par défaut, la taille d'origine est conservée.

### HEIC/HEIF (photos iPhone)

Déposez des fichiers `.heic` / `.heif` dans le popup (ou convertissez un lien d'image HEIC sur une page web) pour les enregistrer en PNG/JPG/WEBP. Le décodage s'effectue entièrement en local via WASM — rien n'est envoyé sur les serveurs.

---

## Structure du menu contextuel

```
ImageConv
├── Enregistrer en PNG (Sans perte)
├── Enregistrer en JPG (Haute qualité)
├── Enregistrer en WEBP (Compact)
├── Enregistrer en AVIF (Meilleure compression)
├── Copier en PNG (Sans perte)
├── Copier en JPG (Haute qualité)
├── Copier en WEBP (Compact)
└── Copier en AVIF (Meilleure compression)
```

Les menus **Copier sous** et **Enregistrer sous** n'apparaissent que lors d'un clic droit sur une image ou un lien pointant vers un fichier image (`.png`, `.jpg`, `.jpeg`, `.webp`, `.avif`, `.gif`, `.bmp`, `.jfif`, `.svg`).

---

## Confidentialité

ImageConv a été conçu avec la confidentialité comme principe fondamental :

- ✅ **Zéro envoi de données** — Tout le traitement des images se fait en mémoire dans votre navigateur
- ✅ **Pas d'analytics** — Aucun suivi, aucune télémétrie, aucun appel distant
- ✅ **Pas de cookies** — Aucune lecture ni écriture de cookies du navigateur
- ✅ **Pas d'historique de navigation** — Aucun accès à vos données de navigation
- ✅ **Mémoire temporaire uniquement** — Les images existent en mémoire pendant la conversion et sont détruites immédiatement après
- ✅ **Permissions minimales** — Ne demande que le strict nécessaire : `contextMenus`, `downloads`, `offscreen`, `storage`, `clipboardWrite`

---

## Fonctionnement

```
Clic droit sur une image
       ↓
Le Service Worker récupère le blob de l'image (gère le cross-origin)
       ↓
Envoie le blob au document Offscreen (DOM caché avec accès Canvas)
       ↓
Le Canvas dessine l'image à sa résolution native
       ↓
Export au format cible avec la qualité spécifiée
       ↓
Renvoie une data URL → déclenche le téléchargement ou copie dans le presse-papiers
       ↓
Détruit toutes les ressources temporaires (blob, canvas, élément image)
```

> **Pourquoi Offscreen ?** Le Manifest V3 de Chrome exécute le Service Worker en arrière-plan, sans accès au DOM. Le Canvas API nécessite un DOM, on utilise donc l'API Offscreen de Chrome pour créer un document caché dédié au traitement des images.

---

## Qualité d'export par défaut

| Format | Qualité | Notes |
|--------|---------|-------|
| PNG | Sans perte | Pas de réglage de qualité — conserve toujours la qualité maximale et la transparence |
| JPG | 92 | Haute qualité, bon compromis entre taille et netteté |
| WEBP | 90 | Format moderne, ~25-35 % plus léger que le JPG à qualité équivalente |
| AVIF | 70 | Nouvelle génération, ~20-30 % plus léger que le WEBP, idéal pour le web |

Toutes les valeurs de qualité sont ajustables via les curseurs du popup (plage : 10–100).

> ℹ️ L'AVIF est produit par un encodeur WASM intégré (le Canvas de Chromium ne peut pas encoder nativement l'AVIF). Les images trop grandes (plus de 25 mégapixels) sont automatiquement converties en WEBP avec une notification.

---

## Avertissement relatif au droit d'auteur

Cette extension fournit uniquement une fonction de conversion de format d'image en local pour le traitement personnel et hors ligne des utilisateurs. Toutes les images, photos et ressources graphiques des pages web appartiennent à leurs propriétaires respectifs. Les utilisateurs ne doivent pas utiliser les images converties à des fins de reproduction commerciale, de distribution non autorisée, de création dérivée ou de toute autre activité portant atteinte au droit d'auteur. Toute responsabilité juridique découlant d'une utilisation inappropriée incombe exclusivement à l'utilisateur.

## Rappel sur les images cross-origin

La fonction de récupération d'images cross-origin est uniquement utilisée pour obtenir des ressources images en vue d'une conversion de format en local. Il est interdit d'utiliser cette fonction pour extraire massivement des images de sites web, ce qui pourrait enfreindre les règles d'accès du site concerné.

---

## Avis sur le code source

> ⚠️ **Ce dépôt ne publie pas le code source.** Il contient uniquement la documentation d'utilisation, les notes de version et les ressources d'assistance. L'extension est distribuée exclusivement via le Chrome Web Store. Aucun package d'installation hors ligne ni code source destiné aux utilisateurs finaux n'est fourni.

---

## Licence

Copyright © 2026 ImageConv. Tous droits réservés.

### Fonctionnement des licences

ImageConv utilise un système de licence basé sur l'appareil :

1. **Achetez** une clé de licence sur [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activez** en cliquant sur le bouton 🔑 du popup et en saisissant votre clé
3. La clé est liée à votre appareil (empreinte matérielle) — une clé, un appareil
4. La licence est validée en ligne toutes les 24 heures ; fonctionne hors ligne jusqu'à 7 jours

### Gratuit vs Payant

| Fonctionnalité | Gratuit | Premium |
|---------|:----:|:-------:|
| Conversion d'images par clic droit (images web) | ✅ | ✅ |
| Enregistrer en PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copier dans le presse-papiers | ✅ | ✅ |
| Curseurs d'ajustement de qualité | ✅ | ✅ |
| Entrée HEIC/HEIF (décodage WASM) | ✅ | ✅ |
| Redimensionnement (pourcentage / pixels) | ✅ | ✅ |
| Récupération d'images cross-origin | ✅ | ✅ |
| Nettoyage intelligent des liens | ✅ | ✅ |
| Conversion locale par glisser-déposer | ❌ | ✅ |
| Conversion de fichiers locaux par lot | ❌ | ✅ |

**Résumé** : Toutes les fonctionnalités liées aux images web (enregistrer/copier par clic droit) sont **gratuites**. La conversion de fichiers locaux (glisser-déposer) nécessite une **licence Premium**.

---

## ❤️ Soutenir

Si ImageConv vous est utile, n'hésitez pas à soutenir le projet !

**[👉 Soutenir sur Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Site officiel](https://www.annmax1983.com/extensions/imageconv)**
