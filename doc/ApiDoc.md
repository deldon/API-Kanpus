# API-DOC Kanpus

14/04/2022

# Absence

### PATCH /absence/9

Ajouter des stagiaires absents à un événement

### Requête :

```json
{
	"users": [
		6
	]
}
```

### GET /absence/7

Voir toutes les absences d'un stagiaire

# Login

### GET /signin

Retourne les informations de la structure pour la page de connexion.

### POST /signin

Connecter un utilisateur

### Requête :

```json
{
	"email": "former@gmail.com",
	"password": "kanpus"
}
```

# Settings

### GET /settings

Retourne toutes les informations de la structure.

### PUT /settings

Modifie les informations de la structure.

### Requête :

```json
{
  "name": "IMCA PROVENCE",
  "address": "Résidence de l’Etoile – 27 boulevard Roger Ricca – 84700 SORGUES",
  "phone_number": "0490861537",
  "email": "info@imca-provence.com",
  "url_image": "image.jpg",
  "course_start_hour_am": "15:31:12",
  "course_end_hour_am": "15:31:12",
  "course_start_hour_pm": "15:31:12",
  "course_end_hour_pm": "15:31:12"
}
```

# User

### GET /user/event_form

Tous les utilisateurs triés par groupe et par promotion

# Former

### GET /user/former

Retourne tous les formateurs triés par statut (titulaires ou intervenants)

### GET /user/former/2

Retourne les informations d'un formateur par son ID

### POST /user/former

Ajouter un formateur

### Requête :

```json
{
	"firstname": "ludo",
	"lastname": "cc",
	"address": "3 rue de la paix 14800 deauville",
	"phone_number": "+33569698794",
	"email": "formef99r@gmail.com",
	"image": "phil.jpg",
	"new_password": "kanpus",
	"confirm_new_password": "kanpus",
	"is_permanent": true,
	"color": "#458498"
}
```

### PATCH /user/former/11

Modifie un formateur par son ID.

### Requête :

```json
{
	"firstname": "Alains",
	"lastname": "Deloins",
	"address": "45 rue fernand michel 84000 AVIGNON",
	"phone_number": "+33678956412",
	"email": "a.del99oin@gmail.com",
	"image": "<http://localhost:5000/avatar/thumbnail.png>",
	"color": "#269987",
	"is_permanent": true
}
```

### DELETE /user/former/11

Supprime un formateur par son ID.

# Trainee

### GET /user/trainee

Tous les stagiaires triés par promotion, y compris ceux sans promotion, pour la page des élèves

### GET /user/trainee/65

Retourne les informations d'un stagiaire par son ID

### POST /user/trainee

Ajouter un stagiaire

### Requête :

```json
{
	"firstname": "999",
	"lastname": "imca",
	"address": "3 rue de la paix 14800 de

auville",
	"phone_number": "+33569698794",
	"email": "trainee999@gmail.com",
	"image": "phil.jpg",
	"new_password": "kanpus",
	"confirm_new_password": "kanpus",
	"promo_id": 1
}
```

### PATCH /user/trainee/65

Modifie un stagiaire par son ID.

### Requête :

```json
{
	"firstname": "romanros",
	"lastname": "deldonos",
	"address": "3 rue de la paix 14800 deauville",
	"phone_number": "33569698794",
	"email": "83ldgdo99rgt88k@pmail.com",
	"image": "phil.jpg",
	"promo_id": 1
}
```

### DELETE /user/trainee/13

Supprime un stagiaire par son ID.

### PATCH /user/password

Modifie le mot de passe de l'utilisateur connecté.

### Requête :

```json
{
	"old_password": "romain2",
	"new_password": "romain3",
	"repeat_password": "romain3"
}
```

### PATCH /user/password/14

Modifie le mot de passe d'un utilisateur par son ID.

### Requête :

```json
{
	"old_password": "kanpus",
	"new_password": "romain",
	"repeat_password": "romain"
}
```

# Event

### GET /event/organizer/2022-04-11

Tous les événements pour l'organisateur à partir de la date indiquée jusqu'à 5 jours plus tard

### GET /event/1

Retourne un événement par son ID

### GET /event/my_course/1

Les événements à partir de la date du jour pour un utilisateur (formateur ou stagiaire), triés par date de début de l'événement avec une pagination commençant à 1.

### POST /event/check_date/null

Retourne les places et les formateurs disponibles pour les dates indiquées.

### Requête :

```json
{
	"name": "MARVIN LAURENCE",
	"start_date": "2022-05-03 09:15:00",
	"end_date": "2022-05-04 17:30:00"
}
```

### POST /event

Ajoute un nouvel événement avec les utilisateurs associés

### Requête :

```json
{
	"name": "yiyi",
	"address": "",
	"note": "",
	"equipment": "",
	"role": "",
	"start_date": "2022-04-19 12:30:00",
	"end_date": "2022-04-27 12:25:00",
	"place_id": 2,
	"trainee": [2],
	"former": [6]
}
```

### PATCH /event/16

Modifie un événement et les utilisateurs associés par son ID

### Requête :

```json
{
	"name": "font mark",
	"address": "null",
	"note": "txt",
	"equipment": "txyt",
	"role": "Perchamn",
	"start_date": "2022-03-28 09:31:00+02",
	"end_date": "2022-03-28 15:00:00+02",
	"place_id": 6,
	"trainee": [1, 2

],
	"former": [4, 6]
}
```

### DELETE /event/26

Supprimer un événement par son ID

# Place

### GET /place

Tous les lieux triés par position

### POST /place/

Ajouter un lieu

### Requête :

```json
{
	"name": "studio 679",
	"position": 15
}
```

### PATCH /place/10

Modifier un lieu par son ID

### Requête :

```json
{
	"name": "Studio 665",
	"position": 20
}
```

### DELETE /place/12

Supprimer un lieu par son ID

# Promo

### GET /promo

Retourne toutes les promotions

### POST /promo

Ajouter une promotion

### Requête :

```json
{
	"name": "zag"
}
```

### PATCH /promo/5

Modifier une promotion par son ID

### Requête :

```json
{
	"name": "Stage été"
}
```

### DELETE /promo/3

Supprimer une promotion par son ID
