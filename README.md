# Ansible Role: Apache

Installs and configures Apache webserver with PHP, composer & drush for Drupal usage.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_version: 7.2

    drush:
      install_path: "/usr/local/lib/drush"
      version: 8.8
      keep_updated: true
      composer_path: "/usr/local/bin/composer"
      path: "/usr/local/bin/drush"

    sites:
      qed42:
        docroot: "/var/www/html/qed42_v2/web"
        server_name: "qed42.d8"
      d8_dev:
        docroot: "/var/www/html/d8_dev/web"
        server_name: "dev.d8"

Feel free to alter the PHP version as per your aplication needs. `Sites` is an array in case you need to spin up multiple virtual host entries for your local instance(Was developed as a part of ansible container, so the folder paths that we see here are mounted on ansible containers from host machine).
