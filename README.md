# ⚡ Watts Up | Plateforme de Réservation IRVE

<p align="center">
  <img src="https://img.shields.io/badge/Role-Lead_Tech_%26_PO-61dafb?style=for-the-badge&logo=react" alt="Role">
  <img src="https://img.shields.io/badge/Backend-Node.js_%26_PostGIS-339933?style=for-the-badge&logo=node.js" alt="Backend">
  <img src="https://img.shields.io/badge/Infrastructure-Docker_%26_CI--CD-2496ed?style=for-the-badge&logo=docker" alt="Infra">
</p>

---

## 👤 À propos de moi

Salut ! 👋 Moi, c'est **Camille Céleste Covarel**.

Développeuse Fullstack avec une forte affinité pour le **Backend** et l'**Architecture logicielle**, j'ai réalisé ce projet dans le cadre de mon Titre Professionnel "Développeur Web et Web Mobile" (DWWM) fin 2025 à la **Wild Code School Toulouse**.

Sur **Watts Up**, j'ai endossé les rôles de **Lead Tech** et **Product Owner**. Mon objectif était de construire une infrastructure robuste, capable d'absorber des volumes de données importants (Open Data IRVE) tout en garantissant une expérience fluide et sécurisée.

> **🤝 Pourquoi ce partage ?**
> Je sais à quel point la préparation d'un titre pro peut être intense. Je partage mes documents officiels (Dossier de Projet, Cahier des Charges, etc.) pour aider les prochains candidats à visualiser les attentes du jury et la structure d'un projet de fin d'études réussi. 
> *Servez-vous en pour apprendre et structurer votre pensée, pas pour copier-coller !*

---

## 🌟 Présentation du projet
**Watts Up** est une solution "Mobile First" développée pour répondre aux défis de la mobilité électrique. L'application permet de gérer et de réserver des points de charge parmi un parc national de plus de **136 000 bornes**.

### 🎯 Objectifs du MVP
* **Localisation précise** via une carte interactive haute performance.
* **Réservation intelligente** de 30 minutes avec gestion automatisée du cycle de vie.
* **Back-office Admin** pour le monitoring et la mise à jour massive des données.

---

## 🛠 La "Sauce" Technique (Why it biches ✨)

En tant que Lead Tech, j'ai fait des choix d'architecture ambitieux pour dépasser le simple CRUD :

### 🛰️ Géospatial & Performance
* **PostGIS :** Utilisation de la puissance de PostgreSQL et de son extension spatiale pour des requêtes de proximité ultra-rapides.
* **MapLibre GL JS :** Rendu GPU pour une fluidité absolue sur mobile, même avec une densité de points importante.

### 🏎️ Data Engineering
* **Streaming CSV :** L'import des 136k lignes de données gouvernementales est géré via un système de **Streaming Node.js**. Résultat : zéro saturation de la RAM et une stabilité serveur totale.

### ⛓️ DevOps & Sécurité
* **CI/CD :** Pipeline automatisée via GitHub Actions (Build, Test & Deploy).
* **Conteneurisation :** Environnement 100% Dockerisé pour une parité Dev/Prod parfaite.
* **Hardening :** JWT en cookies HttpOnly, UUID v4 pour contrer l'énumération, et protection contre le brute-force via `express-rate-limit`.

---

## 🏗 Stack Technique

| Backend | Frontend | Infra / Ops |
| :--- | :--- | :--- |
| **Node.js** / **TypeScript** | **React** / Vite.js | **Docker** & Compose |
| **PostgreSQL** / **PostGIS** | TanStack Query | GitHub Actions |
| Sequelize ORM | MapLibre GL JS | Nginx / Debian 13 |
| Node-Cron | Tailwind CSS | JWT / Bcrypt |

---

## 📁 Ressources pour l'examen

Retrouvez ci-dessous les documents que j'ai présentés pour valider mon titre :

* 📘 [**Dossier de Projet**](./camille_celeste_covarel_dossier_projet.pdf) : Analyse technique profonde, modélisation BDD et bilans.
* 📙 [**Résumé du Cahier des Charges**](./Covarel_Camille_Resume_de_cahier_des_charges.pdf) : Vision produit et périmètre fonctionnel.
* 🖥️ [**Support de Présentation Jury**](./DWWM_Presentation.pdf) : Le deck utilisé pour l'oral final.

---

## ⚙️ Installation

```bash
# 1. Cloner le repo
git clone [https://github.com/votre-compte/watts-up.git](https://github.com/votre-compte/watts-up.git)

# 2. Setup l'environnement
cp .env.example .env

# 3. Lancer l'infrastructure
docker compose up -d --build
