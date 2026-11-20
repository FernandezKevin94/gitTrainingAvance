HOOK PRE-COMMIT – GIT

1. Présentation

Ce hook pre-commit permet de demander à l'utilisateur s'il souhaite enregistrer une information de suivi lors d'un commit.

2. Fonctionnement

Lors de chaque commit, une question est affichée :

"Sauvegarde de la base dans ce commit (y/[n]) ?"

- Si l'utilisateur répond "y" : le dossier suivi est créé si nécessaire, puis le fichier suivi/commitInfo.txt est généré avec la date et l'heure du commit. Ce fichier est automatiquement ajouté au commit.
- Si l'utilisateur répond "n" ou appuie sur Entrée : le commit continue normalement, sans créer de fichier de suivi.

3. Installation

Pour installer le hook dans un dépôt Git :

- Copier le fichier hooks/pre-commit dans le dossier .git/hooks/ du dépôt.
- Vérifier que le fichier est exécutable.

Exemple avec Git Bash :

cp hooks/pre-commit .git/hooks/pre-commit
chmod +x .git/hooks/pre-commit

4. Prérequis

- Git installé.
- Bash disponible (par exemple Git Bash sous Windows).
