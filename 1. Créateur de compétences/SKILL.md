---
name: createur-de-competences
description: Aide à la conception et à la documentation de nouvelles compétences (skills) Antigravity, en respectant les standards officiels et en utilisant exclusivement le français.
---

# Créateur de compétences

Cette compétence guide l'IA pour générer des fichiers `SKILL.md` clairs, cohérents et directement utilisables. Elle assure que chaque nouvelle compétence suit la structure recommandée par Antigravity.

## Quand utiliser cette compétence
Utilisez cette compétence chaque fois que vous devez :
- Créer une nouvelle compétence de zéro.
- Documenter une compétence existante qui manque de structure.
- Refondre une compétence pour la rendre conforme aux standards Antigravity.

## Comment l'utiliser

### 1. Structure du fichier `SKILL.md`
Chaque compétence doit commencer par un frontmatter YAML, suivi du corps en Markdown.

#### Frontmatter YAML
- `name`: Identifiant unique (kebab-case, max 64 caractères).
- `description`: Phrase courte à la troisième personne décrivant l'usage de la compétence. C'est elle qui déclenche l'activation du skill.

#### Corps Markdown
Utilisez les sections suivantes pour structurer la documentation :
- `# [Nom de la compétence]` (Titre principal)
- `## Quand utiliser cette compétence` (Scénarios d'usage)
- `## Comment l'utiliser` (Instructions étape par étape)
- `## Structure des fichiers` (Description des dossiers `scripts/`, `examples/`, `resources/` si nécessaire)
- `## Bonnes pratiques` (Conseils spécifiques au domaine de la compétence)

### 2. Style et Langue
- **Français intégral**: Toutes les descriptions, instructions et commentaires doivent être en français.
- **Clarté et concision**: Utilisez des listes à puces et des titres descriptifs.
- **Ton professionnel**: Adoptez le ton d'un ingénieur logiciel collaboratif.

### 3. Emplacement des fichiers
Les compétences peuvent être :
- **Locales au workspace**: `<workspace-root>/.agent/skills/<nom-du-skill>/SKILL.md`
- **Globales**: `~/.gemini/antigravity/skills/<nom-du-skill>/SKILL.md`

### 4. Divulgation progressive (Progressive Disclosure)
Optimisez le contexte en ne chargeant que le nécessaire. Le frontmatter est indexé en premier ; le corps n'est lu que si la compétence est jugée pertinente.

## Exemple de format attendu (Template)

```markdown
---
name: nom-de-ma-competence
description: Description concise de ce que fait la compétence pour l'indexation.
---

# Nom de la Compétence

Description détaillée...

## Quand utiliser cette compétence
- Cas 1
- Cas 2

## Comment l'utiliser
1. Étape 1
2. Étape 2
```
