# `serpro69.workstation.ansible`

This role installs flatpak and applications.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.app.flatpak
    # other roles...
```
