# `serpro69.workstation.ansible`

This role installs ansible.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.ansible
    # other roles...
```

Install to the 'foo' virtual environment

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.ansible
      vars:
        ansible_virtualenv: "{{ ansible_env.HOME }}/.virtualenvs/foo"
```
