# grille-website

Site de présentation de l'application iOS **grille** — page "coming soon" en attente de la sortie sur l'App Store.

## À propos

Ce dépôt contient uniquement la page web vitrine de l'application **grille**, une app iOS qui affiche les grilles de programmes TV françaises. La page est destinée au marché français et affiche un message d'accueil en attendant la disponibilité de l'app.

Les données de programmes TV sont gérées par un pipeline séparé : [`grille-backend`](https://github.com/Louis-XII/grille-backend).

## Stack technique

- **HTML5** pur — aucun framework, aucune dépendance JavaScript
- **CSS** intégré directement dans le `<head>` de `index.html`
- **Mobile-first** via la balise `<meta name="viewport">`
- **Police système** : `-apple-system, sans-serif` pour une cohérence visuelle avec iOS

Aucune étape de build n'est nécessaire. Le site peut être servi tel quel par n'importe quel hébergeur de fichiers statiques.

## Structure des fichiers

```
grille-website/
├── index.html      # Page principale (coming soon)
└── README.md       # Ce fichier
```

## Développement local

Aucun prérequis n'est nécessaire pour travailler sur ce projet.

```bash
# Cloner le dépôt
git clone https://github.com/Louis-XII/grille-website.git
cd grille-website

# Ouvrir directement dans le navigateur
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

Pour utiliser un serveur local (optionnel) :

```bash
python3 -m http.server 8080
# puis ouvrir http://localhost:8080
```

## Personnalisation

Tous les éléments modifiables se trouvent dans `index.html` :

| Élément | Balise | Description |
|---|---|---|
| Texte d'accueil | `<p>Bienvenue...` | Message affiché sous le titre |
| Lien App Store | `href="#"` dans `.badge` | Remplacer `#` par l'URL réelle sur l'App Store |
| Couleur principale | `color: #007aff` | Bleu iOS par défaut |
| Couleur de fond | `background: #f0f0f5` | Gris clair de la page |
| Titre de l'onglet | `<title>grilleapp</title>` | Nom affiché dans l'onglet du navigateur |

## Déploiement

Le site est conçu pour être déployé sur **GitHub Pages** :

1. Aller dans **Settings → Pages** du dépôt
2. Sélectionner la branche `main` et le dossier racine `/`
3. Cliquer sur **Save**

Le site sera automatiquement publié après chaque `git push` sur `main`. Aucune configuration supplémentaire n'est requise.

## Contribution

1. Forker le dépôt
2. Créer une branche : `git checkout -b feat/ma-modification`
3. Effectuer les modifications dans `index.html`
4. Ouvrir une Pull Request

> Ce projet est intentionnellement minimaliste. Les ajouts de frameworks JavaScript ou de dépendances doivent être justifiés par une vraie nécessité fonctionnelle.

## Liens

- Backend (pipeline EPG) : [Louis-XII/grille-backend](https://github.com/Louis-XII/grille-backend)
- Application iOS sur l'App Store : *(à venir)*
