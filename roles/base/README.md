# `serpro69.workstation.base`

This role installs core packages. It should generally be run before any other roles in this collection, but is technically not a dependency for other roles.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.base
    # other roles...
```

Override additional packages with your own list:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.base
      vars: 
        base_additional_packages:
          - nano
```

