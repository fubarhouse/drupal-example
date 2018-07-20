# Amazee.io Docker Development Boilerplate

Originally forked from the [official example for Drupal 8](https://github.com/amazeeio/drupal-example).

This documentation assumes you're familiar with the original project.

## Starting

Every time you need this, clone it into a new folder for the purposes of namespacing.

  1. Identify a short name for the Drupal site you'd like to make, for example, shortname.
  2. `git clone git@github.com:amazeeio/drupal-example.git ./shortname`
  3. `cd shortname`
  4. Find and replace all instances of `MYSITENAME` and change it to your `shortname` in `.lagoon.yml`, `docker-compose.yml` and `.dockerignore.yml`
  5. Load in your drush alias files into the drush folder.
  6. Run the commands listed below.
  7. You will be responsible for syncronising files and databases inside of the containers, you can find more about that process on the [drush commands website](https://drushcommands.com/).

```sh
$ composer install
$ pygmy start
$ docker-compose up
```

## Finishing

```sh
$ docker-compose down
$ docker-compose rm
$ pymgy down
```

## Notes

* This repository assumes multisite configuration, you can change that my switching out the appropraite paths in the above files to 'default'.
* This configuration is for Drupal 7 only, you can find configuration files in a [separate repository](https://github.com/fubarhouse/drupal-setting-files).
* This configuration assumes your composer file will build to the folder named `docroot`.
* This repository assumes experience with Ruby gems and Docker.
* This repository is basically a dumbed down version of the original so it can be more portable, structured well for Drupal 7 and to basically refresh my memory as required.
* This respository will not change, and provides no warranty.
