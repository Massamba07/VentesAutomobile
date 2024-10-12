# Analyse des Ventes et Prédiction des Tendances du Marché Automobile

## Objectif du Projet

Ce projet vise à créer une **architecture de pipeline de données** permettant de suivre les ventes de véhicules en temps réel, de générer des tableaux de bord interactifs et d'anticiper les tendances du marché automobile. L'objectif est d'aider les équipes métiers à prendre des décisions basées sur des données précises et actuelles.

## Stack Technique

Les outils et technologies utilisés pour ce projet incluent :

- **Langage de programmation** : SQL
- **Entrepôt de données** : Snowflake
- **Intégration et collecte de données** : Airbyte
- **Transformation des données** : dbt (Data Build Tool)
- **Automatisation des pipelines** : GitLab CI/CD, Rundeck
- **Visualisation des données** : Power BI, Metabase

## Architecture du Projet

Voici les principales étapes du pipeline de données, de la collecte des données à la visualisation.

### 1. Collecte des Données

**Airbyte** est utilisé pour extraire les données de plusieurs sources :
- Données internes de vente (ERP, CRM) : modèles de véhicules, dates de vente, prix, localisation des concessions.
- Données externes (API, réseaux sociaux, données de marché) : tendances du marché, prix du carburant, etc.

Les données extraites sont ensuite chargées dans un entrepôt de données centralisé.

### 2. Entrepôt de Données

**Snowflake** sert d'entrepôt de données central pour stocker les données brutes et transformées. C'est ici que les données sont organisées et prêtes pour les transformations.

### 3. Transformation des Données

Les données brutes sont transformées à l'aide de **dbt** pour :
- Nettoyer et structurer les données.
- Créer des modèles analytiques agrégés (ventes par modèle, par région, par concessionnaire).
- Générer des KPI comme le nombre de véhicules vendus, les prix moyens, et les parts de marché.

### 4. Automatisation des Pipelines

- **GitLab CI/CD** permet l'intégration continue des scripts SQL et l'automatisation des déploiements.
- **Rundeck** est utilisé pour l'automatisation de l'exécution des tâches récurrentes, comme la mise à jour quotidienne des données et l'exécution hebdomadaire de prédictions.

### 5. Visualisation des Données

Les données transformées sont visualisées à l'aide de **Power BI** et **Metabase** :
- Création de tableaux de bord pour le suivi des performances des ventes.
- Visualisation des tendances du marché (ventes par modèle, type de motorisation, etc.).
- Rapports interactifs pour les équipes métiers, facilitant la prise de décision.

## Schéma de l'Architecture

Voici un aperçu visuel de l'architecture du pipeline de données :

![Architecture](path_to_image)

## Utilisation

1. **Cloner le projet** :
   ```bash
   git clone https://github.com/username/repository.git
