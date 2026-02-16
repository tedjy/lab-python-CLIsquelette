Voici un squelette en python deja preparer pour commencer a coder un projet

 Install environement variables :

- py -m venv .venv 
- .venv\Scripts\activate 
-  py -m pip install -U pip 
- pip install pytest 

Pour lancer le programme faire appel a main.py en faisant 
- py -m monprojet.main

grace a (__main__.py)

arborescence du projet 

Point d’entrée (main.py) → lance le programme Commandes / options (cli.py) → parse --help, scan, check, etc. Config (config.yaml + .env) → paramètres sans toucher au code Logs (logging_conf.py) → traces propres + fichier log Core (core/) → ta logique métier (ce que fait l’outil) Tests (tests/) → tests simples (smoke test, etc.)

