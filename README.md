# Task Manager API

Task Manager API est une application développée avec NestJS qui permet de gérer des tâches grâce à une API REST. Elle inclut des fonctionnalités de création, consultation, mise à jour et suppression de tâches.

🛠️ Fonctionnalités

    Créer une tâche : Ajouter une nouvelle tâche avec un titre, une description (facultative) et un statut par défaut.
    Consulter les tâches : Récupérer toutes les tâches ou une tâche spécifique grâce à son ID.
    Mettre à jour une tâche : Modifier le titre, la description ou le statut d'une tâche existante.
    Supprimer une tâche : Supprimer une tâche en fonction de son ID.

🚀 Technologies utilisées

    NestJS : Framework Node.js pour développer des applications évolutives.
    TypeORM : ORM pour interagir avec une base de données SQLite.
    Docker : Conteneurisation pour une exécution simplifiée.
    Swagger : Documentation interactive de l'API.

📂 Structure des dossiers

src/
├── tasks/                      # Module des tâches
│   ├── dto/                    # Data Transfer Objects
│   ├── entities/               # Entités TypeORM
│   ├── tasks.controller.ts     # Contrôleur des tâches
│   ├── tasks.service.ts        # Service pour la logique métier
│   └── tasks.module.ts         # Module des tâches
├── app.module.ts               # Module racine
├── main.ts                     # Point d'entrée de l'application

⚙️ Installation et exécution

1. Cloner le projet

git clone [https://github.com/KMAit/taskmanagerapi.git](https://github.com/KMAit/taskmanagerapi.git)
cd task-manager

2. Installer les dépendances

npm install

3. Configurer les variables d'environnement

Créer un fichier .env à la racine du projet :

DATABASE_TYPE=sqlite
DATABASE_NAME=tasks.db
PORT=3000

4. Lancer le projet en local

npm run start

5. Conteneuriser avec Docker (optionnel)

Construire l'image Docker :

docker build -t task-manager .

Lancer le conteneur Docker :

docker run -p 3000:3000 task-manager

🧪 Utilisation de l'API

Documentation interactive

Accéder à Swagger pour tester les endpoints de l'API :

    URL : http://localhost:3000/api

Endpoints disponibles
Méthode Endpoint Description
POST    /tasks      Créer une nouvelle tâche
GET     /tasks      Récupérer toutes les tâches
GET     /tasks/:id  Récupérer une tâche par son ID
PATCH   /tasks/:id  Mettre à jour une tâche
DELETE  /tasks/:id  Supprimer une tâche

🛡️ Tests

Tests end-to-end

npm run test:e2e

📄 Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.
