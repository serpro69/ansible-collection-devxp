# `serpro69.workstation.base`

This role installs [mozilla firefox](https://www.mozilla.org) application.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.app.firefox
    # other roles...
```
