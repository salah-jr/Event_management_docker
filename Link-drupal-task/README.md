# event_management

## Installation

- Clone the project files into a directory.
- At your project terminal which `docker-compose.yml` exists.
- Run `docker-compose up -d --build`. (make sure to run the docker engine)
- Run `composer install` in the `src/app` directory. This will download all the required packages for the platform.
- Fill in your database credentials via the UI and install your drupal site. (this data will come from the docker container).
```
database_name: drupal
database_user: root
database_password: root
database_host: mysql      // The database container name
database_port: 3306
```
- In your settings.php, at the bottom add `$settings['config_sync_directory'] = 'sites/default/config/sync';`
- Got to `src/app`.
- Run `drush config-import -y` to enable the required modules and import all configuration that comes with them

### Note
- The route for the subtask "page for listing published events is: `/events/published`"

<br>

### If you have a problem with configs, please find the attached database 'src/app/database/drupal.sql' in the root directory and import it.

=> Admin credentials in case of importing the database:-
- username = salah
- password = asd12345


## Ports
Nginx => 8080
phpMyAdmin => 8081
