# ansible-collection-devexp

An ansible collection for improved DEVelopment EXPerience. 

This collections contains roles and plugins that I use for setting up my development workstations. You may also want to check out my [ansible-ubuntu-workstation](https://github.com/serpro69/ansible-ubuntu-workstation) playbook that uses this collection for seting up Ubuntu-based workstations.

_NB! This collection is still in early development, and while I do test things and it should mostly work fine, there could be breaking changes between versions until initial stable release_

## Roles

- [`ansible`](roles/ansible) - installs [ansible](https://docs.ansible.com/ansible/latest/index.html) with some additional ansible-related packages
- [`base`](roles/base) - a base role that ensures default system packages
- [`docker`](roles/docker) - installs [docker](https://www.docker.com/)
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

## Testing

### Requirements

- molecule>=4.0.4
- [`molecule-plugins[docker]`](https://github.com/ansible-community/molecule-plugins)

To run tests for all roles: `molecule test`

To run tests only for certain roles, tags are used in the `converge.yml` playbook. Tests for given role(s) can be filtered out with: `ANSIBLE_RUN_TAGS='ansible,base' molecule test` or `molecule test -- --tags 'ansible,base'` (requires `molecule-plugins>=23.4.0` due to issue with tags which was fixed in [molecule-plugins/#120](https://github.com/ansible-community/molecule-plugins/pull/120))
