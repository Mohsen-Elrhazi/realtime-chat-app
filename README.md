# 💬 Application de Chat Temps Réel

![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Flowbite](https://img.shields.io/badge/Flowbite-1C64F2?style=for-the-badge&logo=flowbite&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Pusher](https://img.shields.io/badge/Pusher-300D4F?style=for-the-badge&logo=pusher&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## 📋 À propos du projet

Application web de **messagerie instantanée** développée avec **Laravel**, permettant aux utilisateurs de communiquer en temps réel via **WebSockets** et **Pusher**, avec une interface moderne et responsive conçue avec **Tailwind CSS** et **Flowbite**.

---

## ✨ Fonctionnalités principales

* **🔐 Authentification & Gestion des comptes :** Inscription, connexion sécurisée et gestion du profil utilisateur.
* **⚡ Messagerie instantanée temps réel :** Envoi et réception immédiate de messages sans rechargement de page grâce à **Pusher / Laravel Echo** et **WebSockets**.
* **💬 Gestion des discussions :** Création de nouvelles conversations et navigation fluide entre les différents fils de discussion.
* **📜 Historique persistant :** Sauvegarde complète et consultation de l'historique des échanges dans **MySQL**.
* **📱 Interface responsive :** Design épuré adapté aux écrans desktop et mobile avec **Tailwind CSS** et **Flowbite**.

---

## 🏗️ Architecture & Aspects techniques

* **Architecture MVC multi-couches :** Organisation structurée autour des Contrôleurs, Modèles Eloquent, Vues Blade, Form Requests et Événements (*Events / Broadcasting*).
* **Communication événementielle (*Event Broadcasting*) :** Diffusion des événements Laravel en temps réel vers les clients connectés via **Pusher Channels** et **WebSockets**.
* **Frontend dynamique :** Interactions client fluides en **JavaScript** (Laravel Echo / Axios) combinées aux composants UI **Flowbite** et **Tailwind CSS**.
* **Sécurité & Bonnes pratiques :** Protection CSRF, validation stricte des requêtes, autorisation des canaux privés (`routes/channels.php`) et respect des principes **OOP**.
* **Conteneurisation :** Environnement prêt à l'emploi avec **Docker** pour faciliter le déploiement et la portabilité.

---

## 📂 Structure du projet

```text
├── app/
│   ├── Events/              # Événements de diffusion temps réel (MessageSent, etc.)
│   ├── Http/
│   │   ├── Controllers/     # Contrôleurs (Auth, Chat, Messages, Profil)
│   │   └── Requests/        # Validation des formulaires
│   └── Models/              # Modèles Eloquent (User, Conversation, Message)
├── database/
│   ├── migrations/          # Schéma de la base de données MySQL
│   └── seeders/             # Données de démonstration
├── resources/
│   ├── js/                  # Configuration Laravel Echo, Pusher & logique client
│   ├── css/                 # Fichiers Tailwind CSS
│   └── views/               # Vues Blade & composants Flowbite
├── routes/
│   ├── web.php              # Routes applicatives protégées
│   └── channels.php         # Autorisations des canaux WebSocket privés
└── docker-compose.yml       # Configuration des conteneurs Docker
