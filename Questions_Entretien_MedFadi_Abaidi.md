# Questions d'Entretien - Med Fadi Abaidi
## Ingénieur Full-Stack | React.js, Next.js, Angular, Spring Boot, NestJS

---

## I. Questions Générales

### 1. Parlez-moi de vous.
**Réponse personnalisée :**
> "Je suis Med Fadi Abaidi, étudiant ingénieur en génie logiciel à la Faculté des Sciences de Tunis, passionné par le développement full-stack. J'ai acquis une expérience significative lors de mon stage chez Skillia à Paris où j'ai développé une plateforme LMS complète avec React.js, TypeScript, NestJS et PostgreSQL. Je maîtrise à la fois le frontend (React, Next.js, Angular) et le backend (Spring Boot, NestJS), et j'ai une forte appétence pour les architectures cloud, ayant obtenu les certifications AWS Developer Associate et Solutions Architect Associate. Ce qui me motive, c'est de créer des applications robustes qui résolvent des problèmes concrets."

### 2. Pourquoi avez-vous choisi de devenir ingénieur en développement Full Stack ?
**Réponse personnalisée :**
> "J'ai toujours été fasciné par l'ensemble du cycle de développement d'une application. Lors de mon projet de plateforme vidéo MTube sur Google Cloud Platform, j'ai dû gérer le frontend Next.js, le backend avec Firebase Functions, et le service de transcodage vidéo avec FFmpeg sur Cloud Run. Cette vision d'ensemble me permet de comprendre les contraintes de chaque couche et de prendre de meilleures décisions architecturales. Le full-stack m'offre aussi la flexibilité de contribuer là où l'équipe en a le plus besoin."

### 3. Qu'est-ce qui vous passionne dans le développement d'applications ?
**Réponse personnalisée :**
> "Ce qui me passionne, c'est de transformer des idées complexes en solutions fonctionnelles. Par exemple, dans mon projet d'intégration Mistral AI, j'ai créé un système d'artefacts qui permet de générer du code en temps réel avec prévisualisation live. Voir les utilisateurs interagir avec ces fonctionnalités et les améliorer au fil du temps est très gratifiant. J'apprécie également l'aspect technique : l'optimisation des performances, l'architecture event-driven, et l'intégration d'APIs modernes."

### 4. Comment gérez-vous la pression et les délais serrés ?
**Réponse personnalisée :**
> "Lors de mon stage chez Skillia, nous avions des deadlines serrées pour livrer 30+ fonctionnalités sur 8 modules. J'ai organisé mon travail en utilisant la méthodologie Agile avec des sprints courts, et j'ai priorisé les fonctionnalités critiques comme l'authentification et le moteur de cours SCORM. La communication régulière avec l'équipe via les daily stand-ups m'a permis d'identifier rapidement les blocages. Je maintiens également une couverture de tests (45,5% avec Jest et Playwright) pour éviter les régressions et gagner en confiance lors des déploiements."

### 5. Décrivez une situation où vous avez dû résoudre un problème complexe.
**Réponse personnalisée :**
> "Dans le projet de Système de Surveillance d'Examens, nous avons rencontré un problème de conflits lors de l'assignation des enseignants aux surveillances. Deux enseignants pouvaient être assignés au même créneau s'ils soumettaient simultanément. J'ai résolu ce problème en implémentant une validation côté backend avec Spring Boot qui vérifie les disponibilités en temps réel, utilise des transactions @Transactional pour garantir l'atomicité, et envoie des notifications WebSocket instantanées en cas de conflit. Cette approche a éliminé les conflits tout en maintenant une expérience utilisateur réactive."

---

## II. Questions Techniques

### 1. Expliquez l'architecture d'une application Spring Boot.
**Réponse personnalisée :**
> "Dans le backend du Système de Surveillance d'Examens que j'ai développé, j'ai structuré l'application en plusieurs couches :
> - **Controllers** : Gèrent les requêtes REST (ex: `SurveillanceController`)
> - **Services** : Contiennent la logique métier (ex: `SurveillanceService` avec validation des conflits)
> - **Repositories** : Accès aux données via Spring Data JPA
> - **DTOs** : Objets de transfert pour découpler l'API des entités
> - **Config** : Configuration de sécurité JWT, WebSocket STOMP, et CORS
>
> J'ai également utilisé des event publishers pour les notifications en temps réel et des services d'export (Excel avec Apache POI, PDF avec iText)."

### 2. Comment fonctionne Spring Security ?
**Réponse personnalisée :**
> "Dans mon projet de surveillance d'examens, j'ai configuré Spring Security avec une authentification JWT stateless. Le flow est le suivant :
> 1. L'utilisateur s'authentifie et reçoit un token JWT
> 2. Un `JwtAuthenticationFilter` intercepte chaque requête et valide le token
> 3. La configuration de sécurité définit les endpoints protégés et les rôles (Admin, Enseignant)
> 4. Les CORS sont configurés pour permettre l'accès depuis le frontend Angular
>
> J'ai également implémenté RBAC (Role-Based Access Control) dans mon projet NestJS chez Skillia pour protéger 20+ endpoints avec des guards personnalisés."

### 3. Quelles sont les différences entre React et Angular ?
**Réponse personnalisée :**
> "Ayant travaillé avec les deux :
>
> **React/Next.js** (utilisé chez OK Studios et Skillia) :
> - Bibliothèque flexible, liberté de choix des outils (Chakra UI, Tailwind)
> - Architecture basée sur les hooks (j'ai créé `useChatConversation`, `useArtifactOperations`)
> - Rendu côté serveur natif avec Next.js
>
> **Angular 18** (utilisé dans le Système de Surveillance) :
> - Framework complet avec structure opinionated
> - Standalone components pour une architecture modulaire
> - Injection de dépendances native
> - RxJS intégré pour la gestion des flux asynchrones
>
> Je choisis React pour sa flexibilité sur les projets greenfield, et Angular pour les applications enterprise nécessitant une structure rigide."

### 4. Expliquez le workflow Git et CI/CD.
**Réponse personnalisée :**
> "Dans mon projet de pipeline DevOps, j'ai mis en place un workflow complet :
>
> **Git Flow :**
> - Branches feature pour chaque fonctionnalité
> - Pull requests avec code review
> - Merge vers develop puis main
>
> **Pipeline CI/CD avec Jenkins :**
> 1. **Build** : Compilation de l'application Spring Boot
> 2. **Test** : Exécution des tests unitaires (JUnit)
> 3. **Quality** : Analyse SonarQube pour la qualité du code
> 4. **Package** : Construction de l'image Docker
> 5. **Push** : Publication sur Nexus
> 6. **Deploy** : Déploiement sur Kubernetes
> 7. **Monitor** : Surveillance avec Prometheus/Grafana
>
> J'ai également utilisé GitHub Actions pour l'intégration continue dans mes autres projets."

---

## III. Questions Basées sur Vos Expériences

### 1. Parlez-moi de votre expérience chez Skillia sur la plateforme LMS.
**Réponse personnalisée :**
> "Chez Skillia à Paris, j'ai développé une plateforme LMS complète appelée Knodo. Mes contributions principales :
>
> - **Frontend** : Interface React.js avec TypeScript pour 4 types d'utilisateurs (Admin, Mentor, Learner, Enterprise)
> - **Backend** : API NestJS avec TypeORM et PostgreSQL, 20+ endpoints RESTful protégés par ACL
> - **Fonctionnalités clés** : Moteur de cours conforme SCORM 1.2/2004, import/export EdX OLX, intégration GitHub pour collaboration, planification de mentorat
> - **Sécurité** : Helmet CSP, CORS, bcrypt, guards RBAC
> - **Tests** : 94 tests unitaires Jest (45,5% couverture) et tests E2E Playwright
>
> Nous avons atteint 93% des spécifications fonctionnelles (30/32 features) sur 8+ modules."

### 2. Comment avez-vous architecturé la plateforme vidéo MTube ?
**Réponse personnalisée :**
> "MTube est une plateforme vidéo cloud-native sur Google Cloud Platform avec une architecture microservices :
>
> - **Frontend** : Next.js 14 avec Firebase Auth (Google Sign-In)
> - **API** : Firebase Cloud Functions (génération d'URLs signées, listing vidéos)
> - **Storage** : Google Cloud Storage (buckets raw et processed)
> - **Processing** : Service Docker sur Cloud Run avec FFmpeg pour le transcodage 360p
> - **Events** : Pub/Sub pour déclencher le traitement asynchrone
> - **Database** : Firestore pour les métadonnées vidéo
>
> L'architecture event-driven permet de scaler automatiquement le traitement vidéo en fonction de la charge."

### 3. Expliquez le Système de Surveillance d'Examens que vous avez développé.
**Réponse personnalisée :**
> "C'est une application web pour automatiser la gestion des surveillances d'examens :
>
> **Backend Spring Boot :**
> - Authentification JWT avec Spring Security
> - API RESTful documentée avec Swagger
> - WebSocket STOMP pour les notifications en temps réel
> - Export multi-format (Excel, CSV, PDF)
> - Validation des conflits de planning
>
> **Frontend Angular 18 :**
> - Standalone components avec Angular Material
> - Tableaux de bord avec ApexCharts et ECharts
> - Calendrier interactif (angular-calendar)
> - Internationalisation (4 langues)
> - WebSocket avec reconnexion automatique
>
> **Défis résolus :**
> - Gestion des conflits d'assignation avec transactions
> - Notifications temps réel user-specific
> - Export PDF des convocations avec iText"

### 4. Parlez-moi de votre projet d'intégration Mistral AI.
**Réponse personnalisée :**
> "J'ai créé une application chat IA intégrant Mistral AI avec des fonctionnalités avancées :
>
> **Stack technique :**
> - Next.js 15 avec App Router
> - MongoDB avec Prisma ORM
> - NextAuth.js pour l'authentification
> - Stripe pour les abonnements
>
> **Fonctionnalités innovantes :**
> - Support multi-modèles Mistral (incluant le modèle magistral pour le raisonnement)
> - Streaming en temps réel avec comptage de tokens
> - **Système d'artefacts** : Génération de code avec prévisualisation live HTML/CSS/JS
> - **RAG Projects** : Upload de documents, chunking, embeddings pour des conversations contextuelles
> - Éditeur Lexical pour les documents markdown
> - Dashboard admin avec analytics
>
> **Patterns architecturaux :**
> - Custom hooks (`useChatConversation`, `useMessageSubmit`)
> - Context-based state management
> - Error boundaries pour la résilience"

---

## IV. Questions Techniques Approfondies - Angular

### 1. Qu'est-ce qu'un composant dans Angular ? Expliquez son cycle de vie.
**Réponse avec exemple concret :**
> "Dans le Système de Surveillance, j'ai créé le composant `SurveillanceManagementComponent` :
>
> ```typescript
> @Component({
>   selector: 'app-surveillance-management',
>   standalone: true,
>   imports: [MatTableModule, MatDialogModule, ...],
>   templateUrl: './surveillance-management.component.html'
> })
> ```
>
> **Cycle de vie utilisé :**
> - `ngOnInit` : Chargement initial des surveillances et connexion WebSocket
> - `ngOnChanges` : Mise à jour quand les filtres (session, semestre) changent
> - `ngOnDestroy` : Déconnexion WebSocket et unsubscribe des Observables avec `takeUntil`
>
> J'utilise également `OnPush` change detection pour optimiser les performances des tableaux de données."

### 2. Comment gérez-vous la communication en temps réel dans Angular ?
**Réponse avec exemple concret :**
> "Dans le projet de surveillance, j'ai implémenté les WebSocket avec STOMP/SockJS :
>
> ```typescript
> // NotificationService
> connect(username: string) {
>   const socket = new SockJS(this.serverUrl);
>   this.stompClient = Stomp.over(socket);
>
>   this.stompClient.connect({}, () => {
>     this.stompClient.subscribe(
>       `/user/${username}/queue/notifications`,
>       (message) => this.handleNotification(message)
>     );
>   }, (error) => this.handleReconnection());
> }
> ```
>
> **Fonctionnalités implémentées :**
> - Reconnexion automatique avec retry logic (max attempts)
> - Queues user-specific pour les notifications personnalisées
> - Intégration avec le backend Spring Boot via `SimpMessagingTemplate`"

### 3. Comment structurez-vous les services dans Angular ?
**Réponse avec exemple concret :**
> "J'utilise une architecture de services bien définie :
>
> ```typescript
> @Injectable({ providedIn: 'root' })
> export class SurveillanceService {
>   constructor(private http: HttpClient) {}
>
>   getSurveillances(): Observable<Surveillance[]> {
>     return this.http.get<Surveillance[]>(`${API_URL}/surveillances`)
>       .pipe(
>         catchError(this.handleError)
>       );
>   }
>
>   assignTeacher(id: number, teacherId: number): Observable<void> {
>     return this.http.post<void>(
>       `${API_URL}/surveillances/${id}/assign/${teacherId}`, {}
>     );
>   }
> }
> ```
>
> **Patterns utilisés :**
> - Services singleton avec `providedIn: 'root'`
> - Interceptors pour la gestion centralisée des erreurs et tokens JWT
> - Séparation claire entre services API et services de gestion d'état"

### 4. Expliquez la différence entre Template-Driven Forms et Reactive Forms.
**Réponse avec exemple concret :**
> "Dans mes projets, j'utilise principalement les **Reactive Forms** pour leur flexibilité :
>
> ```typescript
> // Formulaire d'ajout de surveillance
> this.surveillanceForm = this.fb.group({
>   date: ['', Validators.required],
>   heureDebut: ['', Validators.required],
>   heureFin: ['', Validators.required],
>   salle: ['', Validators.required],
>   matiere: ['', Validators.required],
>   enseignants: [[], Validators.minLength(1)]
> });
>
> // Validation personnalisée
> this.surveillanceForm.addValidators(
>   this.validateTimeRange('heureDebut', 'heureFin')
> );
> ```
>
> **Avantages des Reactive Forms :**
> - Logique de validation testable dans la classe
> - Manipulation dynamique des contrôles
> - Observables pour réagir aux changements"

---

## V. Questions Techniques Approfondies - React/Next.js

### 1. Comment architecturez-vous une application Next.js ?
**Réponse avec exemple concret :**
> "Dans l'application Mistral AI, j'utilise l'App Router de Next.js 15 :
>
> ```
> /app
>   /chat/[id]/page.tsx     - Pages de conversation
>   /projects/page.tsx      - Liste des projets RAG
>   /admin/page.tsx         - Dashboard admin
> /pages/api
>   /chat.ts                - API streaming Mistral
>   /stripe/checkout.ts     - Intégration paiement
> /src/components
>   /chat/ChatInput.tsx     - Composants réutilisables
> /src/hooks
>   /useChatConversation.ts - Custom hooks
> ```
>
> **Patterns architecturaux :**
> - Server Components pour le SEO et les performances
> - Custom hooks pour la logique réutilisable
> - Context API pour l'état global (ChatStateProvider)"

### 2. Comment gérez-vous le streaming de données en temps réel ?
**Réponse avec exemple concret :**
> "Pour le chat Mistral AI, j'ai implémenté le streaming avec performance monitoring :
>
> ```typescript
> // API Route avec streaming
> const stream = await mistral.chat.stream({
>   model: 'mistral-large-latest',
>   messages: conversationHistory
> });
>
> for await (const chunk of stream) {
>   const content = chunk.data.choices[0].delta.content;
>   res.write(`data: ${JSON.stringify({ content })}\n\n`);
> }
>
> // Client-side hook
> const useStreamingPerformance = () => {
>   const [metrics, setMetrics] = useState({ tokens: 0, latency: 0 });
>   // Track tokens per second, time to first token, etc.
> };
> ```
>
> **Optimisations :**
> - Server-Sent Events pour le streaming
> - Token counting pour les quotas utilisateur
> - Error boundaries pour la résilience"

### 3. Comment gérez-vous l'état dans une application React complexe ?
**Réponse avec exemple concret :**
> "Dans l'application Mistral, j'utilise une combinaison de patterns :
>
> ```typescript
> // Context pour l'état global
> const ChatStateContext = createContext<ChatState>(null);
>
> // Custom hooks pour la logique
> const useChatConversation = () => {
>   const [messages, setMessages] = useState<Message[]>([]);
>   const [artifacts, setArtifacts] = useState<Artifact[]>([]);
>
>   const addMessage = useCallback((msg: Message) => {
>     setMessages(prev => [...prev, msg]);
>   }, []);
>
>   return { messages, artifacts, addMessage };
> };
>
> // Hook composé
> const useArtifactOperations = () => {
>   // Gère création, mise à jour, versioning des artefacts
> };
> ```
>
> Pour des applications plus complexes, j'envisagerais Zustand ou Redux Toolkit."

---

## VI. Questions Cloud & DevOps

### 1. Expliquez votre architecture AWS 3-Tier.
**Réponse personnalisée :**
> "J'ai déployé une architecture hautement disponible sur AWS :
>
> **Tier 1 - Présentation :**
> - CloudFront CDN pour la distribution globale
> - Route 53 pour le DNS
> - Certificats SSL/TLS
>
> **Tier 2 - Application :**
> - ECS/EKS pour l'orchestration de containers
> - Application Load Balancer pour la répartition de charge
> - Auto Scaling pour la haute disponibilité
>
> **Tier 3 - Données :**
> - RDS avec Multi-AZ pour la base de données
> - S3 pour le stockage d'objets
> - CloudWatch pour le monitoring
>
> Cette architecture assure la scalabilité, la résilience et la sécurité."

### 2. Comment avez-vous utilisé GCP pour la plateforme vidéo ?
**Réponse personnalisée :**
> "L'architecture cloud-native sur GCP :
>
> ```
> User Upload → Signed URL → Cloud Storage (raw)
>                                    ↓
>                              Pub/Sub Message
>                                    ↓
>                          Cloud Run (FFmpeg processing)
>                                    ↓
>                          Cloud Storage (processed)
>                                    ↓
>                          Firestore (metadata update)
> ```
>
> **Avantages :**
> - Scale-to-zero avec Cloud Run
> - Traitement asynchrone découplé
> - Coûts optimisés (pay-per-use)"

### 3. Décrivez votre pipeline CI/CD.
**Réponse personnalisée :**
> "Pipeline complet avec Jenkins :
>
> 1. **Source** : Webhook Git sur push
> 2. **Build** : Maven pour Spring Boot
> 3. **Test** : JUnit + Jacoco (couverture)
> 4. **Quality Gate** : SonarQube analysis
> 5. **Package** : Docker build & tag
> 6. **Registry** : Push vers Nexus
> 7. **Deploy** : kubectl apply sur Kubernetes
> 8. **Verify** : Smoke tests
> 9. **Monitor** : Prometheus metrics + Grafana dashboards
>
> **Automatisations :**
> - Rollback automatique si health check échoue
> - Notifications Slack sur succès/échec"

---

## VII. Questions Comportementales

### 1. Comment travaillez-vous en équipe ?
**Réponse personnalisée :**
> "Chez Skillia, je travaillais dans une équipe internationale avec des développeurs frontend et backend. J'utilisais :
> - **Daily stand-ups** pour la synchronisation
> - **Code reviews** via pull requests
> - **Documentation** technique pour le partage de connaissances
> - **Pair programming** pour les features complexes
>
> En tant que Media Manager au Google Developer Group de la FST, j'ai également développé des compétences en communication et coordination d'équipe."

### 2. Comment vous tenez-vous à jour avec les technologies ?
**Réponse personnalisée :**
> "Je maintiens une veille technologique active :
> - **Certifications** : AWS Developer Associate, Solutions Architect, Azure Fundamentals, Oracle Java
> - **Pratique** : Projets personnels explorant de nouvelles technologies (Mistral AI, SCORM)
> - **Compétitions** : Codeforces (rank Specialist) pour l'algorithmique
> - **Communauté** : Participation au GDG on Campus
> - **Documentation** : Lecture des changelogs (Angular, React, Next.js)"

### 3. Quel est votre plus grand défi technique et comment l'avez-vous surmonté ?
**Réponse personnalisée :**
> "L'implémentation du moteur SCORM 1.2/2004 chez Skillia. SCORM est un standard complexe avec de nombreuses spécifications pour le tracking des cours e-learning.
>
> **Approche :**
> 1. Étude approfondie de la documentation SCORM
> 2. Analyse de players existants open-source
> 3. Implémentation progressive avec tests à chaque étape
> 4. Validation avec des packages SCORM de test
>
> Le résultat : un lecteur compatible avec les contenus SCORM 1.2 et 2004, intégré avec notre système de tracking de progression."

---

## VIII. Questions à Poser à l'Intervieweur

1. "Quelle est la stack technique principale de l'équipe ?"
2. "Comment l'équipe gère-t-elle la dette technique ?"
3. "Quels sont les principaux défis techniques actuels du projet ?"
4. "Comment se déroule le processus de code review ?"
5. "Quelle est la méthodologie Agile utilisée ?"
6. "Y a-t-il des opportunités de formation ou de certifications ?"
7. "Comment l'équipe équilibre-t-elle innovation et stabilité ?"

---

## Récapitulatif - Points Forts à Mettre en Avant

| Domaine | Compétences Clés |
|---------|------------------|
| **Frontend** | React.js, Next.js 14/15, Angular 18, TypeScript, Tailwind CSS |
| **Backend** | Spring Boot, NestJS, Node.js, RESTful API, GraphQL |
| **Cloud** | AWS (ECS, EKS, RDS, S3, CloudFront), GCP (Cloud Run, Pub/Sub, Firebase) |
| **DevOps** | Docker, Kubernetes, Jenkins, GitHub Actions, CI/CD |
| **Bases de données** | PostgreSQL, MySQL, MongoDB, Firestore |
| **Temps réel** | WebSocket (STOMP/SockJS), Server-Sent Events |
| **Sécurité** | JWT, OAuth 2.0, RBAC, Spring Security |
| **Tests** | Jest, Playwright, JUnit |
| **Certifications** | AWS Developer, AWS Solutions Architect, Azure Fundamentals, Oracle Java |

---

*Document personnalisé pour Med Fadi Abaidi - Janvier 2026*
