---
name: brainstorming
description: "À utiliser impérativement avant tout travail créatif (création de fonctionnalités, composants ou modification de comportement). Explore l'intention de l'utilisateur, les exigences et le design avant l'implémentation."
---

# Brainstorming : Transformer les Idées en Designs

## Aperçu
Cette compétence aide à transformer des idées en designs et spécifications complets via un dialogue collaboratif naturel.

Commencez par comprendre le contexte actuel du projet, puis posez des questions une par une pour affiner l'idée. Une fois que vous avez compris ce que vous construisez, présentez le design et demandez l'approbation de l'utilisateur.

<HARD-GATE>
Ne lancez AUCUNE compétence d'implémentation, n'écrivez aucun code, ne créez aucune structure de projet et ne prenez aucune action d'implémentation tant que vous n'avez pas présenté un design et que l'utilisateur ne l'a pas approuvé. Cela s'applique à TOUS les projets, quelle que soit leur simplicité apparente.
</HARD-GATE>

## Anti-Pattern : "C'est trop simple pour avoir besoin d'un design"
Tout projet doit passer par ce processus. Une liste de tâches, un utilitaire à fonction unique, un changement de configuration — tous. Les projets "simples" sont ceux où les hypothèses non examinées causent le plus de travail inutile. Le design peut être court (quelques phrases pour les projets vraiment simples), mais vous DEVEZ le présenter et obtenir l'approbation.

## Liste de Contrôle (Checklist)
Vous DEVEZ créer une tâche pour chacun de ces éléments et les compléter dans l'ordre :

1.  **Explorer le contexte du projet** — vérifiez les fichiers, la documentation, les commits récents.
2.  **Poser des questions de clarification** — une par une, comprendre le but/les contraintes/les critères de succès.
3.  **Proposer 2-3 approches** — avec les compromis et votre recommandation.
4.  **Présenter le design** — par sections adaptées à leur complexité, demander l'approbation après chaque section.
5.  **Rédiger le document de design** — enregistrer dans `docs/plans/YYYY-MM-DD-<sujet>-design.md` et committer.
6.  **Transition vers l'implémentation** — invoquer la compétence `planification` pour créer le plan d'implémentation.

## Principes Clés
- **Une question à la fois** — Ne pas submerger l'utilisateur.
- **Choix multiples privilégiés** — Plus facile à répondre que des questions ouvertes.
- **YAGNI impitoyable** — Supprimer les fonctionnalités inutiles de tout design.
- **Explorer des alternatives** — Toujours proposer 2-3 approches avant de décider.
- **Validation incrémentale** — Présenter le design, obtenir l'approbation avant de continuer.
- **Flexibilité** — Revenir en arrière et clarifier quand quelque chose n'est pas clair.
