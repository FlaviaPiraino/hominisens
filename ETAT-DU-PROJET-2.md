# ÉTAT DU PROJET — Site HominiSens (à lire en début de session)

Dernière mise à jour : 26/07/2026 (dernières actions : identité visuelle validée — bannière d'accueil avec boutons intégrés à l'image, fond aquarelle sur les entêtes intérieures et le pied de page, favicon monogramme —, page confidentialite.html RGPD, conformité Qualiopi vérifiée. Voir CHANGELOG.md). Ce fichier résume tout le projet pour reprendre le travail sans rien réexpliquer.

## 1. Contexte

- Entreprise : HominiSens — Flavia Piraino, praticienne et formatrice en massage bien-être, Mouvaux (59). Soins EN CABINET à Mouvaux ; à domicile uniquement sur demande (20 km max autour de Mouvaux, supplément +10 €). Tél 06 74 25 25 54, mail flaviapiraino@gmail.com.
- Deux activités : soins/massages ET formations professionnelles. C'est l'ORGANISME qui est certifié Qualiopi (pas les formations) — CERTIFOPAC, valable jusqu'au 22/09/2028, CPF non éligible. Repères : psychomotricienne de formation initiale, diplômée RNCP 2018, formatrice agréée depuis 2021, organisme Qualiopi depuis 2025. Carte cadeau valable 6 mois. Propose aussi des ateliers bien-être en petit groupe.
- Site d'origine : Wix (www.hominisens.com), non exportable. Reconstruit en statique HTML/CSS pour être modifiable librement et hébergé sur GitHub Pages.
- Positionnement voulu : haut de gamme, professionnel, chaleureux, humain, bienveillant.

## 2. État actuel : V2 terminée et vérifiée

La version courante est le dossier `hominisens-v2` (livré en zip `hominisens-site-v2.zip`). Elle est générée par un script Python `build_v2.py` (situé hors du dossier du site) : pour toute modification de structure commune (menu, footer, héros), modifier le script puis le relancer ; pour une retouche ponctuelle de texte, éditer directement le fichier HTML concerné.

### Arborescence (26 fichiers)
- 12 pages publiques : index, soins, travail-corps-complet, specifiques, les-petits-plus, tarifs, formations, techniques-tarifs, prise-en-charge, galerie, qui-suis-je, contact.
- 404.html (personnalisée, hors sitemap) et styleguide.html (design system interne, noindex, hors sitemap).
- css/style.css (unique, tokens dans :root), favicon.svg, sitemap.xml, robots.txt.
- Dossiers images/ et documents/ préparés (vides, avec A-LIRE.txt) pour rapatrier les médias hors de Wix.
- README.md (mode d'emploi et déploiement) et CHANGELOG.md (journal détaillé de toutes les phases).

### Phases réalisées (détail dans CHANGELOG.md)
- Phase 0 + 0-bis — Architecture : 14 pages, page contact centrale de conversion, 404, favicon, sitemap/robots.
- Phase 1 + 1-bis — Design : DA complète (voir §3), menu burger mobile, palier tablette, zones tactiles 44 px, icônes SVG (zéro emoji), styleguide.html.
- Phase 2 — Copywriting/CRO : tous les textes réécrits (bénéfices d'abord, vouvoiement chaleureux), CTA sur chaque page, bande CTA de fin de page, formulaire enrichi.
- Phase 3 — SEO : Title ≤ 68c et descriptions ≤ 155c uniques avec mots-clés locaux (Mouvaux, Lille), 1 seul H1/page, schema.org LocalBusiness + 4 FAQPage (20 questions), canonical, Open Graph, maillage interne.
- Phase 4 — Accessibilité : skip link, aria-label nav, focus visible, alt sur 100 % des images, FAQ en details/summary natifs, prefers-reduced-motion.
- Phase 5 — Performances : lazy loading, preconnect polices, zéro dépendance JS (sauf 10 lignes pour le burger).

### Vérifications passées (script de contrôle)
0 lien interne cassé, 0 image sans alt, 1 H1/page, longueurs Title/description conformes, 0 emoji, burger présent partout, 404 et styleguide hors sitemap.

## 3. Design system (référence : styleguide.html)

- Identité (validée le 15/07/2026) : favicon = monogramme HS cerclé fourni par Flavia ; entête d'accueil = bannière complète fournie par Flavia (mot-marque + monstera + aquarelle + tagline « L'art du toucher, l'esprit en mouvement »), en local dans images/entete-accueil.jpg ; pied de page des 15 pages = fond aquarelle images/fond-pied-de-page.jpg avec textes en encre et titres dorés ; entêtes intérieures = fond aquarelle clair images/fond-entete.jpg (textes foncés par-dessus) ; entête d'accueil épurée : bannière seule avec les boutons « Réserver mon soin » et « Découvrir les formations » superposés à l'image (bas centré, ombre légère, fond translucide sur le contour) ; sous 720 px les boutons passent automatiquement sous l'image ; H1 invisible (sr-only) conservé pour le SEO. Mot-marque texte conservé dans la barre de navigation. Un logo SVG animé avait été essayé puis annulé (archivé dans build_v2.py).
- Couleurs (variables dans :root de style.css) : --sauge #74846a = ACTION (seuls les boutons cliquables primaires) ; --or #b58a52 = PRESTIGE (titres H3, prix, badges — jamais en bouton d'action) ; --encre #35302b = texte ; fonds --fond, --sable, --sauge-pale.
- Typographies : Cormorant Garamond (titres, Google Fonts) + Jost (texte). Max 75 caractères par ligne.
- Boutons : .bouton (sauge, primaire), .bouton.contour (secondaire), .bouton.or (exceptionnel). Min 44 px.
- Icônes : SVG inline trait 1,8 px currentColor, jamais d'emoji.
- Composants : .carte (+ .badge, .pousse), .encadre (/.vert/.blanc), .etapes, .chiffres, .faq, .bande-cta, .barre-mobile, .hero (+ .compact), .reassurance.
- Photos (règle pour le futur shooting) : lumière chaude naturelle, matières lin/bois/pierre/huile, 4:3 cartes de soins, carré galerie, portrait 3:4 pour Flavia.

## 4. Contenu métier à ne pas altérer (source de vérité)

- Tarifs soins : 45 min 60 € / 60 min 80 € / 90 min 110 €. Packs 5 : 275/375/520 €. Packs 10 : 530/730/1000 €. Duo : 120/160/220 €. Soins en cabinet à Mouvaux ; à domicile sur demande : +10 € (20 km max). Rebozo ~3 h à 2 praticiennes 300 € ; 4 mains 60 min 160 €. Fidélité : -20 % au 5e soin, -50 % au 10e. -10 € toute l'année : soignants, militaires, policiers, gendarmes, pompiers. Offre du mois (avril 2026 : Feel Good Stretch 60 min à 65 €) — À METTRE À JOUR CHAQUE MOIS dans tarifs.html.
- Formations (tarifs AF/FE) : Relax corps 3 j 600/700 ; Relax buste 2 j 400/500 ; Sportif N1 3 j 600/700 et N2 2 j 500/600 ; Detox 2,5 j 500/600 ; Etoile 2,5 j 500/600 ; Visage anti-âge 3 j 650/750 + Bonus 2 j 400/500 ; Ventre holistique 3 j 600/700 ; Thai Stretch 4 j 900/1000 ; Hawaïen 2,5 j 500/600 ; Prénatal 2 j 400/500. Inscription jusqu'à J-7. Chiffres : 250 h+ depuis 2021, ~20 stagiaires, 100 % d'attestations.
- Mentions obligatoires : massages bien-être NON thérapeutiques, NON sexuels. Uniquement sur rendez-vous.
- Conformité Qualiopi (charte d'usage vérifiée le 15/07/2026) : le logo n'apparaît QU'au niveau organisme (page prise-en-charge), jamais associé à une formation précise ; mention officielle adjacente au logo (« La certification qualité a été délivrée au titre de la ou des catégories d'actions suivantes : ACTIONS DE FORMATION ») ; affichage en mode « fit » (jamais recadrer/déformer la marque). Toujours écrire « organisme certifié », jamais « formations certifiées ».

## 5. Reste à faire

Par Flavia (bloquant pour l'autonomie complète) :
1. Formspree : créer un compte gratuit sur formspree.io et remplacer VOTRE_ID_FORMSPREE dans contact.html ET formations.html (2 occurrences).
2. Rapatriement Wix — FAIT le 26/07/2026 pour : CGV prestations, CGV formations, certificat Qualiopi, accessibilité handicap, plaquette, organigramme, calendrier 2026 (documents/), portrait Flavia et logo Qualiopi officiel (images/). FAIT aussi le 26/07/2026 : 9 photos galerie (remplacent les 12 Wix, section vidéos supprimée) et les 11 programmes détaillés de formation. TERMINÉ le 26/07/2026 : mentions légales et fiche de réclamation intégrées — 0 lien Wix restant, décrochage complet. Avant résiliation Wix : rebrancher le domaine hominisens.com sur le nouvel hébergement.
3. Confirmer le domaine final ; si différent de www.hominisens.com, adapter canonical (dans build_v2.py) et sitemap.xml.
4. Créatif humain : vrai logo vectoriel + shooting photo (brief dans styleguide.html §5).
5. RGPD : compléter les ⚠️ de confidentialite.html (adresse pro, SIRET, durée de conservation, hébergeur) ; internaliser les polices Google (télécharger les woff2 via gwfh.mranftl.com et créer un dossier fonts/) et les images Wix pour cesser la transmission d'IP à des tiers ; mettre à jour les mentions légales (hébergeur) lors de la migration. Aucune bannière cookies nécessaire tant que le site n'ajoute ni analytics ni traceur.
6. Conformité Qualiopi sur le site — FAIT le 26/07/2026 : logo officiel avec Marianne intégré en local, cartouche blanc, zone de protection, mention obligatoire adjacente, lien certificat local. Reste hors site : les programmes PDF par formation et les attestations ne doivent PAS porter la marque Qualiopi.

Prochaines phases proposées (non commencées) :
- Phase 6 — Mise en ligne GitHub Pages + tests réels (Lighthouse, mobile, formulaire).
- Phase 7 — Conversion avancée : réservation en ligne (Calendly/Fresha), avis Google affichés sur le site (vrais avis, avec accord), carte cadeau payable en ligne (Stripe Payment Links), capture email « offre du mois » (Brevo/MailerLite), Google Business Profile, 1 article SEO/mois, analytics léger.
- Optimisation images (WebP + srcset) une fois les fichiers rapatriés en local.

## 6. Conventions de travail

Chaque phase : modifier uniquement les fichiers nécessaires, consigner dans CHANGELOG.md, vérifier par script (liens, alt, H1, longueurs SEO) avant de clore. Jamais d'avis clients inventés, ni de fausses urgences, ni de pop-ups agressives : le positionnement haut de gamme et honnête prime sur les gains de conversion court-termistes.
