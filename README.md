# Kanpus ERP

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

<img src="./doc/img/header.png">

## **Détails du projet**

Kampus ERP (Entreprise Ressource Planning), destiné au centre de formation.

L’application permet une foix connecter, l’agenda des évènements, et des lieux (salle de classe).

Les élèves peuve consulter en lecture seule leur calendrier , tandis que les formateurs peuvent créer modifier et supprimer les évènements, les lieux, les promos, les absences.

Se repos contiens l’API REST de Kanpus



## Technologies utilisées

- Node.js
- Express
- PostgresSQL
- JWT
- B-crypy
- Joy
- Express File upload

## Documents

[Voir la DOC API](./doc/ApiDoc.md)

[Voir Les roles et permition](./doc/permissions.md)

## Base de données

<img src="./doc/img/MCD-kanpus.png">

## Instalation de l’api

Cloner le repos github 

```markdown
git clone git@github.com:deldon/API-Kanpus.git
```

Installer des dépendance npm 

```markdown
npm i
```

Crée un dossier “logs” avec a l’interieur un fichier error.log a la racine du projet.

Modifier le fichier .env

```markdown
PORT=5000
DATABASE_URL=postgres://user:password@localhost:5432/db
SECRET_KEY=aaaaa
URL_SERVER=http://localhost:5000/
```

Crée une bdd avec postgres sql

```markdown
sudo -i -u postgres psql
CREATE DATABASE kanpus OWNER myuser;
```

Déployer la bdd avec sqitch

```markdown
sqitch init kanpus --engine pg --target db:pg:kanpus --top-dir migrations
sqitch deploy
```

**Démarer l’API**
```
npm run dev
```
<img src="./doc/img/kanpus.png">

## Participants au projet

****Romain Deldon****

****Marc Smaniotto****

Une application front a etais developer avec react par :

****Ludovic Lecoq****

****Inès Lujian****
