---
name: design-mobile
description: "Expert en design mobile : UX/UI pour iOS et Android, avec gestion des zones de pouce, performances 60fps, accessibilité et patterns de navigation natifs."
---

# Design Mobile

## Aperçu
Cette compétence guide la conception d'interfaces mobiles performantes, accessibles et respectant les conventions de chaque plateforme (iOS/Android).

## Quand utiliser cette compétence
- Concevoir ou auditer l'UX/UI d'une application mobile.
- Valider des maquettes par rapport aux standards HIG (Apple) et Material Design (Google).
- Optimiser les performances d'animation et de listes.
- Assurer l'accessibilité (WCAG, VoiceOver, TalkBack).

## Questions Obligatoires Avant de Commencer
⛔ Si l'un de ces éléments n'est pas précisé, DEMANDER avant de procéder :
- Plateforme : iOS, Android ou les deux ?
- Framework : React Native, Flutter ou natif ?
- Navigation : Onglets, pile (stack), tiroir (drawer) ?
- Mode hors-ligne requis ?
- Appareils cibles : téléphone uniquement ou tablettes aussi ?

## Score MFRI (Mobile Feature Risk Index)
Avant toute implémentation, calculer :
`MFRI = (Clarté Plateforme + Préparation Accessibilité) − (Complexité Interactions + Risque Performance + Dépendance Réseau)`

| MFRI | Action |
|---|---|
| 6-10 | Procéder normalement |
| 3-5 | Ajouter validation UX et performance |
| < 0 | Repenser avant d'implémenter |

## Anti-Patterns Interdits
| ❌ Jamais | ✅ Toujours |
|---|---|
| ScrollView pour de longues listes | FlatList / FlashList / ListView.builder |
| Cibles tactiles < 44pt (iOS) / 48dp (Android) | Taille minimale respectée |
| Animations sur le thread JS | Pilote natif / GPU |
| Actions uniquement par geste | Bouton de secours disponible |
| Tokens dans AsyncStorage | SecureStore / Keychain |

## Standards Plateforme
| Élément | iOS | Android |
|---|---|---|
| Police | SF Pro | Roboto |
| Taille tactile min | 44pt | 48dp |
| Retour arrière | Glissement depuis le bord | Bouton système |
| Feuilles modales | Bottom Sheet | Dialog / Sheet |
| Icônes | SF Symbols | Material Icons |

## Checklist de Livraison
- [ ] Cibles tactiles ≥ 44-48px partout
- [ ] Mode hors-ligne géré
- [ ] Stockage sécurisé utilisé
- [ ] Listes optimisées (FlatList/FlashList)
- [ ] Testé sur appareils bas de gamme
- [ ] Labels d'accessibilité présents
- [ ] Responsive : téléphone + tablette si applicable
