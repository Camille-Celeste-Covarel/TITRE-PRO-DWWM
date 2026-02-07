⚡ Watts Up - Plateforme de Réservation de Bornes IRVE

    Note aux futurs candidats : Ce dépôt est partagé dans une démarche de transmission. Vous y trouverez mes dossiers de projet et cahiers des charges pour vous aider à comprendre les attendus du titre professionnel Développeur Web et Web Mobile (DWWM). Servez-vous en comme source d'inspiration pour structurer votre propre réussite !

🌟 Le Projet

Watts Up est un prototype d'application (MVP) réalisé pour la société fictive GeoCode. L'objectif : offrir une solution fluide et robuste pour localiser et réserver des bornes de recharge électrique parmi un parc national de plus de 136 000 points de charge.

L'application a été pensée Mobile First, garantissant une expérience utilisateur optimale en situation de mobilité.
🛠 Mon Rôle : Lead Tech & Product Owner

Sur ce projet réalisé en binôme (Agile Scrum), j'ai piloté la vision technique et l'architecture globale. Mon focus s'est porté sur la solidité du Backend et l'industrialisation du déploiement.
Mes réalisations majeures :

    Architecture BDD Spatiale : Implémentation de PostGIS pour gérer des requêtes de proximité complexes sur des milliers de coordonnées GPS avec une latence minimale.

    Ingénierie de la Data : Développement d'un moteur d'importation CSV en Streaming Node.js. Résultat : traitement de 136k lignes sans saturation de la RAM (une prouesse technique pour ce niveau de formation).

    Logique Métier Critique : Conception du cycle de vie des réservations (30 min) avec des tâches automatisées via Node-Cron et une protection stricte contre la double-réservation.

    DevOps & Industrialisation : Mise en place d'une pipeline CI/CD via GitHub Actions avec build d'images Docker et déploiement automatisé.

🚀 Stack Technique (La "Heavy" Stack)
Secteur	Technologies
Backend	Node.js, Express, TypeScript, Sequelize ORM
Frontend	React, Vite.js, TanStack Query, MapLibre GL JS
Database	PostgreSQL + PostGIS (Extension spatiale)
Infrastructure	Docker, GitHub Actions, Nginx, Debian 13
Sécurité	JWT (HttpOnly), Bcrypt, Express-rate-limit, UUID v4
📁 Ressources pour l'examen (Dossiers de Certification)

Pour aider la communauté et les futurs apprenants de la Wild Code School (ou d'ailleurs), je mets à disposition les documents officiels présentés au jury :

    📄 Dossier de Projet : Le cœur du réacteur. Analyse technique, choix d'architecture, modélisation et bilans.

    📄 Résumé du Cahier des Charges : La vision fonctionnelle et les besoins utilisateurs.

    📄 Support de Présentation : Le deck utilisé pour le passage devant le jury.

⚙️ Installation & Lancement

Le projet est entièrement containerisé pour garantir une parité totale entre les environnements de développement et de production.

    Clonage & Config :
    Bash

    git clone https://github.com/votre-username/watts-up.git
    cp .env.example .env

    Déploiement Docker :
    Bash

    docker compose up -d --build

    Accès : L'application est disponible sur localhost:5173. Les migrations Sequelize s'exécutent automatiquement pour initialiser la base PostGIS.

💡 Un mot sur la performance

Contrairement aux solutions classiques type Leaflet, nous avons opté pour MapLibre GL JS pour exploiter le rendu GPU. Couplé à notre backend optimisé, l'affichage de milliers de bornes reste fluide, même sur des appareils mobiles d'entrée de gamme.

Réalisé avec passion par Camille Céleste Covarel - 2025
