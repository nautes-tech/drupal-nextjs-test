# Drupal next test

A basic D9 installation configured to be a back-end site with JSON:API or [Drupal Next.js](https://next-drupal.org/).

[DDEV](https://ddev.readthedocs.io/en/stable/) is already configured but other local servers should work as well.

Basic [postman collection](https://documenter.getpostman.com/view/3589049/VVBavPsq)

## Setup

* `composer install`
* Import the db: `private-files/db/base-db.sql.gz`
* Extract the public files backup `private-files/public-files-bck/public-files.tar.gz` inside `web/sites/default/files`
* Empty the caches, e.g. `ddev drush cr`


### Admin access
```markdown
user: giuseppe.esposito@nautes.com
password: admin
```

### Drupal Next.js credentials

```markdown
# See https://next-drupal.org/docs/environment-variables

# Required
NEXT_PUBLIC_DRUPAL_BASE_URL=https://drupal-next-test.ddev.site
NEXT_IMAGE_DOMAIN=drupal-next-test.ddev.site

# Required for Preview Mode
DRUPAL_PREVIEW_SECRET=secret

# Authentication (Bearer)
DRUPAL_CLIENT_ID=73c0b99b-1a8c-4671-9790-836b915e59c6
DRUPAL_CLIENT_SECRET=secret

# Optional
DRUPAL_SITE_ID=next_js
DRUPAL_FRONT_PAGE=/node
```
