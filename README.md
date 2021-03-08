# Joomla CMS Development Docker Setup

> Docker Compose setup for Joomla with Joomla, MySQL, phpMyAdmin, & Composer Docker images.

## Stuff

The app folder will house the Joomla files. The docker folder will contain the docker compose file and code, config and data folders.

- the code folder is intended for putting project files for component, module, plugin development.
- cd to app/docker/ and run docker compose up -d to start the containers.
- Joomla is running at localhost:8080
- phpMyAdmin is running at localhost:8000

- Configure mysqli support.

  > Until coming up with a better approach follow next steps to setup mysqli support in container.

- On first run after running docker-compose up -d in order to support mysqli run the next steps inside the apache php container in the cli.
- docker-php-ext-install mysqli
- docker-php-ext-enable mysqli
- apachectl restart
