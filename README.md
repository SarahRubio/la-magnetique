## Le projet 

La Magnétique est une association dont l’ambition est de démocratiser les pratiques musicales collectives et les cultures numériques en proposant des ateliers sonores hybrides.

## Technique

Ce site est construit avec [Jekyll](https://jekyllrb.com/) et déployé sur Github Pages.

### Développement en local

#### Prérequis : 
- Ruby
- Jekyll

#### Installation du projet :

    bundle install

#### Lancement du serveur :

    bundle exec jekyll serve

## Gestion du site

### emplacements des pages et convention de nommage

A l'exception de la page d'accueil qui est à la racine du projet, l'ensemble des pages du site se trouvent dans le dossier pages.

Chaque page correspondant à un atelier doit être nommé selon ce format "atelier-nom-de-latelier.md".

- page d'acceuil : index.md
- page "à propos" : pages/a-propos.md
- page "contact" : pages/contact.md
- page "boîte à sons" : pages/atelier-boite-a-sons.md
- page "carte postale sonore" : pages/atelier-carte-postale-sonore.md
- page "doublage" : pages/atelier-doublage.md
- page "lutherie électronique" : pages/atelier-lutherie-electronique.md
- page "paysage sonore" : pages/atelier-paysage-sonore.md
- page "piezo" : pages/atelier-piezo.md
- page "sur mesure" : pages/atelier-sur-mesure.md

### gestion du header

Deux header ont été créés pour le site : 
- `header-with-hero.html` est appliqué sur la page d'accueil
- header.html est appliqué sur l'ensemble des autres pages

Le contenu de ses deux header est accessible depuis le dossier `_includes`
