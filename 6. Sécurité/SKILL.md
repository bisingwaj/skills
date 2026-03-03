---
name: securite
description: "Audit de sécurité complet : scan de vulnérabilités, tests de pénétration, durcissement d'applications web et d'APIs. À utiliser pour détecter et corriger des failles de sécurité."
---

# Sécurité — Scan & Résolution des Failles

## Aperçu
Cette compétence guide un audit de sécurité structuré en plusieurs phases, de la reconnaissance jusqu'au rapport de remédiation, en suivant les standards OWASP.

## Quand utiliser cette compétence
- Effectuer un audit de sécurité sur une application web ou une API.
- Scanner des dépendances à la recherche de vulnérabilités connues.
- Tester la résistance d'un système aux attaques les plus courantes.
- Durcir une application avant sa mise en production.

## Processus en Phases

### Phase 1 : Reconnaissance
- Identifier le périmètre cible.
- Cartographier la surface d'attaque (endpoints, technologies).
- Documenter les technologies utilisées.

### Phase 2 : Scan de Vulnérabilités
- Analyse statique du code (SAST).
- Scan des dépendances (`npm audit`, `snyk`, `trivy`).
- Identification des mauvaises configurations.

### Phase 3 : Tests d'Application Web (OWASP Top 10)
| Vulnérabilité | Outil de test |
|---|---|
| Injection SQL | `sqlmap`, tests manuels |
| XSS | Tests de payload, analyse du DOM |
| Authentification cassée | Tests de session, JWT |
| Contrôle d'accès | Tests d'IDOR, escalade de privilèges |
| Mauvaise configuration | Headers HTTP, CORS, CSP |

### Phase 4 : Sécurité des APIs
- Tester l'authentification/autorisation (JWT, OAuth).
- Vérifier le rate limiting et la validation des entrées.
- Tester la gestion des erreurs (pas d'info sensible exposée).

### Phase 5 : Durcissement
- Sécuriser les en-têtes HTTP (`Helmet.js`, CSP, HSTS).
- Mettre en place l'authentification forte (MFA, bcrypt).
- Chiffrer les données sensibles au repos et en transit.
- Configurer la journalisation et la surveillance des incidents.

### Phase 6 : Rapport
- Documenter chaque vulnérabilité avec sa sévérité (Critique/Haute/Moyenne/Faible).
- Fournir des étapes de remédiation claires et prioritisées.
- Créer un résumé exécutif et un rapport technique détaillé.

## Liste de Contrôle OWASP Top 10
- [ ] Injection (SQL, NoSQL, commande OS)
- [ ] Authentification et gestion de session
- [ ] Exposition de données sensibles
- [ ] Entités XML externes (XXE)
- [ ] Contrôle d'accès défaillant
- [ ] Mauvaise configuration de sécurité
- [ ] Cross-Site Scripting (XSS)
- [ ] Désérialisation non sécurisée
- [ ] Composants avec vulnérabilités connues
- [ ] Journalisation et surveillance insuffisantes
