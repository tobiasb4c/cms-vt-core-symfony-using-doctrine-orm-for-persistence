# CMS-VT | CORE | Symfony - Using Doctrine ORM for persistence

## Overview
The action movie fan club “The Die Hards” are looking to have a famous movie quotes database created.
Because many standard functionalities are needed, your agency suggested to use the Symfony PHP framework for this task.

## User Story 1
*As an EDITOR I want to be able to add new movie quotes to the database, so that the public can query for them later.*

### Acceptance Criteria
- A model for a movie exists
  -Movie name
  -Movie release year
- A model for a movie quote exists
  - Quote
  - Character who quotes
  - Movie (relation)
- New quotes can be added via console or form to the database

## User Story 2
*As an EDITOR I want to be able to list existing movie quotes, so I have an overview what is already stored in the database.*

### Acceptance Criteria
- All quotes existing in the database are listed alphabetically by movie name, featuring the following information:
  - Movie name
  - Movie release year
  - Quote
  - Character who quotes

## User Story 3
*As an EDITOR I want to be able to remove existing movie quotes, so I can delete wrong information from the pool of available quotes.*

### Acceptance Criteria
- Editors can remove movie quote entries from the overview via click of a button

## User Story 4
*As an EDITOR I want to be able to add movies, so I can add quotes for movies not currently present in the databases*

### Acceptance Criteria
- Editors can add movie entries from the overview via click of a button


#### Links
https://my.skilldisplay.eu/en/skillset/120

### Befehle 
- Datenbank definieren in .env

- Make Bundler install
```
composer require --dev symfony/maker-bundle
```

- controller erstellen lassen
```
symfony console make:controller
```

- Model erstellen lassen
```
symfony console make:entity
```

- Datenbabnk ertellen lassen 
``` 
php bin/console doctrine:database:create
```

- Migration erstellen
```
php bin/console make:migration
```

- Datenbank migrieren. Aktualisieren damit die Datenbank die neue Migration anwendet
```
php bin/console doctrine:migrations:migrate
```

- Make Crud befehl 
```
php bin/console make:admin:crud
```
