# Questions d'Entretien - Cognitive Design Systems (CDS)
## Med Fadi Abaidi | Stage Développeur Full-Stack | Toulouse

---

**Poste visé :** Stagiaire Développeur Full-Stack
**Entreprise :** Cognitive Design Systems (CDS) - Solutions CAD automatisées
**Localisation :** Toulouse, France (Centre de l'industrie aérospatiale)
**Stack technique :** React, Node.js, Electron, Three.js, Python, TypeScript

---

## I. Questions Générales

### Parlez-moi de vous.
"Je suis Med Fadi Abaidi, étudiant ingénieur en génie logiciel à la Faculté des Sciences de Tunis, passionné par le développement d'applications web et desktop. J'ai acquis une expérience significative lors de mon stage chez Skillia à Paris, où j'ai développé une plateforme LMS complète avec React.js et TypeScript sur huit modules. Je maîtrise React, Next.js, Node.js et TypeScript, et j'ai une appétence particulière pour la création d'interfaces utilisateur créatives. Ce qui m'attire chez CDS, c'est l'opportunité de contribuer à des solutions innovantes dans l'industrie aérospatiale."

### Pourquoi souhaitez-vous rejoindre Cognitive Design Systems ?
"CDS m'attire pour plusieurs raisons :
- L'industrie aérospatiale de Toulouse représente un environnement d'innovation unique
- Votre mission de développer des solutions CAD automatisées combine créativité et technicité
- J'ai l'habitude de créer des applications from scratch (MTube, Mistral AI)
- Travailler dans une équipe de 10+ développeurs multiculturelle correspond à ma vision du travail collaboratif"

### Qu'est-ce qui vous passionne dans le développement d'applications ?
"Ce qui me passionne le plus :
- L'aspect créatif et la possibilité d'innover dans l'expérience utilisateur
- Créer des systèmes comme les artefacts avec prévisualisation live (projet Mistral AI)
- Développer des animations fluides avec Framer Motion et GSAP (OK Studios)
- Transformer des idées en produits fonctionnels qui améliorent la vie des utilisateurs"

### Comment gérez-vous la pression et les délais serrés ?
"Je gère la pression efficacement :
- Organisation du travail avec des priorités claires
- Communication régulière avec l'équipe pour identifier les blocages
- Utilisation d'outils comme GitHub Projects pour visualiser l'avancement
- Polyvalence pour basculer entre plusieurs projets simultanément"

### Décrivez une situation où vous avez géré un projet de bout en bout.
"Pour la plateforme vidéo MTube, j'ai géré le projet complet :
- **Conception** : Architecture microservices sur Google Cloud Platform
- **Frontend** : Next.js avec Firebase Auth
- **Backend** : Firebase Functions + Cloud Run pour le traitement vidéo FFmpeg
- **Infrastructure** : Cloud Storage, Pub/Sub, Firestore
- Cette expérience m'a appris à prendre des décisions architecturales impactantes"

---

## II. Questions Techniques - Stack CDS

### Expliquez votre expérience avec React et TypeScript.
"J'utilise React et TypeScript quotidiennement :

**Chez Skillia (plateforme LMS) :**
- Interface React.js avec TypeScript pour 4 types d'utilisateurs
- Architecture basée sur les hooks personnalisés
- Gestion d'état avec Context API

**Application Mistral AI :**
- Next.js 15 avec App Router
- Custom hooks : `useChatConversation`, `useArtifactOperations`, `useResizable`
- Composants Chakra UI et Tailwind CSS
- Éditeur de code avec CodeMirror"

### Avez-vous de l'expérience avec Node.js et les applications Electron ?
"**Node.js - Expérience solide :**
- Backend NestJS chez Skillia : 20+ endpoints RESTful, TypeORM, PostgreSQL, JWT, RBAC
- Cache Redis, pagination et lazy loading
- Firebase Functions pour MTube

**Electron :**
- Pas d'expérience directe encore
- Bases solides en React + Node.js pour adaptation rapide
- Electron utilise les mêmes technologies web → prolongement naturel de mon expertise"

### Qu'est-ce que Three.js et avez-vous de l'expérience avec la 3D ?
"Three.js est une bibliothèque JavaScript pour créer des graphiques 3D dans le navigateur via WebGL.

**Mes bases pour l'aborder :**
- Compréhension des concepts 3D : matrices de transformation, systèmes de coordonnées
- Maîtrise avancée de JavaScript/TypeScript
- Python pour l'algorithmique (Codeforces Specialist)
- Très motivé pour apprendre et contribuer aux solutions CAD de CDS"

### Parlez-moi de votre expérience avec Python.
"Python est l'un de mes langages principaux :
- **Algorithmique** : Codeforces Specialist, résolution de problèmes complexes
- **Data Science** : NumPy, Pandas pour le traitement de données
- **Certification** : Oracle Certified Foundations Associate
- Prêt à approfondir pour la R&D sur les algorithmes 3D et modification géométrique"

### Comment créez-vous une webapp from scratch ?
"**1. Phase de conception :**
- Analyse des besoins utilisateur
- Wireframes et maquettes avec Figma

**2. Setup du projet :**
- Create Next App avec TypeScript ou Vite

**3. Structure :**
```
/src
  /components    - Composants réutilisables
  /hooks         - Custom hooks
  /pages         - Routes
  /services      - Appels API
  /types         - Interfaces TypeScript
```

**4. Développement itératif :**
- Composants UI avec Tailwind/Chakra
- Tests avec Jest/Playwright
- CI/CD avec GitHub Actions
- Déploiement Docker"

### Comment gérez-vous les connexions avec des solutions tierces ?
"**Intégrations réalisées :**
- Mistral AI API : chat streaming, function calling, embeddings
- Stripe : checkout, webhooks, abonnements
- Firebase : Auth, Firestore, Cloud Storage
- GitHub API : collaboration étudiant-mentor (Skillia)
- Google Cloud : Pub/Sub, Cloud Run, GCS

**Approche :**
1. Étude approfondie de la documentation API
2. Création d'un service wrapper TypeScript
3. Gestion des erreurs centralisée
4. Tests d'intégration
5. Monitoring et logging"

### Comment concevez-vous et développez-vous des bases de données ?
"**SQL (PostgreSQL, MySQL) :**
- Modélisation relationnelle avec Spring Data JPA
- Migrations via TypeORM (NestJS)
- Optimisation des requêtes, indexation

**NoSQL (MongoDB, Firestore) :**
- Schémas flexibles avec Prisma ORM
- Documents adaptés aux applications temps réel

**Exemple (Système de Surveillance) :**
- Entités : Enseignant, Surveillance, Disponibilité, Session, Matière, Salle
- Relations complexes avec contraintes d'intégrité
- Validation des conflits de planning au niveau base de données"

---

## III. Questions sur l'Expérience Utilisateur (UX)

### Comment accordez-vous une attention particulière à l'expérience utilisateur ?
"**Chez OK Studios :**
- Design mobile-first responsive
- Lazy loading des images avec Next.js Image
- Animations Framer Motion pour les transitions
- Micro-interactions GSAP ScrollTrigger
- Layouts bento grid et effets personnalisés

**Application Mistral AI :**
- Interface split-pane redimensionnable (hook `useResizable`)
- Streaming temps réel avec feedback visuel
- Error boundaries pour gestion gracieuse des erreurs
- Prévisualisation live du code généré"

### Comment gérez-vous le design et le prototypage ?
"- **Figma** : Maquettes, wireframes, design systems
- **Adobe Photoshop** : Retouche et création graphique
- Double casquette développeur/designer (Media Manager au GDG on Campus FST)
- Création d'interfaces cohérentes et esthétiques"

---

## IV. Méthodologie de Travail

### Comment travaillez-vous en équipe ?
"- Daily stand-ups et communication Slack
- Code reviews via pull requests avec feedback constructif
- Pair programming pour les features complexes
- Documentation technique pour le partage de connaissances
- Expérience chez Skillia avec équipe internationale"

---

## V. Questions Techniques Approfondies

### Expliquez l'architecture d'une application React moderne.
"```
/src
  /components
    /ui           - Composants de base (Button, Input, Modal)
    /features     - Composants métier
    /layouts      - Layouts de page
  /hooks          - Custom hooks réutilisables
  /context        - Providers React Context
  /services       - API calls
  /types          - Interfaces TypeScript
  /utils          - Fonctions utilitaires
```

**Patterns utilisés :**
- Composition : composants petits et composables
- Custom hooks : encapsulation de la logique
- Error boundaries : gestion gracieuse des erreurs"

### Comment gérez-vous l'état dans une application React ?
"**État local (useState)** : Composants isolés, formulaires simples

**Context API** : État partagé (thème, authentification, préférences)

**Exemple Mistral AI :**
```typescript
const ChatStateContext = createContext<ChatState>(null);

const useChatConversation = () => {
  const [messages, setMessages] = useState<Message[]>([]);
  const addMessage = useCallback((msg) => {
    setMessages(prev => [...prev, msg]);
  }, []);
  return { messages, addMessage };
};
```

**Zustand/Redux Toolkit** : Applications complexes avec beaucoup d'état global"

### Comment travaillez-vous avec Git et GitHub ?
"**Workflow :**
1. Branche feature pour chaque fonctionnalité
2. Commits atomiques avec messages descriptifs
3. Pull Request pour code review
4. Merge après validation

**CI/CD avec GitHub Actions :**
- Tests automatiques sur chaque PR
- Linting et formatage (ESLint, Prettier)
- Build et déploiement automatisés
- **Certification** : GitHub Actions (GH-200)"

### Comment utilisez-vous Docker dans vos projets ?
"**Exemple (Service traitement vidéo MTube) :**
```dockerfile
FROM node:18
WORKDIR /app
RUN apt-get update && apt-get install -y ffmpeg
COPY package*.json ./
RUN npm install
COPY . .
CMD ["npm", "start"]
```

**Utilisations :**
- Environnements de développement reproductibles
- Déploiement sur Cloud Run (GCP)
- Orchestration avec Kubernetes
- Intégration dans pipelines CI/CD"

---

## VI. Questions Comportementales

### Comment proposez-vous de nouvelles idées ?
"**Exemple chez Skillia :**
J'ai proposé d'intégrer GitHub directement dans la plateforme LMS pour la collaboration étudiant-mentor. Idée retenue et implémentée.

**Mon approche :**
1. Identifier un problème ou opportunité d'amélioration
2. Rechercher des solutions existantes
3. Proposer un POC rapide
4. Présenter avec arguments concrets (UX, performance, maintenabilité)"

### Comment vous adaptez-vous à de nouvelles technologies ?
"**Exemples récents :**
- SCORM 1.2/2004 : Appris et implémenté en quelques semaines
- Mistral AI API : Intégration complète avec streaming et function calling
- Firebase/GCP : Architecture cloud-native pour MTube

**Ma méthode :**
1. Lire la documentation officielle
2. Suivre des tutoriels pratiques
3. Créer un projet minimal pour expérimenter
4. Itérer et approfondir selon les besoins"

---

## VII. Questions Spécifiques à CDS

### Pourquoi l'industrie aérospatiale vous intéresse-t-elle ?
"- L'aérospatiale représente le summum de l'innovation technologique
- Toulouse est le cœur de cette industrie en Europe
- Le challenge de développer des solutions CAD automatisées combine visualisation 3D, algorithmes géométriques et interfaces intuitives
- Créer des outils pour les ingénieurs qui conçoivent les aéronefs de demain"

### Comment aborderiez-vous le développement d'une application Electron chez CDS ?
"**Architecture :**
- **Main process (Node.js)** : Communication inter-process, accès fichiers
- **Renderer process (React/TypeScript)** : Composants UI, hooks
- **Shared** : Types et utilitaires communs

**Considérations techniques :**
- Sécurité : context isolation, preload scripts
- Performance : lazy loading, workers pour calculs lourds
- UX : menus et notifications système natifs
- Updates : auto-updater pour mises à jour"

### Comment contribueriez-vous à la R&D sur les algorithmes 3D en Python ?
"**Compétences applicables :**
- Algorithmique avancée (Codeforces Specialist)
- Python pour le calcul numérique
- Mathématiques 3D : matrices, vecteurs, transformations

**Approche :**
1. Étudier NumPy, SciPy, PyMesh
2. Apprendre les algorithmes CAD fondamentaux
3. Prototyper en Python
4. Intégrer avec Three.js pour la visualisation"

---

## VIII. Défis Techniques et Solutions par Projet

### Plateforme LMS Skillia (Knodo) - Implémentation du standard SCORM

**Défi :** Implémenter un lecteur conforme aux standards SCORM 1.2 et 2004, avec des centaines de spécifications techniques pour le tracking e-learning.

**Solution :**
- Étude approfondie de la documentation officielle ADL
- Analyse de lecteurs SCORM open-source existants
- Implémentation progressive de l'API (LMSInitialize, LMSGetValue, etc.)
- Suite de tests avec packages SCORM de référence
- **Résultat** : Lecteur compatible SCORM 1.2/2004 intégré au système de tracking

---

### Site vitrine OK Studios - Performance des animations complexes

**Défi :** Maintenir 60 FPS avec animations Framer Motion et GSAP ScrollTrigger sur appareils mobiles.

**Solution :**
- Profiling avec Chrome DevTools
- Utilisation exclusive des propriétés GPU (transform, opacity)
- Lazy loading des images avec Next.js Image
- Intersection Observer API pour déclencher animations au viewport
- Media queries pour simplifier animations sur appareils faibles
- **Résultat** : 60 FPS sur smartphones, score Lighthouse > 90

---

### Système de Surveillance d'Examens - Gestion des conflits en temps réel

**Défi :** Éviter les conflits d'assignation simultanée des enseignants avec notifications temps réel.

**Solution :**
- **Backend** : Validation @Transactional pour atomicité des opérations
- **WebSocket** : STOMP pour alertes instantanées sur conflits
- **Frontend** : Service de notifications avec reconnexion automatique et queues user-specific
- **Résultat** : Zéro conflit en production, changements visibles instantanément

---

### Application Chat Mistral AI - Streaming temps réel avec système d'artefacts

**Défi :** Générer du code en temps réel avec prévisualisation live pendant le streaming API.

**Solution :**
- Parser de streaming pour détecter début/fin des artefacts token par token
- Hook `useArtifactOperations` pour création, mise à jour, versioning
- Iframe sandboxée pour prévisualisation sécurisée
- Hook `useStreamingPerformance` pour métriques (time-to-first-token, tokens/sec)
- **Résultat** : Interface fluide avec code généré et prévisualisation live progressive

---

### Plateforme Vidéo MTube - Architecture event-driven sur GCP

**Défi :** Traitement vidéo asynchrone et scalable avec fiabilité en cas d'échec.

**Solution :**
- Upload direct vers Cloud Storage via URL signée
- Message Pub/Sub déclenche Cloud Run pour transcodage FFmpeg
- Vérification d'idempotence contre traitement en double
- Retry automatique en cas d'échec
- Scale-to-zero pour coûts optimisés
- **Résultat** : Traitement de centaines de vidéos simultanément sans intervention

---

### Pipeline CI/CD DevOps - Intégration de multiples outils

**Défi :** Intégrer Jenkins, Docker, SonarQube, Nexus, Kubernetes, Prometheus/Grafana de manière fiable.

**Solution :**
- Configuration as code (Jenkinsfile versionné)
- Quality gates stricts (couverture tests, vulnérabilités)
- Retry avec backoff exponentiel pour opérations réseau
- Health checks post-déploiement
- Rollback automatique si health checks échouent
- **Résultat** : Pipeline automatisé garantissant code de qualité en production

---

### Architecture AWS 3-Tier - Haute disponibilité multi-AZ

**Défi :** Architecture fonctionnelle même en cas de panne d'une zone de disponibilité AWS.

**Solution :**
- **Présentation** : CloudFront CDN + Route 53 avec health checks
- **Application** : ECS multi-AZ + ALB avec Auto Scaling
- **Données** : RDS Multi-AZ avec réplication synchrone + S3
- CloudWatch pour métriques et alarmes
- **Résultat** : SLA haute disponibilité, failover < 1 minute

---

## IX. Questions à Poser à CDS

- "Quelles sont les technologies principales utilisées dans vos solutions CAD actuelles ?"
- "Comment l'équipe est-elle organisée ? Spécialisations frontend/backend ou polyvalence ?"
- "Quels sont les principaux défis techniques actuels ?"
- "Comment se déroule l'onboarding pour un stagiaire ?"
- "Quel type de projets serait confié à un stagiaire ?"
- "Utilisez-vous Three.js ou une autre bibliothèque pour le rendu 3D ?"
- "Y a-t-il des opportunités après le stage ?"

---

## X. Récapitulatif - Adéquation avec le Poste CDS

| Exigence CDS | Mon Expérience |
|--------------|----------------|
| React, TypeScript | Skillia (LMS), Mistral AI, OK Studios |
| Node.js | NestJS (Skillia), Firebase Functions (MTube) |
| Electron | Prêt à apprendre (bases React + Node.js) |
| Three.js / 3D | Motivé, compétences algorithmiques solides |
| Python | Codeforces Specialist, Oracle Certified |
| Webapp from scratch | MTube, Mistral AI, OK Studios |
| Git, GitHub, Docker | GitHub Actions certifié, Docker sur tous projets |
| Figma | Media Manager GDG, design d'interfaces |
| Équipe 10+ devs | Expérience Skillia, GDG on Campus |
| Créativité / UX | Animations, micro-interactions, design systems |

---

## XI. Points Forts à Mettre en Avant

- **Full-Stack polyvalent** : React, Node.js, TypeScript, Python
- **Projets from scratch** : MTube, Mistral AI, Skillia
- **Certifications cloud** : AWS Developer, Solutions Architect, Azure Fundamentals
- **Créativité UX** : Animations, design, micro-interactions
- **Adaptabilité** : Apprentissage rapide de nouvelles technologies
- **Algorithmique** : Codeforces Specialist

---

*Document optimisé pour Cognitive Design Systems (CDS) - Toulouse*
*Med Fadi Abaidi - Janvier 2026*
