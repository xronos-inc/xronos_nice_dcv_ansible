# Ansible role to install NICE-DCV

Install Amazon NICE-DCV on a host.

Features:

- Installs NICE-DCV
- Creates a systemd service for managing xhost permissions
- Creates a systemd service for starting a user DCV session
- Optionally configures X11 for headless operation

This role installs systemd services for starting user DCV sessions at startup and supports multiple users.

## Requirements

Provisioning host:

- Ansible 2.15

Remote host:

- Ubuntu 22.04 or 24.04

## Example playbook

```yaml
- hosts: myhost
  gather_facts: true
  roles:
    - name: xronos_nice_dcv_ansible
      role: xronos_nice_dcv_ansible
```

After running, the following services should be running:

- NICE DCV: `[host or IP]:8443#`

## Variables

- `nice_dcv_major_version`: major version specifier to install (ex. `2024.0`). See [defaults/main.yml](defaults/main.yml) for the default value.
- `nice_dcv_build`: build number to install (ex `18131`). See [defaults/main.yml](defaults/main.yml) for the default value.
- `nice_dcv_headless`: configure X11 for a headless server.
