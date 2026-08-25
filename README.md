# Galerie photo — mode d'emploi

Site de galerie photo pour GitHub Pages. Une fois en ligne, **ajouter une photo = déposer un fichier JPEG dans un dossier**. Rien d'autre à faire : le site se reconstruit tout seul.

## 1. Mise en ligne (une seule fois)

1. Créez un compte sur [github.com](https://github.com) si ce n'est pas déjà fait.
2. Créez un nouveau dépôt (« New repository ») nommé exactement `votrenom.github.io` (remplacez `votrenom` par votre nom d'utilisateur GitHub). Cochez « Public ».
3. Dans le dépôt, cliquez sur « uploading an existing file » (ou « Add file → Upload files ») et glissez-déposez **tout le contenu de ce dossier** (les fichiers ET les dossiers `_layouts`, `assets`, `photos`).
4. Cliquez sur « Commit changes » en bas.
5. Attendez 1 à 2 minutes, puis ouvrez `https://votrenom.github.io` — votre site est en ligne.

Si la page ne s'affiche pas : allez dans Settings → Pages du dépôt et vérifiez que « Source » est réglé sur la branche `main`.

## 2. Ajouter des photos (le quotidien)

1. Ouvrez votre dépôt sur github.com, puis le dossier `photos/`, puis l'album voulu.
2. « Add file → Upload files », glissez vos JPEG, « Commit changes ».
3. Deux minutes plus tard, les photos sont sur le site. C'est tout.

**Nommage conseillé** : `AAAA-MM-JJ-titre-de-la-photo.jpg` (ex. `2026-08-25-marche-aux-puces.jpg`).
- La date sert au tri chronologique du flux (les plus récentes en premier) et s'affiche dans la légende.
- Le reste du nom devient le titre affiché (les tirets deviennent des espaces).
- Sans date, la photo s'affiche quand même — elle sera simplement triée par ordre alphabétique.

**Conseil poids** : exportez vos scans en JPEG d'environ 2000 px de large (qualité 80–85). Le site restera rapide.

## 3. Créer un nouvel album

Un album = un sous-dossier de `photos/`. Pour en créer un depuis le site GitHub :

1. Dans `photos/`, cliquez « Add file → Upload files ».
2. Avant de déposer vos fichiers, il n'est pas possible de créer un dossier vide — déposez donc directement vos photos via « Add file → Create new file », tapez `photos/nom-du-nouvel-album/photo.txt` puis supprimez ce fichier après avoir téléversé vos premières photos… **Plus simple** : préparez le dossier sur votre ordinateur avec les photos dedans, puis glissez le dossier entier dans la fenêtre « Upload files » — GitHub recrée l'arborescence automatiquement.

Le nom du dossier devient le nom de l'album (tirets = espaces). Ex. : `portra-400-paris` → « portra 400 paris ».

## 4. Personnaliser

- **Nom du site** : modifiez la première ligne de `_config.yml` (crayon ✏️ sur github.com, puis « Commit changes »).
- **Photos d'exemple** : supprimez les dossiers `photos/portra-400-paris` et `photos/hp5-bord-de-marne` quand vous ajoutez les vôtres (ouvrir chaque fichier → menu « … » → Delete file).
- **Nom de domaine personnalisé** : Settings → Pages → « Custom domain », puis suivez les instructions DNS de votre registrar.
- **Changer le design** (couleurs, mise en page…) : revenez me voir avec ce que vous souhaitez, je vous préparerai les fichiers mis à jour.

## Structure des fichiers

```
_config.yml          → nom du site
_layouts/            → gabarit des pages (ne pas toucher)
assets/style.css     → styles (ne pas toucher, sauf envie)
index.html           → page Flux (automatique)
albums.html          → page Albums (automatique)
photos/
  ├── un-album/      → vos JPEG
  └── autre-album/   → vos JPEG
```
