# Portfolio BTS SIO — Arthur LECOMTE

Portfolio numérique pour l'épreuve E5 — Support et mise à disposition de services informatiques.
Session 2026 · Lycée Raoul Follereau · Nevers.

## Comment consulter le portfolio

### En ligne

Le portfolio est hébergé sur GitHub Pages, accessible publiquement à l'adresse :
`https://<username>.github.io/<repo>/`

(URL définitive à compléter une fois le dépôt en place.)

### En local (pour l'oral E5)

Site web statique en HTML/CSS/JS pur — aucune installation nécessaire.
Ouvrir `index.html` dans un navigateur (Chrome, Firefox, Edge…).

Pour la version sur clé USB :
1. Copier l'intégralité du dossier `portfolio-arthur/` sur la clé USB.
2. Le jour de l'oral, brancher la clé sur l'ordinateur.
3. Ouvrir `portfolio-arthur/index.html` dans un navigateur.
4. Tout fonctionne sans connexion internet (les polices Google Fonts sont
   chargées en ligne mais le site reste lisible avec les polices système
   en secours).

## Modifier le contenu

Voir le fichier **GUIDE-EDITION.md** pour les instructions détaillées de
modification du texte. En résumé : les zones de texte modifiables sont
encadrées dans les fichiers HTML par des commentaires `<!-- TEXTE
MODIFIABLE -->` bien visibles.

## Structure du portfolio

```
portfolio-arthur/
├── index.html                          # Page d'accueil
├── README.md                           # Ce fichier
├── GUIDE-EDITION.md                    # Guide pour modifier les textes
├── robots.txt                          # Autorisation des moteurs de recherche
├── sitemap.xml                         # Plan du site pour Google
├── css/
│   └── style.css                       # Feuille de style unique
├── js/
│   └── main.js                         # Interactions légères
├── assets/
│   ├── arthur-avatar.jpg               # Avatar circulaire (accueil)
│   ├── arthur-portrait.jpg             # Portrait (page parcours)
│   ├── logo-mention-tb.png             # Logo Mention TB (gradient)
│   ├── logo-mention-tb-sm.png          # Logo petit format
│   └── logo-mention-tb-aplats.png      # Logo en aplats (alternative)
├── pages/
│   ├── parcours.html                   # Mon parcours (phase 1 oral)
│   ├── competences.html                # Les 6 activités du bloc 1
│   ├── situations.html                 # Index des situations pro
│   ├── situation1-discord.html         # Stage 1 : Discord + SEO
│   ├── situation2-websciences.html     # Stage 2 : Websciences
│   ├── tableau-synthese.html           # Tableau de synthèse (obligatoire E5)
│   ├── attestations.html               # Attestations & documents
│   └── veille.html                     # Veille technologique
└── attestations/
    ├── convention-stage1-discord.pdf   # Convention stage 1 (juin-juillet 2025)
    └── attestation-stage2-websciences.pdf  # Attestation stage 2 (janv-mars 2026)
```

## Identité visuelle

Charte cohérente avec la plateforme Websciences (continuité du dossier pro) :
- Couleurs : noir profond (#0a0a0c), or (#d4a84b), blanc cassé (#e8e6df)
- Typographie : Cormorant Garamond (titres), Outfit (corps), JetBrains Mono (code)

## Stages

- **Stage 1** : 02/06/2025 → 04/07/2025 (5 semaines, 24 jours effectifs)
  Création d'un serveur Discord pédagogique + campagne de référencement Google
- **Stage 2** : 19/01/2026 → 13/03/2026 (8 semaines)
  Conception et développement de la plateforme web Websciences (PHP MVC, MySQL)

Tuteur dans les deux stages : M. Thibaut Berdagué-Coutelier, gérant de Mention TB.
Enseignante référente : Mme Anita Guatteri.

## Technologies utilisées

Ce portfolio est un **support de soutenance** conçu pour présenter mes deux situations professionnelles. La réalisation technique principale présentée est la **plateforme Websciences** (situation 2) : architecture MVC PHP/MySQL, génération PDF Python/ReportLab, sécurité applicative.

Le portfolio en lui-même est un site statique (HTML5, CSS3, JavaScript), hébergé sur GitHub Pages.
