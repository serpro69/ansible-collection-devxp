# `serpro69.workstation.desktop.gnome`

This role configures the [gnome](https://www.gnome.org/) desktop environment with themes, tweaks, extensions and so on.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.desktop.gnome
    # other roles...
```

