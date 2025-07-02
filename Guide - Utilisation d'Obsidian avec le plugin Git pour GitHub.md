
---
## Introduction

Le plugin **Git** pour Obsidian permet de synchroniser automatiquement vos notes avec un dépôt Git (comme GitHub). Cela ajoute une gestion de version à vos fichiers Markdown : chaque modification est historisée, sauvegardée à distance et peut être partagée avec d’autres utilisateurs. C’est un outil puissant pour travailler de manière structurée et collaborative dans Obsidian.

Dans le cadre de **SONIA**, ce système nous permet de centraliser **la documentation, les fichiers de travail et les procédures** dans un espace commun. Chaque membre peut ainsi contribuer, retrouver l’historique des modifications et toujours accéder à la dernière version des documents, même depuis une autre machine.

> **Si vous êtes un nouvel utilisateur et que le dépôt GitHub a déjà été créé pour vous**, vous n’avez pas besoin de faire les étapes 1 (création du dépôt) et 3 (création du token). Vous pouvez passer directement aux étapes de clonage et de configuration du plugin.

---
## Étape 1 : Créer un dépôt sur GitHub

1. Allez sur [github.com](https://github.com/).
2. Cliquez sur le profil du compte ELE > **Repositories** > **New**.
3. Remplissez les champs :
	- **Repository name** : `ELEVault`
    - **Description** : `ELEVault`
	- Cochez **Add a README file**.
4. Cliquez sur **Create repository**.

---
## Étape 2 : Installer Git

1. Téléchargez Git depuis [git-scm.com](https://git-scm.com/).
2. Lancez l’installation.
3. Suivez les instructions par défaut.

>  Ici ajouter qu'il faut mettre l'ouverture des fichier avec VSCode mais je sais plus ou c'est dans l'instalation

4. Une fois installé, ouvrez un terminal et entrez :

```bash
git --version
```

>  Vous devriez voir un numéro de version si l'installation a réussi.

---
## Étape 3 : Créer un Personal Access Token sur GitHub

1. GitHub > **Settings** > **Developer settings** > **Personal access tokens** > **Tokens (classic)**.
2. Cliquez sur **Generate new token**.
3. Remplissez les champs :
    - **Note** : `token`
    - **Expiration** : `No expiration`
    - **Scopes** : cochez **repo** uniquement.
4. Cliquez sur **Generate token**.
5. **Copiez et conservez** le token généré en lieu sûr et surtout ne jamais le mettre dans un fichier qui va etre push dans le GitHub sinon enorme bug infernale.

---
## Étape 4 : Installer le plugin Git dans Obsidian

1. Ouvrez Obsidian.
2. Allez dans **Settings** > **Community plugins** > **Browse**.
3. Cherchez **Git**, installez-le et activez-le (**Enable**).

---
## Étape 5 : Cloner le dépôt GitHub dans Obsidian

1. Créez un nouveau dossier dans Obsidian via **New Folder** : `ELEVault`.
2. Appuyez sur `Ctrl+P` pour ouvrir la palette de commandes.
3. Tapez et sélectionnez **Git: Clone an existing remote repo**.
4. Remplissez :
    - **Remote URL** : `https://<TOKEN>@github.com/<UTILISATEUR>/<REPO>.git`
    - **Directory for clone** : `ELEVault`
    - **Depth of clone** : appuyez simplement sur `Enter`.
5. Vérifiez à droite de l’écran qu’**aucune erreur** ne s’est produite.
6. Fermez puis rouvrez Obsidian. Vous devriez voir tous les fichiers du dépôt.

>  Si vous êtes un nouvel utilisateur, demandez à votre représentant ELE de vous fournir l'URL du dépôt à utiliser.

---
## Étape 6 : Faire un premier commit/push

1. Faites une petite modification dans un fichier Markdown.
2. Appuyez sur `Ctrl+P`.
3. Tapez :
    - `Git: Commit all changes`
    - Puis `Git: Push`

> Vos modifications locales sont maintenant en ligne sur GitHub, aller verifier !
> Ensuite pensez bien à supprimer votre modifications.

---
## Étape 7 : Configurer le plugin Git

Dans **Settings** > **Git**, vous pouvez configurer :

- `Pull on startup` : permet de synchroniser automatiquement les modifications à chaque ouverture d’Obsidian.

---
## Étape 8 : Détail des fonctionnalités du plugin Git

Voici quelques commandes utiles disponibles dans Obsidian grace au plugin Git :

| Commande Git (Ctrl+P)                         | Description                                                                                                         |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `Git : Commit`                                | Si des fichiers sont "staged", seuls ceux-ci seront commités ; sinon, commit uniquement les fichiers modifiés.      |
| `Git : Commit all changes`                    | Commit tous les changements sans les pousser.                                                                       |
| `Git : Commit-and-sync`                       | Commit tous les changements, puis fait un pull et un push.                                                          |
| `Git : Commit-and-sync with specific message` | Identique à ci-dessus, mais permet de personnaliser le message de commit.                                           |
| `Git : Commit-and-sync and close`             | Identique à `Commit-and-sync`, mais ferme la fenêtre Obsidian (ordinateur uniquement, ne ferme pas l’appli mobile). |
| `Git : Push` / `Pull`                         | Envoie (push) ou récupère (pull) les changements vers/depuis GitHub.                                                |
| `Git : Clone an existing remote repo`         | Ouvre une boîte de dialogue pour cloner un dépôt distant (URL + authentification).                                  |
| `Git : Open file on GitHub`                   | Ouvre le fichier actuel sur GitHub dans le navigateur (fonctionne uniquement sur ordinateur).                       |
| `Git : Open file history on GitHub`           | Ouvre l'historique du fichier actuel sur GitHub dans le navigateur (fonctionne uniquement sur ordinateur).          |

---
Corentin Coueron 2025-07-02