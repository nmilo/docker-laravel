# Laravel Docker
Set of Docker containers for Laravel app development

## Requirements
To get started, make sure you have Docker installed on your system. Clone this repo, and copy your Laravel project into the src directory.

## Usage
Build docker containers
`docker-compose build` 

Start docker containers
`docker-compose up -d`

To run a command inside any of the docker containers
`docker-compose exec <container_name> <command>`

To attach shell directly to container 
`docker-compose exec <container_name> /bin/sh`

To close docker containers
  `docker-compose down`
  
To run command as sudo, append --user=root to your command
`docker-compose exec --user=root <container_name> <command>`

Visit http://localhost:8080/ to see your application


# Set file permissions on Laravel storage folder
`chgrp -R www-data src/storage`

Note: Add yourself to www-data user group, if you also want to edit storage files.

# Database connection params for env file
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
```