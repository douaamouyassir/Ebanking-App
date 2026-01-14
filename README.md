#  Système de Gestion Bancaire

Application bancaire complète développée avec **Spring Boot** (Backend) et **Angular** (Frontend), intégrant un chatbot intelligent basé sur l'API OpenAI.

##  Description

Cette application est un système de gestion bancaire complet permettant :
- **Pour les Banquiers (ADMIN)** : Gestion complète des clients, comptes, opérations bancaires et statistiques
- **Pour les Clients (USER)** : Consultation de leurs comptes, historique des opérations, et effectuer des transferts
- **Chatbot Intelligent** : Assistant bancaire basé sur l'API OpenAI pour répondre aux questions des utilisateurs

## 📸 Captures d'écran

### Interface de Connexion
![img_6.png](img_6.png)
![img_7.png](img_7.png)

### Dashboard (Banquier - ADMIN)
![img_8.png](img_8.png)

**Description** : Vue d'ensemble avec statistiques globales, graphiques des opérations et répartition des comptes.

### Dashboard (Client - USER)
![img_9.png](img_9.png)

**Description** : Vue personnalisée pour les clients avec leurs comptes et opérations récentes.

### Gestion des Clients
![img_10.png](img_10.png)
![img_11.png](img_11.png)

**Description** : Liste des clients avec recherche, tri, pagination et actions (créer, modifier, supprimer).

### Gestion des Comptes
![img_12.png](img_12.png)
![img_13.png](img_13.png)
**Pour un client existant**
![img_14.png](img_14.png)
**Pour un nouveau client**
![img_15.png](img_15.png)

**Description** : Liste des comptes bancaires avec filtres par type et statut, création et modification.

### Mes Comptes (Client)
![img_16.png](img_16.png)

**Description** : Vue des comptes du client avec soldes et historique des opérations.

### Opérations Bancaires
![img_17.png](img_17.png)

**Description** : Interface pour effectuer des débits, crédits et transferts.

### Chatbot Intelligent
**cote client :**
![img_18.png](img_18.png)
**Cote admin :**
![img_19.png](img_19.png)

**Description** : Assistant bancaire intelligent accessible depuis toutes les pages de l'application.

### Historique des Opérations
![img_20.png](img_20.png)

**Description** : Historique détaillé des opérations avec filtres par date et type.

---

##  Technologies utilisées

### Backend
- **Spring Boot 3.2.0**
- **Spring Security** (Authentification JWT)
- **Spring Data JPA** (Hibernate)
- **H2 Database** (Base de données en mémoire)
- **Spring AI 1.0.0-M6** (Intégration OpenAI)
- **Maven** (Gestion des dépendances)
- **Java 17**

### Frontend
- **Angular 15**
- **TypeScript**
- **Bootstrap 5** (UI Framework)
- **RxJS** (Programmation réactive)
- **Bootstrap Icons** (Icônes)

##  Fonctionnalités

###  Pour les Banquiers (ADMIN)

#### Gestion des Clients
- ✅ Recherche et liste des clients
- ✅ Création de nouveaux clients
- ✅ Modification des informations clients
- ✅ Suppression de clients
- ✅ Consultation des détails clients
- ✅ Tri et pagination

#### Gestion des Comptes
- ✅ Liste de tous les comptes bancaires
- ✅ Création de comptes courants et épargne
- ✅ Modification des comptes (découvert autorisé, taux d'intérêt)
- ✅ Activation/Désactivation de comptes
- ✅ Consultation des détails de comptes
- ✅ Recherche et filtrage des comptes (par type, statut)
- ✅ Tri et pagination

#### Opérations Bancaires
- ✅ Débit sur un compte
- ✅ Crédit sur un compte
- ✅ Transfert entre comptes
- ✅ Historique des opérations

#### Statistiques
- ✅ Dashboard avec statistiques globales
- ✅ Nombre total de clients, comptes, opérations
- ✅ Solde total du système

#### Gestion des Utilisateurs
- ✅ Liste des utilisateurs
- ✅ Gestion des rôles (ADMIN/USER)
- ✅ Activation/Désactivation d'utilisateurs
- ✅ Changement de mot de passe

###  Pour les Clients (USER)

#### Mes Comptes
- ✅ Consultation de tous ses comptes
- ✅ Affichage du solde de chaque compte
- ✅ Historique des opérations par compte
- ✅ Détails des comptes (type, statut, découvert, taux d'intérêt)

#### Mes Transferts
- ✅ Effectuer des transferts entre comptes
- ✅ Sélection du compte source
- ✅ Saisie du compte de destination
- ✅ Montant et description du transfert

#### Historique
- ✅ Consultation de l'historique complet des opérations
- ✅ Filtrage par date et type d'opération

###  Chatbot Intelligent

- ✅ Assistant bancaire basé sur l'API OpenAI
- ✅ Réponses contextuelles selon le rôle (ADMIN/CLIENT)
- ✅ Accès aux données réelles via des outils (tools)
- ✅ Refus poli des questions hors contexte bancaire
- ✅ Service de fallback si l'API AI n'est pas disponible
- ✅ Interface utilisateur moderne et responsive

##  Prérequis

- **Java 17+**
- **Node.js 18+** et **npm**
- **Maven 3.6+**
- **Clé API OpenAI** 

##  Installation

### 1. Configuration Backend

Le backend utilise une base de données H2 en mémoire, aucune configuration supplémentaire n'est nécessaire.

#### Configuration du Chatbot IA 

Pour activer le chatbot IA, ajoutez votre clé API OpenAI dans `src/main/resources/application.properties` :

```properties
spring.ai.openai.api-key=votre-clé-api-openai
```

### 2. Installation Frontend

```bash
cd frontend
npm install
```

## ⚙ Configuration

### Backend (`src/main/resources/application.properties`)

### Frontend (`frontend/environments/environment.ts`)

##  Démarrage

### 1. Démarrer le Backend

```bash
# Depuis la racine du projet
mvn spring-boot:run
```

Ou avec Maven :

```bash
mvn spring-boot:run
```

Le serveur backend sera accessible sur `http://localhost:8081`

### 2. Démarrer le Frontend

```bash
# Depuis le dossier frontend
cd frontend
npm start
# ou
ng serve
```
Le frontend sera accessible sur `http://localhost:4200`


### Diagramme de Cas d'Utilisation (Use Case)

Le diagramme ci-dessous présente tous les cas d'utilisation pour les acteurs **ADMIN** (Banquier) et **USER** (Client) :

User :
![img_1.png](img_1.png)

Admin : 
![img_2.png](img_2.png)
![img_3.png](img_3.png)
![img_4.png](img_4.png)
![img_5.png](img_5.png)

### Diagramme de Classes

Le diagramme ci-dessous présente la structure complète des entités, leurs relations et les principales classes du système :
![images\img.png](img.png)



**Explication des classes principales :**
- **Customer** : Représente un client de la banque
- **BankAccount** : Classe abstraite pour les comptes bancaires
- **CurrentAccount** : Compte courant avec découvert autorisé (hérite de BankAccount)
- **SavingAccount** : Compte épargne avec taux d'intérêt (hérite de BankAccount)
- **AccountOperation** : Opération bancaire (crédit, débit, transfert)
- **AppUser** : Utilisateur du système (ADMIN ou USER)
- **AppRole** : Rôle utilisateur (ADMIN, USER)
- **AuditLog** : Journal d'audit pour la traçabilité
- **AccountStatus** : Statut d'un compte (enum)
- **OperationType** : Type d'opération (enum)

**Relations principales :**
- Un **Customer** peut posséder plusieurs **BankAccount** (1 à plusieurs)
- **CurrentAccount** et **SavingAccount** héritent de **BankAccount**
- Un **BankAccount** contient plusieurs **AccountOperation** (1 à plusieurs)
- Un **AppUser** peut avoir plusieurs **AppRole** (1 à plusieurs)
- Un **AppUser** peut être lié à un **Customer** (association optionnelle)

##  Structure du projet

```
exam_final_java/
├── src/main/java/org/example/exam/
│   ├── agents/              # Agent IA pour le chatbot
│   │   └── BankingAIAgent.java
│   ├── config/              # Configuration Spring
│   │   └── DataInitializer.java
│   ├── dtos/                # Data Transfer Objects
│   ├── entities/            # Entités JPA
│   ├── enums/               # Énumérations
│   │   └── AccountStatus.java
│   ├── exceptions/          # Exceptions personnalisées
│   ├── mappers/             # Mappers DTO
│   ├── repositories/        # Repositories JPA
│   ├── security/            # Configuration sécurité
│   ├── services/            # Services métier
│   │   ├── ChatbotFallbackService.java
│   │   └── BankAccountService.java
│   ├── tools/               # Outils pour l'IA
│   │   └── BankingAgentTools.java
│   └── web/                 # Contrôleurs REST
│       ├── ChatController.java
│       └── BankAccountRestAPI.java
├── src/main/resources/
│   └── application.properties
├── frontend/
│   ├── app/                 # Composants Angular
│   │   ├── account-management/
│   │   ├── edit-account/
│   │   ├── edit-customer/
│   │   └── my-transfers/
│   ├── accounts/            # Composant comptes client
│   ├── chatbot/             # Composant chatbot
│   ├── customers/           # Composant gestion clients
│   ├── services/            # Services Angular
│   ├── model/               # Modèles TypeScript
│   ├── guards/              # Guards de routage
│   └── environments/        # Configuration environnement
└── pom.xml
```


##  Chatbot IA

Le chatbot utilise l'API OpenAI pour fournir des réponses intelligentes basées sur les données réelles de l'application.

### Fonctionnalités du Chatbot

- ✅ Réponses contextuelles selon le rôle (ADMIN/CLIENT)
- ✅ Accès aux données réelles via des outils (tools)
- ✅ Refus poli des questions hors contexte bancaire
- ✅ Service de fallback si l'API AI n'est pas disponible
- ✅ Interface utilisateur moderne et compacte

### Exemples de questions

**Pour les Banquiers :**
- "Combien y a-t-il de clients ?"
- "Recherche le client Youssef"
- "Quelles sont les statistiques du système ?"
- "Quel est le solde de Karim Tazi ?"
- "Liste tous les comptes"

**Pour les Clients :**
- "Quel est mon solde ?"
- "Quels sont mes comptes ?"
- "Quels sont les types de comptes disponibles ?"
- "Comment effectuer un transfert ?"

### Configuration

Le chatbot nécessite une clé API OpenAI dans `application.properties` :

```properties
spring.ai.openai.api-key=votre-clé-api-openai
```

Si la clé n'est pas configurée, le système utilise un service de fallback basé sur des règles qui fournit des réponses préprogrammées.

##  Sécurité

- **Authentification JWT** : Tokens JWT pour l'authentification
- **Spring Security** : Protection des endpoints
- **Guards Angular** : Protection des routes frontend
- **Rôles** : ADMIN et USER avec permissions différentes
- **Audit Logging** : Journalisation de toutes les actions importantes

##  Base de données

L'application utilise **H2 Database** en mémoire avec les entités suivantes :
- `Customer` - Clients
- `BankAccount` (CurrentAccount, SavingAccount) - Comptes bancaires
- `AccountOperation` - Opérations bancaires
- `AppUser` - Utilisateurs
- `AppRole` - Rôles
- `AuditLog` - Journal d'audit

