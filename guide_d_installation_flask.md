# 🚀 Guide d'Installation et de Prise en Main : Flask sur Windows 11

Ce document récapitule les étapes nécessaires pour configurer un environnement virtuel Python et exécuter une application web avec le framework **Flask**.

---

## 📋 1. Prérequis

- **Python 3.x** installé sur Windows 11.
- **Visual Studio Code (VS Code)** comme éditeur de code.

---

## ⚙️ 2. Configuration du Projet et de l'Environnement Virtuel

Ouvre le terminal intégré dans VS Code (`Ctrl` + `~`) au niveau du dossier du projet, puis exécute les commandes suivantes :

### Étape A : Créer l'environnement virtuel (`venv`)
```bash
python -m venv venv
```

### Étape B : Activer l'environnement virtuel (Windows)
Sous **PowerShell** ou **Invite de commandes (CMD)** :
```bash
venv\Scripts\activate
```
> 💡 *Note : Un indicateur `(venv)` apparaît au début de la ligne de commande, confirmant l'activation.*

---

## 📦 3. Installation de Flask

Une fois l'environnement virtuel actif, installe Flask avec `pip` :

```bash
pip install flask
```

---

## 📝 4. Création d'un Fichier Application Minimal (`app.py`)

Créer un fichier nommé `app.py` à la racine du projet avec le code suivant :

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, Flask fonctionne parfaitement !"

if __name__ == '__main__':
    app.run(debug=True)
```

---

## ▶️ 5. Lancement de l'Application

Dans le terminal (avec `(venv)` toujours actif), démarre le serveur de développement :

```bash
python app.py
```

Accède ensuite à l'application depuis un navigateur web à l'adresse suivante :
👉 [`http://127.0.0.1:5000`](http://127.0.0.1:5000)

---

## 📂 6. Structure Recommandée pour un Projet Flask (CRUD)

```text
mon_projet_flask/
├── venv/                # Environnement virtuel (à ajouter au .gitignore)
├── static/              # Fichiers statiques (CSS, JavaScript, images)
├── templates/           # Templates HTML (utilisés par Jinja2)
│   └── index.html
├── app.py               # Script principal (routes et logique)
├── .gitignore           # Fichier spécifiant les éléments à ignorer par Git
└── README.md            # Documentation du projet
```

---

## 🐙 7. Commandes Utiles pour Git

Pour sauvegarder le travail sur un dépôt GitHub distant :

```bash
git add README.md app.py
git commit -m "Ajout du guide d'installation Flask et du serveur de test"
git push origin main
```