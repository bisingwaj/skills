---
name: ui-ux-pro-max
description: Fournit une expertise avancée en UI/UX pour concevoir des systèmes de design, des palettes de couleurs et des interfaces modernes basées sur des données et des meilleures pratiques.
---

# UI-UX Pro Max

Cette compétence permet d'accéder à un vaste ensemble de données et de scripts de recherche pour concevoir des interfaces utilisateur (UI) et des expériences utilisateur (UX) professionnelles et modernes.

## Quand utiliser cette compétence
- Pour concevoir un nouveau système de design (couleurs, typographie, espacements).
- Pour créer des maquettes ou implémenter des composants web (React, Vue, Tailwind).
- Pour auditer l'accessibilité ou la cohérence visuelle d'une interface.
- Pour obtenir des recommandations de structure de pages de destination (Landing Pages).

## Comment l'utiliser

### 1. Analyse des Besoins
Identifiez le type de produit (SaaS, e-commerce, portfolio), l'industrie (fintech, santé, luxe) et le style souhaité (minimaliste, dynamique, sombre).

### 2. Génération du Système de Design (RECOMMANDÉ)
Lancez la commande suivante pour obtenir un guide complet basé sur vos mots-clés :

```bash
python3 ~/.gemini/antigravity/skills/ui-ux-pro-max/scripts/core.py "votre requête ici (ex: fintech luxueuse)" --design-system -p "Nom du Projet"
```

### 3. Recherche par Domaines
Si vous avez besoin de détails spécifiques, utilisez les domaines de recherche :

```bash
python3 ~/.gemini/antigravity/skills/ui-ux-pro-max/scripts/core.py "mot-clé" --domain <domaine>
```

**Domaines disponibles :**
- `product`: Recommandations par type de produit.
- `style`: Styles visuels, effets de verre (glassmorphism), etc.
- `typography`: Fontes Google Fonts, appariements typographiques.
- `color`: Palettes de couleurs par industrie.
- `landing`: Structure des rubriques d'une page de destination.
- `ux`: Meilleures pratiques et anti-patterns UX.

### 4. Directives par Stack Technologique
Obtenez des conseils d'implémentation spécifiques à votre framework :

```bash
python3 ~/.gemini/antigravity/skills/ui-ux-pro-max/scripts/core.py "layout" --stack <votre-stack>
```
*Stacks supportés : `html-tailwind`, `react`, `nextjs`, `vue`, `svelte`, `shadcn`, `swiftui`, `flutter`.*

## Structure des dossiers
- `data/`: Fichiers CSV contenant les règles de design et les recommandations.
- `scripts/`: Scripts Python (`core.py`, `search.py`) pour interroger les données.
- `templates/`: Modèles de référence pour différentes plateformes.

## Liste de contrôle UI/UX (Best Practices)
- **Icônes**: Utilisez des fichiers SVG (Lucide, Heroicons) au lieu des emojis.
- **Accessibilité**: Vérifiez le contraste (4.5:1 minimum) et les balises sémantiques.
- **Feedback**: Ajoutez des états `hover` fluides et des transitions (150-300ms).
- **Responsive**: Testez toujours sur mobile (375px) et bureau (1440px).
