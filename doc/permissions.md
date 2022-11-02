# PERMISSIONS

## SIGNIN

| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/signin/                       |    ✔️  |   ✔️    |    ✔️    |    ✔️    |
|post    |/signin/                       |    ✔️  |   ✔️    |    ✔️    |    ✔️    |


## EVENT

| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/event/organizer/:date         |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|post    |/event/check_date/:event_id    |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|post    |/event/                        |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|get     |/event/my_course/:page_number  |    ✔️  |   ✔️    |    ✔️    |    ⛔    |
|patch   |/event/:event_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|get     |/event/:event_id               |    ✔️  |   ✔️    |    ✔️    |    ⛔    |
|delete  |/event/:event_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔    |


## USER

| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/user/event_form/              |    ✔️  |   ✔️    |    ⛔    |    ⛔ |


## TRAINEE
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/user/trainee/                 |   ✔️  |   ✔️    |    ⛔    |    ⛔ |
|get     |/user/trainee/:user_id         |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|get     |/user/trainee/:user_id         |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|post    |/user/trainee/                 |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|patch   |/user/trainee/:user_id         |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|delete  |/user/trainee/:user_id         |    ✔️  |   ✔️    |    ⛔    |    ⛔ |



## FORMER
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/user/former                   |    ✔️  |   ⛔   |    ⛔    |    ⛔ |
|get     |/user/former/:user_id          |    ✔️  |   ⛔   |    ⛔    |    ⛔ |
|post    |/user/former/                  |    ✔️  |   ⛔   |    ⛔    |    ⛔ |
|patch   |/user/former/:user_id          |    ✔️  |   ⛔   |    ⛔    |    ⛔ |
|delete  |/user/former/:user_id          |    ✔️  |   ⛔   |    ⛔    |    ⛔ |


## PASSWORD
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|patch   |/user/password                 |    ✔️  |   ✔️    |    ✔️    |    ⛔ |
|patch   |/user/password/:user_id        |    ✔️  |   ⛔   |    ⛔    |    ⛔ |


## PLACE
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/place/                        |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|post    |/place/                        |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|patch   |/place/:place_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔ |
|delete  |/place/:place_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔ |


## PROMO
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/promo/                        |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|post    |/promo/                        |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|patch   |/promo/:promo_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|delete  |/promo/:promo_id               |    ✔️  |   ✔️    |    ⛔    |    ⛔    |


## SETTINGS
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/settings/                     |    ✔️  |   ⛔   |    ⛔    |    ⛔    |
|put     |/settings/                     |    ✔️  |   ⛔   |    ⛔    |    ⛔    |


## ABSENCE
| METHOD | ROUTE                         | ADMIN | FORMER | TRAINEE | GUEST |
|--------|-------------------------------|-------|--------|---------|-------|
|get     |/absence/:user_id              |    ✔️  |   ✔️    |    ⛔    |    ⛔    |
|patch   |/absence/:event_id             |    ✔️  |   ✔️    |    ⛔    |    ⛔    |