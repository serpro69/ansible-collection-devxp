# ansible-collection-workstation

An ansible collection of roles that I use for setting up my workstations.

_NB! This collection is still in early development, and while I do test things and it should mostly work fine, there could be breaking changes between versions until initial stable release_

## Roles

- [`base`](roles/base) - a base role that ensures default system packages
- [`sdkman`](roles/sdkman) - installs [sdkman](https://sdkman.io/)

_It is worth noting that all roles can be used independently of each other and there are no dependencies between individual roles._

### Configurable Variables

See each role's individual `defaults/main.yml` file for a list of configurable variables

## Supported OS

This collection currently supports the following operating systems:

- Ubuntu 20.04 (and derivatives)
- Ubuntu 22.04 (and derivatives)

If a given role has different support that the default mentioned above, this is will be noted in the role's readme file.

## Development

The following things need to be kept in mind when developing a new role or modifying existing one:

- all role variables (both `defaults` and `vars`) are prefixed with the role name, e.g. `base_packages`, `sdkman_dir`
  - "internal" (private) variables that shouldn't be exposed are additionally prefixed with `_`, e.g. `_sdkman_selfupdate`
- a role should usually contain molecule directory with tests for self targeting all supported OSes

