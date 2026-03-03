---
name: planification
description: "À utiliser lorsque vous avez des spécifications ou des exigences pour une tâche complexe en plusieurs étapes, avant de toucher au code."
---

# Planification d'Implémentation

## Aperçu
Rédigez des plans d'implémentation complets en supposant que le développeur n'a aucun contexte sur la base de code. Documentez tout ce qu'il doit savoir : fichiers à modifier, code, tests, documentation à consulter, et comment tester les changements. Présentez le plan sous forme de tâches simples et digestes.
Principes : DRY (Don't Repeat Yourself), YAGNI (You Ain't Gonna Need It), TDD (Test Driven Development), Commits fréquents.

**Annonce au début :** "J'utilise la compétence de planification pour créer le plan d'implémentation."

**Emplacement des plans :** `docs/plans/YYYY-MM-DD-<nom-fonctionnalite>.md`

## Granularité des Tâches
Chaque étape est une action unique (2 à 5 minutes) :
1.  **Écrire le test qui échoue**
2.  **Lancer le test pour vérifier l'échec**
3.  **Implémenter le code minimal pour faire passer le test**
4.  **Lancer les tests et vérifier qu'ils passent**
5.  **Committer**

## En-tête Obligatoire du Document de Plan
Chaque plan DOIT commencer par cet en-tête :

```markdown
# Plan d'Implémentation : [Nom de la Fonctionnalité]

**Objectif :** [Une phrase décrivant ce qui est construit]
**Architecture :** [2-3 phrases sur l'approche]
**Tech Stack :** [Technologies et bibliothèques clés]

---
```

## Structure d'une Tâche
```markdown
### Tâche N : [Nom du Composant]
**Fichiers :**
- Créer : `chemin/exact/du/fichier.py`
- Modifier : `chemin/exact/du/fichier_existant.py:123-145`
- Tester : `tests/chemin/du/test.py`

**Étape 1 : Écrire le test qui échoue**
(Code du test ici)

**Étape 2 : Vérifier l'échec**
Commande : `pytest tests/path/test.py::test_name -v`

**Étape 3 : Implémentation minimale**
(Code minimal ici)

**Étape 4 : Vérifier le succès**
Commande : `pytest tests/path/test.py`

**Étape 5 : Committer**
```

## Rappels Importants
- Chemins de fichiers exacts.
- Code complet dans le plan (pas de "ajouter la validation").
- Commandes exactes avec résultats attendus.
- Commits fréquents.
