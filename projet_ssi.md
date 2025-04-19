## Introduction :
Le projet Minecraft Secure Cluster est axé sur le déploiement d’un serveur Minecraft dans un environnement Kubernetes sécurisé en intégrant les bonnes pratiques DevSecOps. L’objectif est la mise en œuvre d’un pipeline CI/CD pour automatiser le déploiement, et ce dans un cadre garantissant la sécurité à chaque étape : du build de l’image au déploiement en cluster.

La solution repose sur une architecture clé en main articulée autour de :
- **GitLab CI** pour l'orchestration du pipeline
- **Kind (Kubernetes in Docker)** comme infrastructure locale
- **Trivy** (analyse de vulnérabilités) et **Cosign** (signature d'images)
- **RBAC Kubernetes** pour un contrôle d'accès granulaire

L’architecture globale du projet est la suivante :

[GitLab CI] -> [Build/Lint/Sign/Scan] -> [Registry] -> [Kubernetes (Kind)]  -> Minecraft Server

## Prérequis : 

Avant de commencer le projet, nous commençons par vérifier que toutes les installations ont été correctement effectuées : 

1. Docker
2. 
