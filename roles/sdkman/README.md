# `serpro69.workstation.sdkman`

This role installs and configures [sdkman](https://sdkman.io/)

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.sdkman
    # other roles...
```

Override default installation dir:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.sdkman
      vars: 
        sdkman_dir: /home/foo/sdk/sdkman
```

Do not modify dotfiles:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.sdkman
      vars: 
        sdkman_bashrc_path: ''
        sdkman_zshrc_path: ''
```
