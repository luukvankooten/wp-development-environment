# Development

This is my local development environment. Everything is managed by composer.

## Setup

First copy to file `.env.example` to `.env`

One liner:

`$ cp .env.examaple .env`

Update the credentials.

### Vagrant 

1. `$ (cd support/vagrant && composer install && vagrant up)`
2. `$ open http://ibericode.wp.test/`

### PHP build in server

1. `$ composer install`
2. `$ php -S localhost:8080 -t ./www`
3. `$ open http://localhost:8080/`

One liner:

`$ composer install && php -S localhost:8080 -t ./www`

### Docker

Not added yet support planned. 
This a small idea to run PHP version 5.2 to latest php version and you could seamless test everything, and with different wordpress and mysql versions. Like a small local pipeline.

## Develop plugin

1. create new directory in `app/plugins/MY_COOL_NEW_PLUGIN`
2. Add a composer.json to the plugin with type `wordpress-plugin`

Example:
```json
{
  "name": "cool_name/cool_name",
  "type": "wordpress-plugin",
  ...
}
```
3. Add the module to composer.json
4. Run `composer require cool_name/cool_name dev-master`