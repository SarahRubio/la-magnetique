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
- `header.html` est appliqué sur l'ensemble des autres pages

Le contenu de ses deux header est accessible depuis le dossier `_includes`

### gestion du footer

Le footer est accessible depuis le dossier `_includes` sous le nom `footer.html`. 

Pour ajouter un logo dans le footer:  
- on importe l'image du logo dans le dossier `assets/img`
- dans le fichier `_includes/footer.html` on ajoute à la suite des autres logos un nouveau snippet de code en modifiant le nom de l'image et son extension ainsi que le contenu de la balise `alt` qui est utilisée pour l'accessibilité du site:

        <div class="column is-one-fifth-desktop is-one-third-mobile">
            <div class="image">
              <img src="{{ site.baseurl }}/assets/img/alpha.jpg" alt="Grand Angoulême L'alpha">
            </div>
        </div>

### gestion du head

Le fichier `head.html` présent dans le dossier `_includes` gère notamment le SEO de chaque page. 

la variable `page.title` va chercher pour chaque page le paramètre `title` présent dans le `frontmatter` de chaque page. 

### modification d'une page du dossier `pages`

Chacune de ces pages fonctionnement avec un `frontmatter` : c'est la première partie de la page séparée par des `---`
Cette partie est essentielle pour chacune de ces pages. La valeur de chacun des arguments doit être changée pour chaque page. e.g :  
    title: piezo

Dans cet exemple `title` est l'argument qui ne doit pas être modifié pour le bon fonctionnement du site. Et `piezo` est la valeur de l'argument qui peut être modifiée en fonction de la page. 

Le plus simple pour créer une nouvelle page est de dupliquer une autre page du dossier `pages` et d'adapter les valeurs.

À ce jour, les arguments sont : 

- `title` : qui sert pour le titre de la page, pour le titre qui s'affiche dans l'onglet du navigateur et pour le titre s'affichant lors du partage sur les réseaux sociaux. 
- `og-description`: qui sert pour la description de page lors du partage sur les réseaux sociaux
- `background-color`: qui sert pour le choix d el acouleur de fond de la page. Ce nom de couleur se réfère à un code couleur inscrit dans le fichier `assets/css/style.css`
- `image`: qui sert pour l'image principale choisie pour la page. Une nouvelle image peut être choisie en modifiant la valeur avec le nom d'une image importée dans le dossier `assets/img`. La valeur ne doit pas contenir le format de l'image (exemple `.png`).
- `intro`: qui sert de texte introductif pour les pages ateliers
- `objectifs`: qui sert à lister les objectifs pour les pages ateliers
- `materiel`: qui sert à lister le matériels sur les pages ateliers
- `infos`: qui sert à lister les infos finales pour les pages ateliers (niveau, âge, nombre, durée)

### gestion des couleurs

##### Changement d'une couleur existante par une autre couleur existante sur une page

Il suffit dans ce cas de changer la valeur `color` présente dans le `frontmatter` de la page choisie.

À ce jour les couleur existante sont :  
- yellow
- aquablue
- azur
- orange
- blueduck

Exemple : 

    ---
    color: yellow
    ---

Pour les ateliers il faut aussi penser à changer le nom de la couleur pour l'affichage sur la page d'accueil.
Il faut se rendre sur la page index.md et modifier le nom présent dans la balise `id` du snippet de code lié à l'atelier. Exemple ici avec `bg-azur` qui pourrait être changé en `bg-yellow` : 

    <div id="bg-azur" class="card-content has-text-centered is-size-5">
        <p>Ateliers sur mesure</p>
    </div>

##### Création d'une nouvelle couleur

Les couleurs sont définies dans le fichier `assets/css/style.css` avec des codes couleur. Exemple avec une couleur nommée `bg-yellow`. À ce nom de couleur est associé :

- une couleur de fond : `background-color` et une couleur pour le texte: `color` :

        .bg-yellow, #bg-yellow {
            background-color: #f5faa0;
            color: #224d52;
        }

- une couleur de fond en cas de survol: `background-color`et une couleur pour le texte: `color`:
  
        #bg-yellow:hover {
            background-color: #f5faa0c4;
        }

- une couleur de fond : `background-color`pour les  titres principaux et une couleur pour le texte des titres principaux (`h1` et `h2`):
  
        .bg-yellow h1,
        .bg-yellow h2 {
            background-color: #224d52;
            color: #f5faa0;
        }

Si on veut ajouter une nouvelle couleur on peut dupliquer ces trois snippets de code et modifier le nom ainsi que les codes pour les différents éléments. exemple:   

        .bg- h1, .bg-black h2 {
            background-color: #00000;
            color: #fffff;
        }   

### modification de la page contact

#### modification des liens

Un lien s'écrit en html comme ceci : 

    <a href="https://monlien.fr" target="_blank" rel="noopener">Mon Lien</a>

Pour modifier un lien existant il suffit de modifier l'url dans la balise `href` et le nom du bouton si besoin qui est entre `<a>` et `</a>`.

Pour créer un nouveau lien on peut copier le code existant correspondant au style souhaité et remplacer les balises `href` et le nom du lien entre `<a>` et `</a>`.
