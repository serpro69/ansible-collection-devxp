# `serpro69.workstation.lsp`

This role installs various language servers.

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

