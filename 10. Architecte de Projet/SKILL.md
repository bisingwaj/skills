---
name: architecte-projet
description: "Guide pour une architecture logicielle de qualité, basée sur Clean Architecture et Domain-Driven Design. À utiliser pour concevoir, analyser ou refactoriser toute base de code."
---

# Architecte de Projet

## Aperçu
Cette compétence fournit des directives pour un développement logiciel axé sur la qualité, basé sur les principes de **Clean Architecture** et du **Domain-Driven Design (DDD)**.

## Quand utiliser cette compétence
- Concevoir l'architecture d'un nouveau projet ou d'une nouvelle fonctionnalité.
- Refactoriser une base de code existante vers une architecture plus maintenable.
- Analyser et recommander des patterns architecturaux adaptés au contexte.
- Répondre à toute question liée au développement logiciel.

## Règles de Style de Code

### Principes Généraux
- **Pattern de retour anticipé** : Toujours utiliser les retours anticipés pour éviter l'imbrication.
- Éviter la duplication via des fonctions et modules réutilisables.
- Décomposer les fonctions de plus de 80 lignes en fonctions plus petites.
- Limiter les fichiers à 200 lignes maximum.

### Architecture & Design (DDD & Clean Architecture)
- **Langage Ubiquitaire** : Les noms de classes et fonctions reflètent le domaine métier.
- **Séparation des couches** : UI → Application → Domaine → Infrastructure.
- **Isolation de la logique métier** : Indépendante des frameworks et bases de données.
- **Cas d'usage clairs** : Chaque use case est isolé et a une responsabilité unique.

### Nommage
| ❌ À éviter | ✅ À utiliser |
|---|---|
| `utils`, `helpers`, `common` | `OrderCalculator`, `UserAuthenticator` |
| `misc.js` | Nom spécifique au contexte borné |

### Anti-Patterns à Éviter
- **Syndrome NIH** : Ne pas réécrire ce qui existe déjà (Auth0, Zustand, etc.).
- **Logique métier dans l'UI** : Séparer clairement les couches.
- **Requêtes DB dans les contrôleurs** : Passer par les repositories.
- Imbrication profonde (max 3 niveaux).

## Checklist Architecturale
- [ ] Les use cases sont clairs et isolés.
- [ ] La logique métier est indépendante du framework.
- [ ] Les noms reflètent le domaine et sont explicites.
- [ ] Les composants sont testables unitairement.
- [ ] Les dépendances vont de l'externe vers l'interne (règle de dépendance).

## Approche Bibliothèque-First
Avant d'écrire du code custom :
1. Chercher une solution existante (npm, PyPI, etc.).
2. Évaluer des services SaaS ou APIs tierces.
3. N'écrire du code custom que pour la logique métier unique.
