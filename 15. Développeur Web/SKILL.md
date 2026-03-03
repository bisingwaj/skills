---
name: developpeur-web
description: "Développeur web fullstack senior : React, Next.js, Node.js, GraphQL, PostgreSQL. Maîtrise la mise en place de projets, l'analyse de qualité de code, les architectures robustes et les workflows modernes."
---

# Développeur Web Fullstack

## Aperçu
Boîte à outils complète pour le développement fullstack moderne, avec les meilleures pratiques et des workflows automatisés pour construire des applications web complètes et maintenables.

## Quand utiliser cette compétence
- Scaffolding d'un nouveau projet web fullstack.
- Analyse et amélioration de la qualité du code.
- Modélisation de l'architecture d'une application web.
- Implémentation de patterns avancés (GraphQL, SSR, microservices).
- Mise en place d'un pipeline CI/CD et déploiement cloud.

## Stack Technologique
| Catégorie | Technologies |
|---|---|
| **Langages** | TypeScript, JavaScript, Python, Go |
| **Frontend** | React, Next.js, React Native, Flutter |
| **Backend** | Node.js, Express, GraphQL, REST |
| **Base de données** | PostgreSQL, Prisma, NeonDB, Supabase |
| **DevOps** | Docker, Kubernetes, Terraform, GitHub Actions |
| **Cloud** | AWS, GCP, Azure |

## Bonnes Pratiques

### Qualité de Code
- Suivre les patterns établis (DRY, SOLID, Clean Architecture).
- Écrire des tests complets (unitaires, intégration, E2E).
- Documenter les décisions architecturales.
- Revues de code régulières.

### Performance
- Mesurer avant d'optimiser.
- Utiliser le cache de manière appropriée (Redis, CDN, mémoire).
- Optimiser les chemins critiques (Server Components, streaming).
- Surveiller en production (Sentry, Datadog).

### Sécurité
- Valider toutes les entrées utilisateur.
- Utiliser des requêtes paramétrées (jamais de SQL brut).
- Implémenter une authentification robuste (JWT, OAuth2).
- Maintenir les dépendances à jour.

## Commandes de Base
```bash
# Développement
npm run dev && npm run test && npm run lint

# Analyse de qualité
python scripts/project_scaffolder.py .
python scripts/code_quality_analyzer.py --analyze

# Déploiement
docker build -t app:latest .
docker-compose up -d
kubectl apply -f k8s/
```

## Workflow de Développement
1. **Setup** : Config environnement, variables `.env`, dépendances.
2. **Qualité** : Linter (ESLint/Prettier), tests automatisés, revue de code.
3. **Architecture** : Patterns documentés dans `docs/architecture/`.
4. **Déploiement** : CI/CD automatisé, monitoring post-déploiement.
