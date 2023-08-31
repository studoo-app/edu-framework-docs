# Comment versionner ?

Pour travailler en mode projet, il est important de versionner son travail. Même tout seul !

Les raisons sont simples :&#x20;

* Revenir en arrière en cas de mauvaise manip et d'implémentation foireuse :smile:
* Avoir plusieurs versions de test, stable…
* Gestion des issues (taches)

#### Pour versionner le projet :&#x20;

1/ Créez un nouveau "repository" chez votre fournisseur GIT (Github, GitLab ...)

{% hint style="warning" %}
**Veuillez noter que le repository doit être VIDE au moment de la création.**
{% endhint %}

2/ Ouvrez un terminal et allez dans à la racine du projet

3/ Tapez les lignes suivantes :&#x20;

* Initialisation du projet&#x20;

```bash
git init
```

* Ajout de l'URL du repository GIT

```bash
git remote add origin <URL GIT>
```

{% hint style="warning" %}
```
Remplacez <URL GIT> par le URL du repository lors sa création
Voici un exemple :
"git remote add origin git@github.com:bfoujols/Testing-Edu-Frame.git"
```
{% endhint %}

* Ajout de la branche "main"

```bash
git branch -M main
```

* Ajout des fichiers pour le commit

```bash
git add * .gitignore .env.example
```

* Ajout du commit 'init project'

```bash
git commit -m 'init project'
```

* Envoi des fichiers sur le repository central git&#x20;

```bash
git push -u origin main
```
