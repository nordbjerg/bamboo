## Bamboo

Proof of concept plug-and-play style modules for Laravel 4. The idea is to have a core (bamboo) which manages the modules; it enables them, it disables them and it loads them.

### What's planned?

#### Core

The core is in charge of managing the modules:

- The core detects new modules and runs the module's (optional) migrations.
- The core can load modules at run-time.
- The core can resolve module dependencies (i.e. an event module may depend on a user module).

#### Module

Each module is essentially a Laravel package. These packages can include (but are not required to):

- Controllers
- Routes
- Models
- Views
- Assets
- Migrations

Each module is required to have a service provider.

### Goals

- Clean, maintanable, and reusable code
- Very flexible modules; it should be possible to extend existing modules, and to create new complex ones (like a bulletin board module)
- It should be easy to install and remove modules (think 1. composer install 2. done)
