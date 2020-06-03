# Development

This is my local development environment. Everything is managed by composer.

## Setup

1. `(cd support/vagrant && composer install) vagrant up`
2. go to `http://ibericode.wp.test/`


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