# Prêt pour démarrer

### Prérequis

Voici la liste des éléments nécessaires pour assurer le bon déroulement du projet.

| Service  | Version |
| -------- | ------- |
| PHP      | ^8.0    |
| Composer | ^2.0    |
| GIT      |         |

### Installation

L'installation va se faire en ligne de commande via un terminal (git-bash, iterm, warp, tabby ...)

#### Choisir son emplacement de projet

Utilisez la commande "cd" pour naviguer dans votre arborescence de fichiers et sélectionner l'emplacement de votre projet.

```bash
cd NOM_DU_DOSSIER // pour avancer dans votre arboresence
cd .. // pour reculer
pwd // pour savoir ou vous êtes dans votre arboresence
```

#### Création du projet

Nous allons créer le projet à l'aide du gestionnaire de paquets "composer". Cette étape vous permettra de construire la base du projet en une seule ligne de commande.

```sh
composer create-project studoo/edu-framework-skeleton NOM_DU_PROJET
```

{% hint style="warning" %}
Remplacez **NOM\_DU\_PROJET** par le nom de votre projet
{% endhint %}

Résultat :&#x20;

```shell
Creating a "studoo/edu-framework-skeleton" project at "./NOM_DU_PROJET"
Installing studoo/edu-framework-skeleton (x.0.0)
  - Downloading studoo/edu-framework-skeleton (x.0.0)
  - Installing studoo/edu-framework-skeleton (x.0.0): Extracting archive
Created project in /Users/redbull/Projects/studoo/NOM_DU_PROJET
Loading composer repositories with package information
Updating dependencies
Lock file operations: 9 installs, 0 updates, 0 removals
  - Locking graham-campbell/result-type (1.1.x-dev 60c5f57)
  - Locking nikic/fast-route (v1.x-dev 4012884)
  - Locking phpoption/phpoption (dev-master dd3a383)
  - Locking studoo/edu-framework (dev-main c5cd9c5)
  - Locking symfony/polyfill-ctype (1.x-dev ea208ce)
  - Locking symfony/polyfill-mbstring (1.x-dev 42292d9)
  - Locking symfony/polyfill-php80 (1.x-dev 6caa573)
  - Locking twig/twig (3.x-dev fea9dfc)
  - Locking vlucas/phpdotenv (dev-master 1a7ea2a)
Writing lock file
Installing dependencies from lock file (including require-dev)
Package operations: 9 installs, 0 updates, 0 removals
  - Installing symfony/polyfill-php80 (1.x-dev 6caa573): Extracting archive
  - Installing symfony/polyfill-mbstring (1.x-dev 42292d9): Extracting archive
  - Installing symfony/polyfill-ctype (1.x-dev ea208ce): Extracting archive
  - Installing phpoption/phpoption (dev-master dd3a383): Extracting archive
  - Installing graham-campbell/result-type (1.1.x-dev 60c5f57): Extracting archive
  - Installing vlucas/phpdotenv (dev-master 1a7ea2a): Extracting archive
  - Installing twig/twig (3.x-dev fea9dfc): Extracting archive
  - Installing nikic/fast-route (v1.x-dev 4012884): Extracting archive
  - Installing studoo/edu-framework (dev-main c5cd9c5): Extracting archive
Generating autoload files
7 packages you are using are looking for funding.
Use the `composer fund` command to find out more!
No security vulnerability advisories found
```

#### Initaliser votre projet

TODO : Explication

```bash
composer edu:init
```

### Démarrer le serveur applicatif

TODO : Erreur + explication

```
composer edu:start
```
