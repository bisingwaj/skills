---
name: brainstorming-multi-agent
description: "Simule un processus de revue structuré avec plusieurs agents spécialisés pour valider les designs, révéler les hypothèses cachées et identifier les modes de défaillance avant l'implémentation."
---

# Brainstorming Multi-Agent (Revue de Design Structurée)

## Aperçu
Transformer un design mono-agent en un **design robuste et validé** en simulant un processus de revue formelle avec plusieurs agents contraints. Ce n'est **pas** du brainstorming parallèle — c'est une **revue de design séquentielle avec des rôles appliqués**.

## Quand utiliser cette compétence
- Valider une architecture ou un design complexe avant implémentation.
- Identifier les hypothèses cachées et les modes de défaillance.
- S'assurer que les contraintes non-fonctionnelles sont respectées.
- Améliorer la confiance dans une décision technique majeure.

## Les 5 Agents (Rôles Non Négociables)

### 1️⃣ Concepteur Principal (Agent Principal)
- **Rôle** : Possède le design, anime le processus de brainstorming standard.
- **Peut** : Proposer des designs, poser des questions, réviser selon les retours.
- **Ne peut pas** : Auto-approuver le design final, ignorer les objections.

### 2️⃣ Agent Sceptique / Challenger
- **Rôle** : Assume que le design va échouer.
- **Peut** : Questionner les hypothèses, identifier les angles morts, signaler les violations YAGNI.
- **Ne peut pas** : Proposer de nouvelles fonctionnalités ni redesigner le système.

### 3️⃣ Agent Gardien des Contraintes
- **Rôle** : Appliquer les contraintes non-fonctionnelles (performance, sécurité, scalabilité, coût opérationnel).
- **Peut** : Rejeter les designs qui violent une contrainte.
- **Ne peut pas** : Modifier les objectifs produit.

### 4️⃣ Agent Avocat de l'Utilisateur
- **Rôle** : Représenter l'utilisateur final (charge cognitive, utilisabilité, flux, gestion d'erreur).
- **Peut** : Signaler les aspects confus ou trompeurs, les mauvais comportements par défaut.
- **Ne peut pas** : Redesigner l'architecture.

### 5️⃣ Agent Intégrateur / Arbitre
- **Rôle** : Résoudre les conflits, finaliser les décisions, appliquer les critères de sortie.
- **Peut** : Accepter/rejeter des objections, demander des révisions, déclarer le design terminé.
- **Ne peut pas** : Inventer de nouvelles idées.

## Le Processus en 3 Phases

### Phase 1 — Design Mono-agent
Le Concepteur Principal crée un design initial et commence un **Journal de Décisions**.

### Phase 2 — Boucle de Revue Structurée
Les agents sont invoqués **un par un** dans l'ordre : Sceptique → Gardien → Avocat.
Chaque retour doit être explicite et scopé. Le Concepteur révise et met à jour le journal.

### Phase 3 — Intégration & Arbitrage
L'Arbitre examine le design final et le journal, accepte ou rejette chaque objection.

## Journal de Décisions (Artefact Obligatoire)
| Décision | Alternatives | Objections | Résolution |
|---|---|---|---|
| ... | ... | ... | ... |

## Critères de Sortie (Stop Strict)
Ne quitter cette compétence que si **TOUT** est vrai :
- [ ] Tous les agents ont été invoqués.
- [ ] Toutes les objections sont résolues ou explicitement rejetées.
- [ ] Le Journal de Décisions est complet.
- [ ] L'Arbitre a déclaré le design acceptable.

**Résultat à signaler :** `APPROUVÉ`, `À RÉVISER`, ou `REJETÉ` avec justification.
