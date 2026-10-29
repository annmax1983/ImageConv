# ImageConv

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | [Deutsch](README_de.md) | [日本語](README_ja.md) | Français

Une extension légère qui convertit des images entre les formats PNG, JPG, WEBP et AVIF — entièrement en local, sans aucun envoi de données.

> Chrome / Edge / Firefox · Manifest V3 · Aucun suivi · Traitement 100 % dans le navigateur

---

## Pourquoi ImageConv ?

La plupart des outils de conversion d'images nécessitent d'envoyer vos fichiers sur un serveur distant. ImageConv fait tout dans votre navigateur grâce au Canvas API — aucune image ne quitte votre navigateur.

| Avantage | Détail |
|-----------|--------|
| 🔒 **Confidentialité avant tout** | Tout le traitement se fait en mémoire dans votre navigateur. Pas d'envoi, pas de suivi. La seule requête sortante est la validation facultative de licence. |
| ⚡ **Conversion instantanée** | Les images de 5 Mo ou moins sont converties en moins de 500 ms. Pas d'attente liée à un aller-retour serveur. |
| 🎯 **Zéro dépendance** | Développé en JavaScript vanilla et avec les APIs natives de Chrome. Aucun framework, aucun surplus. |
| 🌍 **6 langues** | Détecte automatiquement la langue de votre navigateur — anglais, espagnol, allemand, japonais, français, chinois. |
| 📋 **Copier et enregistrer** | Clic droit sur une image pour l'enregistrer ou la copier directement dans le presse-papiers. |
| 📁 **Glisser-déposer** | Déposez des images locales sur le popup pour une conversion rapide. |
| 🖼️ **Export par lots** | Liste toutes les images déjà chargées d'une page, vous choisissez celles à garder et les exportez d'un coup. |

---

## Fonctionnalités

### Fonctionnalités gratuites

| Fonctionnalité | Description |
|---------|-------------|
| 🖼️ **Conversion par clic droit** | Convertissez n'importe quelle image de page web en PNG, JPG, WEBP ou AVIF via le menu contextuel |
| 📱 **Prise en charge HEIC/HEIF** | Convertissez les photos iPhone directement — glisser-déposer, coller ou clic droit. Décodage local via décodeur WASM intégré |
| 📐 **Redimensionnement** | Mise à l'échelle en pourcentage ou dimensions exactes en pixels (laisser un champ vide pour conserver les proportions). S'applique aux conversions du popup et du clic droit |
| 📋 **Copier dans le presse-papiers** | Clic droit → Copier en PNG — collez dans vos e-mails, conversations, documents |
| 📊 **Comparaison de taille** | Une notification affiche la taille originale vs convertie avec le pourcentage d'économie (basé sur les tailles réelles) |
| 🎚️ **Qualité ajustable** | Réglez finement la qualité d'export pour JPG, WEBP et AVIF via des curseurs dans le popup |
| 🔗 **Nettoyage intelligent des liens** | Supprime les paramètres de suivi CDN pour récupérer l'image originale |
| 🌐 **Support cross-origin** | Récupère les images depuis n'importe quel site via le Service Worker |
| 🔤 **i18n en 6 langues** | Le menu contextuel et l'interface s'adaptent automatiquement à la langue de votre navigateur |
| 🛡️ **Remplissage blanc JPG** | Remplit automatiquement les fonds transparents en blanc lors de la conversion PNG → JPG |
| ⏱️ **Anti-doublon** | Ignore les clics répétés sur la même image dans un intervalle de 2 secondes |

### Fonctionnalités Pro (licence requise)

| Fonctionnalité | Description |
|---------|-------------|
| ♾️ **Conversion locale par lots illimitée** | Les dépôts multiples gratuits convertissent jusqu'à 5 fichiers par exécution ; Pro supprime la limite locale |
| 📦 **Exports web volumineux** | Exportez jusqu'à 100 images d'une page en une seule exécution (gratuit : 5) |
| 🗜️ **Export en archive ZIP** | Regroupez un lot web dans un seul fichier `.zip`. Si l'empaquetage échoue ou si l'archive dépasse 4 Go, les images terminées sont enregistrées individuellement |
| 🗂️ **Préréglages de lot** | Enregistrez jusqu'à 12 préréglages format/qualité/redimensionnement dans la boîte de dialogue Options du lot et réappliquez-les en un clic |
| 🏷️ **Modèles de nom de fichier** | Nommez les téléchargements web par lots avec `{name}`, `{index}`, `{format}`, `{date}`, `{width}` et `{height}`. L'extension est ajoutée automatiquement et les collisions reçoivent `-2`, `-3` |

La modification du format, de la qualité et du redimensionnement dans la boîte de dialogue Options du lot reste gratuite. Les préréglages, le nommage des fichiers et la livraison ZIP sont Pro et s'appliquent à la page d'export par lots, pas au glisser-déposer du popup.

---

## Gratuit vs Pro

| | Gratuit | Pro |
|---|:---:|:---:|
| Conversion d'images par clic droit | ✅ | ✅ |
| Copier dans le presse-papiers | ✅ PNG uniquement | ✅ PNG uniquement |
| Ajustement de la qualité | ✅ | ✅ |
| Entrée HEIC/HEIF | ✅ | ✅ |
| Redimensionnement | ✅ | ✅ |
| Récupération d'images cross-origin | ✅ | ✅ |
| Glisser-déposer / coller des images locales | ✅ Jusqu’à 5 fichiers | ✅ Illimité |
| Conversion de fichiers locaux par lot | Jusqu'à 5 par exécution | Illimitée |
| Exporter les images d'une page web | Jusqu'à 5 par exécution | Jusqu'à 100 par exécution |
| Format / qualité / redimensionnement du lot | ✅ | ✅ |
| Préréglages de lot | — | ✅ Jusqu'à 12 |
| Modèles de nom de fichier (page de lot) | — | ✅ |
| Livraison en archive ZIP (page de lot) | — | ✅ |

---

## Aperçu

<!-- Remplacer par de vraies captures d'écran -->
<p align="center">
  <img src="../screenshots/popup.png" alt="Popup ImageConv" width="360">
</p>

<p align="center">
  <img src="../screenshots/context-menu.png" alt="Menu contextuel ImageConv">
</p>

---

## Navigateurs compatibles

| Navigateur | Statut |
|---------|--------|
| Google Chrome | ✅ Entièrement pris en charge |
| Microsoft Edge | ✅ Entièrement pris en charge |
| Mozilla Firefox | ✅ Entièrement pris en charge |
| Brave | ✅ Pris en charge |
| Opera | ✅ Pris en charge |
| Vivaldi | ✅ Pris en charge |
| Tout navigateur basé sur Chromium | ✅ Pris en charge (Manifest V3) |

> **Note Firefox :** Firefox ne propose pas de document offscreen, le pipeline de conversion s'exécute dans le script d'arrière-plan ; la version Firefox ne demande donc pas la permission `offscreen`. Le reste des fonctions se comporte comme sous Chrome / Edge.

---

## Installation

| Store | Lien |
|---|---|
| Chrome Web Store | [Installer dans Chrome](https://chromewebstore.google.com/detail/jfeigfbfnciialfkdfjeofmkhofidehp) |
| Microsoft Edge Add-ons | [Installer dans Edge](https://microsoftedge.microsoft.com/addons/detail/fdjbckphkemnkgljgoongejilpepjpbp) |
| Modules complémentaires Firefox (AMO) | 🔜 En cours d'examen — le lien sera ajouté après publication |

> Installez uniquement depuis les boutiques officielles ci-dessus — évitez les sites de téléchargement tiers.

---

## Utilisation

### Conversion par clic droit

1. Faites un clic droit sur une image dans une page web
2. Sélectionnez **ImageConv** dans le menu contextuel
3. Choisissez **Enregistrer sous** (PNG/JPG/WEBP/AVIF) ou **Copier en PNG**
4. C'est fait — le fichier se télécharge instantanément, ou l'image est copiée dans le presse-papiers en PNG

### Glisser-déposer / Coller (gratuit)

1. Cliquez sur l'icône ImageConv dans votre barre d'outils pour ouvrir le popup
2. Déposez un fichier image local sur la zone de dépôt, ou collez-le avec Ctrl+V
3. Sélectionnez le format cible
4. Le fichier converti se télécharge automatiquement

Les images seules sont toujours gratuites. Dans la version gratuite, déposer plusieurs fichiers convertit les 5 premiers ; une licence Pro supprime cette limite par exécution. Les préréglages de lot, les modèles de nom de fichier et la livraison ZIP ne sont disponibles que sur la page d'export par lots web, pas dans le glisser-déposer du popup.

### Export par lots des images web (gratuit 5, Pro 100)

1. Ouvrez la page dont vous voulez exporter les images (elles doivent déjà être chargées)
2. Cliquez sur l'icône ImageConv, puis sur **Exporter les images de cette page**
3. Un nouvel onglet liste toutes les images trouvées, de la plus grande à la plus petite — cochez celles voulues
4. Cliquez sur **Options** pour définir le format, la qualité et le redimensionnement. Tout le monde peut les modifier ; Pro peut en plus appliquer ou enregistrer un préréglage, modifier le modèle de nom de fichier et choisir **Une archive ZIP** sous Livraison
5. Cliquez sur **Exporter la sélection** (le bouton devient **Exporter ZIP** lorsque la livraison ZIP est active)

Les fichiers individuels sont téléchargés dans `ImageConv/` selon le modèle de nom. Les exécutions ZIP téléchargent un `ImageConv/<host>-YYYYMMDD-HHmm.zip` ; si l'empaquetage échoue ou si l'archive dépasse 4 Go, les images terminées sont enregistrées individuellement.

Les images de moins de 100 px sont masquées par défaut (icônes, avatars, pixels de suivi) — ajustez le filtre dans la barre d'outils. La version gratuite exporte jusqu'à 5 images par exécution ; Pro porte la limite à 100.

### Réglages de qualité

Ouvrez le popup pour ajuster la qualité d'export pour JPG, WEBP et AVIF à l'aide des curseurs. Le PNG est toujours sans perte. Les réglages sont sauvegardés automatiquement.

### Redimensionnement

La section **Redimensionner** du popup prend en charge la mise à l'échelle en pourcentage (5 %–200 %) ou des dimensions exactes en pixels. Laisser un champ vide conserve les proportions. Le réglage s'applique à la fois au glisser-déposer et aux conversions par clic droit ; par défaut, la taille d'origine est conservée.

### HEIC/HEIF (photos iPhone)

Déposez ou collez des fichiers `.heic` / `.heif` dans le popup, ou faites un clic droit sur une image HEIC affichée sur une page, pour l'enregistrer en PNG/JPG/WEBP. Le décodage s'effectue entièrement en local via WASM — rien n'est envoyé sur les serveurs. L'entrée HEIC est gratuite dans toutes les versions.

---

## Structure du menu contextuel

- Enregistrer en PNG (Sans perte)
- Enregistrer en JPG (Haute qualité)
- Enregistrer en WEBP (Compact)
- Enregistrer en AVIF (Meilleure compression)
- Copier en PNG (Sans perte)

Les menus **Enregistrer sous** et **Copier en PNG** n'apparaissent que lors d'un clic droit sur une image, y compris une image à l'intérieur d'un lien. Les liens simples vers des fichiers image n'affichent pas le menu. La sortie vers le presse-papiers est uniquement en PNG.

---

## Confidentialité

ImageConv a été conçu avec la confidentialité comme principe fondamental :

- ✅ **Zéro envoi de données** — Tout le traitement des images se fait en mémoire dans votre navigateur
- ✅ **Pas d'analytics** — Aucun suivi, aucune télémétrie. La seule requête sortante est la validation de licence (clé de licence + un identifiant d'installation aléatoire) lors de l'activation ou quand la vérification en cache de 2 h expire — les données d'image ne sont jamais transmises
- ✅ **Pas de cookies** — Aucune lecture ni écriture de cookies du navigateur
- ✅ **Pas d'historique de navigation** — Aucun accès à vos données de navigation
- ✅ **Mémoire temporaire uniquement** — Les images existent en mémoire pendant la conversion et sont détruites immédiatement après
- ✅ **Permissions minimales** — Uniquement ce dont chaque fonction a besoin : `contextMenus`, `downloads`, `offscreen`, `storage`, `scripting`, `clipboardWrite`, plus `<all_urls>` pour récupérer l'image cliquée et analyser une page pour l'export par lots

---

## Fonctionnement

1. Faites un clic droit sur une image et choisissez le format cible.
2. L'image est récupérée puis décodée dans votre navigateur, y compris depuis des sources cross-origin.
3. Elle est reconstruite à sa résolution native, puis encodée en PNG, JPG, WEBP ou AVIF à la qualité que vous avez réglée.
4. Le résultat se télécharge ou se dépose dans votre presse-papiers, et toutes les ressources temporaires sont libérées aussitôt.

---

## Qualité d'export par défaut

| Format | Qualité | Notes |
|--------|---------|-------|
| PNG | Sans perte | Pas de réglage de qualité — conserve toujours la qualité maximale et la transparence |
| JPG | 92 | Haute qualité, bon compromis entre taille et netteté |
| WEBP | 90 | Format moderne, ~25-35 % plus léger que le JPG à qualité équivalente |
| AVIF | 70 | Nouvelle génération, ~20-30 % plus léger que le WEBP, idéal pour le web |

Toutes les valeurs de qualité sont ajustables via les curseurs du popup (plage : 10–100).

> ℹ️ L'AVIF est produit par un encodeur WASM intégré (le Canvas du navigateur ne peut pas encoder nativement l'AVIF). Les images trop grandes (plus de 25 mégapixels) sont automatiquement converties en WEBP avec une notification.

---

## Avertissement relatif au droit d'auteur

Cette extension fournit uniquement une fonction de conversion de format d'image en local pour le traitement personnel et hors ligne des utilisateurs. Toutes les images, photos et ressources graphiques des pages web appartiennent à leurs propriétaires respectifs. Les utilisateurs ne doivent pas utiliser les images converties à des fins de reproduction commerciale, de distribution non autorisée, de création dérivée ou de toute autre activité portant atteinte au droit d'auteur. Toute responsabilité juridique découlant d'une utilisation inappropriée incombe exclusivement à l'utilisateur.

## Rappel sur les images cross-origin

La fonction de récupération d'images cross-origin est uniquement utilisée pour obtenir des ressources images en vue d'une conversion de format en local. Il est interdit d'utiliser cette fonction pour extraire massivement des images de sites web, ce qui pourrait enfreindre les règles d'accès du site concerné.

---

## Avis sur le code source

> ⚠️ **Ce dépôt ne publie pas le code source.** Il contient uniquement la documentation d'utilisation, les notes de version et les ressources d'assistance. L'extension est distribuée exclusivement via le Chrome Web Store, Microsoft Edge Add-ons et Firefox Add-ons (AMO). Aucun package d'installation hors ligne ni code source destiné aux utilisateurs finaux n'est fourni.

---

## Licence

Copyright © 2026 ImageConv. Tous droits réservés.

### Fonctionnement des licences

ImageConv utilise un système de licence basé sur les activations :

1. **Achetez** une clé de licence sur [annmax1983.com](https://www.annmax1983.com/checkout.html?plugin=imageconv)
2. **Activez** en cliquant sur le bouton 🔑 du popup et en saisissant votre clé
3. Une licence couvre deux installations de navigateur ; chaque activation en lie une. Désactivez une ancienne installation dans le popup pour libérer cette place pour une nouvelle
4. La licence est validée en ligne toutes les 2 heures ; si le serveur est injoignable, la licence en cache continue de fonctionner

### Gratuit vs Payant

| Fonctionnalité | Gratuit | Pro |
|---------|:----:|:---:|
| Conversion d'images par clic droit (images web) | ✅ | ✅ |
| Enregistrer en PNG / JPG / WEBP / AVIF | ✅ | ✅ |
| Copier dans le presse-papiers | ✅ PNG uniquement | ✅ PNG uniquement |
| Curseurs d'ajustement de qualité | ✅ | ✅ |
| Entrée HEIC/HEIF (décodage WASM) | ✅ | ✅ |
| Redimensionnement (pourcentage / pixels) | ✅ | ✅ |
| Récupération d'images cross-origin | ✅ | ✅ |
| Nettoyage intelligent des liens | ✅ | ✅ |
| Glisser-déposer / coller des fichiers locaux | ✅ Jusqu’à 5 fichiers | ✅ Illimité |
| Conversion de fichiers locaux par lot | Jusqu'à 5 par exécution | Illimitée |
| Exporter les images d'une page web | Jusqu'à 5 par exécution | Jusqu'à 100 par exécution |
| Format / qualité / redimensionnement du lot | ✅ | ✅ |
| Préréglages de lot | — | ✅ Jusqu'à 12 |
| Modèles de nom de fichier (page de lot) | — | ✅ |
| Livraison en archive ZIP (page de lot) | — | ✅ |

**Résumé** : La conversion par clic droit, le glisser-déposer/collage d'une image seule, jusqu'à 5 images par exécution par lots et la modification format/qualité/redimensionnement dans la boîte de dialogue Options du lot sont **gratuits**. Une **licence Pro** supprime la limite locale par lots (jusqu'à 100 images web par exécution) et débloque les préréglages de lot, les modèles de nom de fichier et la livraison ZIP.

---

## ❤️ Soutenir

Si ImageConv vous est utile, n'hésitez pas à soutenir le projet !

**[👉 Soutenir sur Ko-fi](https://ko-fi.com/annmax?ref=imageconv)**

**[🌐 Site officiel](https://www.annmax1983.com/extensions/imageconv)**
