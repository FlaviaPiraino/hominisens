# Journal des changements — Refonte HominiSens

## Phase 0 — Audit & architecture (terminée ✅)
- Audit des 11 pages existantes (voir synthèse dans la conversation).
- Nouvelle arborescence : 12 pages HTML + css/style.css + sitemap.xml + robots.txt.
- Création d'une page `contact.html` dédiée (réservation, carte cadeau, événements, formations) — c'était le principal frein à la conversion : aucun point de conversion central n'existait.
- Vérifié : génération sans erreur, 12/12 pages présentes.

## Phase 1 — UI / Design (terminée ✅)
- Nouvelle direction artistique : typographies Cormorant Garamond (titres) + Jost (texte), palette blanc chaud / anthracite / doré / sauge, variables CSS centralisées dans `:root`.
- Navigation repensée : logo texte, menu sticky, bouton « Réserver » permanent.
- Héros par page (image + H1 + sous-titre + CTA), bandeau de réassurance sous chaque héros.
- Nouveaux composants : cartes avec badge et CTA, étapes numérotées, bloc chiffres clés, bandes CTA de fin de page, carte tarif « vedette », barre d'action mobile fixe (Appeler / Réserver).
- Vérifié : CSS unique, aucun style dupliqué entre pages.

## Phase 2 — Copywriting & conversion (terminée ✅)
- Réécriture intégrale des titres, textes et CTA des 12 pages (bénéfices avant caractéristiques, vouvoiement chaleureux, ton haut de gamme).
- CTA orientés action sur chaque page : « Réserver mon soin », « Recevoir le programme », « Demander mon devis financement »…
- Formulaires enrichis : menu déroulant « objet de la demande », champ formation, messages de réassurance (réponse sous 48 h, données non transmises).
- Prix par soin affichés dans les packs (ex. « soit 55 €/soin ») pour rendre la remise tangible.
- Vérifié : chaque page se termine par un appel à l'action ; parcours soin et parcours formation complets en 2 clics max.

## Phase 3 — SEO (terminée ✅)
- Balises Title uniques ≤ 68 caractères et meta descriptions ≤ 155 caractères sur les 12 pages, avec mots-clés locaux (Mouvaux, Lille, métropole lilloise) et métier (massage bien-être, formation massage, Qualiopi).
- 1 seul H1 par page, hiérarchie H2/H3 propre.
- Données structurées schema.org : LocalBusiness (accueil) + FAQPage (accueil, soins, tarifs, formations).
- 4 FAQ rédigées (5 questions chacune) ciblant les requêtes réelles des internautes.
- Maillage interne renforcé (héros → soins/tarifs/contact, footer complet, liens croisés soins ↔ tarifs ↔ contact).
- sitemap.xml + robots.txt générés ; balises canonical et Open Graph sur chaque page.
- Vérifié : script de contrôle — 0 lien interne cassé, 0 image sans alt, longueurs Title/description conformes.

## Phase 4 — Accessibilité (terminée ✅)
- Lien d'évitement « Aller au contenu principal » sur chaque page.
- Navigation avec aria-label, <main id="contenu">, focus visible contrasté sur tous les éléments interactifs.
- Alt descriptifs sur 100 % des images, labels explicites sur tous les champs de formulaire.
- FAQ en <details>/<summary> natifs (accessibles clavier sans JavaScript).
- Respect de prefers-reduced-motion (animations désactivées si demandé par l'utilisateur).
- Vérifié : script de contrôle — 0 image sans alt ; parcours clavier fonctionnel (skip link, focus).

## Phase 5 — Performances (terminée ✅, optimisations restantes listées)
- loading="lazy" sur toutes les images hors héros.
- Préconnexion aux domaines de polices (preconnect), chargement des polices avec display=swap.
- Aucune dépendance JavaScript : site 100 % statique, CSS unique en cache.
- Restant (nécessite vos fichiers sources) : héberger les images en local aux bonnes dimensions (formats WebP/AVIF) au lieu des URLs Wix — voir README.

## À faire par vos soins (5 minutes chacune)
1. Formspree : créer le compte gratuit et remplacer VOTRE_ID_FORMSPREE dans contact.html et formations.html.
2. Images & PDF : les rapatrier en local avant de fermer Wix (voir README).
3. Domaine : si le site n'est pas servi sur www.hominisens.com, adapter les balises canonical et sitemap.xml.

## Phase 0-bis — Architecture complémentaire (terminée ✅)
- Page 404.html personnalisée (même charte, liens de secours vers les pages clés), exclue du sitemap. Servie automatiquement par GitHub Pages en cas d'URL inexistante.
- Favicon SVG (monogramme H, couleurs de la charte) référencé dans les 13 pages.
- Dossiers `images/` et `documents/` créés avec instructions (fichier A-LIRE.txt dans chacun) pour rapatrier vos médias hors de Wix.
- Vérifié : 13 pages générées, favicon présent partout, 0 lien cassé, 404 bien hors sitemap.

## Phase 1-bis — Design system & responsive (terminée ✅)
- Discipline des couleurs actée : sauge = action (tous les boutons cliquables primaires), contour = action secondaire, doré réservé au prestige (titres H3, prix, badges) et foncé d'un cran quand il reste en bouton, pour le contraste.
- Emojis remplacés par un jeu d'icônes SVG cohérent (trait 1,8 px, currentColor) : téléphone, mail, bulle, étoile, cœur, médaille, coche. Rendu identique sur iOS, Android et desktop.
- Menu burger sur mobile/tablette (≤ 900 px) : bouton Réserver toujours visible à côté du burger, menu déroulant plein écran, animation croix, attributs aria-expanded/aria-controls, ~10 lignes de JavaScript vanilla.
- Palier tablette (700–1023 px) : grilles en 2 colonnes, héros compacté.
- Zones tactiles ≥ 44 px : boutons, liens du menu mobile, liens du pied de page, accordéons FAQ.
- Confort de lecture : largeur de ligne plafonnée à 75 caractères dans les encadrés, cartes, étapes et FAQ.
- Nouvelle page interne `styleguide.html` (noindex, hors sitemap) : palette et règles d'usage, échelle typographique, boutons et états, composants, règles photo/icônes/ton.
- Vérifié : 14 pages, 0 emoji résiduel, burger + script présents partout, 0 « bouton or » hors démonstration styleguide, 1 h1/page, 0 lien cassé, 0 image sans alt.

## Révision de contenu du 14/07/2026 (demandes de Flavia — terminée ✅)
- Accueil : nouveau sous-titre du héros (« Praticienne diplômée et formatrice agréée… ») ; bande de réassurance réécrite (psychomotricienne de formation initiale, RNCP 2018, formatrice agréée 2021, organisme Qualiopi 2025, uniquement sur RDV) ; paragraphe d'intro simplifié signé Flavia Piraino ; « Prestations proposées » remplace « Trois façons de prendre soin de vous » ; bloc Recevoir un massage reformulé (15 techniques, 30 à 90 min) ; carte cadeau : validité 6 mois précisée ; étape 3 → « Vous profitez » ; section élargie « Événements, entreprises & ateliers ».
- Correction majeure : les soins ont lieu EN CABINET À MOUVAUX, à domicile uniquement sur demande (20 km max, +10 €). FAQ « Où ont lieu les soins ? » réécrite ; pied de page, méta-descriptions et alt harmonisés en conséquence.
- Correction Qualiopi : c'est l'ORGANISME qui est certifié, pas les formations — pied de page, balise Title formations et méta-descriptions corrigés partout.
- Soins : noms des 15 soins en gras dans les listes.
- Contact : suppression de la phrase « Interventions à domicile… » et du bloc « Bon à savoir avant votre premier soin ».
- Tarifs : sous-titre héros → « Techniques adaptables selon vos besoins ».
- Vérifié : script de contrôle complet (0 erreur) + contrôle ciblé de chacune des modifications demandées.

## Révision de contenu du 15/07/2026 (demandes de Flavia — terminée ✅)
- Formations : « OBJECTIF GÉNÉRAL » en gras puis « COMPÉTENCES VISÉES » à la ligne avant la liste 1-5 ; nouvelle question FAQ « Y a-t-il des prérequis pour se former ? » (ajoutée aussi aux données structurées JSON-LD) ; « Recevez le programme et le calendrier » → « Contactez-moi » ; bouton du formulaire → « Envoyer votre demande ».
- Catalogue des formations : les 10 boutons « Demander le programme & les dates » → « Demander un devis » ; bande du bas → « Réservez votre place » (sans « pour 2026 ») avec bouton « Faire ma demande d'inscription » ; première ligne de chaque bloc (niveau · pression · durée · tarifs) entièrement en gras.
- Qui suis-je : parcours en quatre dates avec nouveau bloc 2021 « Formatrice agréée » (carte 2019 recentrée sur le lancement d'HominiSens) ; bloc histoire remplacé par « Vers le chemin du mieux-être… » avec le texte intégral de Flavia (trois coquilles corrigées : dotée, auprès, états d'âme) ; phrase « Le meilleur moyen de savoir si le courant passe ? » retirée de la bande finale.
- Vérifié : script complet (0 erreur) + contrôle ciblé des 13 modifications, y compris le JSON-LD et le compte exact des 10 boutons devis.

## Identité visuelle du 15/07/2026 — logo animé & favicon (terminée ✅)
- Nouveau favicon : monogramme HS fourni par Flavia (image détourée, recadrée au carré, exportée en 192 px et 32 px PNG, avec apple-touch-icon). L'ancien favicon SVG provisoire est supprimé.
- Logo animé SVG vectoriel (interprétation de la planche d'identité) : « H MINI » en Cormorant Garamond avec le O remplacé par un cercle contenant la silhouette humaine bras écartés, « Sens » en calligraphie Great Vibes. Trois volutes stylisées (sauge et doré, translucides) autour du O.
- Animations conformes à la planche : rotation lente des volutes (30 s/tour) et « respiration » du mot Sens (pulsation 4,5 s) — CSS pur, désactivées automatiquement si l'utilisateur préfère réduire les animations.
- Intégration : logo dans la barre de navigation des 14 pages (version encre sur fond clair, 46 px) et grande version claire (crème/sauge pâle) dans le héros de la page d'accueil, responsive.
- Vérifié : logo présent sur les 14 pages (2 occurrences sur l'accueil), favicons PNG référencés partout, police script chargée, keyframes et prefers-reduced-motion en place, 0 régression au script de contrôle.
- Note : le rendu typographique exact (espacements H/O/MINI/Sens) pourra être micro-ajusté sur retour visuel de Flavia.

## Réversion du 15/07/2026 — logo animé annulé, favicon conservé (terminée ✅)
- Retrait du logo SVG animé (barre de navigation et héros d'accueil) à la demande de Flavia : retour au mot-marque « HominiSens » typographié.
- Retrait de la police Great Vibes (inutilisée) et du bloc CSS d'animations.
- Le favicon monogramme HS (favicon.png 192 px + favicon-32.png) est conservé sur les 14 pages.
- Le code du logo reste archivé dans le script de génération, prêt à être réactivé (en version statique ou animée) si souhaité un jour.
- Vérifié : 0 trace du logo ou de la police script dans les pages, mot-marque texte et favicons présents partout, 0 régression.

## Conformité Qualiopi du 15/07/2026 (terminée ✅)
- Audit du site au regard de la Charte d'usage de la marque Qualiopi (version mars 2023) fournie par Flavia.
- Affichage du logo corrigé : l'URL Wix recadrait l'image (mode « fill »), risque de rognage de la marque interdit par la charte graphique → passage en mode « fit » (logo entier, non déformé).
- Mention de catégorie alignée sur la formulation officielle : « La certification qualité a été délivrée au titre de la ou des catégories d'actions suivantes : ACTIONS DE FORMATION ».
- Vérifié conforme : logo présent uniquement au niveau organisme (page prise-en-charge), jamais associé à une formation en particulier ; mention de catégorie adjacente au logo ; formulations « organisme certifié » exactes sur tout le site.
- À vérifier par Flavia (hors site) : version du logo avec bloc Marianne/République Française, et absence de la marque sur les programmes PDF par formation et sur les attestations.

## Entête de marque du 15/07/2026 — bannière accueil (terminée ✅)
- Bannière d'entête composée à partir des deux visuels fournis par Flavia : feuilles de monstera (image 2) dans les coins supérieurs + mot-marque HominiSens (image 1) centré, fonds harmonisés par correction colorimétrique. Fichier local : images/entete-accueil.jpg (1600×430).
- Nouveau héros « clair » sur la page d'accueil : fond crème assorti à la bannière (#faf8f7), tagline « Formations & massages bien-être — Corps • Énergie • Harmonie », H1, sous-titre et boutons adaptés au fond clair. Les autres pages conservent le héros photo sombre.
- Première image hébergée en LOCAL (dossier images/) : l'accueil ne dépend plus de Wix pour son visuel principal.
- Vérifié : bannière présente et servie localement (~60 Ko), 1 h1/page, 0 image sans alt, 0 lien cassé.

## Réversion du 15/07/2026 — bannière d'entête annulée (terminée ✅)
- Retour au héros photo sombre sur la page d'accueil, à la demande de Flavia (bannière monstera + mot-marque annulée).
- Bloc CSS « héros clair » retiré ; fichier images/entete-accueil.jpg sorti du site (archivé hors livraison, recomposable à la demande).
- Le favicon monogramme HS reste en place.
- Vérifié : héros photo présent, aucune trace de la bannière, 0 régression.

## Conformité CNIL / RGPD du 15/07/2026 (terminée ✅)
- Audit technique complet : AUCUN cookie, aucun stockage local, aucun traceur (pas d'analytics, pas de pixel, pas d'embed) — seuls scripts présents : données structurées JSON-LD et menu burger. Conclusion : bannière cookies NON obligatoire en l'état.
- Nouvelle page confidentialite.html (information article 13 RGPD) : responsable de traitement, données/finalités/base légale, sous-traitants (Formspree, hébergeur), durées de conservation, absence de cookies, droits et recours CNIL. Placeholders ⚠️ à compléter par Flavia : adresse pro, SIRET, durée de conservation, hébergeur final.
- Lien « Politique de confidentialité » ajouté au pied de page des 15 pages et sous les 2 formulaires ; reformulation de la mention inexacte « jamais transmises à des tiers » (Formspree est un sous-traitant).
- Points de vigilance documentés : Google Fonts et images Wix chargées depuis des serveurs tiers (transmission d'IP) → internalisation recommandée ; mentions légales à mettre à jour (hébergeur) lors de la migration hors Wix.
- Vérifié : page présente et dans le sitemap, lien en pied de page sur toutes les pages, 0 régression.

## Identité visuelle du 15/07/2026 — entête, pied de page et favicon (terminée ✅)
- Nouveau favicon : monogramme HS cerclé fourni par Flavia (détouré, 192 px + 32 px).
- Entête d'accueil : bannière complète fournie par Flavia (mot-marque + feuilles de monstera + aquarelle + taglines « Formations & massages bien-être » et « L'art du toucher, l'esprit en mouvement »), servie en local (images/entete-accueil.jpg, 1600×584, ~125 Ko). Héros clair : titre, sous-titre et boutons adaptés au fond crème (#e7e3d9, raccord échantillonné sur le bas de la bannière).
- Pied de page : fond aquarelle fourni par Flavia (images/fond-pied-de-page.jpg, 1800×660, ~100 Ko) sur les 15 pages ; textes passés en encre, titres en doré foncé, liens sombres, séparateur adapté — contrastes vérifiés sur fond clair.
- Vérifié : bannière et fond servis en local, favicon remplacé partout, 1 h1/page, 0 image sans alt, 0 lien cassé.

## Entêtes du 15/07/2026 — accueil épuré & fond aquarelle sur toutes les pages (terminée ✅)
- Accueil : titre et sous-titre retirés de l'entête à la demande de Flavia ; les boutons « Réserver mon soin » et « Découvrir les formations » sont intégrés directement sous la bannière, dans l'entête. Un H1 invisible (classe sr-only) est conservé pour le référencement et les lecteurs d'écran.
- Toutes les autres pages : le bandeau photo sombre (hébergé chez Wix) est remplacé par le fond aquarelle clair fourni par Flavia (images/fond-entete.jpg, 1800×658, ~90 Ko, servi en local). Titres, sous-titres et boutons conservés par-dessus, basculés en couleurs foncées (encre/doré/sauge) pour la lisibilité sur fond clair.
- Bénéfice collatéral : plus aucune image de structure ne dépend de Wix (seules les images de contenu des pages soins/galerie restent à rapatrier).
- Vérifié : 1 h1/page (dont le sr-only de l'accueil), boutons présents dans l'entête, fond local référencé, 0 lien cassé, 0 image sans alt.

## Accueil du 15/07/2026 — boutons superposés à la bannière (terminée ✅)
- Les boutons « Réserver mon soin » et « Découvrir les formations » sont désormais posés SUR la bannière d'entête (bas-centre, zone crème libre), supprimant la bande sous l'image sur ordinateur et tablette.
- Repli automatique sur mobile (< 720 px) : la bannière devenant trop basse, les boutons repassent sous l'image pour rester tactiles et lisibles.
- Vérifié : superposition active, repli mobile en place, H1 invisible conservé, 0 régression.

## Accueil du 15/07/2026 — boutons intégrés à la bannière (terminée ✅)
- La bande sous la bannière est supprimée : les boutons « Réserver mon soin » et « Découvrir les formations » sont désormais superposés à l'image d'entête (bas centré), avec une ombre légère et un fond translucide sur le bouton secondaire pour la lisibilité.
- Comportement mobile : sous 720 px, la bannière devient trop basse pour accueillir les boutons — ils glissent automatiquement juste sous l'image, sans bande de couleur.
- Vérifié : boutons dans le bloc bannière, ancienne bande supprimée, 1 h1/page, 0 régression.

## Rapatriement des photos du 15/07/2026 (terminée ✅)
- 17 photos fournies par Flavia intégrées en local : 3 cartes de l'accueil, 3 cartes de la page Soins, 5 soins corps complet, 6 soins spécifiques.
- Traitement appliqué : orientation EXIF respectée, recadrage 4:3 avec cadrage attentif aux visages sur les photos verticales, redimensionnement 800×600, compression web (~50 Ko/photo, 1,5 Mo au total).
- Textes alternatifs réécrits pour décrire les vraies scènes (référencement image + accessibilité).
- Dépendances Wix restantes : 4 photos page visage (les-petits-plus), 12 photos galerie, 1 portrait (qui-suis-je), 1 logo Qualiopi (prise-en-charge) + les PDF. Attention : 2 photos sources étaient en basse résolution (soins-specifiques 360×480 et soin-rebozo 360×480) — remplacement conseillé par les originaux HD si disponibles.
- Vérifié : 17 fichiers présents et référencés, plus aucune image Wix sur l'accueil, la page Soins, Corps complet et Spécifiques ; 0 lien cassé, 0 image sans alt.

## Photos & bannière du 16/07/2026 (terminée ✅)
- Page visage (les-petits-plus) : les 4 photos Wix remplacées par les photos de Flavia — Relaxant du Buste, Sculptural Face Lifting, Kobido (Gua Sha quartz rose), Renai'Sens. Recadrage 4:3, 800×600, alt descriptifs.
- Page Formations : nouvelle photo « Accompagnement » intégrée dans la section d'introduction (Flavia guidant une stagiaire), encadrée aux arrondis et ombre de la charte.
- Entête d'accueil : bannière remplacée par la nouvelle version fournie (taglines « Massages bien-être & formations »), même gabarit 1600×584, alt mis à jour, couleur de raccord inchangée.
- Dépendances Wix restantes : 12 photos galerie, 1 portrait (qui-suis-je), 1 logo Qualiopi + PDF.
- Vérifié : fichiers présents et référencés, plus aucune image Wix sur la page visage, 0 régression.

## Rapatriement du 16/07/2026 — page Visage, photo Formations, nouvelle bannière (terminée ✅)
- 4 photos de la page Visage-Nuque-Crâne intégrées en local (relax buste, face lifting, Kobido au Gua Sha quartz rose, Renai-Sens) : plus aucune image Wix sur cette page. Même traitement que la veille (EXIF, 4:3, 800×600, ~75 Ko).
- Nouvelle photo « Accompagnement » ajoutée à la page Formations (section d'introduction) : Flavia guidant le geste d'une stagiaire — première image de cette page.
- Bannière d'accueil remplacée par la nouvelle version fournie (tagline « Massages bien-être & Formations », mêmes dimensions 1600×584, alt mis à jour).
- Dépendances Wix restantes : 12 photos galerie, 1 portrait (qui-suis-je), 1 logo Qualiopi (prise-en-charge) + PDF.
- Vérifié : 5 nouveaux fichiers présents et référencés, 0 lien cassé, 0 image sans alt, 1 h1/page.

## Correctif du 16/07/2026 — proportions des images (terminé ✅)
- Bug d'affichage signalé par Flavia : les photos apparaissaient étirées. Cause : attributs width/height fixes sur les images sans « height: auto » dans le CSS — la largeur se réduisait dans les cartes mais pas la hauteur.
- Correction : règle globale img { max-width: 100%; height: auto; } — les proportions d'origine sont désormais respectées à toutes les tailles d'écran. Les fichiers photos eux-mêmes n'étaient pas déformés (recadrage 4:3 propre).

## Correctif du 16/07/2026 — photo Formations (terminé ✅)
- La photo Accompagnement apparaissait en double sur la page Formations (insertion ajoutée à une version déjà présente dans le script) : doublon supprimé, une seule occurrence conservée.
- À la demande de Flavia, la photo n'est plus recadrée en 4:3 : cadre portrait complet (800×1201) pour voir les deux personnes en entier, affichée à 440 px de large maximum.
- Vérifié : une seule occurrence sur la page, proportions correctes.

## Rapatriement des documents & conformité Qualiopi du 26/07/2026 (terminée ✅)
- 7 documents rapatriés de Wix vers documents/ : cgv-prestations.pdf, cgv-formations.pdf (version octobre 2025), certificat-qualiopi.pdf (CERTIFOPAC n° 611811-1, valable 23/09/2025 → 22/09/2028), accessibilite-handicap.pdf (partenaires PSH, MAJ 08/2025), plaquette-offre-formation.pdf (MAJ octobre 2025), organigramme-references.pdf (MAJ juillet 2025), calendrier-2026-formations.pdf (converti depuis le JPG fourni).
- Toutes les URLs hominisens.com/_files correspondantes remplacées par des chemins relatifs dans les 15 pages HTML (footer + boutons Formations, Techniques & tarifs, Prise en charge, index).
- Portrait de Flavia intégré en local sur qui-suis-je.html (images/flavia-portrait.jpg, 900×1350, 3:4 non recadré, ~125 Ko) — plus aucune image Wix sur cette page.
- Conformité Qualiopi (prise-en-charge.html) mise au niveau de la charte d'usage (version mars 2023) :
  - logo officiel avec bandeau « RÉPUBLIQUE FRANÇAISE » intégré en local (images/qualiopi-marianne.jpg, fichier fourni non modifié : ni couleurs, ni typo, ni effets),
  - affiché dans un cartouche blanc quel que soit le fond, avec zone de protection (padding) et largeur fixe 250 px / height:auto (aucune déformation, largeur > taille minimale de 23 mm),
  - mention obligatoire placée immédiatement sous la signature, lisible et de taille équivalente à « processus certifié » : « La certification qualité a été délivrée au titre de la catégorie d'action suivante : ACTIONS DE FORMATION » (formulation au singulier conforme à l'exemple de la charte, une seule catégorie certifiée),
  - lien direct vers le certificat PDF local avec numéro et dates de validité.
- Rappel de la charte respecté : le logo n'apparaît qu'au niveau organisme (jamais associé à une formation précise ni à une publicité pour une action donnée), jamais en transparence, jamais associé au bloc-marque ministériel.
- Dépendances Wix restantes : mentions légales (PDF), fiche de réclamation (PDF), 10 programmes détaillés de formation (PDF, page techniques-tarifs), 12 photos galerie.
- Vérifié : tous les fichiers documents/ et images/ référencés existent, 0 lien local cassé.

## Rapatriement final du 26/07/2026 — galerie & programmes de formation (terminée ✅)
- Galerie : les 12 photos Wix remplacées par les 9 nouvelles photos fournies (Relaxant buste, 4 mains, Sportif ×2, Prénatal, Cervicales, Detox, Ventre holistique, Thaï stretch). Recadrage carré avec cadrage attentif aux visages, 800×800 (ou 723×723 pour les 2 sources plus petites), compression web, alt descriptifs réécrits. Titre « Les vidéos : à vous de tester à la maison ! » et ses 3 vignettes supprimés ; les boutons vers les tutos Instagram/Facebook sont conservés.
- Les 11 programmes détaillés de formation intégrés dans documents/ et liens Wix remplacés (page techniques-tarifs) : programme-relax-corps, relax-buste, sportif (N1&2 combinés), detox, etoile, visage-anti-age, module-bonus-visage, ventre-holistique, thai-stretch, hawaien, prenatal.
- Dépendances Wix restantes : mentions légales (PDF, 15 occurrences en footer) et fiche de réclamation (PDF, page formations). Ce sont les 2 derniers fichiers avant résiliation de Wix.
- Vérifié : 0 image Wix restante sur tout le site, tous les fichiers documents/ et images/ référencés existent.

## Décrochage Wix terminé + mises à jour du 26/07/2026 (terminée ✅)
- Les 2 derniers PDF intégrés : documents/mentions-legales.pdf (MAJ juillet 2026) et documents/fiche-reclamation.pdf. Résultat : 0 lien Wix sur tout le site — l'abonnement Wix peut être résilié dès que le domaine hominisens.com est reconfiguré vers le nouvel hébergement.
- Page Techniques & tarifs : l'encart Visage scindé en 2 formations distinctes, conformément à la plaquette — « VISAGE ANTI-ÂGE » (3 jours, 650 € AF / 750 € FE, badge 100 % satisfaits) et « MODULE BONUS VISAGE — Accessoires & intrabuccal » (2 jours, 400 € AF / 500 € FE, avec le rappel : pas de protocole visage complet, réservé aux praticiens déjà formés). Chaque encart garde son programme PDF et son bouton devis.
- Offre du moment (page Tarifs) passée à Août 2026 : « En août : le Foot Thaï, 45 min à 50 € au lieu de 60 €. » (en gras).
- Pied de page des 15 pages : « Mise à jour du site 07/2026 ».
- EN ATTENTE : recadrage des photos de l'encart Corps complet (page Soins) et du soin Hawaïen (sous-page Corps complet) pour mieux montrer le massé — nécessite les photos originales plein cadre (les fichiers du site sont déjà recadrés en 812×616, impossible d'élargir le champ à partir de ceux-ci).
- Points relevés dans le PDF des mentions légales (à corriger dans le document source si souhaité) : la section « 3. Hébergement » est vide (à compléter avec l'hébergeur choisi au moment de la mise en ligne) et l'en-tête indique encore « En vigueur [06.2021] ».

## Mises à jour du 26/07/2026 (suite) — photos recadrées, chiffres, encart Sportif (terminée ✅)
- Photos remplacées à partir des originaux plein cadre fournis (3840×5760) : images/soins-corps-complet.jpg (encart Corps complet, page Soins) et images/soin-hawaien.jpg (sous-page Corps complet). Recadrage 4:3 (800×600) sur la partie basse de l'image pour bien montrer le massé (tête et dos pour le corps complet, avant-bras sur la jambe pour l'hawaïen) tout en gardant le visage de Flavia.
- Page Formations, bloc « HominiSens Formations en chiffres » : 430 h+ de formations dispensées depuis 2021, 30+ stagiaires formés (dont 10 en 2026, à la date de mise à jour du site).
- Page Techniques & tarifs : l'encart Sportif scindé en 2 formations distinctes, comme le Visage — « SPORTIF — Niveau 1 » (3 jours, 600 € AF / 700 € FE, badge 100 % satisfaits) et « SPORTIF — Niveau 2 » (2 jours, 500 € AF / 600 € FE, avec le rappel : pas d'anatomie au niveau 2, réservé aux praticiens formés). Les deux renvoient au programme commun Niveaux 1 & 2 (PDF).

## Mise à jour du 26/07/2026 (suite) — photo Kobido (terminée ✅)
- images/soin-kobido.jpg (sous-page Soins visage / Les petits plus) remplacée à partir de l'original plein cadre fourni (3840×5760). Recadrage 4:3 (800×600) sur la bande 33–83 % de la hauteur : cadré sur l'action — les mains de Flavia travaillant le visage de la massée (yeux fermés, bandeau), avec le Gua Sha et le rouleau de jade visibles — plutôt que sur le haut du corps de la praticienne. Alt mis à jour (jade au lieu de quartz rose).

## Mise à jour du 26/07/2026 (suite) — badge N2, formulaires, SEO (terminée ✅)
- Techniques & tarifs : badge « 100 % des stagiaires satisfaits » ajouté à SPORTIF — Niveau 2.
- Formulaires de contact (pages Contact et Formations) branchés sur FormSubmit vers flaviapiraino@gmail.com : sujet personnalisé, e-mail reçu en tableau lisible, anti-spam honeypot, redirection après envoi vers la nouvelle page merci.html (noindex). ⚠️ ACTIVATION REQUISE : au tout premier envoi une fois le site en ligne, FormSubmit envoie un e-mail « Activate » à flaviapiraino@gmail.com — cliquer le lien une seule fois, ensuite tout arrive automatiquement.
- Audit SEO/local complet : titres et descriptions uniques ✅, canonicals ✅, alts ✅, sitemap/robots ✅, FAQ schema ✅. Corrections : og:image + og:image:alt ajoutées aux 15 pages (aperçu de partage réseaux sociaux), noindex sur 404.html et styleguide.html, schéma LocalBusiness enrichi (adresse complète 58 rue de Londres, image, gamme de prix 40–300 €), lastmod du sitemap passé au 26/07/2026.
- Note : merci.html volontairement hors sitemap (page technique).
