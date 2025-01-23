A simple Keycloak login theme which is used at Leipzig eSports e.V.

# Install

Opening this repository in VS Code allows you to make use of [Prettier](https://prettier.io/) for code formatting.
Install the [Prettier extension for VS Code](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode).
Run `npm install` in the root of this repository and code should be automatically formatted whenever you save a file.

This repository comes with a Docker Compose file that spins up a development instance of Keycloak.
Theme caching is enabled, so changes are instantly reflected in the user interface.
Run `docker compose up -d` and go to http://localhost:8080 to view the theme.
Keycloak will take a while to start up, so be patient.

# Deploy

Copy the [`les` theme directory](themes) to the theme directory of your production instance.
Themes can be applied per client, so go to the client whose login page you would like to change, scroll to "Login settings" in the "Settings" tab and pick the "les" theme in the "Login theme" dropdown.
If theme caching is enabled, you may need to delete it manually.
If running Keycloak in a container, delete the directory at `/opt/keycloak/data/tmp/kc-gzip-cache`.

# License

Apache 2.0.
