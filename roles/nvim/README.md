# `serpro69.workstation.nvim`

This role installs [neovim](https://neovim.io/) with some additional packages, and sets nvim as default alternative for `vim` and other similar commands.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.nvim
    # other roles...
```

