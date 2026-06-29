# LinkedIn — Design System

> Référence visuelle et UI pour le repositionnement de LinkedIn vers les lycéens/étudiants en pré-orientation (Hackathon J1).

---

## 1. Palette de couleurs

### Couleurs principales

| Nom | Hex | Usage |
|-----|-----|-------|
| Blue Primary | `#0a66c2` | CTA, liens, accents principaux |
| Blue Dark | `#0073b1` | Hover, dégradés |
| Blue Tint | `#e8f3fb` | Backgrounds de badges, icônes |
| Black | `#1a1a1a` | Texte principal |
| Gray Mid | `#666666` | Texte secondaire |
| Gray Light | `#f3f2ef` | Background page |
| White | `#ffffff` | Surfaces cartes |

### Couleurs sémantiques

| Nom | Hex | Usage |
|-----|-----|-------|
| Red | `#cc1016` | Badges notification, alertes |
| Green | `#1a7336` | Statut "ouvert aux opportunités" |
| Amber | `#b57900` | Premium, mises en avant |

---

## 2. Typographie

**Police** : Segoe UI / `-apple-system` / `system-ui` (sans-serif)

| Niveau | Taille | Poids | Usage |
|--------|--------|-------|-------|
| Heading | 24px | 700 | Titres de section, nom de profil |
| Title | 18px | 600 | Sous-titres, intitulés de poste |
| Body | 14px | 400 | Contenu des posts, descriptions |
| Caption | 12px | 400 | Métadonnées, localisation, date |
| Link | 14px | 600 | Liens cliquables (couleur `#0a66c2`) |

**Règles typographiques**
- Interlignage body : `1.6`
- Pas de texte en dessous de `11px`
- Les liens sont toujours en `#0a66c2`, jamais soulignés sauf au hover

---

## 3. Espacement — Grille base 4px

| Token | Valeur | Usage |
|-------|--------|-------|
| xs | 4px | Espacement interne minimal |
| sm | 8px | Gap entre icône et label |
| md | 12px | Padding horizontal compact |
| lg | 16px | Padding standard des cartes |
| xl | 24px | Espacement entre sections |
| 2xl | 32px | Marges de mise en page |
| 3xl | 48px | Grands espacements verticaux |

---

## 4. Élévation & Surfaces

| Niveau | Style | Usage |
|--------|-------|-------|
| Plat | `border: 0.5px solid #e0e0e0` | Séparateurs, contours |
| Carte | `box-shadow: 0 1px 3px rgba(0,0,0,.08)` | Cartes profil, posts |
| Modal | `box-shadow: 0 4px 12px rgba(0,0,0,.12)` | Popups, overlays |

**Radius** : `12px` pour les cartes, `20px` pour les pills/boutons, `50%` pour les avatars.

---

## 5. Composants

### Boutons

| Variante | Style | Usage |
|----------|-------|-------|
| Primary | Fond `#0a66c2`, texte blanc, radius `20px` | Action principale (Se connecter, Postuler) |
| Secondary | Contour `#0a66c2`, texte `#0a66c2` | Action secondaire (Suivre) |
| Ghost | Contour `#666`, texte `#666` | Action tertiaire (Message, Plus) |
| Small | Même styles, `padding: 4px 12px`, `font-size: 13px` | Boutons dans les cartes |

**Règle** : un seul bouton Primary par vue. Le padding horizontal est toujours `≥ 16px`.

---

### Navigation principale

Structure : `Logo | Accueil | Réseau | Emplois | Messages | Notifications`

- Icônes Tabler outline, 20px
- Label 11px sous l'icône
- État actif : `border-bottom: 2px solid #1a1a1a`
- Badges notification : fond `#cc1016`, texte blanc, `10px`, radius `8px`

---

### Carte profil

```
┌─────────────────────────┐
│  [Bannière bleue 56px]  │
│ [Avatar 56px]           │
│  Prénom Nom             │
│  Poste · Entreprise     │
│  Ville · N° relation    │
│  [Se connecter] [···]   │
│ ─────────────────────── │
│  1,4k Relations | 38 Articles | 94% Profil │
└─────────────────────────┘
```

- Bannière : fond `#0a66c2`
- Avatar : border `3px solid white`, initiales en `#0a66c2` sur fond `#e8f3fb`
- Stats : `18px 700` pour le chiffre, `11px` muted pour le label

---

### Carte post (Feed)

```
┌──────────────────────────────────────┐
│ [Avatar 40px]  Nom Prénom            │
│                Poste · Entreprise · 1j │
│                                      │
│  Texte du post sur 14px / 1.6...     │
│                                      │
│  [tag] [tag]                         │
│ ──────────────────────────────────── │
│ 👍 J'aime   💬 Commenter   ↗ Partager │
└──────────────────────────────────────┘
```

---

### Tags & Badges

| Type | Style | Usage |
|------|-------|-------|
| Compétence | Fond `#e8f3fb`, texte `#0a66c2` | Skills du profil |
| Ouvert | Fond `#e6f4ea`, texte `#1a7336` | Disponibilité |
| Premium | Fond `#fff7e6`, texte `#b57900` | Abonnement |
| Notification | Fond `#cc1016`, texte blanc | Compteurs non lus |

**Format** : `padding: 3px 10px`, `border-radius: 20px`, `font-size: 12px`, `font-weight: 500`

---

### Champ de recherche

- Icône loupe intégrée à gauche (`padding-left: 36px`)
- Border `1.5px solid #e0e0e0`, focus `#0a66c2`
- Radius `8px`
- Placeholder en gris muted

---

## 6. Logo & Branding

**Ne jamais recréer le logo manuellement** — toujours utiliser les fichiers officiels des dossiers de branding.

### Fichiers disponibles

| Fichier | Dossier | Usage |
| ------- | ------- | ----- |
| `LI-In-Bug.png` | `in-logo/` | Logo "in" bleu — usage principal sur fond blanc ou clair |
| `InBug-White.png` | `in-logo/` | Logo "in" blanc — sur fond coloré ou sombre |
| `InBug-Black.png` | `in-logo/` | Logo "in" noir — usage monochrome |
| `LI-Logo.png` | `linkedin-logo/` | Logotype complet "LinkedIn" — headers, splash screen |

### Règles d'utilisation

- **Écran de connexion / splash** : utiliser `LI-In-Bug.png` centré, taille `48×48px` minimum.
- **Navigation principale** : utiliser `LI-In-Bug.png` à `28×28px` en haut à gauche.
- **Sur fond sombre** (ex. bannière, overlay) : utiliser `InBug-White.png`.
- **Impression / noir & blanc** : utiliser `InBug-Black.png`.
- Ne jamais étirer, recolorer, ni reconstruire le logo avec des formes géométriques.
- Zone de protection minimale : `8px` autour du logo sur tous les côtés.

---

## 7. Iconographie

**Librairie unique** : [Tabler Icons](https://tabler.io/icons) — variante **outline** exclusivement.  
**Jamais d'emoji** — les emoji sont interdits dans l'interface (rendu incohérent selon l'OS, non accessible, non scalable). Utiliser systématiquement une icône Tabler à la place.

### Tailles

| Contexte | Taille | Épaisseur de trait |
| -------- | ------ | ------------------ |
| Navigation principale | 24px | 1.5px |
| Actions inline (boutons, champs) | 20px | 1.5px |
| Indicateurs compacts (badges, tags) | 16px | 1.5px |

### Couleur

- Hérite toujours de la couleur du texte parent (`currentColor`).
- Sur fond coloré : blanc `#ffffff`.
- Icône active / sélectionnée : `#0a66c2`.
- Icône désactivée : `#b0b0b0`.

### Icônes de référence

| Icône Tabler | Usage |
| ------------ | ----- |
| `ti-home` | Accueil |
| `ti-users` | Réseau |
| `ti-briefcase` | Emplois |
| `ti-message-circle` | Messages |
| `ti-bell` | Notifications |
| `ti-user-plus` | Se connecter / Suivre |
| `ti-send` | Message direct |
| `ti-thumb-up` | J'aime |
| `ti-share` | Partager |
| `ti-search` | Recherche |
| `ti-eye` / `ti-eye-off` | Afficher / masquer mot de passe |
| `ti-chevron-right` | Navigation, liens |
| `ti-x` | Fermer, effacer |
| `ti-check` | Confirmation, succès |
| `ti-alert-circle` | Erreur, avertissement |
| `ti-info-circle` | Information |
| `ti-photo` | Photo de profil / bannière |
| `ti-edit` | Modifier |
| `ti-dots` | Menu contextuel (3 points) |

---

## 8. Champs de formulaire

Tous les champs du produit suivent une grammaire visuelle unique. Ne pas inventer de variantes locales.

### Anatomie d'un champ

```text
[Label — 13px / 600]
┌─────────────────────────────────┐
│  [icône 20px]   Valeur / Placeholder          │
└─────────────────────────────────┘
[Message d'aide ou d'erreur — 12px]
```

- Le **label** est toujours au-dessus du champ, jamais à l'intérieur (pas de floating label).
- L'**icône** est optionnelle, alignée à gauche avec `padding-left: 36px` si présente.
- Le **message** apparaît uniquement en état erreur ou aide contextuelle.

### Dimensions

| Propriété | Valeur |
| --------- | ------ |
| Hauteur | 48px |
| Padding horizontal | 12px (16px si icône) |
| Border-radius | 4px |
| Font-size valeur | 15px / 400 |
| Font-size label | 13px / 600 |
| Font-size message | 12px / 400 |

### États

| État | Bordure | Fond | Texte |
| ---- | ------- | ---- | ----- |
| Default | `1.5px solid #e0e0e0` | `#ffffff` | `#1a1a1a` |
| Focus | `1.5px solid #0a66c2` | `#ffffff` | `#1a1a1a` |
| Erreur | `1.5px solid #cc1016` | `#fff5f5` | `#1a1a1a` |
| Désactivé | `1px solid #e0e0e0` | `#f3f2ef` | `#b0b0b0` |
| Placeholder | — | — | `#999999` |

### Icônes dans les champs

- Utiliser exclusivement des icônes **Tabler outline** — jamais d'emoji.
- Taille fixe : **20px**, couleur `#666666` par défaut, `#0a66c2` au focus.
- Icône de mot de passe : `ti-eye` / `ti-eye-off` cliquable à droite du champ.
- Icône de recherche : `ti-search` à gauche, non cliquable.

### Règles générales

1. Un seul type de champ par formulaire — ne pas mélanger les styles.
2. Espacement entre deux champs : `16px` (token `--space-lg`).
3. Le label et le champ sont toujours groupés dans un même conteneur vertical.
4. Les champs obligatoires n'ont pas d'astérisque — la validation se fait à la soumission avec message d'erreur explicite.

---

## 9. Images & Avatars

Toutes les images sont contenues dans une **boîte image simple** — un frame avec `overflow: hidden` et un fond placeholder neutre. Jamais d'image posée directement sur le canvas sans conteneur.

### Avatar utilisateur

| Taille | Contexte | Forme |
| ------ | -------- | ----- |
| 44px | Carte post, commentaires | Cercle (`border-radius: 50%`) |
| 56px | Carte profil | Cercle |
| 32px | Notifications, suggestions | Cercle |

**Placeholder** : fond `#e0e0e0`, icône `ti-user` centrée en `#aaaaaa`, bordure `1px solid #d0d0d0`.  
**Image réelle** : `object-fit: cover`, même conteneur circulaire.  
**Bordure sur fond coloré** : `3px solid #ffffff` pour détacher l'avatar de la bannière.

### Image de post / média

| Propriété | Valeur |
| --------- | ------ |
| Ratio | 16:9 (paysage) ou 1:1 (carré) |
| Border-radius | `8px` |
| Object-fit | `cover` |
| Placeholder | Fond `#f3f2ef`, icône `ti-photo` centrée en `#b0b0b0` |

### Bannière de profil

| Propriété | Valeur |
| --------- | ------ |
| Hauteur | 56px (mobile), 96px (desktop) |
| Object-fit | `cover` |
| Placeholder | Fond `#0a66c2` (bleu LinkedIn) |

### Bibliothèques d'images recommandées

Pour les maquettes et prototypes, utiliser des photos réelles issues de ces sources :

| Source | Usage | URL |
| ------ | ----- | --- |
| **RandomUser.me** | Avatars / portraits réalistes | `https://randomuser.me/api/portraits/women/{n}.jpg` |
| **Unsplash** | Photos de contenu, bannières | `https://unsplash.com` |
| **UI Faces** | Avatars diversifiés | `https://uifaces.co` |
| **Picsum Photos** | Images génériques (paysages, objets) | `https://picsum.photos/{w}/{h}` |

**Règle** : dans Figma, importer l'image via upload dans la boîte image (`scaleMode: FILL`). Ne jamais laisser de fond bleu ou de texte initiales quand une photo est disponible.

### Bonnes pratiques

1. **Toujours utiliser une boîte image** — un `<div>` ou frame avec `overflow: hidden` + dimensions fixes. Ne jamais laisser une image se redimensionner librement.
2. **Placeholder systématique** — tant que l'image n'est pas chargée, afficher le fond neutre + l'icône Tabler correspondante (`ti-user` pour avatar, `ti-photo` pour média).
3. **Pas d'emoji** dans les placeholders — utiliser uniquement des icônes Tabler outline.
4. **Clipper le contenu** — `clipsContent: true` dans Figma, `overflow: hidden` en CSS.
5. **Jamais de fond bleu sur un avatar** sauf s'il s'agit d'initiales (état de fallback texte, pas image).

---

## 10. Règles de design

1. **Clarté avant tout** — pas de gradients, pas d'ombres lourdes. Flat design avec des bordures fines (`0.5px`).
2. **Le bleu est réservé aux actions** — `#0a66c2` uniquement pour les CTA, liens, et éléments interactifs.
3. **Hiérarchie par le poids** — différencier l'information par `font-weight` (400 / 600 / 700), pas par la couleur.
4. **Mobile-first** — colonnes uniques en dessous de 480px, grille 2 colonnes de 480 à 768px.
5. **Feedback immédiat** — tout élément interactif a un état hover visible (`background: #f3f2ef` ou `border-color: #0a66c2`).
6. **Espacement généreux** — minimum `16px` de padding interne dans les cartes.

---

## 10. Tokens CSS (référence développeur)

```css
:root {
  /* Couleurs */
  --li-blue: #0a66c2;
  --li-blue-dark: #0073b1;
  --li-blue-tint: #e8f3fb;
  --li-black: #1a1a1a;
  --li-gray-mid: #666666;
  --li-gray-bg: #f3f2ef;
  --li-white: #ffffff;
  --li-red: #cc1016;
  --li-green: #1a7336;
  --li-amber: #b57900;

  /* Typographie */
  --font-base: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --text-heading: 700 24px/1.3 var(--font-base);
  --text-title: 600 18px/1.4 var(--font-base);
  --text-body: 400 14px/1.6 var(--font-base);
  --text-caption: 400 12px/1.5 var(--font-base);

  /* Espacement */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 12px;
  --space-lg: 16px;
  --space-xl: 24px;
  --space-2xl: 32px;

  /* Radius */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-pill: 20px;
  --radius-circle: 50%;

  /* Ombres */
  --shadow-card: 0 1px 3px rgba(0, 0, 0, 0.08);
  --shadow-modal: 0 4px 12px rgba(0, 0, 0, 0.12);

  /* Bordures */
  --border-default: 0.5px solid #e0e0e0;
  --border-strong: 1.5px solid #0a66c2;
}
```

---

*Design System — LinkedIn Repositionnement · Hackathon J1 · 2026*
