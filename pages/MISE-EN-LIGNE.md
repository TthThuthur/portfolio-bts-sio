# Mise en ligne du portfolio sur GitHub Pages

Ce guide explique pas à pas comment publier le portfolio en ligne via GitHub Pages.
Aucune installation de logiciel n'est nécessaire — tout se fait depuis le navigateur.

## Vue d'ensemble

À l'arrivée :
- Le portfolio sera accessible à une URL publique du type
  `https://<username>.github.io/<repo>/`
- Toute modification du texte se fera directement depuis le navigateur, sur GitHub
- Le site sera mis à jour automatiquement en moins d'une minute après chaque modification
- Le tout est gratuit, sans limite de durée, sans publicité

---

## Étape 1 — Créer le dépôt GitHub

1. Se connecter sur **github.com** avec le compte d'Arthur.
2. En haut à droite, cliquer sur le bouton **"+"** puis **"New repository"**.
3. Remplir le formulaire :
   - **Repository name** : `portfolio-bts-sio` (ou un autre nom court, en minuscules,
     sans espaces — ce nom apparaîtra dans l'URL)
   - **Description** : `Portfolio numérique BTS SIO option SLAM — Session 2026`
   - Cocher **"Public"** (obligatoire pour GitHub Pages gratuit)
   - **NE PAS** cocher "Add a README file" (on a déjà le nôtre dans le ZIP)
   - **NE PAS** ajouter de .gitignore ni de licence (on les ajoutera après si besoin)
4. Cliquer sur **"Create repository"** en bas.

GitHub redirige vers une page presque vide qui dit "Quick setup" avec une URL
du type `https://github.com/<username>/portfolio-bts-sio.git`.

---

## Étape 2 — Téléverser les fichiers du portfolio

Sur la page d'accueil du dépôt fraîchement créé :

1. Repérer le lien **"uploading an existing file"** dans le bloc gris du milieu
   (sous "...or push an existing repository from the command line"), OU bien
   cliquer sur **"Add file" > "Upload files"** en haut à droite.

2. **Important** : ne pas téléverser le ZIP, mais le **contenu** du dossier
   `portfolio-arthur/`.
   - Ouvrir le ZIP sur l'ordinateur
   - Extraire le contenu (clic droit > "Extraire tout")
   - Ouvrir le dossier `portfolio-arthur/` extrait
   - Sélectionner **TOUT son contenu** (Ctrl+A) :
     `index.html`, `README.md`, `GUIDE-EDITION.md`, `robots.txt`, `sitemap.xml`,
     et les dossiers `css/`, `js/`, `assets/`, `pages/`, `attestations/`
   - Glisser-déposer la sélection dans la zone "Drag files here" du navigateur

3. Patienter pendant le téléversement (les PDF et les images peuvent prendre
   quelques secondes).

4. En bas de la page, dans **"Commit changes"** :
   - Message de commit : `Initial commit — portfolio version 1`
   - Laisser **"Commit directly to the main branch"**
   - Cliquer sur **"Commit changes"**

GitHub revient sur la page principale du dépôt qui affiche maintenant
tous les fichiers.

---

## Étape 3 — Activer GitHub Pages

1. Dans le dépôt, cliquer sur l'onglet **"Settings"** (tout en haut à droite,
   à côté de "Insights").
2. Dans le menu de gauche, cliquer sur **"Pages"** (sous la section "Code and automation").
3. Dans la section **"Build and deployment"** :
   - **Source** : laisser sur "Deploy from a branch"
   - **Branch** : sélectionner **"main"** dans le premier menu déroulant
   - Laisser le second menu sur **"/ (root)"**
   - Cliquer sur **"Save"**
4. La page se recharge. Patienter une minute.
5. Recharger la page. En haut, un encadré vert affiche :
   "Your site is live at `https://<username>.github.io/portfolio-bts-sio/`"

C'est l'URL publique du portfolio.

---

## Étape 4 — Vérifier le rendu

1. Cliquer sur l'URL pour ouvrir le portfolio.
2. Vérifier :
   - La page d'accueil s'affiche avec la photo d'Arthur et le hero
   - La navigation entre les pages fonctionne
   - Les images se chargent (logo Mention TB, portrait page parcours)
   - Les liens vers les PDF d'attestation fonctionnent
3. Si quelque chose manque, attendre 2-3 minutes (la première mise en ligne
   peut être lente) et recharger.

---

## Étape 5 — Ajuster les liens du sitemap

Le fichier `sitemap.xml` contient des URLs avec un username GitHub par défaut
(`arthur-lecomte`). Si le username réel d'Arthur est différent, il faut le
corriger :

1. Dans le dépôt GitHub, cliquer sur le fichier **`sitemap.xml`**.
2. Cliquer sur le crayon **"Edit"** en haut à droite.
3. Faire un Ctrl+H ou rechercher manuellement et remplacer toutes les
   occurrences de `arthur-lecomte.github.io/portfolio-bts-sio` par la vraie
   URL (visible dans Settings > Pages).
4. Cliquer sur **"Commit changes"** en bas, puis confirmer.

Faire la même chose pour `robots.txt`.

---

## Modifier un texte plus tard

À chaque fois qu'Arthur veut modifier un texte :

1. Aller sur le dépôt GitHub : `https://github.com/<username>/portfolio-bts-sio`
2. Naviguer vers le fichier à modifier (ex. `pages/parcours.html`)
3. Cliquer sur le crayon **"Edit"** (icône en haut à droite du contenu du fichier)
4. Modifier le texte (voir le fichier `GUIDE-EDITION.md` pour les bonnes pratiques)
5. En bas, dans "Commit changes" :
   - Message : décrire brièvement la modification (ex. `Mise à jour objectif pro`)
   - Cliquer sur **"Commit changes"**
6. Le site est mis à jour automatiquement en 30 à 60 secondes

GitHub Actions s'occupe du déploiement, sans aucune intervention.

---

## Faire indexer le portfolio par Google

Pour que le portfolio apparaisse dans les résultats de recherche Google :

1. Aller sur **search.google.com/search-console**
2. Cliquer sur **"Ajouter une propriété"**
3. Choisir **"Préfixe d'URL"** et saisir l'URL du portfolio
4. Suivre la procédure de vérification (le plus simple : balise meta dans le
   `<head>` de l'index.html — Search Console fournit le code à coller)
5. Une fois vérifié, soumettre le `sitemap.xml` dans la section "Sitemaps"

Délai d'indexation : 1 à 7 jours typiquement.

---

## Cas particulier : utiliser un nom de domaine personnalisé

Si Arthur souhaite plus tard une URL plus propre (ex. `arthur-lecomte.fr` ou
`portfolio.arthur-lecomte.fr`), c'est possible avec un nom de domaine acheté
ailleurs (OVH, Gandi, etc.). La procédure est documentée par GitHub :
[https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

C'est une étape facultative, à voir éventuellement après le BTS.

---

## Avantage pour le dossier d'Arthur

Le fait d'héberger le portfolio sur GitHub Pages avec un workflow de
modification continue est un atout supplémentaire pour la soutenance :

- Cela démontre une **maîtrise du contrôle de version** (Git, GitHub)
- Cela illustre une démarche de **déploiement continu** (CI/CD)
- C'est une compétence métier directement valorisable

Arthur peut le mentionner brièvement dans sa présentation orale, sur la page
parcours ou sur la page Veille comme un point d'auto-formation.
