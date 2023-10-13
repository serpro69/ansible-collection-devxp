# `serpro69.workstation.app.appimage`

This role configures AppImage integration and installs some apps.

## Requirements

- jmespath (needed for [`community.general.json_query`](https://docs.ansible.com/ansible/latest/collections/community/general/json_query_filter.html#requirements) filter

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role using a playbook as follows:

```yaml
- name: Configure workstation
  hosts: localhost
  roles:
    - role: serpro69.workstation.app.appimage
    # other roles...
```
