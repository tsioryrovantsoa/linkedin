# Avenir — Design System pour Figma

Tout pour reconstruire et modifier Avenir directement dans Figma.

## 1 · Tokens → variables / styles Figma
Fichier : **`avenir.tokens.json`** (format **Tokens Studio for Figma**).

1. Dans Figma, installe le plugin **« Tokens Studio for Figma »** (gratuit).
2. Plugin → menu → **Import** (ou onglet **Tools → Load from file/JSON**) → charge `avenir.tokens.json`.
3. Le set **`avenir`** apparaît. Clique **« Create styles »** (et/ou exporte en **Variables**) pour générer les styles couleur / texte / effets dans le fichier.
4. Modifie les valeurs dans Tokens Studio → tout se met à jour. Les tokens **sémantiques** (`semantic.brand`, `surface-card`…) sont des **alias** qui pointent vers les couleurs de base : change `indigo.500` et tout suit.

**Contenu :** `color` (indigo, coral, iris, ink, plum, cream, line, jade, gold, rose, linkedin) · `semantic` (alias) · `gradient` (fills dégradés) · `spacing` · `borderRadius` · `font` (familles, poids, tailles, interlignes, interlettrage) · `typography` (styles composites display/h1/…/caption) · `boxShadow`.

> ⚠️ **Deux bleus distincts** : `color.indigo.*` = interface (violet) ; `color.linkedin.*` (#0A66C2, cyan) = **endossement uniquement** (ponts LinkedIn). Ne pas confondre.

## 2 · Polices
Installe depuis Google Fonts (gratuit) avant d'appliquer les styles texte :
- **Bricolage Grotesque** (display / titres)
- **Figtree** (corps / UI)
- **Space Grotesk** (chiffres tactiques)

## 3 · Logos → vecteurs éditables
Dossier **`logos/`** (11 SVG). Glisse-dépose un SVG dans Figma : il arrive en vecteur éditable (le mark est 100 % géométrie). Le wordmark utilise Bricolage Grotesque — installe la police ou vectorise le texte.

## 4 · Écrans & composants (optionnel)
Pour récupérer les écrans/composants en frames Figma éditables, utilise le plugin **« html.to.design »** et importe les pages HTML du design system (UI kit `ui_kits/avenir-app/index.html`, charte `explorations/charte.html`). Elles arrivent en calques natifs que tu peux retravailler.

---
*Avenir — « Première lumière ». Primaire indigo calme, corail en accent, neutres crème/plum, endossement LinkedIn.*
