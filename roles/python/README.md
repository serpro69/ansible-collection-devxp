# `serpro69.workstation.python`

This role installs python and adds optional virtualenv support.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.python
    # other roles...
```

Create virtual environments:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.python
      vars: 
        python_virtualenvs:
          - name: foo
            packages:
              - ansible
              - ansible-lint
          - name: bar
            
```

