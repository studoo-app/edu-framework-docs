---
description: Comment démarrer le projet pour visualiser le résultat du code source installé
---

# Comment démarrer

Le code source installé via "composer" fonctionnera avec un serveur web. PHP fourni un serveur web pour développer. En production, on utilisera d'autres serveurs web comme apache, ngnix ...

### Démarrer le serveur web

Pour démarrer le serveur web, il faut obligatoirement être à la racine de votre projet. Pour le savoir voici la commande suivante :&#x20;

```bash
ls -la
```

{% hint style="info" %}
Ce résultat est un exemple et il ne sera probablement pas le vôtre.

L'importance est d'avoir <mark style="background-color:yellow;">**le fichier .env et dossiers suivants :**</mark>&#x20;

* .env
* public/
* vendor/
* app/
{% endhint %}

Exemple d'affichage suite à la commande :&#x20;

```bash
drwxr-xr-x@ 11 prof  staff    352 Aug 10 11:43 .
drwxr-xr-x  14 prof  staff    448 Aug 10 11:43 ..
-rw-r--r--@  1 prof  staff    639 Aug  9 16:50 .env
-rw-r--r--@  1 prof  staff    639 Aug  9 16:50 .env.example
-rw-r--r--@  1 prof  staff     73 Aug  9 16:50 .gitignore
-rw-r--r--@  1 prof  staff   1073 Aug  9 16:50 LICENSE
-rw-r--r--@  1 prof  staff   1465 Aug  9 16:50 README.md
drwxr-xr-x@  4 prof  staff    128 Aug  9 16:50 app
-rw-r--r--@  1 prof  staff    795 Aug  9 16:50 composer.json
-rw-r--r--@  1 prof  staff  23822 Aug 10 11:43 composer.lock
drwxr-xr-x@  3 prof  staff     96 Aug  9 16:50 public
drwxr-xr-x@ 11 prof  staff    352 Aug 10 11:43 vendor
```

#### Commande pour démarrer le serveur web

Dans un terminal, tapez la commande suivante :

```
composer edu:start
```

{% hint style="info" %}
Ce résultat est un exemple et il ne sera probablement pas le vôtre.
{% endhint %}

Exemple d'affichage suite à la commande :&#x20;

```batch
> Composer\Config::disableProcessTimeout
> php -S localhost:8042 -t public
[Thu Aug 10 12:20:53 2023] PHP 8.1.21 Development Server (http://localhost:8042) started
```

Ouvrez un onglet dans votre navigateur préféré puis copier/coller cette adresse (URL)

{% embed url="http://localhost:8042" %}

Voici le résultat :&#x20;

<figure><img src=".gitbook/assets/CleanShot 2023-08-10 at 12.35.14@2x.png" alt=""><figcaption></figcaption></figure>

Bravooooo :tada::tada::tada: Vous êtes prêts pour développer votre projet !!!!!

<figure><img src=".gitbook/assets/excited-minions-gif.gif" alt=""><figcaption></figcaption></figure>

Si vous rencontrez des erreurs, vous pouvez vous rendre sur cette page

{% content-ref url="liste-des-erreurs.md" %}
[liste-des-erreurs.md](liste-des-erreurs.md)
{% endcontent-ref %}

### Quelques explications

Pour ceux qu'ils veulent comprendre la commande :&#x20;

```
composer edu:start
```

Cette commande est un script qui est présent dans le fichier "composer.json" dans la section "scripts"

```json
  "scripts": {
    "edu:start": [
      "Composer\\Config::disableProcessTimeout",
      "php -S localhost:8042 -t public"
    ]
  }
```

Ce script execute 2 commandes :&#x20;

**"Composer\\\Config::disableProcessTimeout"**

Cette commande désactive le timeout du serveur web

**"php -S localhost:8042 -t public"**

Cette commande démarrer le serveur web en pointant sur le dossier public de votre arborescence. Grâce au fichier index.php (qui est le fichier par défaut), le serveur web va pouvoir démarrer sur IP local (loopback) et le port 8042
