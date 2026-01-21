# Boks Key Extractor 📦

Une application web simple et sécurisée pour extraire vos clés privées (Configuration Key & BLE Code) à partir des fichiers de données de l'application Boks (iOS ou Android).

🔗 **[Utiliser l'application en ligne](https://votre-username.github.io/boks-extractor)** (Lien à activer via GitHub Pages)

## 🔒 Confidentialité & Sécurité
Cette application s'exécute **intégralement en local** dans votre navigateur.
- Aucun fichier n'est envoyé sur un serveur.
- Aucune donnée ne quitte votre ordinateur.
- Vous pouvez couper votre connexion internet avant d'utiliser l'outil pour plus de sûreté.

## 🚀 Comment l'utiliser ?

1. **Ouvrez** le fichier `index.html` (ou le site web si hébergé).
2. **Glissez-déposez** le dossier ou le fichier contenant les données de l'app Boks :
    *   **iOS** : Glissez le dossier contenant `IndexedDB.sqlite3`.
    *   **Android** : Glissez le dossier contenant les fichiers `.ldb` ou `.log`.
3. L'outil scanne automatiquement les fichiers et affiche vos clés :
    *   🔑 **Configuration Key**
    *   📡 **BLE Code**

## 📂 Où trouver mes fichiers ?

### iOS (iPhone)
Si vous avez fait un backup de votre iPhone, cherchez dans :
`AppDomain-com.boks.app/Library/WebKit/WebsiteData/Default/.../IndexedDB/`

### Android
Si vous avez accès aux données (root ou backup adb), cherchez dans :
`/data/data/com.boks.app/app_webview/Default/IndexedDB/`

## 🛠 Technique
L'outil utilise l'API `FileReader` et `Uint8Array` de JavaScript pour scanner les fichiers binaires bruts et rechercher les séquences d'octets spécifiques (en UTF-16LE et UTF-8) correspondant aux clés de configuration, tout en ignorant les faux-positifs.

## Licence
MIT
