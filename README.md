# Ansible role to install NICE-DCV

Install Amazon NICE-DCV on a host.

## Requirements

Provisioning host:

- Ansible 2.15

Remote host:

- Ubuntu 22.04

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
