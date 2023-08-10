---
description: Comment installer le framework !
---

# Prêt pour démarrer

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

{% hint style="warning" %}
Remplacez **NOM\_DU\_PROJET** par le nom de votre projet
{% endhint %}

Saisir cette commande dans votre terminal :

```sh
composer create-project studoo/edu-framework-skeleton NOM_DU_PROJET
```

Exemple d'affichage suite à la commande :&#x20;

{% hint style="info" %}
Ce résultat est un exemple et il ne sera probablement pas le vôtre.

L'importance est d'avoir <mark style="background-color:yellow;">**les étapes suivantes :**</mark>&#x20;

#### Creating "studoo/edu-framework-skeleton"

Création d'un dossier temporaire

#### Installing "studoo/edu-framework-skeleton"

Téléchargement et installation du skeleton edu-framework

#### Created project

Création du dossier de votre projet dans votre arborescence de fichier

#### Loading composer

Lecture de votre fichier composer.json sur la partie "require" (liste des librairies)

#### Updating dependencie

Etude des dépendances de librairie (package)

#### Writing lock file&#x20;

Ecriture du fichier composer.lock pour verrouiller les versions des librairies.

#### Installing dependencie

Installation des "vendor". C'est un dossier ou l'ensemble des librairies sont installées

#### Generating autoload files

Ecriture du fichier "/vendor/autoload.php" qui inclut l'ensemble des librairies.

#### \[...]

Résultat de toutes les opérations. Des messages d'alerte concernant les mises à jour peuvent être générés dans cette section.
{% endhint %}

```shell
Creating a "studoo/edu-framework-skeleton" project at "./NOM_DU_PROJET"
Installing studoo/edu-framework-skeleton (1.0.0)
  - Downloading studoo/edu-framework-skeleton (1.0.0)
  - Installing studoo/edu-framework-skeleton (1.0.0): Extracting archive
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

#### Initialiser votre projet

Le projet vient de s'installer, la prochaine étape est d'initialiser les fichiers de configuration.

Vous devez rentrer dans votre projet, via la commande "cd"

```bash
cd NOM_DU_PROJET
```

{% hint style="warning" %}
Remplacez **NOM\_DU\_PROJET** par le nom de votre projet
{% endhint %}

Saisir cette commande dans votre terminal :

```bash
composer edu:init
```

Exemple d'affichage suite à la commande :

{% hint style="info" %}
Ce résultat est un exemple et il ne sera probablement pas le vôtre.

L'importance est d'avoir <mark style="background-color:yellow;">**les étapes suivantes :**</mark>&#x20;

* Création du fichier ".env" si celui n'est pas déjà présent.
{% endhint %}

```bash
> php -r "file_exists('.env') || copy('.env.example', '.env');"
```

Nous verrons plus tard comment configurer ce fichier ".env" qui se trouve à la racine de votre projet.

{% hint style="danger" %}
Le fichier ".env" est **obligatoire** pour le bon fonctionnement du framework
{% endhint %}

Si vous démarrez votre serveur applicatif <mark style="background-color:yellow;">sans le fichier ".env"</mark> (Dotenv), voici le message d'erreur :

```
Fatal error: Uncaught Dotenv\Exception\InvalidPathException: 
Unable to read any of the environment file(s) at [...]
```
