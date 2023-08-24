# `serpro69.workstation.base`

This role installs [node](https://nodejs.org/es) via one of supported node version manager tools.

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

