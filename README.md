# Nextcloud App Tutorial

[![PHPUnit GitHub Action](https://github.com/nextcloud/app-tutorial/workflows/PHPUnit/badge.svg)](https://github.com/nextcloud/app-tutorial/actions?query=workflow%3APHPUnit)
[![Node GitHub Action](https://github.com/nextcloud/app-tutorial/workflows/Node/badge.svg)](https://github.com/nextcloud/app-tutorial/actions?query=workflow%3ANode)
[![Lint GitHub Action](https://github.com/nextcloud/app-tutorial/workflows/Lint/badge.svg)](https://github.com/nextcloud/app-tutorial/actions?query=workflow%3ALint)

This is a syncthing integration for nextcloud

## Development progress / Goals

- [ ] API connection to syncthing
- [ ] Syncthing API php bindings
- [ ] Proof of concept
- [ ] Files sidebar tab
- [ ] Ability to create syncthing share in sidebar
- [ ] User settings
- [ ] Admin settings
- [ ] Install instructions

## Limitations

- Will not work with server side encryption
- Will not work with external storage
- Will not work on servers without the possibility to expose extra ports


## Development
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/JonathanTreffler/sharerenamer/)

It will automatically spin up and configure a full Nextcloud, MariaDB, PhpMyAdmin and syncthing server.

### Nextcloud Login:
**Username:** dev

**Password:** t2qQ1C6ktYUv7

### PhpMyAdmin Login:
**Username:** nextcloud

**Password:** wdGq73jQB0p373gLdf6yLRj5

### OCC
```bash
docker exec -it -u 33 gitpod_app_1 php occ
```

(It is fine to have these static logins, because gitpod has acess control built in and no sensitive data is stored in these dev servers)

## Try it 
To install it change into your Nextcloud's apps directory:

    cd nextcloud/apps

Then run:

    git clone https://github.com/JonathanTreffler/nextcloud-syncthing.git notestutorial

Then install the dependencies using:

    make composer

## Frontend development

The app tutorial also shows the very basic implementation of an app frontend using [Vue.js](https://vuejs.org/). To build the frontend code after doing changes to its source in `src/` requires to have Node and npm installed.

- 👩‍💻 Run `make dev-setup` to install the frontend dependencies
- 🏗 To build the Javascript whenever you make changes, run `make build-js`

To continuously run the build when editing source files you can make use of the `make watch-js` command.
