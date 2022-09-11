# event_management

## Installation

- Paste the project files into a directory.
- At your project terminal which `docker-compose.yml` exist.
- Run `docker-compose up -d --build`.
- Run `composer install` in the src/app. This will download all the required packages for the platform, and add the map structure.
- Fill in your database credentials via the UI and install your drupal site. (this data will come from the docker container).
```
database_name: drupal
database_user: root
database_password: root
database_host: mysql      // The database container name
database_port: 3306
```
- In your settings.php, at the bottom add `$settings['config_sync_directory'] = 'sites/default/config/sync';`
- Run drush config-import -y to enable the required modules and import all configuration that comes with them

<br>

### If you have a problem with configs, please find the attached database 'database/drupal.sql' in the root directory and import it.

=> Admin credentials:-
- username = salah
- password = asd12345
