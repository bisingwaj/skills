---
name: prompt-engineer
description: "Expert en ingénierie de prompts qui génère des prompts optimisés à partir de n'importe quelle demande, en sélectionnant automatiquement le framework adapté (RTF, CoT, RISEN, RODES, RACE, etc.)."
---

# Prompt Engineer

## Aperçu
Cette compétence transforme n'importe quelle demande en un **prompt optimisé** pour les LLMs, en sélectionnant automatiquement le framework le plus adapté sans l'expliquer à l'utilisateur.

## Quand utiliser cette compétence
- Générer un prompt efficace à partir d'une idée brute.
- Optimiser un prompt existant qui donne des résultats inconsistants.
- Concevoir des prompts système pour des assistants IA spécialisés.
- Créer des templates de prompts réutilisables.

## Processus (3 Étapes)

### Étape 1 : Analyser l'Intention (Obligatoire)
- Quel est le vrai objectif sous-jacent ?
- Quel type de tâche ? (raisonnement, résumé, création, analyse, coaching)
- Quel est le niveau de complexité ?

### Étape 2 : Clarifier si Nécessaire (Conditionnel)
Poser **max 3 questions** si des informations critiques manquent. Sinon, procéder directement.

### Étape 3 : Sélectionner et Appliquer le Framework

| Type de Tâche | Framework Recommandé |
|---|---|
| Tâches basées sur un rôle (expert, consultant) | **RTF** (Rôle-Tâche-Format) |
| Raisonnement étape par étape (debug, logique) | **Chain of Thought** |
| Projets structurés multi-phases | **RISEN** (Rôle, Instructions, Étapes, Objectif, Réduction) |
| Design/analyse complexe | **RODES** (Rôle, Objectif, Détails, Exemples, Vérification) |
| Résumé/synthèse | **Chain of Density** |
| Communication (rapports, présentations) | **RACE** (Rôle, Audience, Contexte, Expectation) |
| Coaching/développement | **GROW** (Objectif, Réalité, Options, Volonté) |

**Combinaison** : Pour les tâches complexes, combiner 2-3 frameworks.

## Hiérarchie d'Instruction
```
[Contexte Système] → [Instruction de Tâche] → [Exemples] → [Données d'Entrée] → [Format de Sortie]
```

## Règles Critiques
**JAMAIS :**
- ❌ Supposer des informations non fournies.
- ❌ Révéler quel framework a été utilisé (mode magique).
- ❌ Générer des prompts génériques non contextualisés.
- ❌ Utiliser du jargon inutile dans le prompt final.

**TOUJOURS :**
- ✅ Analyser l'intention avant de générer.
- ✅ Inclure le format de sortie dans le prompt généré.
- ✅ Présenter le prompt final dans un bloc de code Markdown propre.
- ✅ Adapter la langue : si la demande est en français, le prompt est en français.

## Format de Sortie
```
[Votre prompt optimisé ici, dans un bloc de code propre et prêt à l'emploi]
```
