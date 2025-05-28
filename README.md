# Gnotes

Un éditeur de texte open-source conçu avec Python (avec `customtkinter`), utile pour tout type d'usage. Il propose une interface ergonomique, des fonctionnalités utiles, une prise en charge multi-fichiers, des thèmes personnalisables, un mode lecture seule, des plugins dynamiques, des profils d'utilisateur et bien plus.

## ✨ Fonctionnalités principales

- ✅ Interface moderne 
  
- 🗂️ Multi-onglets avec gestion complète des fichiers
- ⏳ Sauvegarde 
- 🔌 Plugins dynamiques (fichiers `.py` dans `/plugins`)
- 🔒 Mode lecture seule par onglet ou global (avec fond grisé + icône)
- 📦 Système de packaging multi-plateforme (AppImage, .deb, .exe, .zip)

---

## 📦 Installation

### 🐍 Prérequis

- Python 3.9+
- `pip install -r requirements.txt`

### 🪟 Windows

pas d'installation, 
il faudra juste décompresser l'archive .zip et double cliquer sur 'Gnotes.exe'

### 🐧Linux (.deb ou AppImage)

make deb        # génère un .deb
make appimage   # génère un .AppImage

### 🍎 macOS (.app)
make macos-app

🌐 Version portable (ZIP)
make zip

📁 Structure du projet

📦 Bloc-notes-Professionnel/
├── main.py                      # Point d'entrée principal
├── core/                        # Fonctionnalités internes
├── ui/                          # Composants UI
├── themes/                      # Thèmes JSON
├── plugins/                     # Plugins dynamiques
├── profiles/                    # Profils d’utilisateur
├── build-scripts/               # Scripts de build (.sh, .iss, .deb)
├── assets/                      # Icônes, images
├── README.md                    # Ce fichier
├── LICENSE                      # Licence MIT
├── Makefile                     # Automatisation cross-platform
└── requirements.txt             # Dépendances Python


🛠️ Développement
Raccourcis utiles (make)
bash
Copier
Modifier
make run            # Lancer l’application
make zip            # Créer une version portable
make windows        # Build InnoSetup pour Windows
make deb            # Build Debian (.deb)
make appimage       # Build Linux AppImage
make macos-app      # Build app MacOS
make release        # Build tout + push vers GitHub release

🧩 Créer un plugin
Ajoutez un fichier .py dans /plugins/ avec une fonction register(app) :

def register(app):
    print("Plugin chargé")
    # Ajouter des fonctionnalités ici

## Ajouter un bouton à la barre d’outils (exemple de plugin)

```python
def load(app, toolbar):
    def custom_action():
        print("Action personnalisée")

    toolbar.add_button(
        icon_path="assets/icons/custom.png",
        command=custom_action,
        tooltip="Bouton personnalisé"
    )


Raccourcis utiles (make)
bash
Copier
Modifier
make run            # Lancer l’application
make zip            # Créer une version portable
make windows        # Build InnoSetup pour Windows
make deb            # Build Debian (.deb)
make appimage       # Build Linux AppImage
make macos-app      # Build app MacOS
make release        # Build tout + push vers GitHub release

🧩 Créer un plugin
Ajoutez un fichier .py dans /plugins/ avec une fonction register(app) :

def register(app):
    print("Plugin chargé")
    # Ajouter des fonctionnalités ici

## Ajouter un bouton à la barre d’outils (exemple de plugin)


def load(app, toolbar):
    def custom_action():
        print("Action personnalisée")

    toolbar.add_button(
        icon_path="assets/icons/custom.png",
        command=custom_action,
        tooltip="Bouton personnalisé"
    )


Forkez le projet

Créez une branche (git checkout -b feature/ma-fonction)

Commitez vos modifications (git commit -m 'Ajout d’une fonctionnalité')

Poussez la branche (git push origin feature/ma-fonction)

Ouvrez une Pull Request 🚀

📫 Contact
Créateur : Nathan Varin
Email : Nathan.varin@outlook.fr
GitHub : M31-p
