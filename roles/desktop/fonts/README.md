# `serpro69.workstation.desktop.gnome`

This role installs various fonts for the user.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.desktop.fonts
    # other roles...
```

