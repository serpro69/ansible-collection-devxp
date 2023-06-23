# ansible-collection-workstation

An ansible collection of roles that I use for setting up my workstations.

## Roles

- [`base`](roles/base) - a base role that ensures default system packages
- [`sdkman`](roles/sdkman) - installs [sdkman](https://sdkman.io/)

### Configurable Variables

See each role's individual `defaults/main.yml` file for a list of configurable variables

## Development

The following things need to be kept in mind when developing a new role or modifying existing one:

- all role variables (both `defaults` and `vars`) are prefixed with the role name, e.g. `base_packages`, `sdkman_dir`
  - "internal" (private) variables that shouldn't be exposed are additionally prefixed with `_`, e.g. `_sdkman_selfupdate`
- a role should usually contain molecule directory with tests for self targeting all supported OSes

