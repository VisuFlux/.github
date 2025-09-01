# VisuFlux 📊

![VisuFlux Logo](https://img.shields.io/badge/VisuFlux-Analytics-blue?style=for-the-badge)
![Version](https://img.shields.io/badge/version-1.0.0-green?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)

**VisuFlux** est une solution complète d'analyse comportementale des utilisateurs web, permettant de tracker, collecter et visualiser les données de navigation en temps réel à travers des heatmaps et des tableaux de bord analytiques.

## 🎯 Vision du Projet

VisuFlux offre aux propriétaires de sites web une compréhension approfondie du comportement de leurs utilisateurs grâce à :
- **Tracking** des interactions utilisateur
- **Visualisation avancée** avec heatmaps et graphiques
- **Architecture microservices** scalable et performante
- **Intégration simple** via un agent JavaScript léger

## 🛠️ Stack Technique

### Backend
| Technologie | Usage | Version |
|-------------|--------|---------|
| **Java** | Langage principal backend | 17+ |
| **Quarkus** | Framework back-end | 3.x |
| **Apache Kafka** | Message Broker | 3.x |
| **MongoDB** | Base de données NoSQL | 6.x |
| **Netflix Eureka** | Service Discovery | 3.x |

### Frontend
| Technologie | Usage | Version |
|-------------|--------|---------|
| **TypeScript** | Agent de tracking | 5.x |
| **Vue** | Dashboard analytics | 3.x |
| **D3.js** | Visualisation données | Latest |

### DevOps & Infrastructure
| Technologie | Usage |
|-------------|--------|
| **Docker** | Containerisation |
| **Docker Compose** | Orchestration développement |
| **Maven** | Build automation |
| **GitHub Actions** | CI/CD |


### 🎯 Agent VisuFlux (TypeScript)
```typescript
// Exemple d'intégration
<script src="https://cdn.visuflux.com/agent.min.js"></script>
<script>
  const agent = new HeatmapAgent({
    apiURL: 'https://visuflux.com',
    endpoint: 'https://api.visuflux.com',
    trackClicks: true,
    trackScroll: true,
    trackMovements: true,
    debug: true
  });

agent.initialize();
</script>
```

**Fonctionnalités :**
- Tracking des clics, scroll, mouvements
- Capture des métriques de performance
- Envoi asynchrone des données

### 🔄 Quarkus-Collector
Service principal de collecte des événements utilisateur.

**Endpoints principaux :**
- `POST /api/v1/track` - Réception des événements
- `GET /api/v1/health` - Health check

### 🔐 Auth Service
Gestion de l'authentification et autorisation.

**Fonctionnalités :**
- JWT Token management
- API Key validation
- Role-based access control

### 📊 Data Service
Traitement et agrégation des données collectées.

**Responsabilités :**
- Traitement des messages Kafka
- Agrégation des métriques
- Nettoyage et enrichissement des données

### 📈 Visualization Service
Service de génération des visualisations et rapports.

**Capacités :**
- Génération de heatmaps
- Calcul de métriques analytiques
- Export de rapports

## 🚀 Démarrage Rapide

### Prérequis
- Docker & Docker Compose
- Java 17+
- Node.js 18+
- Maven 3.8+

### Installation

1. **Cloner le repository**
```bash
git clone https://github.com/VisuFlux/visuflux.git
cd visuflux
```

2. **Lancer l'environnement de développement**
```bash
docker-compose up -d
```

3. **Vérifier le statut des services**
```bash
docker-compose ps
```

4. **Accéder aux interfaces**
- Dashboard Analytics: http://localhost:3000
- Eureka Server: http://localhost:8761
- Kafka UI: http://localhost:8080

### Configuration

Créer un fichier `.env` :
```env
MONGODB_URI=mongodb://localhost:27017/visuflux
KAFKA_BOOTSTRAP_SERVERS=localhost:9092
EUREKA_SERVER_URL=http://localhost:8761/eureka
JWT_SECRET=your-secret-key
```

## 📋 Feuille de Route

### 🎯 Objectifs Court Terme (3 mois)
- [x] **Agent TypeScript v1.0**
  - [x] Tracking basique (clicks, scroll)
  - [x] Optimisation des performances
  
- [ ] **Core Services**
  - [x] Quarkus-Collector opérationnel
  - [ ] Auth Service avec JWT
  - [x] Data Service avec agrégation temps réel
  
- [ ] **Infrastructure**
  - [x] Setup Docker Compose
  - [ ] Monitoring avec Prometheus/Grafana
  - [ ] Tests d'intégration complets

### 🚀 Objectifs Moyen Terme (6-12 mois)
- [ ] **Analytics Avancées**
  - [ ] Heatmaps en temps réel
  - [ ] Funnel analysis
  - [ ] A/B testing intégré
  - [ ] Alertes personnalisées
  
- [ ] **Scalabilité**
  - [ ] Kubernetes deployment
  - [ ] Auto-scaling services
  - [ ] Multi-region support
  - [ ] CDN pour l'agent JS
  
- [ ] **Fonctionnalités Premium**
  - [ ] Session replay
  - [ ] Custom events tracking
  - [ ] API publique pour intégrations
  - [ ] White-label solution

### 🌟 Vision Long Terme (1-2 ans)
  
- [ ] **Écosystème**
  - [ ] Marketplace de plugins
  - [ ] Intégrations natives (Shopify, WordPress, etc.)



## 🤝 Contribution

1. Fork le projet
2. Créer une branch feature (`git checkout -b feature/amazing-feature`)
3. Commit les changements (`git commit -m 'Add amazing feature'`)
4. Push sur la branch (`git push origin feature/amazing-feature`)
5. Ouvrir une Pull Request

### Guidelines de Contribution
- Respecter les conventions de nommage
- Écrire des tests pour toute nouvelle fonctionnalité
- Documenter les changements
- Suivre les principes SOLID et Clean Code

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](https://github.com/VisuFlux/.github/blob/main/LICENSE) pour plus de détails.

---

<div align="center">
  <strong>Made with ❤️ by the VisuFlux Team</strong>
</div>
