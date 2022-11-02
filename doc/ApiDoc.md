# API-DOC kanpus

14/04/2022

# absence

### PATCH /absence/9

Ajouter des trainee absents à un événement

### Request :

```json
{
	"users": [
		6
	]
}
```

### GET /absence/7

Voir toutes les absences d'un trainee

# login

### GET /signin

Retourne les informations de la structure pour la page login.

### POST /signin

Connecter un user

### Request :

```json
{

"email": "former@gmail.com",
"password": "kanpus"

}

```

# settings

### GET /settings

Retourne toutes les informations de la structure.

### PUT /settings

Modifie les informations de la structure.

### Request :

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

# user

### GET /user/event_form

Tous les users triés par group et par promo

# former

### GET /user/former

Retourne tous les former triés par is_permanent (titulaires ou Intervenants)

### GET /user/former/2

Retourne les infos d'un former par id

### POST /user/former

Ajouter un former

### Request :

```json
	{
			"firstname":"ludo",
			"lastname":"cc",
			"address":"3 rue de la paix 14800 deauville",
			"phone_number":"+33569698794",
			"email":"formef99r@gmail.com",
			"image":"phil.jpg",
			"new_password":"kanpus",
			"confirm_new_password":"kanpus",
			"is_permanent":true,
			"color":"#458498"
		}

```

### PATCH /user/former/11

Modifie un former par son id.

### Request :

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

Supprime un former par son id.

# Trainee

### GET /user/trainee

Tous les trainee triés par promo avec les trainee sans promo, pour la page élève

### GET /user/trainee/65

Retourne les infos d'un trainee par id

### POST /user/trainee

Ajouter un trainee

### Request :

```json
	{
			"firstname":"999",
			"lastname":"imca",
			"address":"3 rue de la paix 14800 deauville",
			"phone_number":"+33569698794",
			"email":"trainee999@gmail.com",
			"image":"phil.jpg",
			"new_password":"kanpus",
			"confirm_new_password":"kanpus",
			"promo_id":1
}

```

### PATCH /user/trainee/65

Modifie un trainee par son id.

### Request :

```json
	{
			"firstname":"romanros",
			"lastname":"deldonos",
			"address":"3 rue de la paix 14800 deauville",
			"phone_number":"33569698794",
			"email":"83ldgdo99rgt88k@pmail.com",
			"image":"phil.jpg",
			"promo_id":1
	}

```

### DELETE /user/trainee/13

Supprime un trainee par son id.

### PATCH /user/password

Modifie le mot de password du user connecté.

### Request :

```json
        {
            "old_password":"romain2",
            "new_password":"romain3",
            "repeat_password":"romain3"
        }

```

### PATCH /user/password/14

Modifie le mot de password d'un user par son id.

### Request :

```json
        {
            "old_password":"kanpus",
            "new_password":"romain",
            "repeat_password":"romain"
        }

```

# event

### GET /event/organizer/2022-04-11

Tous les events pour l'organizer de la date indiqué à plus 5 jours

### GET /event/1

Retourne un event par rapport à un id

### GET /event/my_course/1

Les events à partir de la date du jour pour un user (former ou trainee) , trier par date de début de l'event avec la pagination qui débute à 1 .

### POST /event/check_date/null

Retourne les place et les former disponibles pour les dates indiquées.

### Request :

```json
{
	"name": "MARVIN LAURENCE",
	"start_date": "2022-05-03 09:15:00",
	"end_date": "2022-05-04 17:30:00"
}

```

### POST /event

Ajoute un nouveau event avec les users associer

### Request :

```json
{
		"name":"yiyi",
		"address":"",
		"note":"",
		"equipment":"",
		"role":"",
		"start_date":"2022-04-19 12:30:00",
		"end_date":"2022-04-27 12:25:00",
		"place_id":2,
		"trainee":[2],
		"former":[6]
}
```

### PATCH /event/16

Modifie un event et les users associer par rapport à son id

### Request :

```json
{
		"name":"font mark",
		"address":"null",
		"note":"txt",
		"equipment":"txyt",
		"role":"Perchamn",
		"start_date":"2022-03-28 09:31:00+02",
		"end_date":"2022-03-28 15:00:00+02",
		"place_id":6,
		"trainee":[1,2],
		"former":[4,6]
}
```

### DELETE /event/26

Supprimer un event par id

# place

### GET /place

Tous les places trier par position

### POST /place/

Ajouter une place

### Request :

```json
{
	"name":"studio 679",
	"position":15
}
```

### PATCH /place/10

Modifier une place par rapport à son id

### Request :

```json
{
	"name":"Studio 665",
	"position":20
}
```

### DELETE /place/12

Supprimer une place par rapport à son id

# promo

### GET /promo

Retourne toutes les promos.

### POST /promo

Ajouter une promo

### Request :

```json
{
	"name":"zag"
}
```

### PATCH /promo/5

Modifier une promo par rapport à son id

### Request :

```json
{
	"name":"Stage été"
}
```

### DELETE /promo/3

Supprimer une promo par rapport à son id