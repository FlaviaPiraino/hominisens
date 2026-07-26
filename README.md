# Site HominiSens — version statique modifiable

Reconstruction en HTML/CSS du site www.hominisens.com (original construit avec Wix), pour pouvoir le modifier librement et l'héberger sur GitHub Pages.

## Structure du projet

```
hominisens/
├── index.html        → page Accueil
├── soins.html        → page Soins
├── tarifs.html       → page Tarifs
├── formations.html   → page Formations
├── galerie.html      → page Galerie
├── qui-suis-je.html  → page Qui suis-je ?
└── css/
    └── style.css     → toute la mise en forme (couleurs, polices…)
```

## Comment modifier le site

- **Les textes** : ouvrez le fichier `.html` de la page concernée avec n'importe quel éditeur (VS Code, Notepad++, ou même le Bloc-notes) et modifiez le texte entre les balises.
- **Les couleurs et polices** : tout est centralisé en haut de `css/style.css` dans la section `:root`. Changez par exemple `--or: #b98d4f;` pour modifier la couleur dorée partout.
- **Prévisualiser** : double-cliquez simplement sur `index.html` pour ouvrir le site dans votre navigateur.

## ⚠️ Important : les images et les PDF

Pour l'instant, les images et les documents PDF pointent encore vers les serveurs de Wix (`static.wixstatic.com` et `hominisens.com/_files/...`). Cela fonctionne tant que votre site Wix existe, mais **si vous fermez votre abonnement Wix, ces liens mourront**.

À faire pour être 100 % indépendant :
1. Téléchargez vos images (clic droit → « Enregistrer l'image sous… » depuis votre site actuel, ou depuis votre médiathèque Wix).
2. Placez-les dans un dossier `images/` à la racine du projet.
3. Remplacez dans les fichiers HTML les adresses `https://static.wixstatic.com/...` par `images/nom-du-fichier.jpg`.
4. Faites de même avec vos PDF (CGV, calendrier, mentions légales…) dans un dossier `documents/`.

## Ce qui n'a pas pu être copié

- Le **formulaire de contact** de la page Formations (fonctionnalité Wix) : remplacé par un bouton mail. Alternative gratuite : [Formspree](https://formspree.io) ou [Tally](https://tally.so).
- Le rendu n'est pas pixel par pixel identique à Wix (leur code n'est pas exportable), mais tout le contenu et la structure y sont.

## Publier sur GitHub Pages (gratuit)

1. Créez un compte sur [github.com](https://github.com) si besoin.
2. Créez un nouveau dépôt (« New repository »), par exemple `hominisens`.
3. Cliquez sur « uploading an existing file » et glissez-déposez tous les fichiers de ce dossier (en conservant le dossier `css/`).
4. Validez (« Commit changes »).
5. Allez dans **Settings → Pages**, puis sous « Branch », choisissez `main` et `/ (root)`, et enregistrez.
6. Après 1-2 minutes, votre site sera en ligne à l'adresse `https://votre-pseudo.github.io/hominisens/`.

Pour utiliser votre propre nom de domaine (hominisens.com) : Settings → Pages → « Custom domain », puis configurez les DNS chez votre registrar (GitHub fournit la documentation à cette étape).

## Le formulaire de contact (page Formations)

Le formulaire est prêt, il ne manque que votre identifiant Formspree (service gratuit qui envoie les messages du formulaire directement dans votre boîte mail, sans serveur) :
1. Créez un compte gratuit sur https://formspree.io avec l'adresse flaviapiraino@gmail.com.
2. Créez un nouveau formulaire (« New form ») : Formspree vous donne une adresse du type `https://formspree.io/f/abcdwxyz`.
3. Dans `formations.html`, remplacez `VOTRE_ID_FORMSPREE` par cet identifiant (cherchez le commentaire ⚠️ FORMULAIRE).
4. C'est tout : chaque envoi du formulaire arrivera dans votre boîte mail (50 messages/mois en gratuit).

## Ajuster les couleurs

La palette a été rapprochée de l'original (fond blanc cassé, texte anthracite doux, accents doré et vert sauge), mais le code exact des couleurs Wix n'est pas exportable. Pour coller parfaitement :
1. Ouvrez votre éditeur Wix → Thème du site → Couleurs : notez les codes hex (ex. #C0A97E).
2. Ouvrez `css/style.css` : les 7 premières lignes de `:root` contrôlent tout le site. Remplacez les valeurs et rechargez la page.

## Plan complet du site

Pages principales : index, soins, tarifs, formations, galerie, qui-suis-je.
Sous-pages (liées par les boutons) :
- `travail-corps-complet.html` — descriptions des soins corps complet
- `specifiques.html` — Rebozo, 4 mains, Étoile, dos, ventre holistique, pierres chaudes
- `les-petits-plus.html` — soins visage / nuque / crâne
- `techniques-tarifs.html` — les 10 formations avec niveaux, durées et tarifs AF/FE
- `prise-en-charge.html` — financements OPCO, France Travail, FAF, Région, FNE

Les boutons « Descriptions », « Techniques & Tarifs » et « Quelle prise en charge » pointent maintenant vers ces pages locales. Seuls les PDF (programmes détaillés, CGV, calendrier…) pointent encore vers Wix — pensez à les télécharger dans un dossier `documents/` avant de quitter Wix.

## Version 2 (refonte pro)
Cette version remplace la V1 : nouvelle identité visuelle, page contact.html dédiée à la réservation,
FAQ avec données structurées, sitemap.xml, robots.txt, accessibilité renforcée.
Voir CHANGELOG.md pour le détail phase par phase.
