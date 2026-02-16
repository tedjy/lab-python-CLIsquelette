# monprojet — Squelette Python prêt à coder

Un **starter kit** simple et propre pour démarrer rapidement un projet Python : point d’entrée clair, configuration séparée du code, logs propres, structure “core” pour la logique métier, et tests de base.

---

## Installation (Windows)

### 1) Créer et activer l’environnement virtuel

```powershell
py -m venv .venv
.venv\Scripts\activate
```
### 2) Mettre à jour pip + installer les dépendances de base
```powershell
py -m pip install -U pip
pip install pytest
```

# Lancer le programme

## Le projet est conçu pour être lancé en tant que module (meilleure pratique pour éviter les problèmes d’imports).

### Option A — Lancer main.py en module
```powershell
py -m monprojet.main
```
### Option B — Lancer le package (si monprojet/__main__.py existe)
```powershell
py -m monprojet
```

# Arborescence du projet
```powershell
monprojet/
├─ src/
│  └─ monprojet/
│     ├─ __init__.py
│     ├─ __main__.py        # permet: py -m monprojet
│     ├─ main.py            # point d’entrée du programme
│     ├─ cli.py             # commandes & options (help, scan, check…)
│     ├─ logging_conf.py    # configuration des logs (console + fichier)
│     ├─ core/              # logique métier (ce que fait l’outil)
│     │  ├─ __init__.py
│     │  └─ ...
│     └─ config.yaml        # configuration (non sensible)
├─ tests/
│  ├─ test_smoke.py         # tests simples (smoke test, etc.)
│  └─ ...
├─ .env                     # variables d’environnement (à ignorer dans git)
├─ README.md
└─ pyproject.toml / requirements.txt (optionnel)
```
# Rôle de chaque partie

Point d’entrée (main.py) → lance le programme

Commandes / options (cli.py) → parse --help, scan, check, etc.

Config (config.yaml + .env) → paramètres sans toucher au code

Logs (logging_conf.py) → traces propres + fichier de log

Core (core/) → ta logique métier (ce que fait l’outil)

Tests (tests/) → tests simples (smoke test, etc.)