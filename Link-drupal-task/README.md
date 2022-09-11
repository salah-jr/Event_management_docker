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

<br>
<hr>

![Opera Snapshot_2022-09-12_013748_localhost](https://user-images.githubusercontent.com/26637798/189553924-76a3c603-6832-48d6-8e13-7ecb0667b7a8.png)
![Opera Snapshot_2022-09-12_013936_localhost](https://user-images.githubusercontent.com/26637798/189553926-7a27855d-4ab8-4cab-9ded-8c2d8a6045ac.png)
![Opera Snapshot_2022-09-12_013309_localhost](https://user-images.githubusercontent.com/26637798/189553927-e8bec178-c107-48e5-9993-3142f95ebbc1.png)
![Opera Snapshot_2022-09-12_013353_localhost](https://user-images.githubusercontent.com/26637798/189553928-6f04a0e9-26a5-44d1-871d-c492a6046cae.png)
![Opera Snapshot_2022-09-12_013419_localhost](https://user-images.githubusercontent.com/26637798/189553929-8cff1c02-10c0-4f29-8bf4-e266a8fdc814.png)
![Opera Snapshot_2022-09-12_013447_localhost](https://user-images.githubusercontent.com/26637798/189553931-85ffb48e-b483-44a3-a94e-c8ef379b6437.png)
![Opera Snapshot_2022-09-12_013549_localhost](https://user-images.githubusercontent.com/26637798/189553933-81707333-8d89-4adf-84a8-cb0591d6e920.png)
![Opera Snapshot_2022-09-12_013656_localhost](https://user-images.githubusercontent.com/26637798/189553936-47a20eed-981e-430e-82bd-fb2791111806.png)

