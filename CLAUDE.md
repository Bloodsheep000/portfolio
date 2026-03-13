# CLAUDE.md — Règles de présentation du Portfolio

Ce fichier définit les règles de présentation à respecter sur **tout** le portfolio.
Toute modification de la présentation doit être répercutée ici.

---

## Identité visuelle

- **Nom affiché dans le logo** : `Hugo Léonardi` (sur toutes les pages, sans exception)
- **Titre du portfolio** : `Portfolio BTS SIO SISR`
- **Format des balises `<title>`** : `[Nom de la page] - Portfolio BTS SIO SISR`
  - Ex : `Mon CV - Portfolio BTS SIO SISR`, `Mes Missions - Portfolio BTS SIO SISR`
  - Exception : la page d'accueil → `Portfolio - BTS SIO SISR`
- **Footer** : `© 2025 - Hugo Léonardi - Portfolio BTS SIO SISR` (identique sur toutes les pages)

---

## Navigation

La barre de navigation est identique sur toutes les pages. Ordre des liens :

1. `Accueil` → `index.html`
2. `Technicentre de Villeneuve Saint Georges` → `entreprise.html`
3. `CV` → `cv.html`
4. `Projets` → `projets.html`
5. `Missions` → `missions.html`
6. `Veille` → `veille.html`

Le lien correspondant à la page courante porte la classe `class="active"`.

---

## Palette de couleurs (variables CSS)

Définie dans `style.css`, à ne pas modifier sans mettre à jour ce fichier.

| Variable              | Valeur     | Usage                          |
|-----------------------|------------|--------------------------------|
| `--primary-color`     | `#2563eb`  | Boutons, liens actifs, titres  |
| `--primary-dark`      | `#1e40af`  | Gradients, hover               |
| `--secondary-color`   | `#64748b`  | Texte secondaire               |
| `--accent-color`      | `#0ea5e9`  | Accents, highlights            |
| `--text-dark`         | `#1e293b`  | Texte principal                |
| `--text-light`        | `#64748b`  | Texte secondaire               |
| `--bg-light`          | `#f8fafc`  | Fond sections claires          |
| `--bg-white`          | `#ffffff`  | Fond cartes                    |
| `--border-color`      | `#e2e8f0`  | Bordures                       |
| `--success-color`     | `#10b981`  | Éléments validés / complétés   |

---

## Typographie

- **Police** : `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`
- **Interligne** : `1.6` (corps), `1.8` (blocs de texte)
- **Tailles de titres** :
  - `h1` hero : `3rem`
  - `h1` page-header : `2.5rem`
  - `h2` : `2rem`
  - `h3` : `1.5rem`
  - `h4` : `1.2rem`

---

## Règles d'usage des emojis

| Niveau         | Emoji autorisé ? | Remarque                                              |
|----------------|------------------|-------------------------------------------------------|
| `<h1>`         | ❌ Non           | Jamais d'emoji dans les titres de page-header         |
| `<h2>`         | ❌ Non           | Titres de section propres, sans emoji                 |
| `<h3>`         | ✅ Oui           | Emojis acceptés pour les catégories (missions, etc.)  |
| `<h4>` et +    | ✅ Oui           | Emojis acceptés                                       |
| `info-box`     | ✅ Oui           | Emojis acceptés dans les blocs info                   |
| `feature-card` | ✅ Oui           | Emojis dans les icônes de cartes                      |

---

## Structure des pages

### Page d'accueil (`index.html`)
- Section hero avec gradient bleu → bleu foncé
- Grille de 4 feature-cards de navigation rapide
- Deux boutons CTA : `Mon CV` (btn-primary) + `Mes Projets` (btn-secondary)

### Pages internes (toutes sauf index)
- `<section class="page-header">` avec gradient bleu (même que hero)
  - `<h1>` : titre de la page, **sans emoji**
  - `<p>` : sous-titre descriptif court
- `<section class="content-section">` pour le contenu
- Contenu organisé en `<div class="content-card">` (fond blanc, ombre, border-radius 12px)

### Pages de détail projet (`projet1.html`, `projet2.html`)
- Fil d'Ariane (`breadcrumb`) → lien retour vers `projets.html`
- `<section class="project-detail-header">` (même gradient)
  - Badge projet, `h1`, sous-titre, bouton PDF
- `<section class="project-detail-content">` pour le contenu

---

## Composants réutilisables

### Boutons
- `.btn.btn-primary` : fond blanc, texte bleu — CTA principal
- `.btn.btn-secondary` : transparent, bordure blanche — CTA secondaire (sur fond bleu)
- `.btn.btn-full` : pleine largeur (dans les cartes de projet)

### Tags technologiques
- `.tag-small` : petit badge bleu, pour les technologies dans les missions/projets

### Cartes de mission (`.mission-item`)
- Fond clair (`--bg-light`), bordure gauche bleue 4px
- Structure : `h4` titre, `<p><strong>Contexte/Objectifs</strong></p>`, `<ul>`, `.mission-tags`, lien PDF

### Timeline CV (`.timeline-item`)
- Grille 2 colonnes : date (`150px`) + contenu (`1fr`)
- Date en `--primary-color`

---

## Fichiers

| Fichier           | Rôle                                      |
|-------------------|-------------------------------------------|
| `index.html`      | Accueil                                   |
| `cv.html`         | Curriculum Vitae                          |
| `entreprise.html` | Présentation SNCF Voyageurs / Technicentre|
| `missions.html`   | Missions entreprise et école (onglets)    |
| `projets.html`    | Liste des projets BTS                     |
| `projet1.html`    | Détail Projet 1 (Nextcloud/AWS/Terraform) |
| `projet2.html`    | Détail Projet 2 (à compléter)             |
| `veille.html`     | Veille technologique DevOps               |
| `style.css`       | Feuille de style unique (2292 lignes)     |
| `docs/`           | PDFs des comptes-rendus et fiches missions|
| `images/`         | Photos et schémas                         |
