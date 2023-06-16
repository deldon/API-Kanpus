# Kanpus ERP

![Node.js](https://img.shields.io/badge/Node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20Web%20Tokens)

<img src="./doc/img/header.png">

## **Détails du projet**

Kanpus ERP (Enterprise Resource Planning), destiné au centre de formation.

L'application permet, une fois connecté, la gestion de l'agenda des événements et des lieux (salles de classe).

Les élèves peuvent consulter en lecture seule leur calendrier, tandis que les formateurs peuvent créer, modifier et supprimer les événements, les lieux, les promotions et les absences.

Ce dépôt contient l'API REST de Kanpus.

## Technologies utilisées

- Node.js
- Express
- PostgreSQL
- JWT
- Bcrypt
- Joi
- Express File Upload

## Documents

[Consulter la documentation de l'API](./doc/ApiDoc.md)

[Consulter les rôles et les permissions](./doc/permissions.md)

## Base de données

<img src="./doc/img/MCD-kanpus.png">

## Installation de l'API

Cloner le dépôt GitHub :

```markdown
git clone git@github.com:deldon/API-Kanpus.git
```

Installer les dépendances npm :

```markdown
npm install
```

Créer un dossier "logs" avec un fichier error.log à la racine du projet.

Modifier le fichier .env :

```markdown
PORT=5000
DATABASE_URL=postgres://user:password@localhost:5432/db
SECRET_KEY=aaaaa
URL_SERVER=http://localhost:5000/
```

Créer une base de données PostgreSQL :

```markdown
sudo -i -u postgres psql
CREATE DATABASE kanpus OWNER myuser;
```

Déployer la base de données avec Sqitch :

```markdown
sqitch init kanpus --engine pg --target db:pg:kanpus --top-dir migrations
sqitch deploy
```

**Démarrer l'API**
```
npm run dev
```
<img src="./doc/img/kanpus.png">

## Participants au projet

- Romain Deldon
- Marc Smaniotto

Une application front-end a été développée avec React par :

- Ludovic Lecoq
- Inès Lujian
