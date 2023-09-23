# `serpro69.workstation.ansible`

This role sets up my [dotfiles](https://github.com/serpro69/dotfiles).

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.cli.dotfiles
    # other roles...
```
