# `serpro69.workstation.helper.github.install_binary`

This is a helper role that is used to download and install pre-compiled application binaries (usually CLI tools) from a github repository releases.

## Variables

See [`defaults/main.yml`](defaults/main.yml).

## Examples

Run the role from another role as follows:

```yaml
- import_role:
    name: serpro69.workstation.helper.github.install_binary
  vars:
    repo: 'owner/repo'
    version: '1.2.3' # or 'latest'
    binaries_path: '/home/user/.local/bin/'
    man_path: '/usr/share/man/'
    completions_path: '/home/user/.redpill/completions/'
```

