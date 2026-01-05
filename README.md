# SkyBlueIT – CI/CD Kubernetes & Helm

## Description
Projet DevOps mettant en place une chaîne CI/CD complète avec GitLab CI.
L’application est composée de trois microservices :
- gateway
- orders
- users

## Technologies utilisées
- Docker & DockerHub
- GitLab CI/CD
- Kubernetes (k3s)
- Helm
- GitHub

## Déploiement Kubernetes
Les manifestes Kubernetes sont disponibles dans le dossier `k8s/`.
Quatre environnements sont définis à l’aide de namespaces :
- dev
- qa
- staging
- prod

## Déploiement Helm
Un chart Helm est fourni dans le dossier `helm/skyblueit`.
Des fichiers values spécifiques sont utilisés pour chaque environnement.

## CI/CD
Le pipeline GitLab CI :
- construit les images Docker
- les pousse sur DockerHub
- déploie automatiquement sur dev, qa et staging
- déploie en production manuellement (branche main uniquement)
