# Quote App — Déploiement Docker

Ce dépôt contient le fichier `docker-compose.yml` pour lancer l'application **Quote App** (frontend + backend) à partir d'images Docker hébergées sur Docker Hub.

---

## 🔧 Prérequis

- Docker installé : https://www.docker.com/products/docker-desktop
- Docker Hub login avec accès aux images

---

## 🚀 Lancement

Dans un terminal, à la racine du projet :

```bash
docker-compose up
```

- Le **frontend** sera accessible sur `http://localhost:3000`
- Le **backend** tournera sur `http://localhost:5000`

---

## 📦 Structure

- `backend` : Fournit une API pour retourner ou ajouter des citations (`GET` et `POST /quotes`)
- `frontend` : Application React affichant une citation aléatoire et permettant d’en ajouter

---

## 🌐 Images Docker

- Backend : [`akramch77/quote-backend`](https://hub.docker.com/r/akramch77/quote-backend)
- Frontend : [`akramch77/quote-frontend`](https://hub.docker.com/r/akramch77/quote-frontend)

---

## 🧠 Questions de réflexion

### 1. Quelle différence fais-tu entre un `Dockerfile` et un `docker-compose.yml` ?

- **`Dockerfile`** : Sert à définir l’image d’un service. Il contient les instructions pour construire un conteneur : copier les fichiers, installer les dépendances, définir la commande de démarrage, etc.
- **`docker-compose.yml`** : Sert à orchestrer plusieurs services ensemble (frontend, backend, BDD, etc.). Il utilise les images définies par les `Dockerfile` ou celles sur Docker Hub.

---

### 2. Quels sont les avantages de séparer les services dans une architecture Docker ?

- **Isolation** : Chaque service fonctionne indépendamment des autres.
- **Scalabilité** : Tu peux scaler un service spécifique selon les besoins.
- **Maintenance** : Plus facile à tester, mettre à jour ou redémarrer individuellement.
- **Réutilisabilité** : Tu peux réutiliser des services dans d'autres projets.

---

### 3. En quoi Docker Compose facilite-t-il le travail en équipe et le déploiement ?

- **Configuration centralisée** dans un seul fichier.
- **Comportement identique** sur toutes les machines.
- **Déploiement rapide** avec une seule commande `docker-compose up`.
- **Automatisation facile** dans des pipelines CI/CD.

---

### 4. Pourquoi est-il utile de publier une image sur Docker Hub même pour un projet perso ?

- **Partage simple** avec d'autres développeurs.
- **Portabilité** : déploiement sur tout serveur avec Docker.
- **Sauvegarde** de version fonctionnelle.
- **Intégration CI/CD** facilitée pour des builds automatisés.

---
