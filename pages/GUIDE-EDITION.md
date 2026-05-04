# Guide d'édition du portfolio

Ce fichier explique comment modifier facilement les textes du portfolio
sans connaissance technique avancée.

## Repérer les textes modifiables

Dans chaque page HTML, les textes faciles à modifier sont encadrés par
des commentaires en blocs très visibles :

```
<!-- ═══════════════════════════════════════════════════════════════
     TEXTE MODIFIABLE — [description du contenu]
     ═══════════════════════════════════════════════════════════════ -->

<p>...le texte modifiable...</p>

<!-- ═══════════════════════════════════════════════════════════════
     FIN DU TEXTE MODIFIABLE
     ═══════════════════════════════════════════════════════════════ -->
```

Pour modifier un texte, il suffit de :
1. Ouvrir le fichier sur GitHub
2. Cliquer sur le crayon « Edit »
3. Repérer le bloc encadré par les commentaires
4. Modifier UNIQUEMENT le texte entre les balises HTML
5. Cliquer sur « Commit changes »

## Règles à respecter

### Ce qu'on peut modifier librement

✅ Le texte entre `<p>` et `</p>`
✅ Le texte entre `<strong>` et `</strong>` (mots en gras)
✅ Le texte entre `<em>` et `</em>` (mots en italique gold)
✅ Le texte entre `<h2>`, `<h3>`, `<h4>` et leurs balises de fermeture
✅ Le texte entre `<li>` et `</li>` (éléments de liste)

### Ce qu'il NE FAUT PAS toucher

❌ Les balises HTML elles-mêmes : `<p>`, `<div>`, `<span class="...">`, etc.
❌ Les attributs : `class="..."`, `href="..."`, `src="..."`
❌ Les balises de structure : `<div>`, `<section>`, `<article>`
❌ Les liens : `<a href="...">` (sauf si on veut changer la cible)

### Caractères spéciaux

Pour insérer certains caractères dans le HTML, utiliser :
- `&amp;` au lieu de `&`
- `&lt;` au lieu de `<`
- `&gt;` au lieu de `>`
- `&nbsp;` pour un espace insécable
- `&eacute;` pour `é` (optionnel, le `é` direct fonctionne en UTF-8)

## Cas pratiques

### Modifier l'âge d'Arthur dans la page parcours

Fichier : `pages/parcours.html`
Chercher : `j'ai 22 ans`
Remplacer par : `j'ai 23 ans`

### Modifier la description courte du stage 1 sur la page d'accueil

Fichier : `index.html`
Chercher le bloc :
```
<!-- ═══ TEXTE MODIFIABLE — Description courte du stage 1 (carte d'accueil) ═══ -->
<p class="stage-desc">...texte à modifier...</p>
<!-- ═══ FIN ═══ -->
```
Modifier le texte entre les balises `<p>` et `</p>`.

### Ajouter un élément à une liste

Si on a :
```
<ul>
  <li>Premier élément</li>
  <li>Second élément</li>
</ul>
```

Pour ajouter un élément, copier une ligne `<li>...</li>` et la coller :
```
<ul>
  <li>Premier élément</li>
  <li>Second élément</li>
  <li>Nouvel élément</li>
</ul>
```

## En cas de doute

Si une modification casse l'affichage du site :
1. Aller dans l'historique du dépôt GitHub (onglet « Commits »)
2. Trouver la dernière version qui fonctionnait
3. Cliquer sur « Revert » pour annuler la modification

Aucune modification n'est définitive, GitHub garde tout l'historique.

## Pages du portfolio et leur rôle

| Fichier | Contenu |
|---|---|
| `index.html` | Page d'accueil, hero, présentation courte, cartes des stages |
| `pages/parcours.html` | Présentation détaillée, cursus, objectif professionnel |
| `pages/competences.html` | Les 6 activités du bloc 1 du référentiel BTS SIO |
| `pages/situations.html` | Index des deux situations professionnelles |
| `pages/situation1-discord.html` | Détail du stage 1 (Discord + SEO) |
| `pages/situation2-websciences.html` | Détail du stage 2 (Websciences) |
| `pages/tableau-synthese.html` | Tableau de synthèse (obligatoire E5) |
| `pages/attestations.html` | Liens vers les PDF officiels |
| `pages/veille.html` | Veille technologique sur la sécurité web |
