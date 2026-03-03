---
name: creation-video-3d
description: "Expertise avancée pour la création de vidéos programmatiques et de contenu 3D avec Remotion (React). À utiliser pour toute tâche liée à l'animation, la composition, la 3D ou la vidéo générée par code."
---

# Création Vidéo & 3D avec Remotion

## Aperçu
Cette compétence couvre l'utilisation de **Remotion** — le framework React pour créer des vidéos programmatiquement — ainsi que la 3D avec **Three.js** et **React Three Fiber**.

## Quand utiliser cette compétence
- Créer ou modifier des compositions vidéo en React.
- Animer des éléments (texte, images, transitions, séquences).
- Intégrer de la 3D, des GIFs, des sous-titres, des graphiques dans une vidéo.
- Optimiser la performance ou le rendu d'un projet Remotion.

## Comment l'utiliser

### 1. Structure de base d'un projet Remotion
```tsx
import { Composition } from 'remotion';
import { MyVideo } from './MyVideo';

export const RemotionRoot = () => (
  <Composition
    id="MyVideo"
    component={MyVideo}
    durationInFrames={150}
    fps={30}
    width={1920}
    height={1080}
  />
);
```

### 2. Domaines de compétence
| Domaine | Kit d'outils |
|---|---|
| **Animations** | `interpolate`, `spring`, `useCurrentFrame` |
| **Séquençage** | `<Sequence>`, `<Series>`, `<Freeze>` |
| **3D** | `@remotion/three`, React Three Fiber |
| **Audio/Vidéo** | `<Audio>`, `<Video>`, `<OffthreadVideo>` |
| **Texte** | `@remotion/media-utils`, captions |
| **Transitions** | `@remotion/transitions` |
| **Polices** | `@remotion/google-fonts` |
| **Graphiques** | `Victory`, `Recharts` |

### 3. Principes fondamentaux
- Chaque frame est une capture d'un composant React : pensez **état → rendu**.
- Utilisez `useCurrentFrame()` pour accéder au numéro de frame courant.
- Utilisez `interpolate()` pour lier les frames à des valeurs animées.
- Préférez `spring()` pour des animations fluides et naturelles.

### 4. Bonnes pratiques
- **Déterminisme** : le même frame doit toujours produire le même rendu.
- **Performance** : évitez les effets secondaires dans les composants.
- **Préchargement** : utilisez `prefetch()` pour les assets lourds.
- **Tests** : validez visuellement avec le lecteur Remotion avant le rendu.

## Ressources utiles
- Documentation officielle : https://www.remotion.dev/docs
- Templates 3D : `@remotion/three` + React Three Fiber
- Sous-titres : `@remotion/captions` + `@remotion/install-whisper-cpp`
